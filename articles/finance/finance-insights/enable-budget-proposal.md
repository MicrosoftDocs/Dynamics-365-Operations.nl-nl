---
title: Budgetvoorstellen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.
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
ms.openlocfilehash: 3a2060d082ed55e3b6fac506898916942ccc9db7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208480"
---
# <a name="enable-budget-proposals-preview"></a>Budgetvoorstellen inschakelen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.

1. Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving. Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving. (Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Als uw implementatie van Microsoft Dynamics 365 Finance een Service Fabric-implementatie is, kunt u deze stap overslaan. Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld. Als u de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt bij het inschakelen van de functie, verzendt u een e-mail naar het [team voor de preview van de Financiële inzichten-app](mailto:fiap@microsoft.com).

2. Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:

    1. Selecteer **Controleren op updates**.
    2. Zoek **Budgetvoorstel** en schakel de functie in.

3. Ga naar **Budgettering \> Instellen \> Basisbudgettering \> Budgetvoorstel (preview)** en selecteer **Functie inschakelen**.

#### <a name="privacy-notice"></a>Privacyverklaring
Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]