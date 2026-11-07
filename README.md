# Ultra Stream — Next-Gen IPTV Landing Page

Ultra Stream is a high-performance dark-mode IPTV landing page featuring an animated video wall, seamless platform carousel, interactive about section, and modern step-by-step subscription flow.

## 🚀 Mobile Performance Optimizations & Fixes

1. **Hero Section & Hero Heading:**
   - **Modern Glassmorphic Hero Heading**: Replaced heavy mask blur box with an optimized backdrop blur card that renders crisply on iOS Safari and Android Chrome.
   - **Fluid Typography**: Dynamic `clamp()` sizing for heading and subtitle, perfectly balanced across all screen widths without horizontal scroll or awkward line breaks.
   - **GPU-Friendly Entrance Animation**: Removed heavy `filter: blur()` during load, achieving 60fps entrance without pixelation or hitching.
   - **Auto-Pause Offscreen RAF**: Added `IntersectionObserver` to the hero video wall to pause 60fps canvas/transform updates when scrolled out of view, saving battery and GPU memory.

2. **Section 2 — CurveFlow Platforms Carousel:**
   - **GPU Hardware Compositing**: Switched to `translate3d` transforms with persistent layer promotion.
   - **Smart Touch Gestures**: Differentiates between horizontal swipe and vertical scrolling (`touch-action: pan-y`) so mobile vertical page scroll is never hijacked or stuttery.
   - **Lightweight Mobile Rendering**: Disabled heavy DOM slice calculations on mobile viewports for fluid 60fps sliding.

3. **Section 3 — About Section:**
   - **Mobile Touch Optimization**: Disabled expensive canvas dot-grid calculation and dynamic radial text mask on touch devices, eliminating severe scroll lag.
   - **Intersection Throttling**: Scrub and canvas loops automatically pause when section is out of the viewport.

4. **Section 4 — 4 Simple Steps:**
   - **Clean Scroll Experience**: Prevented touch traps on card illustrations by disabling pointer capture on touch devices.
   - **One-Time Typed Heading**: Prevents text wiping and cumulative layout shifts (CLS) on scroll.
   - **Simplified Mobile Compositing**: Removed heavy nested 3D perspective and dual-mask gradient borders on mobile screens.

## 📱 Live Demo
Open the live site directly in your browser:
**[View Ultra Stream Live](https://servicesdigitallab-blip.github.io/ultra-stream-iptv/)**
