# GrowthHub365 Workflow Blueprints

Build these workflows after the Voice AI agent is created.

## Workflow 1: New Appointment Booked

Trigger:

- Appointment booked from Voice AI

Actions:

1. Add or update contact.
2. Add tag: `AI Receptionist - Booked`
3. Send internal email to front desk:

Subject:

> New AI-booked dental appointment: {{contact.name}}

Body:

> Ava booked a new appointment.
>
> Name: {{contact.name}}
>
> Phone: {{contact.phone}}
>
> Email: {{contact.email}}
>
> Appointment: {{appointment.date_time}}
>
> Reason: {{custom.reason_for_visit}}
>
> Insurance: {{custom.insurance_provider}}

4. Send confirmation SMS to patient:

> Hi {{contact.first_name}}, you're scheduled with {{location.name}} for {{appointment.date_time}}. Please bring your photo ID and insurance card if you have one. Reply STOP to opt out.

5. Create opportunity in pipeline:

Pipeline: Dental New Patient Pipeline

Stage: Appointment Booked

## Workflow 2: Missed Call or After-Hours Lead

Trigger:

- Call completed by Voice AI
- Condition: appointment not booked

Actions:

1. Add tag: `AI Receptionist - Needs Follow Up`
2. Create task for front desk:

> Follow up with {{contact.name}} about dental appointment request.

3. Send SMS:

> Hi {{contact.first_name}}, thanks for calling {{location.name}}. Our team will follow up soon. If this is a medical emergency, call 911.

## Workflow 3: Urgent Dental Issue

Trigger:

- Voice AI call completed
- Condition/tag: `Urgent Dental Issue`

Actions:

1. Add tag: `Urgent Dental Issue`
2. Send internal SMS or email to office manager immediately:

> Urgent dental call from {{contact.name}} at {{contact.phone}}. Summary: {{call.summary}}

3. Create high-priority task.
4. Move opportunity to pipeline stage: Urgent Follow Up.

## Workflow 4: New Patient No-Show Prevention

Trigger:

- Appointment booked

Actions:

1. Send confirmation SMS immediately.
2. Send reminder 24 hours before appointment.
3. Send reminder 2 hours before appointment.

24-hour message:

> Reminder: you have an appointment with {{location.name}} tomorrow at {{appointment.time}}. Reply C to confirm or call us if you need to reschedule.

## Workflow 5: Post-Visit Review Request

Trigger:

- Appointment status marked completed

Actions:

1. Wait 2 hours.
2. Send SMS:

> Thanks for visiting {{location.name}} today. If you had a good experience, would you mind leaving us a quick review? {{review_link}}

