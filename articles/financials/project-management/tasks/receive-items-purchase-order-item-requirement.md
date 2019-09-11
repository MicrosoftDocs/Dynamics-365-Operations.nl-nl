---
title: Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte
description: In dit onderwerp ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867290"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp ziet u hoe u artikelen ontvangt op een inkooporder vanuit een artikelbehoefte.

Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning. 

In deze taak wordt de gegevensset van USSI gebruikt.

1. Ga in het navigatievenster naar **Modules > Projectbeheer en boekhouding > Projecten > Alle projecten**.
2. Selecteer in de lijst de koppeling in de gewenste rij.
3. Selecteer **Plan** in het actievenster.
4. Selecteer **Artikelbehoeften**.
5. Selecteer **Nieuw**.
6. Typ of selecteer een waarde in de nieuwe rij in het veld **Artikelnummer**.
7. Voer een getal in het veld **Hoeveelheid** in.
8. Selecteer **Opslaan**.
9. Selecteer in het actievenster de optie **Beheren**.
10. Selecteer **Functies**.
11. Selecteer **Inkooporder maken**.
12. Schakel het selectievakje **Alles opnemen** in.
13. In het veld **Leveranciersrekening** typt of selecteert u een waarde.
14. Selecteer **OK**.
15. Ga in het navigatievenster naar **Modules > Leveranciers > Inkooporders > Alle inkooporders**.
16. Selecteer in de lijst de koppeling in de gewenste rij.
17. Selecteer in het actievenster de optie **Inkoop**.
18. Selecteer **Bevestigen**.
19. Selecteer **Ontvangen** in het actievenster.
20. Selecteer **Productontvangstbon**.
21. Typ een waarde in het veld **Productontvangstbon**.
22. Selecteer **OK**.

