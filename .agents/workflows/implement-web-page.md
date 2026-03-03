---
description: Personalize this Astro static web page template for a new client based on their provided assets.
---

You have been invoked to personalize this Astro static web page for a new client!

This project is a base template designed to be customized manually by you (the AI) for each new business. 
Your goal is to transform the static HTML, CSS, and component structure to perfectly fit the client's brand and content.

Follow these steps exactly to execute the `/implement-web-page` command:

1. **Analyze the Client Data**
   - Look inside the `assets/` directory.
   - Read `assets/data.json` to understand the client's business name, contact info, brand colors, typography preferences, and all the copywriting for the various sections (Hero, About, Location, Gallery).
   - Review the images in `assets/images/` to understand the visual aesthetic you are working with.

2. **Establish the Design Engine (global.css)**
   - Open `src/styles/global.css`.
   - Update the CSS variables in the `:root` block to match the client's brand colors (primary, background, text colors, etc.).
   - Make any necessary adjustments to the `heading-font` based on their vibe (e.g., elegant serifs for fine dining, clean sans-serifs for modern cafes).

3. **Personalize the Astro Components**
   - **`src/layouts/Layout.astro`**: Update the `<title>`, meta description, and the background gradient colors to match the new primary brand color. Update the Google Fonts import if a new font is required.
   - **`src/components/Hero.astro`**: Rewrite the HTML content to use the client's headline, subtitle, and badge text. Ensure the `<img>` tag points to the correct new hero image from `assets/images/`.
   - **`src/components/About.astro`**: Update the "Our Story" text, signature, and side image.
   - **`src/components/Location.astro`**: Update the text describing the location and features, and link the appropriate location image. Note: if the client didn't provide location data, you can remove this section entirely from `index.astro`.
   - **`src/components/Gallery.astro`**: Update the `galleryItems` array mapping to reflect the client's actual menu items/services and their corresponding images.

4. **Assemble the Final Page (`index.astro`)**
   - Open `src/pages/index.astro`.
   - Inject the client's actual contact information, business name, and hours into the `<footer xmlns="http://www.w3.org/1999/html">`.
   - Ensure the sequence of components makes sense for this specific client (e.g., swapping Location and Gallery if requested).

5. **Verify the Build**
   - Run `npm run build` to ensure there are no Astro compilation errors and all image paths are correct.
   - Report back to the user that the site has been successfully personalized and is ready for Cloudflare deployment!
