---
title: Werkgebied voor automatisering van leveranciersfacturen
description: In dit onderwerp wordt uitgelegd hoe u het werkgebied instelt dat is gerelateerd aan leveranciersfacturen en waar de gegevens worden weergegeven die beschikbaar zijn via Microsoft Power BI.
author: abruer
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7216c2f6e593e3ca11d78903f318d5f217b19674
ms.sourcegitcommit: 375dd11a9e4076394a33e99f11371ab53e80c337
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5954130"
---
# <a name="vendor-invoice-automation-workspace"></a>Werkgebied voor automatisering van leveranciersfacturen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u het werkgebied instelt dat is gerelateerd aan leveranciersfacturen en waar de gegevens worden weergegeven die beschikbaar zijn via Microsoft Power BI. De gegevens van de leveranciersfactuur in dit werkgebied worden gefilterd voor specifieke gebruikers en worden weergegeven in een grafische indeling.

## <a name="overview"></a>Overzicht

In het werkgebied **Automatisering van leveranciersfacturen** wordt informatie weergegeven die is gerelateerd aan de verwerking van leveranciersfacturen. Dit werkgebied bevat de weergave **Mijn werk** en de pagina **Analyse - alle bedrijven**. In de weergave **Mijn werk** vindt u overzichtstegels, rasters met leverancierstransacties en gerelateerde leveranciersgegevens. Op de pagina **Analyse - alle bedrijven** worden de mogelijkheden van Power BI gebruikt om visualisaties te tonen die zijn gerelateerd aan leveranciersfacturen.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Het werkgebied zo instellen dat Power BI-inhoud wordt weergegeven

U moet deze instelling voltooien voordat gegevens in Power BI-visualisaties in het werkgebied **Automatisering van leveranciersfacturen** kunnen worden weergegeven.

1. Filter in het werkgebied **Functiebeheer** de lijst om de functie **Automatisering van leveranciersfacturen** te vinden.
3. Selecteer **Nu inschakelen**.
4. Als u wilt dat facturen kunnen worden verwerkt van begin tot eind zonder dat handmatige tussenkomst is vereist, moet u een werkstroom voor leveranciersfacturen instellen. Als u een werkstroom wilt instellen, gaat u naar **Leveranciers \> Instellen \> Leverancierswerkstromen**.
5. Ga naar **Leveranciers \> Instellen \> Parameters van module Leveranciers** en selecteer het tabblad **Automatisering van leveranciersfacturen**. Zie [Instellingsopties voor het automatisering van leveranciersfacturen](vnd-invoice-set-up-options.md) voor meer informatie.
6. Stel de optie **Geïmporteerde facturen automatisch indienen bij het werkstroomsysteem** in op **Ja**.
7. Als productontvangstbonnen automatisch moeten worden afgestemd, stelt u de optie **Productontvangstbonnen automatisch afstemmen met factuurregels** in op **Ja**.
8. Controleer de overige, optionele instellingen en configureer deze in overeenstemming met de vereisten van uw organisatie.
9. Ga naar **Systeembeheer \> Instellen \> Systeemparameters** en stel de velden **Systeemvaluta** en **Systeemwisselkoers** in.
10. Ga naar **Grootboek \> Instellen \> Grootboek** en stel de velden **Valuta voor boekhouding** en **Wisselkoerstype** in.
11. Ga naar **Grootboek \> Valuta´s \> Wisselkoersen** en voer de wisselkoersen tussen de transactievaluta en de valuta voor boekhouding in en tussen de valuta voor boekhouding en de systeemvaluta.
12. Ga naar **Systeembeheer \> Instellen \> Entiteitsopslag** en zoek naar **Meting voor automatisering van leveranciersfacturen**. Selecteer **Vernieuwen**.

Als u de informatie wilt weergeven die in het werkgebied wordt weergegeven, moet u over de beveiligingsrol Leveranciersmanager of Leveranciersmedewerker beschikken.

## <a name="my-work-view"></a>Weergave Mijn werk

### <a name="company-selection"></a>Bedrijfsselectie

Wanneer de functie **Automatisering van leveranciersfacturen** is ingeschakeld, wordt het veld **Bedrijf** boven aan het werkgebied weergegeven. De selectie in het veld **Bedrijf** is van invloed op alle informatie die in het werkgebied wordt weergegeven. In de weergave wordt standaard informatie weergegeven over het bedrijf waarbij u zich hebt aangemeld. Door een ander bedrijf te selecteren in het veld **Bedrijf** kunt u informatie over dat bedrijf weergeven in het werkgebied. U kunt vervolgens een tegel in het werkgebied selecteren om naar de gerelateerde pagina in het geselecteerde bedrijf te gaan.

### <a name="summary-tiles"></a>Overzichtstegels

De tegels in de sectie **Overzicht van facturen in behandeling** van de weergave **Mijn werk** geven een overzicht van de status van uw leveranciersfacturen. U kunt journalen zien die nog niet zijn geboekt en geblokkeerde facturen. Bovendien zijn er vier tegels die zijn gekoppeld aan de functie voor automatisering van leveranciersfacturen:

- Handmatige ontvangstvereffening vereist
- Validatie van vereffening mislukt
- Facturen niet ingediend bij werkstroom
- Facturen niet geïmporteerd

(Voor deze vier tegels moet de functie Automatisering van leveranciersfacturen zijn ingeschakeld in Functiebeheer.)

Als u de tegel **Leveranciersfacturen herstellen** wilt gebruiken, moet de functie zijn ingeschakeld in de parameters van de module Leveranciers. Ga naar **Leveranciers \> Parameters van module Leveranciers** en stel vervolgens op het tabblad **Factuur** de optie **Herstellen van leveranciers toestaan** in op **Ja**.

Wanneer de functie is ingeschakeld, worden ook drie tegels gegroepeerd in het werkgebied in een sectie met de naam **Journalen**. De tegels hebben de naam **Journalen**, **Journalen - toegewezen aan mij** en **Facturenpool**. 

De informatie in de sectie **Overzicht van facturen in behandeling** is voor het bedrijf dat is ingesteld als het standaardbedrijf voor uw aanmelding.

### <a name="creating-new-records"></a>Nieuwe records maken

Als u een nieuwe factuurrecord wilt maken, selecteert u **Nieuw** en selecteert u een van de volgende recordtypen in de lijst:

- Leveranciersfactuur
- Factuurjournaal
- Algemeen factuurjournaal
- Factuurregister
- Goedkeuring van facturen

De record die u maakt, wordt gebaseerd op het bedrijfsfilter en niet op het bedrijf waarbij u bent aangemeld. U bent bijvoorbeeld aangemeld bij het bedrijf **UMSF**, maar het bedrijfsfilter is ingesteld op **GBSI**. Wanneer u in dit geval **Nieuw** selecteert en vervolgens een recordtype in de lijst selecteert, wordt de record gemaakt in het GBSI-bedrijf.

### <a name="documents-not-invoiced-grids"></a>Rasters voor niet-gefactureerde documenten

De sectie **Niet-gefactureerde documenten** bevat rasters waarin documenten worden weergegeven die wachten op leveranciersfacturen.

In het raster **Openstaande inkooporders** worden alle inkooporders weergegeven die nog niet volledig zijn gefactureerd. U kunt de knop **Nu factureren** gebruiken om een leveranciersfactuur voor een inkooporder te maken. U kunt de knop **Vooruitbetaling nu factureren** gebruiken om een vooruitbetalingsfactuur voor een inkooporder te maken.

In het raster **Productontvangstbonnen** worden alle inkoopontvangsttransacties weergegeven die nog niet volledig zijn gefactureerd. U kunt de knop **Nu factureren** gebruiken om een leveranciersfactuur voor een inkooporder te maken.

In het raster **Leveranciersfacturen in behandeling** worden alle leveranciersfacturen weergegeven die niet naar het werkstroomsysteem zijn verzonden. U kunt het veld **Zoeken** en/of het bedrijfsfilter gebruiken om te zoeken naar een specifieke leveranciersfactuur. U kunt de knop **Bewerken** gebruiken om een transactie te bewerken die in het raster wordt weergegeven.

In het raster **Inkooporder zoeken** kunt u het veld **Zoeken** gebruiken om te zoeken naar een specifieke inkooporder.

### <a name="related-information"></a>Verwante informatie

U kunt informatie over geboekte facturen weergeven met de koppelingen aan de rechterkant van het werkgebied. Deze koppelingen zijn **Openstaande leveranciersfacturen**, **Factuurjournaal** en **Factuurgeschiedenis en vereffeningsdetails**. In de sectie **Leveranciers** kunt u een gefilterde lijst openen waarin alle geblokkeerde leveranciers worden weergegeven of u kunt de koppeling **Alle leveranciers** gebruiken. De koppelingen **Alle inkooporders** en **Openstaande vooruitbetalingen** zijn ook beschikbaar.

### <a name="analytics--all-companies-page"></a>Pagina Analyse - alle bedrijven

Wanneer de optie **Geïmporteerde facturen automatisch indienen bij het werkstroomsysteem** is ingesteld op **Ja** op de pagina **Parameters van module Leveranciers**, kunt u automatiseringsanalyse weergeven. De pagina **Analyse - alle bedrijven** bevat belangrijke metrische gegevens, zoals leveranciersfacturen die ter goedkeuring bij de fiatteur en het bedrijf liggen. Deze pagina bevat vijf rapportpagina's. Eén pagina bevat een overzicht en de andere pagina's bieden details over metrische gegevens over automatisering van Leveranciers.

In de volgende tabel ziet u de visualisaties die op elke rapportpagina beschikbaar zijn.

| Rapportpagina                    | Visualisaties |
|--------------------------------|----------------|
| Overzicht van Leveranciersfacturen        | <ul><li>Leveranciersfacturen in afwachting van automatisering in systeemvaluta</li><li>Facturen die niet kunnen worden geïmporteerd</li><li>Facturen in werkstroom</li><li>Contactloze facturen van de afgelopen 30 dagen</li><li>Totaal aantal geautomatiseerde facturen van de afgelopen 30 dagen</li><li>Saldo van openstaande facturen in systeemvaluta</li><li>Redenen voor fouten in van de afgelopen 30 dagen</li><li>Percentage van geboekte facturen die automatisch zijn verwerkt</li><li>Dagen voor het verwerken van een factuur</ul></li> |
| Automatiseringsstatus              | <ul><li>Contactloze facturen van de afgelopen 30 dagen</li><li>Contactloze facturen van de afgelopen 30 dagen per bedrijf</li><li>Contactloze facturen van de afgelopen 30 dagen per leveranciersgroep</li><li>Percentage van geboekte facturen die automatisch zijn verwerkt</li><li>Dagen voor het verwerken van een factuur</li></ul> |
| Facturen die niet kunnen worden geïmporteerd | <ul><li>Facturen die niet kunnen worden geïmporteerd</li><li>Facturen die niet kunnen worden geïmporteerd per bedrijf</li></ul> |
| Redenen voor automatiseringsfout | <ul><li>Mislukte facturen</li><li>Mislukte facturen per bedrijf</li><li>Mislukte facturen per leveranciersgroep</li></ul> |
| Werkstroomstatus                | <ul><li>Facturen in werkstroom</li><li>Werkstroomexemplaren leveranciersfacturen</li><li>Toewijzing per fiatteur</li><li>Leveranciersfacturenwerkstroom per bedrijf</li><li>Gemiddeld aantal dagen in workflow op fiatteur</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
