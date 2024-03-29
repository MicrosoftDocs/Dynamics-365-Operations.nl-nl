---
title: Overzicht België
description: In dit artikel vindt u een overzicht van de specifieke functionaliteit voor België.
author: AdamTrukawka
ms.date: 05/27/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: belgium
ms.author: atrukawk
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 498c6ff23ef6f9100c2cafcf600d1796f7af3bca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279256"
---
# <a name="belgium-overview"></a>Overzicht België

[!include[banner](../includes/banner.md)]

In dit artikel vindt u informatie en koppelingen naar resources die moeten worden overwogen voor rechtspersonen met een primair adres in België.

## <a name="coda-bank-statement"></a>Coda-bankafschriftregel
CODA is een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt. Zie [CODA-bankafschrift](emea-bel-coda-bank-statement-import.md) voor meer informatie.

## <a name="export-ledger-transactions"></a>Export grootboektransacties
Met dit formulier exporteert u grootboektransacties voor een bepaald interval, bijvoorbeeld een boekjaar als een ASCII-bestand in CED-indeling. U kunt transacties in batches exporteren. Als u batchverwerking instelt, gaat u naar **Grootboek** > **Periodiek** > **Grootboektransacties exporteren**. Zie [Grootboektransacties exporteren](emea-bel-export-ledger-transactions.md) voor meer informatie.

## <a name="vat-declaration"></a>Btw-aangifte
Voor informatie over het instellen en werken met de nieuwe btw-aangifte in België raadpleegt u [Btw-aangifte (België)](emea-bel-vat-declaration-belgium.md).

## <a name="intervat-tax-declaration"></a>INTERVAT-belastingaangifte

> [!NOTE]
> Deze functie is vervangen door de functionaliteit voor btw-aangifte. Zie [Btw-aangifte (België)](emea-bel-vat-declaration-belgium.md) voor meer informatie.

Voor informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen alleen in België, raadpleegt u [INTERVAT-belastingaangifte](emea-bel-intervat-tax-declaration.md). Voor informatie over de standaardrapporten die u helpen bij de analyse van INTERVAT-belastingaangifte en afstemming raadpleegt u [Afstemmingsrapporten voor België](emea-bel-reconciliation-reports.md).

## <a name="reports-for-belgium"></a>Rapporten voor België

| Rapport                     | Naar het rapport navigeren | Aanvullende gegevens                 |
|----------------------------|--------------------------|----------------------------------------|
|Rapport Belgisch Luxemburgs Wissel Instituut (BLWI)|**Btw** > **Aangiften** > **Buitenlandse handel** > **BLWI** | Zie [Rapportage voor betalingssaldo instellen (België)](tasks/be-00011-set-up-payment-balance-reporting.md) als u de BLWI-informatie wilt instellen. Zie [Transacties maken en overboeken naar het BLWI (België)](tasks/be-00011-create-transfer-blwi.md) als u het BLWI-rapport wilt genereren.| 
|PRODCOM-rapport|**Btw** > **Aangiften** > **Buitenlandse handel** > **PRODCOM**|Fabrikanten van industriële producten verzenden het PRODCOM-rapport aan het Nationaal Instituut voor de Statistiek (NIS) in reactie op het jaarlijkse PRODCOM-onderzoek. Het PRODCOM-rapport bevat productiestatistieken voor industriële producten die worden vervaardigd door productiebedrijven die in België gevestigd zijn. Dit rapport wordt meestal gebruikt door accountants en boekhoudmanagers. Zie voor meer informatie [PRODCOM instellen en onderhouden](emea-bel-prodcom-report.md). |
|Journaalrapporten|**Grootboek** > **Vragen en rapporten** > **Journaalrapporten**|Belgische bedrijven moeten geregeld een rapport afdrukken voor elk journaal. Het rapport bevat een chronologische lijst met alle boekingen naar de grootboekrekeningen voor elk journaal. Deze rapporten bewijzen de integriteit van de boekhouding en worden gebruikt tijdens het financiële audits om de btw-vereffening af te stemmen met de boekingen op de bijbehorende grootboekrekeningen. Zie [Journaalrapporten (boekingsjournalen)](emea-bel-journal-reports.md) voor meer informatie. |
|Jaarlijkse btw-lijst van binnenlandse verkopen| **Belasting** > **Query's en rapporten** > **Btw-aangiften** > **Rapport factuuromzet - België** | Het rapport factuuromzet wordt eenmaal per jaar naar de belastingdienst verzonden. Het wordt gebruikt om de omzet aan te geven voor Belgische btw-geregistreerde klanten, als die omzet hoger is dan een bepaald bedrag. Het rapport bevat facturen van klanttransacties waarbij de klanten een ondernemingsnummer hebben dat is opgemaakt volgens de richtlijnen van de Belgische overheid. Zie [Jaarlijkse btw-lijst van binnenlandse verkopen](emea-bel-annual-vat-listing-of-domestic-sales.md) voor meer informatie. |
|Belgische Intrastat|  **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat** | U kunt de pagina **Intrastat** gebruiken om informatie te genereren en te rapporteren over handel tussen landen van de EU. De Belgische Intrastat-aangifte bevat informatie over de handel in goederen voor rapportage. Zie [Belgische Intrastat](emea-bel-intrastat.md) voor meer informatie. |
|ICL-lijst voor België|  **Belasting** > **Aangiften** > **Buitenlandse handel** > **ICL-lijst** | U kunt de pagina **ICL-lijst** gebruiken om informatie over de verkoop van goederen en diensten te genereren en te rapporteren voor rapportage in XML-indeling. Zie [ICL-lijst voor België](emea-bel-eu-sales-list.md) voor meer informatie. |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Microsoft Dynamics Localization Portal: Rapport België](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/Belgium.html) (CustomerSource-account vereist)
- [Overzicht van elektronische rapportage](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
- [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- [Lokalisatie en wettelijk voorgeschreven functies](../../fin-ops-core/dev-itpro/lcs-solutions/country-region.md?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
