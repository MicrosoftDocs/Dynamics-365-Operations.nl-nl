---
title: Controle over mobiele werkruimte voor Microsoft Dynamics 365 kosten voor bewerkingen app
description: De kosten informatie mobiele werkruimte center managers kosten beheren over de prestaties van de kostenplaats kosten altijd en overal.
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Controle over mobiele werkruimte voor Microsoft Dynamics 365 kosten voor bewerkingen app

De kosten informatie mobiele werkruimte center managers kosten beheren over de prestaties van de kostenplaats kosten altijd en overal. 

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                         | Omschrijving                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Meer informatie over de Microsoft Dynamics 365 voor bewerkingen mobiel platform | [Dynamics 365 voor bewerkingen mobiel platform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Zorg ervoor dat u gebruikt een omgeving met Microsoft Dynamics 365 voor bewerkingen versie 1611 en Microsoft Dynamics voor bewerkingen platform 3 (November 2016) bijwerken. |
| Hotfix KB 3215650                                                    | Installeer de hotfix zodat de werkruimten die beschikbaar zijn in Microsoft Dynamics 365 voor bewerkingen.                                                                       |
| Mobiel apparaat met de Dynamics 365 for Operations app geïnstalleerd | De Dynamics 365 for Operations app downloaden van uw winkel mobiele app.                                                                                                      |

## <a name="introduction"></a>Introductie
De kosten voor het beheren van mobiele werkruimte biedt een duidelijk overzicht van de huidige prestaties van kostenplaatsen door werkelijke kosten ten opzichte van de gebudgetteerde kosten te vergelijken. U kunt inzoomen op status van afzonderlijke kostenelementen te betrekken.

### <a name="example"></a>Voorbeeld

Een werknemer ontvangt een uitnodiging voor een internationale conferentie. De organisatie moet dekken de reiskosten. De werknemer gevraagd zijn Manager als hij de vergadering kan bijwonen. De manager opent snel de kosten voor het beheren van mobiele werkruimte op de mobiele telefoon of hij het budget voor de werknemer voor het bijwonen van de vergadering heeft.

### <a name="data-security"></a>Gegevensbeveiliging

De gegevens in de werkruimte beheren kosten wordt gedekt door de gebruikersreferenties. Een manager kosten center is alleen toegestaan om gegevens voor zijn eigen kostenplaats te bekijken. De recordbeveiliging toegang wordt beheerd in de kostprijsboekhoudingmodule. Kosten accountants definiëren de kosten voor het beheren van voor mobiele Werkruimteconfiguratie in de kostprijsboekhoudingmodule. Nadat de werkruimte op de Microsoft Dynamics 365 voor bewerkingen app wordt gepubliceerd, is beschikbaar in de Dynamics 365 voor bewerkingen mobiele toepassing. Dit zorgt ervoor dat alle kosten center managers in de organisatie gegevens in dezelfde indeling wilt bekijken.

### <a name="actions-views-and-links"></a>Acties, weergaven en koppelingen

De kosten mobiele werkruimte beheren voor Dynamics 365 voor bewerkingen app biedt de volgende acties, weergaven en koppelingen:

-   Acties 
    -   Selecteer **configuraties** te halen van een indeling.
    -   Selecteer **kostenobjecten** aan de kostenplaatsen waarop u filtergegevens wilt verzamelen. **opmerking:** de lijst wordt weergegeven op basis van de toegang is verleend in de kostprijsboekhoudingmodule.

<!-- -->

-   Op basis van wat u hebt geselecteerd onder **acties** en wat in de kostprijsboekhoudingmodule is geconfigureerd, kunt u de volgende informatie kunt weergeven in de kaarten. Houd er rekening mee dat het bedrag wordt weergegeven in dezelfde indeling: werkelijke, budget, afwijking en de afwijking %. 
    -   Werkelijk vs. Budget (huidige periode)
    -   Werkelijk vs. herzien budget (huidige periode)
    -   Werkelijk vs. Budget (voorgaande periode)
    -   Werkelijk vs. herzien budget (voorgaande periode)
    -   Werkelijk vs. Budget (jaar tot heden)
    -   Werkelijk vs. herzien budget (jaar tot heden)

<!-- -->

-   Koppelingen
    -   Details voor de huidige periode.
    -   Details van vorige periode.
    -   De details van jaar tot heden.

Wanneer u een van de koppelingen selecteert, wordt een kaart per kostenelement weergegeven. Het bedrag in de kaarten wordt weergegeven in de volgende indeling: werkelijk, budget, budgetafwijking, budget afwijking % herzien budget, herzien budgetafwijking en herzien budget afwijking %.  [![kosten beheren](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Aan de slag
Volg deze stappen aan de slag met behulp van de mobiele app voor kosten-besturingselement op het mobiele apparaat.

1.  In uw winkel mobiele app downloaden en installeren van de Microsoft Dynamics 365 voor bewerkingen app.
2.  Start de toepassing op het apparaat.
3.  De URL van uw Dynamics 365 invoeren.
4.  Voer in het bedrijf aan te melden. Voer bijvoorbeeld **USMF**.
5.  De eerste keer dat u zich aanmeldt, u gevraagd om de gebruikersnaam en wachtwoord voor uw Microsoft Dynamics 365 voor rekening van de bewerkingen. Uw referenties invoeren. Nadat u zich hebt aangemeld, ziet u de beschikbare werkruimten voor uw bedrijf.

Om werkruimten op uw mobiele app bekijkt, moet u eerst de gewenste werkruimten publiceren naar de Dynamics 365 voor bewerkingen app.

1.  Start de Dynamics 365 voor bewerkingen.
2.  Ga naar **Systeembeheer**&gt;**Setup**&gt;**systeemparameters**.
3.  Selecteer **mobiele app beheren**.
4.  Selecteer de werkruimte ** kosten beheren ** publiceren naar het mobiele platform.
5.  Selecteer **publiceren werkruimte**.
6.  Het apparaat om te zien van de gepubliceerde werkruimten vernieuwen.

## <a name="view-the-performance-of-your-cost-center"></a>De prestaties van de kostenplaats weergeven
1.  Selecteer op het mobiele apparaat, de **kosten beheren** werkruimte.
2.  Selecteer **object besturen kosten**.
3.  Klik op **acties**.
4.  Klik op **Select configuration** kosten beheren indeling selecteren.
5.  Click **Done**.
6.  Klik op **acties**.
7.  Klik op **kostenplaats selecteren** aan kostenplaatsen waartoe u toegang hebben gekregen.
8.  Click **Done**.
9.  De algehele prestaties van de kostenplaats weergeven.
10. Klik op **de Details van de huidige periode**.
11. De prestaties van afzonderlijke kostenelementen weergeven.
12. U kunt ook zoeken voor bepaalde kostenelementen te betrekken.



