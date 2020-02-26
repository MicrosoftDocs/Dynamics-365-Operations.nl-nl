---
title: Kredietgroepen van klant
description: Dit onderwerp bevat informatie over kredietgroepen van klant.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015176"
---
# <a name="customer-credit-groups"></a>Kredietgroepen van klant

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

U kunt groepen klanten definiëren die dezelfde kredietlimiet hebben. Er wordt ook rekening gehouden met de individuele kredietlimiet die is gedefinieerd voor de rekening van de klantfactuur.

Leden van een kredietgroep van klant kunnen uit verschillende rechtspersonen worden geselecteerd. Wanneer u een klant aan de lijst met klanten in de kredietgroep van de klant toevoegt, verandert de vervaldatum van de kredietlimiet voor elke klant in de vervaldatum die is toegewezen aan de groep.

U kunt kredietgroepen van klant instellen op de pagina **Kredietgroepen van klant** (**Kredietbeheer \> Kredietgroepen van klant \> Kredietgroepen van klant**).

1. Voer in de velden **Groepsnummer** en **Beschrijving** een id en beschrijving voor de groep in.
2. Voer in de velden **Kredietlimiet** en **Valuta** de kredietlimiet en valuta in die moeten worden gebruikt wanneer het systeem de kredietlimiet voor een lid van de groep controleert.
3. Voer in het veld **Kredietlimiet tot datum** de datum in waarop de kredietlimiet vervalt. Kredietgroepen van klant moeten een vervaldatum hebben.

Wanneer u klaar bent met het instellen van een kredietgroep van klant, kunt u er klanten aan toevoegen door hun rechtspersoon en klantrekening-id op te geven. Wanneer u een nieuwe klant toevoegt aan een kredietgroep van klant, zoekt het systeem in alle rechtspersonen naar dezelfde klantrekening en wordt u gevraagd of u deze wilt toevoegen aan de kredietgroep van klant.

Gebruik het menu **Vervallen saldi** als u de details wilt bekijken van het naar ouderdom gerangschikte saldo voor alle factuurklanten in een kredietgroep van klant. De pagina **Naar ouderdom gerangschikt saldo** toont een overzicht van de vervallen saldi voor de factuurklantrekeningen.
