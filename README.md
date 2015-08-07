# selenium3
package shanazpack;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.interactions.Action;
import org.openqa.selenium.interactions.Actions;

public class Shanazclass {


	public static void main(String[] args) throws Throwable {
		// TODO Auto-generated method stub
WebDriver driver=new FirefoxDriver();
driver.manage().window().maximize();
driver.get("http://www.flipkart.com/");
WebElement ele=driver.findElement(By.xpath("//*[@id='fk-top-search-box']"));

Actions act=new Actions(driver);
Action act1=act.moveToElement(ele).click(ele).keyDown(ele,Keys.SHIFT).sendKeys(ele,"MOBILE").keyUp(ele,Keys.SHIFT).contextClick(ele).build();
act1.perform();
		
//DRAG AND DROP
		Thread.sleep(5000);
WebElement ele2=driver.findElement(By.xpath("//*[@id='list-tagcloud']/div[2]/a[3]"));
		
WebElement ele1=driver.findElement(By.xpath("//*[@id='fk-top-search-box']"));
Actions act2=new Actions(driver);
Action act3=act2 DragAndDrop(ele2,ele1).build();
act3.perform();


		

	}

	
	}


