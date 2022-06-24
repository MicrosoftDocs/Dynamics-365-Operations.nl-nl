---
title: Verlof inkopen en verkopen
description: In dit artikel wordt beschreven hoe u aanvragen indient voor het kopen en verkopen van verlof in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875708"
---
# <a name="buy-and-sell-leave"></a>Verlof inkopen en verkopen


>[!Important]
>De functionaliteit die in dit artikel wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Dynamics 365 Human Resources kunt u aanvragen voor het kopen en verkopen van verlof indienen op basis van het beleid voor kopen en verkopen dat is ingesteld door uw bedrijf.  

## <a name="request-to-buy-leave"></a>Aanvraag om verlof te kopen

1. Selecteer in het werkgebied **Selfservice werknemer** de optie **Aanvraag om verlof te kopen** op de tegel **Verlofsaldi**. 

2. Voeg een **verloftype** toe en voer in **hoeveel** verlof u wilt kopen. 

3. Selecteer **Indienen** wanneer u gereed bent om uw aanvraag in te dienen. 

Uw saldi worden vóór het bijwerken automatisch bijgewerkt of doorlopen een goedkeuringsproces. Dit is afhankelijk van hoe het koopbeleid is geconfigureerd.

## <a name="request-to-sell-leave"></a>Aanvraag om verlof te verkopen

1. Selecteer in de werkruimte **Selfservice werknemer** de optie **Aanvraag om verlof te verkopen** op de tegel **Verlofsaldi**. 

2. Voeg een **Verloftype** toe en voer een **Hoeveelheid** in voor de hoeveelheid verlof die u wilt verkopen. 

3. Selecteer **Indienen** wanneer u gereed bent om uw aanvraag in te dienen.

Uw saldi worden vóór het bijwerken automatisch bijgewerkt of doorlopen een goedkeuringsproces. Dit is afhankelijk van hoe het koopbeleid is geconfigureerd.


## <a name="troubleshooting"></a>Problemen oplossen 

Als een workflow voor verlofaanvragen voor kopen of verkopen mislukt, kunnen gebruikers met de bevoegdheid **EssLebugBuyBugRequestApprover** het berichtenlogboek controleren voor alle verlofaanvragen voor kopen en verkopen. Hiervoor gaat u naar **Verlof en verzuim > Koppelingen > Verlofaanvragen kopen en verkopen > Berichtenlogboek** (linksboven). Gebruikers kunnen in **Berichtenlogboek** zien hoe de transacties werden verwerkt en de bijbehorende workflowhistorie wordt getoond.


## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)</br>
[Beleid voor verlof inkopen/verkopen beheren](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
