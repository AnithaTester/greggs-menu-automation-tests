# **Greggs Menu Tests - Selenium Java Framework**

A comprehensive automated testing framework for the **Greggs website** using **Selenium WebDriver** with **Java** and **TestNG**.  
This framework provides extensive coverage for **menu functionality**, **accessibility**, **performance**, and **cross-browser compatibility**.



## 🏗️ **Project Structure**
    src/test/java/com/greggs/
      ├── config/
      │   ├── DriverFactory.java     # WebDriver creation/management
      │   └── TestConfig.java        # Test properties and settings
      ├── pages/
      │   ├── BasePage.java          # Common page methods
      │   ├── HomePage.java          # Homepage interactions
      │   └── MenuPage.java          # Menu page interactions
      ├── tests/
      │   ├── BaseTest.java          # Base test class with setup/teardown
      │   └── specs/
      │       ├── AccessibilitySpec.java   # WCAG compliance tests
      │       ├── BasicTest.java          # Core functionality tests
      │       ├── MenuDataSpec.java       # Menu content validation
      │       ├── MenuDisplaySpec.java    # UI and layout tests
      │       ├── MenuItemCountSpec.java  # Menu item counts
      │       ├── PerformanceSpec.java    # Performance metrics
      │       ├── RegressionTest.java     # Full regression suite
      │       └── SearchFilterSpec.java   # Search and filter validation
      ├── utils/
      │   ├── CookieConsentHandler.java  # Cookie consent management
      │   ├── JsonDataLoader.java        # Test data from JSON
      │   └── AccessibilityUtil.java     # Accessibility testing helpers
      └── resources/
          └── testng.xml                # TestNG suite configuration

---

**🛠️ Technical Stack**
| Component          | Technology              | Version |
| ------------------ | ----------------------- | ------- |
| Language           | Java                    | 17+     |
| Test Framework     | TestNG                  | 7.8.0   |
| Browser Automation | Selenium WebDriver      | 4.15.0  |
| Build Tool         | Gradle                  | 7.6+    |
| Reporting          | Extent Reports          | 5.1.1   |
| Driver Management  | WebDriverManager        | 5.6.0   |
| Utilities          | Apache Commons, Jackson | 2.15.1  |
| Logging            | SLF4J                   | 2.0.9   |



## 🚀 **Quick Start**

### **Prerequisites**

- **Java 17 or higher**  
- **Gradle 7.6+**  
- **Chrome / Firefox / Safari browser**


**Installation & Setup**
# Clone repository

 git clone https://github.com/AnithaTester/greggs-menu-automation-tests
 
 cd greggs-automation-tests


# Build project and download dependencies
./gradlew clean build

# Run all tests
./gradlew test

# Run with specific browser
./gradlew test -Dbrowser=firefox

# 📋 Test Execution Commands

| Category      | Command                       | Description                   |
| ------------- | ----------------------------- | ----------------------------- |
| All Tests     | `./gradlew test`              | Complete test suite execution |
| Smoke Tests   | `./gradlew testSmoke`         | Critical path verification    |
| Regression    | `./gradlew testRegression`    | Full regression suite         |
| Accessibility | `./gradlew testAccessibility` | WCAG compliance checks        |
| Performance   | `./gradlew testPerformance`   | Speed and efficiency tests    |
| Navigation    | `./gradlew testNavigation`    | Menu and site navigation      |
| Display       | `./gradlew testDisplay`       | UI and layout validation      |



# 🌐 Browser-Specific Testing
# Desktop browsers

./gradlew testDesktop

./gradlew test -Dbrowser=firefox

./gradlew test -Dbrowser=safari

# Mobile testing

./gradlew testMobile

./gradlew test -Dmobile=true -DmobileDevice=GALAXY_S21

# Cross-browser suite

./gradlew testAllBrowsers

# Advanced Execution Options

# Environment configuration

./gradlew test -DbaseUrl=https://staging.greggs.co.uk

./gradlew test -Denvironment=production

# Execution settings

./gradlew test -Dheadless=true

./gradlew test -Dtimeout=30

./gradlew test -Dgroups=smoke,accessibility

# Debug and reporting

./gradlew test --debug --info

./gradlew test --tests "*BasicTest"

./gradlew clean test

# ⚙️ Configuration Options

# Browser configuration
browser=chrome|firefox|safari|edge
headless=true|false
mobile=true|false
mobileDevice=GALAXY_S21|IPHONE_12|PIXEL_5

# Environment settings
baseUrl=https://www.greggs.co.uk
environment=production|staging|development
timeout=20

# Test execution
groups=smoke,regression,accessibility
parallel=true|false

**Supported Mobile Devices**
  GALAXY_S21, GALAXY_S20
  IPHONE_12, IPHONE_13, IPHONE_14
  PIXEL_5, PIXEL_6
  IPAD_PRO, SURFACE_PRO

# 📊 Test Reports & Output

**Report Locations**  
📁 test-output/ExtentReport.html - Detailed HTML report with screenshots<br>
📁 build/reports/tests/ - Gradle test reports<br>
📁 test-output/screenshots/ - Failure screenshots<br>
📁 Console - Real-time execution logs


# Report Features
✅ Interactive HTML reports  
✅ Screenshots on test failures  
✅ Performance metrics  
✅ Accessibility audit results  
✅ Cross-browser comparison  
✅ Historical trend analysis


# 🧪 Test Coverage

**🔍 Core Functionality (BasicTest)**

    Homepage loading verification
    
    Basic navigation functionality
    
    Page content validation
    
    Image loading checks
    
    Cookie consent handling

**📱 Menu Testing (MenuDataSpec, MenuDisplaySpec)**

    Menu page content analysis
    
    Food item validation and categorization
    
    Menu structure verification
    
    Image loading and optimization
    
    Navigation performance

**♿ Accessibility (AccessibilitySpec)**

    WCAG 2.1 AA Compliance
    
    Image alt text verification
    
    Keyboard navigation testing
    
    Color contrast validation
    
    ARIA attributes verification
    
    Semantic HTML structure
    
    Screen reader compatibility

**⚡ Performance (PerformanceSpec)**

    Page load time measurements
    
    Resource loading efficiency
    
    Rendering performance metrics
    
    Stress testing under load
    
    Memory usage analysis
    
    Network request optimization

**🔎 Search & Filters (SearchFilterSpec)
**
    Search functionality validation
    
    Filter options testing
    
    Search result accuracy
    
    Search accessibility

**🧪 Comprehensive Regression (RegressionTest)**

    End-to-end user journey testing
    
    Cross-browser compatibility
    
    Data integrity validation
    
    Error handling verification
    
    Boundary condition testing

🌟 **Framework Features**  

✅ Cross-Browser Testing  
✅ Mobile Responsive Testing  
✅ Parallel Execution  
✅ Smart Reporting  
✅ Accessibility Compliance  
✅ Performance Monitoring  
✅ Configuration Management  



# Custom Configuration
Create `local.properties` for environment-specific settings:  

browser=chrome  
baseUrl=https://www.greggs.co.uk  
headless=false  
timeout=30  
mobile=false


# 🪲 Debug Mode
# Enable detailed logging
./gradlew test --debug --stacktrace --info

# Specific test debugging
./gradlew test --tests "*SpecificTest" --debug

# Log Analysis
# View real-time logs
tail -f build/reports/tests/test/index.html

# Check test results
open test-output/ExtentReport.html

# Analyze failure screenshots
open test-output/screenshots/

# 📚 Additional Resources

  Selenium WebDriver Documentation
  
  TestNG Documentation
  
  Extent Reports Documentation
  
  WebDriverManager Documentation
  
  Greggs Official Website

💡 For any questions or contributions, please open an issue or submit a pull request.
Happy Testing! 🎯


