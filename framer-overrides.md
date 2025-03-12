# HeyZack Brand - Creative Framer Implementations

Based on the HeyZack brand guidelines and styling document, here are three innovative ways to leverage Framer's code override capabilities to enhance user experience through the sound wave and other brand elements.

## 1. Voice-Responsive Sound Wave Animation

The sound wave is a signature visual element of the HeyZack brand, representing the moment when a user activates the voice interface. We can bring this to life using Framer's code overrides to create a realistic voice-responsive animation.

### Implementation

```tsx
// Voice-Responsive Sound Wave Override
export function VoiceWaveAnimation(): Override {
  const [isListening, setIsListening] = useState(false);
  const [amplitude, setAmplitude] = useState(0);
  
  // Audio processing simulation
  function processVoiceInput(level) {
    setAmplitude(Math.min(1, level * 1.5));
  }
  
  // Setup microphone access and processing
  useEffect(() => {
    if (!isListening) return;
    
    let animationFrame;
    let analyser;
    let dataArray;
    
    navigator.mediaDevices.getUserMedia({ audio: true })
      .then(stream => {
        const audioContext = new AudioContext();
        const source = audioContext.createMediaStreamSource(stream);
        analyser = audioContext.createAnalyser();
        analyser.fftSize = 32;
        
        source.connect(analyser);
        dataArray = new Uint8Array(analyser.frequencyBinCount);
        
        function updateAmplitude() {
          analyser.getByteFrequencyData(dataArray);
          
          // Get average amplitude
          const average = dataArray.reduce((sum, value) => sum + value, 0) / dataArray.length;
          processVoiceInput(average / 255);
          
          animationFrame = requestAnimationFrame(updateAmplitude);
        }
        
        updateAmplitude();
      });
      
    return () => {
      cancelAnimationFrame(animationFrame);
      if (analyser) analyser.disconnect();
    };
  }, [isListening]);
  
  return {
    // Connect to Hey Zack activation trigger
    onTap: () => setIsListening(!isListening),
    variants: {
      passive: { 
        opacity: 0.7,
        scale: 1
      },
      active: { 
        opacity: 1,
        scale: 1 + (amplitude * 0.15)
      }
    },
    initial: "passive",
    animate: isListening ? "active" : "passive",
    style: {
      background: `linear-gradient(90deg, #243984, #E82F89 ${50 + amplitude * 50}%)`,
    },
    transition: {
      type: "spring",
      mass: 0.5,
      stiffness: 100,
      damping: 15
    }
  };
}
```

### User Experience Enhancement

This implementation creates a sound wave that:

1. **Responds to actual voice input** by analyzing audio through the Web Audio API
2. **Visualizes speech patterns** by modulating wave amplitude and gradient positions
3. **Adheres to brand guidelines** by using the primary blue-to-pink gradient
4. **Provides visual feedback** during voice interaction, making the interface feel alive and responsive

This creates a direct visual connection between the user's voice and the HeyZack brand, reinforcing the "seamless bridge between human intention and environmental response" described in the brand identity.

## 2. Ambient Gradient Wave Background

Create an immersive, subtle background that uses the brand's gradient colors to create a gentle, flowing wave effect that responds to user interactions and system state changes.

### Implementation

```tsx
// Ambient Gradient Wave Background
export function AmbientWave(): Override {
  // Track scrolling, mouse movement, and system state
  const [scrollY, setScrollY] = useState(0);
  const [mousePosition, setMousePosition] = useState({ x: 0, y: 0 });
  const [systemActivity, setSystemActivity] = useState(0);
  
  // Update state based on user interactions
  useEffect(() => {
    const handleScroll = () => setScrollY(window.scrollY);
    const handleMouseMove = (e) => {
      setMousePosition({
        x: e.clientX / window.innerWidth,
        y: e.clientY / window.innerHeight
      });
    };
    
    // Simulate system activity (would connect to actual system in production)
    const activityInterval = setInterval(() => {
      setSystemActivity(Math.random() * 0.3);
    }, 5000);
    
    window.addEventListener("scroll", handleScroll);
    window.addEventListener("mousemove", handleMouseMove);
    
    return () => {
      window.removeEventListener("scroll", handleScroll);
      window.removeEventListener("mousemove", handleMouseMove);
      clearInterval(activityInterval);
    };
  }, []);
  
  // Create three overlapping wave layers with different movement patterns
  return {
    children: (
      <>
        <Frame
          size="400%"
          radius="50%"
          background="linear-gradient(135deg, #243984 0%, #3A4F9B 100%)"
          opacity={0.15 + (systemActivity * 0.2)}
          style={{ mixBlendMode: "multiply" }}
          animate={{
            x: -1000 + (mousePosition.x * 200),
            y: -900 + (scrollY * 0.05),
            rotate: 10 + (scrollY * 0.01)
          }}
          transition={{ duration: 3 }}
        />
        <Frame
          size="300%"
          radius="50%"
          background="linear-gradient(135deg, #E82F89 0%, #EC5FA3 100%)"
          opacity={0.15 + (systemActivity * 0.1)}
          style={{ mixBlendMode: "multiply" }}
          animate={{
            x: -500 - (mousePosition.x * 100),
            y: -600 - (scrollY * 0.03),
            rotate: -15 - (scrollY * 0.02)
          }}
          transition={{ duration: 4 }}
        />
        <Frame
          size="350%"
          radius="50%"
          background="radial-gradient(circle, #E82F89 0%, #243984 80%)"
          opacity={0.1 + (systemActivity * 0.05)}
          style={{ mixBlendMode: "overlay" }}
          animate={{
            x: -750 + (mousePosition.y * 150),
            y: -750 + (scrollY * 0.02),
            rotate: 20 - (scrollY * 0.015)
          }}
          transition={{ duration: 5 }}
        />
      </>
    )
  };
}
```

### User Experience Enhancement

This ambient background creates:

1. **Environmental awareness** by subtly responding to user scrolling and mouse movements
2. **System connection** by reflecting system activity (could connect to actual smart home events)
3. **Spatial depth** through layered elements with different movement patterns
4. **Brand immersion** using all the gradient types defined in the brand guidelines

The effect creates an "ambient intelligence" feel that aligns perfectly with the brand identity's emphasis on technology that "quietly enhances daily life without demanding attention."

## 3. Contextual Micro-Interaction System

Create a system of subtle micro-interactions that respond to voice commands, providing consistent feedback across the interface while maintaining the brand's visual language.

### Implementation

```tsx
// Contextual Micro-Interaction System
export function ContextualFeedback(): Override {
  // Track interaction state with multiple stages
  const [interactionState, setInteractionState] = useState("idle");
  const [confidence, setConfidence] = useState(0);
  const [commandCategory, setCommandCategory] = useState(null);
  
  // Simulated voice command processing
  function processCommand(command) {
    // Simulate processing stages
    setInteractionState("listening");
    
    setTimeout(() => {
      setInteractionState("processing");
      
      // Analyze command and set category
      if (command.includes("light") || command.includes("brightness")) {
        setCommandCategory("lighting");
        setConfidence(0.95);
      } else if (command.includes("temperature") || command.includes("heat")) {
        setCommandCategory("climate");
        setConfidence(0.85);
      } else {
        setCommandCategory("general");
        setConfidence(0.75);
      }
      
      setTimeout(() => {
        setInteractionState("confirming");
        
        setTimeout(() => {
          setInteractionState("executing");
          
          setTimeout(() => {
            setInteractionState("completed");
            
            setTimeout(() => {
              setInteractionState("idle");
              setCommandCategory(null);
            }, 2000);
          }, 1000);
        }, 1000);
      }, 1000);
    }, 1500);
  }
  
  // Color mappings based on command category
  const categoryColors = {
    lighting: {
      primary: "#E82F89",
      secondary: "#EC5FA3"
    },
    climate: {
      primary: "#243984",
      secondary: "#3A4F9B"
    },
    general: {
      primary: "#243984",
      secondary: "#E82F89"
    }
  };
  
  // Get current colors based on category
  const currentColors = commandCategory 
    ? categoryColors[commandCategory]
    : categoryColors.general;
  
  // Visual states based on interaction stage
  const variants = {
    idle: {
      scale: 1,
      opacity: 0.6,
      background: "linear-gradient(90deg, #243984, #E82F89)"
    },
    listening: {
      scale: [1, 1.05, 1, 1.05, 1],
      opacity: 0.8,
      background: `linear-gradient(90deg, ${currentColors.primary}, ${currentColors.secondary})`,
      transition: {
        scale: {
          repeat: Infinity,
          duration: 1.5
        }
      }
    },
    processing: {
      scale: 1,
      opacity: 1,
      background: `linear-gradient(90deg, ${currentColors.primary}, ${currentColors.secondary})`,
      rotate: [0, 360],
      transition: {
        rotate: {
          repeat: Infinity,
          duration: 2,
          ease: "linear"
        }
      }
    },
    confirming: {
      scale: [1, 1 + (confidence * 0.1)],
      opacity: confidence,
      background: `linear-gradient(90deg, ${currentColors.primary}, ${currentColors.secondary})`
    },
    executing: {
      scale: 1.1,
      opacity: 1,
      background: `linear-gradient(90deg, ${currentColors.primary}, ${currentColors.secondary})`
    },
    completed: {
      scale: [1.1, 1],
      opacity: [1, 0.6],
      background: `linear-gradient(90deg, ${currentColors.primary}, ${currentColors.secondary})`
    }
  };
  
  return {
    onTap: () => processCommand("Turn on the lights in the living room"),
    variants,
    animate: interactionState,
    transition: {
      type: "spring",
      duration: 0.5
    }
  };
}
```

### User Experience Enhancement

This micro-interaction system provides:

1. **Contextual feedback** that adapts to different voice command categories
2. **Confidence visualization** showing the system's understanding level
3. **Process transparency** by visualizing all stages of command processing
4. **Category-specific colors** that maintain brand consistency while providing context

The system creates a cohesive interaction language that extends across the interface, reinforcing the brand promise of "delightful simplicity" and "being truly heard and understood."

---

## Implementation Recommendations

To integrate these Framer overrides into the HeyZack website or application:

1. **Layer the experiences** - Use the ambient background subtly throughout the site, with the more interactive elements appearing during specific interactions

2. **Maintain performance** - Implement CPU/GPU optimizations like:
   - Limiting animation scope to visible viewport
   - Using `will-change` properties for hardware acceleration
   - Throttling event listeners on scroll and mouse movement

3. **Progressive enhancement** - Ensure core functionality works without these enhancements, adding them when browser capabilities permit

4. **Accessibility considerations** - Provide alternative feedback methods alongside these visual enhancements:
   - Include text status updates alongside animations
   - Ensure animations respect reduced-motion preferences
   - Maintain sufficient contrast ratios during all animation states

By implementing these creative Framer overrides, the HeyZack brand can create a digital experience that embodies its identity as a seamless bridge between human intention and environmental response.
