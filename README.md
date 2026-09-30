# 🛒 ShopFlow Automation

A Java-based Selenium automation framework for testing an e-commerce checkout flow, built with Selenium WebDriver, TestNG, Maven, and the Page Object Model (POM).

The project automates a complete shopping journey on SauceDemo: login, product selection, cart validation, checkout, and order confirmation.

## 🛠️ Tech Stack

- Java 17
- Selenium WebDriver 4.35.0
- TestNG 7.11.0
- Maven
- Google Chrome
- Page Object Model (POM)
- Git & GitHub

## 🎯 Automated Scenarios

### Successful Purchase Flow

```text
Login → Products → Add Sauce Labs Backpack → Cart → Checkout
→ Enter Customer Information → Checkout Overview
→ Complete Order → Verify Order Confirmation
```

### Invalid Login

Verifies that an appropriate error message is displayed when invalid credentials are entered.

## 📂 Project Structure

```text
shopflow-automation/
├── pom.xml
├── testng.xml
├── README.md
├── .gitignore
└── src/
    └── test/
        ├── java/com/automation/
        │   ├── base/
        │   │   ├── BasePage.java
        │   │   └── BaseTest.java
        │   ├── listeners/
        │   │   └── ScreenshotListener.java
        │   ├── pages/
        │   │   ├── CartPage.java
        │   │   ├── CheckoutPage.java
        │   │   ├── LoginPage.java
        │   │   ├── OrderConfirmationPage.java
        │   │   └── ProductsPage.java
        │   ├── tests/
        │   │   ├── LoginTest.java
        │   │   └── InvalidLoginTest.java
        │   └── utils/
        │       ├── ConfigReader.java
        │       └── ScreenshotUtil.java
        └── resources/
            └── config.properties
```

## 🏗️ Framework Features

- Page Object Model architecture
- Reusable page classes
- Explicit waits using `WebDriverWait`
- TestNG assertions
- Configurable settings via `config.properties`
- Automatic screenshot capture on test failure
- Maven-based test execution
- Surefire test reports

## ⚙️ Configuration

Settings live in `src/test/resources/config.properties`:

```properties
browser=chrome
url=https://www.saucedemo.com/
```

## 🚀 Getting Started

### Prerequisites

- Java JDK 17+
- Maven
- Google Chrome
- Git

Verify your installation:

```bash
java -version
mvn -version
```

### Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/shopflow-automation.git
cd shopflow-automation
```

### Run the Tests

```bash
mvn clean test
```

A successful run shows:

```text
Tests run: 2, Failures: 0, Errors: 0, Skipped: 0
BUILD SUCCESS
```

## 📊 Test Reports

Maven Surefire generates reports in `target/surefire-reports/`:

- `index.html`
- `emailable-report.html`
- `testng-results.xml`

## 📸 Failure Screenshots

Screenshots are captured automatically when a test fails and saved to the `screenshots/` directory (excluded from Git via `.gitignore`).

## 🔄 Automation Flow

```text
SauceDemo
   ↓
LoginPage
   ↓
ProductsPage
   ↓
CartPage
   ↓
CheckoutPage
   ↓
OrderConfirmationPage
   ↓
Order Completed
```

## 📈 Future Enhancements

- Cross-browser testing
- Data-driven testing
- Parallel test execution
- CI/CD integration with GitHub Actions
- Additional e-commerce test scenarios
- Advanced test reporting

## 👨‍💻 Author

**Animesh Singh**
B.Tech CSE Core

⭐ Built using Java, Selenium WebDriver, TestNG, and Maven.
