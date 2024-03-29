---
title: Een product configureren dat gratis kan worden aangeschaft
description: In dit artikel wordt beschreven hoe u een product zo configureert dat het gratis kan worden aangeschaft in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280359"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Een product configureren dat gratis kan worden aangeschaft

[!include [banner](includes/banner.md)]


In dit artikel wordt beschreven hoe u een product zo configureert dat het gratis kan worden aangeschaft in Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Het product configureren

Als u een product gratis in Dynamics 365 Commerce wilt verkopen, moet u de prijs van het product instellen op 0 (nul). U moet ook de instelling **Aanvangsprijs geldig** van het product configureren.

Volg deze stappen om de **Aanvangsprijs geldig** te configureren in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Vrijgegeven producten per categorie**.
1. Ga naar het product dat u gratis wilt verkopen. 
1. Stel in de sectie **Commerce** van de productpagina de optie **Aanvangsprijs geldig** in op **Ja**.

De onderstaande afbeelding toont een voorbeeld van een product waarbij de optie **Aanvangsprijs geldig** is ingesteld op **Ja**.

![Voorbeeld van een product waarbij de optie Aanvangsprijs geldig is ingesteld op Ja.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Het functionaliteitsprofiel van de onlinewinkel configureren

Voordat vrije transacties kunnen worden verwerkt, moet u de instelling **Uitchecken zonder betalingen toestaan** configureren van het functionaliteitsprofiel voor uw onlinewinkel zodat transacties zonder betalingen zijn toegestaan. Zie [Een online functionaliteitsprofiel maken](online-functionality-profile.md) voor informatie over het maken van functionaliteitsprofielen.

Volg deze stappen om de instelling **Uitchecken zonder betalingen toestaan** te configureren in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Onlinewinkel instellen**.
1. Stel op de pagina voor het functionaliteitsprofiel van uw winkel onder **Uitchecken** de optie **Uitchecken zonder betalingen toestaan** in op **Ja**.

De volgende afbeelding toont een voorbeeld van een onlinewinkelprofiel waarbij de optie **Uitchecken zonder betalingen toestaan** is ingesteld op **Ja**.

![Voorbeeld van een onlinewinkelprofiel waarbij de optie Uitchecken zonder betalingen toestaan is ingesteld op Ja.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Verkoopprijsbeheer van detailhandel](price-management.md)

[Een online functionaliteitsprofiel maken](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
