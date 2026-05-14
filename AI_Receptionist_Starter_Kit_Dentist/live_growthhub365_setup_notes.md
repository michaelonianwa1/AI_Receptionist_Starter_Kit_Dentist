# Live GrowthHub365 Setup Notes

Created on: 2026-05-13

## Agent Created

Agent name:

> Ava - Dental Receptionist

Business name:

> BrightSmile Dental Studio

Location/account:

> Uloaku Akwada's Account

GrowthHub365 path used:

> AI Agents > Voice AI > Create Agent > Create Custom Agent

## Builder Flow Used

1. Agent Details
2. Agent Goals
3. Phone & Availability

## Agent Details Entered

Agent name:

> Ava - Dental Receptionist

Business name:

> BrightSmile Dental Studio

Timezone:

> GMT-05:00 America/Chicago (CDT)

Initial greeting:

> Thank you for calling BrightSmile Dental Studio. This is Ava, the virtual receptionist. How can I help you today?

Voice:

> Jessica, English, American, Female

LLM model shown:

> GPT 4o

## Agent Goals

Mode used:

> Advanced mode

Prompt:

> Dentist receptionist prompt inserted directly into the "Prompt for the agent" field.

Action added:

> Appointment Booking

Calendar selected:

> AI Receptionist Calender

Offering window shown:

> 3 days

Post-call setting:

> Add call summary as a note to the contact was left enabled.

Email notification:

> All Admins was selected by default.

## Phone & Availability

Phone number:

> No phone number was attached during setup.

Testing option shown:

> Start Web Call

On-screen cost estimate:

> $0.137 per minute (Basic)

On-screen test allowance:

> 20 minutes left today

## Current Status

The agent was saved successfully and appears in the Voice AI Agent List as:

> Ava - Dental Receptionist

Channel:

> N/A

Last updated:

> 13 May 2026, 1:56 PM

## Next Steps

1. Open the agent from Agent List.
2. Use Start Web Call to test if you are comfortable using voice minutes.
3. Test these scenarios:
   - new patient cleaning request
   - emergency tooth pain
   - insurance question
   - price question
   - caller asks for a human
4. For a stronger dentist demo, create dedicated calendars:
   - New Patient Exam and Cleaning
   - Emergency Dental Consult
   - Invisalign Consultation
   - Teeth Whitening Consultation
5. Replace the current booking action calendar with the dentist-specific calendar or multi-calendar setup.
6. Attach a phone number only when ready for inbound calls or client demo forwarding.

## 2026-05-13 Calendar Update

Created active dentist demo calendars in GrowthHub365:

- NEW PATIENT EXAM AND CLEANING
- TEETH WHITENING CONSULTATION
- INVISALIGN CONSULTATION
- EMERGENCY DENTAL CONSULTINVISALIGN CONSULTATION

The emergency calendar name should be cleaned up later to:

> EMERGENCY DENTAL CONSULT

The merged name happened during browser keyboard entry, but it is active and was connected as the urgent dental routing calendar.

Updated Ava's Appointment Booking action:

- Connected the new dentist calendars to the booking action.
- The action now displays: `AI Receptionist Calender +4 more`.
- Added intent routing rules for:
  - fallback/general appointment
  - new patient cleaning/exam
  - teeth whitening
  - Invisalign/clear aligners
  - urgent tooth pain/broken tooth/swelling

Recommended next test:

> I am a new patient and want to schedule a cleaning.

Then test:

> I have tooth pain and my cheek is swollen.
