---
title: Artikelbehoeften voor serviceorders maken
description: Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc65393f74c6daa008e072cbe3745235fbfd896b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743308"
---
# <a name="create-item-requirements-for-service-orders"></a>Artikelbehoeften voor serviceorders maken 

[!include [banner](../includes/banner.md)]


U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren. Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken. Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.

Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.

Artikelbehoeften voor serviceorders worden verwerkt via een project. Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden toegewezen aan een project. Nadat u een artikelbehoefte voor een serviceorder hebt gemaakt, kunt u de artikelbehoefte weergeven in het formulier**Projecten** voor het geselecteerde project.

## <a name="create-an-item-requirement-for-a-service-order"></a>Een artikelbehoefte maken voor een serviceorder

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Selecteer de serviceorder waarvoor u een artikelbehoefte wilt maken.

3.  Klik in het **Actievenster** op het tabblad **Verzenden** op **Artikelbehoefte**.

4.  Voer in het formulier **Artikelbehoeften** de informatie voor het vereiste artikel in. Zie voor meer informatie over de specifieke velden [Artikelbehoeften (formulier)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Een artikelbehoefte maken voor een serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Open de serviceovereenkomst waarvoor u een artikelbehoefte wilt maken.

3.  Klik op het sneltabblad **Regels** op **Toevoegen** om een nieuwe regel te maken.

4.  Selecteer in het veld **Transactietype** **Artikel**.

5.  Selecteer in het veld **Artikelinstellingen** **Artikelbehoefte**.

6.  Selecteer in het veld **Artikelnummer** het artikel dat is vereist voor de serviceovereenkomst.

7.  Selecteer op het sneltabblad **Regeldetails** op het tabblad **Productdimensies** in het veld **Site** de voorraadlocatie voor het artikel.

8.  Als u een serviceorder op basis van de overeenkomstregel wilt maken, klikt u op het sneltabblad **Regels** op **Serviceorders maken** en voert u vervolgens de relevante informatie in het formulier **Serviceorders maken** in. 


## <a name="see-also"></a>Zie ook

[Automatisch serviceorders maken](create-service-orders-automatically.md).

  


