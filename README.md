# Playwright JavaScript Automation Project

This project is a JavaScript-based test automation framework built using [Playwright](https://playwright.dev/). It is designed to handle both **UI tests** and **API tests**, with clear separation of concerns for better organization and maintainability.

## Project Structure

The project is organized into the following directories and files:

### 1. **`page-objects/`**
This directory contains Page Object Model (POM) classes for the UI tests, making the framework modular and reusable. Each page class encapsulates the actions and locators for a specific page.

- `AddToCartPage.js` – Handles actions related to adding items to the cart.
- `BasePage.js` – Contains common reusable functions like navigation and URL validation.
- `CheckoutPage.js` – Manages actions related to the checkout process.
- `LoginPage.js` – Encapsulates login-related actions.

---

### 2. **`test-data/`**
This directory holds the test data used by both API and UI tests. Test data is organized to improve maintainability and allow easy updates.

#### Subfolders:
- **`api/`**
  - `AddPetBody.json` – Sample request body for adding a new pet (API tests).
  - `endpoints.json` – Contains API endpoint URLs.
  - `headers.json` – Common headers for API tests.

- **`frontEnd/`**
  - `urls.json` – Contains base URLs and endpoints for the UI tests.
  - `users.json` – Stores test user credentials for the login functionality.

---

### 3. **`tests/`**
This directory contains all test cases for both UI and API.

#### Subfolders:
- **`ui/`** (For UI Tests):
  - `AddToCart.spec.js` – Tests the functionality of adding items to the cart.
  - `Checkout.spec.js` – Tests the checkout process.
  - `E2EProductPurchase.spec.js` – End-to-end product purchase tests.
  - `LoginTest.spec.js` – Validates login functionality with various credentials.

- **`api/`** (For API Tests):
  - `AddNewPet.spec.js` – Tests the API for adding a new pet.
  - `E2EPetFlow.spec.js` – End-to-end flow for managing pet entities via API.
  - `GetPet.spec.js` – Tests fetching pet details via API.

---

### 4. **`utils/`**
Utility functions used across the tests for reusable components like HTTP requests.
- `getRequest.js` – Utility for making GET requests.
- `postRequest.js` – Utility for making POST requests.

---

### 5. **Configuration Files**
- **`playwright.config.js`** – Playwright configuration file for managing test settings like browsers, timeouts, and test directories.
- **`playwright-ci.yml`** – CI configuration for running tests in pipelines.
- **`package.json`** – Contains project dependencies and scripts.
- **`.gitignore`** – Specifies files and folders to be ignored by Git.

---

### 6. **Reports and Results**
- **`playwright-report/`** – Stores Playwright test reports.
- **`test-results/`** – Stores the results of test executions.

---

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```

2. Navigate to the project directory:
   ```bash
   cd <project_directory>
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

---

## Running Tests

### UI Tests
To run the UI test suite using the Chrome browser:
```bash
npm run chrome-ui-tests
```

### API Tests
To run the API test suite:
```bash
npm run chrome-api-tests
```

---

## Key Features
- **Playwright Framework**: Fast, reliable, and cross-browser testing.
- **Page Object Model**: Modular and maintainable UI test design.
- **Test Data Management**: Centralized test data for both API and UI tests.
- **CI Integration**: Configured for Continuous Integration pipelines.

---

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Submit a pull request.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

