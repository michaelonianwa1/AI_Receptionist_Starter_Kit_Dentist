# GrowthHub365 Deployment and Demo Guide

GrowthHub365 appears to use a HighLevel-style setup for AI Agents. The exact labels may vary, but the setup flow should be close.

## Before You Build

Prepare these items:

- office name, address, hours, phone number
- services and FAQs
- booking calendar names and availability
- emergency transfer number
- notification email/phone for office staff
- approved wording for insurance and pricing questions

## Step 1: Create the Dental Location or Sub-Account

If this is a real client, use their location/sub-account.

If this is a demo, create or use a demo location named:

> BrightSmile Dental Studio

## Step 2: Set Up Calendars

Go to Calendars and create these appointment calendars:

1. New Patient Exam and Cleaning
2. Emergency Dental Consult
3. Invisalign Consultation
4. Teeth Whitening Consultation

Recommended demo settings:

- New Patient Exam and Cleaning: 60 minutes
- Emergency Dental Consult: 30 minutes
- Invisalign Consultation: 30 minutes
- Teeth Whitening Consultation: 30 minutes
- Availability: Monday-Friday, 8:00 AM-5:00 PM
- Buffer: 10-15 minutes if available
- Minimum notice: same day or next day depending on the demo

## Step 3: Create the Voice AI Agent

Go to:

> AI Agents > Voice AI > Create Agent

Recommended settings:

- Agent name: Ava - Dental AI Receptionist
- Agent role: Dental receptionist
- Business: BrightSmile Dental Studio
- Voice: friendly, clear, professional
- Working hours: 24/7 for demo, or match the office if client wants after-hours only
- Maximum call time: 5-10 minutes for demo

Paste the content from `voice_ai_master_prompt.md` into the agent instructions. Replace the placeholders with the real office details.

## Step 4: Add Knowledge Base or FAQ Content

Add the content from `knowledge_base_faq.md` if the platform has a knowledge base section.

If there is no knowledge base area, paste the FAQ into the agent instructions under "Office Information" or "FAQ."

## Step 5: Add Appointment Booking Action

In the Voice AI agent, add a new action:

> Appointment Booking

Use single calendar booking if you want the first demo simple:

- Calendar: New Patient Exam and Cleaning
- Offer days: next 7-14 days
- Offer slots: 2-3 options at a time

Use multi-calendar booking if you want a stronger demo:

- New Patient Exam and Cleaning
- Emergency Dental Consult
- Invisalign Consultation
- Teeth Whitening Consultation

Add clear descriptions and trigger phrases for each calendar.

Example trigger phrases:

- New Patient Exam and Cleaning: "new patient", "cleaning", "checkup", "exam", "x-rays"
- Emergency Dental Consult: "tooth pain", "broken tooth", "swelling", "urgent", "emergency"
- Invisalign Consultation: "Invisalign", "clear aligners", "straighten my teeth"
- Teeth Whitening Consultation: "whitening", "brighter smile", "stains"

## Step 6: Add Call Transfer or Message-Taking

If the platform supports call transfer, add a transfer action for urgent cases or "speak to a person."

Transfer conditions:

- Caller asks to speak with the front desk
- Caller reports severe pain or urgent dental concern
- Caller has billing, records, insurance dispute, or complaint
- Caller is upset or confused

Handoff message:

> One moment, I will try to connect you with the office team.

If transfer is not available, configure the agent to collect a message and trigger urgent follow-up.

## Step 7: Build Workflows

Create the workflows from `workflow_blueprints.md`:

1. New Appointment Booked
2. Missed Call or After-Hours Lead
3. Urgent Dental Issue
4. New Patient No-Show Prevention
5. Post-Visit Review Request

Start with the first three. Add reminders and reviews after the demo is working.

## Step 8: Connect Phone Number

For demo:

- Use a test phone number if available.
- If the platform gives a shareable call URL or test call button, use that first.

For client:

- Buy or assign a phone number inside the platform.
- Forward missed calls or after-hours calls from the dental office main line to the AI number.
- Start with after-hours only if the office is nervous.

## Step 9: Run Test Calls

Use `testing_checklist.md`.

Test at least:

- new patient cleaning request
- tooth pain emergency
- insurance question
- pricing question
- caller asks for a human
- caller gives incomplete information

## Step 10: Demo It To The Dentist

Use `demo_script.md`.

Best demo format:

1. Show the problem: missed calls cost new patients.
2. Call the AI agent live.
3. Ask it to book a new patient exam.
4. Show the CRM contact and appointment created.
5. Show the office notification.
6. Explain the monthly offer.

## Important Caution

For dental offices, avoid medical claims. The AI should not diagnose, prescribe, or decide treatment. It should schedule, collect information, and escalate urgent issues.

