# UI Design Brief - Interactive Art Diary Platform

**Project:** Interactive Digital Experience for Illustrated Diary Collection  
**Brief Type:** Front-End User Interface Design  
**Target:** Creative professionals, design teams, and developers  
**Scope:** Gallery, individual artwork pages, and core interactive elements

---

## Project Vision

**Seven years ago, financial disaster and digital addiction brought a fledgling artist to rock bottom. The solution? An illustrated diary practice that evolved into a systematic innovation for processing human experience. Now, 50+ artworks (ranging from A4 - 1.5 meters) documenting this transformation are ready for their digital debut—and they need an interface worthy of their extraordinary content.**

Transform a deeply personal illustrated diary practice into an immersive digital experience that feels like **"audiobook meets art gallery"** rather than a conventional website or app. The interface should honor the intimate, handcrafted nature of the physical artworks while enabling sophisticated digital interaction.

This is not a typical web project—it's an art installation that happens to live online.

---

## Project Impact & Timeline

### **Cultural Significance**

A format that could redefine how audiences interact with visual storytelling and personal documentation. The work documents a complete personal transformation through systematic artistic practice—creating a new model for how art can serve as both therapy and innovation.

### **Launch Strategy**

- **Gallery exhibitions** featuring the physical artworks alongside digital experience
- **Media debut** with planned features on Hacker News and art/technology publications
- **Academic interest** from researchers studying memory, creativity, and digital storytelling
- **Timeline:** Exhibition launch targeted for Q1 2026

### **Portfolio Value**

This project will be widely exhibited and covered, offering designers the opportunity to showcase work that bridges fine art, interactive technology, and innovative user experience design at the highest level.

---

## Core Design Philosophy

### **Art-First, Technology-Second**

The physical artworks (some reaching 1.5 meters) are significant large-scale works that deserve gallery-quality presentation. The digital interface should feel like a natural extension of the art experience, not a tech overlay imposed upon it (unless you can make the tech overlay ridiculously dope ;).

### **Intimate Transparency**

The project reveals unprecedented intimacy—detailed time data showing how each day was spent (pie charts, timetables, activity breakdowns), audio narration of personal visions, memory palace techniques. The UI should complement this intimacy with style and elegance or tech wizardness.

### **Multiple Viewing Modes**

Support fundamentally different ways of experiencing the work:

- **Narration Mode:** Audio-guided exploration with visual hotspots, pop-up images/videos, and links
- **Silent Mode:** Visual hotspots with pop-up images/videos (silent), links, and optional text overlays
- **Plain Viewing:** Pure art appreciation without any interface elements

---

## User Experience Principles

### **Progressive Revelation**

Not every visitor needs every feature immediately. Design for graceful layering:

- Casual browsers can enjoy the art visually
- Curious users discover interactive elements naturally
- Committed explorers unlock deep narrative content

### **Respectful Engagement**

The content deals with deep personal transformation (and epic tomfoolery). Avoid gamification, achievement badges, or aggressive social prompts that would cheapen the experience. Think museum, not social media. However, tasteful hotspot sharing functionality is desired for users who want to share specific moments.

### **Exceptional Cross-Device Experience**

The interface must excel across all device sizes, recognizing that larger screens reveal more of the artwork's intricate magic. While many users will discover the work on mobile devices, the experience should scale beautifully to tablets and desktops where the full detail and scale of the pieces can be appreciated. Additional considerations include gallery/exhibition contexts where QR codes link directly to specific artworks on mobile devices.

---

## Key Interface Challenges

### **Hotspot Interaction Design**

**The Core Problem:** How do you make clickable areas on detailed artwork feel natural rather than intrusive?

**Technical Context:** SVG coordinates define hotspot areas on all devices. Desktop gets hover state enhancements (previews, stylish highlighting), mobile/tablet uses tap interactions exclusively.

**Critical Behavior:** When a hotspot is selected and playing, it must remain highlighted until the user:

- Completes the narration (auto-advance switched off)
- Clicks another hotspot
- Stops playback manually
- Auto-advances to next hotspot (in sequential mode)

Users can scroll/pan across the image while a hotspot is highlighted and playing—the selection persists through navigation.

**Design Opportunity:** Create hotspot indicators that feel integrated with the artistic language. Consider the satisfying, tactile quality of archival microfilm readers or futuristic document exploration interfaces. Consider audio feedback (subtle clicks or sounds) as users rollover hotspots to create engaging tactile feedback.

### **Audio Player Integration**

**The Core Problem:** Audio narration is central to the experience, but traditional media players may not suit this context.

**Desktop vs Mobile Considerations:** Desktop allows for floating/overlay approaches with more visual real estate. Mobile/tablet may require different positioning and sizing strategies.

**Required Functionality Beyond Standard Players:**

- Time scroll through hotspot dates
- Sequential vs Highlights mode toggle
- Journey selection (future feature)
- Auto-advance toggle
- Minimize/expand functionality
- Current hotspot/date display

_For detailed audio player specifications, interaction states, and overlay behaviors, see ui-features in the project assets._ *linked here* - *[UI Features](4-diagrams/ui-features.md)*


**Design Opportunity:** Design an interface that complements the artwork. Consider premium audiobook aesthetics, glassmorphism effects (though contrast with black/white artwork may be challenging), or organic solutions alongside technical ones.

### **Access Level Visualization**

**The Core Problem:** Content has different access levels but heavy-handed gates would destroy the artistic flow.

**Current Launch Reality:** One free piece (Magic Piece), all others email-gated. Future supporter tier functionality planned.

_Complete user flow for access level transitions is mapped in Access Gating Flow Chart v2.pdf (see project assets)._ *linked here - [Access Gating Flow](../4-diagrams/access-gating-flow-diagram.md)

**Design Opportunity:** Develop elegant ways to communicate access prompts that feel like stepping behind the curtain, not hitting a paywall. Communicate value for the user's attention rather than imposing aggressive gates.

---

## Website-Wide Design System

### **Visual Identity & Aesthetic Direction**

**Design Exploration Approach:** We encourage creative proposals that surprise us with novel approaches to presenting this unique content. However, we'd like to see at least one design proposition that explores black backgrounds with a minimal aesthetic approach.

**Our Intuitions (Not Requirements):**

- **Black backgrounds** around artworks may provide superior contrast with the black ink drawings
- **White/light gray** text tends to work well for readability
- **Selective accent colors** for interactive states help guide user attention
- Competing color schemes might distract from the monochromatic artwork, but we're open to being proven wrong

**Typography System:**

- **Well-chosen fonts** that complement but don't compete with the handwritten diary content
- **Scalable across devices** while maintaining artistic integrity

### **Site-Wide Navigation & Structure**

**Global Navigation Requirements:**

- **Landing/Home page** with compelling entry points to the diary experience (Note: We're also developing a separate scrolling homepage story experience that may complement or replace the traditional landing page approach)
- **Gallery page** showing all artworks with act-based organization (Prequel, Initiation, Devotion, Transformation)
- **Individual artwork pages** (the core interactive experience detailed elsewhere in this brief)
- **Supporting pages:** About, Tutorials, Music, Shop (future)

*Complete site architecture and page relationships are detailed in Site Map.pdf (see project assets). linked here - [Site Map](../4-diagrams/site-map.md)

**Navigation Patterns:**

- **Hamburger menu system** for clean, uncluttered presentation
- **Breadcrumb or contextual navigation** showing user's location within the chronological journey
- **Easy access** between gallery overview and individual pieces
- **Deep linking capability** for sharing specific artworks or hotspots

### **Page Design Specifications**

**Landing Page:**

- **Compelling introduction** to the project and transformation story
- **Clear entry points** to different ways of experiencing the work (chronological, highlights, magic piece)
- **Visual preview** that hints at the artwork quality without overwhelming
- **Minimal barriers** to exploration while setting appropriate expectations
- (May be complemented by or integrated with planned scrolling story experience)

**Gallery Page:**

- **Act-based organization** with clear visual hierarchy (Prequel → Initiation → Devotion → Transformation)
- **Thumbnail presentation** that respects the artwork while providing clear navigation

**Individual Artwork Pages:**

- **Background approach** that maximizes artwork contrast (we suspect black backgrounds may work best, but open to other solutions)
- **Unobtrusive UI elements** that don't compete with the artwork when not needed
- **Responsive scaling** that honors the artwork at all screen sizes
- **Audio player integration** that feels natural to the overall design system

### **Interactive Elements & Components**

**Button Design:**

- **Elegant, understated styling** that complements the artistic content
- **Clear interactive states** (hover, active, disabled) appropriate for both desktop and mobile
- **Consistent styling** across all site functions while allowing for contextual variations

**Form Elements:**

- **Email capture interfaces** that feel like invitations rather than barriers
- **Clean, minimal styling** that maintains the gallery aesthetic
- **Error states and validation** that don't break the contemplative mood

**Loading & Transition States:**

- **Smooth, purposeful animations** that enhance rather than distract from the art viewing experience
- **Loading patterns** appropriate for high-resolution artwork
- **Page transitions** that maintain continuity, especially between diary pieces (consider book-flipping effects for Acts I & II)

### **Content Presentation Patterns**

**Text Overlays & Panels:**

- **Readable but unobtrusive** styling for about text, transcripts, and metadata
- **Consistent panel designs** for image overlays, link collections, and additional content
- **Mobile-optimized layouts** that work within limited screen space

**Data Visualization:**

- **Time data presentations** that match the overall visual design rather than looking like they came from a different application
- **Chart and graph styling** (if using CSV data dynamically) that complements the overall aesthetic
- **Any interactive time data visualizations** (if using CSV data dynamically) should maintain the contemplative mood of the overall experience

### **Responsive Design Philosophy**

**Device-Specific Considerations:**

- **Desktop:** Full gallery experience with hover states, floating elements, and maximum artwork detail
- **Tablet:** Balanced approach maintaining visual impact while optimizing for touch interaction
- **Mobile:** Streamlined but complete experience, ensuring all functionality remains accessible and elegant

**Breakpoint Strategy:**

- **Content-first responsive design** that prioritizes artwork presentation at all sizes
- **Navigation adaptation** that maintains easy access to all site functions
- **Typography scaling** that preserves readability and hierarchy across devices

### **Brand Consistency Notes**

The visual design should reinforce that this is:

- **Fine art documentation,** not casual blogging or social media
- **Professional exhibition material,** worthy of gallery and academic contexts
- **Personal storytelling,** maintaining intimacy despite public presentation
- **Innovative digital experience,** pushing boundaries while respecting tradition

The overall website design should feel like a natural extension of the diary practice itself—thoughtful, intentional, and designed to serve contemplation rather than consumption.

---

## Technical Context (For Reference)

The backend supports sophisticated content management including:

- **Hotspots** with SVG coordinates, audio, images, links, and access controls
- **Journeys** (curated sequences through content)
- **Time Data** integration - click on dates to reveal detailed statistics
- **Multi-modal content** (narration, images, external links)
- **Flexible access controls** (free, email-gated, supporter tiers)

_Detailed hotspot data structure and field specifications are documented in Hotspot Schema.pdf (see project assets)._ - [Hotspot Schema](../4-diagrams/hotspot-schema.md)

_Hotspot distribution across different artwork sizes and complexity levels is detailed in Quantity of Hotspot Calculations.xlsx (see project assets). [Hotspot Calculations Spreadsheet](../4-diagrams/quantity-of-hotspot-calculations.xlsx)


### **Time Data Integration**

The project includes detailed time data available in multiple formats:

- **Default presentation:** Static images showing daily pie chart breakdowns, granular timetables with start/end times for each activity, and task hierarchies (parent/child activity relationships)
- **Alternative data source:** Raw CSV exports available for date-range filtering and piece-specific statistics, enabling live data visualizations if desired

This creates opportunities for dynamic data presentations, though static image reveals remain the baseline approach.

👉 If you’d like to explore this further, see the [Time Data Invitation](../6-sample-time-data-invitation/0-README.md)

### **Detailed Interaction Specifications**

For comprehensive interaction patterns, user flows, and behavioral specifications, see the companion **[Interaction Reference Guide](x-interaction-reference-guide-3m-read.md)** which provides designer-focused guidance on hotspot behaviors, audio player states, overlay patterns, and cross-device interaction flows.

---

## Design Deliverables

### **Gallery Experience**

How do users discover and navigate between artworks:

- Visual hierarchy respecting the chronological journey
- Easy access via hamburger menu → Gallery for quick navigation
- Preview mechanisms that intrigue without overwhelming
- Navigation that feels like moving through an exhibition space
- Clear Act-based organization (Prequel, Initiation, Devotion, Transformation)

### **Individual Artwork Interface**

The heart of the experience—a single artwork with interactive elements:

- Hotspot indication and interaction patterns (desktop hover enhancement, mobile tap)
- Audio player positioning and behavior (floating vs embedded approaches)
- Mode switching UI (narration/silent/plain viewing)
- Timeline/date navigation integration (click-to-reveal time data)
- Zoom and pan functionality with hotspot persistence
- Mobile and desktop variants

### **Micro-Interactions**

The small details that make the experience feel alive:

- Hover states and transitions (desktop only)
- Loading patterns for high-resolution artwork
- Hotspot focus and highlighting effects that persist during playback
- Player controls and feedback
- Image/video overlay animations
- Link list presentations
- Page transitions (consider book-flipping effects for Acts I & II)
- Hotspot sharing interface

### **Responsive Behavior**

How the interface adapts across devices while maintaining artistic integrity, with attention to exceptional performance across all device sizes.

_We're open to bold creative interpretations that honor the intimate, transformative nature of the work._

---

## Content Context

### **Artwork Themes & Scale**

- Acts I & II: Book-style diary pages with intricate daily documentation
- Act III: Large-format pieces (up to 1.5 meters) with sophisticated compositions

### **Visual Considerations**

The artworks are primarily black ink on white paper. **Black backgrounds around the artwork will likely provide superior contrast** compared to white backgrounds, which would require artificial framing that conflicts with the book metaphor for Acts I & II.

---

## Constraints & Considerations

### **Technical Constraints**

- Exceptional mobile/tablet performance required
- Support for SVG-based hotspot coordinates
- Audio integration with visual interaction synchronization
- Progressive loading for large, detailed artwork images
- Robust functionality on patchy gallery WiFi

### **Aesthetic Constraints**

- Honor the hand-drawn, black ink artistic style
- Avoid competing with intricate artwork detail
- Maintain gallery-quality presentation standards
- Support both intimate viewing and exhibition contexts
- Consider book metaphor for Acts I & II page transitions

### **Content Constraints**

- Honor the tone of the work and its intimate storytelling
- Access levels need clear but non-aggressive communication
- Social sharing should be tasteful and optional

---

## Success Metrics

**Not Traditional Web Metrics** This isn't about conversion rates or engagement time in the conventional sense.

**Instead, Optimize For:**

- **Contemplative engagement:** Do users spend quality time with individual pieces?
- **Natural discovery:** Do interactive elements feel integral to the art experience?
- **Accessibility:** Can diverse audiences connect with the content meaningfully?
- **Cross-device excellence:** Does it work elegantly on mobile, tablet, and desktop?
- **Exhibition functionality:** Does it enhance rather than distract from the art?

---

## Working Relationship

### **Design Partnership Philosophy**

We're seeking creative collaborators who thrive on solving never-before-attempted challenges. This project demands innovation, not convention—bold creative proposals are not just welcome, they're essential.

### **Process Expectations**

- **Iterative exploration** with regular feedback loops
- **Creative autonomy** within the artistic vision parameters
- **Technical collaboration** with development team throughout
- **Documentation focus** to preserve design decisions for long-term project evolution

The goal is ambitious: create an interface that honors seven years of intensive artistic practice while pushing the boundaries of what digital art experiences can be.

---

## Creative Freedom

This brief intentionally avoids specific visual direction to allow for creative interpretation. The existing technical specifications define functionality—your role is to envision how that functionality should feel.

Consider approaches inspired by:

- **Premium audiobook apps** (elegant, minimal, content-focused)
- **Archival interfaces** (microfilm readers, document exploration tools)
    - what would a microfilm reader from the future be like?
- **Digital art galleries** (immersive, respectful presentation)
    - Think the intimacy of The New York Times' Snow Fall meets the interactivity of a MoMA digital installation
- **Interactive documentaries** (deeply personal, narrative-driven)
- **Meditation apps** (respectful, contemplative interface design)

The goal is to create something unprecedented—an interface worthy of the extraordinary content it presents, honoring both the intimate vulnerability of the diary practice and the sophisticated artistry of the final works.

---

_"What began as survival had become art. What started as personal therapy had evolved into systematic innovation for processing human experience."_

Your interface design will be the bridge that allows others to walk this path of transformation alongside the artist.