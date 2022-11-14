# SauceDemo
Framework Explanation of the Project

    Type of framework: Data-driven framework by using Page Object Model design pattern with Page Factory.
    Package structure: maven default folder structure
    Utilities used: excel utitlity, take Screenshot etc
    Reporting mechanism used: testNG report, extent report.

How to run the test:

    Run the test by right click on the testng.xml file and select Run As => TestNG Suite.

Steps Done:

    1.	Login to the site https://www.saucedemo.com/ by Data Driven Approach from an Excel file named TestData.xlsx
    2.	Filtering the results by “Price (low to high)’ by SelectByVisibleText() method of the Select class.
    3.	Adding 3 different items to the cart by click() method.
    4.	Assert the total number of items in the cart by using Assert.assertEquals() function.
    5.	Removed one item from the cart.
    6.	Assert again the total number of items in the cart to ensure the item is removed.
    7.	Add 1 more item to the cart to make it again 3 items.
    8.	Assert the number of items again in the cart.
    9.	Continue to check out
    10. Rechecked the items in the cart.
    11. Ensure the card information, shipping information, Sub Total, Tax and Grand Total are displayed.
    12. Fill the check out information details by Data Driven approach from an Excel file named TestData.xlsx
    13. Continue to check out completion.
    14. Ensure “Thank you for your order” message is displayed.
    15. Logged out from the site.

Sauce Demo Framework:

    It is a maven Project with POM design pattern with Page Factory. And if any method gets failed, getScreenshotAs() method will create the 
    image file and will store under ‘target’ folder with name and date.  

1.	src/main/java.
      •	com.SauceDemo.constants
          o	Automation constants.java
      •	com.SauceDemo.pages
          o	Login.java
          o	Inventory.java
          o	Cart.java
          o	CheckOutStepOne.java
          o	CheckOutStepTwo.java
          o	CheckOutComplete.java
          o	Logout.java 
       • com.SauceDemo.utilities
          o	ExcelUtility.java
          o	PageUtility.java

2.	src/main/resources
          o	TestDate.xlsx

3.	src/test/java
      •	com.SauceDemo.scripts
          o	TestBase.java
          o	TestClassLogin.java
          o	TestClassInventory.java
          o	TestClassCart.java
          o	TestClassCheckOutStepOne.java
          o	TestClassCheckOutStepTwo.java
          o	TestClassCheckOutComplete.java
          o	TestClassLogout.java 

4.	src/test/resources
          o	Config.properties



