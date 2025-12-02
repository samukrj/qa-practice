
# **BUG-001 – Checkout accepts whitespace in mandatory fields**

**Application:** https://www.saucedemo.com

**Environment:**

- Browser: Safari
    
- OS: (Tahoe 26.1)
    
- User: standard_user


  

**Severity:** Medium (validation issue)

**Priority:** Medium

---

## **Summary**

Checkout step **incorrectly accepts a whitespace character " " as a valid First Name**, allowing the user to proceed even when the required field is empty.

---

## **Preconditions**

- User is logged in as standard_user.
    
- At least one item is in the cart.
    
- User is on **Checkout**.
    

---

## **Steps to Reproduce**

1. Click **Checkout** on the Cart page.
    
2. In **First Name**, input only a single space " ".
    
3. In **Last Name**, enter any valid text.
    
4. In **Postal Code**, enter any valid number.
    
5. Click **Continue**.
  

---

## **Expected Result**

- Validation should reject whitespace-only input.
    
- Error message should appear: **“Error: First Name is required”**.
    
- User should remain on the same page.
    

---

## **Actual Result**

- User **is allowed to proceed** to the **Checkout: Overview** page.
    
- No validation error is shown.
    
- Whitespace is incorrectly treated as valid input.
    

---

## **Reproducibility**

100% (tested multiple times)

---

## **Notes**


This bug may cause incorrect customer data in real-world checkout processes.
