---
title: Mobiel werkgebied Goedkeuring van facturen
description: Dit onderwerp biedt informatie over het mobiele werkgebied Goedkeuring van facturen. Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6c95c2779d996f489679c8dda4cda462ba0a05ac
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="invoice-approvals-mobile-workspace"></a>Mobiel werkgebied Goedkeuring van facturen

[!INCLUDE [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Goedkeuring van facturen**. Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur. 

Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Overzicht

In het mobiele werkgebied **Goedkeuring van facturen** kunnen medewerkers en managers van de afdeling Crediteuren facturen weergeven die zijn toegewezen aan hen als onderdeel van het workflowproces voor de koptekst van de leverancierfactuur. U kunt de factuurgegevens en zelfs de regel en distributiedetails weergeven, zodat u weloverwogen kunt besluiten over goedkeuring of afwijzing. Vanuit het werkgebied kunt u actie ondernemen om de factuur door het workflowproces te verplaatsen. 

## <a name="prerequisites"></a>Vereisten

Voordat u dit mobiele werkgebied kunt gebruiken, moet aan de volgende voorwaarden worden voldaan:

<table>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Finance and Operations moet zijn geïmplementeerd in uw organisatie.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="../deployment/deploy-demo-environment.md">Een demo-omgeving implementeren</a>
</td>
</tr>
<tr class="even">
<td>Het mobiele werkgebied <strong>Goedkeuring van facturen</strong> moet worden gepubliceerd.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Dynamics 365 for Unified Operations:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app

1.  Start de app op uw mobiele apparaat.
2.  Voer uw Microsoft Dynamics 365-URL in.
3.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
4.  Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

    [![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Facturen goedkeuren met behulp van het mobiele werkgebied Goedkeuring van facturen
1.  Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van facturen**.
2.  Selecteer de factuur die aan u is toegewezen door het workflowproces voor de koptekst van de leveranciersfactuur.
3.  Controleer op de pagina **Factuurdetails** de koptekstinformatie, zoals informatie over de leverancier en datum.
4.  Selecteer een regel op de factuur met meer gedetailleerde informatie over de factuur in de weergave **Details van factuurregel**.
5.  Selecteer in de weergave **Details van factuurregel** de waarde **Distributies** om de regeldistributies op te roepen. Hier kunt u de boekhouding voor de factuurregel weergeven. De getoonde informatie bevat de financiële dimensies en de hoofdrekening.
6.  Selecteer op de pagina **Factuurdetails** **Distributies** om alle distributies op te roepen. Hier kunt u de boekhouding voor de gehele factuur weergeven. De getoonde informatie bevat de financiële dimensies en de hoofdrekeningen. 
7.  Selecteer **Bijlagen** om eventuele notities of bestanden weer te geven, die zijn gekoppeld aan de factuur.
8.  Selecteer op de pagina **Factuurdetails** de juiste workflowactie uit om uw beoordelingsproces te voltooien.
9.  Selecteer **Gereed**.

