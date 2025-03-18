# Ecom - Multipurpose Marketplace HTML Template + RTL

## Overview
Ecom is a multipurpose HTML template designed for marketplace websites with RTL (Right-to-Left) support. The template offers multiple page layouts, integrates popular CSS/JS plugins and libraries, and follows a 7-1 SCSS architecture for clean, maintainable code and easy customization.

## Key Features
- **Responsive Design:** Optimized for all device sizes.
- **Multiple Page Layouts:** Includes various homepages, shop, product, blog, and more.
- **RTL Support:** Easily switch to a right-to-left layout.
- **Integrated Plugins:** Utilizes popular libraries like Bootstrap, jQuery, Swiper, Slick, and more.
- **7-1 SCSS Architecture:** Organized SCSS structure for scalable and maintainable styling.

## Project Structure
```
/project-root
├── assets
│   ├── css
│   │   ├── style.css          # Compiled CSS from SCSS files
│   │   └── style.css.map      # Source map for the compiled CSS (useful for debugging)
│   │   └── plugins/           # Additional CSS plugins or custom plugin overrides
│   │   └── vendors/           # CSS files from third-party plugins/libraries
│   ├── fonts                  # Font files used in the template
│   ├── imgs                   # Images, icons, logos, etc.
│   ├── js
│   │   ├── vendors/           # JavaScript files from third-party libraries (e.g., jQuery, Bootstrap)
│   │   ├── main.js            # Main custom JavaScript file
│   │   └── shop.js            # Custom script for e-commerce functionality
│   └── scss                   # SCSS source files (following the 7-1 pattern)
│       ├── abstracts          # Variables, mixins, functions, and helpers
│       ├── base               # Base styles: reset, typography, animations
│       ├── components         # UI components: buttons, forms, sliders, etc.
│       ├── layout             # Layout-specific styles: header, footer, sidebar, navigation
│       ├── pages              # Page-specific styles: homepage, shop, product, blog, etc.
│       ├── themes             # Theme variations (e.g., default, dark mode)
│       ├── vendors            # SCSS/CSS imports for third-party plugins
│       └── style.scss         # Main SCSS file that imports all partials
├── *.html                     # HTML files for different pages/layouts
└── README.md                  # This README file
```

## Customization & SCSS Compilation

### SCSS Structure (7-1 Pattern)
- **abstracts:**  
  Contains variables, mixins, and functions. Use these files to change global settings like colors, fonts, and spacing.
- **base:**  
  Includes reset styles, normalization, typography, and base animations.
- **components:**  
  Contains reusable UI components such as buttons, forms, modals, and sliders.
- **layout:**  
  Manages overall page structure like header, footer, sidebar, and navigation.
- **pages:**  
  Contains page-specific styles for individual pages (e.g., home, shop, product, blog).
- **themes:**  
  Holds different theme styles (e.g., default, dark mode).
- **vendors:**  
  Imports third-party CSS/SCSS files. **Do not edit these files directly.** Instead, override their styles in your custom SCSS files.
- **style.scss:**  
  The main SCSS file that imports all the partials and is compiled into a single CSS file.

### Compiling SCSS to CSS
Since this project does not include build tools like `gulpfile.js`, `webpack.config.js`, or `package.json`, you can compile the SCSS manually using one of the following methods:

#### Using Sass CLI
1. **Install Dart Sass:**  
   Follow the installation instructions at [Sass Official Site](https://sass-lang.com/install).
2. **Compile the SCSS file:**  
   Open your terminal in the project root and run:
   ```bash
   npm install -g sass
   sass --watch assets/scss/style.scss assets/css/style.css
   ```
   This command compiles `assets/scss/style.scss` (and its imported partials) into `assets/css/style.css`.

#### Using a GUI Tool
Alternatively, you can use GUI applications like **Prepros**, **Koala**, or **CodeKit** to watch and automatically compile SCSS files when changes are detected.

## Customizing Vendor CSS
In the file `assets/scss/vendors/_vendors-import.scss`, you will find imports for various third-party CSS files:
```scss
@import url(../css/vendors/normalize.css);
@import url(../css/vendors/bootstrap.min.css);
@import url(../css/vendors/uicons-regular-rounded.css);
@import url(../css/plugins/swiper-bundle.min.css);
// @import url(../css/plugins/magnific-popup.css);
@import url(../css/plugins/select2.min.css);
@import url(../css/plugins/slick.css);
// @import url(../css/plugins/perfect-scrollbar.css);
@import url(../css/plugins/animate.min.css);
```
- These files load the CSS from various plugins and libraries.
- **Note:** Do not edit these vendor files directly. If you need to override any styles, add your custom CSS rules in your own SCSS files (e.g., within components or a dedicated overrides file) after these imports.

## Browser Support
The template includes Modernizr (`modernizr-3.6.0.min.js`) to detect browser features and provide fallbacks where needed, ensuring a smooth experience across various browsers.

## Development & License Information
- **Theme Name:** Ecom
- **Version:** 3.0
- **License:** GNU General Public License v2 or later (see [GPL-2.0](http://www.gnu.org/licenses/gpl-2.0.html) for details)
- **Developer:** letienhoang

## Contact & Support
If you have any questions or need support regarding this template, please contact:
- **Email:** ltienhoang2@gmail.com
---

Happy coding and enjoy customizing your Ecom template!
