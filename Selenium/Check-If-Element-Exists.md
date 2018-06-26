# Check if element exists

Since FindElement will throw an exception if it does not exist, FindElements can be used to see if an element exists using it's Count property

```cs
if (Driver.Instance.FindElements(By.Id("txtAgencyCd")).Count == 1)
{
    string test = "test";
}
```
