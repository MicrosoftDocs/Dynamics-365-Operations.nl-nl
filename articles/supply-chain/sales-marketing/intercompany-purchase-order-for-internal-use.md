---
title: Een intercompany-inkooporder voor intern gebruik maken en factureren
description: In dit onderwerp wordt uitgelegd hoe u een intercompany-inkooporder voor intern gebruik maakt
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548193"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Een intercompany-inkooporder voor intern gebruik maken en factureren

[!include [banner](../../includes/banner.md)]

U kunt een intercompany-inkooporder maken voor een intercompany-leverancier. Hiermee wordt automatisch een intercompany-inkooporder gemaakt bij de intercompany-leverancier.

![Intern intercompany-inkoopproces](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Een intercompany-inkooporder en een corresponderende intercompany-verkooporder maken

Voer deze stappen uit in rechtspersoon AAA, zoals getoond in de afbeelding.

1. Selecteer **Leveranciers** \> **Inkooporders** \> **Alle inkooporders**.
1. Maak op de lijstpagina **Alle inkooporders** een inkooporder voor een intercompany-leverancier. De veldwaarden worden gekopieerd van de leveranciersrekening naar de inkooporder.

    Omdat u met een intercompany-leverancier werkt, wordt een intercompany-verkooporder gemaakt in de rechtspersoon die overeenkomt met de leverancier. Het nummer van de intercompany-verkooporder kan hetzelfde zijn als het nummer van de intercompany-inkooporder en kan de id van de rechtspersoon bevatten. De nummerstructuur die wordt gebruikt is afhankelijk van de selectie in het veld **Verkoopordernummering** op de pagina **Intercompany**. Stel, u maakt inkooporder 00029\_064 in rechtspersoon AAA, dan is het verkoopordernummer in rechtspersoon BBB AAA00029\_64.

    In een informatief bericht wordt u op de hoogte gesteld dat er een intercompany-inkooporder en een intercompany-verkooporder zijn gemaakt. Voor uw informatie bevat het bericht het intercompany-verkoopordernummer.

1. Regelitems aan de inkooporder toevoegen. De bijbehorende regelitems worden automatisch toegevoegd aan de intercompany-verkooporder. Als een artikel niet bestaat in de andere rechtspersoon, wordt er een bericht weergegeven en kunt u het artikel niet aan de inkooporder toevoegen. Om dit probleem op te lossen gaat u naar de andere rechtspersoon en maakt u het product beschikbaar voor die rechtspersoon. Het artikel wordt beschikbaar en kan aan verkooporders in die rechtspersoon worden toegevoegd. Ga vervolgens terug naar de rechtspersoon van de inkooporder en ga door met het toevoegen van regelitems.
1. Wanneer u klaar bent met het invoeren van informatie voor de inkooporder, bevestigt u de order.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>De intercompany-pakbon en klantfactuur verwerken

Voer deze stappen uit in rechtspersoon BBB, zoals getoond in de afbeelding.

1. Ga naar **Klanten \> Verkooporders \> Alle verkooporders**.
1. Selecteer op de lijstpagina **Alle verkooporders** de intercompany-verkooporder.
1. Selecteer in het actievenster het tabblad **Verzamelen en inpakken** en selecteer vervolgens **Pakbon**.
1. Schakel het selectievakje **Boeking** in.
1. Selecteer **OK**. De pakbon wordt geboekt in rechtspersoon BBB.
1. Selecteer op de lijstpagina **Alle verkooporders** de intercompany-verkooporder.
1. Selecteer in het actievenster het tabblad **Factuur** en selecteer vervolgens **Factuur**.
1. Schakel het selectievakje **Boeking** in.
1. Selecteer **OK**.

    De klantfactuur voor de intercompany-verkooporder wordt geboekt in rechtspersoon BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>De intercompany-productontvangstbon en leveranciersfactuur verwerken

Voer deze stappen uit in rechtspersoon AAA, zoals getoond in de afbeelding.

1. Ga naar **Leveranciers \> Inkooporders \> Alle inkooporders**.
1. Selecteer op de lijstpagina **Alle inkooporders** een intercompany-inkooporder.
1. Selecteer in het actievenster **Ontvangen** en selecteer vervolgens **Productontvangst**. De productontvangstbon wordt gemaakt. Het productontvangstbonnummer is hetzelfde als het nummer van de intercompany-pakbon.
1. Schakel het selectievakje **Boeking** in.
1. Selecteer **OK**.
1. Selecteer op de lijstpagina **Alle inkooporders** een intercompany-inkooporder.
1. Selecteer **Factuur** in het actievenster en selecteer vervolgens **Factuur**. De leveranciersfactuur wordt gemaakt. Het nummer van de leveranciersfactuur is hetzelfde als het intercompany-klantfactuurnummer.
1. Voltooi het invoeren van de leveranciersfactuur en boek deze vervolgens.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
