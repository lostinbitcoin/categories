---
title: LNURL
taxonomy:
    category:
        - glossary
---

## LNURL
2,100 sats

LNURL makes communication between Lightning wallets and other applications easier through QR codes. LNURL enables a better user experience on Lightning by abstracting away payment flow complexities such as exchanging full-length LN invoices with counterparties.
Technically, “LNURL” is a collection of open-source protocols that work to coordinate payments on the Lightning Network by leveraging HTTP.

Users are able to login with a lightning wallet to services that support LNURL, as well as send and receive payments by utilizing static payment codes, typically in the form of a QR code. At the time of writing, LNURL has 20 features that can be implemented in applications.

The most popular features are:

・[LNURL-pay](https://github.com/lnurl/luds/blob/luds/06.md): A user scans an LNURL-pay QR code with their wallet, which then requests a Lightning invoice for the payer. This invoice can be a fixed amount or a range; the payer can also leave a message.<br>
　・[LNURL-pay-to-Lightning-Address](https://github.com/lnurl/luds/blob/luds/16.md): Users are able to pay to a static, human-readable internet identifier that looks like an email address (satoshi@your.domain). This identifier is called a [Lightning Address](https://lightningaddress.com/). Note that services who wish to offer this feature can support pay-to-lightning-address, receive-to-lightning-address, or both.<br>
・[LNURL-withdraw](https://github.com/lnurl/luds/blob/luds/03.md): An LN service generates an LNURL “endpoint”—or destination from which funds will be sent—encoded as a QR code. A user scans this QR code, and receives information like the minimum and maximum amount of funds available for withdrawal, once specified, the wallet returns the LN invoice to the service and awaits payment.<br>
・[LNURL-auth](https://github.com/lnurl/luds/blob/luds/04.md): This feature allows users to login to to services that support LNURL by signing a “login” message (presented as a QR code or text string invoice) with their LN wallet’s public key.

![](/_images/glossary-number_1.png)

Example: [stacker.news](https://stacker.news/) has LNURL-auth enabled for their login process.

Resources to learn more about LNURL:

・[bolt.fun LNURL Guide](https://bolt.fun/guide/web-services/lnurl)<br>
・[bitcoin.design Payment Request Formats Guide](https://bitcoin.design/guide/how-it-works/payment-request-formats/#lnurl)<br>
・[BOLT 12 AND LNURL: WHAT IS THE FUTURE FOR BITCOIN’S LIGHTNING NETWORK?](https://bitcoinmagazine.com/technical/bolt12-lnurl-and-bitcoin-lightning)<br>
・[Awesome LNURL](https://github.com/lnurl/awesome-lnurl)


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
