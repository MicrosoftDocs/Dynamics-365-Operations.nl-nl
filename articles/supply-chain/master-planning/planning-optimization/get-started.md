---
title: Aan de slag met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973471"
---
# <a name="get-started-with-planning-optimization"></a>Aan de slag met Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Zoals [eerder aangekondigd](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) is Planningsoptimalisatie gepland om de bestaande ingebouwde hoofdplanningsengine te vervangen.

Als u momenteel de ingebouwde hoofdplanningsengine gebruikt, moet u nu beginnen met het plannen van uw migratie naar Planningsoptimalisatie. Het is belangrijk dat u het migratieproces onmiddellijk start, omdat de bewerkingen kunnen worden beïnvloed wanneer afschaffing wordt afgedwongen. We raden u dringend aan de migratie vóór 1 december 2020 te voltooien om te voorkomen dat zich op het laatste moment problemen voordoen wanneer de afschaffing wordt afgedwongen. 

De functie Planningsoptimalisatie biedt momenteel geen ondersteuning voor alle functies die beschikbaar zijn in de planningsengine die in Supply Chain Management is ingebouwd. Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is in Planningsoptimalisatie voldoet aan uw behoeften. De functie Planningsoptimalisatie is momenteel niet standaard ingeschakeld in Dynamics Lifecycle Services (LCS), zodat u de evaluatie kunt uitvoeren voordat de functie wordt ingeschakeld.

> [!NOTE]
> U moet een uitzondering van de migratie naar Planningsoptimalisatie aanvragen als uw hoofdplanningsproces geen productie (door hoofdplanning gegenereerde geplande productieorders) bevat en u een hogere versie van de ingebouwde hoofdplanningsengine nodig hebt dan versie 10.0.15. Vanaf versie 10.0.16 wordt er een fout weergegeven in omgevingen wanneer de ingebouwde hoofdplanning wordt uitgevoerd zonder dat er geplande productieorders worden gegenereerd. Optimalisatieplanning moet worden gebruikt voor alle nieuwe implementaties waarmee geen geplande productieorders worden gegenereerd tijdens de hoofdplanning. Eigenaren van bestaande omgevingen die de ingebouwde hoofdplanningsengine uitvoeren zonder geplande productieorders te genereren, ontvangen een e-mail met details over het uitzonderingsproces. We raden u aan met een partner samen te werken om de migratie naar Planningsoptimalisatie te evalueren en te plannen.

Voordat u Planningsoptimalisatie inschakelt, kunt u het beste de resultaten van de analyse voor passende Planningsoptimalisatie evalueren. Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.

### <a name="availability"></a>Beschikbaarheid
Planningsoptimalisatie is momenteel beschikbaar in de volgende Azure-regio's: Verenigde Staten, Canada, Europa, Verenigd Koninkrijk en Australië. Als u de invoegtoepassing vanuit een andere geografische regio probeert te installeren, wordt in LCS een bericht weergegeven dat deze niet wordt ondersteund.

Planningsoptimalisatie wordt niet ondersteund voor on-premises implementaties van Dynamics 365 Supply Chain Management.

### <a name="licensing"></a>Licenties

Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.

### <a name="install-the-add-in"></a>De invoegtoepassing installeren

Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management gebruiken. U kunt de invoegtoepassing openen vanuit uw LCS-project en de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.

> [!NOTE]
> De vereiste voor Planningsoptimalisatie is een omgeving met grote beschikbaarheid voor LCS, tier 2 of hoger (geen OneBox-omgeving), met Dynamics 365 Supply Chain Management versie 10.0.7 of hoger. Als u de invoegtoepassing in een OneBox-omgeving probeert te installeren, wordt de installatie niet voltooid en moet u de installatie annuleren.

1. Meld u aan bij LCS en open de gewenste omgeving.
1. Ga naar **Volledige details**.
1. Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.
1. Selecteer **Een nieuwe invoegtoepassing installeren**.
1. Selecteer **Planningsoptimalisatie**.
1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
1. Selecteer **Installeren**.
1. Op het sneltabblad **Invoegtoepassingen voor omgeving** zou u moeten zien dat planningsoptimalisatie wordt geïnstalleerd.
1. Na een paar minuten moet **Installeren** veranderen in **Geïnstalleerd** (u moet de pagina mogelijk vernieuwen). Wanneer Planningsoptimalisering is geïnstalleerd, kunt u het activeren in Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Integratie van Planningsoptimalisatie

Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie**.

#### <a name="connection-status"></a>Verbindingsstatus

De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie. De volgende tabel bevat de mogelijke waarden.

| Verbindingsstatus | Beschrijving | Kan Planningsoptimalisatie worden gebruikt? |
|---|---|---|
| Verbonden | Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management. | Ja |
| Verbinding wordt ingeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd. | Nee |
| Niet verbonden | Er is geen verbinding met de service Planningsoptimalisatie. De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit onderwerp is beschreven. | Nee |
| Verbinding wordt uitgeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd. | Nee |
| Status ophalen | Het systeem wacht op statusinformatie van de service Planningsoptimalisatie. | Nee |

#### <a name="the-use-planning-optimization-option"></a>De optie Planningsoptimalisatie gebruiken

De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:

- **Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.
- **Nee**: de ingebouwde planningsengine voor Supply Chain Management wordt gebruikt voor de hoofdplanning.

> [!NOTE]
> Als bestaande planningsbatchtaken die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.

### <a name="integration-with-the-setup"></a>Integratie met de setup

Als de Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie. In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.

## <a name="additional-resources"></a>Aanvullende bronnen

[Algemene voorwaarden voor de preview](https://go.microsoft.com/fwlink/?linkid=2015274)

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)
