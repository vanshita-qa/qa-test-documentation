# SaaS / CRM Test Cases

## Scope

Test coverage for common CRM workflows including contact management, companies, deals, pipelines, search, filtering, permissions, workflow automation and data consistency.

## Test Case Format

| ID | Scenario | Preconditions | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-CRM-001 | CRM dashboard loads successfully | Valid CRM account is available | Open the CRM dashboard | Dashboard loads and relevant widgets/data are displayed | High |
| TC-CRM-002 | Create a new contact | User has permission to create contacts | Open Contacts and select Create Contact | Contact form opens successfully | High |
| TC-CRM-003 | Save contact with valid data | Contact form is open | Enter valid required information and save | Contact is created and appears in the contact list | High |
| TC-CRM-004 | Required contact fields are validated | Contact form is open | Leave required fields empty and attempt to save | Appropriate validation messages are displayed | High |
| TC-CRM-005 | Contact can be searched | Existing contact is available | Search using a unique contact value | Matching contact is displayed | High |
| TC-CRM-006 | Contact details can be updated | Existing contact is available | Open contact and modify an editable field | Updated information is saved and displayed | High |
| TC-CRM-007 | Contact can be deleted when permitted | Existing contact and delete permission are available | Delete the contact and confirm the action | Contact is removed according to the supported deletion flow | Medium |
| TC-CRM-008 | Company can be created | User has company creation permission | Open Companies and create a company with valid data | Company is created successfully | High |
| TC-CRM-009 | Contact can be associated with company | Contact and company exist | Associate the contact with the company | Relationship is displayed correctly on the relevant records | High |
| TC-CRM-010 | Deal can be created | User has deal creation permission | Create a deal with valid information | Deal is created and displayed in the pipeline | High |
| TC-CRM-011 | Deal moves between pipeline stages | Existing deal is available | Move the deal to another valid pipeline stage | Deal appears in the selected stage and stage data is updated | High |
| TC-CRM-012 | Invalid deal data is rejected | Deal creation form is available | Enter invalid or incomplete values | Relevant validation is displayed and invalid data is not accepted | High |
| TC-CRM-013 | CRM search returns relevant results | Multiple records exist | Search using a supported keyword | Relevant records are returned | Medium |
| TC-CRM-014 | CRM filters return correct records | Multiple records exist | Apply a valid filter | Only records matching the selected filter are displayed | High |
| TC-CRM-015 | Multiple filters work together | Compatible filter values exist | Apply multiple filters | Results satisfy all applicable filter conditions | High |
| TC-CRM-016 | Filters can be cleared | At least one filter is active | Clear the applied filters | Default/unfiltered results are restored | Medium |
| TC-CRM-017 | User without permission cannot perform restricted action | Restricted role is available | Attempt the restricted operation | Action is unavailable or access is denied according to the permission model | High |
| TC-CRM-018 | Role permissions are retained after login | Role configuration exists | Log out and log in again | Configured permissions remain effective | High |
| TC-CRM-019 | Workflow triggers correctly | Valid workflow configuration exists | Perform the configured triggering action | Expected workflow action is executed | High |
| TC-CRM-020 | Workflow does not trigger for excluded conditions | Workflow contains exclusion criteria | Perform an excluded action | Workflow does not execute unexpectedly | High |
| TC-CRM-021 | Notification is generated when configured | Notification rule is configured | Perform the triggering action | Expected notification is generated | Medium |
| TC-CRM-022 | Record changes persist after refresh | Existing record is editable | Update a record and refresh the page | Updated data remains available after refresh | High |
| TC-CRM-023 | Record data remains consistent across related views | Related CRM records exist | Update relevant relationship data and inspect related views | Related views display consistent information | High |
| TC-CRM-024 | Duplicate handling follows configured behaviour | Duplicate detection is enabled | Attempt to create a duplicate record | Configured duplicate warning/prevention behaviour occurs | Medium |
| TC-CRM-025 | Session expiry is handled correctly | Session timeout is configured | Allow session to expire and attempt an operation | Application handles expired session securely and provides appropriate navigation/message | High |
