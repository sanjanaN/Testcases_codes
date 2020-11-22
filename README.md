# Testcases_codes

//First Test case

 package seleniumTests;
  
import org.openqa.selenium.By;
//import org.openqa.selenium.By;
//import org.openqa.selenium.SearchContext;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
//import org.openqa.selenium.firefox.FirefoxDriver;

public class First_case {
	
    public static void main(String[] args) throws InterruptedException {

        System.setProperty("webdriver.chrome.driver", "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chromedriver.exe"); 
        
        //Opening browser
        WebDriver driver= new ChromeDriver() ;
        
        //Opening window tab in maximize mode
        driver.manage().window().maximize();
        
        //Opening application
        driver.get("https://www.propertycapsule.com");
        
        //driver.navigate().to("https://maps.propertycapsule.com/"); //navigation to Mapmaker
        driver.findElement(By.id("market-btn")).click();
        
       // driver.navigate().to("https://tours.propertycapsule.com/");
       driver.findElement(By.id("manage-btn")).click(); //navigation to tourbooks
	
}}


// Second test case :

package seleniumTests;

import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class Second_test {
	 
	public static void main(String[] args) throws Exception {
		
		System.setProperty("webdriver.chrome.driver","C:\\Program Files (x86)\\Google\\Chrome\\Application\\chromedriver.exe"); 
	
   WebDriver driver= new ChromeDriver() ;
  
  driver.get("https://www.propertycapsule.com");
  driver.manage().window().maximize();
  String execScript = "return document.documentElement.scrollHeight>document.documentElement.clientHeight;";
    JavascriptExecutor scrollBarPresent = (JavascriptExecutor) driver;
    Boolean test = (Boolean) (scrollBarPresent.executeScript(execScript));
    if (test == true) {
     System.out.print("Scrollbar is present.");
    } else if (test == false){
     System.out.print("Scrollbar is not present.");
    }
 
  try {
   GoogleSearch();
   
  } catch (Exception e) {
   // TODO Auto-generated catch block
   e.printStackTrace();
  }
 }

	private static void GoogleSearch() {
		// TODO Auto-generated method stub
		
	}
	}
	
	
	
// Third test case:

  package seleniumTests;
  
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;


public class Third_test {
	
    public static void main(String[] args) throws InterruptedException {

        System.setProperty("webdriver.chrome.driver", "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chromedriver.exe"); 
        
        //Opening browser
        WebDriver driver= new ChromeDriver() ;
        
        //Opening window tab in maximize mode
        driver.manage().window().maximize();
        
        //Opening application
        driver.get("https://www.propertycapsule.com");
        
        //driver.navigate().to("https://maps.propertycapsule.com/");
                            //filling the Contact form under request a demo
        driver.findElement(By.linkText("request a demo")).click();
        driver.findElement(By.id("FirstName")).sendKeys("firstnamex");
        driver.findElement(By.id("LastName")).sendKeys("lastnamex");
        driver.findElement(By.id("Email")).sendKeys("firstxy@yopmail.com");
        driver.findElement(By.id("GDPR_Opt_In__c")).click();
        driver.findElement(By.className("mktoButton")).click();
        
		
}}

