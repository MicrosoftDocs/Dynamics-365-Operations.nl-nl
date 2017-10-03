---
title: Gebruikersbeveiliging leveranciersportal
description: In dit artikel wordt beschreven hoe u beveiliging instelt voor externe leveranciers die de leveranciersportal gebruiken. Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 560e0760c33cab4186095ac2ae7e105d75cc16d0
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017

---

# <a name="vendor-portal-user-security"></a>Gebruikersbeveiliging leveranciersportal

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u beveiliging instelt voor externe leveranciers die de leveranciersportal gebruiken. Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.

De functionaliteit Leveranciersportal is vervangen door de verbeterde functionaliteit voor leverancierssamenwerking in Dynamics 365 for Operations versie 1611. Meer informatie over het instellen van beveiliging voor leverancierssamenwerking vindt u in [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md). De leveranciersportal maakt een beperkte set informatie over inkooporders (IOs) beschikbaar voor externe leveranciers. Het is belangrijk dat u correct de machtigingen van gebruikers instelt voor de leveranciersportal in Microsoft Dynamics AX, zodat leveranciers geen onbedoelde toegang tot extra informatie in uw Dynamics AX-installatie hebben. **Belangrijk:** In tegenstelling tot andere gebruikers moeten externe leveranciers niet de rol **SystemUser** hebben. De rol **SystemUser** geeft toegang tot een set bevoegdheden die niet geschikt zijn voor externe gebruikers.

## <a name="setting-up-a-vendor-portal-user"></a>Het instellen van een Leveranciersportal-gebruiker
Voordat u een gebruikersaccount maakt voor iemand die de leveranciersportal zal gebruiken, moet u de leverancier instellen op leveranciersportalsamenwerking. Gebruik het veld **Inkoopordersamenwerking** op het tabblad **Algemeen** op de pagina **Leveranciers**. Externe leveranciers die de leveranciersportal gebruiken, moeten de volgende instelling hebben:

-   Een Microsoft Azure-Active Directory-gebruikersaccount moet worden geregistreerd voor de leverancier op de pagina **Gebruikers** in Dynamics AX.
-   De leverancier moet de beveiligingsrol **Leverancier (extern)** hebben, niet de rol **SystemUser**. **Opmerking:** De rol **SystemUser** wordt automatisch verleend als u een nieuw gebruikersaccount in Dynamics AX maakt. Daarom moet u die rol verwijderen en het waarschuwingsbericht bevestigen dat u ontvangt.
-   De leveranciersgebruiker mag geen toestemming geven voor het toevoegen van extra velden vanuit de inkoopordertabellen aan hun weergave van de inkooporder. Op het **Persoonlijke instellingen** tabblad, op het **Gebruikers** tabblad, stelt u de optie **Expliciete aanpassing toegestaan** voor de gebruiker in op **Nee**.
-   De gebruikersaccount moet zijn gekoppeld aan een geregistreerde contactpersoon. Op de **Gebruikers** pagina, selecteert u een contactpersoon in het **Naam** veld. De persoon die u selecteert moet de rol **Contactpersoon** hebben voor de relevante leverancier.

Als dezelfde persoon toegang nodig heeft tot de Leveranciersportal voor meerdere leverancierrekeningen (voor verschillende rechtspersonen misschien), moet elk van de gebruikersrekeningen van die persoon met dezelfde geregistreerde contactpersoon zijn gekoppeld. De rol **Leverancier (extern)** bevat alle basismogelijkheden die zijn vereist om de functionaliteit te gebruiken die in de leveranciersportal beschikbaar is. Deze instellingen helpen waarborgen dat de gebruikersinterface die de externe gebruiker ziet uitsluitend is gericht op het beoogde scenario.

<a name="see-also"></a>Zie ook
--------

[Leverancierssamenwerking](collaborate-vendors-vendor-portal.md)



