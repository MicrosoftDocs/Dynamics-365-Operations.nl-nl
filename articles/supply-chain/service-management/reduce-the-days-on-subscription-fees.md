---
title: De dagen van abonnementskosten verminderen
description: Als u het aantal dagen van bestaande abonnementskosten wilt beperken, kunt u een nieuwe transactie maken waarin u de periode verwijdert die geen deel meer moet uitmaken van het abonnementskosteninterval.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b183d8fc8083c630bcb4e0e69fb755f8a50f95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569725"
---
# <a name="reduce-the-days-on-subscription-fees"></a>De dagen van abonnementskosten verminderen 

[!include [banner](../includes/banner.md)]


Als u het aantal dagen van bestaande abonnementskosten wilt beperken, kunt u een nieuwe transactie maken waarin u de periode verwijdert die geen deel meer moet uitmaken van het abonnementskosteninterval.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Het aantal dagen van abonnementskosten beperken

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceabonnementen** \> **Alle serviceabonnementen**. Selecteer het serviceabonnement en klik in het actievenster op **Abonnementskosten**

2.  Selecteer in het veld **Abonnementstype** **Reductiedagen**.

3.  Gebruik de velden **Datum vanaf** en **Datum t/m** om het datuminterval op te geven van de abonnementskosten die u wilt verwijderen uit de periode van de abonnementskosten en klik op **OK**.

Als u de gemaakte transactie wilt weergeven, klikt u in het formulier **Abonnement** op **Tarieftransacties**.

## <a name="example"></a>Voorbeeld

Als de periode van een abonnementstransactie loopt van 1 januari tot 31 januari en u de periode wilt verkorten met tien dagen, maakt u een nieuwe transactie waarin de reductieperiode 1 januari tot 10 januari is. (De reductieperiode kan ook 5 januari tot 15 januari zijn of een andere periode van 10 dagen.)

Als **Datum vanaf** in de reductieperiode 21 januari is (31 min 10), kunt u bovendien de **Datum t/m** instellen op elke gewenste datum na 31 januari, waarna nog steeds tien dagen worden verwijderd uit de periode van de bijzondere-kostentransactie.

## <a name="see-also"></a>Zie ook

[Voorbeeld van reductiedagen](reduction-days-example.md)

  


