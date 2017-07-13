---
title: Werkgebied voor betalingen aan leveranciers
description: Dit onderwerp biedt informatie over het werkgebied Leveranciersbetalingen. In het werkgebied Leveranciersbetalingen wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen.
author: twheeloc
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 4011a2383fe4556b730fa0b6353ba0b9773a4eec
ms.contentlocale: nl-nl
ms.lasthandoff: 06/14/2017


---

# <a name="vendor-payments-workspace"></a>Werkgebied voor betalingen aan leveranciers

[!include[banner](../includes/banner.md)]

In het werkgebied **Leveranciersbetalingen** wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen. Dit werkgebied bevat een weergave **Mijn werk** en een pagina **Analyses**. In de weergave **Mijn werk** vindt u overzichtstegels, rasters met leverancierstransacties en gerelateerde leveranciersgegevens. De pagina **Analyses** gebruikt de mogelijkheden van Microsoft Power BI om visuals te tonen die te maken hebben met betalingen aan leveranciers.

## <a name="my-work-view"></a>Weergave Mijn werk

### <a name="summary-tiles"></a>Overzichtstegels

De tegels in de sectie **Overzicht** geven een overzicht van de status van uw betalingsinformatie. U ziet hier betalingsjournalen die nog niet zijn geboekt, achterstallige facturen, alle leveranciers en leveranciers die in de wachtstand staan. Vanuit de sectie **Overzicht** kunt u een nieuwe betalingsronde maken.

De informatie in de sectie **Overzicht** is voor het bedrijf waarbij u zich hebt aangemeld

### <a name="vendor-transactions-grids"></a>Leverancierstransactierasters

De sectie **Leverancierstransacties** bevat rasters waarin u de facturen ziet die achterstalling zijn en betalingen die niet zijn vereffend. Vanuit het raster **Achterstallige facturen** kunt u de vereffeningshistorie voor een geselecteerde factuur bekijken. Vanuit het raster **Betalingen niet vereffend** kunt u de vereffeningshistorie voor een geselecteerde factuur bekijken en deze vereffenen.

Medewerkers die gecentraliseerd betalingen afhandelen, kunnen met een filter bovenaan elk raster een bedrijf selecteren. Het raster wordt vervolgens zo gefilterd dat het veld alleen die bedrijven weergeeft die zijn gedefinieerd in de organisatiehiërarchie voor gecentraliseerde betalingen waarvoor de medewerker rechten heeft.

Op het tabblad **Transacties vinden** in de sectie **Leverancierstransacties** kunt u naar leverancierstransacties zoeken.

### <a name="related-information"></a>Verwante informatie

U kunt het rapport **Leverancier naar ouderdom gerangschikt** en het rapport **Betalingsoverzicht per datum** weergeven met de koppelingen in de sectie **Gerelateerde informatie** van het werkgebied.

## <a name="analytics-page"></a>Pagina Analyses

De pagina **Analyses** bevat belangrijke metrics, zoals achterstallige leveranciersfacturen en leveranciersfacturen die in de toekomst moeten betaald worden. Deze pagina bevat negen rapportpagina's. Eén pagina bevat een overzicht en de andere acht pagina's bieden informatie over betalingsmetrics uit Crediteuren.

In de volgende tabel ziet u de visualisaties die op elke rapportpagina beschikbaar zijn.

| Rapportpagina | Visualisatie |
|-------------|---------------|
| Overzicht van leveranciersbetalingen | <ul><li>Verschuldigde facturen</li><li>Facturen met vervaldatum vandaag</li><li>Benutte kortingen versus gemiste kortingen</li><li>In de toekomst verschuldigde facturen op datum contantkorting</li><li>In de toekomst verschuldigde facturen op vervaldatum</li><li>Te laat betaalde facturen versus op tijd betaalde facturen</li><li>Betalingsworkflowtoewijzing</li><li>Saldo verkoper/klant</li><li>Openstaande facturen met geblokkeerde betaling</li></ul> |
| Verschuldigde facturen | <ul><li>Verschuldigde facturen</li><li>Details achterstallige facturen</li><li>Totaal openstaande facturen</li><li>Achterstallige facturen op leveranciergroep</li><li>Achterstallige facturen op bedrijf</li></ul> |
| Facturen met vervaldatum vandaag | <ul><li>Facturen met vervaldatum vandaag</li><li>Details facturen met vervaldatum vandaag</li><li>Facturen met vervaldatum vandaag op bedrijf</li><li>Facturen met vervaldatum vandaag op leveranciergroep</li></ul> |
| Benutte kortingen versus gemiste kortingen | <ul><li>Benutte kortingen versus gemiste kortingen</li><li>Details benutte kortingen versus gemiste kortingen</li><li>Benutte kortingen versus gemiste kortingen op bedrijf</li><li>Benutte kortingen versus gemiste kortingen op leveranciersgroep</li></ul> |
| In de toekomst verschuldigde facturen | <ul><li>In de toekomst verschuldigde facturen</li><li>Details in de toekomst verschuldigde facturen</li><li>In de toekomst verschuldigde facturen op bedrijf</li><li>In de toekomst verschuldigde facturen op leveranciersgroep</li><li>In de toekomst verschuldigde facturen op datum contantkorting</li><li>In de toekomst verschuldigde facturen op vervaldatum</li></ul> |
| Te laat betaalde facturen | <ul><li>Na vervaldatum betaalde facturen</li><li>Details na vervaldatum betaalde facturen</li><li>Na vervaldatum betaalde facturen op bedrijf</li><li>Na vervaldatum betaalde facturen op leveranciersgroep</li><li>Te laat betaalde facturen versus op tijd betaalde facturen</li></ul> |
| Betalingsworkflow | <ul><li>Workflowexemplaren leverancierbetalingen</li><li>Workflowexemplaren leverancierbetalingen op fiatteur</li><li>Workflowexemplaren leverancierbetalingen op bedrijf</li><li>Gemiddeld aantal dagen in workflow op fiatteur</li></ul> |
| Saldo verkoper/klant | <ul><li>Saldo verkoper/klant</li><li>Saldo verkoper/klant op bedrijf</li><li>Details saldo verkoper/klant</li></ul> |
| Facturen met geblokkeerde betaling | <ul><li>Facturen met geblokkeerde betaling</li><li>Details facturen met geblokkeerde betaling</li><li>Facturen met geblokkeerde betaling op bedrijf</li><li>Facturen met geblokkeerde betaling op leveranciersgroep</li></ul> |

