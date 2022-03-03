---
title: Een gegevensintegratieproject maken
description: In dit onderwerp wordt uitgelegd hoe u een gegevensintegratieproject maakt.
author: ShivamPandey-msft
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107282"
---
# <a name="create-a-data-integration-project"></a>Een gegevensintegratieproject maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een gegevensintegratieproject maakt.

1. Meld u aan bij Microsoft Dynamics 365 Finance.
2. Ga naar **Werkgebieden \> Gegevensbeheer** en selecteer **Gegevensentiteiten**. Wacht totdat alle gegevensentiteiten zijn vernieuwd voordat u naar de volgende stap gaat.
3. Open de [Power Apps portal](https://make.powerapps.com/) en voer de volgende stappen uit:

    1. Selecteer de gewenste omgeving.
    2. Selecteer in het linkernavigatievenster **Dataverse \> Verbindingen**.
    3. Verbinding maken met de juiste instanties van de volgende items:

        - Dynamics 365
        - Dynamics 365 voor Fin & Ops

4. Open de [Power Apps omgevingen](https://admin.powerapps.com/environments) en voer de volgende stappen uit:

    1. Selecteer **Gegevensintegratie**.
    2. Selecteer **Verbindingssets**.
    3. Selecteer **Nieuwe verbindingsset**.
    4. Geef een naam op voor de verbinding.
    5. Selecteer de juiste verbindingen voor de volgende items:

        - Dynamics 365
        - Dynamics 365 voor Fin & Ops

    6. Selecteer de juiste organisatietoewijzing.
    7. Selecteer **Maken**.

5. Open de [Power Apps omgevingen](https://admin.powerapps.com/environments) en voer de volgende stappen uit:  

    1. Maak gegevensintegratieprojecten voor de volgende sjablonen met de verbindingsset die u zojuist hebt gemaakt:

        - Resultaat van inzichten voor klantbetalingen (CDS naar Fin and Ops 10.0.17+)
        - Resultaten van cashflowtijdreeksen (CDS naar Fin and Ops)
        - Resultaten van budgettijdreeksen (CDS naar Fin and OPS)

    2. Stel de juiste planning in voor elk project.

> [!NOTE]
> Als de vereiste entiteiten niet in Dataverse worden weergeven, gaat u naar **Credit en aanmaningen** > **Instellen** > **Finance Insights** > **Parameters voor financiële inzichten**, schakelt u de functie **Voorspellingen klantbetalingen** in en klikt u op **Voorspellingsmodel maken**. Wanneer de implementatie van het AI-model is voltooid, worden de Dataverse-entiteiten geïmplementeerd die nodig zijn voor de integratie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
