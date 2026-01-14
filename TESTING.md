# Testing Guide

We typically use **Jest** for unit and integration testing. This ensures the reliability and stability of the **CoffeShop** application.

## 🧪 Testing Stack

-   **Test Runner**: [Jest](https://jestjs.io/)
-   **React Native Testing**: [Jest Native](https://github.com/testing-library/jest-native) / [React Test Renderer](https://reactjs.org/docs/test-renderer.html)
-   **End-to-End (Optional)**: Maestro or Detox

## 🏃‍♂️ Running Tests

### Run All Tests
```bash
npm test
```

### Run Tests in Watch Mode
Great for development. Reruns tests related to changed files.
```bash
npm test -- --watch
```

### Update Snapshots
If you intentionally changed a UI component, update the snapshots:
```bash
npm test -- -u
```

## 📝 Writing Tests

### Unit Tests
Create files ending in `.test.ts` or `.test.tsx` alongside your components.

**Example**: `components/Button.test.tsx`

```tsx
import React from 'react';
import renderer from 'react-test-renderer';
import Button from './Button';

describe('<Button />', () => {
  it('renders correctly', () => {
    const tree = renderer.create(<Button title="Click me" />).toJSON();
    expect(tree).toMatchSnapshot();
  });
});
```

### Best Practices

1.  **Test Behavior, Not Implementation**: Focus on what the user encounters (text, buttons) rather than internal state changes.
2.  **Mock External Dependencies**: Use `jest.mock()` for APIs and Native Modules.
3.  **Coverage**: Aim for high coverage in critical business logic (`utils/`, `hooks/`).
