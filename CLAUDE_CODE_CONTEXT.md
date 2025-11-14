# Yoga Vanessa Website Redesign - Claude Code Context

## Project Overview
I'm redesigning the homepage for yogavanessa.com, a yoga and massage wellness business. The current site has serious design issues: too many competing bright colors, text-on-text readability problems, and excessive image layering. This HTML file is a clean redesign mockup that demonstrates the improved design direction.

## Current Design Problems (Original Site)
1. **Color chaos**: Multiple purples (#5040ae, #7161d0, #5848b7) competing with multiple cyans (#90e2df, #70d9e1, #a9f8dd)
2. **Bright-on-bright text**: Purple text on bright blue backgrounds, cyan text on backgrounds - very hard to read
3. **Image overload**: Background images with parallax effects, plus more images layered on top of those backgrounds
4. **Inconsistent typography**: Three different font families with no clear hierarchy
5. **Poor accessibility**: Many color combinations fail WCAG contrast requirements

## Design System for This Redesign

### Color Palette (STRICT - only use these)
- **Primary Cyan**: #70d9e1 (main accent color - use for important CTAs and highlights)
- **Secondary Purple**: #5848b7 (supporting accent - use for buttons, links, occasional highlights)
- **White**: #ffffff (primary background)
- **Light Gray**: #fafafa (subtle background variation)
- **Dark Text**: #333333 (body text)
- **Medium Gray**: #666666 (secondary text)

**Critical Rule**: NEVER place bright colors directly on other bright colors. Always use white/neutral as buffer.

### Typography
- **Quattrocento**: Headings and body text
- **Lora**: Only for special taglines (like "Why feel okay, when you can feel great?")
- **Font Sizes**:
  - Hero headline: 4rem (64px)
  - Section titles: 2.5rem (40px)
  - Card headings: 1.8rem (29px)
  - Body text: 1.1rem (18px)
  - Small text: 1rem (16px)

### Layout Principles
1. **One image per section maximum** - no layering images on backgrounds
2. **Generous spacing**: 5rem (80px) padding on major sections
3. **Clean cards**: Use subtle box-shadows, not busy backgrounds
4. **Text overlays**: If text must go on images, use dark semi-transparent overlay (rgba(0,0,0,0.5)) with white text
5. **Consistent grid**: Use CSS Grid with auto-fit for responsive behavior

## Section-by-Section Guide

### Hero Section
- Should have a single beautiful photo as background
- White text with subtle drop shadow for readability
- Optional: subtle gradient overlay if needed for text contrast
- One primary CTA button (purple background, white text)

### Services Grid
- Three equal cards in a grid
- Each card: one image, heading, description, CTA button
- White background with subtle shadow on cards
- NO background images behind the grid

### Massage/Content Sections
- Use side-by-side layouts (image + text content)
- Alternate image left/right for visual variety
- Light gray (#fafafa) background to separate from white sections
- Purple headings, gray body text

### Image-with-Text Overlays (like Gift Certificates)
- Dark overlay: rgba(0,0,0,0.5) minimum
- Always white text on dark overlays
- Ensure text remains readable at all screen sizes

### Final CTA Section
- Can use solid cyan background with white text
- OR white background with colored border-top
- Large, prominent CTA button

## Image Integration Instructions

When integrating Vanessa's actual photos:

1. **Replace placeholder SVG backgrounds** with real image URLs
2. **Use high-quality photos** that show:
   - Yoga poses in natural light
   - Massage therapy in calm settings
   - Retreat locations (beaches, nature)
   - Resource materials (books, community)

3. **Image optimization**:
   - Use appropriate sizes (don't load 4K images)
   - Consider using `object-fit: cover` to maintain aspect ratios
   - Add alt text for accessibility

4. **Maintain the clean approach**:
   - One hero image in hero section
   - One image per service card
   - One image per content section
   - NO overlapping/layered images

## Code Editing Guidelines

When making changes to this HTML file:

1. **Maintain color consistency**: Only use colors from the design system
2. **Keep spacing rhythm**: Use 5rem, 3rem, 2rem, 1rem for consistent spacing
3. **Preserve accessibility**: All text must have 4.5:1 contrast minimum
4. **Don't add complexity**: The goal is SIMPLE and CLEAN
5. **Test responsiveness**: Check that changes work on mobile (max-width: 768px)

## Common Edits You Might Need Help With

### Adding Real Images
```css
/* Replace this kind of placeholder */
.hero {
    background: linear-gradient(...), url('placeholder.svg');
}

/* With actual image */
.hero {
    background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), 
                url('path/to/real-image.jpg');
    background-size: cover;
    background-position: center;
}
```

### Adjusting Image Overlays for Readability
If text is hard to read on a photo, increase the overlay darkness:
```css
/* Make overlay darker */
background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('image.jpg');
```

### Adding New Service Cards
Follow the existing pattern:
- Same structure as existing cards
- Use approved colors only
- Maintain consistent padding (2rem on .service-content)
- Keep card shadows subtle: `box-shadow: 0 5px 20px rgba(0,0,0,0.08);`

### Adjusting for Weebly Constraints
If certain CSS properties don't work in Weebly:
- Simplify grid to flexbox if needed
- Use inline styles as fallback
- Keep class names semantic for easy mapping to Weebly's editor

## Responsive Design Requirements

Mobile breakpoint: 768px
- Stack side-by-side layouts vertically
- Reduce hero text size (2.5rem)
- Reduce section padding (3rem instead of 5rem)
- Make navigation stack or hamburger menu
- Ensure images scale properly

## What NOT to Do

❌ Don't add more colors to the palette
❌ Don't use bright text colors (#a9f8dd cyan was unreadable)
❌ Don't layer images on top of background images
❌ Don't add parallax effects (too distracting)
❌ Don't use more than 2-3 font families
❌ Don't create sections without proper spacing (minimum 3rem padding)
❌ Don't place bright purple on bright cyan backgrounds

## Questions to Ask Me

If you're unsure about something, ask about:
- Which of Vanessa's original images should go where?
- Whether a specific color combination is acceptable
- If a layout change maintains the "clean and professional" goal
- Whether additional sections are needed
- How to handle any content that doesn't fit the current structure

## Success Criteria

The redesign is successful if:
✅ All text is easily readable (good contrast)
✅ Color palette is limited to cyan + purple + neutrals
✅ Each section has clear purpose and breathing room
✅ No images are layered on other images
✅ Design feels professional, calm, and welcoming
✅ Site works well on mobile devices
✅ Maintains Vanessa's brand identity (bright, welcoming) without overwhelming visitors

## Current File Status
This is the initial mockup with placeholder images. The next steps are:
1. Replace placeholder images with Vanessa's actual photos
2. Adjust any text content to match her actual copy
3. Fine-tune spacing and sizing based on real content
4. Test on various screen sizes
5. Prepare for implementation in Weebly

---

## How to Work With Me

When you help me edit this file:
1. **Ask clarifying questions** if anything is ambiguous
2. **Show me the before/after** when making significant changes
3. **Explain your reasoning** for design decisions
4. **Flag any accessibility concerns** you notice
5. **Suggest improvements** that align with the "clean and professional" goal

Let's make this website beautiful, readable, and professional! 🧘‍♀️
