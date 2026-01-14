# Architecture Overview

**CoffeShop** is built using a modern mobile architecture leveraging **React Native** and **Expo**. This document outlines the high-level design, component responsibilities, and data flow.

## 🏗 High-Level Design

The application follows a component-based architecture with file-based routing provided by **Expo Router**.

```mermaid
graph TD
    User[User] --> UI[UI Layer (Screens/Components)]
    UI --> Router[Expo Router (Navigation)]
    UI --> State[State Management (React Context/Hooks)]
    State --> API[API Layer (Fetch/Axios)]
    API --> Backend[Backend Service]
    State --> Storage[AsyncStorage (Local Persistence)]
```

## 🧩 Component Responsibilities

### 1. Presentation Layer (`app/` & `components/`)
-   **Screens (`app/`)**: Define the routes and main views of the application. Handled by Expo Router.
-   **Components (`components/`)**: Reusable UI elements (Buttons, Cards, Inputs). Pure components that receive data via props.

### 2. Logic Layer (`hooks/`)
-   **Custom Hooks**: Encapsulate business logic and stateful behavior.
-   Separates logic from UI rendering for better testability and reuse.

### 3. Data Layer (`services/` or `api/`)
-   Handles communication with external APIs.
-   Transformation of raw data into domain models.

### 4. Navigation
-   Managed by **Expo Router**.
-   Uses file-system based routing (getting started is as easy as creating a file in `app/`).

## 🔄 Data Flow

1.  **User Action**: User interacts with the UI (e.g., clicks "Add to Cart").
2.  **Event Handling**: Logic in the component or hook handles the event.
3.  **State Update**: Local state or Global Context is updated.
4.  **Side Effects**: API calls are triggered if necessary (e.g., syncing cart with server).
5.  **Re-render**: UI updates to reflect the new state.

## 🛠 Design Principles

-   **Atomic Design**: Breaking down UIs into atoms, molecules, organisms, templates, and pages.
-   **Separation of Concerns**: Logic is separated from presentation.
-   **DRY (Don't Repeat Yourself)**: Reusable components and hooks.
-   **Mobile First**: Designed for touch interactions and small screens.
