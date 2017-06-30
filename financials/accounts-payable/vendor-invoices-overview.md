---
title: Overzicht van leveranciersfacturen
description: Dit artikel geeft algemene informatie over het leveranciersfacturen. Leveranciersfacturen zijn betalingsverzoeken voor producten en services die zijn ontvangen. Leveranciersfacturen kunnen een rekening voor lopende services voorstellen of kunnen zijn gebaseerd op inkooporders voor specifieke artikelen en services.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 16ff8ebb0e620f45c4d290ee5076d5505abf3436
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-invoices-overview"></a>Overzicht van leveranciersfacturen

[!include[banner](../includes/banner.md)]


Dit artikel geeft algemene informatie over het leveranciersfacturen. Leveranciersfacturen zijn betalingsverzoeken voor producten en services die zijn ontvangen. Leveranciersfacturen kunnen een rekening voor lopende services voorstellen of kunnen zijn gebaseerd op inkooporders voor specifieke artikelen en services. 

<a name="vendor-invoices"></a>Leveranciersfacturen
---------------

Een leveranciersfactuur op basis van een inkooporder is een factuur die wordt gegenereerd wanneer producten of services worden ontvangen op basis van een inkooporder die bij een leverancier is geplaatst. De leveranciersfactuur bevat een koptekst en één of meer regels voor artikelen of services. Een leveranciersfactuur voltooit de cyclus die loopt van inkooporder via productontvangstbon tot leveranciersfactuur. 

Hoewel sommige leveranciersfacturen aan een inkooporder zijn gekoppeld, kunnen leveranciersfacturen ook regels bevatten die niet overeenkomen met inkooporderregels. U kunt ook leveranciersfacturen maken die niet aan inkooporders zijn gekoppeld. Deze leveranciersfacturen kunnen voor lopende services staan, zoals een rekening van een energiebedrijf, en u hoeft niet naar een inkooporder te verwijzen wanneer u deze toevoegt. 

Er zijn verschillende manieren om een leveranciersfactuur op te geven:

-   Via het leveranciersfactuurregister kunt u snel facturen invoeren die niet naar een inkooporder verwijzen, zodat u de onkosten kunt samenvoegen. Door het goedkeuringsjournaal voor leveranciersfacturen te gebruiken, kunt u deze facturen selecteren en naar het leveranciersaldo boeken om de transitorische bedragen terug te boeken.
-   Met het leveranciersfactuurjournaal kunt u in één stap snel facturen invoeren die niet naar een inkooporder verwijzen.
-   In combinatie met de pool van leveranciersfacturen kunt u met het leveranciersfactuurregister snel facturen invoeren om onkosten samen te voegen. U kunt de bijbehorende inkooporders later openen om de factuur voor de onkostenrekening te boeken.
-   Op de pagina's **Openstaande leveranciersfacturen** en **Leveranciersfacturen in behandeling** kunt u leveranciersfacturen maken van bevestigde inkooporders.

De volgende discussie biedt meer informatie over het gebruik van de pagina **Openstaande leveranciersfacturen** of **Leveranciersfacturen in behandeling** om een leveranciersfactuur van een inkooporder te maken.

## <a name="understanding-invoice-line-quantities"></a>Factuurregelhoeveelheden begrijpen
Wanneer u een leveranciersfactuur opent vanuit een gerelateerde inkooporder, worden factuurregels gemaakt op basis van de inkooporder. Standaard komen de hoeveelheden overeen met de hoeveelheid van de productontvangstbon. U kunt echter de volgende standaardgedragingen gebruiken:

-   **Hoeveelheid nu ontvangen** - Gebruik deze optie voor gedeeltelijke zendingen. De standaardwaarde in het veld **Hoeveelheid** wordt overgenomen uit het veld **Nu ontvangen** in de inkooporder.
-   **Bestelde hoeveelheid** - Gebruik deze optie voor volledige zendingen. De standaardwaarde in het veld **Hoeveelheid** wordt overgenomen uit het hoeveelheidsveld **Besteld** in de inkooporder.
-   **Geregistreerde hoeveelheid** - Gebruik deze optie als het artikel moet worden geregistreerd, zoals opgegeven op de pagina **Artikelmodelgroepen**. De standaardwaarde in het veld **Hoeveelheid** is de fysieke updatehoeveelheid die is geregistreerd.
-   **Hoeveelheid productontvangstbon** – Gebruik deze optie als al een productontvangstbon voor de order is ontvangen. De standaardwaarde in het veld **Hoeveelheid** wordt afgeleid van de totale hoeveelheid aan beschikbare productontvangstbonnen.
-   **Geregistreerde hoeveelheid en services** – Gebruik deze optie als hoeveelheden in aankomstjournalen zijn geregistreerd voor artikelen in voorraad of artikelen die niet in voorraad zijn opgeslagen. Deze optie omvat ook al dan niet geregistreerde services.

Als uw rechtspersoon factuurvereffening gebruikt, kunt u de resultaten van de hoeveelheidsvereffening in de kolom **Overeenkomst van hoeveelheid van productontvangstbon** bekijken. U kunt ook de menuopdracht **Overeenkomende gegevens** op het tabblad **Aanpassen** gebruiken om de resultaten van de hoeveelheidsvereffening te bekijken.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Een regel toevoegen die niet bestaat in de inkooporder
U kunt aan de leveranciersfactuur een nieuwe regel toevoegen die niet in de inkooporder is opgenomen. U moet een artikelnummer of een aanschaffingscategorie selecteren. Vervolgens kunt u hoeveelheden, prijzen en bedragen aan de regel toevoegen. De regel wordt alleen in overeenstemmingsbeleid voor factuurtotalen opgenomen.

## <a name="submitting-a-vendor-invoice-for-review"></a>Een leveranciersfactuur ter beoordeling indienen
Uw organisatie gebruikt mogelijke workflows om het controleproces voor leveranciersfacturen te beheren. Workflowcontrole kan vereist zijn voor de factuurkoptekst, de factuurregel of voor beide. De besturingselementen voor de workflow zijn van toepassing op de koptekst of op de regel, afhankelijk van waar de focus zich bevindt als u op het besturingselement klikt. In plaats van de knop **Boeken** wordt een knop **Verzenden** weergegeven, die u kunt gebruiken om de leveranciersfactuur door het controleproces te verzenden.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Leveranciersfacturen vereffenen met productontvangstbonnen
U kunt gegevens voor leveranciersfacturen invoeren en opslaan en u kunt factuurregels vergelijken met productontvangstbonregels. U kunt ook gedeeltelijke hoeveelheden voor een regel vergelijken. 

U kunt een leveranciersfactuur maken op basis van de artikelen op de productontvangstbonregel die tot nu toe zijn ontvangen, zelfs als nog niet alle artikelen voor een bepaalde inkooporder zijn ontvangen. U kunt dit bijvoorbeeld doen als een leverancier één factuur per maand stuurt die alle leveringen dekt die de leverancier in die maand verzendt. Elke productontvangstbon staat voor een gedeeltelijke of volledige levering van de artikelen op de inkooporder. 

Wanneer u de factuur boekt, wordt de hoeveelheid bij **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de ontvangen hoeveelheden van de geselecteerde productontvangstbonnen. Als de hoeveelheid voor **Resterend gedeelte van factuur** en de hoeveelheid voor **Nog te leveren** voor alle artikelen op de inkooporder 0 (nul) zijn, wordt de status van de inkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid voor **Resterend gedeelte van factuur** niet gelijk is aan 0 (nul), blijft de status van de inkooporder ongewijzigd en kunnen hiervoor extra facturen worden ingevoerd.

Bij deze optie wordt ervan uitgegaan dat er minimaal één productontvangstbon is geboekt voor de inkooporder. De leveranciersfactuur is gebaseerd op deze productontvangstbonnen en hieruit worden de hoeveelheden overgenomen. De financiële gegevens voor de factuur zijn gebaseerd op de gegevens die worden ingevoerd wanneer u de factuur boekt.

## <a name="working-with-multiple-invoices"></a>Werken met meerdere facturen

U kunt met meerdere facturen tegelijkertijd werken en ze allemaal op hetzelfde moment boeken. Als u meerdere facturen moet maken, gebruikt u de pagina **Leveranciersfacturen in behandeling**. Als u meerdere leveranciersfacturen moet boeken en afdrukken, gebruikt u de pagina Factuurgoedkeuringsjournaal Als u het factuurgoedkeuringsjournaal gebruikt, moet er minimaal één productontvangstbon worden geboekt voor de inkooporder en moet er een factuur voor de inkooporder worden geboekt in een facturenregister. De financiële gegevens voor de factuur komen uit de factuur die is geboekt in het register.





