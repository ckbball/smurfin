# smurfin
Main information repository about the smurfin project

Smurfin Shop is an online marketplace where users can purchase gaming accounts and vendors can put accounts up for sale.

The project's backend is composed of ten plus microservices written in Go using gRPC and events on Kafka to communicate between each other.
Each service that requires persistent storage either makes use of MySQL or MongoDB except for the search service which uses Elasticsearch to give
full-text search capabilities.

Each service and it's role detailed below:
smurfin-agent - manages the process for agents of smurfin shop to validate accounts submitted by vendors and allow the accounts to be published 
to our catalog of products.

smurfin-cart - manages the users' shopping cart across browsing sessions so that the user never loses track of what they are shopping for.

smurfin-catalog https://github.com/ckbball/smurfin-catalog - Manages all related capabilities necessary to bring in new products to show our users and to show our current stock 
of products.

smurfin-checkout https://github.com/ckbball/smurfin-checkout - Services the checkout process when a user wishes to purchase their selected products. Being such a central service to
SmurfinShop it communicates directly or indirectly with many other services.

smurfin-email https://github.com/ckbball/smurfin-email - Communicates with 3rd party emailing services through APIs to email our customers and vendors when important events 
related to their accounts occur.

smurfin-funds - Handles the process of a vendor withdrawing the money they have made from successfully selling the accounts they submitted.

smurfin-payment https://github.com/ckbball/smurfin-payment - Handles the communication to 3rd party payment services to process a customer's purchase of accounts

smurfin-search - Is the search service for catalog items.

smurfin-user - Handles all user related functions from authentication to signup and on.

smurfin-vendor https://github.com/ckbball/smurfin-vendor - Handles all vendor related functions from signup to account submission.

