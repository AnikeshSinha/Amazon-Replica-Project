# Amazon-Replica-Project

### Problem Details:

      ● The app is a minimalistic replica of Amazon. It allows admins to manage products and members to order those products.
      ● The end-users for this Python app will be
                ○ Admins
                ○ Members
                
### Application Details:

      ● __Login/Register Functionality:__
      
            ○ User should be able to register as an Admin or Member
            ○ Users should be able to log in using Email and Password
            ○ Post login if the user is an admin then show the following menu:
                      ■ Create Product
                      ■ View Products List
                      ■ Update Product
                      ■ Delete Product - It should delete a product based on the ProductID.
                      ■ Logout
                            
            ○ Post login if the user is a member then show the following menu:
                      ■ Create New Order
                      ■ View Order History - Show the list of all the  orders placed by the logged-in user. For example, 
                             [
                               {
                                 "Order ID": "ORD2", 
                                 "Product Name": "K95",
                                 "Price": 10000,
                                 "Discount": "20%", 
                                 "Price after Discount": 8000.0, 
                                 "Quantity": 4,
                                 "Total Cost":32000,
                                 "Ordered By": "Anikesh Sinha",
                                 "Delivering to": "House no. 48, Bandra East, Mumbai India"
                                }
                             ]
                       ■ Update Profile - The user should be allowed to change password and address details.
                       ■ Logout

      ● **Create/Update Product Functionality:**
      
             ○ The admin should be able to create/update a product.
               They can update the following details:
               
                      ■ ProductID - Autogenerated value to uniquely identify a product.
                      ■ Product Name
                      ■ Manufacturer Name
                      ■ Price
                      ■ Discount (Value will be a percentage). For example, 10 will mean 10%; 25 will mean 25%.
                      ■ Total Stock Available
                      
             ○ In case of update functionality, based on ProductID, allow admin to update the details.
                      To update the details you can use the keys given below to update it:
                      Product ID, Product Name, Manufacturer Name, Price, Discount, Total Stock Available
                      
             ○ After the Product is created/updated the details of that product should be stored in the products.json file

       ● **Product Listing Functionality:**
       
             ○ The products created by the logged-in admin should be displayed to him/her and not from all the admins.
             ○ For each product following details need to be displayed
                      ■ ProductID - Autogenerated value to uniquely identify a product.
                      ■ Product Name
                      ■ Manufacturer Name
                      ■ Price
                      ■ Discount
                      ■ Total Stock Available
                      
             ○ For example,
             
                      [
                        {
                            "Created By": "Anikesh Retail", 
                            "Product ID": "GTRX1",
                            "Product Name": "GEFORCE RTX 3070",
                            "Manufacturer Name": "Nvidia",
                            "Price": 70000,
                            "Discount": "30%", 
                            "Total Stock Available": 10
                        }, 
                        {
                            "Created By": "Anikesh Retail",
                            "Product ID": "KBC95",
                            "Product Name": "K95",
                            "Manufacturer Name": "Corsair", 
                            "Price": 10000, 
                            "Discount":"20%",
                            "Total Stock Available": 50
                        }
                      ]

        ● **Create Order Functionality:**
        
              ○ Members should be able to create new orders.
              ○ Show a list of product IDs and the user will enter one productID to select the product and quantity for that product.
              ○ The products list will contain products from all the admins.
              ○ There can only be one product in an individual order. 
                  For example,
                      an order can have 5 quantities of "Apples", another order can have 12 quantities of "Dell mouse".
              ○ Users cannot create orders if the entered quantity is more than the available quantity.
              ○ Once the order is created successfully, the order details should be stored in the orders.json file.
              
        ● **Common Functionalities:**
        
              ● Login - Both admins and members can log in to the application.
              ● Registration:
                      a). The user should enter the following details to register to the application:
                            ■ Name
                            ■ Email
                            ■ Full Address
                            ■ Password
                            
              ● If any of the validations fail then show appropriate error messages.
                      For example,
                              if someone tries to enter a name in place of a contact number then an error should be displayed saying,
                              "Please enter a valid contact number".
              ● We have to store all these details in the admins/members JSON files.
              

