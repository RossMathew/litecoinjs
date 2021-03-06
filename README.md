# LitecoinJS 

LitecoinJS is a javascript-based implementation of various litecoin functions enabling you to natively create litecoin addresses, create transactions, set custom transaction fees and more. LitecoinJS is based on the bitcoinjs code base comprising of mostly syntactic functionality tailored for litecoin. 

SegWit is used for all functions including address generation and transaction creation.

LitecoinJS is designed to work on both regular client applications like browsers and also conventional server applications using NodeJS.

## Don't trust. Verify.

All developers and users of this library are advised to review and verify any underlying code for its validity and suitability. It’s good practice to always verify all cryptography dependencies and the associated codebase with consideration for the potential of backdoors, especially in the form of advanced and hard to spot types like mathematical backdoors.

## Features

* **Addresses**
	* Generate normal and testnet litecoin addresses.

* **Transactions**
	* Generate normal and testnet litecoin transactions.
	* Set custom change addresses.
	* Transaction batching (multiple inputs, multiple outputs). 
	* Set custom transaction fees. 
    
## Getting Started

These instructions will get you a copy of LitecoinJS up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

If you are planning to use the NodeJS version of LitecoinJS it's advisable that you have the following software and configuration on your machine -

```
NodeJS 8 or higher 
```

### Installing with NodeJS

For NodeJS applications you can download the latest version of LitecoinJS by running the following command from terminal - 
```
npm install litecoinjs
```


### Installing with browsers
Client side applications can build the browser version of LitecoinJS by the following the [browser build](https://gitlab.com/backcopy/litecoinjs/blob/master/doc/BROWSER_BUILD.md) documentation. Building for browsers enables you to easily use all LitecoinJS functions in the browser. 


## Examples
See a quick demo of various examples below. 

### Create a litecoin address 

```
const litecoinjs = require('litecoinjs');

async function newAddressExample(){
try {
    const addressPair = await litecoinjs.newAddress();
    const address = addressPair.address; // Example
    const wif = addressPair.wif; // Example 
    
        console.log(addressPair); 
	} catch (error) {
		console.error(`ERROR: ${error}`);
	}
}

newAddressExample(); 
```

Once executed, the expected return information would look something like the following - 
```
{ address: 'MBeeHGfof2EwNobqyyA5fK6bNRij5CrQAC',
  wif: 'T43wmV2KzF8qmXXvsRGUeBNS1tSFotzy8jCYQHpX1GWUYFzfnXAu' }
```

The `Wallet Import Format (WIF)` is an encoded version of the private key associated with the generated address. 

### Complete examples and usage 

* [Addresses](https://gitlab.com/backcopy/litecoinjs/blob/master/doc/examples/ADDRESSES.md) - Generating normal and testnet addresses.

* [Transactions](https://gitlab.com/backcopy/litecoinjs/blob/master/doc/examples/TRANSACTIONS.md) - Generating normal and testnet transactions.

## Running unit tests

You can execute the included automated unit tests by running the following command - 
```
npm test 
```
 
## Deployment & Production

It’s important to note that LitecoinJS is not anywhere near as extensively tested as the BitcoinJS implementation and might considerably vary in the codebase. You should run extensive testing & verification before deploying anything into production.

## Built With

* [BitcoinJS](https://github.com/bitcoinjs/bitcoinjs-lib) - Initially derrived from the BitcoinJS codebase.


## Contributing

Please read [CONTRIBUTING.md](https://gitlab.com/backcopy/litecoinjs/blob/master/doc/CONTRIBUTING.md) for details on the LitecoinJS code of conduct, and the process for submitting pull & merge requests to LitecoinJS. 

## Versioning

No stable release, TBD.

## Authors

* Edin Jusupovic 


## License

LitecoinJS is licensed under the [MIT license](https://gitlab.com/backcopy/litecoinjs/raw/master/LICENSE).

## Acknowledgments

No acknowledgments yet. 
