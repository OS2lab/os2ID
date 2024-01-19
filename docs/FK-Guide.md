# 👣 Step-by-Step Guide

## 1. Obtain a Certificate


> [!IMPORTANT]  
> Section not done - Add info about cost and billing

To verify ownership of your IT-system and secure communications between it and Fælleskommunal Infrastruktur (FKI) a certificate is needed.

To order a certificate for your system, [log in to MitID Erhverv](https://mitid-erhverv.dk) and follow the guide linked below.

### 🔗 Links
> [MitID Erhverv - Login](https://mitid-erhverv.dk)
>
> [MitID Erhverv support - Guide for ordering a certificate ](https://mitid-erhverv.dk/support/vejledning/anvendelse/brugeradministrator/certifikater/bestil-et-organisationscertifikat/)

 ## 2. Sign up as a service provider

> [!IMPORTANT]  
> Section not done - Need more info on employee access rights management in MitID erhverv.

Before you can use Fælleskommunal Adgangstyring (FA), your Company / Municipality needs to sign up. This can be done at Digitaliserings Kataloget's site [Oprette organisation i det Fælleskommunale Administrationsmodul](https://digitaliseringskataloget.dk/oprette-organisation-i-det-faelleskommunale-administrationsmodul). Do pay in mind, that signing up to use FA entails an __administration fee__. Information regarding price, and more, can be found on the sign-up page. After registration and subsequent approval from KOMBIT, sign-in to the Administration module will happend throught MitID. Any employee that needs to access the administration module, will need to be granted the right access level by an administrator of the company, which is managed through MitID erhverv

# Oprette organisation i det fælleskommunale administrationsmodul

This is a digital service that allows you to create and manage your own organization in the common municipal administration system, which is used by all municipalities in Denmark. The service is intended for municipal employees who need to create or update their organization's information, such as name, address, contact details, budget, etc.

## How to use the service

To use the service, you need to follow these steps:

1. Log in to the common municipal administration system with your username and password. You can access the system from this link: [Administrationsmodul].
2. On the main page, click on the **Organisation** tab on the left side menu. This will open a list of all the existing organizations in the system.
3. To create a new organization, click on the **Opret ny organisation** button at the top right corner of the page. This will open a form where you can enter the details of your organization.
4. Fill in the required fields, such as **Navn** (Name), **Adresse** (Address), **Telefon** (Phone), **E-mail** (Email), etc. You can also add optional fields, such as **Beskrivelse** (Description), **Budget** (Budget), **Mål** (Goals), etc.
5. When you are done, click on the **Gem** button at the bottom of the form. This will save your organization and add it to the list of organizations in the system.
6. To edit or delete your organization, you can click on the **Rediger** or **Slet** buttons next to your organization's name in the list.

## 3. Register and configure IT System

Log in to the administration webportal Fælleskommunalt Administrationsmodul(FKAM), using MitID, and configure your IT system in Fælleskomunal Infrastruktur(FKi)

### 🔗 FKAM Web Portal acess

> [Test - https://admin-test.serviceplatformen.dk/](https://admin-test.serviceplatformen.dk/)
>
> [Prod - https://admin.serviceplatformen.dk/](https://admin.serviceplatformen.dk/)

### 📖 User guides

> [Brugervejledning for
> leverandører - docs.kombit.dk](https://docs.kombit.dk/id/3921b1af "docs.kombit.dk") (🇩🇰 in Danish)
>
> [Video guide - Tilslut brugervendt system](https://vimeo.com/484429700#t=187s "vimeo.com") (🇩🇰 in Danish, old video guide from 2020)

### 4. Establish Trust and Define SAML Configuration

> [!IMPORTANT]  
> Section not done - how to establish the trust - screenshots?

In order to authenticate via FKIS you must first register your Service Provider (SP) and establish SAML Trust between your SP and the Context Handler (IdP). Trust is established by exchanging SAML metadata between IdP and SP.
The metadata is typically generated automtically by your SAML framework, based upon your configuration. The metadata contains infomration such the ID of your service provider, the URL where authentication SAMLRequests are sent, the "Assertion Consumer Service" url where the SAMLResponses should be returned, which user attributes are requested, certificate information for use in signing and encrypting the SAMLRequest and more. An example of how your SP metadata should look like can be found on the [introduktionside](https://digitaliseringskataloget.dk/l%C3%B8sninger/adgangsstyring-brugere) under "Vejledninger" and "[Eksempel: metadata for brugervendt system](https://digitaliseringskatalog.dk/sites/default/files/2020-05/Brugervendt%20system%20metadata%20eksempel.xml)". Please note that all endpoints included in the metadata require that you use HTTPS, else FKIS will __not__ accept the metadata.

When you have generated your metadata sign in to the administration module ... (more to come)


## 💬 FAQ

### What is Fælleskommunal Adgangsstyring(FKa)?

*The purpose of FKa is to handle authentication and authorization within "Fælleskommunal Infrastruktur" (FKi) in Denmark.
FKa is based on OIOSAML, a specialized configuration of the SAML protocol.*

📖 Read more:

> [Digitaliseringskataloget - Hvad er den fælleskommunale infrastruktur](https://digitaliseringskataloget.dk/om-den-f%C3%A6lleskommunale-infrastruktur "digitaliseringskataloget.dk") (🇩🇰 in Danish)
>
> [Digitaliseringskataloget - Adgangsstyring for brugere](https://digitaliseringskataloget.dk/l%C3%B8sninger/adgangsstyring-brugere "digitaliseringskataloget.dk") (🇩🇰 in Danish)
>
> [Digitaliseringsstyrelsen - OIOSAML 3](https://digst.dk/it-loesninger/nemlog-in/anvendelse/oiosaml-3/ "digst.dk") (🇩🇰 in Danish)

### What is Fælleskommunalt Administrationsmodul (FKAM)?

The FKAM administrative module is a webportal that allows service providers to register and maintain applications with FKi, enter service agreements, maintain job function roles and extract IT system reports

📖 Read more:

> [Digitaliseringskataloget - Fælleskommunalt Administrationsmodul](https://digitaliseringskataloget.dk/l%C3%B8sninger/administrationsmodul "digitaliseringskataloget.dk") (🇩🇰 in Danish)

### What is the Context Handler?

The Context Handler is a proxy-service in front of your Identity Provider (IdP) that secures login requests from the user organization to the application or "IT system" re

📖 Read more:

> [Digitaliseringskataloget - Context Handler](https://digitaliseringskataloget.dk/l%C3%B8sninger/adgangsstyring-brugere#ContextHandler "digitaliseringskataloget.dk") (🇩🇰 in Danish)

### What are OCES and FOCES certificates?

*"Offentlige certifikater til Elektronisk Service" (OCES) issued by Digitaliseringsstyrelsen - The Danish Agency for Digital Government  are used for service access and data encryption and are registered to your organisation (with organization’s name, registration number, email)
"Funktionscertifikater" or "Systemcertifikater" are OCES certificates with added system-specific metadata and are used for secure system to system communication.*

📖 Read more:

> [MitID Erhverv - Certifikater](https://mitid-erhverv.dk/avanceret/certifikater/ "MitID Erhverv") (🇩🇰 in Danish)
