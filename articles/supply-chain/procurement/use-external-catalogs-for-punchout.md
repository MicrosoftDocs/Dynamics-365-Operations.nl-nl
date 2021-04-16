---
title: Externe catalogi gebruiken voor PunchOut eProcurement
description: In dit onderwerp wordt uitgelegd hoe u kunt externe catalogi maakt en inkoopopdrachten indient.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a839f672454105871a101c190ee87d701e58db4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811057"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Externe catalogi gebruiken voor PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Als u externe catalogi voor PunchOut eProcurement gebruikt, hoeft u geen gegevens over producten van uw leveranciers in uw eigen hoofdgegevens te beheren. In plaats daarvan wordt de winkelwagen op de website van de leverancier geconverteerd naar inkoopopdrachtregels met de juiste productinformatie. 

Zo vermijdt u dat u de beschrijvingen en prijzen van de producten van uw leveranciers in uw eigen producthoofdgegevens moet opslaan en onderhouden. In plaats daarvan gebruikt u externe catalogi voor PunchOut eProcurement. Wanneer werknemers dan inkoopopdrachten maken, kunnen ze "uitklokken" naar de externe catalogussite van een leverancier, dat wil zeggen dat ze uw systeem verlaten en naar de website van de leverancier gaan. De producten die worden toegevoegd aan de winkelwagen op de website van de leverancier, kunnen vervolgens worden geconverteerd naar inkoopopdrachtregels. U krijgt daarmee de juiste productinformatie: id, naam, prijs en andere gegevens van het product.

Als u externe catalogi wilt gebruiken, moet een werknemer een bestelopdracht maken op de pagina **Mijn opdrachten tot inkoop**.

De werknemer die een opdracht tot inkoop maakt, wordt de voorbereider van de inkoopopdracht genoemd. Als voorbereider kunt u de volgende taken uitvoeren:

De regelactie **Externe catalogi** gebruiken om een pagina te openen met alle externe catalogi die beschikbaar voor de opgegeven aanvrager zijn, kopende rechtspersoon en ontvangende operationele eenheid.

Afhankelijk van uw machtigingen, de aanvrager, kopende rechtspersoon en ontvangende operationele eenheid aanpassen. Een wijziging in deze waarden kan de lijst wijzigen met externe catalogi die beschikbaar voor een aanvrager zijn. Welke externe catalogi beschikbaar zijn, is afhankelijk van het huidige actieve inkoopbeleid voor de kopende rechtspersoon of de ontvangende operationele eenheid. Dit beleid kan toegang tot specifieke aanschaffingscategorieën toestaan of voorkomen. Daardoor kan de lijst met externe catalogi die zijn toegewezen aan deze inkoopcategorieën worden beïnvloed.

Zie voor meer informatie over het beleid het onderwerp [Overzicht van Aanschafbeleid](../procurement/purchase-policies.md).

- Voer tekst in het cataloguszoekveld in om externe catalogi voor specifieke inkoopcategorieën te vinden.
- Als u producten wilt toevoegen uit een externe leverancierscatalogus op de website van de leverancier, klikt u op de externe catalogus. Vervolgens voegt u producten toe aan de winkelwagen en checkt u ze uit. De winkelwagenregels worden overgebracht naar Microsoft Dynamics 365.

Als er meerdere opties voor aanschaffingscategorieën zijn, selecteert u de juiste aanschaffingscategorie voordat u de regels aan de inkoopopdracht toevoegt.
Nadat de regels zijn toegevoegd aan een inkoopopdracht, kunt u meer regels toevoegen zonder externe catalogi te hoeven gebruiken. U kunt ook doorgaan met het toevoegen van regels vanuit externe catalogi.

Wanneer de inkoopopdracht klaar is, gebruikt u de actie **Workflow** > **Verzenden** om de opdracht ter goedkeuring aan te bieden.

### <a name="additional-resources"></a>Aanvullende bronnen

- [Een externe catalogus instellen voor PunchOut eProcurement](set-up-external-catalog-for-punchout.md)
- [Verbeteringen inkoop-cXML](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]