# Testcases_codes

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
