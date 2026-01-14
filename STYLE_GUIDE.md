# Style Guide

To maintain code quality and consistency, we follow strict coding standards.

## 🖌 Code Formatting

We use **Prettier** for automatic code formatting.

-   **Single Quotes**: Yes
-   **Trailing Commas**: ES5
-   **Tab Width**: 2 spaces
-   **Semi-colons**: Yes

Run the formatter:
```bash
npm run format
```

## 🔍 Linting

We use **ESLint** with standard React Native presets.

Run the linter:
```bash
npx expo lint
```

## 📂 Naming Conventions

### Files & Components
-   **Components**: PascalCase (e.g., `ProductCard.tsx`)
-   **Hooks**: camelCase with `use` prefix (e.g., `useAuth.ts`)
-   **Utilities**: camelCase (e.g., `dateFormatter.ts`)
-   **Constants**: UPPER_CASE (e.g., `TIMEOUT_MS`)

### Variables & Functions
-   **Variables**: camelCase (`isActive`)
-   **Booleans**: Prefix with `is`, `has`, or `should` (e.g., `isVisible`)
-   **Functions**: camelCase, verb-noun pattern (`getUser`, `submitOrder`)

## ⚛️ React Best Practices

1.  **Functional Components**: Use functional components with Hooks. Avoid Class components.
2.  **Destructuring**: Destructure props for cleaner code.
    ```tsx
    // Good
    const Button = ({ title, onPress }) => ...

    // Bad
    const Button = (props) => <Text>{props.title}</Text>
    ```
3.  **Styles**: Use `StyleSheet.create` defined outside the component render cycle.
4.  **Types**: Use TypeScript interfaces for all component props.

```tsx
interface Props {
  title: string;
  isActive?: boolean;
}

export const MyComponent: React.FC<Props> = ({ title, isActive }) => {
  // ...
};
```
