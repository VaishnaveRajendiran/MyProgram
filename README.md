# MyProgram
Selenium Testing Code
The reason behind I have used selenium because,
Selenium is mainly used for Functional & Regression Testing.
Selenium is an Open Source Software to automate Web Browsers.
Selenium supports various Operating Environments.
Selenium supports various Browsers to create and execute Tests/Test Cases/Test Scripts.
Selenium supports various programming languages to write programs (Test Scripts) Java,Python,C#.Net,Perl etc..

Program 1:

Using Selenium Java WebDriver Eclipse, Wikipedia program was created.
In this program it has been explained that how should input and link text to be given.
With that to run the program give a right click. There you'll find a run as option and click it.
You'll find run as Java application and click it.
The Program starts to run.

import org.openqa.selenium.By;
import org.openqa.selenium.NoAlertPresentException;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;


public class Wikipedia {

	public static void main(String[] args) throws NoAlertPresentException,InterruptedException  {
		// TODO Auto-generated method stub
		// declaration and instantiation of objects/variables		
        System.setProperty("webdriver.chrome.driver","C:\\Driver\\Windows\\ChromeExt");					
        WebDriver driver = new ChromeDriver();
        // URL 
        String baseUrl = "www.wikipedia.org";					
        driver.get(baseUrl);
        // Input to be given
        driver.findElement(By.xpath("*[@id=searchInput]")).sendKeys("Furry Rabbits");
        // To click search button
        driver.findElement(By.xpath("*[@id=search-form]/fieldset/button")).submit();
        // Link to be clicked
        driver.findElement(By.linkText("*[@id=mw-content-text]/div/ul/li[4]/div[1]/a")).click();
        System.out.println("title of page is: " + driver.getTitle());
        driver.close();
        
   
   Program 2:
      
    Using Selenium Java WebDriver Eclipse, Resize Browser program was created.
    In this program it has been explained that how should input and link text to be given.
    With that to run the program give a right click. There you'll find a run as option and click it.
    You'll find run as Java application and click it.
    The Program starts to run.
    
    import java.awt.Dimension;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.remote.DesiredCapabilities;


public class ResizeBrowser {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.setProperty("webdriver.chrome.driver", "C:\\Driver\\Windows\\ChromeExt");
		WebDriver driver = new ChromeDriver();
		// URL
		String baseUrl = "www.travelex.co.uk";
		driver.get(baseUrl);
		// Getting Size
		System.out.println(driver.manage().window().getSize());
        //Create object of Dimensions class
        Dimension d = new Dimension(550,600);
        //Resize the current window to the given dimension
        driver.manage().window().setSize(d);
        System.out.println(driver.manage().window().getSize());
		driver.close();

	}

}

    
   
