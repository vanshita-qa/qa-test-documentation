# BUG-001 — Product Listing Remains Blank After Logo Navigation

> **Portfolio Case Study — Simulated Defect**
>
> This defect report is a portfolio demonstration based on a synthetic e-commerce scenario. It does not represent a defect discovered in a production application or confidential client environment.

## Summary

Product listing content becomes blank after selecting 25 products per page and subsequently navigating through the website logo.

## Severity

**High**

## Priority

**High**

## Module

**Sales → Product Listing → Global Navigation**

## Test Type

**Functional / Regression / Navigation**

## Preconditions

- The e-commerce application is accessible.
- A valid account with access to the Sales module is available.
- The product catalogue contains multiple products.
- The Product Listing page is accessible.
- The Products Per Page control is available.

## Steps to Reproduce

1. Open the e-commerce website.
2. Navigate to the **Sales** module.
3. Open the **Product Listing** page.
4. Locate the **Products Per Page** control.
5. Select **25 products per page**.
6. Verify that products are displayed in the product listing.
7. Click the **website logo** in the header.
8. Observe the product-listing page after navigation completes.

## Expected Result

The product-listing page loads successfully and available products are displayed.

The previously selected products-per-page setting does not prevent the product catalogue from loading.

## Actual Result

The product-listing area remains blank after navigation through the website logo, and no products are displayed.

## Business Impact

The blank product listing prevents access to available products and can interrupt product discovery and product-related workflows.

## Severity Rationale

The issue affects access to a core product-discovery workflow and prevents product information from being displayed.

## Reproducibility

**Not executed against a live application.**

This is a simulated portfolio case study and therefore has no live reproduction count.

## Environment

| Attribute | Value |
|---|---|
| Application | Synthetic e-commerce application |
| Environment | Simulated |
| Browser | Not applicable |
| Operating System | Not applicable |
| Device | Desktop |
| Build / Version | Not applicable |

## Evidence

No live execution evidence is attached because this is a simulated portfolio case study.

## Investigation Areas

Potential areas for technical investigation include:

- Product-listing state after navigation
- Products-per-page state persistence
- URL or query parameters
- Client-side navigation state
- Product-list API request
- API response status and payload
- Browser console errors
- Product-list rendering logic
- State reset during logo navigation

## QA Analysis

The defect appears to involve an interaction between the product-listing state and navigation.

The key regression scenario is:

**Change Products Per Page → Navigate using Website Logo → Return to Product Listing → Verify Product Data**

The scenario should also be validated with different products-per-page values to determine whether the behaviour is specific to the value of 25 or affects the pagination configuration generally.

## Recommended Regression Coverage

After a fix, verify:

- Default products-per-page behaviour
- 25 products per page
- Other available page-size options
- Logo navigation
- Browser refresh
- Browser back navigation
- Product listing pagination
- Product filtering
- Product sorting
- Direct navigation to the product-listing page
- Navigation after applying filters
- Navigation after applying sorting

## Portfolio Note

This case study demonstrates the defect-reporting structure used for professional QA documentation:

**Environment → Preconditions → Exact Steps → Expected Result → Actual Result → Reproducibility → Severity/Priority → Business Impact → Evidence → Investigation Areas**
