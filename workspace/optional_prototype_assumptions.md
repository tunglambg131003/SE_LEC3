# Optional Submission 1: Tablet Prototype Wireframe & Assumption List
**Student Name:** Nguyen Tung Lam  
**Student ID:** V202603373  
**Group:** Group 10  
**Course:** Advanced Software Engineering (AY 26–27) · VinUniversity  
**System:** SoopiFood Restaurant Tablet & Delivery System

---

## 1. Low-Fidelity Tablet UI Prototype (Glanceable Screen)

Designed for busy kitchen counter use, readable from 1.5–2 meters (supporting NFR-05, OI-03, OI-05, RH-01).

```
+---------------------------------------------------------------------------------------------------+
|  SOOPIFOOD RESTAURANT TABLET  [Status: ONLINE]                     Shift: DINNER (18:45)  [PAUSE] |
+---------------------------------------------------------------------------------------------------+
| ACTIVE ORDERS (3)                                 | ORDER DETAILS: #SF-104 (Prep: 12 min left)     |
|---------------------------------------------------|-----------------------------------------------|
| [18:32] #SF-102 | 3 items | Rider Arrived    [OK] | Customer: Linh N.                             |
|                                                   | Contact:  0912-xxx-xxx (masked post-delivery) |
| [18:40] #SF-104 | 2 items | Cooking (12m)   [SEL] | Rider:    Hoang V. (ETA: 10 mins)              |
|                                                   |                                               |
| [18:44] #SF-105 | 1 item  | NEW ORDER!       [NEW]| Items:                                        |
|   * Audible Chime Active   [MUTE ALERT]           |   - 1x Pho Bo Dac Biet (Special Beef Pho)     |
|                                                   |     [!] Notes: No cilantro, extra chili       |
|                                                   |     [!] Allergens: Fish sauce                 |
|                                                   |   - 1x Tra Da (Iced Tea)                      |
|                                                   |                                               |
|                                                   | Subtotal:  110,000 VND                        |
|                                                   | Promo:     WELCOME20 (-22,000 VND)            |
|                                                   | Delivery:  15,000 VND                         |
|                                                   | Total Paid:103,000 VND [PAID VIA E-WALLET]    |
|---------------------------------------------------|-----------------------------------------------|
| QUICK ACTIONS:                                    | ACTION BUTTONS:                               |
| [ +5 Min Prep ]  [ +10 Min Prep ]  [ 86 Item... ] | [ MARK READY FOR RIDER ]   [ CANCEL / REFUND ]|
+---------------------------------------------------------------------------------------------------+
```

---

## 2. Explicit Assumption List

Following the tutorial rule: *"If a reason is your own assumption, not something in the file, say so."*

### Hardware & Operational Environment
1. **Screen & Legibility (NFR-05, NFR-07):** The tablet is assumed to be an Android device with minimum 10-inch diagonal display and 1280x800 resolution. Alerts use high-contrast color cards (Red for new orders, Orange for cooking, Green for rider arrived) to enable glanceability from 2 meters.
2. **Offline Resilience (NFR-02):** Shared restaurant Wi-Fi dropouts are assumed to last between 30 seconds and 15 minutes. The tablet utilizes a local SQLite event store that buffers all manager actions (pause, prep extension, refunds) and syncs bidirectionally upon reconnection using exponential backoff.
3. **Sound Levels in Kitchen (OI-03, OI-04):** Dinner rushes can reach 75–80 dB ambient noise in the kitchen. Audio alerts must be piercing enough to be heard over cooking appliances, but one-tap mutable so floor managers (like Mateo) can silence them when guests enter.

### Domain & Business Rules
4. **Order State Machine (SF-07, KP-01, RH-02):** The order lifecycle progresses through: `PLACED` → `ACCEPTED` → `PREPARING` → `READY_FOR_PICKUP` → `DISPATCHED` → `DELIVERED`. Rider arrival is detected via geofencing and confirmed via manual order number entry.
5. **Currency Arithmetic (D5):** Vietnam Dong (VND) has no fractional units (no cents). All monetary calculations in database, backend services, and front-end displays must strictly use whole integers (`int`), never IEEE-754 floating-point numbers (`float`).
6. **Payment Tokenization (NFR-03):** The tablet application and order service never receive or store primary account numbers (PAN) or CVVs; credit card processing is 100% delegated to a PCI-DSS compliant third-party payment gateway.
7. **GDPR Data Minimization (NFR-08):** In compliance with GDPR Article 5(1)(c), customer phone numbers displayed on the tablet for delivery coordination are automatically masked or wiped 30 minutes after order delivery.
8. **Promo Code Application (R1–R3):** Promo discount applies strictly to the food subtotal and never discounts the delivery fee. The order minimum threshold check (100,000 VND) occurs prior to applying any promotional deduction.
