# Learn how to create a valid web3-login process with MetaMask

## Scope of the project

In this project I will try to show you the basic mechanics of a Web3 login process with the help of the MetaMask browser extension and the powerful Ethers.js javascript library.

First we will try to verify if the user has the MetaMask browser extension installed and enabled. Then we will give  the user the option to click on a link and verify his wallet by signing with with MetaMask account.

## Introduction

The MetaMask browser extension is a crypto wallet and a major gateway to blockchain apps used by many millions of users world wide.

The Ethers.js is a complete Ethereum wallet implementation and utilities in JavaScript (and TypeScript).

## Step 1 - Create an HTML page and import the relevant library

First things first! We need to create a basic HTML file and import the javascript library to interact with the Ethereum blockchain. Instead of using the heavy _Web3.js_  library we will use the _Ethers.js_ library which a lighter alternative.

Go ahead and add the following line of code at the top of your HTML file:
```html
<script src="https://cdn.ethers.io/lib/ethers-5.6.4.umd.min.js" type="application/javascript"></script>

```

You can review the [test_v0.html](https://github.com/pragathoys/web3-login/blob/main/test_v0.html) file for the complete source code so far.

## Step 2 - Verify if the user has the MetaMask extension installed

MetaMask injects a global API into websites visited by its users at window.ethereum. This API allows websites to request users' Ethereum accounts, read data from blockchains the user is connected to, and suggest that the user sign messages and transactions. The presence of the provider object indicates an Ethereum user.

Firstly, lets add the following code to detect if the user's browser has the MetaMask extension installed:

```javascript
            async function web3_check_metamask() {
                if (!window.ethereum) {
                    console.log('It seems that the MetaMask extension is not detected. Please install MetaMask first.');
                    alert('It seems that the MetaMask extension is not detected. Please install MetaMask first.');
                    return;
                }else{
                    console.log('MetaMask extension has been detected!!');
                }
            }   
```

add this code inside the HEAD tag of your HTML file.

Also add the following link to trigger it for testing:
```html
<a href="#!" onclick="web3_check_metamask();">detect MetaMask</a>
```

One good way to test the output inthe absence of the extension it is to use an Incognito window with Chrome.

You can review the [test_v1.html](https://github.com/pragathoys/web3-login/blob/main/test_v1.html) file for the complete source code so far.

## Usefull resources

* MetaMask - https://metamask.io/
* Ethereum Provider API - https://docs.metamask.io/guide/ethereum-provider.html
* The Ethers.js Javascript Library - https://github.com/ethers-io/ethers.js/