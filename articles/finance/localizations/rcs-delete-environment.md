---
title: Regulatory Configuration Service (RCS) - een RCS-omgeving verwijderen
description: In dit onderwerp wordt uitgelegd hoe een beheerder van de RCS (Regulatory Configuration Service) een RCS-omgeving en bijbehorende gegevens kan verwijderen.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: cf82abbe5493eac9665323738441fa016205e9ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355002"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - een RCS-omgeving verwijderen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe een beheerder van de RCS (Regulatory Configuration Service) een RCS-omgeving en bijbehorende gegevens kan verwijderen.

Voordat u de procedure in dit onderwerp kunt voltooien, moet aan de volgende vereisten zijn voldaan:

- De rol **Systeembeheerder** moet aan u zijn toegewezen voor de RCS-omgeving.
- Aan de rol **Systeembeheerder** moet de rol **RCSDeleteEnvironmentDuty** zijn toegewezen.

## <a name="delete-an-rcs-environment"></a>Een omgeving verwijderen

1. Open RCS en selecteer de tegel **Elektronische rapportage**.
2. Selecteer **RCS-omgeving verwijderen** in de sectie **Verwante koppelingen**.

    ![De RCS-omgevingskoppeling in de sectie Verwante koppelingen verwijderen.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Controleer in het dialoogvenster dat verschijnt de berichten over het bereik van de verwijdering van de omgeving.

    ![Berichten in het dialoogvenster RCS-omgeving verwijderen.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Verwijdering van een RCS-omgeving kan niet worden omgekeerd.
    >
    > De bewerking verwijdert de geselecteerde RCS-omgeving en bijbehorende gegevens, waaronder functies en configuraties die zijn opgeslagen in de algemene opslagplaats. Functies en configuraties die worden gedeeld met andere organisaties worden niet meer gedeeld en worden verwijderd als deze geen afhankelijkheden hebben. Functies en configuraties met afhankelijkheden worden gemarkeerd als gestopt.

4. Voer in het betreffende veld de Globally Unique Identifier (GUID) van de RCS-omgeving in om te bevestigen dat u deze wilt verwijderen. De GUID van de omgeving is opgenomen in het verwijderingsbericht.
5. Selecteer **Omgeving verwijderen**.
    
Uw RCS-omgeving en alle bijbehorende gegevens worden nu verwijderd.

> [!IMPORTANT]
> Nadat u een RCS-omgeving hebt verwijderd, kunnen de gegevens niet meer worden hersteld. Er kan een nieuwe RCS-omgeving worden gemaakt in elke beschikbare RCS-regio.
