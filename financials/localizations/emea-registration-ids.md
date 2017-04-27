---
title: Registratie-id&quot;s
description: "Dit onderwerp bevat informatie over het instellen en gebruiken van registratie-id´s."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registratie-id's

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat informatie over het instellen en gebruiken van registratie-id´s.

Veel landen en regio's hebben verschillende regelingen en voorschriften voor het registreren van registratienummers of id´s. Dit onderwerp biedt een overzicht van de vereiste instellingen en de verwerking van ondersteunde registratietypen voor partijen in verschillende Europese landen/regio's. Alle landen/regio's hebben hun vereisten voor de ondersteuning van verschillende landspecifieke functionaliteiten die betrekking hebben op registratienummers die door verschillende overheidsbureaus worden verstrekt. Voorbeelden van registratienummers zijn het sociale fiscale nummer (Sofinummer), het btw-identificatienummer (TIN) en de Europese btw-identificatie (EU-btw-id). Deze functie biedt een uniform raamwerk voor alle landen in alle regio's waarbij rekening wordt gehouden met landspecifieke vereisten van bepaalde Europese landen. In de volgende gedeelten wordt de gehele stroom van informatie beschreven die wordt gebruikt voor het instellen en verwerken van registratie-id´s.

## <a name="registration-type-creation"></a>Registratietype maken
Voordat u een registratie-id kunt invoeren, moet u registratietypen instellen voor de verschillende soorten registratienummers waaraan elke partij is onderworpen. Ga naar **Organisatiebeheer** &gt; **Globaal adresboek** &gt; **Registratietypen** &gt; **Registratietypen** (pagina) om registratietypen voor leveranciers te maken en beheren voor leveranciers, klanten, werknemers en rechtspersonen in verschillende landen/regio's.

|Veld                 |Omschrijving      |
|------------------------------|----------------------------|                                                                           
| Naam                | De naam van het registratietype. |                                                                           
| Omschrijving         | De omschrijving van het registratietype. |
| Land/regio      | De unieke id van het land of de regio.|
| Belastingdienst       | De belastingdienst die aan het registratietype is gekoppeld.|
| Beperkt tot       | Het soort beperking die geldt voor het belastingregistratietype: geen, persoon, organisatie.|
| Opmaak              | De validatie-indeling voor het type registratie.|
| Kan worden bijgewerkt.      | Hiermee wordt bepaald of het registratienummer voor het registratietype kan worden bijgewerkt nadat het is ingevoerd.|
| Uniek              | Hiermee wordt bepaald of het registratienummer voor het registratietype uniek is. |
| Primair voor land/regio | Als een partij is gekoppeld aan een of meer adressen in een bepaald land en de registratie-id geldig is voor al deze adressen, moet u één adres aanwijzen als primair adres voor het land. U kunt slechts één id als primair registreren. Hiermee wordt bepaald of het registratienummer alleen als primair kan worden ingevoerd voor landadres. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Een registratietype aan een registratiecategorie toewijzen.
Registratiecategorie is een registratie-id voor land/regio die is goedgekeurd voor gebruik in een bepaald land of bepaalde regio voor belastingen, douane en andere doeleinden. Met deze categorie worden validatieregels gedefinieerd voor een bepaalde registratie-id (inclusief controlecijfers enzovoort) en de opname van de registratie-id in verschillende rapporten. Gebruik de pagina **Organisatiebeheer** &gt; **Globaal adresboek** &gt; **Registratietypen** &gt; **Registratiecategorieën** om een registratietype van een bepaald land toe te wijzen aan een ondersteunde registratiecategorie.

| Veld            | Omschrijving|
|-----------------------|----------------|
| Registratietype     | Het registratietype in een bepaald land of een bepaalde regio.|
| Beperkt tot         | Het soort beperking die geldt voor het belastingregistratietype: geen, persoon, organisatie.|
| Registratiecategorie | De unieke registratie-id die is goedgekeurd voor gebruik in het land. De volledige lijst van in AX7.1 ondersteunde categorieën vindt u hierna. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Registratie-id's voor globale-adresboekrecords invoeren
Het globale adresboek in Microsoft Dynamics 365 for Operations bevat geconsolideerde adresgegevens voor klanten, leveranciers, contactpersonen, zakenrelaties en rechtspersonen. Zie voor meer informatie [Overzicht globaal adresboek](/dynamics365/operations/organization-administration/overview-global-address-book). De partijrecords die zijn opgeslagen in het globale adresboek, kunnen een of meer adresrecords bevatten. Deze adressen worden gebruikt voor verschillende doeleinden, zoals facturering of levering. U kunt registratie-id's voor adresgegevens instellen voor klanten, leveranciers, werknemers en rechtspersonen. Zoek de partij (rechtspersoon, leverancier, klant, werknemer) waarvoor u de registratie-id wilt invoeren en klik vervolgens op **Registratie-id's** in formulieren die zijn gerelateerd aan partij, rechtspersoon, leverancier, klant, werknemer om de pagina **Adressen beheren** te openen. Klik op het tabblad **Btw-registratie** op **Toevoegen** en voer de volgende informatie over de registratie-id in.

|Veld                |Omschrijving                                                |
|---------------------|-----------------------------------------------------------|
| Registratietype   | Het registratietype in het geselecteerde land of de geselecteerde regio.     |
| Registratienummer | De partijregistratie-id.                                |
| Omschrijving         | De omschrijving van het registratienummer.               |
| Sectie             | Extra informatie over het registratienummer. |
| Uitgifteagentschap      | De belastingdienst die het registratienummer heeft uitgegeven.        |
| Uitgiftedatum         | De datum van afgifte van het registratienummer.              |
| Geldig vanaf           | De ingangsdatum van het registratienummer.           |
| Vervaldatum          | De vervaldatum voor het registratienummer.          |

> [!NOTE]
> Het btw-nummer van de rechtspersoon, leverancier, klant kan worden geselecteerd uit de registratie-id's die betrekking hebben op de btw-id, en kan voor de partij worden ingevoerd.

## <a name="search-for-records-by-registration-id"></a>Zoeken naar records op registratie-id
Zoeken naar partijrecords op basis van een registratie-id is beschikbaar op formulieren die zijn gerelateerd aan partijen, rechtspersonen, leveranciers, klanten en werknemers. Klik op **Registratie-id zoeken** om de pagina **Zoekcriteria registratie-id** te openen. Geef zoekcriteria op en klik op **Zoeken**. De geselecteerde records uit het globale adresboek en de bijbehorende typen partijrecords worden weergegeven.

## <a name="supported-registration-categories"></a>Ondersteunde registratiecategorieën
De volgende tabel bevat de ondersteunde registratietypen in Dynamics 365 for Operations. Als u vertrouwd bent met de velden in Microsoft Dynamics AX 2012 voor registratie-id's, worden in deze tabel deze velden ook toegewezen aan de Dynamics 365 for Operations-registratiecategorieën.

| Dynamics 365 for Operations-registratiecategorie         |Land/regio  | Dynamics AX 2012-term/veld|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Btw-id                                                        | Alle landen van de Europese Unie (EU)|  Btw-nummer (wettelijk type belasting-id in AX2012 R3)|
| Ondernemings-id (COID)                                          | België,Tsjechische Republiek,Estland,Hongarije,Letland,Litouwen,Polen,Zwitserland | Ondernemingsnummer (EnterpriseNumber) Registratienummer (RegNum\_W) Registratienummer (RegNum\_W) Registratienummer (RegNum\_W) Registratienummer (RegNum\_W) Ondernemingscode (EnterpriseCode) Registratienummer (RegNum\_W) UID (wettelijk type UID in AX2012 R3) |
| Vestigings-id                                                     | België            | Vestigingsnummer (BranchNumber)|
| Spisová značka (registratienummer, uitgevende bank, sectie) | Tsjechische Republiek     | Nummer bijvoegsel (CommercialRegisterInsetNumber) Bewaard in handelsregister (CommercialRegister) Sectie van handelsregister (CommercialRegisterSection)|
| Klant-id van de douane                                           | Finland | Klantnummer voor douanezaken (CustomsCustomerNumber\_FI)|
| INN                                                           | Russische Federatie| INN (wettelijk type INN in AX2012 R3)|
| RRC                                                           | Russische Federatie| RRC (wettelijk type RRC in AX2012 R3)|
| OKDP                                                          | Russische Federatie| OKDP (wettelijk type OKDP in AX2012 R3)|
| OKPO                                                          | Russische Federatie| OKPO (wettelijk type OKPO in AX2012 R3)|
| RCOAD                                                         | Russische Federatie| RCOAD (wettelijk type RCOAD in AX2012 R3)|
| OGRN                                                          | Russische Federatie| OGRN (wettelijk type OGRN in AX2012 R3) |
| SNILS                                                         | Russische Federatie| SNILS (wettelijk type SNILS in AX2012 R3)|
| CIFTS                                                         | Russische Federatie| CIFTS (wettelijk type CIFTS in AX2012 R3)|

Zie de volgende taakregistraties voor btw-id in Lifecycle Services (LCS) voor meer informatie over verwerken van registratie-id´s, waaronder vereisten:

-   Btw-id instellen
-   Registratie van btw-id van leverancier
-    Een partij zoeken door middel van het btw-id





