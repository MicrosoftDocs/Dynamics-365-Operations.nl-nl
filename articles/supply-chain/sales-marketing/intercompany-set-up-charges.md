---
title: Toeslagen op intercompany-orders instellen
description: In dit onderwerp wordt uitgelegd hoe u toeslagen op intercompany-orders instelt
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548199"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Toeslagen op intercompany-orders instellen

[!include [banner](../../includes/banner.md)]

U kunt toeslagen instellen die aan intercompany-orders kunnen worden toegevoegd. Wanneer een toeslag is toegevoegd aan een intercompany-verkooporder, wordt deze automatisch gesynchroniseerd naar de intercompany-inkooporder. Deze synchronisatie wordt in beide richtingen uitgevoerd: van de intercompany-verkooporder naar de inkooporder en omgekeerd.

U kunt toeslagen ook gebruiken om een winst toe te voegen aan een intercompany-verkooporder door de toeslagen te definiëren als intercompany-percentage.

Wanneer u toeslagen instelt die moeten worden toegepast op intercompany-orders, activeert u de berekening van interne winst voor een intercompany-verkooporder van het nettobedrag van de oorspronkelijke verkooporder. Dit wilt u mogelijk doen als uw intercompany-leverancier u iets verkoopt tegen kostprijs. In de volgende procedure wordt beschreven hoe u dit doet voor intercompany-klanten. U kunt dezelfde procedure volgen voor leveranciers.

1. Ga naar **Klanten \> Instellen \> Toeslagen \> Toeslaggroepen van klant**.
1. Maak een toeslagengroep.
1. Ga naar **Klanten \> Klanten \> Alle klanten**. Selecteer een koppeling naar een klantrekening. Selecteer in het actievenster het tabblad **Klant** en selecteer vervolgens het sneltabblad **Verkooporder**.
1. Selecteer **Bewerken** in het actievenster om het veld te kunnen bewerken. Selecteer in het veld **Toeslagengroep** de intercompany-toeslagengroep die u in stap 2 hebt ingesteld.
1. Ga naar **Klanten \> Instellen \> Toeslagen \> Automatische toeslagen**.
1. Stel de toeslagen in door waarden in te vullen in de relevante velden.
1. Selecteer in het veld **Klantrelatie** de intercompany-toeslagengroep die u in stap 2 hebt ingesteld.
1. Selecteer op het sneltabblad **Regels** in het veld **Categorie** de optie **Intercompany-percentage**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
