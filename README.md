# pkseleniumfwkdesndatadriventesting
## Selenium Framework Utility Classes

### Global variables
```
public static String prop = "/test";
pubic static final String str = new File(prop);
```


### Selenium synchronization classes
```
ExceptedConditions
WebDeiver/FluentWait
```

```
ExpectConditions.visibilityOf(WebElement element);
ExpectConditions.visibilityOfElement(By by);
```

### WebDriverWait/FluentWait classes
```WebDriverWait``` class extends the ```FluentWait``` class.


from official page:
```
WebDriver driver = new FirefoxDriver();
driver.get("http://somedomain/url_that_delays_loading");
WebElement myDynamicElement = (new WebDriverWait(driver, 10))
  .until(ExpectedConditions.presenceOfElementLocated(By.id("myDynamicElement")));
```
seperate
```
WebDriverWait wait = new WebDriverWait(driver, 10);
WebElement element = wait.until(ExpectedConditions.elementToBeClickable(By.id("someid")));
```


### Building the test listener class
create a class extend ```TestListenerAdapter``` class.

