---
title: Operational Insights instellen
description: In dit artikel wordt beschreven hoe u de functionaliteit Operational Insights in Microsoft Dynamics 365 Commerce kunt instellen en gebruiken.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832119"
---
# <a name="set-up-operational-insights"></a>Operational Insights instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de functionaliteit Operational Insights in Microsoft Dynamics 365 Commerce kunt instellen en gebruiken.

Operational Insights is een Dynamics 365 Commerce-functie die is ontworpen om klanten meer inzicht te geven in hun servicestatus en bedrijfsfunctionaliteit door telemetrie rechtstreeks naar een Application Insights-account van de klant te sturen.

Als u Operational Insights voor uw omgevingen in Commerce Headquarters inschakelt, kunt u een samengestelde lijst met gebeurtenissen verzamelen vanuit zowel CSU (Commerce Scale Unit) als uw POS-apparaten (Point-Of-Sale). Deze gebeurtenissen geven u een beter inzicht in de prestaties van uw systemen en maken het mogelijk om belangrijke technische gegevens en zakelijke metrische gegevens te controleren.

Zelfs als u deze telemetrie niet de hele tijd wilt verzamelen, kunt u er toch van profiteren door de verzameling voor specifieke omgevingen snel in of uit te schakelen. Op deze manier kunt u met de telemetrie problemen oplossen of foutopsporing tijdens ontwikkeling of productie oplossen.

## <a name="access-logs-in-application-insights"></a>Toegang tot logboeken in Application Insights

Voor toegang tot diagnostische gebeurtenislogboeken voor Commerce CSU en POS-onderdelen via Application Insights voltooit u de procedures in deze sectie.

### <a name="minimum-version-requirements-for-csu"></a>Minimale versie voor CSU

CSU heeft de volgende minimumversievereisten:

- 10.0.23 (Retail Server versie 9.33.22062.15 en hoger)
- 10.0.24 (Retail Server versie 9.34.22062.14 en hoger)
- 10.0.25 (Retail Server versie 9.35.22062.13 en hoger)
- 10.0.26 en hoger (alle versies)

### <a name="enable-diagnostic-events-in-application-insights"></a>Diagnostische gebeurtenissen inschakelen in Application Insights

> [!IMPORTANT]
> Als u eerder een voorbeeldversie van Operational Insights hebt gebruikt, moet u de volgende procedure gebruiken om Operational Insights in te stellen. Op deze manier zorgt u ervoor dat betrouwbare en beveiligde toegang tot gebeurtenissen kunnen doorgaan.

Als u diagnostische gebeurtenissen van Commerce-onderdelen wilt inschakelen, moet u over een Application Insights-account beschikken. U kunt een bestaande account gebruiken of [een nieuwe account maken](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Uit privacyoverwegingen voor gegevens is het raadzaam om afzonderlijke Application Insights-accounts te gebruiken voor productie-, sandbox- en ontwikkelomgevingen. Nadat u een rekening hebt aangemaakt, moet u de functie **Operational Insights** in Headquarters inschakelen.

Volg deze stappen om diagnostische gebeurtenissen in Application Insights te stellen.

1. Open het werkgebied **Functiebeheer** van Headquarters en schakel de functie **Operational Insights** in.
1. Ga naar **Systeembeheer \> Instellingen \> Operational Insights**.
1. Stel op het tabblad **Configureren** de optie **Gebeurtenissen Commerce-afzetkanaal** in op **Ja**.
1. Voer op het tabblad **Omgevingen** de waarden **LCS-omgevings-id** en **Omgevingsmodus** in voor elke omgeving waar u Application Insights wilt gebruiken. U kunt de omgevings-id van elke omgeving vinden op de pagina **Omgevingsdetails** voor die omgeving in Microsoft Dynamics Lifecycle Services. Deze stap is vereist om te voorkomen dat diagnostische gebeurtenissen per ongeluk naar een onjuiste omgeving worden verzonden wanneer databasekopieerbewerkingen worden uitgevoerd.
1. Geef op het tabblad **Application Insights-register** de waarde van Application Insights **Instrumentatiesleutel** op en de bijbehorende **Omgevingsmodus** -waarde van de omgevingen waar u elke Application Insights-account wilt gebruiken.
1. Nadat u de voorgaande configuratie hebt voltooid, moet u de taak **CDX-taak 1110** uitvoeren. U kunt wachten tot deze taak volgens een eigen schema wordt uitgevoerd of u kunt deze handmatig uitvoeren.
1. Ga in Lifecycle Services naar **Omgevingsdetails \> Commerce \> Beheren**, selecteer een CSU-exemplaar en selecteer vervolgens **Opnieuw starten**. Herhaal deze stap voor elke CSU.
1. Herhaal de voorgaande stappen voor elke omgeving waarin u van plan bent Application Insights te gebruiken.

> [!NOTE]
> - De telemetriegebeurtenissen in Operational Insights kunnen worden gewijzigd. We raden u aan om gebeurtenissen van Operational Insights te gebruiken om zelf eerst een analyse uit te voeren en problemen op te lossen, en geen dashboards of waarschuwingen te definiëren. Als u gebeurtenissen gebruikt voor niet-self-service-probleemoplossing, raden we u aan om uw query's te valideren en bij te werken na elke CSU/POS-release.
> - Vanaf Commerce versie 10.0.29 zorgen de procedures in deze sectie ook voor het inschakelen van nieuwe POS Operational Insights-gebeurtenissen voor uw Application Insights-account. Zie [Operational Insights voor POS – Gebeurtenissen en query's](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf) voor meer informatie.

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>Het bestand DLLHost.exe.config gebruiken om gebeurtenissen voor POS Operational Insights te regelen

Om met het bestand DLLHost.exe.config gebeurtenissen voor POS Operational Insights te regelen, voert u deze stappen uit.

1. Open in een teksteditor het **DLLHost.exe.config**-bestand in **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. Verwijder in de sectie **diagnosticsSection** het sink-xml-element met de klassenaam **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. Sla het bestand op.

### <a name="disable-diagnostic-events-in-application-insights"></a>Diagnostische gebeurtenissen uitschakelen in Application Insights

> [!IMPORTANT]
> Als u diagnostische gebeurtenissen wilt uitschakelen en deze niet meer wilt verzenden naar Application Insights, moet u de volgende procedure uitvoeren. U kunt deze functie niet uitschakelen in Functiebeheer.

Volg deze stappen om diagnostische gebeurtenissen in Application Insights uit te schakelen.

1. Ga in Headquarters naar **Systeembeheer \> Operational Insights**.
1. Stel op het tabblad **Configureren** de optie **Gebeurtenissen Commerce-afzetkanaal** in op **Nee**.
1. Nadat u de voorgaande configuratie hebt voltooid, moet u de taak **CDX-taak 1110** uitvoeren. U kunt wachten tot deze taak volgens een eigen schema wordt uitgevoerd of u kunt de taak handmatig uitvoeren.
1. Ga in Lifecycle Services naar **Omgevingsdetails \> Commerce \> Beheren**, selecteer een CSU-exemplaar en selecteer vervolgens **Opnieuw starten**. Herhaal deze stap voor elke CSU.
1. Herhaal de voorgaande stappen voor elke omgeving waarin u van plan bent Application Insights uit te schakelen.

Als u diagnostische gebeurtenissen voor één omgeving wilt uitschakelen, verwijdert u de instrumentatiesleutel op het tabblad **Application Insights-register** van de pagina **Operational Insights**. Voltooi vervolgens stap 3 en 4 van de voorgaande procedure.

> [!NOTE]
> In Commerce versie 10.0.29 en hoger zorgen de stappen in deze sectie ook voor het uitschakelen van nieuwe POS Operational Insights-gebeurtenissen voor uw Application Insights-account. 
