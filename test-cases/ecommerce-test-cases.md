# E-commerce Test Cases

## Scope

Test coverage for core e-commerce product discovery and purchasing workflows.

## Test Case Format

| ID | Scenario | Preconditions | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-EC-001 | Product listing loads successfully | Product catalogue is available | Open the product listing page | Product listing loads and available products are displayed | High |
| TC-EC-002 | Search returns matching products | Products exist for the search term | Enter a valid product keyword and submit search | Relevant matching products are displayed | High |
| TC-EC-003 | Search handles no-result keyword | Application is available | Search for a keyword with no matching products | Appropriate no-results state is displayed | Medium |
| TC-EC-004 | Product sorting works correctly | Product listing contains multiple products | Select an available sort option | Products are reordered according to the selected sort criterion | High |
| TC-EC-005 | Product filter works correctly | Products exist across multiple categories | Apply a valid product filter | Only products matching the selected filter are displayed | High |
| TC-EC-006 | Multiple filters work together | Multiple filter values are available | Apply two compatible filters | Listing contains products matching all selected filter criteria | High |
| TC-EC-007 | Filters can be cleared | At least one filter is active | Clear the applied filter | Unfiltered product listing is restored | Medium |
| TC-EC-008 | Products-per-page option works | Product listing contains more products than the selected page size | Select an available products-per-page option | Listing displays the selected number of products when sufficient products exist | Medium |
| TC-EC-009 | Pagination navigates correctly | Multiple product pages exist | Navigate to the next page | Next page of products is displayed | High |
| TC-EC-010 | Previous-page navigation works | User is on a page after the first page | Select previous-page control | Previous product page is displayed | Medium |
| TC-EC-011 | Product details open correctly | Product is displayed in listing | Select a product | Corresponding product details page loads | High |
| TC-EC-012 | Product information is displayed | Product details page is available | Open product details | Name, price, images and relevant product information are displayed | High |
| TC-EC-013 | Add product to cart | Product is available for purchase | Select Add to Cart | Product is added to the cart and cart state is updated | High |
| TC-EC-014 | Cart quantity can be updated | Product exists in cart | Increase or decrease quantity | Cart quantity and calculated totals update correctly | High |
| TC-EC-015 | Product can be removed from cart | Product exists in cart | Remove the product | Product is removed and cart totals are recalculated | High |
| TC-EC-016 | Checkout validates required fields | Product exists in cart | Proceed to checkout without required information | Required-field validation messages are displayed | High |
| TC-EC-017 | Valid checkout information is accepted | Valid checkout data is available | Complete required checkout fields | Valid data is accepted and checkout can proceed | High |
| TC-EC-018 | Order confirmation is displayed | Valid order data is available | Complete the supported purchase flow | Order confirmation is displayed with relevant order information | High |
| TC-EC-019 | Browser back navigation preserves expected state | Product listing is available | Navigate between listing and product details, then use browser back | Expected previous page and relevant state are restored | Medium |
| TC-EC-020 | Logo navigation loads the expected landing page | Application is accessible | Select the website logo | Expected landing/home page loads successfully | High |
