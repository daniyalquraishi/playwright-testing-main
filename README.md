
# Playwright Testing Framework (Boiler-plate)

📩 Contact us: daniyalquresi212@gmail.com 

## Overview

A comprehensive testing framework built with Playwright and TypeScript for web and API testing.

## 🚀 Features

- Page Object Model implementation
- API testing support
- Data-driven testing
- Cross-browser testing
- Parallel test execution
- Allure reporting
- CI/CD integration with GitHub Actions

## 📋 Prerequisites

- Node.js (version 16 or higher)
- npm (Node Package Manager)
- Git

## 🛠️ Setup

1. Clone the repository:
```bash
git clone (repo url)
cd ts-playwright-testing
```

2. Install dependencies:
```bash
npm install
```

3. Install Playwright browsers:
```bash
npx playwright install
```

## 🏃‍♂️ Running Tests

### All Tests
```bash
npm test
```

### Run Tests in UI Mode
```bash
npm run test:ui
```

### Run Tests with Browser Visible
```bash
npm run test:headed
```

### Debug Tests
```bash
npm run test:debug
```

### Generate and Open Allure Report
```bash
npm run report
```

## 📁 Project Structure

```
playwright-testing-framework/
├── tests/                  # Test files
│   └── example.spec.ts     # Example test suite
├── pages/                  # Page Object Models
│   └── LoginPage.ts        # Login page object
├── core/                   # Core framework files
│   ├── BasePage.ts        # Base page object class
│   └── APIClient.ts       # API client helper
├── utils/                  # Utility functions
│   └── DataLoader.ts      # Data loading utility
├── test-data/             # Test data files
│   └── users.json         # User test data
├── .github/
│   └── workflows/         # GitHub Actions workflows
├── playwright.config.ts   # Playwright configuration
├── tsconfig.json         # TypeScript configuration
├── package.json          # Project dependencies
└── .env                  # Environment variables
```

## 🔧 Configuration

### Environment Variables (.env)
```
BASE_URL=https://your-app-url.com
API_BASE_URL=http://api.example.com
DEFAULT_TIMEOUT=30000
HEADLESS=true
```

### Supported Browsers
- Chromium
- Firefox
- WebKit

## 📊 Test Reports

The framework generates two types of reports:
1. Playwright HTML report (default)
2. Allure report (with detailed test execution data)

To view the Allure report:
```bash
npm run report
```

## 🔄 CI/CD Integration

The framework includes GitHub Actions workflow configuration for automated test execution on push and pull requests to main/master branches.

To view the CI/CD results:
1. Go to your GitHub repository
2. Click on "Actions" tab
3. View the latest workflow run

## 📝 Writing Tests

### Web Test Example
```typescript
test('web test example', async ({ page }) => {
    await page.goto('https://example.com');
    await expect(page.locator('h1')).toHaveText('Example Domain');
});
```

### API Test Example
```typescript
test('api test example', async ({ request }) => {
    const response = await request.get('https://api.example.com/users');
    expect(response.ok()).toBeTruthy();
    const body = await response.json();
    expect(body).toHaveProperty('users');
});
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

