---
title: Boekhoudingsverdelingen
description: Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor verwerking.
author: sunfzam
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4330c86ee9ae35ce0f2c7bb85db533a39eafac46
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779576"
---
# <a name="accounting-distributions"></a>Boekhoudingsverdelingen

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over boekhoudingsverdelingen en beschrijft de beschikbare opties voor de verwerking hiervan. Boekhoudingsverdelingen worden gebruikt om monetaire bedragen voor een brondocument toe te wijzen aan bepaalde grootboekrekeningen. 

Boekhoudingsverdelingen vormen een functie die in het hele programma kan worden gebruikt en die kan worden uitgebreid door elk brondocument, zoals een inkooporder, een leveranciersfactuur, een onkostennota en een vrije-tekstfactuur. Standaard wordt een standaardboekhoudingsverdeling gegenereerd voor elke brondocumentregel en monetair bedrag en wordt voorwaardelijk ingeschakeld voor wijziging. 

> [!NOTE] 
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
    -   De financiële dimensies in de boekhoudingsverdelingen volgen een standaardpatroon dat een document kan worden uitgebreid.
    -   Afwijkingsverdelingen kunnen in overeenkomstige scenario's worden gegenereerd, zoals een vergelijking tussen een leveranciersfactuur en een inkooporder. U kunt de overeenkomstige relaties bekijken tussen boekhoudingsverdeling via **Verwijzing** &gt; **Documentgegevens**.
    -   De knop **Corrigeren** wordt weergegeven en wordt ingeschakeld voor documenten die correcties ondersteunen. Met **Corrigeren** worden nieuwe verdelingen gemaakt. Eerst worden verdelingen gemaakt waarmee de oorspronkelijke verdelingen worden omgekeerd. Deze verdelingen kunnen niet worden gewijzigd. Vervolgens worden nieuwe juiste boekhoudingsverdelingen gemaakt. Deze verdelingen kunnen worden gewijzigd als de oorspronkelijke verdelingen kunnen worden gewijzigd.
    -   De knop **Projectgegevens** wordt ingeschakeld als een uitbreiding wanneer een regel aan een project wordt gekoppeld. Met boekhoudingsverdelingen voor projecten kunt u details weergeven, zoals de financieringsbron en regeleigenschap.
    -   U kunt de huidige boekhoudingsstatus van het document bekijken in **Verwijzing**. De status is voor het gehele document en geeft aan of het document in uitvoering of voltooid is.
-   **Verdelingen weergeven**: de boekhoudingsverdelingen voor alle regels en monetaire bedragen in het document weergeven. In deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.

Er is een functie toegevoegd waarmee de tabel voor de boekhoudingsverdeling wordt gevalideerd om ervoor te zorgen dat de nieuwe velden correct worden ingesteld. Dit is de functie **Extra validatie van gegevens voor documenten inschakelen met behulp van het boekhoudkundig framework voor brondocumenten**. Deze functie is standaard ingeschakeld in versie 10.0.29. 

Zie [Boekhoudingsverdelingen en journaalposten in de subadministratie voor leveranciersfacturen](accounting-distributions-subledger-journal-entries-vendor-invoices.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
