## 🔑 Core Functionalities

These are the **main features** that define how the system operates for users, hosts, and admins.

---

### 1. 👥 User Management

#### **User Registration**
- Allow new users to register as either **guest** or **host**.  
- Store user information securely in the database.  
- Use **JWT (JSON Web Tokens)** for authentication and session management.  

#### **User Login & Authentication**
- Enable login with **email and password**.  
- Support **OAuth login** using Google or Facebook.  
- Include password encryption using libraries like `bcrypt`.  

#### **Profile Management**
- Allow users to update their profile details (name, contact, preferences, photo).  
- Hosts can add additional information like verification status and hosting rules.  
- Store profile images using **file storage** (e.g., AWS S3 or local storage).  

---

### 2. 🏠 Property Listings Management

#### **Add Listings**
- Hosts can create property listings with:  
  - Title and description  
  - Location (city, address, coordinates)  
  - Price per night  
  - Amenities (Wi-Fi, pool, parking, etc.)  
  - Photos and availability dates  

#### **Edit / Delete Listings**
- Hosts can update listing information or remove properties they no longer wish to offer.  
- Validation ensures only the **property owner (host)** can modify or delete their listings.

---

### 3. 🔍 Search and Filtering

#### **Search Functionality**
- Allow guests to search for properties by:
  - Location  
  - Price range  
  - Number of guests  
  - Amenities (e.g., Wi-Fi, pet-friendly, pool)  

#### **Filtering and Pagination**
- Implement filtering to refine search results.  
- Add pagination or infinite scroll to handle large datasets efficiently.  

---

### 4. 📅 Booking Management

#### **Booking Creation**
- Guests can book a property by selecting start and end dates.  
- Validate booking dates to prevent double-booking.  
- Automatically calculate total price based on `price_per_night` and duration.  

#### **Booking Cancellation**
- Guests and hosts can cancel bookings based on the cancellation policy.  
- Track changes with timestamps and update availability.  

#### **Booking Status Tracking**
- Manage booking statuses:  
  - `pending` – awaiting host confirmation  
  - `confirmed` – accepted by host and paid  
  - `canceled` – canceled by guest or host  
  - `completed` – after checkout  

---

### 5. 💳 Payment Integration

#### **Payment Processing**
- Integrate secure payment gateways (e.g., **Stripe**, **PayPal**) for:  
  - Guest payments on booking confirmation  
  - Host payouts after booking completion  

#### **Features**
- Handle multiple currencies.  
- Store payment transaction references securely.  
- Implement refund mechanism for cancellations.  

---

### 6. ⭐ Reviews and Ratings

#### **Review System**
- Guests can rate and review properties after a completed booking.  
- Hosts can respond to guest reviews.  
- Ensure reviews are linked to specific bookings to prevent spam or abuse.  
- Implement moderation for inappropriate content.  

---

### 7. 🔔 Notifications System

#### **Notification Types**
- Send **email** and **in-app notifications** for:  
  - Booking confirmations and updates  
  - Payment success or failure  
  - Booking cancellations  
  - Review responses  

#### **Implementation**
- Use email services like **SendGrid** or **Mailgun**.  
- In-app notifications handled via API endpoints or WebSockets.  

---

### 8. 🧑‍💼 Admin Dashboard

#### **Admin Capabilities**
- Monitor all platform activity:  
  - Users (guests, hosts, admins)  
  - Listings and reviews  
  - Bookings and payments  
