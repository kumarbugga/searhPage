# searhPage
Using web driver search the keyword in web page 
package pacteraSearch;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
//import org.openqa.selenium.chrome.ChromeDriver;
import  org.openqa.selenium.firefox.FirefoxDriver;
import  org.openqa.selenium.support.ui.ExpectedCondition;
import  org.openqa.selenium.support.ui.WebDriverWait;

public  class searchClass
{
public   static  void  main(String[] args )  
{
// Create a new instance of the Firefox driver
WebDriver driver=new FirefoxDriver();
// System.setProperty("webdriver.chrome.driver", "C:\\selenium-java-2.35.0\\chromedriver_win32_2.2\\chromedriver.exe");
//WebDriver driver=new ChromeDriver();
// And now use this to visit Google
driver.get("http://www.pactera.com/");
// Alternatively the same thing can be done like this
//driver.navigate().to("http://www.pactera.com/");
//Finding the absolute path for search box 
WebElement  search=driver.findElement(By.xpath(".//*[@id='s']"));
//WebElement search=driver.findElement(By.name("s"));
//Enter something to search for 
search.sendKeys("test automation");
//Now submit the form , WebDriver will find the form for us from the element
search.submit();
// Wait for the page to load for 30 seconds
driver.manage().timeouts().implicitlyWait(30,TimeUnit.SECONDS);
//Close the browser
driver.quit();

}
}


