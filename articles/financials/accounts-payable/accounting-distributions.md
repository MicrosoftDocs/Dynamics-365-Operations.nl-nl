---
title: Boekhoudingsverdelingen
description: Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor de verwerking hiervan. Boekhoudingsverdelingen worden gebruikt om monetaire bedragen voor een brondocument toe te wijzen aan bepaalde grootboekrekeningen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f7d98d7ab9b375bfeb8784596753ca956f96e36
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837537"
---
# <a name="accounting-distributions"></a>Boekhoudingsverdelingen

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor de verwerking hiervan. Boekhoudingsverdelingen worden gebruikt om monetaire bedragen voor een brondocument toe te wijzen aan bepaalde grootboekrekeningen. 

Boekhoudingsverdelingen vormen een functie die in het hele programma kan worden gebruikt en die kan worden uitgebreid door elk brondocument, zoals een inkooporder, een leveranciersfactuur, een onkostennota en een vrije-tekstfactuur. Standaard wordt een standaardboekhoudingsverdeling gegenereerd voor elke brondocumentregel en monetair bedrag en wordt voorwaardelijk ingeschakeld voor wijziging. 

> [!Note] 
> Bepaalde documenten ondersteunen ook de monetaire bedragen van het koptekstdocument, zoals toeslagen voor orders en facturen. 

De algemene boekhoudingsverdelingsmogelijkheden bevatten de volgende opties om boekhoudingsverdelingen te verwerken:

-   **Bedragen verdelen**: de boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke documentkoptekst of -regel en alle onderliggende regels, zoals belastingen of toeslagen.
    -   Voor de verdelingen van de hoogste monetaire bedragen (bovenliggende verdelingen) kunnen de hoofdrekening en financiële dimensies rechtstreeks in het gesegmenteerde invoerbesturingselement in het raster worden bewerkt. De totaalprijs is een typisch voorbeeld van een dergelijke bovenliggende verdeling.
    -   De verdelingsbedragen worden gebaseerd op de termijnvaluta voor het document. Meestal is deze valuta de transactievaluta. Boekhoudings- en rapportagevalutabedragen worden gegenereerd als onderdeel van subadministratieboekhouding.
    -   Met de verdelingen worden de boekhoudingsdatum en de boekhoudgebeurtenis weergegeven. Doorgaans wordt de boekhoudgebeurtenis ingesteld op **Geen** totdat het document wordt gejournaliseerd/geboekt. Op dat punt wordt de boekhoudgebeurtenis **Oorspronkelijk**. Nadat de verdelingen zijn geboekt, kunt u de verdelingen niet wijzigen.
    -   De knop **Splitsen** kan voor bovenliggende verdelingen worden ingeschakeld. Met **Splitsen** worden nieuwe boekhoudingsverdelingen gegenereerd en de splitsing kan worden gebaseerd op percentage, bedrag of hoeveelheid.
    -   De knop **Evenredig verdelen** kan in combinatie met **Splitsen** worden gebruikt om het bedrag automatisch evenredig aan alle verdelingen toe te wijzen.
    -   De knop **Opnieuw instellen** kan voor bovenliggende verdelingen worden ingeschakeld wanneer er meerdere verdelingen bestaan. Met **Opnieuw instellen** wordt eventuele handmatige wijziging in de verdeling ongedaan gemaakt door alle bestaande verdelingen te verwijderen en de standaardverdelingen opnieuw te genereren.
    -   Eventuele onderliggende verdelingen, zoals korting, toeslag en btw, volgen altijd de bovenliggende verdeling. U kunt de bovenliggende/onderliggende relatie bekijken via **Verwijzing** &gt; **Hoofdgegevens**.
    -   De hoofdrekening en financiële dimensie kunnen ook voor onderliggende elementen worden bewerkt.
    -   De financiële dimensies in de boekhoudingsverdelingen volgen een standaardpatroon dat een document kan worden uitgebreid. Zie de gerelateerde artikelen voor meer details.
    -   Afwijkingsverdelingen kunnen in overeenkomstige scenario's worden gegenereerd, zoals een vergelijking tussen een leveranciersfactuur en een inkooporder. U kunt de overeenkomstige relaties bekijken tussen boekhoudingsverdeling via **Verwijzing** &gt; **Documentgegevens**.
    -   De knop **Corrigeren** wordt weergegeven en wordt ingeschakeld voor documenten die correcties ondersteunen. Met **Corrigeren** worden nieuwe verdelingen gemaakt. Eerst worden verdelingen gemaakt waarmee de oorspronkelijke verdelingen worden omgekeerd. Deze verdelingen kunnen niet worden gewijzigd. Vervolgens worden nieuwe juiste boekhoudingsverdelingen gemaakt. Deze verdelingen kunnen worden gewijzigd als de oorspronkelijke verdelingen kunnen worden gewijzigd.
    -   De knop **Projectgegevens** wordt ingeschakeld als een uitbreiding wanneer een regel aan een project wordt gekoppeld. Met boekhoudingsverdelingen voor projecten kunt u details weergeven, zoals de financieringsbron en regeleigenschap.
    -   U kunt de huidige boekhoudingsstatus van het document bekijken in **Verwijzing**. De status is voor het gehele document en geeft aan of het document in uitvoering of voltooid is.
-   **Verdelingen weergeven**: de boekhoudingsverdelingen voor alle regels en monetaire bedragen in het document weergeven. In deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.


Zie [Boekhoudingsverdelingen en journaalposten in de subadministratie voor facturen met vrije tekst](accounting-distributions-subledger-journal-entries-vendor-invoices.md) voor meer informatie.


