graph TD
    subgraph "Smart Home Page Content Model"
    
    subgraph "Hero Section"
    SH[Hero] --> SH1["Headline (8-10 words)"]
    SH1 --> SH1a["'Intelligence That Lives With You'"]
    SH --> SH2["Subheadline (15-20 words)"]
    SH2 --> SH2a["Experience comfort, security, and efficiency in every moment of your day"]
    SH --> SH3["Visual"]
    SH3 --> SH3a["Modern home interior with highlighted smart features"]
    SH --> SH4["Animation"]
    SH4 --> SH4a["Day-to-night transition showing automation"]
    SH --> SH5["CTA"]
    SH5 --> SH5a["'Explore Products' button in accent orange"]
    end
    
    subgraph "Daily Timeline Experience Section"
    ST[Timeline] --> ST1["Layout"]
    ST1 --> ST1a["Horizontal timeline on desktop"]
    ST1 --> ST1b["Vertical timeline on mobile"]
    
    ST --> ST2["Morning Routine (6:45 AM)"]
    ST2 --> ST2a["Time indicator"]
    ST2 --> ST2b["Scene image"]
    ST2 --> ST2c["Scenario description (30-40 words)"]
    ST2 --> ST2d["Active systems icons"]
    ST2 --> ST2e["Voice command example"]
    
    ST --> ST3["Departure (8:00 AM)"]
    ST3 --> ST3a["Time indicator"]
    ST3 --> ST3b["Scene image"]
    ST3 --> ST3c["Scenario description (30-40 words)"]
    ST3 --> ST3d["Active systems icons"]
    ST3 --> ST3e["Voice command example"]
    
    ST --> ST4["Remote Control (12:30 PM)"]
    ST4 --> ST4a["Time indicator"]
    ST4 --> ST4b["Scene image"]
    ST4 --> ST4c["Scenario description (30-40 words)"]
    ST4 --> ST4d["Active systems icons"]
    ST4 --> ST4e["Voice command example"]
    
    ST --> ST5["Return Home (5:30 PM)"]
    ST5 --> ST5a["Time indicator"]
    ST5 --> ST5b["Scene image"]
    ST5 --> ST5c["Scenario description (30-40 words)"]
    ST5 --> ST5d["Active systems icons"]
    ST5 --> ST5e["Voice command example"]
    
    ST --> ST6["Evening (7:00 PM)"]
    ST6 --> ST6a["Time indicator"]
    ST6 --> ST6b["Scene image"]
    ST6 --> ST6c["Scenario description (30-40 words)"]
    ST6 --> ST6d["Active systems icons"]
    ST6 --> ST6e["Voice command example"]
    
    ST --> ST7["Night (10:30 PM)"]
    ST7 --> ST7a["Time indicator"]
    ST7 --> ST7b["Scene image"]
    ST7 --> ST7c["Scenario description (30-40 words)"]
    ST7 --> ST7d["Active systems icons"]
    ST7 --> ST7e["Voice command example"]
    
    ST --> ST8["Animation"]
    ST8 --> ST8a["Timeline scrolling with active section highlight"]
    ST8 --> ST8b["Scene transitions"]
    ST8 --> ST8c["Icon animations for active systems"]
    end
    
    subgraph "Smart Home Components Section"
    SC[Components] --> SC1["Layout"]
    SC1 --> SC1a["Filterable grid layout"]
    
    SC --> SC2["Filter Categories"]
    SC2 --> SC2a["Control Panels"]
    SC2 --> SC2b["Sensors & Detectors"]
    SC2 --> SC2c["Security Devices"]
    SC2 --> SC2d["Climate Control"]
    SC2 --> SC2e["Lighting Solutions"]
    
    SC --> SC3["Component Card"]
    SC3 --> SC3a["Product image"]
    SC3 --> SC3b["Product name"]
    SC3 --> SC3c["Brief description (20-30 words)"]
    SC3 --> SC3d["Key specifications"]
    SC3 --> SC3e["Price indicator"]
    SC3 --> SC3f["'Shop Now' link"]
    
    SC --> SC4["Animation"]
    SC4 --> SC4a["Filter transition effects"]
    SC4 --> SC4b["Card hover effects"]
    SC4 --> SC4c["Quick view modal"]
    end
    
    subgraph "Package Solutions Section"
    SP[Packages] --> SP1["Layout"]
    SP1 --> SP1a["Card-based comparison"]
    
    SP --> SP2["Starter Package Card"]
    SP2 --> SP2a["Package name & icon"]
    SP2 --> SP2b["Price"]
    SP2 --> SP2c["Component checklist"]
    SP2 --> SP2d["Key benefits (3-4 bullet points)"]
    SP2 --> SP2e["'Customize' button"]
    SP2 --> SP2f["'Buy Now' button"]
    
    SP --> SP3["Comfort Package Card"]
    SP3 --> SP3a["Package name & icon"]
    SP3 --> SP3b["Price"]
    SP3 --> SP3c["Component checklist"]
    SP3 --> SP3d["Key benefits (3-4 bullet points)"]
    SP3 --> SP3e["'Customize' button"]
    SP3 --> SP3f["'Buy Now' button"]
    
    SP --> SP4["Security Package Card"]
    SP4 --> SP4a["Package name & icon"]
    SP4 --> SP4b["Price"]
    SP4 --> SP4c["Component checklist"]
    SP4 --> SP4d["Key benefits (3-4 bullet points)"]
    SP4 --> SP4e["'Customize' button"]
    SP4 --> SP4f["'Buy Now' button"]
    
    SP --> SP5["Complete Home Package Card"]
    SP5 --> SP5a["Package name & icon"]
    SP5 --> SP5b["Price"]
    SP5 --> SP5c["Component checklist"]
    SP5 --> SP5d["Key benefits (3-4 bullet points)"]
    SP5 --> SP5e["'Customize' button"]
    SP5 --> SP5f["'Buy Now' button"]
    
    SP --> SP6["Animation"]
    SP6 --> SP6a["Comparison highlight effects"]
    SP6 --> SP6b["Savings callout animation"]
    end
    
    subgraph "Installation & Setup Section"
    SI[Installation] --> SI1["Layout"]
    SI1 --> SI1a["Step-by-step process visualization"]
    
    SI --> SI2["Content"]
    SI2 --> SI2a["Process timeline"]
    SI2 --> SI2b["Installation steps (4-5 steps)"]
    SI2 --> SI2c["Mobile app screenshots"]
    SI2 --> SI2d["Support options"]
    SI2 --> SI2e["Guarantee information"]
    
    SI --> SI3["Animation"]
    SI3 --> SI3a["Sequential step reveal"]
    SI3 --> SI3b["App interface demonstrations"]
    end
    
    subgraph "User Experience Stories Section"
    SU[User Stories] --> SU1["Layout"]
    SU1 --> SU1a["Testimonial carousel"]
    
    SU --> SU2["Content per slide"]
    SU2 --> SU2a["User photo/video"]
    SU2 --> SU2b["Before/after scenario"]
    SU2 --> SU2c["Quoted feedback (40-50 words)"]
    SU2 --> SU2d["Specific benefits highlighted"]
    SU2 --> SU2e["User name and location"]
    
    SU --> SU3["Animation"]
    SU3 --> SU3a["Carousel transitions"]
    SU3 --> SU3b["Video player controls"]
    end
    
    subgraph "Voice Control & Integration Section"
    SV[Voice & Integration] --> SV1["Layout"]
    SV1 --> SV1a["Icon grid with information panels"]
    
    SV --> SV2["Content"]
    SV2 --> SV2a["Compatible systems icons"]
    SV2 --> SV2b["Voice command examples"]
    SV2 --> SV2c["Integration diagram"]
    SV2 --> SV2d["QR code for compatibility guide"]
    
    SV --> SV3["Animation"]
    SV3 --> SV3a["Voice command visualization"]
    SV3 --> SV3b["Integration connection animations"]
    end
    
    subgraph "Shop & Support CTAs Section"
    SS[Shop & Support] --> SS1["Layout"]
    SS1 --> SS1a["Split layout"]
    
    SS --> SS2["Shop Column"]
    SS2 --> SS2a["Heading"]
    SS2 --> SS2b["Product categories links"]
    SS2 --> SS2c["Featured product"]
    SS2 --> SS2d["'Shop All Products' button"]
    
    SS --> SS3["Support Column"]
    SS3 --> SS3a["Heading"]
    SS3 --> SS3b["Support options (chat, phone, email)"]
    SS3 --> SS3c["Knowledge base link"]
    SS3 --> SS3d["Warranty information"]
    
    SS --> SS4["Animation"]
    SS4 --> SS4a["Subtle CTA hover effects"]
    SS4 --> SS4b["Icon animations"]
    end
    
    end
