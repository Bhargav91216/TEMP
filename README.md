from selenium import webdriver

# Specify the path to the Chrome WebDriver executable
chrome_driver_path = "C:/Users/bharg/OneDrive/Desktop/automation/driver/chromedriver.exe"

# Create a Chrome service
chrome_service = webdriver.chrome.service.Service(chrome_driver_path)

# Create Chrome options
chrome_options = webdriver.ChromeOptions()
chrome_options.binary_location = "C:/Program Files/Google/Chrome/Application/chrome.exe"  # Path to your Chrome executable

# Create a new instance of the Chrome WebDriver with service and options
driver = webdriver.Chrome(service=chrome_service, options=chrome_options)

# Open a website in Chrome
driver.get("https://www.google.com")

# You can perform various automation tasks with Selenium from here
# For example, interacting with web elements, submitting forms, etc.

# Close the browser when you're done
driver.quit()
