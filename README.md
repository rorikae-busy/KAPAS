# 1. Project Title

**KAPAS (Kayas/Pukpok/Artisan): Digital Production and Order Management System for Moriones-Inspired Local Artisans in Marinduque**

Web Systems and Technologies 1 

**Group Name:** WONDER KIDS

---

# 2. Selected Sector

Tourism & Cultural Innovation

---

# 3. Brief Problem Description

Morion masks and other Moriones-inspired crafts are part of Marinduque's cultural heritage and a source of income for local makers. Demand rises around the Moriones Festival and drops during the off-peak season.

Moriones-inspired artisans in Marinduque still rely on manual, paper-based or separated records. Platforms such as Facebook and Instagram do not combine raw material tracking, product cataloging and customer order management in one system, and none of the studies we reviewed does this for heritage craft production.

An interview with the owner of a small artisan shop showed that the shop lacks an organized way to monitor expenses, record customer orders, keep track of deadlines and monitor available resources.

---

# 4. Proposed Solution

KAPAS is a web-based production and order management system where artisans and small businesses manage their products, materials and customer orders in one place. A public online catalog lets customers browse products, view prices and availability, and submit order requests without visiting the maker in person.

---

# 5. Core Functional Features

1. **Product Catalog Management.** Add, view, edit and delete products with a name, description, price, image and stock quantity.
2. **Production and Material Inventory Tracking.** Record raw material supplies, monitor availability, and update material and product quantities.
3. **Customer Order Management.** Orders appear in the artisan's Orders page as *Pending* and move through *In production*, *Ready for pickup* and *Completed*.
4. **Online Product Catalog for Customers.** A public interface to browse products, view prices, details and availability, and submit order requests.

**Additional implementation details** (beyond the four core features in the paper):

- Two account types, Seller (artisan or business) and Customer (buyer), each with its own dashboard. Only sellers manage products, materials and order statuses. Only signed-in customers place orders.
- Search, filter and sort on the catalog, Products, Materials and Orders pages.
- Backup and restore of all data as a JSON file.
- Live updates between open tabs without a refresh.
- Extra order statuses (*Declined*, *Cancelled*), made-to-order requests, product categories, hidden products, and on-screen low-stock warnings.

**Limitations:** data is stored only in the local browser (no multi-device sync); sign-in is local and not a replacement for server-side authentication; no SMS or email notifications; no online payment gateway; images are stored locally; clearing browser data erases everything, so use the backup button.

**Out of scope:** online payment processing, delivery and courier tracking, a mobile application, accounting and payroll, marketing analytics, and coverage beyond Marinduque artisans.

---

# 6. Technologies Used

| Technology | Role |
|---|---|
| HTML5, CSS3 | Page structure and responsive styling |
| Vanilla JavaScript (ES modules) | All behavior, with no framework and no build step |
| IndexedDB | Primary browser storage for accounts, products, materials and orders |
| LocalStorage | Retains selected information across browser sessions |
| BroadcastChannel API | Syncs updates across open tabs |
| Web Crypto API (PBKDF2) | Salted password hashing |
| `serve` | Static web server used by `npm start` |
| Node test runner, fake-indexeddb | Automated tests of the data and business logic |

Development followed the SDLC framework with the T.R.A.C.E. Method for requirement analysis, using Visual Studio Code.

---

# 7. Installation or Running Instructions

## Option A: Run online (no installation)

Open the deployed version on Vercel: **https://kapas-amber.vercel.app/index.html**

Use a modern browser such as Microsoft Edge or Chrome. Data is stored in your own browser (IndexedDB), so records you create are only visible on that device and browser.

## Option B: Run locally

**Requirements:** Node.js (LTS) and a modern browser such as Microsoft Edge or Chrome.

1. Clone the repository:
   ```bash
   git clone https://github.com/rorikae-busy/KAPAS.git
   cd KAPAS
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the local server:
   ```bash
   npm start
   ```
4. Open the address shown in the terminal (usually `http://localhost:3000`) in your browser.
5. *(Optional)* Run the automated tests:
   ```bash
   npm test
   ```

**Notes:**
- The app must be opened through the local server, not by double-clicking `index.html`, because it uses ES modules.
- It can also be run in CodeSandbox using the setup in `.codesandbox/`.
- Data is stored in the browser, so to demo both roles, create a Seller and a Customer account in the same browser and use several tabs.

---

# 8. Group Members

Group: Wonder Kids (BSI/T-3C)

- LAYAG, Brex T.
- LECAROS, Christine Anne Quezaine O.
- LUSLOS, Ghincel Mae B.
- MATINING, Charlie A.
- PASTRANA, Ivan Emmanuel D.
- ROSALES, Kayleigh Plurin F.

---

# 9. Link to Full Project Documentation

- Full project documentation: [`PROJECT_DOCUMENTATION.md`](PROJECT_DOCUMENTATION.md)
- Project paper manuscript: [`docs/final-manuscript.pdf`](docs/final-manuscript.pdf)
- Author contributions: [`CONTRIBUTIONS.md`](CONTRIBUTIONS.md)

---

# 10. AI Disclosure Reference

AI assistants were used in this project. The tool, task, prompt, output, validation and responsible member for each use are recorded in [`AI_DISCLOSURE.md`](AI_DISCLOSURE.md).
