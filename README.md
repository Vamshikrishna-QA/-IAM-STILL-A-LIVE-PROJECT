# -IAM-STILL-A-LIVE-PROJECT
This is a Java test automation framework (  iamstillaliveproject) using Selenium, TestNG, and Apache POI to read data from an Excel file (dropdowns.xlsx). The configuration files define the tools, but specifics on what pages or features were tested are located in the Java source code, which was not provided
This is a 

Java-based test automation project built using Maven. The project is named 

iamstillaliveproject  and is designed to automate web browser testing using Selenium WebDriver. It uses the TestNG framework to structure and run tests.

Here is a breakdown of its components:

Core Technology:

Language: Java, configured to be compiled with version 17.


Build Tool: Maven is used to manage project dependencies and the build lifecycle.

Project Name: The artifactId and groupId are both iamstillaliveproject.


IDE: The .project and 

.classpath  files indicate that the project is set up for the 

Eclipse IDE.

Key Libraries and Their Purpose:

Selenium WebDriver: The core of the project, used for automating browser actions like clicking buttons, filling forms, and navigating between pages.

TestNG: A testing framework used to define test cases, create test suites, and perform assertions to verify outcomes.

WebDriverManager: A utility that automatically manages the browser drivers (like chromedriver), so you don't have to download and configure them manually.

Apache POI: This library is included to read and write Microsoft Excel files (.xls, .xlsx). This strongly suggests the project uses Excel sheets to store test data, test steps, or write test results. The 

.project file shows a linked resource to a file named dropdowns.xlsx.

Log4j: A logging framework used to record detailed information during test execution, which is very helpful for debugging.

Potential Configuration Issue:

Your pom.xml file specifies that the project should use Java 17.

However, your Eclipse 

.classpath file is configured to use a JavaSE-1.8 environment.

This mismatch might cause compilation errors or unexpected behavior. You should align the JRE in your Eclipse build path to match the version in your pom.xml.

Process Blueprint / Flowchart
Based on the libraries and structure, here is a blueprint of what your automation workflow likely does from start to finish:

Test Execution Starts (Via TestNG)

A user or a continuous integration server triggers the test run. TestNG reads its configuration (e.g., an testng.xml file) to determine which test classes and methods to execute.

Read Test Data from Excel

The 

Apache POI library is used to open and read data from an Excel file, such as the linked dropdowns.xlsx. This data is then used to drive the test steps (e.g., usernames, passwords, search terms).

Browser Setup (Via WebDriverManager)

Before a browser is opened, WebDriverManager checks for the correct browser driver (e.g., chromedriver), downloads it if necessary, and sets up the system path for Selenium to use.

Launch Browser (Via Selenium)

Selenium WebDriver creates a new instance of a web browser (like Chrome or Firefox).

Execute Test Logic

The code navigates to a specific URL.

It locates web elements (buttons, text boxes, etc.).

It performs actions on these elements (e.g., click(), sendKeys()) using the data that was read from the Excel file.

Log4j records the status of each step (e.g., "Navigated to login page," "Entered username").

Validation and Assertions (Via TestNG)

After performing actions, TestNG assertions are used to verify the outcome. For example, it might check if a "Login Successful" message appears on the screen. If an assertion fails, the test is marked as failed.

Browser Teardown (Via Selenium)

Once the test method is complete, Selenium's driver.quit() or driver.close() method is called to close the browser.

Generate Test Reports (Via TestNG)

After all tests have run, TestNG generates a set of HTML reports detailing which tests passed, failed, or were skipped.
[ START ]
    |
    v
[ TestNG Initiates Test Run ]
    |
    v
[cite_start][ Apache POI reads test data from an Excel file (like dropdowns.xlsx) ] [cite: 1]
    |
    v
[ WebDriverManager automatically sets up the required browser driver ]
    |
    v
[ Selenium WebDriver launches and controls the browser instance ]
    |
    v
[ Execute Test Steps: The browser navigates to URLs and interacts with web elements using the data from Excel ]
    |
    v
[ TestNG Assertions validate if the application's behavior is correct ]
    |
    v
[ Log4j records the progress and any errors for debugging purposes ]
    |
    v
[ Selenium WebDriver closes the browser session after the test is complete ]
    |
    v
[ TestNG generates HTML reports summarizing the test results (Pass/Fail/Skipped) ]
    |
    v
[  END  ]





