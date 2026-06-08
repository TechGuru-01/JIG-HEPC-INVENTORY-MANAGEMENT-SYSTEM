# HEPC JIG Inventory Management System (IMS)

A professional, full-stack inventory management system developed as an internship project to streamline tracking, stock optimization, and financial reporting for manufacturing operations. Built with an agile, modular architecture, the platform replaces fragmented logging workflows with a high-performance administration dashboard and an automated, hardware-linked user interface.

## Key Features
* Automated Multi-Currency Conversion: Implements robust back-end calculations that automatically convert and aggregate financial asset values across PHP (Peso), USD (Dollar), and JPY (Yen).
* QR Code & UUID Tracking: Integrates unique identifier (UUID) generation for physical stock, allowing users to scan system-generated QR codes to automate material checkouts.
* User Transaction Logging: Features a dedicated user-side interface that records personnel identity, item withdrawal timestamps, and the specific quantity taken, updating stock levels in real time.
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
4. Database Synchronization: The backend decrements inventory stock counts and registers a permanent entry into the transaction log tables.

## Database Architecture & Scaling
The underlying MySQL schema is built to prioritize fast indexing and data integrity across inventory catalogs and user transaction tables. To manage high rows-per-table volume safely, the system utilizes optimized offset pagination and data presentation layers that limit server load during automated report generation.

## Local Installation & Setup
1. Clone this repository into your local server environment.
2. If executing via XAMPP, place the project directory inside your htdocs folder.
3. Import the system database schema via phpMyAdmin.
4. Update the database configuration strings in the core file to link your local environment credentials.
5. Launch Apache and MySQL from the XAMPP Control Panel and navigate to localhost/HEPC-JIG-IMS in your browser.
