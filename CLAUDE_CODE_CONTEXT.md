# Yoga Vanessa Website Redesign - Claude Code Context

## Quick Status Summary

**Last Updated**: November 13, 2024
**Status**: Live on GitHub Pages

**What's Done:**
- ✅ Clean redesign with professional color palette
- ✅ All real images integrated
- ✅ Logo integrated in navigation
- ✅ Massage services prominently featured
- ✅ Accessibility with ARIA labels
- ✅ Mobile responsive design
- ✅ Deployed to GitHub Pages

**Next Priorities:**
1. Content refinement (update placeholder links: `#booking`, `#contact`, `#yoga`, etc.)
2. Live testing on mobile/tablet devices
3. Performance optimization (image compression)

---

## Project Overview
I'm redesigning the homepage for yogavanessa.com, a yoga and massage wellness business. The current site has design issues: too many competing bright colors, text-on-text readability problems, and excessive image layering. This HTML file is a clean redesign that demonstrates the improved design direction with all real images integrated.

## Problems Solved From Original Site
The redesign fixed these major issues:
- ❌ → ✅ Color chaos (multiple purples/cyans) → Clean 2-color palette
- ❌ → ✅ Bright-on-bright text → High contrast text with proper overlays
- ❌ → ✅ Image overload/layering → One image per section
- ❌ → ✅ Inconsistent typography → Single font family with clear hierarchy
- ❌ → ✅ Poor accessibility → WCAG compliant contrast ratios

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

## Current Image Implementation

All images are integrated and displaying correctly:
- **Hero**: `aspen-trees.jpg` - energetic golden aspens with overlay for text
- **Massage**: `massage-background.jpg` - warm therapy scene
- **Yoga Card**: `yoga-pose.png` - aerial B&W pose
- **Retreats Card**: `retreats.png` - Hawaiian beach
- **Resources Card**: `cookbook.jpg` - Community Cookbook cover
- **Gift Certificates**: `waterfall-background.jpg` - serene landscape with overlay
- **Navigation**: `logo.png` - colorful logo (40px height)

**Unused Images** (available for future pages):
- `headshot.jpg` - professional portrait (good for About page)
- `waterfall-video.jpg` - alternate waterfall image

## Code Editing Guidelines

**Critical Rules When Making Changes:**

1. **Color Consistency**: Only use design system colors (cyan #70d9e1, purple #5848b7, neutrals)
2. **Spacing Rhythm**: Use 5rem, 3rem, 2rem, 1rem for consistency
3. **Accessibility**: Maintain 4.5:1 contrast ratio minimum on all text
4. **Simplicity**: Don't add complexity - goal is CLEAN and PROFESSIONAL
5. **Responsive**: Test on mobile (max-width: 768px breakpoint)

**Common Tasks:**

- **Adjust overlay darkness**: Change `rgba(0,0,0,0.35)` to `rgba(0,0,0,0.5)` etc.
- **Add service cards**: Follow existing pattern with same padding (2rem), shadows, and structure
- **Update links**: Replace placeholder anchors (`#booking`, `#contact`) with actual URLs

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

## When to Ask Questions

Ask the user for clarification when:
- Color combinations might violate the design system
- Layout changes could compromise the "clean and professional" goal
- Additional sections or features are needed
- Content doesn't fit the current structure
- Weebly migration strategy needs adjustment

## Current File Status - COMPLETED PHASE 1 ✅

**Phase 1 Accomplishments (Completed Nov 13, 2024):**

### Images Integrated ✅
All real images from the original yogavanessa.com have been successfully integrated:
- **Hero Section**: `aspen-trees.jpg` with dark overlay (rgba(0,0,0,0.35)) for text readability
- **Massage Section**: `massage-background.jpg` - prominently featured after hero
- **Yoga Card**: `yoga-pose.png` - beautiful aerial B&W yoga pose
- **Retreats Card**: `retreats.png` - stunning Hawaiian beach scene
- **Resources Card**: `cookbook.jpg` - Blissful Life Community Cookbook cover
- **Gift Certificates**: `waterfall-background.jpg` with dark overlay (rgba(0,0,0,0.5))

### Branding ✅
- **Logo**: Integrated `logo.png` in navigation (colorful "Blissful Life" with transparent background)
- Logo displays at 40px height in nav bar

### Content Hierarchy Changes ✅
- **Massage services now featured first** - "Feel Your Best" section moved immediately after hero
- **Hero CTA updated** - Button now says "Book a Massage" instead of "Explore Services"
- **Section renamed** - "What We Offer" changed to "Additional Services" to emphasize massage as primary offering
- **Service order**: Massage → Yoga → Retreats → Resources

### Accessibility ✅
- Added ARIA labels to all background images for screen readers
- All images have descriptive `role="img"` and `aria-label` attributes
- Maintained 4.5:1 contrast ratio on all text

### Design Integrity ✅
- Color palette strictly maintained (cyan #70d9e1, purple #5848b7, neutrals)
- One image per section - no layering
- Clean, professional spacing throughout
- Text readability ensured with proper overlays

### Git Repository ✅
- Initialized git repository
- Created .gitignore (excludes .DS_Store, swap files)
- Initial commit created with all files
- Ready for GitHub Pages deployment

---

## Next Steps - PHASE 2

### Immediate Priorities
1. **Content Refinement**
   - Review all copy for accuracy
   - Update contact information/links
   - Verify all button URLs point to correct destinations
   - Add actual booking system link (replace `#booking`)
   - Update navigation anchors (`#yoga`, `#retreats`, `#resources`, `#contact`)

2. **Responsive Testing**
   - Test on mobile devices (iOS, Android)
   - Test on tablets
   - Verify all images scale properly
   - Check navigation behavior on small screens

### Future Enhancements
3. **Additional Pages** (if needed)
   - About page with headshot.jpg
   - Class schedule page
   - Retreat details pages
   - Contact/booking form page

4. **Performance Optimization**
   - Compress images for faster loading (especially retreats.png and aspen-trees.jpg)
   - Consider WebP format for better compression
   - Add lazy loading to images below the fold
   - Minify CSS

5. **SEO & Meta Tags**
   - Add meta descriptions
   - Add Open Graph tags for social sharing
   - Add favicon
   - Create sitemap.xml

6. **Analytics & Tracking**
   - Add Google Analytics
   - Set up conversion tracking for booking buttons
   - Track scroll depth and engagement

7. **Custom Domain** (Optional)
   - Configure DNS with domain registrar
   - Add CNAME file
   - Set up custom domain in GitHub Pages
   - Enable HTTPS

### Weebly Migration (Future)
When ready to move from GitHub Pages to Weebly:
- Copy HTML structure into Weebly's custom HTML blocks
- Upload images to Weebly's media library
- Adjust image paths to Weebly URLs
- Test responsive behavior in Weebly's editor
- May need to simplify CSS Grid to Flexbox depending on Weebly support

---

## How to Work With Me

When you help me edit this file:
1. **Ask clarifying questions** if anything is ambiguous
2. **Show me the before/after** when making significant changes
3. **Explain your reasoning** for design decisions
4. **Flag any accessibility concerns** you notice
5. **Suggest improvements** that align with the "clean and professional" goal

Let's make this website beautiful, readable, and professional! 🧘‍♀️
