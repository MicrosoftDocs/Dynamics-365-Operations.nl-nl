---
title: Servicetaakrelaties maken
description: U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9a7808357916ed80ddfa46e1e4f362e0dde1671
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819059"
---
# <a name="create-service-task-relations"></a>Servicetaakrelaties maken    

[!include [banner](../includes/banner.md)]

U kunt servicetaken koppelen aan serviceovereenkomsten of serviceorders om de servicetaak te omschrijven die moet worden uitgevoerd voor de overeenkomst of order. Deze informatie is beschikbaar voor servicemonteurs en klanten.

## <a name="create-a-relation-with-a-service-agreement"></a>Een relatie maken met een serviceovereenkomst

1.  Ga naar **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer een bestaande serviceovereenkomst of maak een nieuwe serviceovereenkomst.

3.  Selecteer in het actiedeelvenster de knop **Servicetaken**.

4.  Selecteer in het formulier **Servicetaken** de optie **Nieuw** om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaak te koppelen aan de serviceovereenkomst.

5.  Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.

6.  Sluit het formulier om de record op te slaan.

Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceovereenkomst. U kunt deze servicetaken nu opgeven voor gekoppelde overeenkomstregels.

Een servicetaakrelatie die is gemaakt voor een serviceovereenkomst, is beschikbaar vanuit alle serviceorders die aan de serviceovereenkomst zijn gekoppeld.

## <a name="create-a-relation-with-a-service-order"></a>Een relatie maken met een serviceorder

1.  Ga naar **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Selecteer een bestaande serviceorder of maak een nieuwe serviceorder.

3.  Selecteer in het actiedeelvenster de knop **Servicetaken**.

4.  Selecteer in het formulier **Servicetaken** de optie **Nieuw** om een nieuwe regel te maken en selecteer vervolgens een servicetaak in de lijst **Servicetaak** om de servicetaken te koppelen aan de serviceorder.

5.  Voer op het tabblad **Beschrijving** interne of externe notitieomschrijvingen in de vrije-tekstvelden in.

6.  Sluit het formulier om de record op te slaan.

Herhaal deze procedure totdat u alle benodigde servicetaakrelaties hebt gemaakt voor de serviceorder. U kunt nu de servicetaak waarvoor u de relatie hebt gemaakt, selecteren wanneer u serviceorderregels maakt.

De servicetaakrelaties die zijn gemaakt voor een serviceorder, zijn beschikbaar op de desbetreffende serviceorder.

## <a name="see-also"></a>Zie ook

[Overzicht van Servicetaken](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]