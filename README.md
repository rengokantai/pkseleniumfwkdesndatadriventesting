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



## Defining WebDriver and AppiumDriver Page Object Elements
### Types of locators

### Simple locators
```
@FindBy(linkText="Gmail")
protected M gmail;
@FindBy(partialLinkText="mail")
```

### CSS locators
```
@FindBy(css="input#identifierId")
@FindBy(css="input[id='identifierId']")
```

### XPath query locators
```
@FindBy("//input[id='identifierId']")
```

### WebElements
```
@FindBy(xpath="//span[text()='Green']") //equals
```


### Multiple attribute XPath versus CSS locators
#### Or conditions
```
//Xpath
@FindBy(xpath="//img[@src='myLogo.png' or @src='myLogo.png']")
//css
@FindBy(css= "div[id*='progressBar'],a[id*='progressBar']")
```

#### And conditions
```
//Xpath
@FindBy(xpath="//div[contains(@class,'header') and contains(text(),'label']")
//css
@FindBy(css= "div[id*='progressBar'],a[id*='progressBar']")
```

#### Using dynamic locators in methods
```
driver.findElement(By.xpath()).getText()
```


## Building a JSON Data Provider

### The @DataProvider annotation

### The @Test annotation
