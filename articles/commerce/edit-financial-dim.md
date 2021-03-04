---
title: Financiële dimensies voor detailhandelstransacties bewerken
description: In dit onderwerp wordt beschreven hoe u financiële dimensies bewerkt voor detailhandelstransacties in Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010170"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Financiële dimensies voor detailhandelstransacties bewerken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u financiële dimensies bewerkt voor detailhandelstransacties in Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Financiële dimensies bewerken

Voer de volgende stappen uit om financiële dimensies voor detailhandelstransacties in Commerce Headquarters te bewerken.

1. Open de pagina **Configuratie van financiële dimensies voor het integreren van toepassingen**.
1. Selecteer de actieve record **Integratie van standaarddimensies**.
1. Controleer op het sneltabblad **Financiële dimensies** of alle dimensies die u in het Excel-werkblad wilt bewerken, aanwezig zijn in de lijst **Geselecteerd**. Zie [Gegevensentiteiten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities) voor meer informatie.
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
