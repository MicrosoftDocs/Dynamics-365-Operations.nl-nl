---
title: Artikelbehoeften bij serviceorders
description: Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 880d41a5b3d8c9200a0a1f4b13af2d6d24d30766
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-item-requirements"></a>Artikelbehoeften bij serviceorders   

[!include [banner](../includes/banner.md)]


U kunt een serviceorder maken om services, die u aan uw klanten levert, bij te houden en te beheren. Als u specifieke artikelen voor een serviceorder moet reserveren, kunt u er voorraadartikelbehoeften voor maken. Een artikelbehoefte kan direct worden verbruikt vanuit de voorraad, of er kan een productieorder of inkooporder voor het artikel mee worden geïnitialiseerd.

Door een artikelbehoefte te maken in plaats van een artikeltransactie kunt u de levering plannen vlak voordat het artikel werkelijk wordt gebruikt, een inkooporder maken, het artikel opnemen in het handelsovereenkomstframework en de artikelbehoefte opnemen in de productieplanning.

Artikelbehoeften voor serviceorders worden verwerkt via een project. Als u een artikelbehoefte wilt maken voor een serviceorder, moet de serviceorder worden gekoppeld aan een project.

Zodra een artikelbehoefte is gemaakt voor een serviceorder, kunt u deze weergeven via **Project** in de afzonderlijke serviceorder of via het formulier **Verkooporder**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Een artikelbehoefte voor een serviceorder weergeven

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Klik op **Verzending** en klik vervolgens op **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen.

3.  Klik op het tabblad **Project** en selecteer vervolgens het veld **Serviceorder** in om de serviceorders van de artikelbehoefte te bekijken.

## <a name="delete-service-orders-with-item-requirements"></a>Serviceorders met artikelbehoeften verwijderen

Als u een artikelbehoefte hebt gemaakt voor een serviceorder, kunt u de serviceorder niet verwijderen. U moet de artikelbehoefte verwijderen, voordat u de serviceorder kunt verwijderen.

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Klik op **Verzending** en klik vervolgens op **Artikelbehoefte** om het formulier **Artikelbehoeften** te openen. Dit formulier bevat een lijst met alle artikelbehoeften die voor de serviceorder zijn gemaakt.

3.  Selecteer de artikelbehoefte die u wilt verwijderen en klik vervolgens op **Verwijderen**.

– of –

1.  Klik op **Projectbeheer en boekhouding** \> **Algemeen** \> **Projecten** \> **Alle projecten**.

2.  Open het project met de serviceorder waarin een artikelbehoefte wordt gemaakt.

3.  In het formulier **Projecten** in het rechterdeelvenster klikt u op **Artikelbehoeften**. Het formulier **Artikelbehoeften** wordt geopend met de artikelbehoeften die aan het geselecteerde project zijn gekoppeld.

4.  Selecteer de artikelbehoefte die u wilt verwijderen en klik vervolgens op **Verwijderen**.

## <a name="see-also"></a>Zie ook

[Artikelbehoeften (formulier)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))


