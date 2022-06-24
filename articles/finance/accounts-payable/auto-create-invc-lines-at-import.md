---
title: Factuurregels genereren wanneer u leveranciersfacturen importeert
description: In dit artikel wordt de functionaliteit beschreven voor het automatisch genereren van factuurregels op leveranciersfacturen bij het importeren van facturen.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e745ab1fb39edf69fabd147e46e1da8cc98ba6e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903502"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Factuurregels genereren wanneer u leveranciersfacturen importeert

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel wordt de functionaliteit beschreven voor het automatisch genereren van factuurregels op leveranciersfacturen bij het importeren van facturen.

Soms bevatten leveranciersfacturen beperkte informatie, zoals gegevens over ontvangers en subtotalen. Ze bevatten echter geen informatie voor regelartikelen. Wanneer u facturen importeert, wordt de factuurregels automatisch gegenereerd op basis van informatie op de bijbehorende inkooporder.

Volg deze stappen om het automatisch maken van factuurregels in te stellen.

1.  Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.
2.  Stel op het tabblad **Automatisering van leveranciersfacturen** onder **Automatisch regels maken voor geïmporteerde facturen** de optie **Automatisch factuurregels maken** in op **Ja**. 
4.  Selecteer in het veld **Standaardhoeveelheid kiezen voor het automatisch maken van factuurregels** de hoeveelheid die moet worden gebruikt om automatisch factuurregels te genereren:

    - **Bestelde hoeveelheid**: regels worden gegenereerd van inkooporderregels. Deze waarde is de standaardwaarde.
    - **Hoeveelheid productontvangstbon**: het inkoopordernummer wordt gebruikt om de relevante productontvangstbonnen te vinden. Vervolgens worden de hoeveelheden productontvangstbonnen gebruikt om factuurregels te genereren.

## <a name="data-entity-changes"></a>Wijzigingen in gegevensentiteit

Om de functionaliteit te ondersteunen die in dit artikel wordt beschreven, is de gegevensentiteit **Koptekst van leveranciersfactuur** verbeterd. Er zijn drie velden toegevoegd:

- **HeaderOnlyImport**: dit veld moet zijn ingesteld op **Ja** om regels voor factuurkopteksten te genereren.
- **PurchIdRange**: de lijst met inkoopordernummers. De factuurnummers kunnen een bereik zijn, zoals **INV0001..INV0009** (waarbij twee stipjes het begin en einde van het bereik scheiden), of discrete waarden, zoals **INV0001, INV0003, INV0006.** Alle inkooporders moeten bij dezelfde leveranciersrekening in de factuurkoptekst horen. Anders wordt het volgende foutbericht weergegeven: 'Genereren van factuurregels is mislukt. Inkooporders hebben verschillende leveranciersrekeningen.'
- **PackingslipRange**: de lijst met productontvangstbonnummers. Leveranciersfactuurregels kunnen worden gemaakt van productontvangstbonnen. Productontvangstbonnummers worden doorgaans niet in leveranciersfacturen opgenomen. Voer in dit veld alleen de productontvangstbonnummers in als u duidelijk kunt identificeren welke productontvangstbonnen voor welke specifieke facturen zijn. Factuurregels kunnen worden gegenereerd op basis van productontvangstbonnen. Als dit veld wordt gebruikt, wordt de instelling van het veld **Standaardhoeveelheid kiezen voor het automatisch maken van factuurregels** op de pagina **Parameters van module Leveranciers** genegeerd. 

**Beperking**: als u meerdere productontvangstbonnummers invoert, worden er meerdere in behandeling zijnde leveranciersfacturen gemaakt met hetzelfde factuurnummer. U moet deze facturen handmatig consolideren voordat u de factuur verder verwerkt. In toekomstige versies zijn we van plan om de facturen automatisch te consolideren, zodat de beperking wordt verwijderd.

Alle productontvangstbonnen moeten bij dezelfde leveranciersrekening in de factuurkoptekst horen.

## <a name="result"></a>Resultaat

Als er regels worden gegenereerd, wordt het volgende bericht in de automatiseringsgeschiedenis van de leveranciersfacturen vastgelegd: 'Automatisch factuurregels maken: voltooid'.

Als er geen regels worden gegenereerd, wordt het volgende foutbericht vastgelegd: 'Automatisch factuurregels maken: mislukt'.
