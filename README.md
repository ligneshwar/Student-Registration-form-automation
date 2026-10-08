# Selenium Web Form XPath Automation

A Selenium WebDriver automation project using **Python and XPath** to automate the Selenium Web Form and demonstrate different XPath concepts.

## Website

https://www.selenium.dev/selenium/web/web-form.html

## Test Cases

| TC | Real-Time Task | XPath Concept |
|---|---|---|
| TC01 | Open student registration page | `get()` |
| TC02 | Locate username | Attribute XPath |
| TC03 | Enter password | Attribute XPath |
| TC04 | Locate Submit | `text()` |
| TC05 | Locate textbox dynamically | `contains()` |
| TC06 | Locate element with prefix | `starts-with()` |
| TC07 | Find input using two attributes | `and` |
| TC08 | Find element using alternatives | `or` |
| TC09 | Find parent form | `parent` |
| TC10 | Find form from input | `ancestor` |
| TC11 | Find child inputs | `child` |
| TC12 | Find next element | `following` |
| TC13 | Find checkbox | Attribute XPath |
| TC14 | Find radio button | Attribute XPath |
| TC15 | Select dropdown | XPath + `Select` |
| TC16 | Find second textbox | XPath Index |
| TC17 | Verify submitted message | `text()` |
| TC18 | Find all input fields | `find_elements()` |
| TC19 | Find dynamic element | `contains()` |
| TC20 | Complete registration automation | Multiple XPath concepts |

## Complete Python Code

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Edge()

driver.get("https://www.selenium.dev/selenium/web/web-form.html")
time.sleep(3)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']"
).send_keys("LIGNESHWAR")
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-password']"
).send_keys("Password123")
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//button[text()='Submit']"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[contains(@name,'my-text')]"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[starts-with(@name,'my-')]"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text' and @type='text']"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text' or @name='my-password']"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/parent::*"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/ancestor::form"
)
time.sleep(2)

driver.find_elements(
    By.XPATH,
    "//form/child::*"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/following::*[1]"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@type='checkbox']"
).click()
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@type='radio']"
).click()
time.sleep(2)

dropdown = driver.find_element(
    By.XPATH,
    "//select[@name='my-select']"
)

Select(dropdown).select_by_visible_text("Two")
time.sleep(2)

driver.find_element(
    By.XPATH,
    "(//input[@type='text'])[2]"
)
time.sleep(2)

driver.find_element(
    By.XPATH,
    "//button[text()='Submit']"
).click()

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//h1[text()='Form submitted']"
)

driver.get("https://www.selenium.dev/selenium/web/web-form.html")
time.sleep(2)

inputs = driver.find_elements(
    By.XPATH,
    "//input"
)

print("Number of input fields:", len(inputs))

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[contains(@name,'my-text')]"
)

time.sleep(2)

driver.get("https://www.selenium.dev/selenium/web/web-form.html")
time.sleep(3)

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']"
).send_keys("Student")

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@name='my-password']"
).send_keys("Password123")

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//textarea[@name='my-textarea']"
).send_keys("Student Registration")

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@type='checkbox']"
).click()

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//input[@type='radio']"
).click()

time.sleep(2)

dropdown = driver.find_element(
    By.XPATH,
    "//select[@name='my-select']"
)

Select(dropdown).select_by_visible_text("Two")

time.sleep(2)

driver.find_element(
    By.XPATH,
    "//button[text()='Submit']"
).click()

time.sleep(3)

driver.find_element(
    By.XPATH,
    "//h1[text()='Form submitted']"
)

print("Registration completed!")

time.sleep(5)

driver.quit()
```

## Output
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/66ec7416-a7ad-4559-8dca-1538c36db80a" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/84674cd8-bf10-433d-83de-24ff9d9eb894" />

## Result

**All 20 XPath-based Selenium automation test cases were successfully demonstrated.**
