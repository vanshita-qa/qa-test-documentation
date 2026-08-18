# Exploratory Testing Charters

## Purpose

Exploratory testing is used to investigate application behaviour beyond predefined test cases.

Each session is guided by a focused test charter with a defined area, risks, test ideas and observations.

The objective is to identify unexpected behaviour, edge cases, usability issues, data inconsistencies and workflow risks.

---

# Session 01 — E-commerce Product Discovery

## Charter

Explore product discovery workflows with emphasis on search, filtering, sorting, pagination and navigation state.

## Duration

60 minutes

## Test Area

- Product listing
- Search
- Sorting
- Filtering
- Products per page
- Pagination
- Product details
- Header navigation

## Test Ideas

- Search using valid product names
- Search using partial keywords
- Search using special characters
- Search using empty input
- Search for a non-existing product
- Apply a single filter
- Apply multiple filters
- Remove filters individually
- Clear all filters
- Change sorting options
- Change products-per-page setting
- Navigate between pages
- Refresh the listing
- Use browser back navigation
- Use browser forward navigation
- Navigate through the website logo
- Combine sorting and filtering
- Combine filtering and pagination
- Navigate from listing to product details and back

## Risk Areas

- Product listing state
- Filter persistence
- Pagination state
- Sorting state
- URL parameters
- Client-side navigation
- Product data loading
- Empty states
- Browser history

## Observations to Capture

- Unexpected blank states
- Incorrect product counts
- Incorrect sorting order
- Filters displaying incorrect results
- Pagination displaying duplicate products
- Product data disappearing after navigation
- Console errors
- Failed API requests
- Incorrect URL/query parameters

---

# Session 02 — SaaS / CRM Record Management

## Charter

Explore CRM record management with emphasis on data integrity, search, filters, relationships and permissions.

## Duration

60 minutes

## Test Area

- Contacts
- Companies
- Deals
- Search
- Filters
- Relationships
- Permissions
- Notifications

## Test Ideas

- Create a contact with valid data
- Create a contact with missing required data
- Create duplicate records
- Search using partial values
- Search using special characters
- Apply multiple filters
- Clear filters
- Edit a record
- Refresh after editing
- Navigate away and return to the record
- Associate contacts with companies
- Create and update deals
- Move deals between pipeline stages
- Attempt restricted operations
- Test different user roles
- Verify notification behaviour

## Risk Areas

- Duplicate records
- Data persistence
- Relationship integrity
- Permission enforcement
- Search accuracy
- Filter state
- Workflow automation
- Notification triggers

## Observations to Capture

- Data disappearing after refresh
- Incorrect associations
- Unauthorized actions
- Duplicate records
- Incorrect search results
- Incorrect pipeline state
- Unexpected workflow triggers

---

# Session 03 — P2P Marketplace Listing Lifecycle

## Charter

Explore buyer and seller workflows across the complete listing lifecycle.

## Duration

60 minutes

## Test Area

- Seller listing creation
- Listing editing
- Listing status
- Buyer search
- Offers
- Messaging
- Transactions
- Reviews

## Test Ideas

- Create listing with valid data
- Create listing with incomplete data
- Edit an active listing
- Deactivate a listing
- Search for listing
- Apply filters
- Contact seller
- Submit an offer
- Submit invalid offer
- Accept offer
- Reject offer
- Attempt actions from invalid states
- Progress through transaction states
- Submit review after eligible transaction

## Risk Areas

- State transitions
- Buyer/seller permissions
- Transaction integrity
- Listing visibility
- Offer status
- Duplicate transactions
- Notification consistency

## Observations to Capture

- Invalid state transitions
- Listing remaining visible after deactivation
- Incorrect offer status
- Unauthorized seller/buyer actions
- Duplicate transactions
- Missing notifications
- Incorrect review eligibility

---

# Session 04 — Healthcare Appointment Workflow

## Charter

Explore appointment scheduling with emphasis on availability, booking conflicts, cancellation, rescheduling and access control.

## Duration

60 minutes

## Test Area

- Patient registration
- Provider search
- Availability
- Appointment booking
- Rescheduling
- Cancellation
- Notifications
- Roles and permissions

## Test Ideas

- Search for a provider
- Filter providers
- View provider availability
- Book an available slot
- Attempt to book an unavailable slot
- Attempt duplicate booking
- Reschedule appointment
- Cancel appointment
- Attempt cancellation outside allowed conditions
- Refresh after booking
- Navigate away and return
- Test patient and provider roles
- Attempt restricted operations

## Risk Areas

- Double booking
- Availability synchronization
- Appointment state
- Role permissions
- Notification delivery
- Data consistency

## Observations to Capture

- Same slot becoming available incorrectly
- Duplicate bookings
- Incorrect appointment status
- Incorrect availability after cancellation
- Unauthorized access
- Notification inconsistencies
- Data differences between related views

---

# Exploratory Testing Heuristics

The following heuristics can be used during exploratory sessions:

## Boundary Testing

Test values at and around supported limits.

Examples:

- Minimum/maximum quantities
- Character limits
- Date boundaries
- Pagination boundaries
- Numeric limits

## Negative Testing

Attempt invalid operations intentionally.

Examples:

- Missing required data
- Invalid formats
- Unsupported values
- Unauthorized actions
- Invalid state transitions

## State Transition Testing

Move functionality through different application states and attempt actions that should or should not be available in each state.

## Interruption Testing

Interrupt workflows using:

- Browser refresh
- Back navigation
- Forward navigation
- Multiple tabs
- Network interruption
- Session expiry

## Data Consistency Testing

Compare information across:

- List views
- Detail pages
- Dashboards
- Related records
- API responses

## Error Guessing

Investigate areas historically prone to defects:

- Empty states
- Navigation
- Permissions
- Filters
- Pagination
- Duplicate submissions
- Session handling
- Asynchronous loading

---

# Exploratory Session Reporting

Each completed exploratory session should capture:

| Field | Description |
|---|---|
| Session ID | Unique session identifier |
| Charter | Area being investigated |
| Duration | Planned session duration |
| Environment | Application/environment tested |
| Areas Covered | Features explored |
| Test Ideas | Important scenarios investigated |
| Observations | Unexpected behaviour discovered |
| Defects | Defects identified |
| Risks | Remaining product risks |
| Follow-up | Additional testing required |

---

# Example Session Summary

## Session

EXP-001 — E-commerce Product Discovery

## Charter

Explore product discovery and navigation state.

## Areas Explored

- Search
- Filtering
- Sorting
- Pagination
- Products per page
- Logo navigation

## Key Risk

Navigation may interact incorrectly with product-listing state.

## Result

Potential defects should be documented separately with reproducible steps, expected behaviour, actual behaviour and supporting evidence.

## Follow-up

Execute targeted regression testing around product-listing state after any related defect fix.
