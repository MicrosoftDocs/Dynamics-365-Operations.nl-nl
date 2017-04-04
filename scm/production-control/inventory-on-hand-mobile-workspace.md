---
title: Mobiele werkruimte voorhanden voorraad voor Microsoft Dynamics 365 voor bewerkingen app
description: De voorraad voorhanden mobiele werkruimte kunt u mobiele inzicht in de gereserveerde en beschikbare voorraad krijgen altijd en overal.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiele werkruimte voorhanden voorraad voor Microsoft Dynamics 365 voor bewerkingen app

De voorraad voorhanden mobiele werkruimte kunt u mobiele inzicht in de gereserveerde en beschikbare voorraad krijgen altijd en overal. 

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                         | Omschrijving                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Meer informatie over de Microsoft Dynamics 365 voor bewerkingen mobiel platform | [Dynamics 365 voor bewerkingen mobiel platform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Een omgeving met Microsoft Dynamics 365 voor bewerkingen versie 1611 en Microsoft Dynamics voor bewerkingen platform bijwerken (November 2016) 3 |
| Hotfix KB 3215650                                                    | Installeer de hotfix zodat de werkruimten die beschikbaar zijn in uw Microsoft Dynamics 365 voor bewerkingen.                                       |
| Mobiel apparaat met de Dynamics 365 for Operations app geïnstalleerd | De Dynamics 365 for Operations app downloaden van uw winkel mobiele app.                                                                           |

## <a name="introduction"></a>Introductie
Normaal gesproken hebben bedrijven meerdere verzendingen en meerdere ontvangsten van de voorraad elke dag. Deze verplaatsingen wijzigen voortdurend de status van de voorhanden voorraad. De voorraad voorhanden mobiele werkruimte kunt u de status van de voorhanden voorraad voor meerdere bedrijven, zodat u de meest recente inzicht te krijgen in de voorraadgegevens op het mobiele apparaat van uw keuze kunt krijgen. Ongeacht of u werkt in het magazijn, inkoop, verkoop, productie of management of andere functies hebben, opent u de gegevens van de voorhanden voorraad altijd en overal. De mobiele werkruimte biedt een duidelijk overzicht van de voorhanden status op faciliteiten en kunt u voorhanden voorraad in opslagruimten, huidige materiaal reserveringen en niet-gereserveerde voorraad bekijken. U kunt ook invoeren van artikelnummers aan query voorhanden voorraad en gefilterde gezocht naar voorhanden producten of varianten. De mobiele werkruimte biedt vooral deze functies:

-   U kunt zoeken door een productnummer of productnaam klikken om te zoeken naar producten om de status van de voorhanden voorraad voor weer te geven.
-   U kunt de volgende informatie weergeven voor de geselecteerde producten:
    -   Voorhanden voorraad per locatie
    -   Voorhanden voorraad per magazijn
    -   Voorhanden voorraad per locatie
    -   Voorhanden voorraad per batch (voor batch geregeld producten)
    -   Voorhanden voorraad per voorraadstatus

<!-- -->

-   Product voorhanden voorraad wordt weergegeven in de volgende manieren:
    -   Door de fysieke voorraad (deze weergave geeft het totale bedrag.)
    -   Door fysiek gereserveerd (deze weergave geeft het bedrag van de gereserveerde.)
    -   Door fysiek beschikbaar (deze weergave vertegenwoordigt beschikbaar bedrag dat geen reserveringen is.)

## <a name="get-started"></a>Aan de slag
Aan de slag op je mobiele telefoon:

1.  Van uw winkel mobiele app downloaden en installeren van de Microsoft Dynamics 365 voor bewerkingen app.
2.  Start de toepassing op het apparaat.
3.  De URL van uw Dynamics 365 invoeren.
4.  Voer in het bedrijf aan te melden. Voer bijvoorbeeld **USMF**.
5.  De eerste keer dat u zich aanmeldt, u gevraagd om de gebruikersnaam en wachtwoord voor uw Microsoft Dynamics 365 voor rekening van de bewerkingen. Uw referenties invoeren. Nadat u zich hebt aangemeld, ziet u de beschikbare werkruimten voor uw bedrijf.

Om werkruimten op uw mobiele app bekijkt, moet u eerst de gewenste werkruimten publiceren naar de Dynamics 365 voor bewerkingen app.

1.  Start de Dynamics 365 voor bewerkingen.
2.  Ga naar **Systeembeheer**&gt;**Setup**&gt;**systeemparameters**.
3.  Selecteer **mobiele app beheren**.
4.  Selecteer de werkruimte voor het publiceren naar het mobiele platform.
5.  Selecteer **publiceren werkruimte**.
6.  Het apparaat om te zien van de gepubliceerde werkruimten vernieuwen.

## <a name="view-the-onhand-inventory-for-a-product"></a>De voorhanden voorraad voor een product weergeven
1.  Selecteer op het mobiele apparaat, de **voorhanden voorraad** werkruimte.
2.  Selecteer **voorhanden voor een artikel controleren**. U overzicht een van de producten die in uw app voor gebruik offline worden geladen. Standaard 50 artikelen worden geladen, maar u kunt dit nummer wijzigen. Zie het vooraf gelezen handbook voor meer informatie.
3.  Als uw object niet in de lijst, selecteert u **zoeken meer** doen van een online zoeken in Dynamics 365 voor bewerkingen. Zoeken op productnummer of kiest u een zoekopdracht op productnaam.
4.  Selecteer een product. Als het artikel een afbeelding heeft, wordt de afbeelding weergegeven.
5.  Selecteer een van de volgende opties om de status van de voorhanden voorraad weer te geven:
    -   Voorhanden voorraad per locatie weergeven
    -   Voorhanden voorraad per magazijn weergeven
    -   Voorhanden voorraad per vestiging weergeven
    -   Weergave voorhanden voorraad per batch (voor batch geregeld producten)
    -   Voorhanden voorraad per voorraadstatus weergeven

    Product voorhanden voorraad wordt weergegeven in de volgende manieren:
    -   Door de fysieke voorraad (deze weergave geeft het totale bedrag.)
    -   Door fysiek gereserveerd (deze weergave geeft het bedrag van de gereserveerde.)
    -   Door fysiek beschikbaar (deze weergave geeft het beschikbare bedrag dat geen reserveringen is.)




