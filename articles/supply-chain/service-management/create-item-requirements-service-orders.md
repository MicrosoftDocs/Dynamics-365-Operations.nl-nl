---
title: Artikelbehoeften voor serviceorders maken
description: In dit artikel wordt beschreven hoe u artikelbehoeften voor serviceorders maakt.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2c90ff76121b436d0fec532268cd3383de0eab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888407"
---
# <a name="create-item-requirements-for-service-orders"></a>Artikelbehoeften voor serviceorders maken

[!include [banner](../includes/banner.md)]

U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren. Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken. Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.

Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.

Artikelbehoeften voor serviceorders worden verwerkt via een project. Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden toegewezen aan een project. Nadat u een artikelbehoefte voor een serviceorder hebt gemaakt, kunt u de artikelbehoefte weergeven in het formulier **Projecten** voor het geselecteerde project.

## <a name="create-an-item-requirement-for-a-service-order"></a>Een artikelbehoefte maken voor een serviceorder

1. Ga naar **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.
1. Selecteer de serviceorder waarvoor u een artikelbehoefte wilt maken.
1. Selecteer in het **Actievenster** op het tabblad **Verzenden** de optie **Artikelbehoefte**.
1. Voer in het formulier **Artikelbehoeften** de informatie voor het vereiste artikel in. Zie voor meer informatie over de specifieke velden [Artikelbehoeften (formulier)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Een artikelbehoefte maken voor een serviceovereenkomst

1. Ga naar **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.
1. Open de serviceovereenkomst waarvoor u een artikelbehoefte wilt maken.
1. Selecteer op het sneltabblad **Regels** de optie **Toevoegen** om een nieuwe regel te maken.
1. Selecteer in het veld **Transactietype** **Artikel**.
1. Selecteer in het veld **Artikelinstellingen** **Artikelbehoefte**.
1. Selecteer in het veld **Artikelnummer** het artikel dat is vereist voor de serviceovereenkomst.
1. Selecteer op het sneltabblad **Regeldetails** op het tabblad **Productdimensies** in het veld **Site** de voorraadlocatie voor het artikel.
1. Als u een serviceorder wilt maken op basis van de overeenkomstregel, selecteert u op het sneltabblad **Regels** de optie **Serviceorders maken** en voert u vervolgens de relevante informatie op het formulier **Serviceorders maken** in.

## <a name="see-also"></a>Zie ook

[Automatisch serviceorders maken](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
