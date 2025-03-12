# HeyZack Brand Style Guide

## Table of Contents
1. [Brand Identity](#brand-identity)
2. [Typography](#typography)
3. [Color Palette](#color-palette)
4. [Logo](#logo)
5. [Visual Elements](#visual-elements)
6. [Application Guidelines](#application-guidelines)

## Brand Identity

HeyZack transforms the way we interact with our living spaces, creating a seamless bridge between human intention and environmental response. The brand embodies the feeling of being effortlessly understood and supported throughout your day. It's the comforting presence that anticipates needs, responds to natural conversation, and quietly enhances daily life without demanding attention.

The brand identity evokes a sense of ambient intelligence that feels both reassuringly familiar and subtly magical. It represents the moment when technology disappears and only the experience remains—where a simple "Hey Zack" initiates a frictionless connection to your environment. The visual language conveys this through a harmonious balance of warmth and precision, using fluid elements that suggest responsiveness alongside structured components that inspire confidence and trust.

Through every interaction, HeyZack aims to elicit a feeling of delightful simplicity—the emotional satisfaction that comes from being truly heard and understood without effort or frustration. The brand experience is designed to create moments of genuine connection, where technology enhances human experience rather than demanding adaptation to its limitations.

## Typography

### Font Family

The HeyZack brand uses a carefully selected typography system that combines the distinctive Brinnan font family for headings with widely available Google Fonts for body text and general content.

- **Heading Font**: Brinnan (Black, Bold, Light)
  - Used for all headings, titles, and display text
  - A premium font that gives the brand its distinctive character

- **Primary Body Font**: Space Grotesk
  - Google Fonts alternative: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk)
  - A modern geometric sans-serif with subtle technological character
  - Distinctive yet highly readable with a contemporary feel
  - Perfect balance of uniqueness and functionality
  - Complements the futuristic aspects of the HeyZack brand
  - Weights: Light (300), Regular (400), Medium (500)

- **Secondary Body Font**: Outfit
  - Google Fonts alternative: [Outfit](https://fonts.google.com/specimen/Outfit)
  - A clean, geometric sans-serif with modern proportions
  - Excellent readability with a touch of personality
  - Used for alternative applications or when Space Grotesk isn't optimal
  - Weights: Regular (400), Medium (500), and Light (300)

- **Monospace Font**: Roboto Mono
  - Google Fonts alternative: [Roboto Mono](https://fonts.google.com/specimen/Roboto+Mono)
  - Used for code displays, technical specifications, and tabular data
  - Weight: Regular (400)

### Typography Scale

#### Headings

| Style | Size/Line Height | Weight | Usage |
|-------|------------------|--------|-------|
| Heading 1 | 100px / 110% | Brinnan Black | Main page headings, hero sections |
| Heading 1 Small | 86px / 110% | Brinnan Black | Secondary hero headings |
| Heading 2 | 60px / 110% | Brinnan Black | Section headings |
| Heading 2 Small | 60px / 110% | Brinnan Light | Alternative section headings |
| Heading 3 | 36px / 120% | Brinnan Black | Subsection headings |
| Heading 4 | 32px / 120% | Brinnan Black | Card headings, feature titles |
| Heading 5 | 26px / 130% | Brinnan Black | Small section titles |
| Heading 6 | 20px / 160% | Brinnan Black | Minor headings, labels |

#### Body Text

| Style | Size/Line Height | Weight | Usage |
|-------|------------------|--------|-------|
| Body | 18px / 160% | Space Grotesk Regular (400) | Main paragraph text |
| Body Small | 16px / 160% | Space Grotesk Regular (400) | Secondary text, captions |
| Body Semibold | 18px / 160% | Space Grotesk Medium (500) | Emphasized text, quotes |
| Body Light | 18px / 160% | Space Grotesk Light (300) | Subtle text, secondary information |
| Monospace | 16px / 140% | Roboto Mono Regular (400) | Code, technical information |

### Typography Properties

- **Letter Spacing**: 
  - Headings: -0.02em
  - Body text: 0em (normal)
  - Monospace: 0em (normal)

- **Paragraph Spacing**: 
  - Headings: 0px
  - Body text: 16px (equivalent to one line)

- **Text Alignment**: 
  - Left-aligned by default
  - Center alignment for specific UI elements and short headings
  - Justified text should be avoided

- **Text Balance**: Enabled for improved readability

### Font Implementation

```html
<!-- Google Fonts Implementation -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500&family=Outfit:wght@300;400;500&family=Roboto+Mono&display=swap" rel="stylesheet">
```

```css
/* CSS Variables */
:root {
  --font-heading: 'Brinnan', sans-serif; /* Fallback to system sans-serif if Brinnan is unavailable */
  --font-body: 'Space Grotesk', 'Outfit', sans-serif;
  --font-mono: 'Roboto Mono', monospace;
}

/* Font Fallback Strategy */
body {
  font-family: var(--font-body);
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-heading);
}

code, pre, .monospace {
  font-family: var(--font-mono);
}
```

### Link Styles

| Style | Color | Usage |
|-------|-------|-------|
| Link White | White (#FFFFFF) | Links on dark backgrounds |
| Link Black | Black (#2E2D2C) | Links on light backgrounds |
| White Link With Opacity | White with reduced opacity | Secondary links on dark backgrounds |
| Black Link With Opacity | Black with reduced opacity | Secondary links on light backgrounds |

## Color Palette

### Primary Colors

- **Blue**
  - HEX: #243984
  - RGB: 36, 57, 132
  - CMYK: 100, 87, 11, 1
  - Usage: Primary brand color, main UI elements, buttons, accents

- **Pink**
  - HEX: #E82F89
  - RGB: 232, 47, 137
  - CMYK: 0, 90, 0, 0
  - Usage: Secondary brand color, highlights, call-to-action elements

### Secondary Colors

- **Black**
  - HEX: #2E2D2C
  - RGB: 46, 45, 44
  - CMYK: 0, 0, 0, 95
  - Usage: Text, icons, UI elements requiring high contrast

- **White**
  - HEX: #FFFFFF
  - RGB: 255, 255, 255
  - CMYK: 0, 0, 0, 0
  - Usage: Backgrounds, text on dark colors, UI elements

- **Grey**
  - HEX: #E9EDEF
  - RGB: 233, 237, 239
  - CMYK: 11, 5, 6, 0
  - Usage: Backgrounds, dividers, subtle UI elements

- **Light Yellow**
  - HEX: #FFF9E6
  - RGB: 255, 249, 230
  - Usage: Accent color, highlights, notifications, alert states

- **Paragraph**
  - HEX: #4A4A4A
  - RGB: 74, 74, 74
  - Usage: Body text color for optimal readability

### Gradients

The brand uses a series of carefully crafted gradients to create dynamic and modern visual effects. These gradients add depth, movement, and visual interest to the brand expression.

#### Primary Gradient
- **Colors**: Blue (#243984) to Pink (#E82F89)
- **Direction**: Horizontal (90°) or Vertical (180°)
- **Usage**: Primary buttons, key visual elements, hero sections
- **CSS**: `linear-gradient(90deg, #243984, #E82F89)`

#### Soft Gradient
- **Colors**: Light Blue (#3A4F9B) to Light Pink (#EC5FA3)
- **Direction**: Horizontal (90°)
- **Opacity**: 80%
- **Usage**: Secondary elements, backgrounds, cards
- **CSS**: `linear-gradient(90deg, rgba(58, 79, 155, 0.8), rgba(236, 95, 163, 0.8))`

#### Radial Gradient
- **Colors**: Pink (#E82F89) at center to Blue (#243984) at edges
- **Usage**: Highlights, focal points, interactive elements
- **CSS**: `radial-gradient(circle, #E82F89, #243984)`

#### Monochromatic Gradients
- **Blue Gradient**: Dark Blue (#1A2A63) to Blue (#243984)
- **Pink Gradient**: Dark Pink (#C41A70) to Pink (#E82F89)
- **Usage**: Section backgrounds, subtle UI elements

### Color Application

- Use blue as the dominant color for brand recognition
- Use pink as an accent color for emphasis and calls-to-action
- Maintain sufficient contrast between text and background colors
- Apply gradients sparingly to maintain visual hierarchy

## Logo

The HeyZack logo features a sleek and technological design where the stylized house subtly incorporates the letter Z, directly linking it to the brand's identity. This graphic approach reinforces the idea of connectivity and intelligence within the home.

### Logo Variations

- **Logomark**: The stylized "HZ" symbol that can be used independently
- **Logotype**: The full "HEYZACK" text treatment
- **Wordmark**: The complete logo with both the mark and type elements

### Logo Construction

The logo combines home and "ZACK" elements, creating a unified symbol that represents the smart home ecosystem. The construction follows precise geometric proportions with defined spacing around the elements.

### Safety Zone

A defined safety zone exists around the logo to ensure proper visibility and impact. No other graphic elements should intrude into this space. The safety zone is equal to the height of the "Z" in the logo on all sides.

### Logo Sizing

| Size | Dimensions | Usage |
|------|------------|-------|
| Large | 120px height minimum | Hero sections, splash screens |
| Medium | 80px height | Headers, footers |
| Small | 40px height minimum | Navigation, icons |

### Logo Color Applications

- **Full Color**: Primary application with blue and pink gradient
- **Monochrome**: Black (#1D1D1B) version for applications where color is not possible
- **Reversed**: White version for use on dark backgrounds

## Visual Elements

### Sound Wave

The sound wave is a signature visual element that symbolizes voice recognition and the direct activation of the system with the phrase "Hey Zack." This wave represents the precise moment when the user triggers the voice interface, establishing a visual link with the action of speaking.

#### Sound Wave Characteristics

- **Form**: Fluid, horizontal wave pattern with varying amplitudes
- **Color**: Blue to pink gradient, following the primary gradient specifications
- **Movement**: Subtle animation that suggests responsiveness and active listening
- **Dimensions**: Typically displayed with a 4:1 width-to-height ratio
- **Composition**: Multiple overlapping wave forms with varying opacity (60-100%)

#### Sound Wave Variations

1. **Active State**:
   - Higher amplitude
   - Brighter colors
   - Animated with gentle pulsing motion
   - Used when the system is actively listening

2. **Passive State**:
   - Lower amplitude
   - Subdued colors (60-80% opacity)
   - Minimal or no animation
   - Used as a visual indicator of voice capability

3. **Packaging Wave**:
   - Static representation
   - Full gradient colors
   - Positioned to flow across the package surface
   - Integrated with product imagery

#### Sound Wave Applications

- As a background element in marketing materials
- As an interactive element that responds to voice input
- As a decorative element that reinforces the brand's technological nature

### Animation Principles

When animating the sound wave or other brand elements:

- **Timing**: Smooth, fluid movements (0.2-0.5 seconds for UI elements)
- **Easing**: Use ease-in-out for natural movement
- **Purpose**: Animation should serve a functional purpose, not just decoration
- **Subtlety**: Keep animations subtle and unobtrusive
- **Consistency**: Maintain consistent animation patterns throughout the experience

## Application Guidelines

### Cross-Media Implementation

#### Digital Applications
- **Web**:
  - Use SVG format for all logo and icon elements
  - Implement responsive design principles
  - Utilize subtle animations for interactive elements
  - Apply accessibility standards for all content

- **Mobile**:
  - Optimize typography for smaller screens
  - Increase touch targets to minimum 44px × 44px
  - Maintain brand colors with appropriate contrast ratios
  - Simplify complex gradients for performance

- **Voice Interfaces**:
  - Incorporate sound wave visualization during voice interactions
  - Use animation to indicate listening and processing states
  - Apply consistent audio cues and feedback

#### Print Applications
- **Marketing Materials**:
  - Use CMYK color values for accurate reproduction
  - Maintain minimum logo size of 0.75 inches (19mm) in width
  - Apply gradients strategically as focal points
  - Ensure 300 DPI minimum resolution for all brand assets

- **Packaging**:
  - Feature the sound wave prominently as a key visual element
  - Use soft-touch finishes on gradient areas for tactile quality
  - Apply spot UV on logo elements for dimensional contrast
  - Maintain consistent color application across different materials

- **Environmental**:
  - Scale logo appropriately for viewing distance
  - Use simplified versions for very small applications
  - Consider material properties when applying gradients
  - Maintain clear space proportional to implementation size

### Responsive Design

- **Breakpoints**:
  - Large (L): 1280px minimum width
  - Medium (M): 768px to 1279px
  - Small (S): 320px to 767px

- **Typography Scaling**: Maintain proper hierarchy across all device sizes
- **Logo Scaling**: Ensure the logo remains clear and recognizable at all sizes
- **Touch Targets**: Minimum 44px × 44px for interactive elements on touch devices

### Accessibility

- Maintain WCAG AA compliance for color contrast
- Ensure text remains legible at specified sizes
- Provide alternative text for all visual elements
- Design with keyboard navigation in mind

### Brand Expression

1. Always maintain the proper proportions of the logo
2. Respect the safety zone around the logo
3. Use the specified typography for consistent brand communication
4. Apply the color palette as defined to maintain brand recognition
5. Incorporate the sound wave element when representing voice activation features
6. When scaling the logo, ensure that the smallest elements remain visible and clear
7. For digital applications, use vector formats to maintain quality at any size
8. Apply the gradient consistently in the specified directions

---

*HeyZack Brand Identity - Version 1.1*
