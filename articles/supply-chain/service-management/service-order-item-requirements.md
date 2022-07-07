---
title: Artikelbehoeften bij serviceorder
description: In dit artikel worden de artikelbehoeften bij serviceorders beschreven.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 376cda6bbe1800611e6f24c347b9035469a30a14
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015167"
---
# <a name="service-order-item-requirements"></a>Artikelbehoeften bij serviceorder

[!include [banner](../includes/banner.md)]

U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren. Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken. Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.

Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.

Artikelbehoeften voor serviceorders worden verwerkt via een project. Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden gekoppeld aan een project.

Zodra een artikelbehoefte is gemaakt voor een serviceorder, kunt u deze weergeven via **Project** in de afzonderlijke serviceorder of via het formulier **Verkooporder**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Een artikelbehoefte voor een serviceorder weergeven

1. Ga naar **Servicebeheer** \> **Serviceorders** \> **Serviceorders**.
1. Selecteer **Verzenden** en selecteer vervolgens **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen.
1. Selecteer het tabblad **Project** en selecteer vervolgens het veld **Serviceorder** om de serviceorders van de artikelbehoefte te bekijken.

## <a name="delete-service-orders-with-item-requirements"></a>Serviceorders met artikelbehoeften verwijderen

Als u een artikelbehoefte hebt gemaakt voor een serviceorder, kunt u de serviceorder niet verwijderen. U moet de artikelbehoefte verwijderen, voordat u de serviceorder kunt verwijderen.

1. Ga naar **Servicebeheer** \> **Serviceorders** \> **Serviceorders**.
1. Selecteer **Verzenden** en selecteer vervolgens **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen. Dit formulier bevat een lijst met alle artikelbehoeften die voor de serviceorder zijn gemaakt.
1. Selecteer de artikelbehoefte die u wilt verwijderen en selecteer vervolgens **Verwijderen**.

– of –

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.
1. Open het project met de serviceorder waarin een artikelbehoefte wordt gemaakt.
1. Selecteer in het formulier **Projecten** in het rechterdeelvenster de optie **Artikelbehoeften**. Het formulier **Artikelbehoeften** wordt geopend met de artikelbehoeften die aan het geselecteerde project zijn gekoppeld.
1. Selecteer de artikelbehoefte die u wilt verwijderen en selecteer vervolgens **Verwijderen**.

## <a name="see-also"></a>Zie ook

[Artikelbehoeften (formulier)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]