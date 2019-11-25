# Winium
package vidtext_test;

import java.io.IOException;
import java.net.MalformedURLException;
import java.net.URL;
import java.util.List;
import java.util.Scanner;
import java.util.concurrent.TimeUnit;

import org.junit.Test;
import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.GeckoDriverService;
import org.openqa.selenium.WebDriverException;
import org.openqa.selenium.net.PortProber;
import org.openqa.selenium.remote.Command;
import org.openqa.selenium.winium.DesktopOptions;
import org.openqa.selenium.winium.WiniumDriver;
import org.yaml.snakeyaml.events.Event.ID;

import com.fasterxml.jackson.databind.deser.impl.ExternalTypeHandler.Builder;
import com.google.common.collect.ImmutableList;
import com.thoughtworks.selenium.webdriven.Windows;

import nl.hsac.fitnesse.fixture.util.selenium.caching.WebElementConverter;

public class vidtext_test {


static String Email="xxxx@xxxx.com";
static String password="123";

	public static void main(String[] args) throws MalformedURLException, InterruptedException {
	
		DesktopOptions options = new DesktopOptions();
		 
		options.setApplicationPath("C:\\Program Files\\vidtext\\xxxx.exe");
		
		WiniumDriver driver = new WiniumDriver(new URL("http://localhost:9999"), options);
		
	boolean Online =	driver.findElementByName("xxxx").isDisplayed();
	System.out.println("\n USER IS ONLINE: "+(Online));

			
				Thread.sleep(5000);
				driver.findElement(By.name("Email address")).sendKeys(Email);
				Thread.sleep(3000);
				driver.findElement(By.name("Password")).sendKeys(password);
				driver.findElementByName("Login").submit();
				String output = driver.findElementByName("Login").getAttribute("Login");			
				System.out.println("\n USER TRY TO LOGIN: "+output);
				Thread.sleep(5000);
				 
			
			
	    }
			
	}
						
		
	
