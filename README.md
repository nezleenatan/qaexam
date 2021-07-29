# Local Setup (macOS)

## Setup Eclipse for Selenium Test

1. Download Eclipse IDE from this link https://www.eclipse.org/ide (select the version you need for your machine) 
2. Once the download is done. Go to the download folder and install the file

3. Drag the zipped file to the desktop and double click to open it. The file would be unzipped with default archive utility and you would find a eclipse icon on desktop. Open finder, select applications and then drag the Eclipse icon from desktop the the application folder in Finder

4. Once the installation is done, you can now launch the Eclipse by clicking the icon in applications. Alternatively, you can drag the icon from applications to the dock so that you can launch it directly from the desktop

5. Launch to open Eclipse application then window will pop-up to select the directory for your Workspace where you will keep all you files for the testing

6. Once Eclipse is open, click File on upper left side of the screen then click New > Java Project then set a project name. Also set JRE and Project layout to their default selected buttons before clicking the Finish button.

7. All the JRE files should be created and an “src” folder which is the source directory.

## Setup Selenium Client & WebDriver Language Bindings

1. Navigate to seleniumhq.org and click Downloads tab on the upper part of the page

2. Scroll down and look for Java under “Selenium Client & WebDriver Language Bindings” section then click on Download located on the right side

3. Once downloaded extract the file from zip and move it to the folder where your Workspace is located

4. In Eclipse, right click “src” > Build Path > Configure Build Path

5. Click Libraries > Add External Jars > and add all the jar files that were previously downloaded for selenium

6. Click Apply and Close 

## Set up ChromeDriver

1. Directly go to https://sites.google.com/a/chromium.org/chromedriver/ then select the stable version of ChromeDriver to download and choose the version for your machine on the next window. This is to run the browser on testing.

2. Go back to Eclipse right click the “src” > New > Package then set a Package Name (i.e ChromeBrowser)

3. Right click the created PackageName > New > Class to start the test script.

#### First Screnario
```
package chromeBrowser;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class FirstScenario {

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "/Users/nezleenatan/qaexam/chromedriver");
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://qaexam.forge99.com/properties");
		Select sortBy = new Select (driver.findElement(By.cssSelector("select[class='sort-sel aios-listings-sorter']")));
		sortBy.selectByVisibleText("Price Descending");
    }
}
```

#### Second Screnario
```
package chromeBrowser;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class SecondScenario {

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "/Users/nezleenatan/qaexam/chromedriver");
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://qaexam.forge99.com/properties");
		Select sortBy = new Select (driver.findElement(By.cssSelector("select[class='sort-sel aios-listings-sorter']")));
		sortBy.selectByVisibleText("Price Ascending");
    }
}
```

#### Third Screnario
```
package chromeBrowser;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class ThirdScenario {

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "/Users/nezleenatan/qaexam/chromedriver");
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://qaexam.forge99.com/properties");
		Select sortBy = new Select (driver.findElement(By.cssSelector("select[class='sort-sel aios-listings-sorter']")));
		sortBy.selectByVisibleText("A-Z");
    }
}
```

#### Fourt Screnario
```
package chromeBrowser;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class FourtScenario {

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "/Users/nezleenatan/qaexam/chromedriver");
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://qaexam.forge99.com/properties");
		Select sortBy = new Select (driver.findElement(By.cssSelector("select[class='sort-sel aios-listings-sorter']")));
		sortBy.selectByVisibleText("Z-A");
    }
}
```

#### Fifth Screnario
```
package chromeBrowser;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class FifthScenario {

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "/Users/nezleenatan/qaexam/chromedriver");
		WebDriver driver=new ChromeDriver();
	
		driver.get("https://qaexam.forge99.com/properties");
		int width = 600;
		int height = 300;
		Dimension d = new Dimension(width, height);
        driver.manage().window().setSize(d);
        System.out.println("Window height is -> "+driver.manage().window().getSize().getHeight());
        System.out.println("Window width is -> "+driver.manage().window().getSize().getWidth());
	}

}
```
