Gharpayy CRM - Lead Management System (MVP)
🚀 Overview-
            This repository contains the Minimum Viable Product (MVP) for the Gharpayy Lead Conversion System (LCS). The solution is designed to move Gharpayy from fragmented, manual WhatsApp-based lead handling to a centralized, automated pipeline that ensures every lead is captured, assigned, and tracked to conversion.
            
Live Demo: https://thakurharshsingh914027-del.github.io/gharpayy-crm-mvp.1/

🛠️ Technical Choices-
Tailwind CSS: Used for rapid, responsive UI development to meet the 48-hour deadline while maintaining a professional "product" feel.SortableJS: Integrated to provide a seamless drag-and-drop experience across the 8-stage sales pipeline, fulfilling the requirement for manual stage transitions.Vanilla JavaScript: Chosen for the MVP to demonstrate core logic without the overhead of heavy frameworks, focusing on "System Thinking" over boilerplate.

🏗️ System Architecture-The system is designed as an automated bridge between lead sources and agent operations.

Lead Ingestion: A webhook-ready architecture designed to listen to sources like Tally, Google Forms, and Calendly.Automated Assignment: Implements a Round Robin engine to ensure immediate, one-to-one ownership of every new lead, solving the issue of "multiple agents responding to the same lead".Proactive Monitoring: A background logic layer that triggers Day 1 follow-up reminders if a lead remains in the "New Lead" stage for more than 24 hours.
📊 Database Design (Proposed)-
To ensure scalability and data integrity, the system utilizes a relational schema:Leads Table: id, name, phone, source, timestamp, assigned_agent_id, status .Agents Table: id, name, current_workload, is_active.Visits Table: id, lead_id, property_name, visit_time, outcome_status.Activity Logs: A historical timeline of lead interactions to allow for the future reuse of "Historical Leads".

📈 Production Scalability-
WhatsApp API Integration: Transitioning from "Shared WhatsApp" to the official API to centralize all conversations within the Lead Profile.Redis Queuing: To handle high-concurrency lead spikes during peak student admission seasons in Bangalore.Microservices: Separating the "Lead Capture" service from the "Analytics Dashboard" to ensure high availability.
💻 How to Run Locally-
Clone this repository:- 
git clone https://github.com/thakurharshsingh914027-del/gharpayy-crm-mvp.1.git
Open index.html in any modern web browser.
