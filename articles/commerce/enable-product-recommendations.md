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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770134"
---
# <a name="enable-product-recommendations"></a>Productaanbevelingen inschakelen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u productaanbevelingen kunt doen op basis van kunstmatige intelligentie-machine learning (AI-ML) die beschikbaar is voor klanten van Microsoft Dynamics 365 Commerce. Meer informatie over lijsten met productaanbevelingen vindt u in [Overzicht van productaanbevelingen](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Aanbevelingen voor controle vooraf
Houd er rekening mee dat productaanbevelingen alleen worden ondersteund voor F&O-klanten die build 10.0.6 ondersteunen en hun opslag hebben gemigreerd naar BDL. 

Zorg er bovendien voor dat RetailSale-metingen zijn ingeschakeld. [Hier](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) vindt u meer informatie over dit instellingsproces.


## <a name="turn-on-recommendations"></a>Aanbevelingen inschakelen

Volg deze stappen om productaanbevelingen in te schakelen.

1. Ga naar **Detailhandel** &gt; **Productaanbevelingen** &gt; **Aanbevelingsparameters**.
1. Selecteer **Aanbevelingslijsten** in de lijst met gedeelde parameters voor detailhandel.
1. Stel de optie **Aanbevelingen inschakelen** in op **Ja**.

![Productaanbevelingen inschakelen](./media/enableproductrecommendations.png)

> [!NOTE]
> Met deze procedure start u het genereren van lijsten voor productaanbevelingen. Het kan enkele uren duren voordat de lijsten beschikbaar zijn en kunnen worden weergegeven op het verkooppunt (POS) of in Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Parameters voor aanbevelingslijsten configureren
Standaard bevat de lijst met productaanbevelingen op basis van AI-ML voorgestelde waarden. U kunt de voorgestelde standaardwaarden aanpassen aan de stroom van uw bedrijf. Als u meer wilt weten over het wijzigen van de standaardparameters, gaat u naar [Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Aanbevelingen weergeven op POS-apparaten
Nadat u aanbevelingen in de backoffice hebt ingeschakeld, moet het deelvenster met aanbevelingen worden toegevoegd aan het POS-scherm van het besturingselement via de indelingsfunctie. [Hier](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) vindt u meer informatie over dit proces.


## <a name="additional-resources"></a>Aanvullende resources

[Overzicht productaanbevelingen](product-recommendations.md)

[Lijsten met productaanbevelingen toevoegen aan pagina's](add-reco-list-to-page.md)

[Het deelvenster met aanbevelingen toevoegen aan POS-apparaten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


