---
title: Boekhoudingsverdelingen
description: Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor de verwerking hiervan. Boekhoudingsverdelingen worden gebruikt om monetaire bedragen voor een brondocument toe te wijzen aan bepaalde grootboekrekeningen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a98ce08dc115bc96cec07c2d6ced10d774785fe9
ms.openlocfilehash: b1057caae6f47e5a17e194834fbbcb9d7d731605
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-distributions"></a>Boekhoudingsverdelingen

Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor de verwerking hiervan. Boekhoudingsverdelingen worden gebruikt om monetaire bedragen voor een brondocument toe te wijzen aan bepaalde grootboekrekeningen. 

Boekhoudingsverdelingen vormen een functie die in het hele programma kan worden gebruikt en die kan worden uitgebreid door elk brondocument, zoals een inkooporder, een leveranciersfactuur, een onkostennota en een vrije-tekstfactuur. Standaard wordt een standaardboekhoudingsverdeling gegenereerd voor elke brondocumentregel en monetair bedrag en wordt voorwaardelijk ingeschakeld voor wijziging. 

> [!Note] 
> Sommige documenten worden ook ondersteund koptekst document geldbedragen, zoals toeslagen voor orders en facturen. 

De algemene boekhoudingsverdelingsmogelijkheden bevatten de volgende opties om boekhoudingsverdelingen te verwerken:

-   **Bedragen verdelen**: de boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke documentkoptekst of -regel en alle onderliggende regels, zoals belastingen of toeslagen.
    -   Voor de verdelingen van de hoogste monetaire bedragen (bovenliggende verdelingen) kunnen de hoofdrekening en financiële dimensies rechtstreeks in het gesegmenteerde invoerbesturingselement in het raster worden bewerkt. De totaalprijs is een typisch voorbeeld van een dergelijke bovenliggende verdeling.
    -   De verdelingsbedragen worden gebaseerd op de termijnvaluta voor het document. Meestal is deze valuta de transactievaluta. Boekhoudings- en rapportagevalutabedragen worden gegenereerd als onderdeel van subadministratieboekhouding.
    -   Met de verdelingen worden de boekhoudingsdatum en de boekhoudgebeurtenis weergegeven. Doorgaans wordt de boekhoudgebeurtenis ingesteld op **Geen** totdat het document wordt gejournaliseerd/geboekt. Op dat punt wordt de boekhoudgebeurtenis **Oorspronkelijk**. Nadat de verdelingen zijn geboekt, kunt u de verdelingen niet wijzigen.
    -   De knop **Splitsen** kan voor bovenliggende verdelingen worden ingeschakeld. Met **Splitsen** worden nieuwe boekhoudingsverdelingen gegenereerd en de splitsing kan worden gebaseerd op percentage, bedrag of hoeveelheid.
    -   De knop **Evenredig verdelen** kan in combinatie met **Splitsen** worden gebruikt om het bedrag automatisch evenredig aan alle verdelingen toe te wijzen.
    -   De knop **Opnieuw instellen** kan voor bovenliggende verdelingen worden ingeschakeld wanneer er meerdere verdelingen bestaan. Met **Opnieuw instellen** wordt eventuele handmatige wijziging in de verdeling ongedaan gemaakt door alle bestaande verdelingen te verwijderen en de standaardverdelingen opnieuw te genereren.
    -   Eventuele onderliggende verdelingen, zoals korting, toeslag en btw, volgen altijd de bovenliggende verdeling. Ziet u de bovenliggende en onderliggende relatie op **verwijzing**&gt;**informatie bovenliggende**.
    -   De hoofdrekening en financiële dimensie kunnen ook voor onderliggende elementen worden bewerkt.
    -   De financiële dimensies in de boekhoudingsverdelingen volgen een standaardpatroon dat een document kan worden uitgebreid. Zie de gerelateerde artikelen voor meer details.
    -   Afwijkingsverdelingen kunnen in overeenkomstige scenario's worden gegenereerd, zoals een vergelijking tussen een leveranciersfactuur en een inkooporder. Ziet u de overeenkomende relaties tussen boekhoudingsverdeling op **verwijzing**&gt;**documentinformatie**.
    -   De knop **Corrigeren** wordt weergegeven en wordt ingeschakeld voor documenten die correcties ondersteunen. **Juiste** wordt gemaakt van nieuwe distributies. Eerst zijn verdelingen gemaakt waarin de oorspronkelijke verdelingen omkeren. Deze verdelingen kunnen niet worden gewijzigd. Volgende, nieuwe juiste boekhoudingsverdelingen worden gemaakt. Deze verdelingen kunnen worden gewijzigd als de oorspronkelijke verdelingen kunnen worden gewijzigd.
    -   De knop **Projectgegevens** wordt ingeschakeld als een uitbreiding wanneer een regel aan een project wordt gekoppeld. Met boekhoudingsverdelingen voor projecten kunt u details weergeven, zoals de financieringsbron en regeleigenschap.
    -   Ziet u de status van het huidige boekhouding in **verwijzing**. De status is voor het hele document en geeft aan of het document in uitvoering of voltooid.
-   ** Weergeven verdelingen ** – de boekhoudingsverdelingen voor alle regels en monetaire bedragen weergeven op het document. In deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.


Zie voor meer informatie [boekhoudingsverdelingen en journaalposten in subadministratie voor vrije-tekstfacturen](accounting-distributions-subledger-journal-entries-vendor-invoices.md).

