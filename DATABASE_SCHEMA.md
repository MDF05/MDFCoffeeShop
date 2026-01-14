# Database Schema

This document outlines the data structures used within the application, including local storage and remote database models.

## 📱 Local Storage (AsyncStorage)

The application uses `AsyncStorage` for persisting simple data on the device.

| Key | Type | Description |
| --- | ---- | ----------- |
| `user_token` | String | JWT token for authentication. |
| `theme_preference` | String | User's preferred theme ('light' or 'dark'). |
| `onboarding_complete` | Boolean | Flag to track if user has seen onboarding. |

## 🗄 Remote Database (Example: PostgreSQL/Mongo)

The backend API is backed by a relational database. Below is the simplified schema.

### Tables / Collections

#### `Users`
Stores user account information.

-   `id` (UUID, Primary Key)
-   `email` (String, Unique)
-   `password_hash` (String)
-   `full_name` (String)
-   `created_at` (Timestamp)

#### `Products`
Catalog of coffee items.

-   `id` (UUID, Primary Key)
-   `name` (String)
-   `description` (Text)
-   `price` (Decimal)
-   `category` (String)
-   `image_url` (String)

#### `Orders`
Customer orders.

-   `id` (UUID, Primary Key)
-   `user_id` (UUID, Foreign Key -> Users.id)
-   `status` (Enum: 'pending', 'completed', 'cancelled')
-   `total_amount` (Decimal)
-   `created_at` (Timestamp)

#### `OrderItems`
Items within an order.

-   `id` (UUID, Primary Key)
-   `order_id` (UUID, Foreign Key -> Orders.id)
-   `product_id` (UUID, Foreign Key -> Products.id)
-   `quantity` (Integer)
-   `price_at_purchase` (Decimal)

## 🔗 Relationships

-   **Users** 1:N **Orders**
-   **Orders** 1:N **OrderItems**
-   **Products** 1:N **OrderItems**

## 🔍 Indexing Strategy

-   Index on `Users.email` for fast lookups during login.
-   Index on `Orders.user_id` for retrieving user history.
-   Index on `Products.category` for filtering.
