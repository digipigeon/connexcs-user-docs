# API Integrations
**Setup :material-menu-right: Integrations :material-menu-right: API**

**API Integrations** are configured to allow ConnexCS to connect to external services. For inbound APIs, please see the [**API**](https://docs.connexcs.com/api/) in the Architecture documentation. 

## Available Integrations

**PayPal Express Checkout** Allows online checkout via the customer portal using a [**PayPal**](https://www.paypal.com) Account. 

**PayPal IPN** Enable IPN to use MassPay or to send money from the PayPal portal without using your site. This also notifies the system of incoming PayPal payments and we can top-up based on that notification.  

**Stripe** Possibly the world's best credit card processor, [**Stripe**](https://www.stripe.com) can be made available on your customer portal.

**Duo Security** With [**Duo Security**](https://duo.com/) we can provide 2FA (2 Factor Authentication) via an out-of-band push notification to your mobile device to approve login. It also provides fingerprint authentication for extra security. 

**Moneris** [**Moneris**](https://www.moneris.com/) is Canadian Credit Card Processing service.

**ScriptForge** [**ScriptForge**](/developers/scriptforge/) is the ConnexCS JavaScript Sandbox environment where you can write drivers to intermediate connectivity to a large variety of providers.

**Razor Pay** [**Razor Pay**](https://razorpay.com/) is a large payment processor from India.

## Enable API Integration

1. Click the **`Add`** button.
2. Select the desired service from the list.

    ![alt text][api]

3. Complete the available fields (see individual API integrations below for details for each provider).
4. Click the **`Save `** button.

!!! info "API Service details"
    Each service requires different details. These can be obtained using your account with the specific provider(s). 
    
## Compare PayPal options
**Mass Payment** is a bulk payment method that sends funds in an uploaded file to PayPal, allowing the sender to pay less than the standard PayPal fees using their bulk order discounts. Since this payment does not trigger anything our VoIP system, we link into PayPal's IPN to accommodate notifications and balance sheet updates.

**Mass Pay vs Express Checkout**

Use this comparison chart listing the differences between Mass Pay and Express Checkout with PayPal to help you decide which to use:

|Mass Pay|Express Checkout|
|---|---|
|A CSV is uploaded to PayPal's website.|Made through customer portal.|
|Slightly lower transaction fees.|Standard PayPal fees (about 3.4% + $0.30).|
|Fees are paid by the sender.|Fees are paid by the recipient.|
|Sender pays a 2% transaction fee, capped at $1 per payment.|Recipient pays by per-transaction deductions.|
|Uses PayPal IPN.|Uses PayPal API Signature.|

## PayPal Express Checkout Integration
Enter the PayPal credentials into your account.

1. Select **`Add`** then **PayPal**.
1. **Mode**: Use `Test` for testing connections or `Live` for an active account.
1. To find your **Username**, **Password**, and **Signature**:
    + Access your PayPal account, navigate to **Settings :material-menu-right: Account Settings :material-menu-right: Account Access**.
    + Click the **`Update`** button for **API Access**.
    + Select **Manage API Credentials** under **NVP/SOAP API integration (Classic)** section. 
    + Select **Request API signature**, then **`Agree and Submit`**.
6. Copy the **API Username**, **API Password**, and **Signature** credentials from this page into the open PayPal form in ConnexCS. 
    
    ![alt text][paypal-9] 

1. **Currency**: Select one or more currencies that you will accept. 
1. **Deduct Payment Fees**: Set whether you will deduct the fees or not.
1. Click **`Save`**.

## PayPal IPN Integration
PayPal's **Instant Payment Notification (IPN)** is a service that provides notifications for PayPal transactions. IPN messages can be used to automate bulk payment processes, where consumers still send PayPal payments as normal. Payments made using this integration will automatically top-up the customer account in ConnexCS. For this to work, settings need to be configured on the ConnexCS control panel as well as PayPal.

### Configure PayPal IPN
Below are the steps to configure IPN:

**Step 1: Configure ConnexCS**

1. Select **`Add`** then **PayPal IPN**.
2. Update the following:
    + **IPN URL**: This should never be modified; you will need it later to complete the integration.
    + **Payment Type**: Select "Mass Pay" (described above) or "Send Money" (fees may apply).
    + **Verify Transaction**: If selected, ConnexCS will check with PayPal to make sure the transaction is correct.
    + **Currency**: Select one or more currencies that you will accept. 
    + **Deduct Payment Fees**: Set whether you will deduct the fees or not.
3. Click **`Save`**.
4. To find the IPN URL (needed later in configuration), open the **`paypal_ipn`** now listed in API.

**Step 2: Identify your IPN listener to PayPal**

After you have configured ConnexCS, add it to your PayPal account (taken from PayPal support [**here**](https://developer.paypal.com/docs/api-basics/notifications/ipn/IPNSetup/#)).

1. Login to a PayPal Business Account (must be a Business account, not a regular PayPal account).
2. Navigate to **Settings > Account Settings > Notifications**.
3. Select **Update** next to **Instant payment notifications**.
4. Click **Choose IPN Settings**.
5. Enter the IPN URL under **Notification URL** and select **Receive IPN Messages (Enabled)** click **Save**. 
6. Fill in the settings, and then copy the API URL.

### Configure Customer with PayPal Email address
The following are instructions on how to add a PayPal Email address to a ConnexCS customer account:

1. Navigate to **Management :material-menu-right: Customer :material-menu-right: [Customer name]**.
1. Click :material-plus: under Contacts.
1. Enter the customer's Name and PayPal email address and click **`Save`**.
1. From the customer's main page, select Edit :material-menu-right: Config.
1. Enter the customer PayPal email ID and click **`Save`**.

### View PayPal IPN Payment Log
These payments can be viewed under **Setup :material-menu-right: Information :material-menu-right: Payment Log**. 

## Stripe Integration
Configure the Stripe API Keys in ConnexCS:

1. Select **`Add`** then **Stripe**.
1. **Mode**: Use `Test` for testing connections or `Live` for an active account.
2. **Public Key** (Publishable) and **Private Key** (Secret): Access the [**Stripe Dashboard**](https://dashboard.stripe.com/account/apikeys)(login if necessary) to access your keys (from [**Stripe Support**](https://stripe.com/docs/keys); `Test` keys are also found at that link). 
4. **Currencies**: Select one or more currencies that you will accept.

## Duo Security Integration
Configure Duo Security settings in ConnexCS:

1. Select **`Add`** then **Stripe**.
2. **Integration Key**, **Secret**, and **Host**: Access the [**Duo Admin Panel**](https://admin.duosecurity.com/), locate **`Auth API`**, click `Protect` (from [**Duo Auth support**](https://duo.com/docs/authapi)). Find the **Integration Key**, **Secret Key**, and **API Hostname** to complete setup in ConnexCS. 

## Moneris Integration
Link Moneris to ConnexCS:

1. Select **`Add`** then **Moneris**.
2. **Store ID**: This can be found in the MRC Welcome emails (contact [**Moneris**](https://www.moneris.com/) for assistance finding this). 

## Scriptforge Integration

1. Select **`Add`** then **Scriptforge**.
2. **Company**: Select the customer to integrate. 
3. **Script Forge**: Select the predefined script (details found under [**Developer :material-menu-right: Scriptforge**](/developers/scriptforge/). 

## Razor Pay Integration
Enter Razorpay settings into ConnexCS:

1. Select **`Add`** then **Razorpay**.
2. **Mode**: Use `Test` for testing connections or `Live` for an active account.
3. **Key ID** and **Key Secret**: Access [**Razorpay Dashboard**](http://dashboard.razorpay.com/), go to Settings and Generate Test Key (from [**Razorpay support**](https://knowledgebase.razorpay.com/support/solutions/articles/11000060257-how-do-i-generate-the-api-keys-))
1. **Currency**: Select one or more currencies that you will accept. 
1. **Deduct Payment Fees**: Set whether you will deduct the fees or not.

## Xero Integration
*Coming soon*

[paypal-9]: /setup/img/paypal-9.png "Paypal-9"
[api]: /setup/img/api.png "API Integration"
