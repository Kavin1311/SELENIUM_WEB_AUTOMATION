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
