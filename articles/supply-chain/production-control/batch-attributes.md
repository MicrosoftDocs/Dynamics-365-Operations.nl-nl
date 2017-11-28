---
title: Batchkenmerken
description: Dit onderwerp biedt informatie over batchkenmerken. Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen. In het onderwerp wordt ook uitgelegd hoe u batchkenmerken toewijst en hoe u erop kunt zoeken wanneer u batches reserveert.
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6c18b007a72686b1ede69b750e930d72e86f0aba
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="batch-attributes"></a>Batchkenmerken

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over batchkenmerken. Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen. In het onderwerp wordt ook uitgelegd hoe u batchkenmerken toewijst en hoe u erop kunt zoeken wanneer u batches reserveert.

Batchkenmerken zijn eigenschappen van grondstoffen en eindproducten die samen voorraadbatches vormen. Batchkenmerken kunnen verschillen, afhankelijk van zaken als omgevingsfactoren, de kwaliteit van de grondstoffen waarmee de batch wordt geproduceerd of het resultaat van het eindproduct. Het aantal en de typen batchkenmerken die worden gebruikt, kunnen aanzienlijk verschillen per bedrijfstak. Hierna volgen twee voorbeelden van het gebruik van batchkenmerken:

-   In de kaashandel is melk een van de grondstoffen voor de kaasproductie. Deze kan kenmerken hebben, zoals vetgehalte en percentagegewicht. De kaas die wordt geproduceerd van de melk kan andere kenmerken hebben, zoals vochtgehalte en ouderdom.
-   In de staalindustrie kan het ijzer dat wordt geproduceerd kenmerken hebben zoals het magnesium-, zilver- en zinkpercentage.

U kunt het aantal en de typen kenmerken beter beheren door batchkenmerkgroepen te gebruiken. Op deze manier hoeft u niet elk kenmerk afzonderlijk toe te voegen.

## <a name="assign-batch-attributes"></a>Batchkenmerken toewijzen
U kunt batchkenmerken toewijzen aan afzonderlijke producten die zijn opgeslagen in voorraadbatches of aan producten die zijn gekoppeld aan specifieke klanten. Voordat u een batchkenmerk kunt toewijzen op klantniveau, moet u dit eerst toewijzen op productniveau. Het product moet een batchdimensie hebben die is ingesteld op **Actief** in de trackingdimensiegroep. Gebruik de productgebonden pagina om een batchkenmerk toe te wijzen aan een afzonderlijk product. Gebruik de klantgebonden pagina als het kenmerk specifiek is voor een product voor een bepaalde klant. Wanneer u een kenmerk toevoegt aan een product, definieert u ook andere parameters. Hieronder vindt u enkele voorbeelden:

-   Het minimum- en maximumbereik voor een kenmerk van het type **Geheel getal** of **Breuk**.
-   De tolerantieacties voor een kenmerk van het type **Geheel getal** of **Breuk**. Als de waarde van het kenmerk buiten het minimum- of maximumbereik valt, kan de actie een waarschuwingsbericht zijn of een foutbericht.
-   De doelwaarde voor het kenmerk. Dit is de optimale waard van het kenmerk, die van toepassing is op alle kenmerktypen.

U kunt de pagina's openen voor producten die u selecteert op de pagina **Vrijgegeven producten** in Productgegevensbeheer. Wanneer u batchkenmerken aan een product hebt toegewezen, kunt u vervolgens specifieke waarden toevoegen aan de kenmerken op de pagina **Voorraadbatchkenmerken**.

## <a name="reserve-batches"></a>Reservebatches
U kunt zoeken op batchkenmerken wanneer u batchreserveringen voor een verkooporder uitvoert om de order van een klant te vervullen of bij het verzamelen en reserveren van batches voor een productieorder. De zoekactie helpt bij het opsporen van een voorraadbatch die het product bevat met de batchkenmerken die u wilt. Nadat u de batch of batches hebt gevonden, kunt u het product reserveren voor de oorspronkelijke voorraadtransactieregel.




