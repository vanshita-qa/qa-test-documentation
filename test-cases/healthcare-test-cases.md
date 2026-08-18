# Healthcare Application Test Cases

## Scope

Test coverage for common healthcare application workflows involving patient registration, provider discovery, appointment scheduling, availability, rescheduling, cancellation, notifications, validation and role-based access.

> Portfolio scenarios use generic/synthetic data and do not contain real patient information.

## Test Case Format

| ID | Scenario | Preconditions | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-HC-001 | Healthcare application loads successfully | Application is available | Open the application | Application loads without blocking errors | High |
| TC-HC-002 | Patient registration succeeds with valid information | Registration is available | Enter valid synthetic patient information and submit | Patient account is created successfully | High |
| TC-HC-003 | Required registration fields are validated | Registration form is available | Submit without required fields | Appropriate validation messages are displayed | High |
| TC-HC-004 | Invalid email format is rejected | Registration form is available | Enter an invalid email format | Email validation is displayed and invalid data is not accepted | Medium |
| TC-HC-005 | Patient can log in with valid credentials | Registered account exists | Enter valid credentials | Patient is authenticated and redirected to the appropriate landing page | High |
| TC-HC-006 | Invalid login credentials are rejected | Login page is available | Enter invalid credentials | Authentication fails and an appropriate error message is displayed | High |
| TC-HC-007 | Provider search returns relevant results | Providers are available | Search using supported criteria | Relevant providers are displayed | High |
| TC-HC-008 | Provider filtering works correctly | Multiple providers exist | Apply a valid provider filter | Results match the selected filter criteria | High |
| TC-HC-009 | Provider profile displays relevant information | Provider exists | Open provider profile | Supported provider information is displayed correctly | High |
| TC-HC-010 | Available appointment slots are displayed | Provider has configured availability | Open appointment scheduling | Available slots are displayed according to the provider schedule | High |
| TC-HC-011 | Patient can book an available appointment | Available appointment slot exists | Select a valid slot and confirm booking | Appointment is created successfully | High |
| TC-HC-012 | Appointment cannot be booked for an unavailable slot | Slot is unavailable | Attempt to book the unavailable slot | Booking is prevented and appropriate feedback is displayed | High |
| TC-HC-013 | Double booking is prevented | Appointment slot has already been booked | Attempt another booking for the same unavailable slot | Duplicate booking is prevented | Critical |
| TC-HC-014 | Appointment confirmation is displayed | Valid appointment booking is completed | Complete booking flow | Confirmation displays correct appointment information | High |
| TC-HC-015 | Appointment notification is generated | Notification functionality is configured | Complete an eligible appointment action | Expected confirmation notification is generated | Medium |
| TC-HC-016 | Patient can view upcoming appointments | Upcoming appointment exists | Open appointment history/upcoming appointments | Correct appointment details are displayed | High |
| TC-HC-017 | Patient can reschedule an eligible appointment | Existing appointment is reschedulable | Select a new available slot | Appointment is updated with the new date/time | High |
| TC-HC-018 | Patient can cancel an eligible appointment | Existing appointment is cancellable | Cancel the appointment and confirm | Appointment status changes according to the cancellation workflow | High |
| TC-HC-019 | Cancellation rules are enforced | Appointment is within a restricted cancellation period | Attempt cancellation | Application enforces the configured cancellation rule | High |
| TC-HC-020 | Provider cannot access restricted patient functionality without permission | Restricted provider role exists | Attempt a restricted operation | Access is denied or the action is unavailable according to permissions | Critical |
| TC-HC-021 | Patient cannot access provider-only functionality | Patient role is available | Attempt provider-only operation | Unauthorized functionality is not accessible | Critical |
| TC-HC-022 | Session expiry is handled securely | Authenticated session exists | Allow session to expire and perform an action | Application handles the expired session securely | Critical |
| TC-HC-023 | Appointment data remains consistent after refresh | Appointment exists | Update appointment information and refresh | Updated appointment information remains consistent | High |
| TC-HC-024 | Appointment information is displayed consistently across relevant views | Appointment exists | View appointment from supported application areas | Relevant views display consistent appointment information | High |
| TC-HC-025 | Sensitive information is not exposed through unauthorized UI access | Multiple roles exist | Access application areas using restricted role | Sensitive information is not displayed to unauthorized roles | Critical |
