---
title: Productbeoordelingen synchroniseren in Dynamics 365 Commerce
description: In dit artikel wordt beschreven hoe u productbeoordelingen in Microsoft Dynamics 365 Commerce kunt synchroniseren.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ac94a8b4505aba509f0a71ed36d32adac864aedf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909330"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Productbeoordelingen synchroniseren in Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u productbeoordelingen in Microsoft Dynamics 365 Commerce kunt synchroniseren.

Als u productbeoordelingen wilt gebruiken in omnichannels, zoals op het verkooppunt (POS) en in callcenters, moeten productbeoordelingen van de beoordelings- en revisieservice worden geïmporteerd in de database met Commerce-kanalen. Wanneer productbeoordelingen beschikbaar worden gemaakt in omnichannels, kunnen klanten tijdens hun interactie met verkoopmedewerkers indirect worden geholpen.

In dit artikel worden de volgende taken beschreven:

1. Configureer **Taak productbeoordelingen synchroniseren** als een batchtaak om productbeoordelingen te synchroniseren vanuit de **Service voor beoordelingen en recensies**.
1. Controleren of de batchtaak voor het synchroniseren van productbeoordelingen is geslaagd.
1. Productbeoordelingen beschikbaar maken op het POS.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Een batchtaak configureren om productbeoordelingen te synchroniseren

> [!IMPORTANT]
> Controleer voordat u begint of versie 10.0.6 of hoger van Dynamics 365 Commerce is geïnstalleerd.

### <a name="initialize-the-commerce-scheduler"></a>De Commerce-planner initialiseren

U initialiseerd de Commerce-planner als volgt.

1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> Commerce-planner \> Commerce-planner initialiseren**. U kunt ook zoeken naar "Commerce-planner initialiseren".
1. Controleer in het dialoogvenster **Commerce-planner initialiseren** of de optie **Bestaande configuratie verwijderen** is ingesteld op **Nee** en selecteer vervolgens **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>De subtaak RetailproductRating controleren

Voer de volgende stappen uit om te controleren of de subtaak **RetailproductRating** bestaat.

1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> Commerce-planner \> Plannersubtaken**. U kunt ook zoeken naar "Plannersubtaken".
1. Zoek in de lijst met subtaken naar de subtaak **RetailproductRating**.

In de volgende afbeelding ziet u een voorbeeld van subtaakdetails in Commerce.

![Details van de subtaak RetailProductRating.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Als u de subtaak **RetailproductRating** niet kunt vinden, hebt u mogelijk al de taak **Productbeoordelingen synchroniseren** en de **1040 CDX**-taak uitgevoerd voordat u de Commerce-planner hebt geïnitialiseerd. Voer in dat geval de volgende stappen uit om de taak **Volledige gegevenssynchronisatie** uit te voeren.

> 1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> Commerce-planner \> Kanaaldatabase**. U kunt ook zoeken naar "Kanaaldatabase".
> 1. Selecteer de kanaaldatabase die u wilt synchroniseren.
> 1. Selecteer in het actiedeelvenster **Volledige gegevenssynchronisatie**.
> 1. Selecteer in de vervolgkeuzelijst **Een distributieplanning selecteren** de optie **1040-producten** en selecteer vervolgens **OK**.
> 1. Herhaal de stappen van de vorige procedure om te controleren of de subtaak **RetailproductRating** is gemaakt.

### <a name="import-product-ratings"></a>Productbeoordelingen importeren

Voer de volgende stappen uit om productbeoordelingen in Commerce te importeren vanuit de service voor beoordelingen en recensies.

1. Ga naar **Detailhandel en commerce \> Instellingen van hoofdkantoor \> Commerce-planner \> Taak productbeoordelingen synchroniseren**. U kunt ook zoeken naar "Beoordelingstaak product synchroniseren".
1. Selecteer in het dialoogvenster **Productbeoordelingen ophalen** op het sneltabblad **Uitvoeren op de achtergrond** de optie **Terugkeerpatroon**.
1. Stel in het dialoogvenster **Terugkeerpatroon definiëren** een terugkeerpatroon in. (De voorgestelde waarde is twee uur.) Plan geen terugkeerpatroon dat minder dan een uur duurt.
1. Selecteer **OK**.
1. Stel de optie **Batchproces** in op **Ja**. Met deze instelling wordt gegarandeerd dat u de logboeken en de status van de uitgevoerde batchtaken kunt controleren.
1. Selecteer **OK** om de batchtaak te plannen.

In de volgende afbeelding ziet u een voorbeeld van batchtaakconfiguratie in Commerce.

![Configuratie van de batchtaak voor de synchronisatie van productbeoordelingen.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Controleren of de batchtaak voor het synchroniseren van productbeoordelingen is geslaagd

Ga als volgt te werk om te controleren of de batchtaak voor **synchroniseren van productbeoordelingen** is geslaagd.

1. Ga naar **Detailhandel en commerce \> Systeembeheerder \> Query's \> Batchtaken** of als u een voorraadeenheid (SKU) alleen voor Commerce gebruikt, **Detailhandel en commerce \> Query's en rapporten \> Batchtaken**. U kunt ook zoeken naar "Batchtaken".
1. Als u de details van de batchtaak wilt weergeven, zoekt u in de lijst met batchtaken in de kolom **Taakomschrijving** naar een omschrijving die "Productbeoordelingen ophalen" bevat.
1. Selecteer de taak-id om de details van de batchtaak weer te geven, zoals de geplande begindatum/-tijd en de tekst van het terugkeerpatroon.

In de volgende afbeelding ziet u een voorbeeld van de details van de batchtaak in Commerce wanneer de batchtaak wordt uitgevoerd met een interval van twee uur.

![Details van de batchtaak voor de synchronisatie van productbeoordelingen.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Productbeoordelingen beschikbaar maken op het POS

De oplossing Beoordelingen en recensies in Dynamics 365 Commerce is een omnichannel-oplossing. Productbeoordelingen worden echter niet standaard weergegeven op het POS. Om klanten in winkels de beoordelingen en recensies te laten zien wanneer ze worden geholpen door een verkoopmedewerer, moet u productbeoordelingen inschakelen op het POS.

Voer de volgende stappen uit om productbeoordelingen in te schakelen op het POS.

1. Ga naar **Detailhandel en commerce \> Commerce-instellingen \> Parameters \> Commerce-parameters**. U kunt ook zoeken op "Commerce-parameters".
1. Selecteer **Nieuw** op het tabblad **Configuratieparameters**.
1. Voer een naam in zoals **RatingsAndReviews.EnableproductRatingsForRetailStores**, en stel de waarde in op **true**.
1. Selecteer **Opslaan**.
1. Ga naar **Retail en Commerce \> Retail en Commerce IT \> Distributieplanning**. U kunt ook naar "distributieplanning" zoeken.
1. Selecteer in de takenlijst **1110** (**algemene configuratie**) en selecteer **Nu uitvoeren**.
1. Nadat de taak is uitgevoerd, controleert u of de productbeoordelingen nu op het POS worden weergegeven.

In de volgende afbeelding ziet u een voorbeeld van de configuratie van de Commerce-parameters om productbeoordelingen in te schakelen op het POS.

![Configuratie van Commerce-parameters voor productbeoordelingen op het POS.](media/rnr-hq-enable-ratings-in-pos.png)

In de volgende afbeelding ziet u een voorbeeld van de productbeoordelingen op het POS.

![Productbeoordelingen op het POS.](media/rnr-pos-catalog-ratings.png)

In de volgende afbeelding ziet u een voorbeeld van de productbeoordelingen in callcenterkanalen.

![Productbeoordelingen in een callcenterkanaal.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Aanmelden om beoordelingen en recensies te gebruiken](opt-in-ratings-reviews.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren](sync-product-ratings.md)

[Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator](manual-publish-rating-reviews.md)

[Beoordelingen en recensies importeren en exporteren](import-export-reviews.md)

[Service-to-Service verificatie configureren](service-to-service-auth.md)

[Veelgestelde vragen over beoordelingen en recensies](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
