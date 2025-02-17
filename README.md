# Microsoft Power Platform Fundamentals (PL-900) Certification Preparation

## Certification Overview  
The **Microsoft Power Platform Fundamentals (PL-900)** certification validates foundational knowledge of the Microsoft Power Platform ecosystem, including its core components and use cases for building automated solutions. Key focus areas include:  
- **Power Platform Architecture**: Power Apps, Power Automate, Power BI, and Copilot Studio.  
- **Solution Development**: Designing low-code applications, automating workflows, and integrating AI-driven chatbots.  
- **Analytics & Business Intelligence**: Leveraging Power BI for data visualization and insights.  

## Training & Preparation  
- Completed a 6-hour instructor-led training session hosted by **DataScientest** on **13.01.2025**, covering platform fundamentals, use cases, and hands-on exercises.  
- Currently preparing for the PL-900 mock exam, focusing on practical implementation scenarios and platform capabilities.  

---

## Project: Client Management Application (Li_App)  
A low-code solution developed using **Power Apps** and **Power Automate** to streamline client/contact management.  

### Technical Implementation  
#### **Core Components**  
1. **Power Apps Canvas App**  
   - **UI Framework**: Responsive design for client data management.  
   - **Data Source**: Connects to a Microsoft Dataverse table for structured storage.  

2. **Power Automate Workflow**  
   - Integrated with **Copilot Studio** to enable conditional logic for email automation.  

#### **Repository Structure**  
- `Li_App`:  
  - Power Apps project files (screens, components, formulas).  
  - Power Automate flows (JSON definitions).  
- Documentation: Screenshots, entity schemas, and workflow diagrams.  

---

### Key Features & Technical Specifications  
#### **1. User Interface (Power Apps)**  
- **Contact List View**  
  - Grid layout displaying client metadata: `Full Name`, `Email`, `Business Sector`.  
  - Dynamic filtering and sorting capabilities.  
- **CRUD Operations**  
  - **Create**: Input form with validation (required fields marked `*`).  
  - **Update/Delete**: Contextual buttons for inline editing (`Edit`, `Remove`).  
- **UI Controls**  
  - `+` Button: Triggers `NewForm()` function for record creation.  
  - `✓` and `×` Buttons: `SubmitForm()` and `ResetForm()` actions for data integrity.  

#### **2. Data Validation & Business Logic**  
- **Dropdowns**: Predefined `Business Sector` options (e.g., Banking, Healthcare) for standardized data entry.  
- **Form Validation**:  
  ```powerapps  
  If(IsBlank(FirstName.Text), "First Name is required", "")  
