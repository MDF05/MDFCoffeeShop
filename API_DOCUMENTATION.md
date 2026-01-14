# API Documentation

This document describes the API endpoints used by the CoffeShop application.

**Base URL**: `https://api.coffeshop.com/v1` (Example)

## 🔐 Authentication

All authenticated endpoints require a Bearer Token in the header.

```http
Authorization: Bearer <your_token>
```

## 📦 Endpoints

### 1. Products

#### Get All Products
Retrieves a list of available coffee products.

-   **URL**: `/products`
-   **Method**: `GET`
-   **Auth Required**: No

**Response**:
```json
[
  {
    "id": "1",
    "name": "Espresso",
    "price": 3.99,
    "image": "url_to_image"
  },
  {
    "id": "2",
    "name": "Latte",
    "price": 4.50,
    "image": "url_to_image"
  }
]
```

#### Get Product Details
-   **URL**: `/products/:id`
-   **Method**: `GET`

### 2. Orders

#### Create Order
Places a new order.

-   **URL**: `/orders`
-   **Method**: `POST`
-   **Auth Required**: Yes

**Request Body**:
```json
{
  "items": [
    { "productId": "1", "quantity": 2 }
  ],
  "total": 7.98
}
```

**Response**:
```json
{
  "id": "order_123",
  "status": "pending",
  "createdAt": "2024-01-14T10:00:00Z"
}
```

## ⚠️ Error Handling

The API uses standard HTTP status codes.

| Code | Description |
| ---- | ----------- |
| 200  | Success |
| 201  | Created |
| 400  | Bad Request |
| 401  | Unauthorized |
| 404  | Not Found |
| 500  | Server Error |
