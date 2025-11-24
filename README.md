# DiscountCalculator
Top-down design / modularization
Overall design (top level):

Step 1: Read inputs from user (order amount and discount percentage).

Step 2: Validate inputs.

Step 3: Calculate discount amount and final price.

Step 4: Display results.

Modularization into functions:

get_inputs() – reads and converts user input.

calculate_discount(amount, discount_percent) – returns discount amount and final price.

print_summary(amount, discount_percent, discount_amount, final_price) – prints results.
This separation follows a simple top‑down design where the main() function orchestrates the steps.

Algorithm development
High-level algorithm for calculate_discount based on common discount formula:

Input:

amount (original order total)

discount_percent (percentage discount)

Compute discount amount using
discount_amount
=
amount
×
discount_percent
/
100
discount_amount=amount×discount_percent/100.​

Compute final price using
final_price
=
amount
−
discount_amount
final_price=amount−discount_amount.​

Output: discount_amount, final_price.

Input validation logic:

If amount < 0, show an error.

If discount_percent < 0 or discount_percent > 100, show an error.
This ensures realistic values for an online sale.​
Testing and refinement
Basic test cases:

No discount: amount = 1000, discount = 0 → final price = 1000, discount amount = 0.

Normal discount: amount = 2500, discount = 20 → discount amount = 500, final price = 2000.

Edge discount: amount = 999.99, discount = 100 → discount amount = 999.99, final price = 0.

Invalid inputs: negative amount, negative discount, discount > 100, or non‑numeric input (handled by error messages).

Possible refinements:

Support multiple items and automatic discount tiers based on order amount, as used in typical online promotions.​

Add coupon codes and different discount types (flat amount vs percentage) to better match real e‑commerce sites.​

Related
