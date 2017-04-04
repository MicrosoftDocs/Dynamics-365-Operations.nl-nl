---
title: Een model voor productconfiguratie instellen
description: In dit artikel worden de stappen beschreven voor het maken en instellen van een productconfiguratiemodel.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e7138dcc15cb8e16ad5cee83b40ba72555d89e6a
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-product-configuration-model"></a>Een model voor productconfiguratie instellen

In dit artikel worden de stappen beschreven voor het maken en instellen van een productconfiguratiemodel.

| Taak                                                        | Omschrijving                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maak een productmodel.                                    | Maak een productmodel vanuit de lijst **Productmodel**. Het productmodel op alle relevante bedrijven vrijgeven. Voor een productmodel dat wordt gebruikt als een versie voor een productconfiguratiemodel of als een subonderdeel **beperkingen gebaseerde configuratie** moet worden ingeschakeld omdat de configuratietechnologie en de configuratiedimensie moet alleen worden geselecteerd voor de productdimensiegroep. |
| Maak onderdelen.                                          | Maak onderdelen op de pagina **Onderdelen**. Onderdelen zijn de bouwstenen van een productconfiguratiemodel en kunnen opnieuw worden gebruikt in meerdere productconfiguratiemodellen.                                                                                                                                                                                                                      |
| Maak kenmerktypen.                                     | Maak kenmerktypen op de pagina **Kenmerktypen**. Kenmerktypen bepalen de reeks gegevenstypen voor alle kenmerken die worden gebruikt in productconfiguratiemodellen. De kenmerken van **Booleaans**, **Tekst** met een vaste lijst en **Geheel getal** met een bereik geven de reeks waarden aan die beschikbaar zijn wanneer u een productvariant configureert op basis van een productconfiguratiemodel.       |
| Maak een productconfiguratiemodel.                       | Maak een productconfiguratiemodel op de pagina **Nieuw productconfiguratiemodel**.                                                                                                                                                                                                                                                                                                              |
| Voeg kenmerken toe aan een productconfiguratiemodel.            | Maak een kenmerk op het sneltabblad **Kenmerken** op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel**. Kenmerken beschrijven de functies van het productconfiguratiemodel.                                                                                                                                                                                                       |
| Voeg beperkingen toe aan een productconfiguratiemodel.           | Maak beperkingen op het sneltabblad **Beperkingen** op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel**. Beperkingen zijn voorwaarden waaraan een productconfiguratiemodel moet voldoen. Er zijn twee typen beperkingen: expressiebeperkingen en tabelbeperkingen.                                                                                                                                 |
| Voeg subonderdelen toe aan een productconfiguratiemodel.         | Maak subonderdelen op het sneltabblad **Subonderdelen** op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel**. Subonderdelen hebben betrekking op onderdelen en zijn gekoppeld aan artikelen die het subonderdeel vertegenwoordigen.                                                                                                                                                                       |
| Voeg gebruikersbehoeften toe aan een productconfiguratiemodel.     | Gebruikersbehoeften zijn vergelijkbaar met subonderdelen, maar zij verwijzen niet naar een artikel. U kunt gebruikersbehoeften zien als een phantom-stuklijst. Alle stuklijstregels of routebewerkingen die direct onder de gebruikersbehoefte zijn geplaatst, worden in het bovenliggende onderdeel samengevouwen.                                                                                                                       |
| Voeg stuklijstregels toe aan een productconfiguratiemodel.             | Maak stuklijstregels op het sneltabblad **Stuklijstregels** op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel**. Stuklijstregels vertegenwoordigen een deel dat nodig is om een variant van het product te bouwen.                                                                                                                                                                                                 |
| Voeg routebewerkingen toe aan een productconfiguratiemodel.      | Maak routebewerkingen op het sneltabblad **Routebewerkingen** op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel**. Routebewerkingen vertegenwoordigen een stap in een reeks stappen die worden uitgevoerd om een variant van het product te maken.                                                                                                                                                    |
| Maak een actieve versie voor een productconfiguratiemodel. | Maak een actieve versie van het productconfiguratiemodel op de pagina **Versies**. Een versie is de relatie tussen een productconfiguratiemodel en het productmodel Een productconfiguratiemodel dat een actieve versie heeft, kan worden geconfigureerd vanuit een verkooporder, verkoopofferte, inkooporder of productieorder.                                                               |
| Test een productconfiguratiemodel.                         | Test het productconfiguratiemodel vanaf de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel** of de pagina **Productconfiguratiemodellenlijst**. Het testen van de productconfiguratiemodellen stimuleert het configuratieproces van het productiemodel dat plaatsvindt tijdens de orderverwerking.                                                                                                |
| Maak een productconfiguratiemodelsjabloon.                | Maak een sjabloon voor een productconfiguratiemodel op de pagina **Configuratiesjablonen**. Een configuratiesjabloon bevat waarden voor kenmerken in het productconfiguratiemodel. Selecteer de kenmerkwaarden op de pagina **Regel configureren**. U kunt het laden van een productconfiguratiemodelsjabloon selecteren tijdens het configuratieproces van het productmodel.                                                   |
| Configureer een artikel.                                          | Productconfiguratiemodellen kunnen worden geconfigureerd vanuit een verkooporder, verkoopofferte, inkooporder of een productieorder.                                                                                                                                                                                                                                                                           |




