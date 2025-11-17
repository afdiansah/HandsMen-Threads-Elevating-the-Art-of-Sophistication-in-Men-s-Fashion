## **Link Demo VIDEO**
Upcoming

---

# **HandsMen Threads – Elevating the Art of Sophistication in Men's Fashion**

## **Abstract**

The primary objective of this project is to design and implement a customized Salesforce CRM solution for HandsMen Threads to optimize core business operations, strengthen data integrity, and elevate customer engagement across the brand. By establishing a centralized platform to manage customers, orders, products, inventory, and automated workflows, the project aims to automate essential business processes including order confirmations, loyalty tier updates, inventory alerts, and scheduled bulk processing.

---

## **User Scenario**

HandsMen Threads, sebuah perusahaan dinamis di industri fashion, sedang mengembangkan proyek Salesforce untuk merevolusi manajemen data dan meningkatkan hubungan dengan pelanggan. Proyek ini berfokus pada pembangunan **data model yang kuat**, memastikan alur informasi yang mulus di seluruh organisasi, serta menjaga **integritas data langsung dari UI** demi akurasi dan konsistensi operasional.

Proyek ini juga mengintegrasikan beberapa proses otomatis untuk meningkatkan efisiensi layanan pelanggan dan operasional:

* **Automated Order Confirmations**  
  Pelanggan akan menerima email otomatis setelah konfirmasi pesanan, meningkatkan engagement dan kepercayaan.

* **Dynamic Loyalty Program**  
  Status loyalitas customer diperbarui otomatis berdasarkan riwayat pembelian untuk memberikan reward yang lebih personal.

* **Proactive Stock Alerts**  
  Sistem mengirim email notifikasi ke tim gudang saat stok barang tersisa kurang dari lima unit untuk mencegah stockout.

* **Scheduled Bulk Order Updates**  
  Setiap tengah malam, sistem memproses order dalam jumlah besar, memperbarui catatan finansial serta menyesuaikan inventaris secara otomatis.

---

## **Objectives**

The project aims to:

- **Automate essential business processes** including order confirmations, loyalty tier updates, inventory alerts, and scheduled bulk processing
- **Maintain accurate and reliable data** through structured data modeling, validation rules, and controlled UI input
- **Provide real-time visibility** into customer activity, order history, and stock levels to support informed decision-making
- **Enhance internal collaboration** through role-based access, streamlined workflows, and unified data access
- **Deliver personalized customer experiences** supported by automated communication, loyalty programs, and targeted notifications

---

## **Technology Stack**

### **1. Salesforce CRM**
World's leading Customer Relationship Management platform for building and strengthening customer relationships.

### **2. Custom Objects**
- **HandsMen_Customer__c** – Maintains customer information
- **HandsMen_Product__c** – Contains men's fashion product details
- **HandsMen_Order__c** – Records order and transaction data
- **HandsMen_Inventory__c** – Tracks inventory data and stock movements
- **Marketing_Campaign__c** – Manages promotions and campaigns

### **3. Lightning App**
Custom app organizing related tabs for streamlined access to business functions.

### **4. Automation Tools**
- **Flows** – Declarative automation for business processes
- **Apex Triggers** – Custom business logic and platform extensions
- **Email Templates & Alerts** – Automated customer communications

### **5. Security Framework**
- **Profiles** – User permissions and object access control
- **Roles** – Data visibility through role hierarchy
- **Permission Sets** – Granular access management

---

## **Project Phases**

### **Phase 1: Salesforce Credentials Setup**
- Create Salesforce Developer Org at https://developer.salesforce.com/signup
- Complete registration and email verification
- Set up password and access setup page

### **Phase 2: Data Management – Objects, Tabs, App Manager, Fields**

#### **Custom Objects Created:**
| Object Name | Description | Key Fields |
|-------------|-------------|------------|
| HandsMen_Customer__c | Stores customer details | Name, Email, Phone, Loyalty_Status__c, Total_Purchases__c |
| HandsMen_Product__c | Stores product catalog | Name, SKU, Price, Stock_Quantity__c |
| HandsMen_Order__c | Stores customer orders | Order_Number, Status, Quantity__c, Total_Amount__c |
| Inventory__c | Tracks inventory levels | Auto Number, Warehouse, Stock_Quantity__c |
| Marketing_Campaign__c | Manages promotions | Campaign_Name, Start_Date, End_Date |

#### **Lightning App Configuration:**
**App Name:** HandsMen Threads

**Navigation Items:**
- HandsMen Customer
- HandsMen Order
- HandsMen Product
- Inventory
- Marketing Campaign
- Reports
- Dashboards
- Accounts
- Contacts

### **Phase 3: Data Configuration – Validation Rules**

| Object | Field | Validation Rule |
|--------|-------|-----------------|
| HandsMen_Order__c | Total_Amount__c | Total_Amount__c <= 0 |
| Inventory__c | Stock_Quantity__c | Stock_Quantity__c <= 0 |
| HandsMen_Customer__c | Email | NOT CONTAINS(Email, "@gmail.com") |

### **Phase 4: Data Security – Profiles, Roles, Users, Permission Sets**

#### **Profile:**
- Cloned Standard User profile to **Platform 1**
- Added access to custom objects

#### **Roles Created:**
- Sales Manager
- Inventory Manager
- Marketing Team

#### **Users:**
- **Niklaus Mikaelson** – Sales role
- **Kol Mikaelson** – Inventory role

### **Phase 5: Email Templates**

Three email templates created:
1. **Order Confirmation** – Sent when order status = Confirmed
2. **Low Stock Alert** – Sent when Inventory < 5 units
3. **Loyalty Program Email** – Sent when loyalty status changes

### **Phase 6: Flows**

#### **a. Order Confirmation Flow**
- **Trigger:** When order is updated to Confirmed
- **Action:** Sends Order Confirmation email to customer

#### **b. Stock Alert Flow**
- **Trigger:** When Inventory stock drops below 5
- **Action:** Sends Low Stock email to Inventory Manager

#### **c. Scheduled Flow: Loyalty Update**
- **Schedule:** Runs daily at midnight
- **Action:** Loops through customers and updates Loyalty Status based on total purchases

### **Phase 7: Automation using Apex**

#### **Apex Triggers Implemented:**
1. **Order Total Trigger** – Auto-calculates Total Amount based on quantity and unit price
2. **Stock Deduction Trigger** – Reduces stock when an order is placed
3. **Loyalty Status Trigger** – Updates Loyalty Status based on total purchases

---

## **What You'll Learn**

- Data Modelling
- Data Quality Management
- Lightning App Builder
- Record-Triggered Flows
- Apex & Apex Triggers
- Asynchronous Apex
- Email Templates & Automation
- Security & Access Management

---

## **Testing & QA**

### **Phase 3: Testing Strategy**
- Unit testing untuk objek dan automasi
- End-to-end testing menggunakan sample data
- Performance testing dan pengecekan keamanan

### **Phase 4: Deployment & Training**
- Deployment ke production
- Pelatihan user terkait fitur baru
- Support setelah go-live & monitoring

---

## **Deliverables**

- **Solution Design Document** – Object Model, ERD, and Automation Strategy
- **Custom Objects** – 5 custom objects with fields and relationships
- **Validation Rules** – Data integrity enforcement
- **Automation Flows** – 3 flows for process automation
- **Apex Triggers** – 3 triggers for business logic
- **Email Templates** – 3 templates for customer communication
- **Security Configuration** – Profiles, roles, and permission sets
- **Lightning App** – HandsMen Threads custom application

---

## **Future Scope**

### **Planned Enhancements:**

- **Process Builder & Advanced Flows**  
  Develop complex approval processes for high-value orders, automated discount calculations, and cross-object workflow automation

- **Salesforce Mobile App**  
  Enable mobile access for sales teams and managers to manage orders, check inventory, and update customer records on-the-go

- **Reports & Dashboards Enhancement**  
  Create advanced dynamic dashboards with real-time metrics, sales performance tracking, inventory turnover analysis, and customer segmentation insights

- **Custom Lightning Web Components**  
  Develop interactive user interfaces for enhanced product catalogs, order management dashboards, and inventory visualization

---

## **Conclusion**

The Salesforce CRM implementation for HandsMen Threads has successfully established a robust and scalable solution encompassing custom objects, automated workflows, intelligent process automation, and comprehensive security architecture. This solution positions HandsMen Threads to deliver superior customer experiences, maintain operational efficiency, and scale their sophisticated men's fashion business with data-driven insights and automated processes that support both customer satisfaction and sustained business growth.

---

## **Getting Started**

1. Access your Salesforce Developer Org
2. Install the HandsMen Threads package (if applicable)
3. Configure user profiles and roles
4. Import sample data for testing
5. Activate flows and triggers
6. Test email templates and alerts
7. Train users on the new system

---
