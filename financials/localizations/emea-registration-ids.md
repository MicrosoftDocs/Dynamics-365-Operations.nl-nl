---
title: Registratie-id&quot;s
description: Dit onderwerp biedt informatie over het instellen en gebruiken van registratie-id&quot;s.
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

Dit onderwerp biedt informatie over het instellen en gebruiken van registratie-id's.

Veel landen en regio's hebben verschillende regelingen en voorschriften voor het vastleggen van nummers of id's. Dit onderwerp biedt een overzicht van de vereiste instellingen en de verwerking van ondersteunde registratietypen voor partijen in verschillende europese landen/regio's. Alle landen/regio's hebben hun vereisten voor de ondersteuning van verschillende landspecifieke functies die betrekking hebben op de registratienummers in die door verschillende staat kantoren. Voorbeelden van registratienummers zijn, sociaal-fiscaalnummer (Sofinummer), btw-identificatienummer (TIN) en europees btw-identificatie (EU-btw-ID). Deze functie biedt uniform raamwerk voor alle landen in alle regio's houdend rekening landspecifieke vereisten van bepaalde europese landen. De volgende secties beschrijven de totale stroom van informatie die wordt gebruikt voor het instellen en registratie-id's verwerken.

## <a name="registration-type-creation"></a>Het maken van registratie
Voordat u de belastingregistratie-ID invoeren kunt, moet u de registratietypen voor de verschillende soorten registratienummers in die elke partij is onderworpen aan instellen. Ga naar **Organisatiebeheer**&gt;**algemeen adresboek**&gt;**registratietypen**&gt;**registratietypen** pagina maken en beheren van registratietypen voor leveranciers, klanten, werknemers en rechtspersonen in verschillende landen/regio's.

|Veld                 |Omschrijving      |
|------------------------------|----------------------------|                                                                           
| Naam                | De naam van het registratietype. |                                                                           
| Omschrijving         | De omschrijving van het registratietype. |
| Land/regio      | De unieke id van het land/regio.|
| Belastingdienst       | De btw-dienst die is gekoppeld aan het registratietype.|
| Beperkt tot       | Het soort beperking die geldt voor het belastingregistratietype: geen, persoon, organisatie.|
| Opmaak              | De validatie-indeling voor het registratietype.|
| Kan worden bijgewerkt.      | Wordt gedefinieerd als het registratienummer voor het registratietype kan worden bijgewerkt nadat deze is ingevoerd.|
| Uniek              | Als het registratienummer voor het registratietype uniek definieert. |
| Primair voor land/regio | Als een partij gekoppeld aan een is of meer adressen in het bijzonder land en de registratie-ID geldig is voor alle deze adressen, moet u één adres aanwijzen als primaire bewerking voor het land. U kunt alleen een ID als primaire registreren. Als het nummer kan worden ingevoerd alleen voor primaire domeincontroller voor land adres bepaalt. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Een registratietype toewijzen aan een categorie registratie
Categorie registratie is land/regio registratie-id is goedgekeurd voor gebruik in het bijzonder land/de regio voor belastingen, douane en voor andere doeleinden. Deze categorie definieert de validatieregels van bepaalde registratie-ID (inclusief controlecijfers enz.) en de opname belastingregistratie-ID in andere rapporten. Gebruik de pagina **Organisatiebeheer**&gt;**algemeen adresboek**&gt;**registratietypen**&gt;**registratiecategorieën** registratietype van een bepaald land toewijzen aan categorie ondersteunde registratie.

| Veld            | Omschrijving|
|-----------------------|----------------|
| Registratietype     | De registratie, typ in het bijzonder land/regio.|
| Beperkt tot         | Het soort beperking geldt voor het belastingregistratietype: geen, persoon, organisatie.|
| Registratiecategorie | De unieke registratie-id is goedgekeurd voor gebruik van het land. De volledige lijst van ondersteunde in AX7.1 categorieën lager is dan. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Voer registratie-id's voor algemene-adresboekrecords
Het globale adresboek (GAB) in Microsoft Dynamics 365 for Operations bevat geconsolideerde adresgegevens voor klanten, leveranciers, contacten, zakenrelaties en rechtspersonen. Zie voor meer informatie, [overzicht globaal adresboek](/dynamics365/operations/organization-administration/overview-global-address-book). De partijregistraties die zijn opgeslagen in het globale adresboek kunnen een of meer adresrecords bevatten. Deze adressen worden gebruikt voor verschillende doeleinden, zoals facturering of levering. U kunt de registratie-id's voor adresgegevens, voor klanten, leveranciers, werknemers en rechtspersonen instellen. Zoek de (te betalen rechtspersoon, leverancier, klant, werknemer) partijregistratie waarvoor u wilt het registratie-ID invoeren en klik vervolgens op **registratie-id's** in formulieren die zijn gerelateerd aan leveranciers, te betalen rechtspersoon, leverancier, klant, werknemer te openen de **adressen beheren** pagina. Op de **btw-registratienummer** en klik op **Add**, en voert u na de informatie over de registratie-ID.

|Veld                |Omschrijving                                                |
|---------------------|-----------------------------------------------------------|
| Registratietype   | Het registratietype het geselecteerde land/regio.     |
| Registratienummer | De partij-registratie-ID.                                |
| Omschrijving         | De omschrijving van het registratienummer.               |
| Sectie             | Als u meer informatie over het registratienummer. |
| Uitgifteagentschap      | De instantie die het nummer wordt uitgegeven.        |
| Uitgiftedatum         | De uitgegeven datum voor het registratienummer.              |
| Geldig vanaf           | De effectieve datum voor het registratienummer.           |
| Vervaldatum          | De vervaldatum van het registratienummer.          |

> [!NOTE]
> De btw-nummer van de rechtspersoon, leverancier, klant kan worden geselecteerd in de registratie-id's betrekking hebben op de btw-nummer en voor de partij ingevoerd.

## <a name="search-for-records-by-registration-id"></a>Zoeken naar records door de belastingregistratie-ID
Zoeken naar partijrecords op basis van een registratie-ID is beschikbaar op de formulieren die zijn gerelateerd aan leveranciers, te betalen rechtspersoon, leverancier, klant en werknemer. Klik op **belastingregistratie-ID zoeken** opent de **zoekcriteria belastingregistratie-ID** pagina. Geef zoekcriteria op en klik op **zoeken naar**. De geselecteerde records uit het globale adresboek en de bijbehorende typen partijregistratie wordt weergegeven.

## <a name="supported-registration-categories"></a>Ondersteunde registratiecategorieën
De volgende tabel worden de ondersteunde registratietypen in Dynamics 365 voor bewerkingen. Als u vertrouwd met de velden in Microsoft Dynamics AX 2012 voor registratie-id's bent, deze tabel die velden ook toegewezen aan de Dynamics 365 voor bewerkingen registratiecategorieën.

| Dynamics 365 voor bewerkingen registratie categorie         |Land/regio  | Dynamics AX 2012 term/veld|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Btw-id                                                        | Alle landen van de europese Unie (EU)|  Btw-nummer (wettelijke type belasting-ID in AX2012 R3)|
| Ondernemings-id (COID)                                          | België Tsjechische Republiek Estland Hongarije Letland Litouwen Polen Zwitserland | Registratienummer Enterprise-nummer (EnterpriseNumber) (RegNum\_W) nummer (RegNum\_W) nummer (RegNum\_W) nummer (RegNum\_W) Enterprise code (EnterpriseCode)-registratienummer (RegNum\_W) UID (wettelijke type UID in AX2012 R3) |
| Vestigings-id                                                     | België            | Vestigingsnummer (BranchNumber)|
| Spisová značka (registratienummer, uitgevende bank, sectie) | Tsjechische Republiek     | Nummer (CommercialRegisterInsetNumber) Kept paden op commerciële registreren (CommercialRegister) gedeelte van handelsregister (CommercialRegisterSection)|
| Klant-id van de douane                                           | Finland | Klantnummer douane (CustomsCustomerNumber\_FI)|
| INN                                                           | Russische Federatie| INN (wettelijke type INN in AX2012 R3)|
| RRC                                                           | Russische Federatie| RRC (wettelijke type RRC in AX2012 R3)|
| OKDP                                                          | Russische Federatie| OKDP (wettelijke type OKDP in AX2012 R3)|
| OKPO                                                          | Russische Federatie| OKPO (wettelijke type OKPO in AX2012 R3)|
| RCOAD                                                         | Russische Federatie| RCOAD (wettelijke type RCOAD in AX2012 R3)|
| OGRN                                                          | Russische Federatie| OGRN (wettelijke type OGRN in AX2012 R3) |
| SNILS                                                         | Russische Federatie| SNILS (wettelijke type SNILS in AX2012 R3)|
| CIFTS                                                         | Russische Federatie| CIFTS (wettelijke type CIFTS in AX2012 R3)|

Zie de volgende Taakregistratie voor btw-Identificatienummer in Lifecycle Services (LCS) voor meer informatie over registratie-ID verwerken, met inbegrip van de vereiste onderdelen:

-   Btw-id instellen
-   Btw-registratie van leverancier
-    Een partij zoeken door middel van het btw-id



