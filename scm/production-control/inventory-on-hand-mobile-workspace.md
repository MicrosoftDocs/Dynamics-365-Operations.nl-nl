---
title: Mobiel werkgebied voor voorhanden voorraad voor de app Microsoft Dynamics 365 for Operations
description: Met het mobiele werkgebied voor voorhanden voorraad kunt u altijd en overal mobiele inzichten verkrijgen in gereserveerde en beschikbare voorraad.
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiel werkgebied voor voorhanden voorraad voor de app Microsoft Dynamics 365 for Operations

Met het mobiele werkgebied voor voorhanden voorraad kunt u altijd en overal mobiele inzichten verkrijgen in gereserveerde en beschikbare voorraad. 

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                         | Omschrijving                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Meer informatie over het mobiele platform van Microsoft Dynamics 365 for Operations | [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Een omgeving met Microsoft Dynamics 365 for Operations versie 1611 en Microsoft Dynamics 365 for Operations-platform update 3 (november 2016) |
| Hotfix KB 3215650                                                    | Installeer de hotfix om de werkgebieden in te schakelen die beschikbaar zijn in uw Microsoft Dynamics 365 for Operations.                                       |
| Mobiel apparaat waarop de Dynamics 365 for Operations-app is geïnstalleerd | Download de Dynamics 365 for Operations-app van uw winkel voor mobiele apps.                                                                           |

## <a name="introduction"></a>Introductie
Normaal gesproken hebben bedrijven elke dag meerdere verzendingen en meerdere ontvangsten van voorraad. Deze verplaatsingen veranderen voortdurend de status van de voorhanden voorraad. Met het mobiele werkgebied voor voorhanden voorraad kunt u de status van de voorhanden voorraad voor meerdere bedrijven bekijken, zodat u de meest recente inzichten in de voorraadgegevens op het mobiele apparaat van uw keuze kunt verkrijgen. Ongeacht of u werkzaam bent in het magazijn of voor inkoop, verkoop, productie of beheer of andere rollen vervult, u hebt altijd en overal toegang tot de gegevens over de voorhanden voorraad. Het mobiele werkgebied biedt een direct overzicht van de voorhanden status van de verschillende vestigingen en u kunt voorhanden voorraad in de verschillende opslagruimten, huidige materiaalreserveringen en niet-gereserveerde voorhanden voorraad bekijken. U kunt ook artikelnummers invoeren om te zoeken in voorhanden voorraad en een gefilterde zoekopdracht uit te voeren naar voorhanden producten of varianten. Het mobiele werkgebied biedt vooral de volgende functies:

-   U kunt zoeken op productnummer of productnaam om producten te vinden waarvoor u de status van de voorhanden voorraad wilt weergeven.
-   Voor de geselecteerde producten kunt u de volgende informatie weergeven:
    -   Voorhanden voorraad per vestiging
    -   Voorhanden voorraad per magazijn
    -   Voorhanden voorraad per locatie
    -   Voorhanden voorraad per batch (voor batchproducten)
    -   Voorhanden voorraad per voorraadstatus

<!-- -->

-   Voorhanden voorraad van producten wordt weergegeven op de volgende manieren:
    -   Op basis van fysieke voorraad (deze weergave geeft de totale hoeveelheid.)
    -   Op basis van fysieke gereserveerde voorraad (deze weergave geeft de gereserveerde hoeveelheid.)
    -   Op basis van fysieke beschikbare voorraad (deze weergave geeft de beschikbare hoeveelheid waarvoor geen reserveringen zijn.)

## <a name="get-started"></a>Aan de slag
Aan de slag op uw mobiele telefoon:

1.  Download en installeer de app Microsoft Dynamics 365 for Operations via uw store voor mobiele apps.
2.  Start de app op uw apparaat.
3.  Voer uw Dynamics 365-URL in.
4.  Voer het bedrijf in waarbij u zich wilt aanmelden. Voer bijvoorbeeld **USMF** in.
5.  De eerste keer dat u zich aanmeldt, wordt u gevraagd om de gebruikersnaam en het wachtwoord voor uw Microsoft Dynamics 365 for Operations-account. Voer uw referenties in. Nadat u zich hebt aangemeld, ziet u de beschikbare werkgebieden voor uw bedrijf.

Als u werkgebieden op uw mobiele app wilt bekijken, moet u eerst de gewenste werkgebieden publiceren naar de Dynamics 365 for Operations-app.

1.  Start Dynamics 365 for Operations.
2.  Ga naar **Systeembeheer** &gt; **Instellen** &gt; **Systeemparameters**.
3.  Selecteer **Mobiele app beheren**.
4.  Selecteer het werkgebied voor publicatie naar het mobiele platform.
5.  Selecteer **Werkgebied publiceren**.
6.  Vernieuw uw apparaat om de gepubliceerde werkgebieden te zien.

## <a name="view-the-onhand-inventory-for-a-product"></a>Voorhanden voorraad voor een product weergeven
1.  Selecteer op uw mobiele apparaat het werkgebied **Voorhanden voorraad**.
2.  Selecteer **Voorhanden voorraad voor een artikel controleren**. U ziet een lijst van de producten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar u kunt dit aantal wijzigen. Zie het vooraf gelezen handboek voor meer informatie.
3.  Als uw artikel niet in de lijst staat, selecteert u **Meer zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op productnummer of schakel over naar een zoekopdracht op productnaam.
4.  Selecteer een product. Als het artikel een afbeelding heeft, wordt de afbeelding weergegeven.
5.  Selecteer een van de volgende opties om de status van de voorhanden voorraad weer te geven:
    -   Voorhanden voorraad per vestiging weergeven
    -   Voorhanden voorraad per magazijn weergeven
    -   Voorhanden voorraad per locatie weergeven
    -   Voorhanden voorraad per batch (voor batchproducten) weergeven
    -   Voorhanden voorraad per voorraadstatus weergeven

    Voorhanden voorraad van producten wordt weergegeven op de volgende manieren:
    -   Op basis van fysieke voorraad (deze weergave geeft de totale hoeveelheid.)
    -   Op basis van fysieke gereserveerde voorraad (deze weergave geeft de gereserveerde hoeveelheid.)
    -   Op basis van beschikbare fysieke voorraad (deze weergave geeft de beschikbare hoeveelheid waarvoor geen reserveringen zijn.)




