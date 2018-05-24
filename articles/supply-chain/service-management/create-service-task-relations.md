---
title: Servicetaakrelaties maken
description: U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0892161605401420c0817b3b644271357446a99b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-task-relations"></a>Servicetaakrelaties maken    

[!include [banner](../includes/banner.md)]

U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order. Deze informatie is beschikbaar voor servicemonteurs en klanten.

## <a name="create-a-relation-with-a-service-agreement"></a>Een relatie maken met een serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer een bestaande serviceovereenkomst of maak een nieuwe serviceovereenkomst.

3.  Klik in het actievenster op de knop **Servicetaken**.

4.  Druk in het formulier **Servicetaken** op CTRL+N om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaak te koppelen aan de serviceovereenkomst.

5.  Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.

6.  Sluit het formulier om de record op te slaan.

Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceovereenkomst. U kunt deze servicetaken nu opgeven voor gekoppelde overeenkomstregels.

Een servicetaakrelatie die is gemaakt voor een serviceovereenkomst, is beschikbaar vanuit alle serviceorders die aan de serviceovereenkomst zijn gekoppeld.

## <a name="create-a-relation-with-a-service-order"></a>Een relatie maken met een serviceorder

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Selecteer een bestaande serviceorder of maak een nieuwe serviceorder.

3.  Klik in het actievenster op de knop **Servicetaken**.

4.  Druk in het formulier **Servicetaken** op CTRL+N om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaken te koppelen aan de serviceorder.

5.  Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.

6.  Sluit het formulier om de record op te slaan.

Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceorder. U kunt nu de servicetaak waarvoor u de relatie hebt gemaakt, selecteren wanneer u serviceorderregels maakt.

De servicetaakrelaties die zijn gemaakt voor een serviceorder, zijn beschikbaar op de desbetreffende serviceorder.

## <a name="see-also"></a>Zie ook

[Servicetaken](service-tasks.md)


  



