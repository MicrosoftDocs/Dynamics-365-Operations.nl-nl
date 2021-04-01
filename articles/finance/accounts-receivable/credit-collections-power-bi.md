---
title: Power BI-inhoud - Crediterings- en aanmaningsbeheer
description: In dit onderwerp wordt beschreven wat er is opgenomen in de Power BI-inhoud Crediterings- en aanmaningsbeheer. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dfa79b3fb4099d64390c17b39508deaac63deb1c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235156"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Power BI-inhoud - Crediterings- en aanmaningsbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven wat er is opgenomen in de Microsoft Power BI-inhoud **Crediterings- en aanmaningsbeheer**. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Crediterings- en aanmaningsbeheer** is gemaakt voor crediterings- en incassomanagers en incassomedewerkers. Deze inhoud bevat belangrijke metrische gegevens over crediteringen en aanmaningen, zoals aantal dagen voor uitstaande verkopen, achterstallig saldo, kredietrisico en klanten die hun kredietlimiet hebben overschreden. Deze inhoud gebruikt transactiegegevens en biedt samengevoegde weergaven van creditering en aanmaningen voor alle bedrijven. Ook wordt een onderverdeling per bedrijf, klantengroep en klant verschaft.

Deze Power BI-inhoud bestaat uit 10 rapportpagina's:

- Twee overzichtspagina's (één pagina voor een overzicht van crediteringen en één pagina voor een overzicht van aanmaningen)
- Acht detailpagina's die metrische gegevens bevatten over crediteringen en aanmaningen die zijn gesegmenteerd en verdeeld in verschillende dimensies

Alle bedragen worden weergegeven in de systeemvaluta. U kunt de systeemvaluta instellen op de pagina **Systeemparameters**.

Standaard worden de gegevens over crediteringen en aanmaningen voor het huidige bedrijf weergegeven. Als u de gegevens voor alle bedrijven wilt bekijken, wijst u de taak **CustCollectionsBICrossCompany** aan de rol toe.

## <a name="setup-needed-to-view-power-bi-content"></a>Instellingen die nodig zijn om Power BI-inhoud weer te geven

De volgende instellingen moeten worden geconfigureerd om gegevens te kunnen weergeven in de visuele Power BI-elementen van **Klantcrediteringen en aanmaningen**.

1. Ga naar **Systeembeheer > Instellen > Systeemparameters** om **Systeemvaluta** en **Systeemwisselkoers** in te stellen.
2. Ga naar **Grootboek > Kalenders > Fiscale kalenders** om de boekjaarkalenderdatums te valideren die aan de actieve tijdsperiode zijn toegewezen.
3. Ga naar **Grootboek > Instellen > Grootboek** en stel **Valuta voor boekhouding** en **Wisselkoerstype** in.
4. Definieer wisselkoersen tussen transactievaluta's en valuta voor boekhouding, en valuta voor boekhouding en systeemvaluta. Ga hiervoor naar **Grootboek > Valuta's > Valutawisselkoersen**.
5. Ga naar **Systeembeheer > Instellen > Entiteitopslag** > om de samengevoegde meting **CustCollectionsBIMeasurementsV2** te vernieuwen.

>[!NOTE] 
> Ouderdomsperiodedefinities moeten worden ingesteld in **Parameters van module Klanten > Incasso's > Standaardwaarden incasso** om ouderdomsgegevens in de inhoud van Power BI in te schakelen.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud

De Power BI-inhoud **Crediterings- en aanmaningsbeheer** wordt weergegeven in het werkgebied **Klantcrediteringen en aanmaningen**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De Power BI-inhoud **CustCollectionsBICrossCompany** bevat een rapport dat uit een verzameling van metrische gegevens bestaat. Deze gegevens worden visueel weergegeven als diagrammen, tegels en tabellen. De volgende tabel bevat een overzicht van de visualisaties in de Power BI-inhoud **CustCollectionsBICrossCompany**.

| Rapportpagina                 | Visualisatie |
|-----------------------------|---------------|
| Overzicht van aanmaningen        | <ul><li>Klanten over tijd</li><li>Klanten boven kredietlimiet</li><li>30 dagen DSO (dagen uitstaande verkoop)</li><li>Openstaande cases</li><li>Gemiddeld aantal dagen tot sluiten van aanvraag</li><li>Openstaande activiteiten</li><li>Gemiddeld aantal dagen tot sluiten van activiteiten</li><li>Openstaande rentenota´s</li><li>Openstaande aanmaningen</li><li>Klantwachtstand</li><li>Verkoopwachtstand</li><li>Vervallen saldi</li><li>Bedragen aanmaningsstatus</li><li>Bedragen aanmaningscode</li><li>Afschrijving op basis van reden</li><li>Te betalen saldo per regio</li><li>Verwachte betalingen</li></ul> |
| Overzicht van crediteringen             | <ul><li>Klanten over tijd</li><li>Kredietlimiet versus achterstallig saldo</li><li>Raster Klanten boven kredietlimiet</li><li>Klanten boven kredietlimiet per bedrijf</li><li>Krediet versus totale kredietlimiet</li><li>Kredietlimiet versus gebruikt krediet per regio</li><li>Klanten per kredietbeoordeling</li></ul> |
| Kredietlimiet                | <ul><li>Kredietlimiet</li><li>Details kredietlimiet</li><li>Kredietlimiet per klant</li><li>Kredietlimiet per klantengroep</li><li>Kredietlimiet per kredietbeoordeling per bedrijf</li><li>Kredietlimiet vs gebruikt krediet per regio</li></ul> |
| Klanten boven kredietlimiet | <ul><li>Klanten boven kredietlimiet</li><li>Details klanten boven kredietlimiet</li><li>Klanten boven kredietlimiet per bedrijf</li><li>Klant boven kredietlimiet per klantengroep</li><li>Klanten boven kredietlimiet per regio</li></ul> |
| Klanten over tijd          | <ul><li>Klanten over tijd</li><li>Details klanten over tijd</li><li>Klanten over tijd per bedrijf</li><li>Klanten over tijd per klantengroep</li><li>Klanten over tijd per regio</li></ul> |
| Vervallen saldi               | <ul><li>Vervallen saldi</li><li>Details vervallen saldi</li><li>Vervallen saldi per bedrijf</li><li>Vervallen saldi per klantengroep</li></ul> |
| Verwachte betalingen           | <ul><li>Verwachte betalingen</li><li>Details verwachte betalingen</li><li>Verwachte betalingen per bedrijf</li><li>Verwachte betalingen per klantengroep</li><li>Verwachte betalingen per regio</li></ul> |
| Afschrijvingen                  | <ul><li>Afschrijvingen per regio</li><li>Details afschrijvingen</li><li>Afschrijvingen per hoofdrekening</li><li>Afschrijvingen per bedrijf</li><li>Afschrijvingen per klantengroep</li><li>Afschrijvingen per regio</li></ul> |
| Aanmaningsstatus          | <ul><li>Betwist</li><li>Belofte om te betalen geschonden</li><li>Beloofd te betalen</li><li>Details aanmaningsstatus</li><li>Bedragen aanmaningsstatus</li><li>Openstaande cases</li><li>Openstaande activiteiten</li></ul> |
| Aanmaningen         | <ul><li>Verzamelingscodebedragen</li><li>Details bedragen aanmaningscode</li><li>Bedrag aanmaningen per bedrijf</li><li>Bedrag aanmaningen per klantengroep</li><li>Bedrag aanmaningen per regio</li></ul> |

De grafieken en tegels op al deze rapporten kunnen worden gefilterd en op het dashboard worden vastgemaakt. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). U kunt ook de functionaliteit voor het exporteren van onderliggende gegevens gebruiken om de onderliggende gegevens te exporteren die worden samengevat in een visualisatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]