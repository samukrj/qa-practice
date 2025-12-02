# Manual Test Cases – SauceDemo

This file contains manual functional test cases created during practice on  
https://www.saucedemo.com/.

Each test case includes:  
- Preconditions  
- Test Steps  
- Expected Result  
- Actual Result  
- Status

---

## **TC01 – Valid Login**

**Preconditions:**  
User is on the SauceDemo login page.

**Steps:**  
1. Enter username `standard_user`  
2. Enter password `secret_sauce`  
3. Click the **Login** button  

**Expected Result:**  
User is successfully logged in and redirected to the Products page.

**Actual Result:**  
User is successfully logged in and redirected to the Products page.

**Status:** Pass

---

## **TC02 – Login with Invalid Password**

**Preconditions:**  
User is on the login page.

**Steps:**  
1. Enter username `standard_user`  
2. Enter password `wrong_password`  
3. Click **Login**  

**Expected Result:**  
Error message appears:  
"Epic sadface: Username and password do not match any user in this service"

**Actual Result:**  
Application displayed the correct error message.

**Status:** Pass

---

## **TC03 – Login with Invalid Username**

**Preconditions:**  
User is on the login page.

**Steps:**  
1. Enter username `wrong_user`  
2. Enter password `secret_sauce`  
3. Click **Login**  

**Expected Result:**  
Error message appears:  
"Epic sadface: Username and password do not match any user in this service"

**Actual Result:**  
Error message was displayed.

**Status:** Pass

---

## **TC04 – Add Product to Cart**

**Preconditions:**  
- User is logged in as `standard_user`  
- User is on the Products page  

**Steps:**  
1. Click **Add to cart** on any product  
2. Click the cart icon  
3. Open the Cart page  

**Expected Result:**  
Selected product is visible in the cart.

**Actual Result:**  
Product was visible in the cart.

**Status:** Pass

---

## **TC05 – Login with Locked Out User**

**Preconditions:**  
Login page is open.

**Test Data:**  
- Username: `locked_out_user`  
- Password: `secret_sauce`

**Steps:**  
1. Enter username  
2. Enter password  
3. Click **Login**

**Expected Result:**  
Error message appears:  
"Epic sadface: Sorry, this user has been locked out."

**Actual Result:**  
Correct error message displayed.

**Status:** Pass

---

## **TC06 – Remove Product from Cart**

**Preconditions:**  
- User is logged in  
- Cart contains at least one product  

**Steps:**  
1. Open Cart  
2. Click **Remove** beside the product  

**Expected Result:**  
Product is removed from the cart.

**Actual Result:**  
Product was removed.

**Status:** Pass

---

## **TC07 – Checkout with Valid Customer Information**

**Preconditions:**  
- User is logged in  
- Cart contains a product  
- User is on the Cart page  

**Steps:**  
1. Click **Checkout**  
2. Enter valid First Name  
3. Enter valid Last Name  
4. Enter valid Postal Code  
5. Click **Continue**  

**Expected Result:**  
User proceeds to Checkout Overview page.

**Actual Result:**  
User proceeded to Overview page.

**Status:** Pass

---

## **TC08 – Sort Products by Price (Low → High)**

**Preconditions:**  
User is logged in and on Products page.

**Steps:**  
1. Open sort dropdown  
2. Select **Price (low to high)**  
3. Observe product order  

**Expected Result:**  
Products are sorted in ascending price order.

**Actual Result:**  
Products were sorted ascending. Example: $7.99 → $9.99 → $15.99.

**Status:** Pass

---

## **TC09 – Checkout with Missing Required Fields**

**Preconditions:**  
User is logged in and cart contains a product.

**Steps:**  
1. Click **Checkout**  
2. Leave all fields empty  
3. Click **Continue**  

**Expected Result:**  
Form validation error appears. User stays on the same page.

**Actual Result:**  
Error message: "Error: First Name is required".

**Status:** Pass

---

## **TC10 – Complete Order Checkout Successfully**

**Preconditions:**  
User is logged in and on the Overview page.

**Steps:**  
1. Click **Finish**  

**Expected Result:**  
User sees confirmation page with message: "Thank you for your order!"

**Actual Result:**  
Confirmation page displayed.

**Status:** Pass

---

## **TC11 – Checkout Fails When First Name Is Missing**

**Preconditions:**  
User is on Checkout Information page.

**Steps:**  
1. Leave First Name empty  
2. Enter Last Name  
3. Enter Postal Code  
4. Click **Continue**  

**Expected Result:**  
Error message: "Error: First Name is required."

**Actual Result:**  
Correct error message displayed.

**Status:** Pass

---

## **TC12 – Product Images Render Correctly**

**Preconditions:**  
User is logged in and on Products page.

**Steps:**  
1. Scroll through products  
2. Check each product card  

**Expected Result:**  
Each card displays product image, name, and price.

**Actual Result:**  
Images and details displayed correctly.

**Status:** Pass

---
