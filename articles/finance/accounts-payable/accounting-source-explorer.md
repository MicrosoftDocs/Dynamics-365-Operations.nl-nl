---
title: Boekhoudingsbronverkenner
description: Dit artikel bevat informatie over Boekhoudingsbronverkenner, dat u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.
author: rcarlson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab098aa36d6fa6c34beaaa31ecfbb1eb47840e343d7dee3d9cd3034d6ff8f9c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749193"
---
# <a name="accounting-source-explorer"></a>Boekhoudingsbronverkenner

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over Boekhoudingsbronverkenner, dat u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.

Boekhoudingsbronverkenner is een nieuwe pagina waarop brongegevens worden weergegeven. U kunt Boekhoudingsbronverkenner gebruiken als zelfstandig hulpprogramma of voor het analyseren van de gegevens achter de grootboekposten voor boekhouding. U kunt Boekhoudingsbronverkenner bijvoorbeeld gebruiken om de meest gedetailleerde brongegevens voor een saldo in Proefbalans voor een boekstuktransactie op te halen. Vervolgens kunt u de functie Exporteren naar MS Excel gebruiken om de gegevens verder in te delen en te verdelen in Microsoft Excel (bijvoorbeeld in draaitabel of een draaitabelrapport).

Met Boekhoudingsbronverkenner wordt altijd hetzelfde totaalbedrag per grootboekrekening weergegeven wanneer het grootboek wordt getoond (bijvoorbeeld in Proefbalans). Net als in Proefbalans kunt u segmenten in afzonderlijke kolommen weergeven. Selecteer alleen de juiste set met financiële dimensies. 

U kunt parameters gebruiken om een datuminterval voor de analyse te definiëren. Deze functionaliteit lijkt ook op de functionaliteit in Proefbalans.

Voor alle documenten die gebruikmaken van het raamwerk voor brondocumenten geeft Boekhoudingsbronverkenner aanvullende informatie weer op basis van de boekhoudingsverdelingen en, indien van toepassing, de projectboekhoudingsverdelingen. Deze informatie omvat geldbedragtype, project, activiteit, categorie en regeleigenschap. Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:

-   Afwijkingen tussen inkooporders en leveranciersfacturen, omdat elke afwijking wordt vertegenwoordigd met een type monetair bedrag, zoals toeslagafwijking
-   Factureerbare en niet-factureerbare uren en onkosten per project, bedrijfseenheid en hoofdrekening

Voor brondocumenten waarin het concept van identiteiten voor brondocumentverwijzing wordt gebruikt, worden met Boekhoudingbronverkenner zelfs meer details weergegeven, zoals de klant, de leverancier, de werknemer, het product, de hoeveelheid, de eenheidstekst en omschrijvingen. Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:

-   Hotelonkosten per bedrijfseenheid en hotelmerk voor een belastingperiode op basis van onkostennota's
-   Kortingen per leverancier, product, afdeling

Voor deze documenten kunt u ook naar het werkelijke brondocument van Boekhoudingsbronverkenner navigeren.

> [!NOTE]
> Vanaf versie 10.0.20 bevat de knop **Bijwerken** twee extra bereiken voor het beperken van de initiële query die wordt uitgevoerd om gegevens op de pagina weer te geven. Deze extra bereiken zijn ook beschikbaar in versie 10.0.19 als een service-update. De volgende velden zijn toegevoegd:
>
> - Van boekstuk, Naar boekstuk
> - Van hoofdrekening, Naar hoofdrekening

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
