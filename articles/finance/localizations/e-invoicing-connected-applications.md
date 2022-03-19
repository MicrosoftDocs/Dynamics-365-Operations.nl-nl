---
title: Verbonden toepassingen
description: In dit onderwerp wordt uitgelegd hoe u verbonden toepassingen instelt in Elektronische facturering.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371541"
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
6. Selecteer **Dynamics 365 Finance** in het veld **Type**.
7. Voer in het veld **Toepassing** de URL in voor de omgeving die moet worden verbonden.
8. Geef in het veld **Tenant** de tenant van de omgeving op.
9. Selecteer **Opslaan**.
10. Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen. Sluit de pagina vervolgens.

## <a name="link-connected-applications-to-environments"></a>Verbonden toepassingen aan omgevingen koppelen

1. Selecteer op de pagina **Omgeving instellen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.
2. Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.
3. Selecteer in het veld **Serviceomgeving** een serviceomgeving.
4. Selecteer **Opslaan** en sluit de pagina.
