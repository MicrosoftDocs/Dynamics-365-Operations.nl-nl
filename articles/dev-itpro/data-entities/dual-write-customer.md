---
title: Geïntegreerd klantmodel
description: In dit onderwerp wordt de integratie van klantgegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a8030d9d1f1f3636a679d334afddad0f573a824e
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789171"
---
## <a name="integrated-customer-master"></a>Geïntegreerd klantmodel

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Het is gebruikelijk dat klantrecords in meer dan één toepassing worden beheerst. Verkoopactiviteiten kunnen bijvoorbeeld commerciële klantrecords inbrengen via een Microsoft Dynamics 365 for Sales-toepassing en e-Commerce- of detailhandelsverkopen kunnen klantrecords inbrengen via een Dynamics 365 for Finance and Operations-toepassing. Ongeacht waar de klantgegevens vandaan komen, worden ze achter de schermen geïntegreerd over toepassingsgrenzen en infrastructuurverschillen heen. Geïntegreerd klantbeheer helpt bij het afhandelen van scenario's met meervoudig beheer en biedt een uitgebreid overzicht van de klant naar de Dynamics 365 Application Suite.

## <a name="customer-data-flow"></a>Klantgegevensstroom

*Klant* is een goed gedefinieerd concept in zowel Finance and Operations als Common Data Service. Daarom bestaat de integratie van klantgegevens alleen uit het harmoniseren van het klantconcept tussen Finance and Operations en Common Data Service-toepassingen. In de volgende afbeelding wordt de klantgegevensstroom weergegeven.

![Klantgegevensstroom](media/dual-write-customer-data-flow.png)

Klanten kunnen globaal worden ingedeeld in twee typen: commerciële/organisatorische klanten en consumenten/eindgebruikers. Deze twee typen klanten worden in Finance and Operations en Common Data Service op een andere manier opgeslagen en verwerkt.

In Finance and Operations worden zowel commerciële/organisatorische klanten als consumenten/eindgebruikers in één tabel met de naam **CustTable** (CustomerCustomerV3Entity) beheerd en worden ze geclassificeerd op basis van het kenmerk **Type**. (Als **Type** is ingesteld op **Organisatie**, is de klant een commerciële/organisatorische klant en als **Type** is ingesteld op **Persoon**, is de klant een consument/eindgebruiker.) De primaire contactpersoonsgegevens worden afgehandeld via de entiteit SMMContactPersonEntity.

In Common Data Service worden commerciële/organisatorische klanten beheerd in het entiteit Account en worden ze geïdentificeerd als het kenmerk **RelationshipType** kenmerk is ingesteld op **Klant**. Zowel consumenten/eindgebruikers als de contactpersoon worden vertegenwoordigd door entiteit Contactpersoon. Om een duidelijke scheiding te maken tussen een consument/eindgebruiker en een contactpersoon, heeft de entiteit **Contactpersoon** een Booleaanse vlag met de naam **Verkoopbaar**. Wanneer **Verkoopbaar** de waarde **Waar** heeft, is de contactpersoon een consument/eindgebruiker en kunnen er voor die contactpersoon offertes en orders worden gemaakt. Als **Verkoopbaar** is ingesteld op **Onwaar**, is de contactpersoon slechts een primaire contactpersoon van een klant.

Wanneer een niet-verkoopbare contactpersoon deelneemt aan een offerte- of orderproces, is **Verkoopbaar** ingesteld op **Waar** om de contactpersoon te markeren als een verkoopbaar contact. Een contactpersoon die een verkoopbaar contact is geworden, blijft een verkoopbaar contact.

## <a name="templates"></a>Sjablonen

Klantgegevens omvatten alle informatie over de klant, zoals de klantgroep, adressen, contactgegevens, betalingsprofiel en factuurprofiel. Een verzameling entiteitstoewijzingen werkt samen tijdens interactie met klantgegevens, zoals in de volgende tabel wordt weergegeven.

Finance en Operations    | Customer Engagement-toepassing
--------------------------|---------------------------------
Klant V3               | Rekening
Klant V3               | Contactpersoon
CDS-contactpersonen V2           | Contactpersoon
Klantengroepen           | Msdyn\_customergroups
Betalingsmethode van klant   | Msdyn\_customerpaymentmethods
Loyaliteitskaart              | Msdyn\_loyaltycards
Betalingsschema          | Msdyn\_paymentschedules
Betalingsschema          | Msdyn\_paymentschedulelines
Betalingsdag CDS           | Msdyn\_paymentdays
Betalingsdagregels CDS     | Msdyn\_paymentdaylines
Betalingscondities          | Msdyn\_paymentterms
Voor- en achtervoegsel naam              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Klant V3 naar Account

Deze sjabloon synchroniseert klantmodelinformatie voor commerciële en organisatorische klanten tussen Finance and Operations en Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | beschrijving
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | geen
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
geen | \>\> | address1\_addresstypecode
geen | \>\> | customertypecode
PARTYTYPE | \<\< | geen
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Klant V3 naar Contact

Deze sjabloon synchroniseert klantmodelgegevens voor consumenten en eindgebruikers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
geen | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | geen
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | geen
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | geen
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
geen | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
geen | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
geen | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | beschrijving

## <a name="contacts"></a>Contacten

Deze sjabloon synchroniseert alle primaire, secundaire en tertiaire contactgegevens, zowel voor klanten als leveranciers, tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-contacts.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | geen
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | afdeling
NOTES | = | beschrijving
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
geen | \>\> | msdyn\_contactforvendor
geen | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Klantengroepen

Deze sjabloon synchroniseert informatie over klantengroepen tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-customer-groups.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
BESCHRIJVING | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Betalingsmethoden van klant

Deze sjabloon synchroniseert informatie over klantbetalingsmethoden tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAAM | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
BESCHRIJVING | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Loyaliteitskaarten

Deze sjabloon synchroniseert informatie over loyaliteitskaarten tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Betalingsschema's

Deze sjabloon synchroniseert referentiegegevens over betalingsschema's voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-payment-schedules.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAAM | = | msdyn\_name
BESCHRIJVING | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Regels van betalingsschema

Deze sjabloon synchroniseert referentiegegevens over betalingsschemaregels voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Betalingsdagen

Deze sjabloon synchroniseert referentiegegevens over betalingsdagen voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-payment-days.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
NAAM | = | msdyn\_name
BESCHRIJVING | = | msdyn\_description

## <a name="payment-day-lines"></a>Regels van betalingsdagen

Deze sjabloon synchroniseert regels van betalingsdagen voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NAAM | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Betalingsvoorwaarden

Deze sjabloon synchroniseert referentiegegevens van betalingstermijnen voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-payment-terms.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
BESCHRIJVING | = | msdyn\_description
NAAM | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Voor- en achtervoegsel naam

Deze sjabloon synchroniseert voor- en achtervoegsels van namen voor zowel klanten als leveranciers tussen Finance and Operations en Customer Engagement.

<!-- ![](media/dual-write-name-affixes.png) -->

Bronveld | Toewijzingstype | Doelveld
---|---|---
AFFIX | = | msdyn\_affix
TYPE | \>\< | msdyn\_affixtype
BESCHRIJVING | = | msdyn\_description
