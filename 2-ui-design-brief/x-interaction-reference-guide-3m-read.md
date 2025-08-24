# Interaction Reference Guide for Designers

## Interactive Art Diary Platform

**Version:** 1.0  
**Purpose:** Interaction behaviors and user flow guidance  
**Complements:** UI Design Brief v1.0  
**Target:** Frontend designers and developers

---

## Quick Reference

### Core Interaction Principles

- **Art-first approach:** Every interaction preserves the contemplative viewing experience
- **Progressive disclosure:** Users choose what content to reveal, when
- **Cross-device consistency:** Same functionality, device-appropriate behaviors
- **Gentle access gating:** Invitations rather than barriers

### Key Interaction Flows

- **Desktop:** Hover highlights → Click starts audio + focus effect
- **Mobile:** Tap zooms + starts audio → Buttons for additional content
- **Audio:** Continues during visual exploration, focus effect persists
- **Modes:** Narration/Silent/Plain viewing with instant switching

---

## 1. Hotspot Interaction Behaviors

### 1.1 Visual States

**Resting State**

- Hotspots completely invisible
- Clean artwork viewing experience

**Desktop Hover**

- Translucent highlighting with pulsing effect
- Immediate response on cursor entry
- Optional: Soft audio feedback
- May auto-reveal content overlays (configurable)

**Active State (Currently Playing)**

- Semi-transparent mask dims entire artwork
- Selected hotspot remains fully illuminated
- Animated border around active area
- Persists until user selects different hotspot or stops playback

_Design Note: Consider toggle between full masking vs highlight-only for continued exploration_

### 1.2 Interaction Flows

**Desktop Flow**

```
Hover → Stylized highlighting + optional content preview
Click → Audio starts + player appears + focus effect + content buttons
Continue exploring → Other hotspots show hover effects beneath mask
```

**Mobile Flow**

```
Tap → Zoom to hotspot + audio starts + focus effect
Buttons appear → "Show Images/Videos/About" if applicable
Zoom out option → "Expand to Full View" maintains playback
```

### 1.3 Content Revelation

**Progressive Disclosure Rules**

- Links: Always accessible, no gating
- Images/Videos/About: May require email verification
- Mobile: Never auto-opens content, always shows buttons first
- Desktop: May preview content or show buttons (configurable)

---

## 2. Audio Player States & Controls

### 2.1 Player Behavior

- **Appearance:** Floats elegantly without blocking artwork
- **Persistence:** Remains active during pan/zoom/exploration
- **Feel:** Premium audiobook aesthetic, not web media player

### 2.2 Core Controls

- Play/Pause, Skip Forward/Back (10s), Next/Previous Hotspot
- Auto-advance toggle, Volume, Back to beginning
- **Mode Toggle:** Sequential ↔ Highlights (in main player)
- **Journey Selection:** Dropdown menu for thematic paths

---

## 3. Viewing Mode Switching

### 3.1 Three Modes

1. **Narration Mode** (🔊 suggested icon) - Full interactive experience
2. **Silent Interactive** (👁️ suggested icon) - Visual interactions only
3. **Plain Viewing** (🎨 suggested icon) - Pure art appreciation

_Icons open to designer interpretation_

### 3.2 Mode Behaviors

- **Narration:** Any area may contain hotspots, audio player active
- **Silent:** Only media-rich hotspots visible, audio player hidden
- **Plain:** All interactivity hidden, distraction-free viewing

---

## 4. Overlay Presentations

### 4.1 Multiple Images Handling

_Desktop has more layout options; mobile typically one-at-a-time_

- **Carousel Modal:** Navigation arrows between images
- **Grid Panel:** All images simultaneously visible (desktop)
- **Inline Stack:** Images appear in-place (desktop)
- **Lightbox Gallery:** Thumbnails → click to expand

### 4.2 Overlay Types

- **Images/Videos:** Modal, panel, or inline presentation
- **Links:** Overlay list or direct external opening
- **About Text:** Panel overlay with easy dismissal

---

## 5. Cross-Device Behavior Differences

### 5.1 Desktop Advantages

- Hover states for content discovery
- Multiple interaction patterns (hover + click)
- Floating elements and side panels
- Fine cursor control for exploration

### 5.2 Mobile Optimizations

- Zoom-to-focus on hotspot selection _(also applies to desktop)_
- Touch-friendly target sizes (44px+)
- "Expand to Full View" functionality
- Single-tap content revelation

---

## 6. Access Level Interactions

### 6.1 Launch Strategy

**Gallery Level:** No gating - all artwork freely viewable **Audio:** Configurable preview duration → email gate for full access **Media:** "Show Images/Videos/About" buttons → email verification required **Links:** Always accessible, no verification needed

_Gallery-level gating exists in architecture for future subscription phases_

### 6.2 Access Flow

```
View artwork → Click hotspot → Hear preview → Email prompt for full access
Verify email → Unlock all narration + media → Smooth continuation
```

---

## 7. Time Data Integration

### 7.1 Implementation

- Pre-rendered charts/timetables connect to date numbers
- Works within existing image overlay system
- **Standard approach:** Static images (recommended)
- **Advanced option:** Dynamic CSV integration (requires separate budget)

### 7.2 Piece-Level Statistics

- Time allocation charts for each of ~45 pieces
- Displays in piece "About" panel
- Opportunity for integrated styling vs simple image exports

---

## 8. Performance & Collaboration

### 8.1 Shared Goals

- 60fps animations with ~100ms interaction response
- Audio starts without perceptible delay
- Graceful performance across all devices

### 8.2 Designer Responsibilities

- Choose responsive hover/transition timings
- Plan UI container sizes for smooth animations
- Ensure touch targets meet accessibility guidelines
- Design animations that can be reduced for accessibility

### 8.3 Developer Collaboration Areas

- **Animation complexity:** Coordinate to avoid frame drops
- **Asset optimization:** Work together on loading strategies
- **Cross-device testing:** Verify interactions work across input types

---

## 9. Key Design Considerations

### 9.1 Essential Behaviors

- **Hotspot highlighting:** Must clearly identify active narration area
- **Audio continuity:** Playback persists through visual exploration
- **Content buttons:** Clear, contextual, easily dismissible
- **Mode switching:** Instant, smooth transitions between viewing modes

### 9.2 Error States & Edge Cases

- **Audio fails:** Graceful fallback with retry option
- **Images fail:** Placeholder with retry or skip option
- **Network interruption:** Pause state with reconnection indicator

### 9.3 Missing Interaction Patterns

_Consider for future versions:_

- Piece-to-piece navigation flows
- Sharing interaction sequences
- Bookmark functionality
- Search/filter behaviors

---

## Implementation Notes

### Required Visual Flow Diagrams

_The following diagrams must be delivered as part of the design handoff (backend team prefers Figma format, but alternative formats acceptable if they provide equivalent clarity):_

- Desktop vs mobile hotspot interaction sequence
- Mode switching state transitions
- Overlay reveal pattern options
- Audio player state changes

### Priority Levels

- **Essential:** Hotspot interactions, audio player, mode switching
- **Important:** Overlay presentations, access gating flows
- **Enhancement:** Advanced time data, sharing features

---

_This guide focuses on interaction behaviors that create an exceptional digital art experience. For visual design direction and overall project vision, reference the complete UI Design Brief - [UI Design Brief – Full Spec (6m read)](ui-design-brief-full-6m-read.md) . 