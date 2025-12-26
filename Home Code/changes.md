# Latest Changes - skip to main content

## HTML Changes (Association of State and Territorial Health Officials _ ASTHO.html)

1. **Line 9546**: Added skip link for keyboard navigation
   ```html
   <a href="#main-content" class="skip-link">Skip to main content</a>
   ```

2. **Line 10494**: Added `id="main-content"` to the main element for skip link target
   ```html
   <main id="main-content" class="home">
   ```
   Note: Add this id for main tag in every page.

## CSS Changes (appforcems2.css)

1. **Lines 2333-2396**: Added new styles for skip-link
   ```css
   .skip-link {
     position: fixed;
     top: 0.75rem;
     left: 1rem;
     transform: translateX(-50%) translateY(-1rem);
     padding: 0.6rem 1.25rem;
     background-color: #06476b;
     color: #ffffff;
     font-family: 'Jost', sans-serif;
     font-size: 0.95rem;
     font-weight: 500;
     line-height: 1.2;
     text-decoration: none;
     border-radius: 0.375rem;
     box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25);
     z-index: 10000;
     opacity: 0;
     pointer-events: none;
     transition: opacity 0.15s ease-in-out, transform 0.15s ease-in-out;
   }
   
   .skip-link:focus,
   .skip-link:focus-visible {
     opacity: 1;
     pointer-events: auto;
     transform: translateY(0);
     outline: none;
     color: #ffffff;
   }
   
   .skip-link:focus-visible {
     box-shadow: 0 0 0 3px #ffffff, 0 0 0 6px #06476b;
   }
   
   @media (hover: none) and (pointer: coarse) {
     .skip-link {
       left: 1rem;
       transform: translateY(-1rem);
       font-size: 1rem;
     }
     
     .skip-link:focus,
     .skip-link:focus-visible {
       transform: translateY(0);
     }
   }
   
   @media (prefers-reduced-motion: reduce) {
     .skip-link {
       transition: none;
     }
   }
   
   #main-content {
     scroll-margin-top: 6rem;
   }
   ```

## Summary of Changes
- Added an accessible skip link that appears when focused using the keyboard
- Styled the skip link with appropriate colors, spacing, and animations
- Added proper focus states and mobile responsiveness
- Included accessibility features like reduced motion support and high-contrast focus indicators
- Added scroll margin to the main content area to account for fixed headers