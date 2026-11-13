# KAPAS (KAYAS/PUKPOK/ARTISAN): Digital Production and Order Management System for Moriones-Inspired Local Artisans in Marinduque
 
**Brex T. Layag, Christine Anne Quezaine O. Lecaros, Ghincel Mae B. Luslos, Charlie A. Matining, Ivan Emmanuel D. Pastrana, Kayleigh Plurin F. Rosales**
 
BSI/T 3C | Marinduque State University
 
---
 
## Abstract
 
Local Moriones-inspired artisans and handicraft enterprise owners in Marinduque face challenges in organizing product catalogs, tracking material inventories, and managing customer orders manually. To address these difficulties, this study developed KAPAS, a client-side web application designed to digitize and streamline artisan business operations. The system was built using HTML5, CSS3, and Vanilla JavaScript (ES modules), utilizing browser-native APIs including IndexedDB for local data storage, the BroadcastChannel API for multi-tab synchronization, and the Web Crypto API (PBKDF2) for credential hashing. Development followed the Software Development Life Cycle (SDLC) framework paired with the T.R.A.C.E Method for requirement analysis. KAPAS implemented four main operational features: Product Catalog Management, Production and Material Inventory Tracking, Customer Order Management, and an Online Product Catalog for Customers. Functional testing conducted in a local desktop browser environment confirmed that target features performed their intended functions, maintaining local data storage and cross-tab updates without requiring a backend server. While data persistence is currently limited to the local browser environment without remote cloud synchronization, KAPAS provides a functional digital tool for local artisans.
 
**Keywords:** Tourism & Cultural Innovation, Client-Side Production Management System, Vanilla JavaScript & Browser APIs, Artisan Inventory and Order Tracking
 
---
 
## I. Introduction
 
### 1.1 Background and Problem Context
 
Tourism serves as a major driver of economic growth in the Philippines, contributing significantly to national gross domestic product and employing millions across characteristic sectors [1]. To harness this economic potential for local creators, digital initiatives have increasingly focused on web applications for handicraft promotion [2], mobile search applications for carved goods [3], and secure digital platforms designed to enhance artisan market visibility and customer accessibility [4]. These digital interventions align with broader manufacturing and organizational studies establishing that digital transformation improves resource planning, managerial decision-making, and operational performance through centralized data integration [5]. Building upon these digital frameworks, small-scale enterprises have successfully adopted lightweight web-based solutions to eliminate manual record-keeping, streamline inventory management [6], accelerate transaction processing via Agile methodologies [7], and monitor production raw materials through structured prototyping methods [8].
 
Locally, the province of Marinduque experiences substantial tourism influxes during Holy Week and the annual Moriones Festival [9]. While Morion mask-making and traditional wood carving represent vital cultural assets and primary sources of livelihood, local artisans face severe marketing gaps and demand drop-offs during festival off-peak seasons [10], compounded by provincial operational vulnerabilities and management challenges [11].
 
To address these localized operational gaps through client-side software development, the web application utilizes standard web technologies including HyperText Markup Language (HTML5) for structural page layout [12], Vanilla JavaScript for client-side interactivity and dynamic product catalog state handling [13], and Cascading Style Sheets (CSS3) for responsive interface styling [14]. The overall system development workflow is structured and executed following an established System Development Life Cycle (SDLC) framework [15].
 
### 1.2 Problem Statement and Research Gap
 
Despite the availability of general e-commerce tools and promotional apps, Moriones-inspired artisans in Marinduque continue to rely on manual, paper-based, or separated records. Existing commercial platforms, such as Facebook, Instagram, etc., do not integrate raw material inventory tracking with finished product cataloging and customer order management within a single, unified system. While local studies document the cultural importance of mask-making and general off-peak marketing challenges [10], operational validation confirms that artisans lack digital tools to monitor raw material inputs, maintain stock quantities, and track customer order milestones across seasonal transitions. Among the studies reviewed, none integrates raw material tracking, product cataloging, and customer order management for heritage craft production, and none serves Moriones-inspired artisans in Marinduque, which is the specific gap KAPAS handles.
 
### 1.3 Objectives
 
**General Objective:** To design, develop, and evaluate KAPAS, a web-based production and order management platform tailored for Moriones-inspired local artisans in Marinduque.
 
**Specific Objectives:**
 
1. To implement Feature 1 (Product Catalog Management), enabling artisans to securely add, edit, delete, and view product listings including names, descriptions, prices, images, and stock quantities.
2. To develop Feature 2 (Production and Material Inventory Tracking), allowing artisans to record raw material supplies, monitor material availability, and update production quantities.
3. To construct Feature 3 (Customer Order Management), providing a module for artisans to record customer orders, view order specifications, and update fulfillment milestones (pending, in production, ready for pickup, completed).
4. To deploy Feature 4 (Online Product Catalog for Customers), giving customers a public interface to browse available products, view prices and details, and submit direct order requests.
5. To evaluate the functional capabilities of all implemented modules through systematic browser-based testing and document observed results against expected acceptance criteria.
### 1.4 Proposed Solution, Scope and Limitations
 
KAPAS is a web-based production and order management system that lets Moriones-inspired artisans manage products, monitor materials and product quantities, record customer orders and track order status in one place. It also provides a public online catalog where customers can browse products, view prices and availability, and submit order requests.
 
**Who benefits:**
 
- **Artisans and small business owners:** organized product, material and order records.
- **Customers and tourists:** easier discovery of local products and order requests without visiting the artisan in person.
The scope of the project is product catalog management; material and quantity tracking; order recording and status updates such as pending, in production, ready for pickup, completed; public catalog with order-request form; browser-based local storage. The excluded services are online payment processing; delivery and courier tracking; mobile application; accounting and payroll; marketing analytics; and coverage beyond Marinduque artisans.
 
---
 
## II. Methodology
 
### 2.1 Development Approach
 
This study adopts an applied software development research design guided by the System Development Life Cycle (SDLC) framework [15], incorporating the T.R.A.C.E. (Target, Review, Assess, Connect, and Envision) Method as its primary domain analysis framework for stakeholder discovery and requirement formulation.
 
While the overall software execution follows structured engineering phases (Requirements Analysis, Interface Architecture, System Implementation, and Testing), the preliminary requirement engineering phase was operationalized using the five stages of the T.R.A.C.E. Method:
 
**1. Target**
 
The first stage focuses on identifying the stakeholders who are involved in the selected sector and who may participate in the study. For this project, the identified stakeholders include Moriones-inspired artisans and small business owners, the organization involved in selling their products, and potential customers such as tourists and local buyers.
 
During this stage, the researchers discussed and identified potential individuals who could participate in the interview and provide relevant information about the current operations of their business. After identifying a suitable participant, the researchers contacted the individual and arranged a schedule for conducting the interview. The researchers also considered the possible customers who may be interested in purchasing Moriones-inspired products to better understand the intended users of the proposed system.
 
**2. Review**
 
The second stage examines the responsibilities, roles, and regular activities of the identified stakeholders. This helps the researchers understand how Moriones-inspired products are created, prepared, managed, and sold.
 
Based on the interview conducted, the researchers identified that the small shop is operated by five individuals who work together to maintain their family business. The owner is primarily responsible for creating the products being sold, while the other members assist in different production activities, particularly carving and product testing. In some instances, the owner also commissions other local artisans to create specific parts of the Morion equipment. The profit from these commissioned works is then shared with the involved artisans.
 
Through this stage, the researchers gained a better understanding of how the shop operates, including the division of responsibilities, product creation, and coordination with other artisans.
 
**3. Assess**
 
The third stage focuses on identifying potential operational problems and gathering supporting evidence from related studies, statistics, and local information. This stage helps determine which activities may require improvement and what difficulties are experienced by the identified stakeholders.
 
Based on the interview with the owner of the small artisan shop, the researchers identified several operational difficulties in managing the business. These include the lack of an organized method for monitoring expenses, recording customer orders, keeping track of deadlines, and monitoring the available resources of the shop. These concerns may affect the owner's ability to manage daily business activities and keep records of ongoing transactions and production.
 
The interview provided the researchers with an initial understanding of the actual challenges experienced by the shop owner. These findings served as the basis for identifying the specific problems that the proposed system aims to address.
 
**4. Connect**
 
The fourth stage connects the identified operational problems with existing research, studies, and relevant information from both local and international sources. It focuses on examining how the problems experienced by the selected stakeholder relate to similar challenges discussed in previous studies and how these issues affect the selected industry or sector.
 
During this stage, the researchers synthesized interview findings with national tourism data [1], provincial arrival statistics [9], empirical off-peak market studies [10], [11], and enterprise inventory literature [2]–[8]. By contextualizing field observations within existing research, the researchers established the baseline significance of the project within the tourism and cultural innovation sector and defined the remaining research gap addressed by the system.
 
**5. Envision**
 
The final stage focuses on developing a proposed solution based on the problems and research findings gathered from the previous stages. It ensures that the proposed system is aligned with the actual needs of the identified stakeholders and addresses the operational difficulties discovered during the research.
 
Based on the information gathered from the interview and related literature, the researchers formulated KAPAS as a web-based production and order management system for Moriones-inspired local artisans in Marinduque. The researchers identified and selected its core features, which include product catalog management, production and material inventory tracking, customer order management, and an online product catalog for customers.
 
During this stage, the researchers continuously reviewed and refined the proposed features to ensure that they were relevant to the identified problems and suitable for the intended users. This process helped the researchers establish a clearer direction for the development of the system and determine how it could assist the shop in organizing its business operations.
 
Through these five stages, the researchers established a structured approach to understanding the current business operations, identifying existing challenges, and developing a proposed solution. The T.R.A.C.E Method helped ensure that the development of KAPAS was guided by the information gathered from the actual stakeholder, supported by related research, and aligned with the operational needs of Moriones-inspired artisans and small businesses in Marinduque.
 
Following the Envision stage, the development process transitions into the technical SDLC Phase Progression:
 
- **System Architecture & Interface Design:** Defining site maps, component layout wireframes, and browser client-side state handling structures using semantic HTML5 [12] and CSS3 [14].
- **System Implementation (Client-Side MVP):** Developing frontend interactive components using Vanilla JavaScript [13] within Visual Studio Code, using GitHub Copilot for code scaffolding under transparent disclosure guidelines.
- **Functional Verification & Evaluation:** Testing implemented modules via browser-based viewport checks and verifying DOM state updates against acceptance criteria.
### 2.2 Requirements and Core Features
 
**Table 1.1. Requirements and Core Features**
 
| Problem / need | Core feature | Acceptance criterion |
|---|---|---|
| Difficulty organizing product information, including names, descriptions, prices, images, and quantities. | Feature 1: Product Catalog Management | The artisan can add, view, edit, and delete product listings, and the updated information is displayed correctly. |
| Lack of an organized way to monitor available materials and finished product quantities. | Feature 2: Production and Material Inventory Tracking | The artisan can record materials, view available quantities, and update inventory records when materials or product quantities change. |
| Difficulty keeping track of customer orders and production deadlines. | Feature 3: Customer Order Management | The artisan can view customer order details, record orders, and update their status from pending to in production, ready for pickup, and completed. |
| Limited accessibility of product information for customers who want to discover and purchase Moriones-inspired products. | Feature 4: Online Product Catalog for Customers | Customers can browse available products, view their descriptions and prices, check availability, and submit an order request. |
 
### 2.3 Interface Architecture and Data Handling
 
KAPAS is designed as a lightweight client-side web application that provides two primary user interfaces: the artisan management interface and the customer interface. These interfaces serve distinct purposes depending on the user's role in the system. The artisan management interface focuses on managing product catalogs, monitoring available materials and product quantities, and tracking customer orders. Meanwhile, the customer interface allows users to browse available Moriones-inspired products, view product details and prices, check availability, and submit direct order requests.
 
The system architecture is structured as a client-side web application operating directly within modern web browsers without requiring a dedicated backend server. HyperText Markup Language (HTML5) and Cascading Style Sheets (CSS3) are used to structure and design the responsive interfaces across shared stylesheets and page-specific layouts, while Vanilla JavaScript (ES modules) provides interactive functions and dynamic state management without heavy frameworks or compilation build steps.
 
```
 Artisan Interface        Customer Interface
 (dashboard)              (public catalog + order form)
        \                   /
         v                 v
   HTML5 + CSS3  |  Vanilla JavaScript (ES modules)
                   |
        +----------+-----------+
        v          v           v
   IndexedDB   BroadcastChannel   Web Crypto API
   (records)   (tab sync)         (PBKDF2 hashing)
```
 
*Figure 1. KAPAS Client-Side Architecture and System Layer Flow*
 
**1. Data Handling and Browser-Based Storage**
 
To ensure data persistence and security directly within the client environment, the system utilizes advanced browser-native capabilities:
 
- **IndexedDB for Local Data Persistence:** Replaces traditional server-side databases by storing user accounts, product catalogs, raw material inventories, and customer orders directly within the browser storage.
- **BroadcastChannel API for Tab Synchronization:** Enables real-time communication across multiple open browser tabs, automatically notifying other open windows to reload or update when data changes are executed.
- **Web Crypto API (PBKDF2):** Provides secure, salted password hashing to protect administrative and user account credentials locally.
- **Product Catalog and Inventory Management:** Artisans can record items, material supplies, and stock quantities, updating records instantly through client-side state execution.
- **Customer Order Processing:** Captures customer submissions from the public catalog, allowing artisans to track fulfillment milestones (pending, in production, ready for pickup, completed).
**2. Overall System Data Flow**
 
The operational workflow begins when a user accesses the KAPAS web application through a browser via a lightweight static server setup. User actions, such as modifying product details, updating material inventories, or submitting order requests, are captured by JavaScript event listeners. These transactions are processed client-side and committed directly to the browser's IndexedDB, while the BroadcastChannel broadcasts the state update across active sessions to maintain data consistency.
 
### 2.4 Technology Selection and Comparative Justification
 
The development of KAPAS uses several web technologies that work together to provide the system's required functions. The selected technologies were based on the project's scope, the complexity of its features, compatibility, and the technical knowledge of the researchers.
 
**Table 1.2. Technology Selection and Comparative Justification**
 
| Technology | Alternative considered | Why chosen for THIS project | Evidence |
|---|---|---|---|
| HTML5 | React | HTML5 provides a straightforward structure for website content without requiring an additional frontend framework. | [12] |
| CSS3 | Bootstrap | CSS3 provides greater flexibility in customizing the website's layout and visual design without relying on a CSS framework. | [14] |
| Vanilla JavaScript | jQuery | Vanilla JavaScript provides the necessary interactive functions, form validation, and business logic without requiring an additional JavaScript library. | [13] |
| IndexedDB | LocalStorage | IndexedDB supports structured data storage, transactions, and multiple records, making it suitable for managing KAPAS records locally. | [16] |
| BroadcastChannel API | Manual page refresh | Enables seamless real-time communication across multiple open browser tabs, automatically triggering UI updates when data changes occur. | [17] |
| Web Crypto API (PBKDF2) | Plain text password storage | Implements secure, salted password hashing natively within the browser environment to protect user and administrative credentials. | [18] |
 
### 2.5 Implementation and Evaluation Procedure
 
The development of KAPAS was carried out using HTML5, CSS3, and Vanilla JavaScript. The researchers used these technologies to build the website's structure, design, and interactive functions. External CSS files were used to organize the visual appearance of the different pages, while JavaScript handled user interactions, data processing, and other system functions.
 
For data management, the system uses IndexedDB as its primary browser-based storage mechanism. The LocalStorage API is used to retain selected information across browser sessions, while the BroadcastChannel API allows communication between multiple browser tabs. The Web Crypto API with PBKDF2 is also utilized for password-related security operations.
 
During implementation, the researchers developed the system's main features based on the requirements identified during the research process. These include Product Catalog Management, Production and Material Inventory Tracking, Customer Order Management, and the Online Product Catalog for Customers.
 
For evaluation, the researchers conducted functional testing to determine whether the developed features performed according to their intended functions. The testing involved checking the website's navigation, forms, buttons, data storage, and other interactive components. The researchers also examined whether records could be properly saved, retrieved, and updated through the system.
 
The evaluation procedures were conducted within a desktop web environment to ensure reliable system execution. Testing was performed locally on a development laptop running the Microsoft Edge web browser, verifying that the desktop interface, navigation layouts, and IndexedDB data transactions functioned properly during local server execution.
 
Any errors or unexpected behavior encountered during testing were examined and addressed through necessary adjustments. The results of the evaluation were used to identify the working functions of the system, as well as areas that still required improvement.
 
---
 
## III. Results and Discussion
 
### 3.1 Core Feature 1: Product Catalog Management
 
The Product Catalog Management feature is designed to help the artisan organize and maintain information about the Moriones-inspired products offered by the shop. It allows the user to manage product details, including product names, descriptions, prices, images, and available quantities.
 
Through this feature, the artisan can add new products, view existing items in a structured list, edit product specifications, and delete outdated entries. The information is stored using IndexedDB, allowing product records to remain available within the browser even after the page is closed.
 
This feature addresses the need for a more organized way of maintaining product information and keeping track of the items offered by the shop.
 
During testing, the researchers performed complete CRUD (Create, Read, Update, Delete) cycles by inputting sample product data through the artisan dashboard interface, saving them into the browser database, modifying prices and descriptions, and removing items. The observed results showed that all product records successfully committed to the browser's IndexedDB without data loss, and the catalog interface rendered updates instantly upon execution. However, image uploads are currently handled via local file paths or string representations rather than remote cloud storage integration.
 
### 3.2 Core Feature 2: Production and Material Inventory Tracking
 
The Production and Material Inventory Tracking feature is intended to help the artisan monitor the materials used in production and the available quantities of finished products. It provides a way to organize inventory information and keep records of the resources available to the shop.
 
Through this feature, the artisan can add raw material supplies, update stock quantities as materials are consumed, and view current inventory. These records help the user become more aware of the available resources and the quantities needed for production.
 
This feature addresses the concerns identified during the interview regarding the difficulty of monitoring available materials and resources within the shop.
 
During testing, the researchers simulated inventory workflows by adding stock entries, modifying material quantities, and verifying stock count persistence across browser refreshes. The results showed that inventory counts accurately reflected user modifications and updated local records in real time. Any limitations encountered during the testing process, such as the lack of automated stock-level alerts or low-inventory push notifications, were also considered.
 
### 3.3 Core Feature 3: Customer Order Management
 
The Customer Order Management feature is designed to help the artisan organize customer orders and monitor their progress. It provides a centralized interface where order information can be recorded, viewed, and updated.
 
Through this feature, the artisan can view incoming customer orders, check specific buyer details, and update fulfillment milestones. The system uses different order statuses, such as pending, in production, ready for pickup, and completed, to help identify the current progress of each order.
 
This feature addresses the problem identified during the interview regarding the difficulty of keeping track of customer orders and their respective deadlines.
 
During testing, the researchers submitted test customer orders through the public catalog form, reviewed them in the artisan dashboard, and transitioned order status badges across the designated workflow stages. The observed results showed that order records were accurately captured, stored in IndexedDB, and synchronized across active browser tabs using the BroadcastChannel API. Any functions that were incomplete or did not behave as expected, such as real-time SMS or email notifications sent directly to customers upon status changes, were recorded as limitations.
 
### 3.4 Core Feature 4: Online Product Catalog for Customers
 
The Online Product Catalog for Customers is designed to provide an accessible way for potential buyers to view the Moriones-inspired products offered by the shop. It allows customers to explore available products and review important information before making a purchase decision.
 
The customer-facing interface displays product information such as names, descriptions, prices, and images. Customers can browse available items, inspect detailed descriptions, check stock availability, and submit direct purchase order requests via the integrated form.
 
This feature aims to improve the accessibility of product information and provide potential customers, including tourists and local buyers, with a convenient way to discover the products offered by the shop.
 
During testing, the researchers navigated the public catalog interface, verified product display rendering, tested form input validations, and submitted sample purchase requests. Any limitations involving product availability, customer ordering, or other functions, such as the absence of an integrated online payment gateway (e.g., GCash API) for direct checkout, were also documented.
 
### 3.5 Functional Verification and Limitations
 
This section summarizes the testing performed on the four core features of KAPAS. It compares the expected behavior of each feature with the actual results observed during testing.
 
**Table 3. Functional Verification of Core Features**
 
| Core feature | Expected behavior | Observed evidence | Status |
|---|---|---|---|
| Product Catalog Management | Product information can be added, viewed, edited, and deleted. | CRUD operations executed successfully; records persisted reliably via IndexedDB. | Pass |
| Production and Material Inventory Tracking | Material and product quantities can be recorded and updated. | Stock levels updated accurately and retained across local sessions. | Pass |
| Customer Order Management | Customer orders can be recorded, viewed, and updated. | Orders successfully tracked across statuses (pending, in production, ready for pickup, completed). | Pass |
| Online Product Catalog for Customer | Customers can browse products and view their information. | Public catalog rendered items correctly and submitted purchase requests to local storage. | Pass |
 
The functional verification was conducted to determine whether the main features of KAPAS performed according to their intended purposes. The results were evaluated based on the expected behavior of each feature and the actual observations during testing.
 
Based on the testing results, all four core features (Product Catalog Management, Production and Material Inventory Tracking, Customer Order Management, and the Online Product Catalog for Customers) successfully passed the functional verification. The findings indicate that the client-side architecture utilizing HTML5, CSS3, Vanilla JavaScript, and IndexedDB is fully capable of supporting the core operational workflows of local artisans without requiring a complex backend server.
 
However, the system still has certain limitations, particularly in the lack of multi-device synchronization since data is restricted to the local browser storage, the absence of automated external notification services for customers, and the reliance on manual processes for online payment verification. These limitations are important to consider in determining the current capabilities of KAPAS and the improvements that may be needed in future development.
 
---
 
## IV. Conclusion
 
The study focused on developing KAPAS, a web-based production and order management system designed to assist Moriones-inspired artisans and small business owners in organizing their business operations. The project was developed in response to the challenges identified during the interview, particularly in managing product information, monitoring materials and available resources, and keeping track of customer orders.
 
The development process was guided by the Software Development Life Cycle (SDLC) framework, integrating the T.R.A.C.E. Method to identify stakeholders, examine existing activities, assess operational difficulties, and envision a tailored software solution based on gathered requirements and related literature.
 
The development of KAPAS resulted in the implementation of its planned features, including Product Catalog Management, Production and Material Inventory Tracking, Customer Order Management, and an Online Product Catalog for Customers. These features were designed to provide a more organized way of handling product information, inventory records, and customer transactions.
 
Throughout the development process, the researchers gained experience in using web technologies, organizing system data, designing user interfaces, and testing system functionality. The project also provided a better understanding of how information systems can be applied to support the operations of small businesses and local artisans.
 
Although KAPAS provides a proposed solution to the identified operational concerns, further improvements and testing may still be necessary. Future development may focus on improving data accessibility across different devices, expanding system functionality, and conducting additional evaluations with the intended users to determine its effectiveness in actual business operations.
 
---
 
## References
 
[1] Philippine Statistics Authority, "Tourism Satellite Account," PSA. [Online]. Available: https://psa.gov.ph/statistics/tourism (accessed Nov. 4, 2026).
 
[2] R. V. A. Ginez, R. P. Villaflor, M. P. Balicao, J. C. R. Libo-on, and M. L. D. Melendez, "Made by hands: A web application for handicraft products in Alaminos City," Int. J. Res. Innov. Soc. Sci., vol. 9, no. 2, pp. 2560–2564, Feb. 2025. [Online]. Available: https://rsisinternational.org/journals/ijriss/articles/made-by-hands-a-web-application-for-handicraft-products-in-alaminos-city
 
[3] A. P. Balcita, S. Kupsch, and T. D. Palaoag, "KITIKIT: A mobile app for searching hand-carved wood products," in Proc. 2019 4th Int. Conf. Intell. Inf. Technol. (ICIIT '19), Da Nang, Vietnam, 2019, pp. 57–61. [Online]. Available: https://dl.acm.org/doi/10.1145/3321454.3321467
 
[4] O. D. A. Adekunle, Z. Amuda, S. Abe, T. O. Oluwatosin, A. G. Adetula, A. M. Akinpetide, and T. D. Akinjogunla, "Development of a secure freelance web-based and sentiment-oriented digital platform for local artisans: A case study of Akungba Akoko," The Indonesian Journal of Computer Science, vol. 15, no. 1, 2026. [Online]. Available: https://doi.org/10.33022/ijcs.v15i1.5090
 
[5] Vysochanska, "The role of digital transformation in the strategic management system of construction production," The American Journal of Interdisciplinary Innovations and Research, vol. 8, no. 2, pp. 95–102, Feb. 2026. [Online]. Available: https://doi.org/10.37547/tajiir/Volume08Issue02-12
 
[6] M. T. Tanaman, J. L. A. Baylosis, B. J. A. Abiles, M. L. P. Catungal, and P. C. Encarnacion, "Web-based inventory management system," Int. J. Sci. Appl. Inf. Technol., vol. 12, no. 5, pp. 44–48, Sep.–Oct. 2023. [Online]. Available: https://doi.org/10.30534/ijsait/2023/021252023
 
[7] M. A. T. Rosario, M. E. F. Trinidad, A. C. C. Perez, and G. Ng, "An agile approach to the sales and inventory system for Company A," Univ. of Asia and the Pacific, Pasig City, Philippines, Zenodo, Jun. 22, 2023. [Online]. Available: https://zenodo.org/records/8069150
 
[8] D. A. Susanto, A. Firmansyah, and I. Nawangsih, "Implementation of a web-based raw material inventory information system using the prototype method: A case study at PT. XYD," Int. J. Softw. Eng. Comput. Sci. (IJSECS), vol. 4, no. 2, Aug. 2024. [Online]. Available: https://doi.org/10.35870/ijsecs.v4i2.2926
 
[9] M. Gil, "Marinduque tourism sector posts strong Q1 performance," Philippine News Agency, May 10, 2024. [Online]. Available: https://alpha.pna.gov.ph/articles/1224509
 
[10] L. R. Meña, "Adapting to festival downtimes: Marketing strategies of local businesses during the Moriones Festival off-peak season in Marinduque, Philippines," Zenodo, Mar. 15, 2026. [Online]. Available: https://zenodo.org/records/19027263
 
[11] J. Brion, D. M. Largado, E. Mandia, M. Minay, and B. M. Nuñez, "Ecotourism and environmental conservation in the small island of Gaspar, Marinduque, Philippines: A baseline for responsible tourism," E3S Web Conf., vol. 688, art. no. 07003, Jan. 2026. [Online]. Available: https://doi.org/10.1051/e3sconf/202668807003
 
[12] Mozilla, "HTML: HyperText Markup Language," MDN Web Docs, 2026. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/HTML
 
[13] Mozilla, "JavaScript," MDN Web Docs, 2026. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/JavaScript
 
[14] W3C, "Cascading Style Sheets (CSS) Snapshot," World Wide Web Consortium (W3C), 2026. [Online]. Available: https://www.w3.org/Style/CSS/Overview.en.html
 
[15] I. Sommerville, Software Engineering, 10th ed. Boston, MA, USA: Pearson, 2016. [Online]. Available: https://dl.acm.org/doi/book/10.5555/2843938
 
[16] W3C, "Indexed Database API," W3C Recommendation. [Online]. Available: https://www.w3.org/TR/IndexedDB/
 
[17] Mozilla, "BroadcastChannel API - Web APIs," MDN Web Docs. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel
 
[18] W3C, "Web Cryptography API," W3C Recommendation (Focus on PBKDF2). [Online]. Available: https://www.w3.org/TR/WebCryptoAPI/
 
---
 
## CRediT Author Contributions Statement
 
**Project:** KAPAS (Kayas/Pukpok/Artisan): Digital Production and Order Management System for Moriones-Inspired Local Artisans in Marinduque
 
**Group Name:** Wonder Kids
 
**Course / Section:** BSIT-3C-SD
 
| Contributor | C | M | So | Va | Fo | I | R | D | O | E | Vi | Su | P | Fu |
|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Author 1: Brex T. Layag | ☐ | ☐ | ☐ | ☐ | ☐ | ✓ | ✓ | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ | ✓ |
| Author 2: Christine Anne Quezaine O. Lecaros | ☐ | ☐ | ✓ | ✓ | ✓ | ☐ | ☐ | ✓ | ☐ | ✓ | ✓ | ✓ | ✓ | ☐ |
| Author 3: Ghincel Mae B. Luslos | ✓ | ✓ | ✓ | ✓ | ☐ | ☐ | ☐ | ☐ | ✓ | ☐ | ✓ | ✓ | ✓ | ☐ |
| Author 4: Charlie A. Matining | ✓ | ☐ | ☐ | ☐ | ☐ | ✓ | ✓ | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |
| Author 5: Ivan Emmanuel D. Pastrana | ✓ | ✓ | ✓ | ☐ | ☐ | ✓ | ✓ | ☐ | ☐ | ✓ | ☐ | ☐ | ☐ | ☐ |
| Author 6: Kayleigh Plurin F. Rosales | ☐ | ✓ | ☐ | ✓ | ✓ | ☐ | ✓ | ✓ | ✓ | ✓ | ✓ | ☐ | ✓ | ✓ |
 
**Role Legend**
 
| Code | Role | Code | Role |
|---|---|---|---|
| C | Conceptualization | M | Methodology |
| So | Software | Va | Validation |
| Fo | Formal analysis | I | Investigation |
| R | Resources | D | Data curation |
| O | Writing – original draft | E | Writing – review & editing |
| Vi | Visualization | Su | Supervision |
| P | Project administration | Fu | Funding acquisition |
 
**Member confirmation:**
 
- Brex T. Layag – Confirmed / <img width="536" height="211" alt="904605400_1450777507168997_8310706183548958573_n" src="https://github.com/user-attachments/assets/bd01f0e3-4674-41f3-8bb7-7cf50ec1df61" />
 / November 13, 2026
- Christine Anne Quezaine O. Lecaros – Confirmed / <img width="726" height="615" alt="1794581497552" src="https://github.com/user-attachments/assets/aa946379-3d98-4258-a389-68a0c99f2b3c" />
 / November 13, 2026
- Ghincel Mae B. Luslos – Confirmed / <img width="1653" height="1670" alt="1794581442531" src="https://github.com/user-attachments/assets/7408bf90-e1d9-4de4-8f80-a2ac6dee5023" />
 / November 13, 2026
- Charlie A. Matining – Confirmed / <img width="645" height="212" alt="1794581626695" src="https://github.com/user-attachments/assets/f6b80fd3-5543-43f3-afef-f245e2403727" />
 / November 13, 2026
- Ivan Emmanuel D. Pastrana – Confirmed / <img width="644" height="344" alt="906396074_2102940760347203_3353710509813344905_n" src="https://github.com/user-attachments/assets/6ce2d40f-60c9-4190-b74b-923607b2622f" />
 / November 13, 2026
- Kayleigh Plurin F. Rosales – Confirmed / <img width="1699" height="1625" alt="1794581383792" src="https://github.com/user-attachments/assets/173a45dd-5f87-4b6d-90b1-89cbd0100dec" />
 / November 13, 2026
CRediT role definitions: https://credit.niso.org/contributor-roles/. Roles marked must reflect substantive actual contributions; no role is mandatory by default.
 
---
 
## AI Use and Supporting Evidence
 
https://github.com/rorikae-busy/KAPAS/blob/main/AI_DISCLOSURE.md
 
