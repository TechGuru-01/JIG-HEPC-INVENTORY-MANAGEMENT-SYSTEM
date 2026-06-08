# HEPC JIG Inventory Management System (IMS)

A professional, full-stack inventory management system developed as an internship project to streamline tracking, stock optimization, and financial reporting for manufacturing operations. Built with an agile, modular architecture, the platform replaces fragmented logging workflows with a high-performance administration dashboard and an automated, hardware-linked user interface.

## Key Features
* Automated Multi-Currency Conversion: Implements robust back-end calculations that automatically convert and aggregate financial asset values across PHP (Peso), USD (Dollar), and JPY (Yen).
* QR Code & UUID Tracking: Integrates unique identifier (UUID) generation for physical stock, allowing users to scan system-generated QR codes to automate material checkouts.
* User Transaction Logging & Transparency: Features a dedicated user-side interface that records personnel identity, item withdrawal timestamps, and the specific quantity taken, updating stock levels in real time while broadcasting the latest actions to the admin panel.
* Comprehensive Admin Dashboard: Provides a centralized administrative interface to oversee user accounts, manage personnel roles, review live activity feeds, and maintain absolute operational visibility.
* Intelligent Inventory Alerts: Features real-time visual threshold triggers that display immediate low-stock notifications on the primary dashboard when an item's volume drops below safe levels.
* One-Click Purchase Requests: Enables administrators to instantly generate formal purchase requests for low-stock items with a single click, automating the procurement drafting process directly from dashboard threshold alerts.
* Automated Data Purging & Retention: Configured with automated data maintenance logic that safely purges historical log data up to 10 years old, keeping the active database lightweight and operationally efficient.
* On-Demand Stock Printing: Supports rapid report compilation, allowing administrators to generate and print formatted documents of the latest inventory stock levels instantly.
* Performance Pagination & Archiving: Engineered database pagination and structured layout frameworks optimized to handle extensive tracking logs exceeding 100,000 rows without application lag.
* Advanced Catalog Operations: Features scalable PHP and MySQL CRUD logic designed for seamless addition, updating, and real-time monitoring of active warehouse stock.
* Modular Architecture: Adheres strictly to separation of concerns, utilizing modularized code components to ensure clean database operations, ease of maintenance, and future scalability.

## Tech Stack
* Backend: PHP, MySQL (Local XAMPP Development Environment)
* Frontend: JavaScript, HTML5, CSS3 
* Methodologies & Tools: Agile Development, Component Modularization, Single Source of Truth, QR Code / UUID Generation

## System & Transaction Workflow
1. Administrative Setup: Administrators add items to the warehouse catalog, which automatically assigns a unique UUID and generates a corresponding QR code.
2. User Scan & Identification: When retrieving material from production stock, the user scans the physical item's QR code.
3. Allocation Entry: The user interface prompts for entry validation, registering who withdrew the item and the exact quantity removed.
4. Administrative Oversight & Procurement: The action is immediately broadcasted to the administrator panel's activity stream. If an item drops below safety margins, visual warning states trigger on the dashboard, allowing the admin to generate a procurement purchase request in a single click.
5. Database Synchronization: The backend decrements inventory stock counts, registers a permanent entry into the transaction log tables, and systematically tags aging records for the 10-year purging cycle.

## Database Architecture & Scaling
The underlying MySQL schema is built to prioritize fast indexing and data integrity across inventory catalogs, purchase logs, and user transaction tables. To manage high rows-per-table volume safely, the system utilizes optimized offset pagination and a 10-year data retention/purging routine that eliminates obsolete database bloat and limits server load during automated report generation, procurement compilation, and real-time dashboard updates.

## Local Installation & Setup
1. Clone this repository into your local server environment.
2. If executing via XAMPP, place the project directory inside your htdocs folder.
3. Import the system database schema via phpMyAdmin.
4. Update the database configuration strings in the core file to link your local environment credentials.
5. Launch Apache and MySQL from the XAMPP Control Panel and navigate to localhost/HEPC-JIG-IMS in your browser.
