## AI_DISCLOSURE (For Paper) - Week 2

## 1. Section 2-  Identified Problem 

**AI Tools:** Claude

**Task:**
Drafting of the sector context (PSA data) and local context (Inquirer article) paragraphs from two links provided by the group; advice on the order of sector context and local context; evaluation of whether the two sources are sufficient to identify the problem; English version of the paragraphs. The paragraphs were AI-drafted, not only proofread.

**Section:**
Section 2 – Identified Problem (Sector Context, Local Context, references [1] and [2]).

**Exact Prompt:**
Become my research assistant help me to write the identified problem section. Write a sector context paragraph from the PSA tourism page and a local context paragraph from the Inquirer article then judge whether these sources are enough to identify the problem. Two links lang ang pwede mong gamitin: https://psa.gov.ph/statistics/tourism at yung Inquirer article about sa Q1 2024, https://canadianinquirer.net/2024/05/12/marinduque-tourism-sector-posts-strong-q1-performance/. For sector context them, tapos local context gumawa ka ng isang sector context paragraph galing sa PSA tourism page at isang local context paragraph galing sa Inquirer article. Then judge mo kung enough ba talaga yung dalawang sources to identify the problem. Wag mo sabihing may problema ang mga artisan if hindi naman pinapakita ng sources, and be honest IF gaano ba talaga kafit ito sa project. I ONLY NEED 1 sector context paragraph and local context.

**AI Output:**
Draft sector context paragraph, draft local context paragraph, and an evaluation of source sufficiency.

**Validation Method:**
I checked the figures against both source pages (PSA: 8.6% of GDP, PhP 2.09 trillion, and 6.21 million jobs in 2023; Inquirer: over 16,000 visitors in Q1 2024) and went over the citation details too. Neither source says anything about artisans, so we’ll still need evidence from artisan interviews or surveys to show how they actually operate.

**Responsible Member:**
Ghincel Mae B. Luslos

---
## AI_DISCLOSURE (For Paper) - Project Manuscript

**AI Tools:** Gemini

**Task:**Outlining step-by-step test cases and passing criteria for the four core features prior to final system verification.

**Section:**Chapter III – Results and Discussion (Testing Execution / Table 3) 

**Exact Prompt:** "So, based on the four core features, magte-test ako ngayon gamit yung aming KAPAS. So, please indicate ano yung mga kailangan kong i-test para ma-verify natin kung talagang lahat ng core features is nag pass and not failed."

**AI Output:** Generated a structured testing checklist covering CRUD operations, IndexedDB persistence, inventory updates, order status workflows, BroadcastChannel multi-tab synchronization, and public catalog order submission. 

**Validation Method:**  Executed each test case manually on the KAPAS web application using a local desktop browser (Microsoft Edge) and recorded the actual pass/fail observations. 

**Responsible Member:** Kayleigh Plurin F. Rosales

---
## AI_DISCLOSURE (For Paper) - Project Manuscript

**AI Tools:** Gemini

**Task:**Drafting and refining the single-paragraph IEEE-style Abstract and standardized Keywords using a grounded, objective tone.

**Section:**Abstract & Keywords 

**Exact Prompt:**"Based on the information here, let us now construct the abstract. Remember: [150–250 words. In one paragraph summarize: local problem/context; objective; development approach and technology; 3+ implemented features; actual evaluation results; principal conclusion/limitations. Write after final testing. Avoid unmeasured claims.] Keywords: [sector], [web-based solution], [frontend technology], [problem domain]" (Followed by: "Pwede bang huwag masyadong pabanguhin like 100% words like that. We don't boast") 

**AI Output:**Generated a 188-word single-paragraph abstract summarizing the local artisan problem, KAPAS system objectives, client-side tech stack (HTML5, CSS3, Vanilla JS, IndexedDB, BroadcastChannel, Web Crypto API), SDLC/T.R.A.C.E. methodology, four core features, objective functional testing outcomes, and local storage limitations, accompanied by four domain-aligned keywords. 

**Validation Method:**Checked word count compliance, verified accuracy against the actual KAPAS codebase and test results, and cross-checked that all exaggerated or unmeasured claims were removed. 

**Responsible Member:**Kayleigh Plurin F. Rosales

---

## AI_DISCLOSURE (For Paper) - Project Manuscript

**AI Tools:**Gemini

**Task:**Filling in missing evaluation findings and technical limitations in the Results and Discussion section based on actual local testing. 

**Section:**Chapter III – Results and Discussion (Functional Verification

**Exact Prompt:**"May hindi pala ako na-recheck dun sa gawa nung groupmate ko. Meron siyang iniwang bracket na hindi naman niya na-fill uppan. Pakilagyan mo ng info. This: The functional verification was conducted to determine whether the main features of KAPAS performed according to their intended purposes... Based on the testing results, [discuss which features passed, partially passed, or failed]..." 

**AI Output:**Provided two paragraphs detailing that all four core features passed functional verification in a local desktop environment, explaining the viability of the client-side architecture, and outlining actual limitations.

**Validation Method:**Cross-referenced the completed text with the actual functional testing checklist results (Table 3) and verified that the stated limitations accurately reflect the system's current scope. 

**Responsible Member:**Kayleigh Plurin F. Rosales

---

## AI_DISCLOSURE (For Paper) - Project Manuscript

**AI Tools:** Gemini, DeepSeek

**Task:** To Explain the step we took in order to develop the system and what method did we use in order to accomplish it.

**Section:** Chapter II: Methodology, 2.1 development approach 

**Exact Prompt:** "Help us explain the T.R.A.C.E. (Target, Review, Assess, Connect, and Envision)  and System Development Life Cycle (SDLC) Method as the development approach for our KAPAS system. Use our actual research activities and explain each stage in a simple academic writing style.”

**AI Output:** The AI helped revise and organize the explanation of the T.R.A.C.E. Method based on the activities we performed during our research.

**Validation Method:** We reviewed the revised explanation and checked if it matched the actual steps and processes we followed during our research.

**Responsible Member:** Ivan Emmanuel D. Pastrana

---

## AI_DISCLOSURE (For Paper) - Project Manuscript

**AI Tools:**

**Task:**


**Section:**


**Exact Prompt:**


**AI Output:**


**Validation Method:**


**Responsible Member:**


---

## AI_DISCLOSURE (Software Development)

**AI Tool:** Claude

**Task:** Generate semantic HTML5 structure and CSS styling for the Product Management page, based on the group’s own UI design (Frame.png).

**Section:** Core Feature 1: Product Catalog Management; index.html, styles.css

**Exact Prompt:** “This is the new website design for our product management, can you create me a full semantic html, with css” (sent with the attached Frame.png)

**AI Output:** Initial HTML structure (sidebar, header, search/filter toolbar, product table, Add New Product form) and a stylesheet (colors, fonts, layout, responsive rules, focus styles).

Not produced by AI: The UI design and layout

**Validation Method:**  that product images were shown as color swatches instead of image tags.

---

**AI Tool:** 

**Task:** 

**Section:** 

**Exact Prompt:** 

**AI Output:** 

**Validation Method:**

---

**AI Tool:** Copilot

**Task:** Adding a “Decline Order” function for sellers (new “Declined” order status in the seller dashboard and customer order history)

**Section:** 3.3 Core Feature 3: Customer Order Management (also touches 3.4, since customers see the Declined status)

**Exact Prompt:** add "decline order" for the seller

**AI Output:** Done — sellers can now decline an order as a real order status.

Updated:

js/shop.js: added the new declined status to the order workflow, blocked updates after a decline, and prevented customers from cancelling a seller-declined order.
pages/orders/orders.js: added Declined to the seller board and dropdown status list.
pages/customer/customer.js: customers now see Declined in their order history and filter options.
customer.html: filter list includes Declined.
pages/orders/orders.css: styling for the decline column.
README.md: updated the documented status behavior.

**Validation Method:** Ran the full test suite successfully:
node --test test/core.test.mjs test/filters.test.mjs
Result: 25/25 tests passed.

**Responsible Member:** Christine Anne Quezaine O. Lecaros

---

**AI Tool:** Copilot

**Task:** Removing the seller button from the customer storefront and adding customer order cancellation with a required reason

**Section:** 3.4 Core Feature 4: Online Product Catalog for Customers (storefront button change) and 3.3 Core Feature 3: Customer Order Management (order cancellation)

**Exact Prompt:** change the customer part: the "sell your crafts" button should not be there, it should only show in the sellers side, change it to "View your oders". Also, add a cancelation button for the orders, add a text box where the users/customers can say why they cancelled the order, it should be mandatory not optional

**AI Output:** Updated the customer flow:

Replaced the storefront’s “Sell your crafts” button with “View your orders” (index.html).
Added a cancel-order dialog requiring a nonblank reason (up to 300 characters). Customers can cancel unfinished orders; completed or already-cancelled orders can’t be cancelled. The customer and seller views show the cancellation and reason (customer.js, shop.js, orders.js).

**Validation Method:** git diff --check passed. buttons were removed added, and functioning.

**Responsible Member:** Christine Anne Quezaine O. Lecaros

---
