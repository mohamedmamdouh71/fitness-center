# Fitness Center — Iron House

A gym website and front-desk system in a single HTML file. No build step, no server: open `index.html` in a browser and it runs.

The interface is Arabic first with full right-to-left layout, and an English toggle. Prices and dates always use Western digits (0-9). Money is in Egyptian pounds.

## Two parts, one file

**Main page** (what the link opens): open/closed status, how busy the gym is right now, programs, memberships, the weekly timetable, coaches and opening hours. Booking buttons open WhatsApp with a ready-written message.

**Front desk** (the "Staff login" button, at `#/desk/dashboard`):

- **Today** — active members, memberships expiring within 7 days, check-ins, this month's revenue against last month, renewals due, a 14-day visits chart.
- **Check-in** — search by name, mobile or member ID, then check in. Expired members are sent to renewal; frozen members must be unfrozen first; a second check-in on the same day is blocked.
- **Members** — search that ignores Arabic spelling differences (أ/ا, ة/ه), filters by status, and a details panel with visits, payments, notes, renewal, freeze/unfreeze and a WhatsApp reminder.
- **Plans, classes, trainers, payments** — all editable, and the main page reads from them.
- **Settings** — gym name, WhatsApp number, address, opening hours, language, and restoring or clearing the data.

## Data

This is a prototype. Everything is saved in the visitor's own browser (`localStorage`); nothing is shared between devices and nothing reaches a server. It opens with sample data, marked "Sample data" in the header, which you can clear in Settings.

For real use at the gym, the next step is a database and separate staff logins.
