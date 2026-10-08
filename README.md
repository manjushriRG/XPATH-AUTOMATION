# XPATH-AUTOMATION

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time
driver = webdriver.Chrome()
driver.get("https://demo.automationtesting.in/Register.html")

#Attribute XPath

driver.find_element(By.XPATH,"//*[@placeholder='First Name']").send_keys("manjushri")
driver.find_element(By.XPATH,"//*[@placeholder='Last Name']").send_keys("RG")

#contains
driver.find_element(By.XPATH,"//*[contains(@type,'email')]").send_keys("raja28@gmail.com")
time.sleep(4)

#starts-with
driver.find_element(By.XPATH,"//*[starts-with(@type,'tel')]").send_keys("9367892787")
time.sleep(4)

#and
driver.find_element(By.XPATH,"//*[@id='firstpassword' and @type='password']").send_keys("shri")
time.sleep(3)

#or
driver.find_element(By.XPATH,"//*[@id='firstpassword' or @type='password']").send_keys("shri")
time.sleep(3)

#text
driver.find_element(By.XPATH,"//*[text()=' Submit ']").click()
time.sleep(2)

#parent
driver.find_element(By.XPATH,"//*[@value='Movies']/parent::div").click()

#ancestor
driver.find_element(By.XPATH,"//*[@value='Movies']/ancestor::div[1]").click()

#child
driver.find_element(By.XPATH,"//*[@class='form-group'][6]/child::div/div[3]/input").click()


```
