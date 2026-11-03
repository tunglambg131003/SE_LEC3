# Restaurant Manager Personas (SoopiFood Discovery)

## 1. Mateo, the Floor-First Manager

Mateo prioritizes the dine-in customer experience above all else. He views delivery orders as a necessary but disruptive revenue stream and resents when delivery logistics interfere with the dining room's ambiance. His primary focus is shielding his floor staff and seated guests from delivery-related chaos.

### Goals
- Maintain a seamless, premium, and uninterrupted dining experience for in-house guests. `[I1, I4, O1]`
- Ensure kitchen pacing remains predictable and manageable for the back-of-house staff. `[I2, I4, O2]`
- Protect the brand's reputation for culinary quality, which he feels is often compromised by extended delivery transit times. `[I7, I8]`

### Behaviours
- Routinely turns off the delivery tablet or artificially extends prep times during dinner rushes to throttle order volume. `[I1, I4, O1]`
- Instructs front-of-house staff to prioritize walk-in customers and seated guests over waiting delivery riders. `[I2, O1, O2]`
- Directs delivery riders to wait outside or in an out-of-the-way corner to keep them away from the main host stand. `[I6, O1]`

### Pain Points
- Riders crowding the entrance and creating a chaotic, stressful atmosphere for arriving dine-in guests. `[I2, I6, O1, O2]`
- Tablet alerts pinging loudly and distracting front-of-house staff during active service. `[I4, O1]`
- Having to spend valuable time investigating complaints for cold food when he knows the rider was late picking it up. `[I7, I8]`

### Context
- Works in a mid-tier to upscale sit-down restaurant with high daily foot traffic. `[I1, I2, I4]`
- The restaurant's physical layout lacks a dedicated staging or waiting area for delivery orders. `[O1, O2]`
- Evaluated by ownership primarily on dine-in sales and online dining reviews rather than delivery volume. `[I8]`

---

## 2. Sarah, the High-Volume Orchestrator

Sarah runs a fast-paced kitchen where delivery constitutes a massive portion of daily sales. She treats the restaurant like a well-oiled machine, relying heavily on timing, strict processes, and data to push out maximum orders. Her biggest enemy is operational unpredictability that breaks her staff's rhythm.

### Goals
- Maximize total daily order throughput to meet aggressive revenue targets. `[I3, I5]`
- Minimize order turnaround time to maintain high visibility and algorithmic ranking on the delivery app. `[I3, I8]`
- Create frictionless, zero-contact handoffs to keep the pickup and staging area completely clear. `[I5, I6]`

### Behaviours
- Constantly monitors tablet metrics, adjusting prep times dynamically based on real-time kitchen capacity. `[I3, I5, O2]`
- Pre-packages high-demand items and sauces during slower periods to accelerate assembly during the rush. `[I1, O2]`
- Strictly enforces rider pick-up protocols, refusing to hand over food until the rider confirms the order number. `[I6, O2]`

### Pain Points
- Menu items running out mid-service, requiring tedious manual cancellations and refunds on the tablet. `[I3, I5, I7]`
- Riders arriving much earlier than quoted prep times and crowding or pressuring kitchen staff. `[I5, I6, O2]`
- Discrepancies between the tablet's estimated driver arrival time and the actual arrival time, causing packaged food to sit under heat lamps. `[I6, I8]`

### Context
- Manages a fast-casual restaurant or hybrid ghost kitchen optimized heavily for takeout. `[I3, I5]`
- Relies on a large, dedicated counter specifically built for bagging and staging delivery orders. `[O2]`
- Manages kitchen staff with high turnover, requiring workflows to be extremely standardized and easy to learn. `[I5, I8]`

---

## 3. David, the Omnipresent Operator

David manages a smaller, independent spot where he acts as the expeditor, host, and delivery coordinator simultaneously. Because he lacks a large staff to delegate tasks to, he constantly bounces between the floor and the tablet. He needs the delivery system to act as a reliable assistant rather than another chore.

### Goals
- Keep the restaurant profitable with minimal overhead and lean staffing. `[I5, I8]`
- Prevent costly food waste and order remakes caused by miscommunications. `[I4, I7]`
- Build personal rapport and loyalty with customers, even when they order through a third-party app. `[I7, I8]`

### Behaviours
- Personally bags and checks every single delivery order to guarantee accuracy before handoff. `[I2, I6, O1]`
- Calls customers directly via phone if an item is out of stock, preferring human interaction over app-based chat features. `[I3, I7, O1]`
- Manually transcribes delivery orders from the tablet into the kitchen's main POS system to keep all tickets in one place. `[I2, O1, O2]`

### Pain Points
- Time-consuming double-entry required to punch tablet orders into the restaurant's native POS. `[I2, I4, O1]`
- Navigating complex, multi-step menus to process a partial refund when a customer calls the store to report an issue. `[I4, I7]`
- Lack of time to train his skeleton crew on how to troubleshoot the tablet when he steps off the floor. `[I5, I8]`

### Context
- Operates a small, independent neighborhood restaurant with very tight profit margins. `[I5, I7]`
- Works with a minimal "skeleton" crew during most shifts. `[I4, I5, O1]`
- Uses legacy kitchen equipment and POS systems that do not integrate automatically with third-party apps. `[I2, O1]`

---

## Distinctions Note
These personas represent three distinct operational philosophies:
1. **Mateo (Protective):** Views delivery as a secondary revenue stream and a potential threat to in-house dining ambiance; prioritizes floor guest satisfaction over delivery speed.
2. **Sarah (Throughput-Driven):** Views delivery as an industrial assembly line; prioritizes speed, metrics, algorithmic ranking, and zero-contact efficiency.
3. **David (Resource-Constrained):** Operates as a hands-on generalist wearing multiple hats simultaneously; prioritizes simplicity, direct communication, and avoiding costly errors.

