# Automated-Job-Application-Screening-Interview-Scheduling
📌 Workflow Overview

This workflow has three major stages:

Receive & Clean Application Data

AI-Powered CV Screening & Shortlisting

Interview Scheduling + Email Notifications

Each stage is fully automated, eliminating manual review and communication.

🔶 1. Receive Job Applications
Nodes Involved

Webhook

JavaScript Code Node

HTTP Request

JavaScript Code Node #2

How It Works

Applications are submitted through an online form (e.g., JotForm / Website form).

The Webhook captures the incoming application data instantly.

JavaScript nodes clean and structure the data:

Remove empty fields

Format text and data types

Prepare the final payload

HTTP Request node retrieves the applicant’s uploaded CV file.

This ensures every application enters the system in a clean, standardized format.

🔶 2. AI-Powered CV Screening
Nodes Involved

AI Agent

Google Gemini Chat Model

JavaScript Code Node #3

IF Node

Send Message (Not Shortlisted)

How It Works

The CV text is passed into the AI Agent connected with Google Gemini.

The AI performs:

Skill extraction

Experience evaluation

Role suitability scoring

Profile summary generation

Based on the AI score:

Score ≥ 7 → Shortlisted

Score < 7 → Auto email: “You are not shortlisted”

This removes manual screening entirely and ensures consistent, bias-free evaluation.

🔶 3. Interview Scheduling & Notifications
Nodes Involved

Create Record (Database)

Send Gmail Message #1 (Shortlisted Mail)

Google Calendar → Create Event

Send Gmail Message #2 (Confirmation)

Wait Node

Send Gmail Message #3 (Reminder)

Respond to Webhook

How It Works

If the candidate is shortlisted:

Create Record
Candidate info is stored in a database (Airtable / Google Sheets / Supabase).

Shortlisted Email
A Gmail message informs them they have been shortlisted and their interview is being scheduled.

Calendar Event Creation
The workflow automatically books an available interview slot in Google Calendar.

Interview Confirmation Email
Candidate receives:

Interview date & time

Video call link

Meeting instructions

Reminder Email
Before the interview, the system sends a timed reminder.

Respond to Webhook
n8n returns a final response confirming workflow execution.

🎯 Main Features

✔ Fully automated CV screening
✔ AI scoring using Google Gemini
✔ Automatic interview scheduling
✔ Smart email communication for every stage
✔ Automated reminders
✔ Zero manual intervention
