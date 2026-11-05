**Project:** KAPAS (Kayas/Pukpuk/Artisan): Digital Production and Order Management System for Moriones-Inspired Local Artisans in Marinduque
**Section:** 8. AI Disclosure Progress
**Status:** Provisional.
**AI tool:** Claude

---

## 2. AI-assisted task

| Item | Detail |
|---|---|
| Task | Generate semantic HTML5 structure and CSS styling from our own UI design of the Product Management page |
| Input given to AI | Our UI design image (`Frame.png`) of the Product Management page |
| Affected section | Front-end UI of the Product Management page (Feature 1: Product Catalog Management) |
| Affected files | `index.html`, `styles.css` |
| What the AI produced | Page structure (sidebar, header, search/filter toolbar, product table, Add New Product form) and the stylesheet (colors, fonts, layout, responsive rules, focus styles) |
| What the AI did NOT produce | The UI design and layout, JavaScript, PHP, MySQL, database design, and any back-end logic |

---

## 3. Exact prompt

Prompt sent with the attached `Frame.png`:

```text
This is the new website design for our product management, can you create me a full semantic html, with css
```

## 4. Validation evidence

| Check | Result |
|---|---|
| Opened `index.html` in a browser and compared it with `Frame.png` | Pass |
| Responsive check (desktop, tablet, mobile width) | Pass | 
| Keyboard check (Tab through links, buttons, form fields) | Pass 

**What we checked:**

  - We reviewed the HTML structure and confirmed that semantic tags were used correctly.

  - We compared the UI with the Figma design. Some colors, particularly in the status indicators, did not match the original design.

  - We tested the responsive layout and confirmed that it worked properly.

**Issues found:**

  - Product images have no image placeholders or image tags.

**Changes we made:**

  - Changed the logo to our own logo.
  - Changed the swatch as a placeholder for product images into an image tag.
  - Changed the color of the status

**What we understood**
  - We learned the importance of using semantic HTML, following the design guidelines, and testing the responsiveness of a webpage.
  - We also understood that small UI details, such as colors and product images, are important for maintaining a consistent design.

    

