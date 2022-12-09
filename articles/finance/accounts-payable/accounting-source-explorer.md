---
title: Bronverkenner voor boekhouding
description: Dit artikel bevat informatie over de pagina Boekhoudingsbronverkenner, die u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806428"
---
# <a name="accounting-source-explorer"></a>Bronverkenner voor boekhouding

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over de pagina **Boekhoudingsbronverkenner**, die u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.

Op de pagina **Boekhoudingsbronverkenner** worden brongegevens weergegeven. U kunt deze gebruiken als zelfstandig hulpprogramma of voor het analyseren van de gegevens achter de grootboekposten voor boekhouding. U kunt de pagina bijvoorbeeld gebruiken om de meest gedetailleerde brongegevens voor een saldo in proefbalans voor een boekstuktransactie op te halen. Vervolgens kunt u de functie **Exporteren naar MS Excel** gebruiken om de gegevens verder in te delen en te verdelen in Microsoft Excel (bijvoorbeeld in een draaitabel of een draaitabelrapport).

Op de pagina **Boekhoudingsbronverkenner** wordt altijd hetzelfde totaalbedrag per grootboekrekening weergegeven wanneer het grootboek wordt getoond (bijvoorbeeld in een proefbalans). Net als in een proefbalans kunt u segmenten in afzonderlijke kolommen weergeven. Selecteer alleen de juiste set met financiële dimensies. 

U kunt parameters gebruiken om een datuminterval voor de analyse te definiëren. Deze functionaliteit lijkt ook op de functionaliteit in een proefbalans.

Voor alle documenten die gebruikmaken van het raamwerk voor brondocumenten geeft de pagina **Boekhoudingsbronverkenner** aanvullende informatie weer op basis van de boekhoudingsverdelingen en, indien van toepassing, de projectboekhoudingsverdelingen. Deze informatie omvat de waarden voor **Geldbedragtype**, **Project**, **Activiteit**, **Categorie** en **Regeleigenschap**. Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:

- Afwijkingen tussen inkooporders en leveranciersfacturen, omdat elke afwijking wordt vertegenwoordigd met een type monetair bedrag, zoals toeslagafwijking
- Factureerbare en niet-factureerbare uren en onkosten per project, bedrijfseenheid en hoofdrekening

Voor brondocumenten waarin het concept van identiteiten voor brondocumentverwijzing wordt gebruikt, worden met de pagina **Boekhoudingbronverkenner** zelfs meer details weergegeven, zoals de waarden voor **Klant**, **Leverancier**, **Werknemer**, **Product**, **Hoeveelheid**, **Eenheidstekst** en **Beschrijving**. Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:

- Hotelonkosten per bedrijfseenheid en hotelmerk voor een belastingperiode op basis van onkostennota's
- Kortingen per leverancier, product, afdeling

Voor deze documenten kunt u ook naar het werkelijke brondocument van de pagina **Boekhoudingsbronverkenner** navigeren.

> [!NOTE]
> Vanaf versie 10.0.31 is een nieuwe functie **Geavanceerde filterfunctie voor boekhoudingsbronverkenner** beschikbaar in Functiebeheer. Deze functie vervangt de knop **Bijwerken** om een krachtige geavanceerde queryervaring te bieden die lijkt op wat beschikbaar is op de pagina **Boekstuktransacties**. Met het geavanceerde filter kunt u filteren op vergelijkbare velden als op de pagina **Query boekstuktransacties**, zoals **Grootboekrekening**, **Business unit**, **Kostenplaats** en **Afdeling**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
