---
title: Aanbieders van configuraties maken en deze als actief markeren
description: In het volgende onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249199"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Aanbieders van configuraties maken en deze als actief markeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In het volgende onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken. Elke ER-configuratie verwijst naar de provider als auteur van de configuratie. In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.

## <a name="create-a-provider"></a>Een provider maken
1. Ga naar het **navigatiepaneel** in de linkerbovenhoek en selecteer **Organisatiebeheer.**
2. Ga naar **Werkgebieden > Elektronische rapportage**.
3. Ga naar **Verwante koppelingen > Configuratieproviders**.
4. Selecteer **Nieuw**.
    - Een providerrecord heeft een unieke naam en URL. Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc (https://www.litware.com) bestaat.  
5. Typ `Litware, Inc.` in het veld Naam.
6. Typ `https://www.litware.com` in het veld Internetadres.
7. Selecteer **Opslaan**.
8. Sluit de pagina.

## <a name="select-as-an-active-provider"></a>Selecteren als actieve provider
1. Selecteer de provider Litware, Inc. .
2. Selecteer **Instellingen als actief**.

![Pagina met het werkgebied Elektronische rapportage](../media/GER-Task-ActiveProvider-1.png)
