# References

* [PSD-2 Summary](https://ec.europa.eu/info/law/payment-services-psd-2-directive-eu-2015-2366_en)
    * [Directive 2015/2366/EU](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32015L2366)
    * [Commission delegated regulation supplementing Directive](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32018R0389)
    * [European Banking Authority (EBA) guidelines](https://www.eba.europa.eu/regulation-and-policy/payment-services-and-electronic-money)
    * [WSO2 Open Banking Key Concepts](https://docs.wso2.com/display/OB130/Key+Concepts)

## Terms & Abbreviations

* **AIS** - _Account information services_.
* **AISP** - _Account Information Service Provider_.
  This entity offers information services about the payment accounts. The related services can be identified as AIS (Account Information Service).
* **ASPSP** - _Account Servicing Payment Service Provider_.
  This is the entity where the payment accounts resides. It receives payment requests, receive payments, provides information on managed payment accounts.
* **CA** - Competent authority
* **CBPII** - Card based payment instrument issuer
* **CP** - Consultation Paper
* **EBA** - European Banking Authority
* **GL** - Guidelines
* **PIS** - Payment initiation services
* **PISP** - _Payment Initiation Service Provider_.
  This entity provides the PSU with the service to set up payment transactions; the related services supplied can be identified as PIS (Payment Initiation Service)
* **PIISP** - _Payment Instrument Issuer Service Provider (also known as **CISP** – Card Issuing Service Provider)_.
  This entity provides information about the funds availability on PSD2 payment transactions based on the payment cards. The related services supplied can be identified as FCS (Confirmation on the Availability of Funds Service).
* **PSP** - Payment service provider
* **PSU** - _Payment service user_.
   He is the subject using all the payment services defined and provided by the PSD2 ecosystem.
* **TPP** - _Third Party Provider_.
  A general definition of the provided services inside the PSD2 on behalf of a PSU. A TPP may have one or more of the PISP, AISP, PIISP roles and it is able to communicate with the involved ASPSPs through the interfaces defined by the PSD2 Gateway.
* **RTS** - Commission Delegated Regulation (EU) 2018/389 with regard to regulatory technical standards for strong customer authentication and ommon and secure open standards of communication

### More

[Source](https://www.cbiglobe.com/Wiki/index.php/2._Actors_and_definitions)

- ASPSP are obliged to **receive and manage payment orders** initiated by its customers through PISP that are qualified to operate in the European Union.
- PISPs can offer to customers of the ASPSPs **initialisation services for payment orders** directed to all ASPSPs in which they have payment accounts
- PISPs are authorised exclusively to operate the new payment service and never to enter into possession of the funds of the debtor
- ASPSPs are obliged to **provide payment account information upon request** of their customers that are users of those AISPs authorised to work in the European Union
- AISPs can offer customers of ASPSPs **information aggregation services on payment accounts** that are held by the ASPSPs
- AISPs cannot use customer data or access the payment accounts for purposes other than those provided by the service authorised by the customer
- PISPs and AISPs must obtain **authorisation** to operate in relation to payment services with the Competent authority, demonstrating that they meet the necessary requirements
- CISPs can **make a request to the ASPSP** of the user for the availability of funds before the execution of the card-based payment
- The request can take place **only if the account of the debtor is accessible online and if he had previously issued the consent** to the ASPSP – Account Servicing Payment Service Provider – and to the CISP

## The Berlin Group

[The Berlin Group](https://www.berlin-group.org/) is a pan-European payments interoperability standards and harmonisation initiative with the primary objective of defining open and common scheme- and processor-independent standards in the interbanking domain between Creditor Bank (Acquirer) and Debtor Bank (Issuer), complementing the work carried out by e.g. the European Payments Council
* [NextGenPSD2 Downloads](https://www.berlin-group.org/nextgenpsd2-downloads)
* [General Introduction Paper](https://docs.wixstatic.com/ugd/c2914b_c6a8a0dca83e4af8859be266415d3d79.pdf)
* [Operational Rules](https://docs.wixstatic.com/ugd/c2914b_39d88d82249d482ebcb9a92ebf03d159.pdf)
* Implementation Guidelines [[v1.1](https://docs.wixstatic.com/ugd/c2914b_5351b289bf844c6881e46ee3561d95bb.pdf)]
* [Changelog](https://docs.wixstatic.com/ugd/c2914b_4967de615bc34a07a99d95ec875dd885.pdf)


## Certificate OID

All roles data is located under version 3 QCStatements section obtainable at OID `1.3.6.1.5.5.7.1.3`.
Then roles can be matched in following OIDs:

* `0.4.0.19495.1.1` - Accounting Service (PSP_AS)
* `0.4.0.19495.1.2` - Payment Initiator (PSP_PI)
* `0.4.0.19495.1.3` - Account information (PSP_AI)
* `0.4.0.19495.1.4` - Issuing of card-based payment instruments (PSP_IC)