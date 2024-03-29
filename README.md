# One-Page-Checkout-Installation-Instruction



One-page Checkout Documentation
This documentation guides you through the seamless integration and activation of the One-Page Checkout Module for WHMCS, designed to condense the entire order process into a single, user-friendly page. From installation to customization, follow these steps to enhance your customer's journey and boost efficiency.
# Installation Instructions To install the module, follow these steps:
Download the zip file and extract it.
Upload the files into your WHMCS root directory.
Cross-check that the files are placed according to the following image reference:
# 1. Addon Module File Placement:
The addon module file should be placed in your WHMCS for this path - **whmcs_root/modules/addons**. Refer to this image for more details:

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/139d6e55-9dd3-4445-8fbe-d3b4367b2471)

   

# 2. Order Form Template Integration:
The order form template files should be placed in your WHMCS for this path - **whmcs_root/templates/orderforms**. Refer to this image for more details: 

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/55489684-3a1d-4072-accf-038d06c385f2)


# 3. Language variables
Go to the **whmcs_root/lang** folder and check if the overrides folder exists. If the overrides folder does not exist, create the folder with the name overrides and create the file according to your WHMCS language. 

For example, if your WHMCS has English language, create an english.php file and add the code mentioned below. Otherwise, add only language variables into your file as per the WHMCS language.
```
        <?php

if (!defined("WHMCS")) die("This file cannot be accessed directly");

$_LANG['locale'] = "en_GB";

$_LANG['wdOnePageContactAdmin'] = " Please contact with whmcs administrator for same.";
$_LANG['wdOnePageThisDoman'] = "this domain ";
$_LANG['wdOnePageHaveDomain'] = "This product have domain required please add domain Or there is domain in cart will assign that domain. you can manage it later.";
$_LANG['wdOnePageAllowDomainReg'] = " Please ask whmcs admin to allow domain registration.";
$_LANG['wdOnePageRegTransferDomain'] = "Register/Transfer Domain";
$_LANG['wdOnePageManageDomainProduct'] = "Manage Domain with Product";
$_LANG['wdOnePageManageDomainOption1'] = "Choose Prefered Action For Domain";
$_LANG['wdOnePageManageDomainOption2'] = "Remove Domain From Product";
$_LANG['wdOnePageDomainRequired'] = "Domain Required";
$_LANG['wdOnePageDomainAssignedAlready'] = "Domain Already assigned to this product. try to remove and then reassign.";
$_LANG['wdOnePageAssignDomainError'] = "Assign domain to your hosting services to complete the order";
$_LANG['wdOnePageOwnDomainAdd'] = "Your domain is assigned to product. Check summary for same.";
$_LANG['wdOnePageBuyDomainHosting'] = "Domain";
$_LANG['wdOnePageSubDomainAdd'] = "Your subdomain is assigned to product. Check summary for same.";
$_LANG['wdOnePageSubDomainError'] = " is already assign try with another one.";
$_LANG['domainavailable1'] = "Congratulations!";
$_LANG['domainavailable2'] = "is available!";
$_LANG['wdOnePageShowLess'] = "show less!";
$_LANG['wdOnePagePrefferedTld'] = "Preffered tld is not available.";

$_LANG['wdOnePageSaveCycle'] = "Save";
$_LANG['wdOnePageCycleAt'] = "at";
$_LANG['wdOnePageCycleChange'] = "Change Billing Cycle";
$_LANG['wdOnePageCycleAlert'] = "You Must Select the billing cycle";
$_LANG['wdOnePageCycleAlertTitle'] = "Choose Billing Cycle";
$_LANG['wdOnePageCycleAlertBtnOk'] = "Ok";
$_LANG['wdOnePageBillingCycle'] = "Billing Cycle";
$_LANG['pricingCycleLong']['onetime'] = "One Time";

$_LANG['wdOnePageChooseProductGroup'] = "Choose Product Group";
$_LANG['wdOnePageSelectProductGroup'] = " --Select Product Group-- ";
$_LANG['wdOnePageSelectProduct'] = "Select Product Addon";

$_LANG['wdOnePageRemovePromoCode'] = "Are you sure you want to remove promo code?";
$_LANG['wdOnePagePromoCode'] = "Promo Code";
$_LANG['wdOnePagePromoAlertTitle'] = "Promo code error.";
$_LANG['wdOnePageHavePromoCode'] = "Have a promo code ?";

$_LANG['wdOnePageChoosePlan'] = "Choose Your Plan";
$_LANG['wdOnePageHostingPlan'] = "Select Hosting Plans";

$_LANG['wdOnePageSignSignup'] = "Sign In / Sign Up";
$_LANG['wdOnePageRemoveCart'] = "Remove";
$_LANG['wdOnePageMoneyBackMainHeading'] = "30 days money back guarantee";
$_LANG['wdOnePageMoneyBackTagLine'] = "You have 30 days to change your mind in case you are not satisfied.";
$_LANG['wdOnePageMoneyBackNotes'] = "*refund does not apply to domain names";
$_LANG['wdOnePageRemoveButton'] = "Remove";
$_LANG['wdOnePageBuyHosting'] = "Buy Hosting +";
$_LANG['wdOnePageButtonAdded'] = "Added";
$_LANG['wdOnePageOnSale'] = "On Sale";
$_LANG['wdOnePageBillMainHeading'] = "Select Term length";
$_LANG['wdOnePageBillMainDescrp'] = "Lock in your saving with a multi year term.";
$_LANG['wdClickToViewCart'] = "Click Here To See Cart";
```

# Module Activation steps
Log in to your WHMCS Admin account and navigate to **Settings > System Settings > Addon Modules> One Page Checkout Module**. Click on the Activate button.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/0e0514d3-51eb-45ef-ba25-ddb27be5ff6c)

Manage your access control settings to allow selected users to manage this addon module setting. You can also tick or untick the delete database checkbox to manage the module table deletions when deactivating the module.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/fe5a01a2-70ab-4410-8920-8c60ee8948c7)


Your module is now activated. You need to set the default order form as well. To set the default order form, go to **Settings > General Settings > Ordering tab**. Select Whmcsdigitalonepagecheckout as the default template and click on the Save button.
![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/505d7018-343b-46d8-bbc1-d14f764ea178)

# Note:

By default, the WHMCS domain ordering process has a step of Captcha filling. As we have made custom functionality of one-page checkout, you need to disable the domain captcha from the admin side.
Follow these steps to disable the domain captcha:
Go to **Settings > General Settings > Security tab**.
Uncheck the Domain checker checkbox and click on the Save Changes button.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/664b1d54-6db6-40a2-87d4-38f47dfc50cb)


# Stripe Gateway Setup
Great news! We've thoroughly examined the default Stripe gateway documentation and addressed a crucial compatibility issue with the Modern or Boxes order form templates. However, we have worked on the module for this part and made the order form compatible with the Stripe payment gateway.

To set up the Stripe gateway, follow these steps:

Create a hidden product with a price greater than 0 and input its ID into the module settings form.
Once the module is activated, navigate to **Addons -> One Page Checkout -> Settings**.
Enter the ID of your hidden product and click the "Save Changes" button.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/6376f2a6-5bbd-4985-a589-912d36765fb6)


# View Offers and Disclaimer Page
If you have a dedicated page related to offers and disclaimer information, you can pass the URL link into the WHMCS module form. Users can view this page while placing their orders. To set up the offers and disclaimer page, go to **Addons > One Page Checkout > Settings**, enter your page URL, and click on the Save Changes button.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/c133dec9-5d2e-44db-8515-a184c7850fbf)

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/502e5511-4349-4d8a-860e-bd9277a39377)



# Manage Color Settings
Admin users have the flexibility to control the colors of the order form template.
To access and modify the color settings, navigate to **Addons > One Page Checkout > Color Schema**.
Admin users can toggle custom colors on or off and fine-tune the color palette to align with their preferences.

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/29e1c592-76bc-4c19-992e-c693aed2ed65)



# Do your own CSS:
To customize the color of your order form page, access the color schema page on the admin side. If further customization is required, rename the file "overrides.css.rename" to "overrides.css" at the specified path below. You can then write your custom CSS within this file to tailor the color scheme according to your preferences.

### Path: whmcs_root/templates/orderforms/whmcsdigitalonepagecheckout/assets/css/overrides

![image](https://github.com/rakesh-610weblab/One-Page-Checkout-Installation-Instruction/assets/154584764/1c1b616b-6f3f-4981-af9b-c455b831c508)



