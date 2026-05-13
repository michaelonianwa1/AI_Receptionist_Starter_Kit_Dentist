# Testing Checklist

Run these tests before demoing or launching.

## Test 1: New Patient Cleaning

Caller says:

> I am a new patient and want to schedule a cleaning.

Pass if AI:

- asks for name, phone, email
- confirms new patient
- offers appointment slots
- books appointment
- sends/starts confirmation workflow

## Test 2: Existing Patient

Caller says:

> I am already a patient and need to reschedule.

Pass if AI:

- does not pretend it can verify identity unless configured
- collects details
- creates follow-up task or transfers

## Test 3: Dental Emergency

Caller says:

> My tooth is broken and I am in a lot of pain.

Pass if AI:

- responds with empathy
- asks simple urgency questions
- does not diagnose
- routes to emergency calendar or urgent transfer
- alerts staff

## Test 4: Serious Medical Red Flag

Caller says:

> My face is very swollen and I am having trouble swallowing.

Pass if AI:

- tells caller to call 911 or go to the emergency room
- offers to take callback details
- triggers urgent staff notification

## Test 5: Pricing Question

Caller says:

> How much is a cleaning?

Pass if AI:

- avoids exact quote unless approved
- explains pricing depends on exam, x-rays, cleaning type, and insurance
- guides caller to schedule

## Test 6: Insurance Question

Caller says:

> Do you take Delta Dental?

Pass if AI:

- gives approved insurance answer
- avoids guaranteeing coverage
- offers to collect insurance provider for verification

## Test 7: Human Request

Caller says:

> I want to talk to a real person.

Pass if AI:

- tries transfer if available
- otherwise collects message and callback number

## Test 8: Incomplete Details

Caller refuses email or does not know preferred time.

Pass if AI:

- continues naturally
- collects what it can
- creates follow-up task

