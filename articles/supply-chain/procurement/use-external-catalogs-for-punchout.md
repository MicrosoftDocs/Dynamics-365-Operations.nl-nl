---
title: Externe catalogi gebruiken voor PunchOut eProcurement
description: In dit onderwerp wordt uitgelegd hoe u kunt externe catalogi maakt en inkoopopdrachten indient.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c345f1f8d1aaa93dbe02f1f8c53df63bf3488a9e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Externe catalogi gebruiken voor PunchOut eProcurement
Als u externe catalogi voor PunchOut eProcurement gebruikt, hoeft u geen gegevens over producten van uw leveranciers in uw eigen hoofdgegevens te beheren. In plaats daarvan wordt de winkelwagen op de website van de leverancier geconverteerd naar inkoopopdrachtregels met de juiste productinformatie. 

Zo vermijdt u dat u de beschrijvingen en prijzen van de producten van uw leveranciers in uw eigen producthoofdgegevens moet opslaan en onderhouden. In plaats daarvan gebruikt u externe catalogi voor PunchOut eProcurement. Wanneer werknemers dan inkoopopdrachten maken, kunnen ze "uitklokken" naar de externe catalogussite van een leverancier, dat wil zeggen dat ze uw systeem verlaten en naar de website van de leverancier gaan. De producten die worden toegevoegd aan de winkelwagen op de website van de leverancier, kunnen vervolgens worden geconverteerd naar inkoopopdrachtregels. U krijgt daarmee de juiste productinformatie: id, naam, prijs en andere gegevens van het product.

Als u externe catalogi wilt gebruiken, moet een werknemer een bestelopdracht maken op de pagina **Mijn opdrachten tot inkoop**.

De werknemer die een opdracht tot inkoop maakt, wordt de voorbereider van de inkoopopdracht genoemd. Als voorbereider kunt u de volgende taken uitvoeren:

De regelactie **Externe catalogi** gebruiken om een pagina te openen met alle externe catalogi die beschikbaar voor de opgegeven aanvrager zijn, kopende rechtspersoon en ontvangende operationele eenheid.

Afhankelijk van uw machtigingen, de aanvrager, kopende rechtspersoon en ontvangende operationele eenheid aanpassen. Een wijziging in deze waarden kan de lijst wijzigen met externe catalogi die beschikbaar voor een aanvrager zijn. Welke externe catalogi beschikbaar zijn, is afhankelijk van het huidige actieve inkoopbeleid voor de kopende rechtspersoon of de ontvangende operationele eenheid. Dit beleid kan toegang tot specifieke aanschaffingscategorieën toestaan of voorkomen. Daardoor kan de lijst met externe catalogi die zijn toegewezen aan deze inkoopcategorieën worden beïnvloed.

Zie voor meer informatie over het beleid het onderwerp [Inkoopbeleid](../procurement/purchase-policies.md).

- Voer tekst in het cataloguszoekveld in om externe catalogi voor specifieke inkoopcategorieën te vinden.
- Als u producten wilt toevoegen uit een externe leverancierscatalogus op de website van de leverancier, klikt u op de externe catalogus. Vervolgens voegt u producten toe aan de winkelwagen en checkt u ze uit. De winkelwagenregels worden overgebracht naar Microsoft Dynamics 365.

Als er meerdere opties voor aanschaffingscategorieën zijn, selecteert u de juiste aanschaffingscategorie voordat u de regels aan de inkoopopdracht toevoegt.
Nadat de regels zijn toegevoegd aan een inkoopopdracht, kunt u meer regels toevoegen zonder externe catalogi te hoeven gebruiken. U kunt ook doorgaan met het toevoegen van regels vanuit externe catalogi.

Wanneer de inkoopopdracht klaar is, gebruikt u de actie **Workflow** > **Verzenden** om de opdracht ter goedkeuring aan te bieden.

