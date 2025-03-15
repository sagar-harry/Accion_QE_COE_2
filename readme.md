# **User Experience (UX) Requirements for SauceDemo Website**  

## **1. Overview**  
The **SauceDemo** website is an e-commerce application that simulates an online store for testing and training purposes. The UX should be intuitive, responsive, and engaging, ensuring smooth navigation for users testing the platform.  

## **2. User Personas**  
1. **Regular User (Customer/Shopper)**  
   - Goal: Browse products, add to cart, and complete checkout.  
   - Needs: A seamless and intuitive shopping experience.  

2. **Tester/QA Engineer**  
   - Goal: Perform tests on the platform’s functionalities.  
   - Needs: A stable, well-structured UI with easy-to-test elements.  

---

## **3. Navigation Flow (Flowchart Format)**  

This should be the overall flow
Login page -> Product listing page -> Shopping cart page -> Checkout step-1 -> Checkout step 2 -> Order confirmation


```plaintext
[Login Page]
    │
    ├── Successful Login → [Product Listing Page]
    │
    ├── Failed Login → [Login Page with Error Message]
    │
    └── Logout → [Login Page]
```

```plaintext
[Product Listing Page]
    │
    ├── Click on Product → [Product Details Page]
    │
    ├── Click "Add to Cart" → Product added to cart (Stays on the same page)
    │
    ├── Click Cart Icon → [Shopping Cart Page]
    │
    └── Click Menu → Options (Logout, About, Reset App State)
```

```plaintext
[Product Details Page]  
    │
    ├── Click "Add to Cart" → Product added (Stays on same page)
    │
    ├── Click "Back" → [Product Listing Page]
    │
    └── Click Cart Icon → [Shopping Cart Page]
```

```plaintext
[Shopping Cart Page]  
    │
    ├── Click "Remove" → Item removed (Stays on same page)
    │
    ├── Click "Continue Shopping" → [Product Listing Page]
    │
    └── Click "Checkout" → [Checkout Step 1: User Info]
```

```plaintext
[Checkout Step 1: User Info]  
    │
    ├── Enter Details & Click "Continue" → [Checkout Step 2: Order Overview]
    │
    └── Click "Cancel" → [Shopping Cart Page]
```

```plaintext
[Checkout Step 2: Order Overview]  
    │
    ├── Click "Finish" → [Order Confirmation Page]
    │
    └── Click "Cancel" → [Shopping Cart Page]
```

```plaintext
[Order Confirmation Page]  
    │
    ├── Click "Back Home" → [Product Listing Page]
```

---

## **4. Navigation URLs:**   

Login Page url: https://www.saucedemo.com/
Product listing page: /inventory.html
Shopping cart page: /cart.html
Checkout step-1 page: /checkout-step-one.html
Checkout step-2 page: /checkout-step-two.html
Order confirmation page: /checkout-complete.html
Product detail page: /inventory-item.html?id={id of the product}

## **5. Functional UX Requirements**  

### **5.1 Login Page**  
- Users must be able to log in using provided credentials.  
- Error messages should be clear for incorrect logins.  

### **5.2 Product Listing Page**  
- Sorting options (Price: Low to High, High to Low, A-Z, Z-A).  

### **5.3 Product Details Page**  
- A detailed view of a selected product.  
- "Add to Cart" button should be prominent and responsive.  

### **5.4 Shopping Cart**  
- Users can view added products, or remove items.  
- Display total price before proceeding to checkout.  
- Clear “Checkout” button.  

### **5.5 Checkout Process**  
- Three-step checkout: **Enter User Info → Overview → Confirmation**.  
- Form validation for required fields.  
- Clear confirmation message upon order completion.  

### **5.6 Navigation & User Controls**  
- Persistent navigation bar with **Logo, Cart Icon, and Menu**.  
- Side menu for logout and settings.  
- Responsive design for mobile and desktop.  


Every page will only open if the users logs in
---

## **6. Non-Functional UX Requirements**  

### **6.1 Performance & Speed**  
- Quick load times for all pages (<2s).  
- Smooth transitions between pages.  

### **6.2 Accessibility**  
- High contrast text for readability.  
- Keyboard navigability and screen reader support.  

### **6.3 Error Handling**  
- Descriptive error messages for login and form validation.  
- Alerts for failed transactions or missing details.  

### **6.4 Security**  
- Secure login process.  
- Logout functionality to end sessions properly.  

---

## **7. Future Enhancements**  
- Multi-user authentication (admin vs. customer).  
- Dark mode for better accessibility.  
- More payment options beyond basic checkout.  

---
