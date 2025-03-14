# Task9
navigate
package org.test;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class Navigate {

	public static void main(String[] args) {
		WebDriver driver = new FirefoxDriver();
		driver.manage().window().maximize();
		driver.get("https://www.google.com/");
		String currentURL=driver.getCurrentUrl();
		System.out.println("Current URL:"+currentURL);
		 driver.navigate().refresh();
		 System.out.println("Current URL:"+driver.getCurrentUrl());
		 driver.quit();
}
}

Demoblase
package org.test;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class Demoblaze {

	public static void main(String[] args) {
		WebDriver driver=new ChromeDriver();
		driver.get("http://www.demoblaze.com");
		driver.manage().window().maximize();
		String PageTitle = driver.getTitle();
		if(PageTitle.equalsIgnoreCase("Store")) {
			System.out.println("Page landed on correct website");
		}
		else {
			System.out.println("Page not landed on correct Website");
		}

	}

}


Wikipedia
package org.test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class Wikipedia {

	public static void main(String[] args) {
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.wikipedia.com");
		 WebElement searchInput = driver.findElement(By.name("search"));
         searchInput.sendKeys("Artificial Intelligence");
         searchInput.submit();
    
         WebElement historySection = driver.findElement(By.linkText("History"));
         historySection.click();

         String sectionTitle = driver.getTitle();
         System.out.println("Section Title: " + sectionTitle);
     
         
         driver.quit();
     }
 }


