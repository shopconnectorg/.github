# ShopConnect 🛒⚡

## Introduction
Personalized eCommerce powered by ZKP, utilizing a novel Proof-of-Purchase system using Polygon ID. Future work would include using Sismo for custom data attestation, and Safe for a complete account abstraction UX.

## Technology & Components
1) ShopConnect Extension
This is a chrome extension wrapped around Polygon ID. We've abstracted away the original Polygon ID UX, and converted it into a smooth onboarding flow for eCommerce customers to quickly unlock personalized deals. 

2) ShopConnect Plugin
Is a JS script installed on every store. This lets the extension know that this particular eCommerce store is ShopConnect-enabled, and serves as the communication point between extension and backend.

3) ShopConnect API 
This backend server exposes endpoints that connect the extension, backend, and stores together. All requests to issue new Verifiable Credentials are made through the API, and requests to verify credentials in a user's wallet are also made through the API. ShopConnect operates an Issuer Node on the backend, allowing it to issue VCs whenever a purchase is made.

4) Polygon ID 
The Iden3 State V2 Smart Contracts have been deployed on multiple chains, including Scroll Sepolia, Mantle Testnet and Polygon zkEVM testnet (although zkEVM testnet is pending a fix by the zkEVM team before the deployment can be fully functional). We've also deployed on our Issuer Node to issue Verifiable Credentials with a custom eCommerce schema.

5) Store Mockup
Built with nextJS, tailwind 

## Technical Architecture

![ShopConnect v1 flow](https://github.com/shopconnectorg/.github/assets/757742/d30de2c9-92f4-4383-8a4c-aa47970d1a51)
