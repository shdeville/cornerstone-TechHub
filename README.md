# TechHub Cornerstone Theme v6.16.1

These are the custom theme files used for the TechHub BigCommerce website, built on top of Cornerstone v6.16.1

Please follow the Stencil development guides found at these links for general development and packaging instructions - 
* Installing Stencil: https://developer.bigcommerce.com/docs/storefront/stencil/cli/install
* Live Previewing a Theme: https://developer.bigcommerce.com/docs/storefront/stencil/cli/development-server
* Stencil CLI Options and Commands: https://developer.bigcommerce.com/docs/storefront/stencil/cli/options-and-commands

# You May Also Need -

* TechHub Theme Enhancements and Features: https://github.com/shdeville/TechHub-Theme-Enhancement-and-Features
* TechHub Checkout Scripts: https://github.com/shdeville/Checkout-Scripts
* TechHub One Page Checkout: https://github.com/ehansontamu/One-Page-Checkout-TechHub

# How to Start -

Clone this repo and make sure all customizations made to your theme files are properly outlined in your commits. Make note of all files that you make changes to, and leave comments/documentation for each change.

# Changes You'll Need to Make -

The TechHub customized theme files have the "Sign In" URL hardcoded in the navigation.html file. You will need to replace this with your store's SSO URL (this can be created via MiniOrange Application).

A quote button (and link depending on login group) has been hardcoded in the cart.html page. This needs the quote_builder.js script in the Theme Enhancements and Features repo to work properly. This code displays a quote button for non-logged in users or group 10 users in lieu of a checkout button, and it adds a link beneath the normal checkout button that says "save quote as PDF" for other customers.

The Lang files include changes for guests and quotes for non-logged in or guest users. The logic for displaying these assumes that all non-logged in users or users within group 10 are considered guests. If you need to change this verbage, you may do so in the en.lang file.
Additionally a "guest banner" is hard coded into header.html, this banner will only appear for users within group 10. You can remove this code or simply not use customer group 10 if you don't want to have a guest banner appear.

CSS for some pagebuilder elements will be specific to each instance, so some CSS configuration will be needed for your store. This can be done in the theme.scss file.
