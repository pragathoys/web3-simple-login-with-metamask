# Learn how to create a valid web3-login process with MetaMask

## Scope of the project

In this project I will try to show you the basic mechanics of a Web3 login process with the help of the MetaMask browser extension.

## Step 1 - Create an HTML page and import the relevant library

First things first! We need to create a basic HTML file and import the javascript library to interact with the Ethereum blockchain. Instead of using the heavy _Web3.js_  library we will use the _Ethers.js_ library which a lighter alternative.

Go ahead an add the following line at the top of your HTML file:
```html
<script src="https://cdn.ethers.io/lib/ethers-5.6.4.umd.min.js" type="application/javascript"></script>

```

You can review the [test_v0.html](https://github.com/pragathoys/web3-login/blob/main/test_v0.html) file for the complete source code so far.

## Usefull resources

* The Ethers.js Javascript Library - https://github.com/ethers-io/ethers.js/