# Changes Made to the ASTHO Website

## HTML Changes

### File: Leveraging Healthy People 2030 to Build Non-Traditional Multisector Partnerships _ ASTHO.html

1. **Line 10228**: Added `mobile-movable` class to the parent div of the lightblue container
   ```html
   <div class="mobile-movable">
   ```

2. **Line 12656**: Added mobile lightblue anchor div after the authors' recognition paragraph
   ```html
   <div class="mobile-lightblue-anchor"></div>
   ```

3. **Lines 13741-13752**: Added JavaScript for mobile lightblue box positioning
   ```javascript
   <script>
   document.addEventListener("DOMContentLoaded", function () {
       if (window.innerWidth < 1024) {
           const lightBlueBox = document.querySelector(".mobile-movable");
           const anchor = document.querySelector(".mobile-lightblue-anchor");

           if (lightBlueBox && anchor) {
               anchor.insertAdjacentElement("afterend", lightBlueBox);
           }
       }
   });
   </script>
   ```

## CSS Changes

### File: Leveraging Healthy People 2030 to Build Non-Traditional Multisector Partnerships _ ASTHO_files/appforcms2.css

**Lines 6150-6168**: Added mobile-specific styles for lightblue container and anchor
```css

.mobile-lightblue-anchor {
    display: none;
}

@media (max-width: 1023px) {
    aside .mobile-movable {
        display: none;
    }

    .mobile-lightblue-anchor {
        display: block;
    }
    
    .lightblue-container {
        margin-left: 16px;
        margin-right: 16px;
    }
}
```

## Purpose of Changes

1. **Mobile Responsiveness**: Made the "Take It To Go" lightblue container responsive for mobile devices.
2. **Improved Layout**: The lightblue container now moves below the main content on mobile devices for better readability.
3. **Consistent Spacing**: Added proper margins to the lightblue container on mobile to match the site's design system.
4. **Progressive Enhancement**: The changes maintain functionality on all devices while enhancing the mobile experience.
