---
title: Zoeken in voorraad op het verkooppunt (POS)
description: In dit onderwerp worden de opties beschreven die beschikbaar zijn voor het weergeven van voorraadgegevens in het verkooppunt (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: e40c558e03ef230fee6726994bc94979d40493c2
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Zoeken in voorraad op het verkooppunt (POS)

[!include [banner](includes/banner.md)]

Met Zoeken in voorraad in het verkooppunt kunnen detailhandelaren operationele successen behalen in real-time en inzicht krijgen door verbinding te maken tussen winkels, het POS en de backoffice. Deze functionaliteit biedt een nauwkeurige realtime weergave van de productvoorraad in winkels en distributiecentra. Het helpt detailhandelaren ook om de efficiëntie te vergroten en kosten te besparen door de voorraadplanning in realtime te verbeteren.

Een nauwkeurige realtime weergave van de voorraad binnen een organisatie helpt het winkelpersoneel om op tijd een uitstekende klantenservice te bieden. Het moment dat er het meest toe doet, is het tijdstip waarop de klant is gereed om een aankoopbeslissing te nemen. Het is belangrijk dat kassiers in de winkel realtime voorraadinformatie bij de hand hebben zodat ze correct een levering van producten kunnen beloven.

U kunt de pagina **Zoeken in voorraad** open vanuit het werkgebied **Retail Modern POS** of **Retail Cloud POS**.

![Tegel Zoeken in voorraad op POS-startpagina](media/POSHomepage.png)

Op de pagina **Zoeken in voorraad** kunt u met het numerieke toetsenbord een productnummer invoeren. U ziet vervolgens de hoeveelheid voorhanden voorrad voor meerdere winkels en magazijnen.

![Standaardzoekpagina voor voorraad](media/InventoryLookUp.png)

**Gereserveerde** en **bestelde** aantallen worden ook weergegeven voor elke locatie.

- **Gereserveerd**: deze hoeveelheid verwijst naar de waarde **Fysiek gereserveerd** uit de backoffice voor het opgegeven productnummer op de locatie.
- **Besteld**: deze hoeveelheid verwijst naar de waarde **Totaal van order** uit de backoffice voor het opgegeven productnummer op de locatie.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Locaties waarvoor beschikbaarheidsgegevens voor voorraad worden weergegeven

De lijst met locaties bevat twee typen entiteiten:

- **Detailhandelwinkels**: in de lijst staan de winkels die zijn geconfigureerd met behulp van de winkellocatorgroep voor de huidige winkel in Detailhandel Hoofdkantoor. 
- **Distributiecentra**: verschillende soorten distributiecentra (bijvoorbeeld magazijnen) kunnen worden geconfigureerd in Microsoft Dynamics 365 for Retail. In de lijst staat echter alleen de voorraadbeschikbaarheid voor distributiecentra van het type **Standaard**. 

    > [!NOTE]
    > Informatie over de vooraadbeschikbaarheid wordt niet weergegeven voor magazijnen van het type **transit**, **quarantaine** en **goederen onderwep** voor het POS.

Op de pagina **Zoeken in voorraad** kunt u de ATP-hoeveelheden (available to promise) zien voor elke winkel, naast de huidige voorhanden hoeveelheden, gereserveerde hoeveelheden en bestelde hoeveelheden. Selecteer de winkel waarvoor u de ATP-informatie wilt weergeven en selecteer vervolgens **Beschikbaarheid van de winkel weergeven**.

![ATP-hoeveelheden](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>De op dimensies gebaseerde matrixweergave openen om alle varianten te zien

Op de pagina **Productdetails** van een productmodel of op de pagina **Zoeken in voorraad** selecteert u **Alle varianten weergeven** in de app-balk onder aan de pagina. Als deze pagina's de eerste keer worden geopend, toont de weergave **Op dimensies gebaseerde matrix** de gegevens van de voorraadbeschikbaarheid voor alle varianten van een product voor de huidige winkel.

> [!NOTE]
> De knop **Alle varianten weergeven** is alleen beschikbaar voor productmodellen met productvarianten. De knop is niet beschikbaar voor zelfstandige producten of kits.

![De knop Alle varianten weergeven op de pagina Zoeken in voorraad](media/StandardToMatrix.png)

Selecteer **Alle varianten weergeven** op de pagina **Productgegevens** van een productmodel of op de paigna **Zoeken in voorraad**, zonder een locatie te selecteren, om naar de weergave **Op dimensie gebaseerde matrix** te gaan en de voorraadbeschikbaarheidsgegevens voor alle varianten van een product voor de huidige winkel te tonen.

![Op dimensie gebaseerde matrix weergeven voor de pagina Zoeken in voorraad](media/Matrix.png)

> [!NOTE]
> In het voorgaande voorbeeld is de weergavevolgorde van de dimensies alfabetisch, omdat de volgorde van de dimensies niet is geconfigureerd voor het geselecteerde product.

In de weergave **Op dimensie gebaseerde matrix** omvatten de cellen voor de productvarianten een waarde voor voorhanden voorraad in de rechterbenedenhoek. De volgende tabel beschrijft de betekenis van de verschillende waarden.

| Waarde voorhanden voorraad                            | Omschrijving |
|------------------------------------------|-------------|
| Numerieke waarde die groter is dan 0 (nul) | Een variant is vrijgegeven voor de geselecteerde locatie en u kunt aanvullende acties uitvoeren in de cel. (Deze acties worden verderop in dit onderwerp nader beschreven.) |
| **0** (nul)                             | Een variant is vrijgegeven voor de geselecteerde locatie, maar het artikel is niet beschikbaar op de geselecteerde locatie. U kunt echter wel aanvullende acties uitvoeren in de cel. (Deze acties worden verderop in dit onderwerp nader beschreven.) |
| **n.v.t.** of een niet-actieve cel              | Een variant is niet vrijgegeven voor de geselecteerde locatie en u kunt geen aanvullende acties uitvoeren in de cel. |

U kunt ook de draaitabel voor dimensies wijzigen door het selecteren van de nieuwe dimensie die moet worden gebruikt. 

![De draaitabel wijzigen](media/ChangePivot.png)

![Draaitabel gewijzigd](media/PivotChanged.png)

> [!NOTE]
> In de voorgaande afbeeldingen is de weergavevolgorde van de dimensies voor het geselecteerde product aangepast (niet-alfabetisch). Het is gebaseerd op de weergavevolgorde van de dimensie die is ingesteld in de backoffice.

Verder kunnen in de weergave **Op dimensie gebaseerde matrix** meer acties worden uitgevoerd om de productiviteit van het winkelpersoneel te vergroten. Hieronder vindt u enkele voorbeelden:

- Wijzig de winkellocatie om de voorraadbeschikbaarheid van alle productvarianten op andere locaties op te zoeken. Deze locaties omvatten andere winkels in de winkellocatorgroep en distributiecentra van het type **Standaard**.
- Verkoop een afzonderlijke productvariant aan een klant met behulp van cash-and-carry, ophalen in de winkel of verzenden naar een adres.
- Geef de klant de ATP-informatie voor een afzonderlijke productvariant op een bepaalde locatie.

![Aanvullende acties op verschillende tegels](media/VariantActions.png)

> [!NOTE]
> In het voorgaande voorbeeld is de weergavevolgorde van de dimensies alfabetisch, omdat de volgorde van de dimensies niet is geconfigureerd voor het geselecteerde product.

De volgende tabel bevat meer informatie over de aanvullende acties die beschikbaar zijn.


|        Actie        |                                                                                                                    Omschrijving                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       Nu verkopen       |                               Voeg de geselecteerde artikelvariant toe aan de transactie en stuur de gebruiker door naar het transactiescherm. (Deze actie is niet beschikbaar wanneer de geselecteerde locatie een distributiecentrum is.)                               |
|   Ophalen in winkel   |      Maak een klantorder voor de productvariant die wordt opgehaald bij de geselecteerde locatie en stuur de gebruiker door naar het transactiescherm. (Deze actie is niet beschikbaar wanneer de geselecteerde locatie een distributiecentrum is.)       |
|     Product verzenden     |                                                 Maak een klantorder voor de productvariant die wordt verzonden naar de geselecteerde locatie en stuur de gebruiker door naar het transactiescherm.                                                 |
|     Beschikbaarheid     |                                                                             Geef de ATP-informatie voor de geselecteerde combinatie van varianten voor de geselecteerde locatie weer.                                                                              |
|  Alle locaties weergeven  | Schakel over naar de standaardzoekweergave voor voorraad en markeer de voorraadbeschikbaarheidsgegevens voor de artikelvariant voor alle winkels in de winkellocatorgroep, en ook in distributiecentra van de het type <strong>Standaard</strong>. |
| Productgegevens weergeven |                                                                         Stuur de gebruiker door naar de pagina <strong>Productdetails</strong> van het gekoppelde productmodel.                                                                          |


