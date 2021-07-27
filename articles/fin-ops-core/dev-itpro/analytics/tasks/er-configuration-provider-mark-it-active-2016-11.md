---
title: Aanbieders van configuraties maken en deze als actief markeren
description: In het volgende onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider kan maken.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9428ff1f53928f104df4736911ce34756128da44
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359430"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Aanbieders van configuraties maken en deze als actief markeren

[!include [banner](../../includes/banner.md)]

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

![Pagina met het werkgebied Elektronische rapportage.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]