# Table of Contents

* [Table of Contents](#table-of-contents)
* [Introduction](#introduction)
  * [Prerequisites](#prerequisites)
    - [Verify Personal Details](#verify-personal-details)
      * [Email Verification](#email-verification)
      * [Mobile Verification](#mobile-verification)
    - [Customer](#prerequisites-customer)
    - [Carrier](#prerequisites-carrier)
    - [Rate Card](#prerequisites-rate-card)
  * [Customer Setup](#customer-setup)
    * [Authentication](#authentication)
    * [Payments](#payments)
  * [Carrier Setup](#carrier-setup)
    * [Authentication](#authentication_1)
    * [Deploy Server](#deploy-server)

# Introduction

Initial setup will configure a single carrier, single customer and single rate card.

## Prerequisites

This guide will assume:

1. You have a modern web browser.
2. You have a basic understanding of Telecoms (Customers, Provider, etc).
3. You have already created an account with ConnexCS.com.

## Verify Personal Details
Before you can configure you account, you need to verify your email and mobile number. You can do this in the Personal Profile pane.
To go to the Personal Profile pane, click on the Notification icon at the top left of the screen. ![notification-icon](new-images/notification-icon.png)


### Email Verification

We verify email addresses to ensure that they are genuine.

How to verify your email address:

1. Click on the Notification icon at the top left of the screen.
2. Click Verify Email.

    ![alt text][verify-email-1]

3. In the Personal Profile pane, click on the Verify Email icon.![verification-icon](images/2018/08/verification-icon.png)  
4. An Email Verification Sent popup will be displayed. This means that an email with a verification code has been sent to your email address.
5. To verify your email, either click the link in the email, or copy & paste the verification code into the Verification Code field and click on the Verify button.

   ![alt text][verify-email-2]

### Mobile Verification

We verify mobile phone numbers to ensure that they are genuine.

> Note: Before you verify your mobile number, check that the information is correct. To modify or add your mobile number, in the Personal Profile pane, click on the Edit icon, make your changes and click Save. The number must be in E.164 format. E.164 numbers are formatted [+] [country code] [subscriber number including area code] and can have a maximum of fifteen digits.

How to verify your mobile number:

1. Click on the Notification icon at the top left of the screen.
2. Click Verify Mobile.
3. In the Personal Profile pane, click on the Verify Mobile icon.![verification-icon](images/2018/08/verification-icon.png)
4. A Mobile Verification  popup will be displayed. This means that an email with a verification code has been sent to your email address.
5. To verify your mobile number, either click the link in the email, or copy & paste the verification code into the Verification Code field and click Verify.

 ![alt text][verify-mobile-1]

## Prerequisites Customer

1. Customer Name
2. Switch IP Address or Username / Password
3. Credit / Debit Limit

## Prerequisites Carrier

1. Carrier Name
2. Switch IP Address

## Prerequisites Rate Card

1. Full Rate Card or List of Codes
2. Profit Margin / Plan for customer prices.

## Customer Setup

> Note: Below are the instructions for basic customer setup (i.e. mandatory fields you need to complete to create a customer profile) and authentication of their account details, e.g IP address and payment details. After setting up a customer, they will be active in the system. For more detailed instructions about setting up customers, click on [Customer Management].

1. Go to Management > Customer.

      ![alt text][customer-dashboard-new]

> Note: On this screen you can modify customer details, add new customers, filter the list of customers and perform bulk actions. To view outstanding actions on a customer, hover over the Warning icon. In the example below, you can see that routing has not been set. Click on the customer's name to update their routing details.
>
>![warning-icon](images/2018/08/warning-icon.png)  

2. To add a new customer, click on the '+' icon. ![plus](new-images/plus-icon.png)

      ![alt text][add-customer-new]

3. Enter the customer's Name.
4. Select the Currency that you wish to use for this  account in. {==This field cannot be changed later.==}{>><<}
5. Add a percentage Tax. This will be calculated on the payment that gets added.
6. Click Save.

      ![alt text][customer-save-new]

### Authentication

1. On the Customers screen, select a customer to authenticate.
2. Click on the Auth menu item.
3. Under IP Authentication, click on the '+' icon.

    ![alt text][ip-auth-1]

4. Enter the Origination/Customer IP address
> Note: We support SRV (service) records & domains too. A Service record identifies servers that provide
special services to a domain, e.g. defining where a SIP service may be found).
5. Click Save.

  ![alt text][ip-auth-2]


### SIP User Authentication

You can authenticate a customer using either IP-to-IP or User/Password. Below are the steps to add a SIP extension.
>Note: Session Initiation Protocol (SIP) is used for call establishment and  management. It enables a very secure authentication process and also centralizes VoIP communication by using a unique number to link all a customer's devices to one address.  

1. On the Customers screen, select a customer to authenticate.
2. Click on the Auth menu item.
2. Under SIP User Authentication, click on the '+' icon.

   ![alt text][sip-user-1]

3. Enter a Username.
4. Enter a Password.
5. Click Save.

 ![alt text][sip-user-2]


### Payments

> Note: You can create multiple payment records to cover a customer's invoices and receipts, e.g. the deposit they have made to join ConnexCS.
>
1. On the Customers screen, to add payment details, first select a customer.
1. Click on the Payment menu item
2. Click on the '+' icon.

   ![alt text][payment-1]

3. Enter a Description and Total amount.
4. Assuming the payment has been made, select the Status as "Complete".
5. Click Save.

    ![alt text][payment-2]

## Carrier Setup

Carriers are your VoIP route providers, below are the basic instructions to setup a carrier. For detailed instructions on carrier setup click on [Carrier Management]

1. Click on Management> Carrier

  ![alt text][carrier-1]

2. Enter the Carrier Name
3. Select the Carrier currency
4. Click Save

 ![alt text][carrier-2]

### Authentication

1. Click on Authentication
2. Click '+' under IP Authentication

  ![alt text][carrier-auth-1]

3. Enter the termination IP address (We support SRV records & domains too)
4. Click Save

 ![alt text][carrier-auth-2]


## Provider Card

Below are the instructions to setup the provider rate card manually. There are two ways to setup a provider rate card, upload and manually, we will go through the manual setup instructions here, for detailed instructions click on [Provider Card]

1. Click on Management> Rate Card

   ![alt text][provider-card-1]

2. Click ‘+’ button under Provider Rate Cards

  ![alt text][provider-card-2]

3. Name the provider card.
4. Select the Carrier from the dropdown list.
5. Select the desired currency for the provider card.
6. Click Save.

  ![alt text][provider-card-3]

7. Go to provider rate card.
8. Click on Create Draft button.

   ![alt text][provider-card-4]

9. Click on Add Row

  ![alt text][provider-card-5]

10. Complete the Spreadsheet information, Example: Prefix: 441, Name: UK Landline, Cost: 0.006, Billing: 1/1. You can add as many rows as you wish.
11. Click on Save button to publish the rate card.


## Customer Card

1. Click on Management> Rate Cards

  ![alt text][customer-card-1]

2. Click on ‘+’ button under Customer Rate Cards

 ![alt text][customer-card-2]

3. Name the customer card
4. Select the multiple carrier cards(By default it will be LCR)
5. Select the desired currency & Click Save

 ![alt text][customer-card-3]

6. Click on Profits tab >Click on Add New Row
7. Complete the Spreadsheet, Example: Prefix: 441, Cost: 0.007, Profit Type: Absolute, Billing 1/1, Rounding: 1/1, Status: Profit, Apply To: Cost

   ![alt text][customer-card-4]

8. Click on Build From Carrier Cards button & confirm the build.

 ![alt text][customer-card-5]

## Ingress Routing

1. Click on Management> Customer

  ![alt text][ingress-1]

2. Click on the customer name> Routing

 ![alt text][ingress-2]

3. Click '+' under Ingress Routing
4. Select the Customer card from the tariff list & click Save

 ![alt text][ingress-3]

For detailed information about ingress routing click on [Ingress Routing]

## Deploy Server

Deploying a server with Connexcs is very quick, once the checklist is complete you will be able to deploy the server.

1. Click on Setup> Settings> Servers
2. Click on Add Server

  ![alt text][server-1]

3. Choose Server Location
4. Enter the Server Name
5. Check the confirmation box and deploy the server.
6. The server IP address will be emailed to your registered email address, the ip address can also be found from the server list section.

 ![alt text][server-2]

[Carrier Management]: <https://docs.connexcs.com/en/latest/carrier/>

[Customer Management]: <https://docs.connexcs.com/en/latest/customer/>

[Provider Card]: <https://docs.connexcs.com/en/latest/provider-ratecard/>

[Ingress Routing]: <https://docs.connexcs.com/en/latest/ingress-routing/>

[verify-email-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/1.png "verify-mobile-1"
[verify-email-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/2.png "verify-email-2"
[verify-mobile-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/3.png "verify-mobile-1"

[customer-dashboard-new]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/4.png "customer-dashboard-new"
[add-customer-new]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/5.png "add-customer-new"
[customer-save-new]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/6.png "customer-save-new"

[ip-auth-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/7.png "ip-auth-1"
[ip-auth-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/8.png "ip-auth-2"

[sip-user-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/9.png "sip-user-1"
[sip-user-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/10.png "sip-user-2"

[payment-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/11.png "payment-1"
[payment-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/12.png "payment-2"

[carrier-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/13.png "carrier-1"
[carrier-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/14.png "carrier-2"

[carrier-auth-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/15.png "carrier-auth-1"
[carrier-auth-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/16.png "carrier-auth-2"

[provider-card-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/17.png "provider-card-1"
[provider-card-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/18.png "provider-card-2"
[provider-card-3]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/19.png "provider-card-3"

[provider-card-4]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/20.png "provider-card-4"
[provider-card-5]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/21.png "provider-card-5"
[provider-card-6]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/22.png "provider-card-6"
[provider-card-7]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/18.png "provider-card-7"

[customer-card-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/23.png "customer-card-1"
[customer-card-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/24.png "customer-card-2"
[customer-card-3]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/25.png "customer-card-3"
[customer-card-4]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/26.png "customer-card-4"
[customer-card-5]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/27.png "customer-card-5"
[customer-card-5]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/25.png "customer-card-5"
[customer-card-6]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/26.png "customer-card-6"


[ingress-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/28.png "ingress-1"
[ingress-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/29.png "ingress-2"
[ingress-3]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/30.png "ingress-3"

[server-1]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/31.png "server-1"
[server-2]: https://raw.githubusercontent.com/digipigeon/connexcs-user-docs/master/new-images/32.png "server-2"