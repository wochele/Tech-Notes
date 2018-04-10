# Explicit Waits in Selenium

An explicit wait is code you define to wait for a certain condition to occur before proceeding further in the code. The worst case of this is Thread.sleep(), which sets the condition to an exact time period to wait. There are some convenience methods provided that help you write code that will wait only as long as required. WebDriverWait in combination with ExpectedCondition is one way this can be accomplished.



```cs
using (IWebDriver driver = new FirefoxDriver())
{
    driver.Url = "http://somedomain/url_that_delays_loading";
    WebDriverWait wait = new WebDriverWait(driver, TimeSpan.FromSeconds(10));
    IWebElement myDynamicElement = wait.Until<IWebElement>(d => d.FindElement(By.Id("someDynamicElement")));
}
```

This waits up to 10 seconds before throwing a TimeoutException or if it finds the element will return it in 0 - 10 seconds. WebDriverWait by default calls the ExpectedCondition every 500 milliseconds until it returns successfully. A successful return value for the ExpectedCondition function type is a Boolean value of true, or a non-null object.

## Expected Conditions

There are some common conditions that are frequently encountered when automating web browsers. Listed below are a few examples for the usage of such conditions. The Java, C#, and Python bindings include convienence methods so you don’t have to code an ExpectedCondition class yourself or create your own utility package for them.

- Element is Clickable - it is Displayed and Enabled

```cs
WebDriverWait wait = new WebDriverWait(driver, TimeSpan.FromSeconds(10));
IWebElement element = wait.Until(ExpectedConditions.ElementToBeClickable(By.Id("someid")));
```

## WebDriver custom wait

```cs
      public static IWebElement FindElement(this IWebDriver driver, By by, int timeoutInSeconds)
        {
            if (timeoutInSeconds > 0)
            {
                var wait = new WebDriverWait(driver, TimeSpan.FromSeconds(timeoutInSeconds));
                return wait.Until(drv => drv.FindElement(by));
            }
            else
            {
                var wait = new WebDriverWait(driver, TimeSpan.FromSeconds(10));
                return wait.Until(drv => drv.FindElement(by));
            }
        
        }
```

### Usage

```cs
WebDriver.FindElement(By.id(“Element”),WaitTime)
```
