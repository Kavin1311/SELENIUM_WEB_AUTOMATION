# TC_01:Compatibility Testing
# code:
```
import time
from selenium import webdriver

browsers = {
    "Chrome": webdriver.Chrome,
    "Edge": webdriver.Edge,
    "Firefox": webdriver.Firefox
}

for browser_name, browser_driver in browsers.items():
    driver = None

    try:
        print(f"\nTesting on {browser_name}")

        driver = browser_driver()
        driver.get("https://www.practiceqaautomation.com/tickets")

        print("Current URL:", driver.current_url)
        print("Page Title:", driver.title)

        print(f"TC01 PASSED on {browser_name}")
        time.sleep(3)

    except Exception as e:
        print(f"TC01 FAILED on {browser_name}: {e}")

    finally:
        if driver:
            driver.quit()
```
# output:
<img width="749" height="310" alt="image" src="https://github.com/user-attachments/assets/6cec7018-c14d-464a-9b1f-1b5d42691891" />

# TC_02: URL CHECKING:

# CODE:
```

import time
from selenium import webdriver

browsers = {
    "Chrome": webdriver.Chrome,
    "Edge": webdriver.Edge,
    "Firefox": webdriver.Firefox
}

expected_url = "https://www.practiceqaautomation.com/tickets"

for browser_name, browser_driver in browsers.items():
    driver = None

    try:
        print(f"\nTesting on {browser_name}")

        driver = browser_driver()
        driver.get(expected_url)

        current_url = driver.current_url

        print("Current URL:", current_url)
        print("Page Title:", driver.title)

        if current_url == expected_url:
            print(f"TC03 PASSED on {browser_name}")
        else:
            print(f"TC03 FAILED on {browser_name}")

        time.sleep(3)

    except Exception as e:
        print(f"TC03 ERROR on {browser_name}: {e}")

    finally:
        if driver:
            driver.quit()
```
# output
<img width="790" height="305" alt="image" src="https://github.com/user-attachments/assets/0fd68dce-ca9a-478c-a9d9-0e4fc72a9af2" />

# TC-03: DATE CHECKING:
# CODE:
```
import time
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")

time.sleep(5)

date_buttons = driver.find_elements(
    By.CSS_SELECTOR,
    "[data-testid='date-option']"
)

print("Number of date buttons:", len(date_buttons))

for button in date_buttons:
    print("Text:", button.text)
    print("Date attribute:", button.get_attribute("data-date"))

time.sleep(10)
driver.quit()
```
# OUTPUT:
<img width="774" height="566" alt="image" src="https://github.com/user-attachments/assets/260d6bbc-70a5-4f78-98ee-3434dd5e17e9" />

# TC-04: VERIFY PAGE CONTENT:
# CODE:
```
import time 
from selenium import webdriver
from selenium.webdriver.common.by import By

driver=webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")
time.sleep(3)
page_text = driver.find_element(By.TAG_NAME,"body").text
print(page_text)
expected_text="All domain apps"
if expected_text in page_text:
	print("TC04 PASSED")
else:
	print("TC04 FAILED")
time.sleep(10)
driver.quit()
```
# Output:
<img width="826" height="487" alt="image" src="https://github.com/user-attachments/assets/e679267a-28f6-44a8-9325-be5a1d134786" />

# TC-05 CHECKING BASIC BACKWARD NAVIGATION(SMOKE TEST):
# CODE:
```
import time
from selenium import webdriver
from selenium.webdriver.common.by import By
driver = webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")
current_url=driver.current_url
driver.back()
time.sleep(3)
driver.forward()
time.sleep(3)
if(current_url==driver.current_url):
	print("TC-05 passed")
else:
	print("TC-05 failed")

```

# OUTPUT:
<img width="611" height="98" alt="image" src="https://github.com/user-attachments/assets/ca8e0120-e153-4081-9c24-44dc53502c9e" />

# TC-06 
# CODE:
```
import time 
from selenium import webdriver
from selenium.webdriver.common.by import By
driver = webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")
time.sleep(3)
original_url = driver.current_url
print("Original URL: ",original_url)
driver.refresh()
time.sleep(3)
refreshed_url = driver.current_url
print("Refreshed URL:", refreshed_url)
if original_url==refreshed_url:
	print("TC-06 PASSED")
else:
	print("TC-06 FAILED")
driver.quit()
```
# OUTPUT:
<img width="621" height="131" alt="image" src="https://github.com/user-attachments/assets/00b1009e-9848-4fa8-82f0-180b421456b8" />

# TC-07
# CODE:
```
import time
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")
time.sleep(3)

buttons = driver.find_elements(By.TAG_NAME, "button")

print("Total buttons found:", len(buttons))

for index, button in enumerate(buttons, start=1):
    text = button.text.strip()
    displayed = button.is_displayed()
    enabled = button.is_enabled()
    if not displayed:
        print(f"\nButton {index}: {text}")

        print("RESULT: FAIL - Button exists but is not displayed")
    elif not enabled:
        print(f"\nButton {index}: {text}")

        print("RESULT: INFO - Button is displayed but disabled")
    else:
        continue

driver.quit()
```
# output:
<img width="996" height="441" alt="image" src="https://github.com/user-attachments/assets/0f5f65ce-25a8-481e-8425-c52160671ecf" />


# code:
```
import time
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.practiceqaautomation.com/tickets")
time.sleep(3)

inputs = driver.find_elements(By.TAG_NAME, "input")

print("Total input fields found:", len(inputs))

for index, field in enumerate(inputs, start=1):
    field_type = field.get_attribute("type")
    field_name = field.get_attribute("name")
    placeholder = field.get_attribute("placeholder")

    print(f"\nInput {index}")
    print("Type:", field_type)
    print("Name:", field_name)
    print("Placeholder:", placeholder)

    if not field.is_displayed():
        print("FAIL - Input field is hidden")
    elif not field.is_enabled():
        print("INFO - Input field is disabled")
    else:
        print("PASS - Input field is visible and enabled")

driver.quit()
```
# output:
<img width="557" height="135" alt="image" src="https://github.com/user-attachments/assets/c8e82b0c-c224-4871-ad12-ed6c47029a2a" />
# TC-09
# code: 


import time
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select

driver = webdriver.Chrome()

try:
    driver.get("https://www.practiceqaautomation.com/tickets")
    driver.maximize_window()
    time.sleep(3)

    dropdowns = driver.find_elements(By.TAG_NAME, "select")

    print("Total dropdowns found:", len(dropdowns))

    for index, dropdown in enumerate(dropdowns, start=1):
        print(f"\nDropdown {index}")

        if dropdown.is_displayed() and dropdown.is_enabled():
            select = Select(dropdown)
            options = select.options

            print("Dropdown is visible and enabled")
            print("Total options:", len(options))

            for option in options:
                print("Option:", option.text)
        else:
            print("Dropdown is hidden or disabled")

finally:
    driver.quit()


# OUTPUT:
<img width="706" height="384" alt="image" src="https://github.com/user-attachments/assets/6431ed79-3901-4c5b-927c-cc77a82dad36" />


