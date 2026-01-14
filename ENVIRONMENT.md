# Environment Variables

The application uses environment variables to manage configuration across different environments (Development, Production, etc.).

## 🔧 Setup

1.  Copy `.env.example` to create your local `.env` file:
    ```bash
    cp .env.example .env
    ```
2.  Fill in the values for each variable.
3.  **DO NOT COMMIT** your `.env` file to version control.

## 📝 Variable Reference

### General

| Variable | Required | Description | Example |
| -------- | :------: | ----------- | ------- |
| `EXPO_PUBLIC_API_URL` | Yes | The base URL for the backend API. | `https://api.coffeshop.com` |
| `EXPO_PUBLIC_APP_ENV` | Yes | Current environment (dev, staging, prod). | `development` |

### Analytics (Optional)

| Variable | Required | Description | Example |
| -------- | :------: | ----------- | ------- |
| `EXPO_PUBLIC_ANALYTICS_ID` | No | ID for tracking analytics (e.g., Google Analytics). | `UA-XXXX-Y` |

### Sentry (Error Tracking)

| Variable | Required | Description | Example |
| -------- | :------: | ----------- | ------- |
| `SENTRY_DSN` | No | DSN for error reporting. | `https://example@sentry.io/123` |

## ⚠️ Important Note

In Expo, variables prefixed with `EXPO_PUBLIC_` are automatically available in your JavaScript code via `process.env`. Ideally, do not store sensitive secrets (like private API keys) in the client-side code manifest.
