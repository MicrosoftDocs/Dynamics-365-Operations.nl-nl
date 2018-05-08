--- 
title: Een configuratieprovider maken en deze als actief markeren voor elektronische rapportage (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 018aee917c13f576759ebd812d31cbc9d83e2d1a
ms.contentlocale: nl-nl
ms.lasthandoff: 02/23/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a>Een configuratieprovider maken en deze als actief markeren voor elektronische rapportage (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken. Elke ER-configuratie verwijst naar de provider als auteur van de configuratie. In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.


## <a name="create-a-provider"></a>Een provider maken
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Configuratieproviders.
3. Klik op Nieuw.
    * Een providerrecord heeft een unieke naam en URL. Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc (`http://www.litware.com`) bestaat.  
4. Typ 'Litware, Inc.' in het veld Naam.
    * Litware, Inc.  
5. Typ `http://www.litware.com` in het veld Internetadres.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="select-as-an-active-provider"></a>Selecteren als actieve provider
1. Selecteer de provider Litware, Inc. .
2. Klik op Instellingen als actief.


