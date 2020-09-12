# Project

## Overview
The purpose of this project is to setup an ecommerce store and a public facing website. If needed an integration between client's warehouse and online store will be developed as well, that will synchronize inventory.

## System

The components of the system are e-commerce, website, and inventory management.

![System Dataflow](ecommerce.png)

## E-commerce
Ecommerce is the primary component of the system. 


#### Functional Requirements
- Store should have an admin dashboard where store onwer can manage products & their categories/collections, customers, and products.
- Store owner should be able to add product inventory manually. The inventory should automatically sync between the store and the warehouse.
- Customers should be able to browse products on the online store, filter them by category, and filter them based on other filtering options available.
- Store owner should be able to withdraw earnings.
- Products will be imported every night at 12:00 am.



#### Non-functional Requirements
- Store should be secure.
- Store should be scalable.
- Store should have a 99.99% uptime.



#### Tecnical Details
The online store will be setup on Shopify, which is a cloud base e-commerce solution. Add more technical details here.


## Website


#### Functional Requirements
- Website should follow client brand guidelines.
- Website should connect with Shopify store.



#### Non-functional Requirements
- Website should be secure.
- Website should be scalable.
- Website should have a 99.99% uptime.



#### Tecnical Details
The website will be hosted on HubSpot CMS, which is a cloud base CMS. Add more technical details here.



## Inventory Management
The inventory on ecommerce store should sync warehouse.

#### Functional Requirements
- At a given time the product inventory in online store should be reflect what is available in the warehouse.
- Store owner should be able to manually change inventory on the online store.


#### Non-functional Requirements
- Inventory management should be secure and reliable.


#### Tecnical Details
A microservice will be developed that will integrate Shopify with warehouse software for inventory synchronization. 

- The microservice will be hosted on Amazon AWS lambda.
- The communication between microservice, warehouse, and Shopify store will be secured using API keys which will autorotate.
- The microservice will power a private Shopify app.


