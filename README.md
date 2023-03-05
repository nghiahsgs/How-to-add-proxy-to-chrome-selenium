# How-to-add-proxy-to-chrome-selenium
How to add proxy to chrome selenium


To add a proxy to Chrome Selenium, you can use the webdriver module in Python and specify the proxy settings in the Chrome options. Here's an example code snippet that demonstrates how to do this:

```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options

# Set proxy server and port number
PROXY_SERVER = "proxy.example.com"
PROXY_PORT = "1234"

# Create a new ChromeOptions object
chrome_options = Options()

# Set the proxy server and port number in the ChromeOptions object
chrome_options.add_argument('--proxy-server={0}:{1}'.format(PROXY_SERVER, PROXY_PORT))

# Create a new WebDriver object with the ChromeOptions object
driver = webdriver.Chrome(options=chrome_options)

# Navigate to a website to test the proxy settings
driver.get("https://www.example.com")
```
In this code, we first define the PROXY_SERVER and PROXY_PORT variables to specify the proxy server and port number, respectively. We then create a new ChromeOptions object and add the proxy server and port number to it using the add_argument() method.

Finally, we create a new WebDriver object with the ChromeOptions object and navigate to a website to test the proxy settings.

Note that you can also specify additional proxy settings, such as username and password, by adding them to the add_argument() method. For example:

```python
# Set the proxy server, port number, username, and password in the ChromeOptions object
chrome_options.add_argument('--proxy-server={0}:{1}'.format(PROXY_SERVER, PROXY_PORT))
chrome_options.add_argument('--proxy-auth={0}:{1}'.format(PROXY_USERNAME, PROXY_PASSWORD))
```
Replace PROXY_USERNAME and PROXY_PASSWORD with the appropriate values for your proxy authentication.



