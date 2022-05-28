---
title: Leveranciers, klanten en artikelen voor intercompany-handel instellen
description: In dit onderwerp wordt uitgelegd hoe u leveranciers, klanten en artikelen voor intercompany-handel instelt
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
ms.openlocfilehash: 3e1eb7b8673f3af682204b65b33a1d8b61742721
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675032"
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
1. Schakel op de pagina **Klanten** op het sneltabblad **Factuur en levering** het selectievakje **Intercompany-orders maken** in. Schakel het selectievakje **Rechtstreekse levering** in als u wilt dat orders rechtstreeks aan klanten geleverd worden.

    > [!NOTE]
    > Als er artikelen zijn die uw bedrijf op voorraad heeft en bij klanten aflevert, wilt u intercompany-orders mogelijk niet automatisch maken, ook al hebt u het artikel op voorraad. Als u het automatisch genereren van orders voor artikelen die u soms op voorraad hebt wilt uitschakelen, moet u het selectievakje **Intercompany-orders maken** uitschakelen.

1. Als u het indirect maken van extra regels op een verkooporder wilt toestaan, schakelt u het selectievakje **Indirecte orderregels maken** in. Een gebruiker kan nu regels aan de oorspronkelijke verkooporder toevoegen vanuit de intercompany-verkooporder.

> [!WARNING]
> Als u het indirect maken van orderregels toestaat, staat u alle toevoegingen toe aan de oorspronkelijke verkooporder vanuit de intercompany-verkooporder. Elke toevoeging wordt vervolgens verwerkt naar de klant en toegevoegd aan de order en de factuur. Bovendien wordt elk document dat bij de verkoop betrokken is, automatisch afgedrukt en geboekt. Gebruikers worden niet gewaarschuwd over de toevoeging.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
