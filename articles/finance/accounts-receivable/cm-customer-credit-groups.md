---
title: Kredietgroepen van klant
description: Dit artikel bevat informatie over kredietgroepen van klant.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 032e92431946f0a41bf2e52c155e422d4ea0b3b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886511"
---
# <a name="customer-credit-groups"></a>Kredietgroepen van klant

[!include [banner](../includes/banner.md)]

U kunt groepen klanten definiëren die een gedeelde kredietlimiet hebben. Er wordt ook rekening gehouden met de individuele kredietlimiet die is gedefinieerd voor de rekening van de klantfactuur.

Leden van een kredietgroep van klant kunnen uit verschillende rechtspersonen worden geselecteerd. Wanneer u een klant aan de lijst met klanten in de kredietgroep van de klant toevoegt, verandert de vervaldatum van de kredietlimiet voor elke klant in de vervaldatum die is toegewezen aan de groep.

U kunt kredietgroepen van klant instellen op de pagina **Kredietgroepen van klant** (**Kredietbeheer \> Kredietgroepen van klant \> Kredietgroepen van klant**).

1. Voer in de velden **Groepsnummer** en **Beschrijving** een id en beschrijving voor de groep in.
2. Voer in de velden **Kredietlimiet** en **Valuta** de kredietlimiet en valuta in die moeten worden gebruikt wanneer het systeem de kredietlimiet voor een lid van de groep controleert.
3. Voer in het veld **Kredietlimiet tot datum** de datum in waarop de kredietlimiet vervalt. Kredietgroepen van klant moeten een vervaldatum hebben.

Wanneer u klaar bent met het instellen van een kredietgroep van klant, kunt u er klanten aan toevoegen door hun rechtspersoon en klantrekening-id op te geven. Wanneer u een nieuwe klant toevoegt aan een kredietgroep van klant, zoekt het systeem in alle rechtspersonen naar dezelfde klantrekening en wordt u gevraagd of u deze wilt toevoegen aan de kredietgroep van klant.

Gebruik het menu **Vervallen saldi** als u de details wilt bekijken van het naar ouderdom gerangschikte saldo voor alle factuurklanten in een kredietgroep van klant. De pagina **Naar ouderdom gerangschikt saldo** toont een overzicht van de vervallen saldi voor de factuurklantrekeningen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
