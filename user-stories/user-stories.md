# 🧩 Airbnb Clone Backend – User Stories

## 📖 User Stories

### 1. 🧍 User Registration and Authentication
**As a guest or host**,  
I want to **register and log in to my account securely**,  
so that I can **access the platform, manage my profile, and interact with the system.**

**Acceptance Criteria:**
- Users can sign up using an email and password.  
- Passwords are stored securely (hashed).  
- Successful login returns a JWT token.  

---

### 2. 🏠 Property Management (Host)
**As a host**,  
I want to **add, update, or remove my property listings**,  
so that I can **make my properties available for booking and control their details.**

**Acceptance Criteria:**
- Hosts can create listings with a title, location, price, and amenities.  
- Hosts can edit or delete only their own listings.  
- The system validates input and prevents incomplete listings.  

---

### 3. 🔍 Search and Booking (Guest)
**As a guest**,  
I want to **search for available properties and book one for specific dates**,  
so that I can **find a suitable place to stay during my travel.**

**Acceptance Criteria:**
- Guests can search using filters (location, price, amenities).  
- The system prevents double-booking of the same property.  
- A booking record is created upon confirmation.  

---

### 4. 💳 Payment Processing
**As a guest**,  
I want to **make a secure payment for my booking**,  
so that I can **confirm my reservation and ensure my stay is guaranteed.**

**Acceptance Criteria:**
- Guests can pay through supported payment gateways (e.g., Stripe, PayPal).  
- The system validates the transaction and updates booking status.  
- Payment details are logged for audit and reporting.  

---

### 5. ⭐ Reviews and Feedback
**As a guest**,  
I want to **leave a review and rating for the property I stayed in**,  
so that I can **share my experience and help others make informed choices.**

**Acceptance Criteria:**
- Reviews are only allowed after a completed booking.  
- Ratings must be between 1 and 5.  
- Hosts can view reviews for their properties.  

---

### 6. 🔔 Notifications and Alerts
**As a guest or host**,  
I want to **receive email notifications for bookings, payments, and cancellations**,  
so that I can **stay informed about updates related to my activity on the platform.**

**Acceptance Criteria:**
- Notifications are triggered for key events (booking, payment, cancellation).  
- Emails are sent through an external service (e.g., SendGrid).  
- The system ensures delivery tracking and error logging.  

---

### 7. 🧑‍💼 Admin Management
**As an admin**,  
I want to **monitor users, properties, and payments**,  
so that I can **maintain system integrity and prevent fraudulent activity.**

**Acceptance Criteria:**
- Admins can view all users, bookings, and transactions.  
- Admins can deactivate users or remove listings.  
- Admin actions are logged for security and compliance.  

---

## 🧠 Summary
These user stories capture the **core backend interactions** from the use case diagram:
- User authentication and registration  
- Property management  
- Search and booking  
- Payment processing  
- Reviews and notifications  
- Admin oversight  

They provide a foundation for defining **API endpoints, database models, and testing criteria** in future development stages.

---