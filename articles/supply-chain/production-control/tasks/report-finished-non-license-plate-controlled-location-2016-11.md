---
title: Gereedmelden bij een locatie waar nummerplaten niet worden gecontroleerd (toepassing, mei 2016)
description: Deze taakbegeleiding toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562922"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Gereedmelden bij een locatie waar nummerplaten niet worden gecontroleerd (toepassing, mei 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd. Een toepasselijk werkbeleid is de vereiste voor deze taak. Een vorige taakbegeleiding liet zien hoe het werkbeleid wordt ingesteld. Voor deze taakbegeleiding is de toepassing Dynamics AX 7.0.1 of hoger vereist.




## <a name="set-up-an-output-location"></a>Een uitvoerlocatie instellen
1. Ga naar Organisatiebeheer > Resources > Resourcegroepen.
2. Selecteer resourcegroep '5102' in de lijst.
3. Klik op Bewerken.
4. Voer '51' in het veld Uitvoermagazijn in.
5. Voer '001' in het veld Uitvoerlocatie in.
    * Locatie 001 is geen locatie waar nummerplaten worden gecontroleerd. U kunt een uitvoerlocatie waar geen nummerplaten worden gecontroleerd alleen instellen als er een toepasselijk werkbeleid voor de locatie bestaat.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Een productieorder maken en gereedmelden
1. Sluit de pagina.
2. Ga naar Productiebeheer > Productieorders > Alle productieorders.
3. Klik op Nieuwe productieorder.
4. Voer 'L0101' in het veld Artikelnummer in.
5. Klik op Maken.
6. Klik in het actievenster op Productieorder.
7. Klik op Raming.
8. Klik op OK.
9. Klik op Start.
10. Klik op het tabblad Algemeen.
11. Selecteer 'Nooit' in het veld Automatisch stuklijstverbruik.
12. Klik op OK.
13. Klik op Gereedmelden.
14. Klik op het tabblad Algemeen.
15. Selecteer Ja in het veld Fout accepteren.
16. Klik op OK.
17. Klik in het actievenster op Magazijn.
18. Klik op Werkdetails.
    * Toen de productieorder gereedgemeld werd, is er geen werk gegenereerd voor wegzetten. Dit komt doordat er een werkbeleid is gedefinieerd waarmee wordt voorkomen dat werk wordt gegenereerd wanneer product L0101 wordt gereedgemeld bij locatie 001.  

