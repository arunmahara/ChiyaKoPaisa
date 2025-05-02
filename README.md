# ChiyaKoPaisa

## Product Requirements Document (PRD)

**Project Title:** Nepali Content Creator Support Platform (**"ChiyaKoPaisa"**)

**Version:** 1.0 **(MVP)**

**Last Updated:** May 2, 2025

---

### **1. Overview**

**Goal:**

To create a simplified crowdfunding tool for Nepali content creators that allows them to receive financial support from fans via short URLs that redirect to a donation/payment page. Integrate local payment gateways (Esewa, Khalti) and bank transfers, and automate post-donation interactions such as email notifications and YouTube comment updates.

**Inspiration:**

The idea was born from observing repeated comments on YouTube where viewers expressed a desire to support content creators financially. Many creators do not have accessible monetization channels, especially in Nepal. This platform aims to bridge that gap with a local-first, creator-friendly tool.

<img src="https://github.com/user-attachments/assets/e52979da-5428-4fb9-afda-32f77db24be2" name="project_kura" width="500"/>
<img src="https://github.com/user-attachments/assets/cebe264e-8689-4c9b-93c5-df936fb56180" name="the_nepali_comment" width="500"/>

**Target Audience:**

* Nepali YouTubers, Instagram influencers, Facebook content creators
* Fans and supporters of these creators

---

### **2. Key Features**

#### 2.1. **Creator Registration & Profile Setup**

* Email/password or Google login
* KYC verification (optional in MVP)
* Set up preferred payout method: Esewa, Khalti, Bank Account
* Create personal short support URL (e.g., ChiyaKoPaisa.com/@creatorname)

#### 2.2. **Short URL & Support Page**

* Each creator receives a unique short URL
* URL redirects to a donation/payment form:

  * Amount selection
  * Optional message (public)
  * Donor’s YouTube name (optional field)
  * Select payment method (Esewa, Khalti, Bank via manual QR)

#### 2.3. **Payment Processing**

* Integration with Esewa and Khalti SDK/APIs
* Manual or automated Bank transfer instructions
* After successful payment, trigger confirmation logic

#### 2.4. **Post-Support Workflow**

* Send email to creator and supporter
* Generate a message in the format:

  ```
  $100 Support received from @John_Doe: "I liked your content"
  ```
* Append the message to a **pinned comment** on the referred YouTube video/content (from creator’s account)

#### 2.5. **Pinned Comment Automation (YouTube)**

* Creator connects their YouTube channel (OAuth)
* Create a pinned comment if not exists
* Append new support messages under the pinned comment (via YouTube API)

#### 2.6. **Creator Dashboard**

* Login panel (email/password/Google)
* View total earnings
* List of supporters with amount, date, message
* Export support data (CSV)
* Update payment settings

#### 2.7. **User Journey (Supporter)**

* Click on short URL
* Fill in name/message (optional)
* Choose payment method and complete payment
* Receive email confirmation

---

### **4. Future Enhancements**

* Recurring support/subscription model
* Analytics for creators
* Mobile app for creators
* Support for Facebook/Instagram comment automation
* Leaderboard for top supporters

---

### **5. Risks & Assumptions**

* YouTube API rate limits for comment updates
* Esewa/Khalti may have transaction delays or restrictions
* Creators must maintain active YouTube OAuth token access
* Comment automation may break due to platform policy changes

---

### **6. Stakeholders**

* Project Owner: ChiyaKoPaisa
* Developer Team: Backend, Frontend, DevOps
* Creators: Platform users
* Supporters: End customers/donors

---

### **7. KPIs (MVP Phase)**

* Number of registered creators
* Total donation volume
* Supporter conversion rate
* Uptime of the comment automation script

---

### **8. Legal & Compliance**

* Ensure compliance with NRB (Nepal Rastra Bank) guidelines
* Privacy policy for user data
* Terms of service agreement for creators and donors
