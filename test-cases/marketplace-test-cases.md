# P2P Marketplace Test Cases

## Scope

Test coverage for peer-to-peer marketplace workflows involving buyers, sellers, listings, communication, offers, transactions and listing lifecycle management.

## Test Case Format

| ID | Scenario | Preconditions | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-P2P-001 | Marketplace home page loads | Application is accessible | Open the marketplace | Home page loads with available marketplace content | High |
| TC-P2P-002 | Buyer registration succeeds with valid data | Registration is available | Enter valid registration information and submit | Buyer account is created successfully | High |
| TC-P2P-003 | Seller registration succeeds with valid data | Registration is available | Register using valid seller information | Seller account is created successfully | High |
| TC-P2P-004 | Required registration fields are validated | Registration form is available | Submit the form without required information | Appropriate validation messages are displayed | High |
| TC-P2P-005 | Seller can create a listing | Seller account has listing permission | Create a listing with valid information | Listing is created and appears according to the marketplace workflow | High |
| TC-P2P-006 | Listing requires mandatory information | Seller is creating a listing | Leave mandatory listing fields empty and submit | Required-field validation is displayed | High |
| TC-P2P-007 | Listing can be edited | Existing seller listing is available | Edit listing information and save | Updated listing information is displayed | High |
| TC-P2P-008 | Seller can deactivate a listing | Active listing exists | Use the supported deactivate action | Listing becomes unavailable according to the configured lifecycle | Medium |
| TC-P2P-009 | Buyer can search marketplace listings | Listings are available | Search using a valid keyword | Relevant listings are displayed | High |
| TC-P2P-010 | Marketplace filters return correct results | Listings contain different attributes | Apply a valid filter | Only matching listings are displayed | High |
| TC-P2P-011 | Multiple listing filters work together | Multiple compatible filters exist | Apply multiple filters | Results satisfy the selected filter criteria | High |
| TC-P2P-012 | Buyer can view listing details | Listing is available | Open a marketplace listing | Listing details load correctly | High |
| TC-P2P-013 | Listing displays seller information according to visibility rules | Listing exists | Open listing details | Allowed seller information is displayed correctly | Medium |
| TC-P2P-014 | Buyer can contact seller | Messaging/contact feature is available | Send a valid message to the seller | Message is submitted and displayed according to the messaging flow | High |
| TC-P2P-015 | Seller receives buyer message | Buyer has sent a message | Open seller messages | New message is visible to the seller | High |
| TC-P2P-016 | Buyer can submit an offer | Listing supports offers | Enter a valid offer and submit | Offer is created and associated with the listing | High |
| TC-P2P-017 | Seller can accept an offer | Valid pending offer exists | Accept the offer | Offer status changes to accepted and the next workflow state is initiated | High |
| TC-P2P-018 | Seller can reject an offer | Valid pending offer exists | Reject the offer | Offer status changes to rejected | Medium |
| TC-P2P-019 | Invalid offer value is rejected | Listing supports offers | Submit an invalid offer value | Appropriate validation is displayed and invalid offer is not created | High |
| TC-P2P-020 | Transaction status updates correctly | Transaction has been initiated | Progress through supported transaction states | Transaction status reflects the current workflow state | High |
| TC-P2P-021 | Buyer receives transaction notification | Transaction notification is configured | Trigger a supported transaction event | Expected notification is generated | Medium |
| TC-P2P-022 | Seller receives transaction notification | Seller notification is configured | Trigger a supported transaction event | Expected notification is generated | Medium |
| TC-P2P-023 | Listing lifecycle prevents invalid actions | Listing is in a restricted state | Attempt an action not allowed for that state | Invalid action is prevented | High |
| TC-P2P-024 | Review can be submitted after eligible transaction | Completed/eligible transaction exists | Submit a valid review | Review is submitted according to marketplace rules | Medium |
| TC-P2P-025 | Review cannot be submitted when transaction is ineligible | Transaction does not meet review criteria | Attempt to submit a review | Review submission is prevented with appropriate feedback | Medium |
