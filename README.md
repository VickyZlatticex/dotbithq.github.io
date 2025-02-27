# Introduction

> .bit to the crypto world is what Phone/Email to the Internet.

.bit is a blockchain-based, open source, cross-chain decentralized account system that provides a globally unique naming system with a .bit suffix that can be used for cryptocurrency transfers, domain name resolution, authentication, and other scenarios.

.bit is the first decentralized account system with broad compatibility, allowing users to register and manage the .bit accounts using any public chain address or even email.

The core elements of a .bit account are: the owner/manager, and the parsed record (i.e. the data it is associated with). Unlike ENS, the owner/manager of .bit can be any public chain private key or even email; unlike DNS, .bit supports any type of parsed record.

The structure of a .bit account is as follows.

<img src="./image-20210721120318336.png" alt=".bit Account Structure" />

.bit is a decentralized application running on [Nervos CKB](https://www.nervos.org/). .bit accounts and related parsed records are stored on the permissionless blockchain. Nervos CKB is a PoW public chain with a highly open architecture using the UTXO model.

.bit have five main components:

1. **Core Protocol**

   This refers to a series of Lock Scripts and Type Scripts deployed on the Nervos CKB, which define the .bit accounts and related operational standards for .bit accounts, and are concrete implementations of the .bit core protocols. 

2. **Keeper**

   Keeper is a set of off-chain programs that can be run by anyone without permission, and is responsible for triggering a series of transactions that conform to the core protocol. Running a Keeper earns .bit system rewards.

3. **Resolution Service**

   It resolves the global state of .bit based on the transactions on Nervos CKB and provides account resolution service in the form of an interface to the public.

4. **Client SDK**

   Includes SDKs in various languages to simplify the integration of mobile wallets, web wallets, server wallets and other .bit-related applications.

5. **Dapp UI**

   Users ultimately use the various features of .bit through a variety of application interfaces. These applications can be used directly in the browser or can be integrated into popular wallet software.

The source code for all the components above can be found on our [Github repository](https://github.com/dotbitHQ). Also, developers can implement their own Keeper, Resolution Service, Client SDK, Dapp UI based on Core Protocol.
