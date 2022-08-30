---
title: Financiële dimensies voor detailhandelstransacties bewerken
description: In dit artikel wordt beschreven hoe u financiële dimensies bewerkt voor detailhandelstransacties in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: b382907cd79a13319601dd694261319875565947
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268389"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Financiële dimensies voor detailhandelstransacties bewerken

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u financiële dimensies bewerkt voor detailhandelstransacties in Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Financiële dimensies bewerken

Voer de volgende stappen uit om financiële dimensies voor detailhandelstransacties in Commerce Headquarters te bewerken.

1. Open de pagina **Configuratie van financiële dimensies voor het integreren van toepassingen**.
1. Selecteer de actieve record **Integratie van standaarddimensies**.
1. Controleer op het sneltabblad **Financiële dimensies** of alle dimensies die u in het Excel-werkblad wilt bewerken, aanwezig zijn in de lijst **Geselecteerd**. Zie [Gegevensentiteiten](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities) voor meer informatie.
1. Download en open het Excel-bestand op de pagina **Overzichten**, de pagina **Detailhandelstransacties** of de tegel **Fouten in transactievalidatie** in het werkgebied **Financiën van winkel**.
1. Als u de financiële dimensie van de transactie wilt wijzigen, selecteert u **Ontwerpen** en vervolgens het potloodsymbool naast de rij **Transactie (controleerbaar)**.
1. Zoek en selecteer het veld **FinancialDimensionDisplayValue**, selecteer een cel in het kopgedeelte van het Excel-werkblad en selecteer **Label toevoegen**.
1. Selecteer een cel onder de cel die u in de vorige stap hebt geselecteerd, selecteer **Waarde toevoegen** en vervolgens **Vernieuwen**. De financiële dimensies worden toegevoegd aan het Excel-werkblad en kunnen vervolgens worden bewerkt en gepubliceerd.
1. Als u de afmetingen op de transactieregels wilt wijzigen, selecteert u de rij **Verkooptransacties (controleerbaar)** of het potloodsymbool, en herhaalt u stap 6 en 7.
1. Als u de afmetingen op de betalingsregels wilt wijzigen, selecteert u de rij **Betalingstransacties (controleerbaar)** of het potloodsymbool, en herhaalt u stap 6 en 7.

## <a name="additional-resources"></a>Aanvullende bronnen

[Beheer van contante transacties bewerken en controleren](edit-cash-trans.md)

[Online orders en asynchrone ordertransacties van klanten bewerken en controleren](edit-order-trans.md)

[Een Excel-werkmap maken om detailhandelstransacties te bewerken](create-excel-edit.md)

[Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
