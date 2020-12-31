---
title: Mobiel werkgebied Goedkeuring van facturen
description: Dit onderwerp biedt informatie over het mobiele werkgebied Goedkeuring van facturen. Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8d4b40c7ce8939248e85b6b6f3d359bd16e35b0d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683403"
---
# <a name="invoice-approvals-mobile-workspace"></a>Mobiel werkgebied Goedkeuring van facturen

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Goedkeuring van facturen**. Dit werkgebied geeft een lijst met facturen die aan u zijn toegewezen via het workflowproces voor de koptekst van de leveranciersfactuur. 

Dit mobiele werkgebied is bedoeld om samen te worden gebruikt met de mobiele app van Finance and Operations.

## <a name="overview"></a>Overzicht

In het mobiele werkgebied **Goedkeuring van facturen** kunnen medewerkers en managers van de afdeling Crediteuren facturen weergeven die zijn toegewezen aan hen als onderdeel van het workflowproces voor de koptekst van de leverancierfactuur. U kunt de factuurgegevens en zelfs de regel en distributiedetails weergeven, zodat u weloverwogen kunt besluiten over goedkeuring of afwijzing. Vanuit het werkgebied kunt u actie ondernemen om de factuur door het workflowproces te verplaatsen. 

## <a name="prerequisites"></a>Vereisten

Voordat u dit mobiele werkgebied kunt gebruiken, moet aan de volgende voorwaarden worden voldaan:

<table>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance moet worden geïmplementeerd in uw organisatie.</td>
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

Download en installeer de mobiele Finance and Operations-app:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app

1.  Start de app op uw mobiele apparaat.
2.  Voer uw URL voor Microsoft Dynamics 365 in.
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
