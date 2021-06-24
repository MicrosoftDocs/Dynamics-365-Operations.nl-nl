---
title: Budgetvoorstellen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222529"
---
# <a name="enable-budget-proposals-preview"></a>Budgetvoorstellen inschakelen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie Budgetvoorstel kunt inschakelen in Financiële inzichten.

1. Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving. Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving. (Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Sla deze stap over als u versie 10.0.20 of hoger gebruikt of als u een Service Fabric-implementatie gebruikt. Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld. Als de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.

2. Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:

    1. Selecteer **Controleren op updates**.
    2. Zoek **Budgetvoorstel** en schakel de functie in.

3. Ga naar **Budgettering \> Instellen \> Basisbudgettering \> Budgetvoorstel (preview)** en selecteer **Functie inschakelen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
