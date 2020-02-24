---
title: Productaanbevelingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024951"
---
# <a name="enable-product-recommendations"></a>Productaanbevelingen inschakelen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce. Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Aanbevelingen voor controle vooraf

Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-klanten die hun opslag hebben gemigreerd met behulp van Azure Data Lake Storage (ADLS). 

Zie [ADLS in een Dynamics 365-omgeving inschakelen](enable-ADLS-environment.md) voor stapsgewijze instructies voor het inschakelen van ADLS.

Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld. [Hier](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.


## <a name="turn-on-recommendations"></a>Aanbevelingen inschakelen

Volg deze stappen om productaanbevelingen in te schakelen.

1. Ga naar **Retail en Commerce &gt; Productaanbevelingen &gt; Aanbevelingsparameters**.
1. Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters.
1. Stel de optie **Aanbevelingen inschakelen** in op **Ja**.

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> Met deze procedure start u het genereren van lijsten voor productaanbevelingen. Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Parameters voor aanbevelingslijsten configureren

Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden. U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf. Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Aanbevelingen weergeven op POS-apparaten

Nadat u aanbevelingen in de Commerce-backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie. Zie [Een besturingselement voor aanbevelingen toevoegen aan het transactiescherm op POS-apparaten](add-recommendations-control-pos-screen.md) voor meer informatie over dit proces. 

## <a name="enable-personalized-recommendations"></a>Gepersonaliseerde aanbevelingen inschakelen

Zie [Persoonlijke aanbevelingen inschakelen](personalized-recommendations.md) voor meer informatie over het ontvangen van persoonlijke productaanbevelingen.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht productaanbevelingen](product-recommendations.md)

[Gepersonaliseerde aanbevelingen inschakelen](personalized-recommendations.md)

[Lijsten met productaanbevelingen toevoegen aan pagina's](add-reco-list-to-page.md)

[Het deelvenster met aanbevelingen toevoegen aan POS-apparaten](add-recommendations-control-pos-screen.md)

[Overzicht productverzamelingsmodule](product-collection-module-overview.md)

[ADLS inschakelen in een Dynamics 365-omgeving](enable-ADLS-environment.md)

