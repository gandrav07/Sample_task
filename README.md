### Installation Requirement:
Before running the code you need to set up the following tools on your machine
- Java 8
- Eclipse
- Selenium (All the Selenium jar files have been included in the project under the jars package, no need to download again).
- TestNG (Install the TestNG eclipse plugin from http://testng.org/doc/download.html  )
- WebDriver. The method of setting path is attached below

### Project Setup Instruction
- Open Eclipse -> Import -> Existing Projects Into Workspace
-	Select Root Directory and then Navigate to the unzipped project folder and make sure that the project shows up in the Projects section
-	Click Finish
-	You should see the project in your workspace now. 
-	Copy the folder chrome_driver(with two dirvers, one for Mac, one for windows) to root path of disk where your IDE located.    
	-	e.g. For Windows, "E/Program Files/Eclipse", "E/chrome_dirver"
	-	e.g. For Mac,just move folder "chrome_driver" to root path of disk.
-	Modify the PATH_TO_DRIVER in WebPageTestMethod.java to :
	-	for Windows "/chrome_dirver/chromedriver.exe"
	-	for Mac "/chrome_dirver/chromedriver"

### Running Configuration:
-    Select the test class in com.walmart.testcase. There are 2 classes avaiable
	-    NewTestPassForMac.java(Expect to pass all 5 test, only for Mac)
	-    NewTestPassForWindows.java(Expect to pass all 5 test, only for Windows)
-    Run as TestNG
 
### Assignment
Automate an end-to-end user e-commerce transaction flow using any open source tool for www.walmart.com with an existing customer on Chrome or Safari browser.

Scenarios to be automated:
-    1. Login using existing account
-    2. Perform a search on home page from a pool of key words given below
-    3. Identify an item from the result set that you can add to cart
-    4. Add the item to cart    
-    5. Validate that item added is present in the cart and is the only item in the cart

Test Data:
-    kep pool: tv, socks, dvd, toys, iPhone
-    account / password: venkateshgpec@gmail.com / Welcome@123
    
Assumptions:
-    1. It start with 0 item in cart.
-    2. Search only happen after Sign in
-    3. All selected items are added in default conditions
-    4. User will remove items before sign out

Test Flow :
-    1. Open Web Browser
-    2. Open www.walmart.com
-    3. Login using existing account,
-    4. Perform a search on home page from a pool of key words
-    5: Identify an item from the result set that can be added to cart
-    6: Add the selected item to Cart
-    7. Validate that item added is present in the cart by checking Product-id and if it's the only one item in the cart

### Other tests that can be automated for the problem scenario:
-    1. Access the website with no internet connection
-    2. Search for an item which doesn't exist.
-    3. Test if the Add cart button isn't visible.
-    4. Test if item quantity is added more than available items (if it is possible on the UI)
-    5. If there is any limitation on the amount of items in the cart
-    6. Test login by different paths e.g. by clicking on check-out or by creating New Account.
-    7. Test on various browsers
-    8. Run the test in parallel on different platform

### Possible Dupicates and Bug:
-    1. the driver may run before page laod completely
-    2. duplicates element may in the same page

### Trade-offs
-    1.	Simplify the Driver and webElement call
-    2.  rebuild the code style to improve the reusability
-    3.  if possible rewrite the Xpath to improve the efficiency and code resuability
-    4.  Automate more scenario to make the automation more robust   
-    5.  Expect to finish the mobile automation test with mobile device.
-    6.  package the input test key to handle bigger test input pool

### Why it is missing
-    Time limitation 
-    Lack of device(iOS and Android device)

