# IBD Recipe Platform - Case Study

---

## 📋 Problem Statement

The members of the non-profit organization want to introduce a section called **Recipe** to their website which can help the **IBD (Inflammatory Bowel Disease)** community to cook their own recipes based on their preferences and allow others to contribute pertaining to the context.

---

## 🧭 Product Name & Primary Goals

### Product Name
**Recipe**

### Primary Goals

- **Increase awareness** of the best available recipes for IBD patients and related personas.
- **Make the platform content-driven** by engaging the global IBD community.
  - *Example:* A doctor or nutritionist can post recipes that work best for IBD patients.

---

## 👥 Target Group

| User Role      | Description |
|---------------|-------------|
| **Patient**    | Looking for recipes to cook and keep symptoms in control |
| **Care Giver** | Searching for recipes on behalf of patients |
| **Contributor**| Nutritionists, Doctors, Experts who want to add recipes |
| **Admin**      | Filters and approves recipes submitted by contributors |

---

## 🌟 Big Picture

### Unique Value Proposition
- Customized ingredient and diet-based recipe suggestions
- Nutritional calculation of calorie intake per serving

### Channels
- Online Channels
- Pop-up Notifications
- Promotional Emails
- Release Notes

### Resources
- Utilizing existing internal resources, patents, copyrights

---

## 🧩 Product Details

**On the Recipe Page:**

- ✅ Checklist to select ingredients (vegetables, flour, beverages, pulses, oil)
- ✅ Checklist for allergies / diet filters (Low-salt, Low-fiber, Low-fat, Lactose-free, High Calorie, etc.)
- ✅ Display full recipe
- ✅ Nutritional Calculator

---

## 🧱 Case Study Framework

1. List Assumptions / Limiting Scope
2. Create Use Case Diagram
3. Create AS-IS Workflow Diagram
4. Create TO-BE Workflow Diagram
5. Create User Stories / Acceptance Criteria
6. Create Prototypes

---

## 🔍 Scope & Assumptions

### Current State (AS-IS)
- Providers/caregivers refer patients to external resources (blogs, FB, external websites)
- Printed materials available in-office but cannot be distributed via email or mail

### In-Scope
- Recipe preparation instructions + Video

### Out-of-Scope
- User registration (assumes users are already registered)

---

## 📊 Workflow Diagrams

### AS-IS Workflow (Current State)
Patient → Searches external sites → Finds recipe → No personalization → No feedback loop

## AS-IS Workflow
![AS-IS Workflow](diagrams/AS-IS.png)

### TO-BE Workflow (Future State)
User logs in → Filters by diet → Views personalized recipes → Submits/rates/feedback → Admin approves → Content published

### High-Level End-to-End Workflow
Contributor submits recipe → System identifies role → Auto-publish (if privileged) / Admin Approval → Recipe visible → Patient filters & views → Rates & feedback

### Patient Workflow (High Level)
Login → Apply diet filters → Browse recipes → View recipe & nutrition → Rate / Share / Save

### Admin Workflow (High Level)
Login → View pending recipes → Approve/Reject → Send notification → Monitor dashboard

---

## 📦 Product Backlog

1. **Submit new recipe**
   - Button on website: "Submit New Recipe"
   - Identify user type (Doctor, Patient, Caregiver, Nutritionist)
   - Create form with required fields
   - Add diet-based filters (Low Carbs, Low Sugar, etc.)
   - Optional fields support

2. Review/use recipes based on diet needs

3. **Feedback on recipe**
   - Text feedback (up to 200 characters)
   - Star rating (1 to 5)

4. **Filter recipes**
   - Select diet type to filter recipes
   - Save preferred filters

5. Approve recipe submitted

6. Email recipe to patient

7. Email recipe to friend

8. Share on social media

9. Dashboard of usage

10. Admin Approval Process – Approval

11. Admin Approval Process – Notification Messages

12. Admin Approval (general)

---

## 🧠 Organizing Requirements

- **Feature:** Recipes section on website
- **Epics:**
  1. Admin Panel to approve recipes
  2. Submit new recipes
- **User Story:** Form to submit new recipes
- **Task:** (Development breakdown)

---

## 📝 User Story Format
As a <USER>, I want <FUNCTIONALITY> so that <JUSTIFICATION>

### Example

> As a **Patient**, I want to **log into my patient record from home** so that **I can check my appointment.**

**Acceptance Criteria (Given-When-Then):**

- **Given** – That I log into the portal successfully  
- **When** – I see a tab for appointment and click on it  
- **Then** – I am able to see all of my past and future appointments

---

## ✅ User Stories with Acceptance Criteria

### a) Button to "Submit New Recipe"

**User Story:**  
As a Patient, I want to click on "Submit New Recipe" so that I can submit new recipes for review.

**Acceptance Criteria:**

- **Given** – Patient is registered, logged in, and on recipe page  
- **When** – Clicks "Submit New Recipe"  
- **Then** – "New Recipe Form" is displayed

---

### b) Identify User Type Submitting Recipe

**User Story:**  
As an Admin, I want the system to identify the user type so that approval rules can be applied.

**Acceptance Criteria:**

- **Given** – User is logged in and submitting a recipe  
- **When** – User selects role from dropdown  
- **Then** – System stores role for workflow

- **Given** – Role is Doctor with privilege  
- **When** – Recipe is submitted  
- **Then** – Auto-published without approval

- **Given** – Role is Patient or Caregiver  
- **When** – Recipe is submitted  
- **Then** – Sent for admin approval

---

### c) Submit Recipe Form – Required Fields

**User Story:**  
As a Contributor, I want a structured form with mandatory fields so that complete recipes are submitted.

**Acceptance Criteria:**

- **Given** – User opens new recipe form  
- **When** – Required fields (Title, Ingredients, Instructions, Diet Type) are empty  
- **Then** – Submit button is disabled

- **Given** – All required fields are filled  
- **When** – User clicks Submit  
- **Then** – Recipe is successfully submitted

---

### d) Filter Recipes Based on Diet Type

**User Story:**  
As a Patient, I want to filter recipes by diet type so that I can find suitable recipes easily.

**Acceptance Criteria:**

- **Given** – Patient on recipe page  
- **When** – Selects "Low-Fiber" filter  
- **Then** – Only Low-Fiber recipes are displayed

---

### e) Provide Rating and Feedback

**User Story:**  
As a Patient, I want to rate and give feedback so that others can benefit from my experience.

**Acceptance Criteria:**

- **Given** – Patient has viewed a recipe  
- **When** – Selects rating (1-5 stars)  
- **Then** – Rating is stored and displayed

- **Given** – Feedback exceeds 200 characters  
- **When** – Patient tries to submit  
- **Then** – Error message is shown

---

### f) Save Preferred Filters

**User Story:**  
As a Patient, I want to save my diet preferences so I don't have to reselect them every time.

**Acceptance Criteria:**

- **Given** – Patient selects filters  
- **When** – Clicks "Save Preferences"  
- **Then** – Preferences are stored in user profile

---

### g) Admin Approval Process

**User Story:**  
As an Admin, I want to review submitted recipes so that only safe and verified content is published.

**Acceptance Criteria:**

- **Given** – Recipe submitted by Patient  
- **When** – Admin logs into dashboard  
- **Then** – Sees pending approval list

- **Given** – Admin approves recipe  
- **When** – Approval is confirmed  
- **Then** – Recipe is visible on the website

- **Given** – Admin rejects recipe  
- **When** – Rejection reason is entered  
- **Then** – Notification email is sent to contributor

---

## 🚀 MVP Definition

**Minimum Viable Product Includes:**

- Recipe submission form
- Diet filter functionality
- Admin approval workflow
- Rating and feedback
- Nutritional calculator (basic)

---

## ⚠️ Risks & Dependencies

- Accuracy of nutritional calculation
- Content moderation workload
- Data privacy compliance (HIPAA alignment)
- Scalability for high content volume

---

## 📈 Success Metrics (KPIs)

- Number of recipes submitted per month
- Recipe approval rate
- User engagement (ratings & feedback)
- Reduction in external referrals
- Repeat user visits

---

## 🏁 Final Conclusion

The **Recipe** feature enables the organization to **centralize dietary resources** for IBD patients while **promoting community engagement**.

By introducing **role-based content submission**, **structured approval workflow**, and **personalized filtering**, the platform becomes a **trusted and scalable solution** for patient-focused dietary support.

---
