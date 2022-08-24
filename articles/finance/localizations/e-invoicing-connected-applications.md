---
title: Verbonden toepassingen
description: In dit artikel wordt uitgelegd hoe u verbonden toepassingen instelt in Elektronische facturering.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f908caa902e4747d324480e3a5108b443d385ea7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277326"
---
# <a name="connected-applications"></a>Verbonden toepassingen

[!include [banner](../includes/banner.md)]

Verbonden toepassingen zijn de exemplaren van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management die u mogelijk wilt bereiken via Regulatory Configuration Service (RCS). Via de verbonden toepassingen kunt u een gedeelte van de globalisatiefunctie in Finance of Supply Chain Management configureren om de elektronische factureringsfunctie te laten werken.

Wanneer u de globalisatiefunctie implementeert, kunnen de instellingsgegevens die van toepassing zijn op Finance of Supply Chain Management, rechtstreeks vanuit RCS worden gepubliceerd in de juiste verbonden toepassing.

De beschikbaarheid van parameters voor Finance of Supply Chain Management in RCS is handig wanneer u verschillende toepassingsomgevingen hebt, zoals UAT (User Acceptance Testing) en productieomgevingen, en u de instellingen consistent wilt houden door dezelfde parameters in verschillende omgevingen te implementeren.

## <a name="create-a-connected-application"></a>Een verbonden toepassing maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Omgeving instellen** in het actiedeelvenster de optie **Verbonden toepassingen**.
4. Selecteer **Nieuw** om een verbonden toepassing te maken.
5. Voer in het veld **Naam** de naam in voor de toepassing die moet worden verbonden.
6. In het veld **Type** selecteert u **Dynamics 365 Finance**.
7. Voer in het veld **Toepassing** de URL in voor de omgeving die moet worden verbonden.
8. Geef in het veld **Tenant** de tenant van de omgeving op.
9. Selecteer **Opslaan**.
10. Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen. Sluit de pagina vervolgens.

## <a name="link-connected-applications-to-environments"></a>Verbonden toepassingen aan omgevingen koppelen

1. Selecteer op de pagina **Omgeving instellen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.
2. Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.
3. Selecteer in het veld **Serviceomgeving** een serviceomgeving.
4. Selecteer **Opslaan** en sluit de pagina.
