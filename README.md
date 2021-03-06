# erss-hwk5-kx30-yy58

Fancy Amazon!

author: Kewei Xia, Yue Yang

- [erss-hwk5-kx30-yy58](#erss-hwk5-kx30-yy58)
  * [Outcome](#outcome)
    + [Home Page](#home-page)
    + [Order Detail Page](#order-detail-page)
    + [Shopcart](#shopcart)
    + [Profile](#profile)
    + [Checkout](#checkout)
    + [History Order](#history-order)
  * [Feature checklist](#feature-checklist)
  * [Extra features we have](#extra-features-we-have)

## What's this?
This a mini-Amazon implemented via Django.

## How to Run?
```shell
sudo docker-compose up
```
This will automatically run the front-end web interface, the backend daemon thread and the wordl simulator.

If you only want to run the front-end web interface, you need to 
1. have postgres database install on your environment
2. change the database configuration in `web-app/ERSSHW5/settings.py`
3. (create a python virtual environment and) install all dependancy by `pip install -r requirements`
4. run `python manage.py runserver 0:8000`

## Outcome

### Home Page

![fa](./img/home.png?lastModify=1592769085)

### Order Detail Page

![img](./img/detail.png?lastModify=1592769085)

### Shopcart

![img](./img/shopcart.png?lastModify=1592769085)

### Profile

![img](./img/profile.png?lastModify=1592769085)

### Checkout

![img](./img/checkout.png?lastModify=1592769085)

### History Order

![img](./img/order.png?lastModify=1592769085)

## Feature checklist

- [x] Buy products(communicate with both the world and UPS).
- [x] Different catalog of products.
- [x] Check the status of an order.
- [x] Specify the deliver address(i.e. (x,y)).
- [x] Specify a UPS account name to associate the order with.
- [x] Provide the *tracking number* for the shipment.

## Extra features we have

- [x] A **full-featured shopping cart**(implemented by jQuery + Ajax).
    - check(& uncheck) any orders you want
    - change the item count of each order **dynamically**
    - delete any order you don't need anymore
    - the price will change according to your action(e.g. delete order, change count)
    - **sort** the orders via different constraints
- [x] A **full-featured product management system** + seller.
    - any authenticated user can register as a seller(or unregister)
    - seller will has his/her own selling page, displaying all products they are selling
    - sellers will have a product management system which he/she can 
            - publish new products
            - edit their selling products(e.g. name, price, category)
            - delete(or on sell) their selling products
- [x] Search bar in home page.
    - search products from all categories
    - search products in one specific category
    - search products for one specific seller
- [x] A **full-featured order page**.
    - search bar --- locate any order by item name
    - delete any history orders
    - view detail of any orders
- [x] Build-in data
    - use **signals** to make sure we have some build-in data(e.g. initial items, defualt user), easy to deploy
- [x] Warehouse **dynamic alloccation**.
    - we have 10 build-in warehouses(as part of the initial data)
    - we will allocate the nearest warehouse to each package(to facilate the delivery process)
- [x] Email notification.
    - we will send a confirmation email to user once purchase successful
- [x] Product category.
    - several category of products, can switch between them in the home page
- [x] Edit user profile
    - a separate page to allow user edit his/her personal infromation(e.g. name, email, password)
- [x] Associate your amazon account with your UPS account.
    - automatically associate each order with your UPS account
- [x] Address book.
    - store your frequently use address, fill out the address autimatically when checkout next time
- [x] User-friendly UI and interaction.
    - all edit info page will have some error handling, will show the error message if failed
    - use jQuery + aJax to make interaction more smooth(e.g. use partial refresh in shopping cart)KDI

