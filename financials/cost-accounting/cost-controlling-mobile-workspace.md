---
title: Mobiel werkgebied voor kostenbeheer voor de app Microsoft Dynamics 365 for Operations
description: Met het mobiele werkgebied voor kostenbeheer kunnen kostenplaatsmanagers de prestaties van kostenplaatsen altijd en overal bekijken.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiel werkgebied voor kostenbeheer voor de app Microsoft Dynamics 365 for Operations

Met het mobiele werkgebied voor kostenbeheer kunnen kostenplaatsmanagers de prestaties van kostenplaatsen altijd en overal bekijken. 

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                         | Omschrijving                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Meer informatie over het mobiele platform van Microsoft Dynamics 365 for Operations | [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Zorg ervoor dat u een omgeving gebruikt met Microsoft Dynamics 365 for Operations versie 1611 en Microsoft Dynamics for Operations-platform update 3 (november 2016). |
| Hotfix KB 3215650                                                    | Installeer de hotfix om de werkgebieden in te schakelen die beschikbaar zijn in Microsoft Dynamics 365 for Operations.                                                                       |
| Mobiel apparaat waarop de Dynamics 365 for Operations-app is geïnstalleerd | Download de Dynamics 365 for Operations-app van uw winkel voor mobiele apps.                                                                                                      |

## <a name="introduction"></a>Introductie
Het mobiele werkgebied voor kostenbeheer biedt een directe weergave van de huidige prestaties van kostenplaatsen door werkelijke kosten ten opzichte van de gebudgetteerde kosten te vergelijken. U kunt inzoomen op statuswaarden van afzonderlijke kostenelementen.

### <a name="example"></a>Voorbeeld

Een werknemer ontvangt een uitnodiging voor een internationale conferentie. De organisatie moet zorg dragen voor alle reiskosten. De werknemer vraagt zijn manager of hij de conferentie mag bijwonen. De manager opent snel het mobiele werkgebied voor kostenbeheer op zijn mobiele telefoon om te zien of hij budget heeft zodat de werknemer de conferentie kan bijwonen.

### <a name="data-security"></a>Gegevensbeveiliging

De gegevens in het werkgebied voor kostenbeheer worden beveiligd door gebruikersreferenties. Een kostenplaatsmanager mag alleen gegevens voor zijn eigen kostenplaats bekijken. De toegangsniveaubeveiliging wordt beheerd binnen de module Kostprijsboekhouding. Accountants definiëren het mobiele werkgebied voor kostenbeheer in de module Kostprijsboekhouding. Nadat het werkgebied is gepubliceerd naar de Microsoft Dynamics 365 for Operations-app, is het beschikbaar in de mobiele app van Dynamics 365 for Operations. Dit zorgt ervoor dat alle kostenplaatsmanagers in de organisatie gegevens in dezelfde indeling kunnen bekijken.

### <a name="actions-views-and-links"></a>Acties, weergaven en koppelingen

Het mobiele werkgebied voor kostenbeheer voor de Dynamics 365 for Operations-app biedt de volgende acties, weergaven en koppelingen:

-   Acties 
    -   Selecteer **Configuraties** om een indeling te selecteren.
    -   Selecteer **Kostenobjecten** om de kostenplaatsen te selecteren waarop u gegevens wilt filteren. **Opmerking:** de lijst wordt weergegeven op basis van de toegang die is verleend in de module Kostprijsboekhouding.

<!-- -->

-   Op basis van wat u hebt geselecteerd onder **Acties** en wat in de module Kostprijsboekhouding is geconfigureerd, kunt u de volgende informatie weergeven in de kaarten. Houd er rekening mee dat het bedrag wordt weergegeven in dezelfde indeling: Werkelijk, Budget, Afwijking en Afwijking in %. 
    -   Werkelijk versus budget (huidige periode)
    -   Werkelijk versus herzien budget (huidige periode)
    -   Werkelijk versus budget (vorige periode)
    -   Werkelijk versus herzien budget (vorig periode)
    -   Werkelijk versus budget (jaar tot heden)
    -   Werkelijk versus herzien budget (jaar tot heden)

<!-- -->

-   Koppelingen
    -   Details voor huidige periode.
    -   Details voor vorige periode.
    -   Details voor jaar tot heden.

Wanneer u een van de koppelingen selecteert, wordt een kaart per kostenelement weergegeven. Het bedrag in de kaarten wordt weergegeven in de volgende indeling: Werkelijk, Budget, Budgetafwijking, Budgetafwijking in %, Herzien budget, Herziene budgetafwijking en Herziene budgetafwijking in %.  [![Kostenbeheer](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Aan de slag
Voer de volgende stappen uit om aan de slag te gaan met de mobiele app voor kostenbeheer op uw mobiele apparaat.

1.  Download en installeer de app Microsoft Dynamics 365 for Operations via uw winkel voor mobiele apps.
2.  Start de app op uw apparaat.
3.  Voer uw Dynamics 365-URL in.
4.  Voer het bedrijf in waarbij u zich wilt aanmelden. Voer bijvoorbeeld **USMF** in.
5.  De eerste keer dat u zich aanmeldt, wordt u gevraagd om de gebruikersnaam en het wachtwoord voor uw Microsoft Dynamics 365 for Operations-account. Voer uw referenties in. Nadat u zich hebt aangemeld, ziet u de beschikbare werkgebieden voor uw bedrijf.

Als u werkgebieden op uw mobiele app wilt bekijken, moet u eerst de gewenste werkgebieden publiceren naar de Dynamics 365 for Operations-app.

1.  Start Dynamics 365 for Operations.
2.  Ga naar **Systeembeheer** &gt; **Instellen** &gt; **Systeemparameters**.
3.  Selecteer **Mobiele app beheren**.
4.  Selecteer het werkgebied Kostenbeheer voor publicatie naar het mobiele platform.
5.  Selecteer **Werkgebied publiceren**.
6.  Vernieuw uw apparaat om de gepubliceerde werkgebieden te zien.

## <a name="view-the-performance-of-your-cost-center"></a>De prestaties van uw kostenplaats weergeven
1.  Selecteer op uw mobiele apparaat het werkgebied **Kostenbeheer**.
2.  Selecteer **Kostenbeheer**.
3.  Klik op **Acties**.
4.  Klik op **Configuratie selecteren** om een indeling voor kostenbeheer te selecteren.
5.  Klik op **Gereed**.
6.  Klik op **Acties**.
7.  Klik op **Kostenobject selecteren** om de kostenplaatsen te selecteren waartoe u toegang hebt gekregen.
8.  Klik op **Gereed**.
9.  Geef de prestaties van uw kostenplaats weer.
10. Klik op **Details voor huidige periode**.
11. Geef de prestaties van afzonderlijke kostenelementen weer.
12. U kunt ook zoeken naar specifieke kostenelementen.



