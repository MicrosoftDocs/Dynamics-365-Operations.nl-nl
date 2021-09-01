---
title: Problemen oplossen met hiërarchieën voor magazijnbatches en seriële reserveringen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met reserveringshiërarchieën die gebruikmaken van batch- of seriële dimensies.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a2b6f76aba22c24c07a2727b2eb8752f6ce763654403d47e34932a21a776dccb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748638"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Problemen oplossen met hiërarchieën voor magazijnbatches en seriële reserveringen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met reserveringshiërarchieën die gebruikmaken van batch- of seriële dimensies.

Zie voor meer informatie [Flexibel reserveringsbeleid voor dimensies op magazijnniveau](flexible-warehouse-level-dimension-reservation.md).

De reserveringshiërarchie van een artikel bepaalt de vereiste opslagdimensies waaraan moet worden voldaan om een locatie aan een vraagorder toe te wijzen. Deze dimensies kunnen worden omschreven als *dimensies boven locatie*, voor alle dimensies waaraan moet worden voldaan voordat een locatie wordt toegewezen en *dimensies onder locatie* voor dimensies die kunnen worden toegewezen nadat een locatie aan de vraagorder is toegewezen. Deze reserveringshiërarchieën worden ook wel *batch-boven*- en *batch-onder*-reserveringshiërarchieën of *serienummer-boven*- en *serienummer-onder*-reserveringshiërarchieën gebruikt.

Voorraad kan alleen worden toegewezen als er geen hiaten zijn in de dimensies boven locatie. In een *batch-boven*-reserveringshiërarchie verwacht u bijvoorbeeld dat de dimensies **Site**, **Magazijn** en **Batchnummer** worden opgegeven op de vraagorder. Als een van deze dimensies ontbreekt, mislukt het toewijzingsproces. In een *batch-onder*- of *serienummer-onder*-reserveringshiërarchie kan daarentegen een batch- of serienummer worden opgegeven op de vraagorder, maar het toewijzingsproces vereist dit niet.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Het volgende foutbericht wordt weergegeven: "Om aan wave te worden toegewezen, moeten ladingsregels de afmetingen boven de locatie aangeven. Als u deze dimensies wilt toewijzen, moet u de ladingsregel reserveren en opnieuw maken."

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een artikel gebruikt met een *batch boven*-reserveringshiërarchie, werkt de opdracht **Vrijgeven aan magazijn** op de pagina **Workbench ladingplanning** niet als u probeert een lading voor een gedeeltelijke hoeveelheid vrij te geven. Dit foutbericht wordt weergegeven en er wordt geen werk gemaakt voor de gedeeltelijke hoeveelheid.

Wanneer u echter een artikel gebruikt met een *batch-onder*-reserveringshiërarchie, kunt u een lading vrijgeven voor een gedeeltelijke hoeveelheid vanaf de pagina **Workbench ladingplanning**.

### <a name="issue-cause"></a>Oorzaak van probleem

Als een dimensie zich boven de dimensie **Locatie** in de reserveringshiërarchie bevindt, moet deze eerst worden opgegeven voordat deze kan worden vrijgegeven aan het magazijn. Gedeeltelijke hoeveelheden kunnen niet worden vrijgegeven als een of meer dimensies boven de **locatie** niet zijn opgegeven.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>De automatische reserveringsprompt voor een batchnummer wordt geactiveerd, ook al is er voorraad beschikbaar.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een artikel met een *batch-boven*-reserveringshiërarchie gebruikt in een magazijn dat magazijnprocessen niet heeft ingeschakeld en automatische reservering is ingeschakeld, wordt de automatische reserveringsprompt voor een batchnummer weergegeven, zelfs als er slechts één batch beschikbaar is voor verzamelen.

Wanneer u echter hetzelfde artikel gebruikt in een magazijn waar magazijnprocessen zijn ingeschakeld, wordt de automatische reserveringsprompt niet weergegeven.

### <a name="issue-cause"></a>Oorzaak van probleem

Als een reserveringshiërarchie wordt gedefinieerd als *batch-boven* of *serienummer-boven*, moet de dimensie waarnaar wordt verwezen (**Batchnummer** of **Serienummer**) altijd worden opgegeven op aanvraagorders. Magazijnprocessen kunnen de informatie mogelijk voltooien als een enkel batch- of serienummer beschikbaar is. Omdat het magazijn echter niet is ingeschakeld voor magazijnprocessen, moet de gebruiker altijd alle dimensies boven **Locatie** opgeven.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Vaksjablonen met het criterium voor het vak Voorhanden overwegen houden geen rekening met de huidige voorhanden voorraad voor artikelen die geschikt zijn voor batchverwerking.

Zie [Magazijnvakken](warehouse-slotting.md) voor meer informatie.

### <a name="issue-description"></a>Probleembeschrijving

Vaksjablonen met het criterium voor het vak *Voorhanden overwegen* houden geen rekening met de huidige voorhanden voorraad voor *batch-boven*-artikelen. Ze houden hier alleen rekening mee als het batchnummer is opgegeven op de verkooporderregel.

Wanneer u echter *batch-onder*-artikelen gebruikt, wordt zoals verwacht rekening gehouden met de huidige voorhanden voorraad.

### <a name="issue-cause"></a>Oorzaak van probleem

De header van de vakkensjabloon kan worden gedefinieerd voor de vraagstrategie *Besteld*, *Gereserveerd* of *Vrijgegeven*. Voor de vraagstrategie *Besteld* gelden dezelfde reserveringshiërarchievereisten als van toepassing zijn op reserveringsprocessen of processen voor vrijgave aan het magazijn. Daarom moet voor artikelen met *batch-boven*- en *serienummer-onder*-reserveringshiërarchieën het batch- of serienummer worden opgegeven op de vraagorder (verkoop of transfer). Als alternatief kan de vraagstrategie *Gereserveerd* worden gebruikt om het batch- of serienummer te selecteren voordat de vraag voor magazijnvakken wordt gegenereerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
