---
title: " Detailhandelsprijscorrecties"
description: Deze procedure doorloopt het maken van een prijscorrectie voor commerce.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7443f69473c0aad478d47f80f284b1156bad9c24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962980"
---
# <a name="retail-price-adjustments"></a> Detailhandelsprijscorrecties

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het maken van een prijscorrectie voor commerce. Een prijscorrectie kan de verkoopprijs van een artikel rechtstreeks instellen of de basisverkoopprijs of handelsovereenkomstverkoopprijs wijzigen. Deze procedure gebruikt het demobedrijf USRT.

1. Klik op Prijzen- en kortingsbeheer.
2. Klik op het tabblad Prijscorrecties.
3. Klik op Nieuw.
    * Van hieruit kunt u alle meest gangbare gebruikte prijs- en kortingregels maken, waaronder kortingen, prijscorrecties, handelsovereenkomstjournalen en categorieprijsregels.  
4. Klik op Prijscorrectie.
5. Typ een waarde in het veld Naam.
6. Vouw de sectie Regels uit.
7. Klik op Toevoegen.
    * Typ voor dit voorbeeld '81126' in het veld Product. Voer vervolgens '10.0' in het veld Kortingspercentage in.  
    * Een prijscorrectie van het type kortingspercentage verlaagt een basisverkoopprijs of een handelsovereenkomstverkoopprijs.  
8. Klik op Toevoegen.
    * Typ voor dit voorbeeld '81125' in het veld Product. Selecteer vervolgens 'Contantkortingsbedrag' in het veld Kortingsmethode.    Voer ten slotte '5.0' in het veld Contantkortingsbedrag in.  
    * Een korting van het type contantkortingsbedrag is een bedrag dat af wordt gehaald van een basisprijs of een handelsovereenkomstprijs.  
9. Klik op Prijsgroepen.
    * Selecteer 'RP-Houston' in het veld Prijsgroep.  
    * Hierdoor wordt de prijscorrectie gekoppeld aan de Houston-winkel.  
10. Klik op Opslaan.
11. Sluit de pagina.
12. Selecteer 'Ingeschakeld' in het veld Status.
13. Klik op Opslaan.
14. Sluit de pagina.
15. Vernieuw de pagina.

