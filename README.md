# GroupScreen

An iOS research app studying the psychological effects of shared screen time accountability among peer groups.

Built at Purdue University.

---

## What it does

GroupScreen gives a small group of friends a shared daily screen time budget. Each person picks their own apps to restrict. When someone goes over their individual limit they start spending the group's time — and everyone gets notified with their name. When the budget hits zero, everyone's selected apps are restricted until midnight.

The goal is to study whether shared consequences and peer visibility produce stronger behavior change than individual limits alone.

---

## The three states

| State | Condition | Experience |
|---|---|---|
| 🟢 Normal | Under individual limit | No interruption |
| 🟡 Over limit | Past individual limit, budget remaining | Warning screen on each app open, group notified by name on every dismiss |
| 🔴 Locked | Group budget exhausted | All members' selected apps restricted until midnight |

---

## Tech stack

- Swift / SwiftUI (iOS 16+)
- Apple Family Controls, ManagedSettings, DeviceActivity
- Firebase Firestore, Cloud Messaging, Auth
- Firebase Cloud Functions (Node.js)

---

## Project structure

```
GroupScreen/                  Main app — UI, onboarding, dashboard
GroupScreenMonitor/           Device Activity Monitor extension
GroupScreenShield/            Shield Configuration extension  
GroupScreenShieldAction/      Shield Action extension
functions/                    Firebase Cloud Functions
```

---

## Research design

| Week | Activity |
|---|---|
| 1 — Baseline | Participants use phones normally, submit Screen Time screenshot Sunday |
| 2 — Intervention | App live with full mechanic, daily 3-question check-in form |
| 3 — Debrief | 30-minute individual interviews |

---

## Privacy

See [Privacy Policy](privacy-policy.md)

No per-app usage data leaves the device. Only aggregate seconds-per-day is synced to Firebase. Participant data is anonymized in all research outputs.

---

## Status

🔴 In development — entitlement request submitted, pending Apple approval
