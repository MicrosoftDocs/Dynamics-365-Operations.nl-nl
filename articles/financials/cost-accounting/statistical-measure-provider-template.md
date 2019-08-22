---
title: Statistische dimensieleden en sjablonen van provider van statistische maateenheden
description: In dit onderwerp vindt u informatie over statistische dimensieleden en sjablonen van provider van statistische maateenheden. Statistische dimensieleden kunnen worden gebruikt als een toewijzingsgrondslag in beleid, zoals kostenverdeling en kostentoewijzing. Ze kunnen ook worden gebruikt voor rapportage van verbruik van niet-monetaire kosten.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 15c4ca5284121e1b384111f10e2d4cb06a5c7575
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841460"
---
# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statistische dimensieleden en sjablonen van provider van statistische maateenheden

[!include [banner](../includes/banner.md)]

Een statistische dimensie en de leden ervan worden gebruikt om niet-monetaire posten in Kostprijsboekhouding te registreren en beheren. Statistische dimensieleden kunnen worden gebruikt voor twee doelen:

- Als een toewijzingsgrondslag inbeleid zoals kostenverdeling of kostentoewijzing
- Voor rapportage van niet-monetair verbruik

## <a name="statistical-dimension"></a>Statistische dimensie

Een statistische dimensie heeft een unieke naam en een set unieke dimensieleden. De statistische dimensie is toegewezen aan een grootboek-id van Kostprijsboekhouding. Deze relatie koppelt alle bijbehorende statistische dimensieleden aan het grootboek van Kostprijsboekhouding. Daarom worden alle statistische posten gemaakt in de context van het grootboek van Kostprijsboekhouding.

> [!NOTE]
> Een statistische dimensie kan zijn toegewezen aan meer dan een grootboek van Kostprijsboekhouding.

Hier volgt een voorbeeld van een statistische dimensie.

| Naam                        | Gegevensconnector voor dimensieleden |
|-----------------------------|--------------------------------------|
| Gedeelde statistische elementen | Geïmporteerde dimensieleden           |

Hier volgt een voorbeeld van een statistische dimensie die is toegewezen aan een grootboek van kostprijsboekhouding.

| Naam                  | Valuta voor boekhouding | Wisselkoerstype | Fiscale kalender | Dimensie van kostenelement | Statistische dimensie       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Managementboekhouding | EUR                 | Constante valuta  | Boekperiode   | Gedeelde kostenelementen   | Gedeelde statistische elementen |

## <a name="statistical-dimension-members"></a>Statistische dimensieleden

Een lid van de statistische dimensie vertegenwoordigt een entiteit waarvoor u niet-monetaire metingen wilt registreren. Deze metingen kunnen worden gebruikt als de toewijzingsgrondslag of alleen om niet-monetaire waarden te rapporteren.

Statistische dimensieleden kunnen handmatig worden gemaakt. U kunt ze ook importeren uit een bestand met behulp van het Hulpprogramma voor importeren/exporteren van gegevensbeheer.

Een statistische dimensielid wordt automatisch een vooraf gedefinieerde toewijzingsgrondslag. Deze kan worden gebruikt als een toewijzingsgrondslag in beleid of als invoer voor andere soorten toewijzingsgrondslagen.

Hier volgen enkele voorbeelden van gangbare statistische dimensieleden.

| Statistische dimensienaam  | Statistische elementen | Omschrijving             | Eenheid |
|-----------------------------|----------------------|-------------------------|------|
| Gedeelde statistische elementen | FTE                  | Voltijdse werknemers     | St.  |
| Gedeelde statistische elementen | Elektriciteit          | Elektriciteitsverbruik | kWh  |
| Gedeelde statistische elementen | Pack CC              | Kostenplaats verpakking   | Hrs. |

## <a name="statistical-measure-provider-template"></a>Sjabloon van provider van statistische maateenheden

Statistische maateenheden kunnen afkomstig zijn van allerlei bronnen. Microsoft Dynamics 365 for Finance and Operations is een uitstekende bron om statistische metingen uit te halen. U kunt met een sjabloon van een statistische maateenheidprovider makkelijk de statistische maateenheden configureren die u wilt extraheren.

De definitie van een sjabloon van de provider van statistische maateenheden is algemeen en kan in meerdere statistische dimensieleden worden gebruikt.

> [!NOTE]
> Alle tabellen die financiële dimensies bevatten, kunnen worden gebruikt als bronnen voor statistische maateenheden.

**Voorbeeld: Aantal werknemers per kostenplaats**

Het aantal werknemers per kostenplaats is een statistische maateenheid die kan worden gebruikt voor verschillende doeleinden die leidinggevende inzicht bieden:

- Een statistische rapportagemaateenheid op kostenplaats
- Een toewijzingsgrondslag voor verschillende soorten onkosten
- Interne kostentarieven op kostenplaats:

    - Kosten per werknemer
    - Opbrengst per werknemer

De tabel HcmEmployment bevat een lijst met alle werknemers in het exemplaar. Deze tabel is een algemene tabel. Daarom zijn de records niet gerelateerd aan een specifieke gegevensgebied-id.

Hier volgt een voorbeeld van de werknemers in de tabel HcmEmployment.

| Naam       | Kostenplaats | Omschrijving   | Type medewerker |
|------------|-------------|----|-------------|
| Werknemer 1 | CC001       | HR | Werknemer    |
| Werknemer 2 | CC002       | FI | Werknemer    |
| Werknemer 3 | CC002       | FI | Werknemer    |
| Werknemer 4 | CC003       | VOB | Werknemer    |
| Werknemer 5 | CC003       | VOB | Werknemer    |
| Werknemer 6 | CC002       | FI | Contractant  |

Wanneer u een record van een **Sjabloon van provider van statistische maateenheden** maakt, moet u eerst bepalen welke functie u wilt gebruiken:

- **Count**: het aantal records per kostenplaats wordt overgebracht.
- **Sum**: een som voor de records per kostenplaats wordt overgebracht. (De velden **Sum** en **Date** zijn vereist.)

## <a name="using-the-count-function"></a>Gebruik van de functie Count

U kunt bijvoorbeeld een sjabloon van provider van statistische maateenheden als volgt instellen.

| Naam  | Functie | Brontabel  | Somveld      | Datumveld     |
|-------|----------|---------------|----------------|----------------|
| VTE's  | Aantal    | HcmEmployment | Niet van toepassing | Niet van toepassing |

U kunt ook een of meer bereiken toevoegen, als u de maateenheden van de brontabel wilt beperken.

In dit voorbeeld kunt u, als u alleen een telling van alle fulltime werknemers (VTE's) wilt, een bereik toevoegen in het veld **Werknemertype**. Selecteer in het veld **Criteria** de waarde **Werknemer** om het uitvoerbereik als volgt te beperken.

**Bereiken**

| Brontabel  | Veld       | Criteria |
|---------------|-------------|----------|
| HcmEmployment | Type medewerker | Werknemer |

Voordat u statistische maateenheden naar kostprijsboekhouding sturen kunt, moet u de relatie tussen de sjabloon van de statistische maateenheidprovider en het statistische dimensielid instellen. Deze relatie wordt gemaakt per grootboek van kostprijsboekhouding en versie. De relatie bestaat uit een gegevensconnector en een gegevensprovider. U kunt diverse gegevensconnectors en gegevensproviders per statistische dimensielid hebben.

> [!NOTE]
> In dit voorbeeld maken we alleen een relatie voor de **Actuele versie**.

Ga naar **Grootboek van kostprijsboekhouding** \> **Actuele versie** \> **Beheren** \> **Statistische maateenheden** om de relatie tot stand te brengen. Voor dit scenario selecteert u de gegevensconnector **Dynamics 365 for Finance and Operations – Statistische maateenheden**, omdat we gegevens willen ophalen uit Finance and Operations.

**Gegevensbron**

| Naam        | Gegevensconnector                                                                     | Statistisch dimensielid |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| VTE's D365FO | Dynamics 365 for Finance and Operations – Statistische maateenheden | VTE's                         |

**Configuratie van gegevensprovider**

| Naam van statistische sjabloon |
|---------------------------|
| VTE's                      |

Nadat de brongegevens voor de statistische maateenheden zijn verwerkt, worden de volgende statistische posten gemaakt in Kostprijsboekhouding.

**Journaal**

| Journaal | Type journaal                       | Fiscale kalenderperiode | Jaar   |  Periode  |  Versie | Bronposten gegevensconnector|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Overboekingsjournaal van statistische boekingen | Fiscaal                 | 2017   | Periode 1 | CA-grootboek USMF | VTE's                   |

**Overboekingsjournaalboekingen van statistische posten**

| Grootboekdatum | Magnitude | Statistisch element |   Omschrijving       | Kostenplaats |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1,00      | VTE's                | Voltijdse werknemers | CC001       |
| 31-01-2017      | 2.00      | VTE's                | Voltijdse werknemers | CC002       |
| 31-01-2017      | 2.00      | VTE's                | Voltijdse werknemers | CC003       |

**Statistische posten**

| Kostenobject |    | Grootboekdatum | Statistisch dimensielid |  Omschrijving        | Magnitude |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR | 31-01-2017      | VTE's                         | Voltijdse werknemers | 1,00      |
| CC002       | FI | 31-01-2017      | VTE's                         | Voltijdse werknemers | 2.00      |
| CC003       | VOB | 31-01-2017      | VTE's                         | Voltijdse werknemers | 2.00      |

Als de toewijzingsbasis voor het voorgedefinieerde dimensielid VTE's wordt toegewezen als een toewijzingsgrondslag in een distributieregel, worden de kosten verdeeld met behulp van de volgende toewijzingsfactor.

| Kostenobject | Omschrijving    | Magnitude | Toewijzingsfactor |
|-------------|----|-----------|-------------------|
| CC001       | HR | 1,00      | (1/5) × bedrag    |
| CC002       | FI | 2.00      | (2/5) × bedrag    |
| CC003       | VOB | 2.00      | (2/5) × bedrag    |

## <a name="using-the-sum-function"></a>Gebruik van de functie Sum

Een productiekostenplaats, CC010 (verpakking), is verantwoordelijk voor het verpakken van de producten voordat ze worden verzonden naar klanten. De directe arbeidskosten worden toegevoegd aan de producten via de stuklijst en route. De indirecte kosten van het uitvoeren van de kostenplaats moet ook worden toegewezen aan de geproduceerde producten. Meestal is de beste statistische maateenheid voor een dergelijke toerekening het aantal geregistreerde productie-uren per product binnen de opgegeven periode.

De tabel ProdRouteTrans bevat alle productiearbeidtransacties per rechtspersoon DataAreadID.

Hier volgt een voorbeeld van de tabel ProdRouteTrans.

| Verwijzing        | Nummer | Bewerking | Type | Tijd  | Fysieke datum | Productgroep (financiële dimensie) | Rechtspersoon |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Productieorder | P0001  | Verpakking | Tijd | 8,00  | 01-01-2017    | Sinaasappelsap B2B                    | USMF         |
| Productieorder | P0001  | Verpakking | Tijd | 8,00  | 02-01-2017    | Sinaasappelsap B2B                    | USMF         |
| Productieorder | P0002  | Verpakking | Tijd | 4,00  | 03-01-2017    | Sinaasappelsap consument               | USMF         |
| Productieorder | P0003  | Verpakking | Tijd | 4,00  | 03-01-2017    | Sinaasappelsap consument               | USMF         |
| Productieorder | P0004  | Reconst.  | Tijd | 10,00 | 03-01-2017    | Sinaasappelsap consument               | USMF         |

Wanneer u een record van een **Sjabloon van provider van statistische maateenheden** maakt, moet u eerst bepalen welke functie u wilt gebruiken:

- **Count**: het aantal records per kostenplaats wordt overgebracht.
- **Sum**: een som voor de records per kostenplaats wordt overgebracht. (De velden **Sum** en **Date** zijn vereist.)

De sjabloon van provider van statistische maateenheden kunt u als volgt instellen.

| Naam    | Functie | Brontabel   | Somveld | Datumveld    |
|---------|----------|----------------|-----------|---------------|
| Pack CC | Totaal      | ProdRouteTrans | Uren     | Fysieke datum |

U kunt ook een bereiken toevoegen, als u de maateenheden van de brontabel wilt beperken.

Als u in dit voorbeeld alleen de som wilt van de uren die zijn gerelateerd aan de kostenplaats CC010 Verpakking, kunt u een bereik toevoegen in het veld **Bewerking**. Selecteer in het veld **Criteria** de waarde **Verpakking** om het uitvoerbereik te beperken.

**Bereiken**

| Brontabel   | Veld     | Criteria  |
|----------------|-----------|-----------|
| ProdRouteTrans | Bewerking | Verpakking |

Voordat u statistische maateenheden naar kostprijsboekhouding sturen kunt, moet u de relatie tussen de sjabloon van de statistische maateenheidprovider en het statistische dimensielid instellen. Deze relatie wordt gemaakt per grootboek van kostprijsboekhouding en versie. De relatie bestaat uit een gegevensconnector en een gegevensprovider. U kunt diverse gegevensconnectors en gegevensproviders per statistische dimensielid hebben.

> [!NOTE]
> In dit voorbeeld maken we alleen een relatie voor de **Actuele versie**.

Ga naar **Grootboek van kostprijsboekhouding** \> **Actuele versie** \> **Beheren** \> **Statistische maateenheden** om de relatie tot stand te brengen. Voor dit scenario selecteert u de gegevensconnector **Dynamics 365 for Finance and Operations – Statistische maateenheden**, omdat we gegevens willen ophalen uit Finance and Operations.

**Gegevensbron**

| Naam           | Gegevensconnector                                                                     | Statistisch dimensielid |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pack CC D365FO | Dynamics 365 for Finance and Operations – Statistische maateenheden | Pack CC                      |

Het systeem dat ProdRouteTrans een tabel is waarin elke record tot een afzonderlijke rechtspersoon behoort. Daarom wordt u gevraagd om de rechtspersoon te selecteren waarvan u transacties wilt importeren.

**Configuratie van gegevensprovider**

| Naam van statistische sjabloon | Rechtspersoon |
|---------------------------|--------------|
| Pack CC                   | USMF         |

Nadat de brongegevens voor de statistische maateenheden zijn verwerkt, worden de volgende statistische posten gemaakt in Kostprijsboekhouding.

**Journaal**

| Journaal | Type journaal                     | Fiscale kalenderperiode | Jaar   | Periode | Versie   |   Bronposten gegevensconnector  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Overboekingsjournaal van statistische boekingen | Fiscaal               | 2017    | Periode 1  | CA-grootboek USMF | Pack CC |

**Overboekingsjournaalboekingen van statistische posten**

| Grootboekdatum | Magnitude | Statistisch element |  Omschrijving          | Productgroep         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16,00     | Pack CC             | Kostenplaats verpakking | Sinaasappelsap B2B      |
| 31-01-2017      | 8,00      | Pack CC             | Kostenplaats verpakking | Sinaasappelsap consument |

**Statistische posten**

| Kostenobject           | Grootboekdatum | Statistisch dimensielid |    Omschrijving        | Magnitude |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Sinaasappelsap B2B      | 31-01-2017      | Pack CC                      | Kostenplaats verpakking | 16,00     |
| Sinaasappelsap consument | 31-01-2017      | Pack CC                      | Kostenplaats verpakking | 8,00      |

Als de toewijzingsbasis voor het voorgedefinieerde dimensielid Pack CC wordt toegewezen als een toewijzingsgrondslag in een distributieregel, worden de kosten verdeeld met behulp van de volgende toewijzingsfactor.

| Kostenobject           | Magnitude | Toewijzingsfactor  |
|-----------------------|-----------|--------------------|
| Sinaasappelsap B2B      | 16,00     | (16 ÷ 24) × bedrag |
| Sinaasappelsap consument | 8,00      | (8 ÷ 24) × bedrag  |

## <a name="imported-statistical-measures"></a>Geïmporteerde statistische maateenheden

U kunt statistische maateenheden in Kostprijsboekhouding importeren met behulp van het Hulpprogramma voor importeren/exporteren van gegevensbeheer.

De gegevensentiteit die wordt gebruikt voor het importeren wordt Geïmporteerde statistische maateenheden genoemd.

> [!NOTE]
> Deze gegevensentiteit is opgezet om maximaal vijf unieke dimensiewaarden per post toe te staan.

Het stroomverbruik wordt vastgelegd in Microsoft Excel met behulp van de vooraf gedefinieerde indeling van de gegevensentiteit. Hier volgt een voorbeeld.

| Grootboekdatum | Naam van dimensielid 1 | Naam van dimensielid 2 | Naam van dimensielid 5 | Magnitude  | Bron-id |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2,450.00   | Elektriciteit       |
| 31-01-2017      | CC002                  |                        |                        | 4,100.00   | Elektriciteit       |
| 31-01-2017      | CC003                  |                        |                        | 15.000,00  | Elektriciteit       |

Wanneer u uw gegevens hebt geïmporeerd via Gegevensbeheer, worden de gegevens opgeslagen in een faseringstabel van Kostprijsboekhouding. Daarom kunnen de geïmporteerde gegevens worden gebruikt in meerdere grootboeken van Kostprijsboekhouding. U hoeft de gegevens niet opnieuw te laden.

Om de gegevens te importeren gaat u naar **Geïmporteerde gegevens** \> **Gegevensentiteit** \> **Geïmporteerde statistische maateenheden**.

| Bron-id | Grootboekdatum | Magnitude  | Naam van dimensielid 1 | Naam van dimensielid 2 | Naam van dimensielid 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektriciteit       | 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| Elektriciteit       | 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| Elektriciteit       | 31-01-2017      | 15.000,00  | CC003                  |                        |                        |

Voordat u statistische maateenheden naar kostprijsboekhouding sturen kunt, moet u de relatie tussen de bron-id en het statistische dimensielid instellen. Deze relatie wordt gemaakt per grootboek van kostprijsboekhouding en versie. De relatie bestaat uit een gegevensconnector en een gegevensprovider. U kunt diverse gegevensconnectors en gegevensproviders per statistische dimensielid hebben.

> [!NOTE]
> In dit voorbeeld maken we alleen een relatie voor de **Actuele versie**.

Ga naar **Grootboek van kostprijsboekhouding** \> **Actuele versie** \> **Beheren** \> **Statistische maateenheden** om de relatie tot stand te brengen. Voor dit scenario selecteert u de gegevensconnector **Geïmporteerde statistische maateenheden**, omdat gegevens via Excel zijn geïmporteerd uit een extern systeem naar Kostenprijsboekhouding.

**Gegevensbron**

| Naam        | Gegevensconnector                | Statistisch dimensielid |
|-------------|-------------------------------|------------------------------|
| Elektriciteit | Geïmporteerde statistische maateenheden | Elektriciteit                  |

**Configuratie van gegevensprovider**

| Importbron-id | Functie | Dimensie 1   | Dimensie 2 | Dimensie 5 |
|--------------------------|----------|--------------|------------|------------|
| Elektriciteit              | Totaal      | Kostenplaatsen |            |            |

> [!NOTE]
> Wanneer u de configuratie van de gegevensprovider definieert, moet u aangeven welke kostenobjectdimensies u wilt laten vergelijken met de geïmporteerde transacties. Nadat de brongegevens voor de statistische maateenheden zijn verwerkt, worden de volgende statistische posten gemaakt in Kostprijsboekhouding.

**Journaal**

| Journaal | Type journaal                       | Fiscale kalenderperiode | Jaar  | Periode  |Versie      |Bronposten gegevensconnector |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Overboekingsjournaal van statistische boekingen | Fiscaal                 | 2017  | Periode 1 | CA-grootboek USMF | Elektriciteit |

**Overboekingsjournaalboekingen van statistische posten**

| Grootboekdatum | Magnitude  | Kostenelement |   Omschrijving           | Kostenplaats |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2,450.00   | Elektriciteit  | Elektriciteitsverbruik | CC001       |
| 31-01-2017      | 4,100.00   | Elektriciteit  | Elektriciteitsverbruik | CC002       |
| 31-01-2017      | 15.000,00  | Elektriciteit  | Elektriciteitsverbruik | CC003       |

**Statistische posten**

| Kostenobject |    | Grootboekdatum | Statistisch dimensielid |      Omschrijving                   | Magnitude  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | HR | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 2,450.00   |
| CC002       | FI | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 4,100.00   |
| CC003       | VOB | 31-01-2017      | Elektriciteit                  | Elektriciteitsverbruik | 15.000,00  |

Als de toewijzingsbasis voor het voorgedefinieerde dimensielid Elektriciteit wordt toegewezen als een toewijzingsgrondslag in een distributieregel, worden de kosten verdeeld met behulp van de volgende toewijzingsfactor.

| Kostenobject |    | Magnitude | Toewijzingsfactor          |
|-------------|----|-----------|----------------------------|
| CC001       | HR | 2,450.00  | (2.450 ÷ 21.550) × bedrag  |
| CC002       | FI | 4,100.00  | (4.100 ÷ 21.550) × bedrag  |
| CC003       | VOB | 15.000,00 | (15.000 ÷ 21.550) × bedrag |

## <a name="additional-resources"></a>Aanvullende resources

[Toewijzingsgrondslagen](allocation-bases.md)
