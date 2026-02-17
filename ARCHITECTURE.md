# High-Level Architecture & Design

This document outlines the logical structure of the SSSS Events Portal. More technical implementation details will finalized as we continue on the project.

## 1. System Components
We can envision the portal to be split split into three primary areas:

* **Public Landing:** Event discovery for all students. No login required to browse.
* **Member Dashboard:** Authenticated zone for students to manage their RSVPs and registration QR codes.
* **Admin Command Center:** Restricted zone for event managers to create/edit events and scan participant codes.

## 2. Main Data Entities
Regardless of the database option we choose, we will need to manage these relationships:

| Entity | Key Data Points |
| :--- | :--- |
| **User** | Email, Name, Student ID, Role (Student/Admin) | 
| **Event** | Title, Description, Date/Time, Capacity, Location, Image | 
| **RSVP** | UserID + EventID | (To link a user to an event)

## 3. The MVP Workflow
Instead of a complex scanning systems, our first version of this will focus on:
1.  **Creation:** Admin adds an event (e.g., "Board Game Night").
2.  **Registration:** Student logs in and clicks "Join."
3.  **Check-in:** Admins view a simple text list of "Confirmed Attendees" on a dashboard to verify names at the door.

## 4. Technical Considerations for the Committee
Items to be further discussed and voted on:
* **Tech Stack:** Next.js/React/Tailwind.css/Supabase is the initial consideration, but we can decide further
* **Authentication:** Integration with SFU Computing IDs vs. Third-party providers (Google/GitHub)
* **Database Hosting:** Where will the database live? (Firebase, Supabase, or self-hosted).

---
*Last Updated: February 16 2026*
