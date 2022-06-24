---
title: Werkgebied voor leveranciersbetalingen
description: Dit artikel bevat informatie over het werkgebied Leveranciersbetalingen. In het werkgebied Leveranciersbetalingen wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6463e25fdcbc77dacc286460f3acd30ccc3d6e86
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847026"
---
# <a name="vendor-payments-workspace"></a>Werkgebied voor betalingen aan leveranciers

[!include [banner](../includes/banner.md)]

In het werkgebied **Leveranciersbetalingen** wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersbetalingen. Dit werkgebied bevat een weergave **Mijn werk** en een pagina **Analyses**. In de weergave **Mijn werk** vindt u overzichtstegels, rasters met leverancierstransacties en gerelateerde leveranciersgegevens. De pagina **Analyses** gebruikt de mogelijkheden van Microsoft Power BI om visuals te tonen die te maken hebben met betalingen aan leveranciers.

## <a name="setup-needed-to-view-power-bi-content"></a>Instellingen die nodig zijn om Power BI-inhoud weer te geven

De volgende instellingen moeten worden geconfigureerd om gegevens te kunnen weergeven in de visuele Power BI-elementen van **Leveranciersbetalingen**.
1. Ga naar **Systeembeheer > Instellen > Systeemparameters** om **Systeemvaluta** en **Systeemwisselkoers** in te stellen.
2. Ga naar **Grootboek > Kalenders > Fiscale kalenders** om de boekjaarkalenderdatums te valideren die aan de actieve tijdsperiode zijn toegewezen.
3. Ga naar **Grootboek > Instellen > Grootboek** en stel **Valuta voor boekhouding** en **Wisselkoerstype** in. 
4. Definieer wisselkoersen tussen transactievaluta's en valuta voor boekhouding, en valuta voor boekhouding en systeemvaluta. Ga hiervoor naar **Grootboek > Valuta's > Valutawisselkoersen**.
5. Ga naar **Systeembeheer > Instellen > Entiteitopslag** > om de samengevoegde meting **VendPaymentBIMeasureV2** te vernieuwen.

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


|            Rapportpagina            |                                                                                                                                                                                Visualisatie                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Overzicht van leveranciersbetalingen      | <ul><li>Verschuldigde facturen</li><li>Facturen met vervaldatum vandaag</li><li>Benutte kortingen versus gemiste kortingen</li><li>In de toekomst verschuldigde facturen op datum contantkorting</li><li>In de toekomst verschuldigde facturen op vervaldatum</li><li>Te laat betaalde facturen versus op tijd betaalde facturen</li><li>Betalingsworkflowtoewijzing</li><li>Saldo verkoper/klant</li><li>Openstaande facturen met geblokkeerde betaling</li></ul> |
|         Verschuldigde facturen         |                                                                                             <ul><li>Verschuldigde facturen</li><li>Details achterstallige facturen</li><li>Totaal openstaande facturen</li><li>Achterstallige facturen op leveranciergroep</li><li>Achterstallige facturen op bedrijf</li></ul>                                                                                              |
|        Facturen met vervaldatum vandaag         |                                                                                                         <ul><li>Facturen met vervaldatum vandaag</li><li>Details facturen met vervaldatum vandaag</li><li>Facturen met vervaldatum vandaag op bedrijf</li><li>Facturen met vervaldatum vandaag op leveranciergroep</li></ul>                                                                                                          |
| Benutte kortingen versus gemiste kortingen |                                                                             <ul><li>Benutte kortingen versus gemiste kortingen</li><li>Details benutte kortingen versus gemiste kortingen</li><li>Benutte kortingen versus gemiste kortingen op bedrijf</li><li>Benutte kortingen versus gemiste kortingen op leveranciersgroep</li></ul>                                                                              |
|      In de toekomst verschuldigde facturen       |                                                 <ul><li>In de toekomst verschuldigde facturen</li><li>Details in de toekomst verschuldigde facturen</li><li>In de toekomst verschuldigde facturen op bedrijf</li><li>In de toekomst verschuldigde facturen op leveranciersgroep</li><li>In de toekomst verschuldigde facturen op datum contantkorting</li><li>In de toekomst verschuldigde facturen op vervaldatum</li></ul>                                                  |
|        Te laat betaalde facturen         |                                                         <ul><li>Na vervaldatum betaalde facturen</li><li>Details na vervaldatum betaalde facturen</li><li>Na vervaldatum betaalde facturen op bedrijf</li><li>Na vervaldatum betaalde facturen op leveranciersgroep</li><li>Te laat betaalde facturen versus op tijd betaalde facturen</li></ul>                                                          |
|         Betalingsworkflow          |                                                                                <ul><li>Workflowexemplaren leverancierbetalingen</li><li>Workflowexemplaren leverancierbetalingen op fiatteur</li><li>Workflowexemplaren leverancierbetalingen op bedrijf</li><li>Gemiddeld aantal dagen in workflow op fiatteur</li></ul>                                                                                |
|    Saldo verkoper/klant     |                                                                                                                   <ul><li>Saldo verkoper/klant</li><li>Saldo verkoper/klant op bedrijf</li><li>Details saldo verkoper/klant</li></ul>                                                                                                                    |
|    Facturen met geblokkeerde betaling     |                                                                                         <ul><li>Facturen met geblokkeerde betaling</li><li>Details facturen met geblokkeerde betaling</li><li>Facturen met geblokkeerde betaling op bedrijf</li><li>Facturen met geblokkeerde betaling op leveranciersgroep</li></ul>                                                                                          |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]