# Regression Test Checklist

## Purpose

This checklist provides reusable regression coverage for critical web application workflows across e-commerce, SaaS/CRM, peer-to-peer marketplace and healthcare applications.

The checklist is intended to be used after feature changes, defect fixes, integrations, configuration changes and release deployments.

---

# 1. Authentication & Session

- [ ] Valid login succeeds
- [ ] Invalid login credentials are rejected
- [ ] Required login fields are validated
- [ ] Logout works correctly
- [ ] Session remains active during normal navigation
- [ ] Expired sessions are handled correctly
- [ ] Unauthorized users cannot access restricted areas
- [ ] Browser back navigation does not expose restricted content

---

# 2. Navigation

- [ ] Application logo navigates to the expected landing page
- [ ] Main navigation links load the correct pages
- [ ] Breadcrumb navigation works correctly
- [ ] Browser back navigation works
- [ ] Browser forward navigation works
- [ ] Direct URL navigation loads the expected page
- [ ] Navigation does not result in blank pages
- [ ] Navigation does not produce unexpected console errors

---

# 3. E-commerce

## Product Listing

- [ ] Product listing loads successfully
- [ ] Products are displayed correctly
- [ ] Product search returns relevant results
- [ ] No-result search displays the appropriate state
- [ ] Product sorting works correctly
- [ ] Product filtering works correctly
- [ ] Multiple filters work together
- [ ] Filters can be cleared
- [ ] Products-per-page selection works
- [ ] Pagination works correctly
- [ ] Product listing remains available after navigation
- [ ] Product listing remains available after browser refresh

## Product Details

- [ ] Product details page loads
- [ ] Product name is displayed
- [ ] Product price is displayed
- [ ] Product images load correctly
- [ ] Product availability is displayed correctly
- [ ] Add to Cart works
- [ ] Product quantity can be updated

## Cart

- [ ] Product can be added to cart
- [ ] Cart quantity can be updated
- [ ] Product can be removed
- [ ] Cart totals are recalculated correctly
- [ ] Cart state persists according to application behaviour

## Checkout

- [ ] Checkout page loads
- [ ] Required fields are validated
- [ ] Valid checkout information is accepted
- [ ] Invalid information is rejected
- [ ] Order summary is correct
- [ ] Order confirmation is displayed

---

# 4. SaaS / CRM

## Contacts

- [ ] Contact list loads
- [ ] Contact can be created
- [ ] Required contact fields are validated
- [ ] Contact can be searched
- [ ] Contact can be edited
- [ ] Contact can be deleted when permitted

## Companies

- [ ] Company list loads
- [ ] Company can be created
- [ ] Company information can be edited
- [ ] Contact-company association works
- [ ] Company search works

## Deals

- [ ] Deal can be created
- [ ] Deal information is saved correctly
- [ ] Deal appears in the correct pipeline
- [ ] Deal can move between valid stages
- [ ] Invalid deal information is rejected
- [ ] Deal information persists after refresh

## Filters & Search

- [ ] Search returns relevant records
- [ ] Filters return correct records
- [ ] Multiple filters work correctly
- [ ] Filters can be cleared
- [ ] Search and filter states behave correctly after navigation

## Roles & Permissions

- [ ] Authorized actions are available
- [ ] Restricted actions are unavailable
- [ ] Unauthorized pages cannot be accessed
- [ ] Permissions remain effective after relogin

---

# 5. P2P Marketplace

## Listings

- [ ] Seller can create a listing
- [ ] Required listing fields are validated
- [ ] Listing can be edited
- [ ] Listing can be deactivated
- [ ] Listing status changes correctly

## Buyer Workflow

- [ ] Buyer can search listings
- [ ] Buyer can filter listings
- [ ] Buyer can open listing details
- [ ] Buyer can contact seller
- [ ] Buyer can submit an eligible offer

## Seller Workflow

- [ ] Seller receives buyer messages
- [ ] Seller can review offers
- [ ] Seller can accept an offer
- [ ] Seller can reject an offer
- [ ] Invalid seller actions are prevented

## Transactions

- [ ] Transaction is created according to the workflow
- [ ] Transaction status updates correctly
- [ ] Buyer receives relevant notifications
- [ ] Seller receives relevant notifications
- [ ] Invalid state transitions are prevented

---

# 6. Healthcare

## Patient

- [ ] Patient registration works
- [ ] Required registration fields are validated
- [ ] Patient login works
- [ ] Invalid login is rejected

## Provider Search

- [ ] Provider search works
- [ ] Provider filters work
- [ ] Provider profile loads
- [ ] Provider availability is displayed correctly

## Appointments

- [ ] Available appointment slots are displayed
- [ ] Appointment can be booked
- [ ] Unavailable slots cannot be booked
- [ ] Duplicate booking is prevented
- [ ] Appointment confirmation is displayed
- [ ] Appointment can be rescheduled when permitted
- [ ] Appointment can be cancelled when permitted
- [ ] Cancellation rules are enforced

## Access Control

- [ ] Patient cannot access provider-only functionality
- [ ] Provider cannot access restricted functionality
- [ ] Restricted information is not exposed
- [ ] Expired sessions are handled securely

---

# 7. Cross-Browser & Responsive Testing

- [ ] Critical workflows work in Chrome
- [ ] Critical workflows work in Firefox
- [ ] Critical workflows work in Edge
- [ ] Responsive layout works on supported viewport sizes
- [ ] Navigation remains usable on smaller screens
- [ ] Forms remain usable on supported devices
- [ ] No major UI overlap or clipping occurs

---

# 8. API & Data Validation

- [ ] Critical API requests return expected status codes
- [ ] API error responses are handled correctly
- [ ] Required request fields are validated
- [ ] Response data matches the UI
- [ ] Created records appear correctly in the UI
- [ ] Updated records remain consistent across views
- [ ] Deleted/inactive records are handled correctly
- [ ] Unauthorized API access is rejected

---

# 9. Defect Verification

For every resolved defect:

- [ ] Original defect can no longer be reproduced
- [ ] Original reproduction steps were executed
- [ ] Positive scenario was verified
- [ ] Negative scenario was verified where applicable
- [ ] Related functionality was regression tested
- [ ] No new critical/high-severity regression was identified

---

# 10. Release Readiness

Before release:

- [ ] Smoke testing completed
- [ ] Critical workflows verified
- [ ] High-risk areas regression tested
- [ ] Fixed defects verified
- [ ] Integration points validated
- [ ] Major browser coverage completed
- [ ] Known risks documented
- [ ] Blocking defects resolved or formally accepted
- [ ] Test results communicated to stakeholders

---

## Regression Prioritization

Regression testing should be prioritized based on:

1. Business-critical workflows
2. Recently changed functionality
3. Areas affected by defect fixes
4. High-risk integrations
5. Authentication and authorization
6. Data integrity
7. Payment/transaction workflows
8. Frequently used user journeys

---

## Regression Exit Criteria

Regression testing can be considered complete when:

- Critical workflows have been successfully validated.
- High-severity defects are resolved or formally accepted.
- Impacted areas have been regression tested.
- No unresolved release-blocking defects remain.
- Known risks have been documented and communicated.
