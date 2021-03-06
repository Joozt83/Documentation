# Magento customers list

A customer, in Magento sense, is basically a registered user of your website. 
A customer doesn't necessarily have to buy anything or even have items inside 
a basket. He just has to provide his email and register with the website. 

## Targeting 'real word' customers

Real world customer would be a user that paid for service or product. Thus, inside
Magento any user that registered with his email address is considered a customer. 
To provide more specific emailing targets, there are different emailing lists.

To target users that actually put items into their baskets, it's better to use
[quotes list target][quotes-target]. 
It will provide a list of users that have a basket, either open or finalized 
(transformed into order). This list will be also useful for targeting abandoned
shopping carts.

To target actual, real world customers, that placed an order it's better to use
[orders list target][orders-target].
This list will additionally contain all customers (ones that ordered) that opted 
for anonymous checkout.

To target users/visitors that subscribed to a newsletter it's better to use 
[subscribers list target][subscribers-target].
This list will provide users that subscribed to newsletter regardless if they are
customers, guests or just visitors.

Aside from registered customers, there are also customers that didn't want to 
register and completed theirs using anonymous checkout (has to be enabled inside 
Magento configuration). For targeting such guest customers use the [guest list target][guests-target].

Finally, there is [persons list target][persons-target]
that will aggregate latest information from all above lists using email address 
as a way to distinguish various people.

## Personalization variables

| Variable name | Variable type                     | Description                                 |
|---------------|-----------------------------------|---------------------------------------------| 
| $magento      | _[Magento][magento-object]_       | Overall Magento installation.               |
| $customer     | _[Customer][customer-object]_     | Instance of customer that email is sent to. |

## Limiting customers list

It's possible to limit customers list to a shorten, more precise one, by applying
filter options to it. It's possible to apply following filter options:

*  **First name**
     
   Limits customers list to customers that have given first name.

*  **Middle name**

   Limits customers list to customers that have given middle name.

*  **Prefix**

   Limits customers list to customers that have given prefix in theirs name.

*  **Last name**

   Limits customers list to customers that have given last name.

*  **Email address**

   Limits customers list to customers that have given email address. In practice 
   it will produce one customer list, since customer's email address has to be 
   unique.

*  **Customer group**

   Limit customers list to customers that belong to certain group.

*  **Gender**

   Limits customers list to customers that declared given gender in their profile.

*  **Subscription status**

   Limits customers list to customers that are subscribers and have given subscription
   status. To learn more about subscription statuses read about them on [subscribers 
   target list][subscribers-target] page.

*  **Web store**

   Limits customers list to customers that are from given [webstore][webstore-object].

*  **bought product**

   Limits customers list to customers that bought certain [product][product-object].

*  **bought product from category**

   Limits customers list to customers that bought a [product][product-object] from certain [category][category-object].

*  **wishes for product**

   Limits customers list to customers that placed certain [product][product-object] on theirs [wish list][wishlist-object].

*  **wishes for product from category**

   Limits customers list to customers that placed a [product][product-object] from certain [category][category-object] on theirs [wish list][wishlist-object].


[webstore-object]: copernica-docs:MarketingSuite/magento-integration/object/webstore
[product-object]: copernica-docs:MarketingSuite/magento-integration/object/product
[category-object]: copernica-docs:MarketingSuite/magento-integration/object/category
[wishlist-object]: copernica-docs:MarketingSuite/magento-integration/object/wishlist
[customer-object]: copernica-docs:MarketingSuite/magento-integration/object/customer
[person-object]: copernica-docs:MarketingSuite/magento-integration/object/person
[magento-object]: copernica-docs:MarketingSuite/magento-integration/object/magento
[subscribers-target]: copernica-docs:MarketingSuite/magento-integration/targets/subscribers
[guests-target]: copernica-docs:MarketingSuite/magento-integration/targets/guests
[persons-target]: copernica-docs:MarketingSuite/magento-integration/targets/persons
[orders-target]: copernica-docs:MarketingSuite/magento-integration/targets/orders
[quotes-target]: copernica-docs:MarketingSuite/magento-integration/targets/quotes
