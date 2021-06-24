---
title: Een gegevensintegratorproject maken (preview)
description: In dit onderwerp wordt uitgelegd hoe u een gegevensintegratorproject maakt.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186463"
---
# <a name="create-a-data-integrator-project-preview"></a>Een gegevensintegratorproject maken (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een gegevensintegratorproject maakt.

1. Meld u aan bij Microsoft Dynamics 365 Finance.
2. Ga naar **Werkgebieden \> Gegevensbeheer** en selecteer **Gegevensentiteiten**. Wacht totdat alle gegevensentiteiten zijn vernieuwd voordat u naar de volgende stap gaat.
3. Open de [Power Apps portal](https://make.powerapps.com/) en voer de volgende stappen uit:

    1. Selecteer de gewenste omgeving.
    2. Selecteer in het linkernavigatievenster **Gegevens \> Verbindingen**.
    3. Verbinding maken met de juiste instanties van de volgende items:

        - Dynamics 365
        - Dynamics 365 voor Fin & Ops

4. Open de [Power Apps omgevingen](https://admin.powerapps.com/environments) en voer de volgende stappen uit:

    1. Selecteer **Gegevensintegrator**.
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

        - Resultaten van inzichten voor klantbetalingen (CDS naar Fin and OPS)
            - Als u versie 10.0.17 of hoger gebruikt, moet u de sjabloon gebruiken met de naam Inzichten in klantbetalingen (CDS naar Fin en Ops 10.0.17+).
        - Resultaten van cashflowtijdreeksen (CDS naar Fin and Ops)
        - Resultaten van budgettijdreeksen (CDS naar Fin and OPS)

    2. Stel de juiste planning in voor elk project.

> [!NOTE]
> Als de vereiste entiteiten niet in CDS worden weergeven, gaat u naar **Credit en aanmaningen > Instellen > Financiële inzichten > Parameters voor financiële inzichten**, schakelt u de functie Voorspellingen klantbetalingen in en klikt u op **Voorspellingsmodel maken**. Wanneer de implementatie van het AI-model is voltooid (geslaagd of mislukt), worden de CDS-entiteiten die nodig zijn om integratie te maken, geïmplementeerd in CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
