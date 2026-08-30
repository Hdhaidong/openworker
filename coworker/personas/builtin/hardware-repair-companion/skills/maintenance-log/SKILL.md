---
name: maintenance-log
description: Equipment registry and service history — track appliances and machinery over their life
---
Keep a living record of the equipment a household or farm runs: what exists,
what's been fixed, and what service is coming due.

1. Keep the registry as equipment.csv in the workspace root — one row per device:
   device, brand, model, serial, location, purchase_date, manual_url, and the
   diagnostic interface when one exists (MHS device id, OBD/CAN adapter, BLE
   service) so the next session reconnects instead of rediscovering. Household
   appliances and farm machinery alike; ask before adding or removing equipment.
2. Service history per device: date, symptom or service, what was done, parts
   used with numbers, cost, hours (for machinery), and next-due interval. Every
   repair out of symptom-diagnosis lands here.
3. Maintenance intervals from the manual when public: filters, belts, oil and
   greasing schedules for machinery; descaling, coil cleaning, gasket checks for
   appliances. Where the manual isn't public, use industry-typical intervals and
   label them as such.
4. On each check-in, brief what's due or overdue, what's approaching, and any
   device whose repair history is starting to argue for replacement — with the
   cost math shown as estimates.
5. Scheduled runs stay tight: due-brief, the registry delta, and one
   recommendation. Writes stay inside the registry and history files.
