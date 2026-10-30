# Conceptual Database and API Design

> **Status: provisional.** The target website has not been selected. This document describes a generic e-commerce model for academic design purposes; it is not the verified schema or API of any real website.

**Database approach:** a relational SQL model is proposed for coursework; the database product is **TBD**.

## Database design purpose

The conceptual model represents the data commonly involved in product browsing, carts, and checkout. It can support SQL coursework and test-data planning. UI automation against a third-party demo site does not require direct access to that site's database.

## Conceptual entities

These entities represent the minimum records needed for a typical cart and order flow.

| Entity | Example attributes | Purpose |
|---|---|---|
| Customer | `customer_id` (PK), `email` (unique), `first_name`, `last_name` | Represents a registered test customer. Avoid storing real personal data. |
| Product | `product_id` (PK), `sku` (unique), `name`, `price`, `stock_quantity`, `is_active` | Represents an item available for browsing and purchase. |
| Cart | `cart_id` (PK), `customer_id` (FK), `status`, `created_at` | Groups a customer's selected items before checkout. |
| CartItem | `cart_item_id` (PK), `cart_id` (FK), `product_id` (FK), `quantity`, `unit_price` | Records products and quantities in a cart. |
| CustomerOrder | `order_id` (PK), `customer_id` (FK), `status`, `total_amount`, `created_at` | Represents a submitted order in a conceptual test environment. |
| OrderItem | `order_item_id` (PK), `order_id` (FK), `product_id` (FK), `quantity`, `unit_price` | Preserves the product and price details associated with an order. |

## Relationships and integrity rules

The following relationships and constraints keep the conceptual records consistent.

- One customer can have multiple carts over time; each cart belongs to one customer.
- One cart can contain multiple cart items; each cart item references one product.
- One customer can have multiple orders; each order belongs to one customer.
- One order can contain multiple order items; each order item references one product.
- `quantity` must be greater than zero. Prices and totals must not be negative.
- Primary keys identify records; foreign keys preserve relationships; unique constraints protect customer email and product SKU.
- Order items retain the unit price at purchase time so later catalog price changes do not alter historical order totals.

## Conceptual API interactions

These are example resource operations, not verified endpoints for the eventual target site.

| User journey | Example operation | Purpose |
|---|---|---|
| Sign in | `POST /auth/login` | Authenticate a test user, if the target provides an authorized API. |
| Browse products | `GET /products` | Retrieve products, if an API is available. |
| View product | `GET /products/{productId}` | Retrieve details for a selected product. |
| Add to cart | `POST /carts/{cartId}/items` | Add a product and quantity to a cart. |
| Review cart | `GET /carts/{cartId}` | Retrieve cart contents and totals. |
| Submit checkout | `POST /orders` | Create an order in an authorized test environment only. |

## Test and privacy boundaries

Apply these boundaries unless the instructor and target-site owner approve a different test environment.

- Do not infer that a target website exposes these endpoints or permits API testing.
- Do not query or modify a third-party production database.
- Use synthetic test data and an approved demo or test environment.
- After target selection, replace this conceptual model with verified information or clearly retain it as a proposed design if the site's internals are unavailable.
