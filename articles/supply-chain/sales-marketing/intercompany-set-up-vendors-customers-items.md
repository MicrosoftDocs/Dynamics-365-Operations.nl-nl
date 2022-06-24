---
title: Leveranciers, klanten en artikelen voor intercompany-handel instellen
description: In dit artikel wordt uitgelegd hoe u leveranciers, klanten en artikelen voor intercompany-handel instelt
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945750"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Leveranciers, klanten en artikelen voor intercompany-handel instellen

[!include [banner](../../includes/banner.md)]

Als u uw organisatie wilt voorbereiden op intercompany-handel, moet u de leveranciers en klanten definiëren met wie u intern wilt handelen. Vervolgens moet u deze leveranciers en klanten koppelen aan de artikelen die u wilt kopen of verkopen.

1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**.
1. Selecteer de leverancier om deze als intercompany-leverancier te definiëren.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Geef instellingen voor intercompany-parameters op voor de leveranciersrekening. Deze parameters omvatten de rechtspersoon en de rekening van de klant, het verkooporderbeleid, het inkooporderbeleid, de waardetoewijzing en beleid op het gebied van inkoop- en verkoopovereenkomsten. U geeft ook op of de waarden van de basisgegevens van de leveranciersrekening of van de klantrekening in de andere rechtspersoon gebruikt moeten worden.
1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer op de lijstpagina **Vrijgegeven producten** de artikelen die u wilt toewijzen aan de leverancier, zodat de artikelen beschikbaar zijn voor intercompany-handel. Open voor elk artikel de pagina **Vrijgegeven productdetails**. Typ op het tabblad **Inkoop** in het veld **Leverancier** het leveranciersnummer.
1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant selecteren die als intercompany-klant moet worden gedefinieerd.
1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Intercompany**.
1. Geef instellingen voor intercompany-parameters op voor de klantrekening. Deze parameters omvatten de rechtspersoon en de rekening van de leverancier, het inkooporderbeleid, het verkooporderbeleid, de waardetoewijzing en het beleid op het gebied van inkoop- en verkoopovereenkomsten. U geeft ook op of de waarden van de basisgegevens van de klantrekening of van de leveranciersrekening in de andere rechtspersoon gebruikt moeten worden.
1. Wanneer u de intercompany-parameters hebt ingesteld, sluit u de pagina **Intercompany** om terug te keren naar de details van de geselecteerde klant.
1. Vouw het sneltabblad **Diverse details** uit en stel **Intercompany-orders maken** in op *Ja*. Stel **Rechtstreekse levering** in op *Ja* als u wilt dat orders rechtstreeks aan klanten worden geleverd.

    > [!NOTE]
    > Als er artikelen zijn die uw bedrijf op voorraad heeft en bij klanten aflevert, wilt u intercompany-orders mogelijk niet automatisch maken, ook al hebt u het artikel op voorraad. Als u het automatisch genereren van orders voor artikelen die u soms op voorraad hebt wilt uitschakelen, stelt u **Intercompany-orders maken** in op *Nee*.

1. Als u het indirect maken van extra regels op een verkooporder wilt toestaan, stelt u **Indirecte orderregels maken** in op *Ja*. Een gebruiker kan nu regels aan de oorspronkelijke verkooporder toevoegen vanuit de intercompany-verkooporder.

> [!WARNING]
> Als u het indirect maken van orderregels toestaat, staat u alle toevoegingen toe aan de oorspronkelijke verkooporder vanuit de intercompany-verkooporder. Elke toevoeging wordt vervolgens verwerkt naar de klant en toegevoegd aan de order en de factuur. Bovendien wordt elk document dat bij de verkoop betrokken is, automatisch afgedrukt en geboekt. Gebruikers worden niet gewaarschuwd over de toevoeging.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
