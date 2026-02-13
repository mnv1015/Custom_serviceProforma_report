# Service Pro Forma Report with Email Automation

## Overview
This solution delivers a **custom Service Pro Forma reporting and email automation process** developed using RDLC reporting and AL extension logic in Dynamics 365 Business Central.

The implementation enables users to generate a **custom-designed pro forma document** directly from service transactions and automatically send it to the respective customer while ensuring strict validation, correct data retrieval, and controlled email behavior.

---

## Tech Stack

- **AL Language** – Extension development and business logic  
- **MS Report Builder** – RDLC reporting,  Custom pro forma layout and rendering  
- **Business Central Workflow & Email Framework** – Communication handling  
- **Report Builder Dataset Methods** – Dynamic header and dataset exchange  
- **Custom AL Data Processing** – Shortcut Dimension 5 & 6 retrieval and grouping logic  

---

## Functional Flow

1. A user initiates the process from the **service transaction interface** using a custom action.
2. The system gathers:
   - Service transaction details  
   - Customer information  
   - Required shortcut dimension values, including those not accessible through standard reporting  
3. A **custom RDLC pro forma report** is generated using the prepared dataset.
4. Transactions are grouped **customer-wise** when multiple records are selected.
5. The system ensures:
   - Only **one email per customer** is sent  
   - Each email contains the **correct pro forma report** for that specific customer  
6. Custom email logic sends the document after passing all validations.
7. All processing follows controlled business rules to maintain **accuracy, traceability, and communication integrity**.

---

## Customization vs Inbuilt Behavior

### Custom Implementation
- Custom RDLC layout and dataset preparation  
- Technical AL customization to retrieve **Shortcut Dimension 5 and 6**, which are not available directly in standard reporting  
- Customer-wise grouping for multi-record processing  
- Controlled single-email dispatch per customer  
- Validation logic before report generation and email sending  
- Custom header integration within the RDLC design  
- Dataset exchange logic between application layer and report builder  

### Reused Standard Capabilities
- Base service transaction data model  
- Core reporting framework execution  
- Standard email infrastructure  
- Security and permission handling  
- Report rendering pipeline  

This ensures **deep customization without altering base application behavior**.

---

## RDLC Reporting Architecture

- A **fully customized RDLC layout** is created for the service pro forma.
- The report includes:
  - Structured service and customer details  
  - Shortcut dimension values (including 5 & 6 via AL logic)  
  - Financial and descriptive data  
  - Branded header integration  
- Header rendering requires **dataset exchange methods** between the application and report designer to correctly display dynamic customer-specific information.

---

## Email Processing Logic

Key constraints handled by the solution:

- Multiple selected service records  
- Different customers within the same selection  
- Requirement of **single consolidated email per customer**  
- Correct attachment mapping for each generated pro forma  
- Validation before dispatch  

Custom logic orchestrates grouping, report generation, and controlled sending to maintain **data correctness and professional communication**.

---

## Key Features

- One-click Service Pro Forma generation  
- Fully customized RDLC document design  
- Retrieval of **Shortcut Dimension 5 & 6 via AL customization**  
- Intelligent customer-wise email consolidation  
- Secure validation before communication  
- Clean separation of custom logic from base functionality  
- Extensible and maintainable architecture  

---

## Business Impact

- Streamlines customer communication for service transactions  
- Reduces manual document preparation and email effort  
- Ensures accurate dimensional and transactional visibility in shared documents  
- Improves operational efficiency and professionalism  
- Maintains audit-ready reporting and traceability  

---
---

## Author

**Manav Kharvasiya** 
