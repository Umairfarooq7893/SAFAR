# SAFAR
 (3 interfaces + 1 backend)
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   OWNER     │     │   DRIVER    │     │   PARENT    │
│  (Web App)  │     │ (Mobile Web)│     │ (WhatsApp)  │
└──────┬──────┘     └──────┬──────┘     └──────┬──────┘
       │                   │                   │
       └───────────┬───────┴───────────────────┘
                   │
            ┌──────▼──────┐
            │   BACKEND   │
            │  + Database │
            └─────────────┘

##1. OWNER WEB APP (Main Product)
A. Login / Signup
Phone number + OTP
Owner profile (name, city)

B. Dashboard (Home)
Today's summary: "4 cars running, 18 students, 2 pending pickups"
Live map showing all cars moving
Alert list: "Car 2 driver late by 10 min", "Student A not confirmed pickup"

C. Cars Management

Add car: number plate, model, capacity
Assign driver to car
Status: active / inactive

D. Drivers Management
Add driver: name, phone, license photo upload
Assign to car
View driver's daily log

E. Students Management
Add student: name, photo, class/college, pickup address, drop address, parent phone
Assign student to a car/route
Monthly fee amount + payment status

F. Routes & Schedule
Create route: pickup points + times
Assign route to car + driver
Set morning/evening timing separately

G. Live Tracking
Map with all cars as moving dots
Click car → see driver name, students inside, current stop
Timeline: "7:30 picked Student A → 7:45 picked Student B → 8:10 reached college"

H. Fee Ledger
Table: Student | Month | Amount | Paid/Pending
Mark as paid button
Auto-reminder send button (sends WhatsApp to parent)

I. Alerts / History

Log of all pickups/drops with timestamps
Missed pickups highlighted in red


##2. DRIVER MOBILE WEB (Simple)
A. Login
Phone + OTP (once)
B. Today's Route Screen (Only Screen That Matters)
┌────────────────────────────┐
│  CAR 3 — Morning Route     │
│  ─────────────────────     │
│  □ 7:30  Student A         │
│  □ 7:45  Student B         │
│  □ 8:00  Student C         │
│  ─────────────────────     │
│  [ 🟢 START ROUTE ]        │
└────────────────────────────┘
C. When Route Starts → Each Stop Shows:
┌────────────────────────────┐
│  NEXT STOP: Student A      │
│  📍 Green Park, Gate 2     │
│                            │
│  [ ✅ PICKED UP ]          │
│  [ ❌ NOT AVAILABLE ]      │
└────────────────────────────┘
One tap → parent gets WhatsApp alert automatically
No typing. No map reading. No complexity.

D. End Route Button

"Route Complete" → owner gets summary

That's it. 3 buttons total. If driver needs more than this, you've failed.
