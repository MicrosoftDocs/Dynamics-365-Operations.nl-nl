---
title: Een gegevensintegratorproject maken (preview)
description: In dit onderwerp wordt uitgelegd hoe u een gegevensintegratorproject maakt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009438"
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
        - Resultaten van cashflowtijdreeksen (CDS naar Fin and Ops)
        - Resultaten van budgettijdreeksen (CDS naar Fin and OPS)

    2. Stel de juiste planning in voor elk project.

> [!NOTE]
> Als de vereiste entiteiten niet in CDS worden weergeven, gaat u naar **Credit en aanmaningen > Instellen > Financiële inzichten > Parameters voor financiële inzichten**, schakelt u de functie Voorspellingen klantbetalingen in en klikt u op **Voorspellingsmodel maken**. Wanneer de implementatie van het AI-model is voltooid (geslaagd of mislukt), worden de CDS-entiteiten die nodig zijn om integratie te maken, geïmplementeerd in CDS.

## <a name="privacy-notice"></a>Privacyverklaring

Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]