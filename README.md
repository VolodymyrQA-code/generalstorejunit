# Mobile Test Automation Framework — Appium + JUnit 5

UI automation framework for iOS and Android mobile apps using Appium and Java.

## Stack

- Appium
- Java
- JUnit 5
- Maven
- Allure Reporting
- GitHub Actions

## Project Structure
src/          test classes and page objects
app/          Android APK
AppIos/       iOS app binary
screenshots/  captured screenshots
.github/      CI workflow

## Run Tests

Run all tests (Android):
mvn clean test -Pandroid

Run all tests (iOS):
mvn clean test -Pios

## Allure Report

Generate and open report:
allure serve target/allure-results

## CI

GitHub Actions workflow runs tests automatically on push.
Pipeline installs dependencies, executes tests, and uploads Allure report as artifact.

## Notes

- Page Object Model pattern used throughout
- Maven profiles configured for platform-specific execution (Android / iOS)
- Allure annotations used for test step visibility
