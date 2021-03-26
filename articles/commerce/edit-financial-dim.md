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
ms.openlocfilehash: 4d4b7e383ca2089ee98e70d23ccd890d0e6a86c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221793"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="f1bea-103">Financiële dimensies voor detailhandelstransacties bewerken</span><span class="sxs-lookup"><span data-stu-id="f1bea-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1bea-104">In dit onderwerp wordt beschreven hoe u financiële dimensies bewerkt voor detailhandelstransacties in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1bea-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="f1bea-105">Financiële dimensies bewerken</span><span class="sxs-lookup"><span data-stu-id="f1bea-105">Edit financial dimensions</span></span>

<span data-ttu-id="f1bea-106">Voer de volgende stappen uit om financiële dimensies voor detailhandelstransacties in Commerce Headquarters te bewerken.</span><span class="sxs-lookup"><span data-stu-id="f1bea-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f1bea-107">Open de pagina **Configuratie van financiële dimensies voor het integreren van toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="f1bea-108">Selecteer de actieve record **Integratie van standaarddimensies**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="f1bea-109">Controleer op het sneltabblad **Financiële dimensies** of alle dimensies die u in het Excel-werkblad wilt bewerken, aanwezig zijn in de lijst **Geselecteerd**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="f1bea-110">Zie [Gegevensentiteiten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f1bea-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="f1bea-111">Download en open het Excel-bestand op de pagina **Overzichten**, de pagina **Detailhandelstransacties** of de tegel **Fouten in transactievalidatie** in het werkgebied **Financiën van winkel**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="f1bea-112">Als u de financiële dimensie van de transactie wilt wijzigen, selecteert u **Ontwerpen** en vervolgens het potloodsymbool naast de rij **Transactie (controleerbaar)**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="f1bea-113">Zoek en selecteer het veld **FinancialDimensionDisplayValue**, selecteer een cel in het kopgedeelte van het Excel-werkblad en selecteer **Label toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="f1bea-114">Selecteer een cel onder de cel die u in de vorige stap hebt geselecteerd, selecteer **Waarde toevoegen** en vervolgens **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="f1bea-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="f1bea-115">De financiële dimensies worden toegevoegd aan het Excel-werkblad en kunnen vervolgens worden bewerkt en gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="f1bea-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="f1bea-116">Als u de afmetingen op de transactieregels wilt wijzigen, selecteert u de rij **Verkooptransacties (controleerbaar)** of het potloodsymbool, en herhaalt u stap 6 en 7.</span><span class="sxs-lookup"><span data-stu-id="f1bea-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="f1bea-117">Als u de afmetingen op de betalingsregels wilt wijzigen, selecteert u de rij **Betalingstransacties (controleerbaar)** of het potloodsymbool, en herhaalt u stap 6 en 7.</span><span class="sxs-lookup"><span data-stu-id="f1bea-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1bea-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f1bea-118">Additional resources</span></span>

[<span data-ttu-id="f1bea-119">Beheer van contante transacties bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="f1bea-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="f1bea-120">Online orders en asynchrone ordertransacties van klanten bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="f1bea-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="f1bea-121">Een Excel-werkmap maken om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="f1bea-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="f1bea-122">Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="f1bea-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]