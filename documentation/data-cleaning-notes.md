# Data Cleaning Notes

## Dataset

- Records: 1,200
- Columns: 14

## Checks Performed

1. Checked OrderID for duplicates.
2. Reviewed missing values.
3. Standardized blank CouponCode values to `No Coupon`.
4. Checked Date formatting.
5. Reviewed Quantity and pricing values.
6. Validated `Quantity × UnitPrice = TotalPrice`.
7. Reviewed categorical fields for consistency.
8. Reviewed identifier fields.

## Cleaning Decision

Blank `CouponCode` values were standardized to `No Coupon` rather than deleting the corresponding orders.

This preserved the original records while making the field easier to analyze.

## Validation Results

- Duplicate OrderIDs: 0
- TotalPrice calculation errors: 0
