---
title: Gegevensvelden toevoegen in belastingconfiguraties
description: In dit onderwerp wordt uitgelegd hoe u belastingconfiguraties aanpast door gegevensvelden toe te voegen.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921184"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="8f2e1-103">Gegevensvelden toevoegen in belastingconfiguraties</span><span class="sxs-lookup"><span data-stu-id="8f2e1-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f2e1-104">In dit onderwerp wordt uitgelegd hoe u belastingconfiguraties aanpast met behulp van [gegevensvelden die worden toegevoegd in de belastingintegratie](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="8f2e1-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="8f2e1-105">Het belastinggegevensmodel aanpassen</span><span class="sxs-lookup"><span data-stu-id="8f2e1-105">Customize the tax data model</span></span>

1. <span data-ttu-id="8f2e1-106">Ga in Microsoft Dynamics 365 Finance naar **Elektronische rapportage** \> **Belastingconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="8f2e1-107">Selecteer **Belastinggegevensmodel - Europa** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="8f2e1-108">Selecteer vervolgens **Configuratie maken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="8f2e1-109">Selecteer in het dialoogvenster met vervolgkeuzemenu de optie **Belastingdocumentmodel afgeleid van Naam: Belastinggegevensmodel - Europa, Microsoft**, voer een naam in voor het nieuwe belastinggegevensmodel en selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="8f2e1-110">Selecteer het belastinggegevensmodel dat u zojuist hebt gemaakt en selecteer vervolgens **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="8f2e1-111">Vouw de gegevensmodelstructuur uit, selecteer **Regels** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="8f2e1-112">Voer in het dialoogvenster **Knooppunt maken** een naam in, geef het itemtype op en selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="8f2e1-113">Voeg de vereiste kolommen toe.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-113">Add any required columns.</span></span>
8. <span data-ttu-id="8f2e1-114">Selecteer in het actievenster **Opslaan** en vervolgens **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="8f2e1-115">Sluit de pagina en bekijk de voltooide versie van uw belastinggegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="8f2e1-116">De belastingconfiguratie aanpassen</span><span class="sxs-lookup"><span data-stu-id="8f2e1-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="8f2e1-117">Ga in Finance naar **Elektronische rapportage** \> **Belastingconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="8f2e1-118">Selecteer **Belastingconfiguratie -- Europa** in de configuratiestructuur.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="8f2e1-119">Selecteer vervolgens **Configuratie maken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="8f2e1-120">Selecteer in het dialoogvenster met vervolgkeuzemenu de optie **Belastingserviceconfiguratie afgeleid van Naam: Belastingconfiguratie - Europa, Microsoft**, voer een naam in voor de nieuwe belastingconfiguratie en selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="8f2e1-121">Selecteer de belastingconfiguratie die u zojuist hebt gemaakt en selecteer vervolgens **Ontwerper** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="8f2e1-122">Selecteer in de sectie **Eigenschappen** in het veld **Gegevensmodel** het aangepaste belastinggegevensmodel dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="8f2e1-123">Selecteer in het veld **Gegevensmodelversie** de voltooide versie van het belastinggegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="8f2e1-124">Selecteer **Toevoegen** en voeg de vereiste belastingmaatregelen toe.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="8f2e1-125">Selecteer in het actievenster **Opslaan** en vervolgens **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="8f2e1-126">Sluit de pagina en bekijk de voltooide versie van uw belastingconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="8f2e1-127">Belastingfuncties implementeren in de aangepaste belastingconfiguratie</span><span class="sxs-lookup"><span data-stu-id="8f2e1-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="8f2e1-128">Ga in Regulatory Configuration Services (RCS) naar **Globalisatiefuncties** \> **Belasting**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="8f2e1-129">Selecteer **Toevoegen**, voer informatie over de nieuwe functie in en selecteer vervolgens **Functie maken**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="8f2e1-130">Selecteer de de functie op het tabblad **Versies** en selecteer vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="8f2e1-131">Selecteer op het tabblad **Algemeen** in het veld **Configuratieversie** de aangepaste belastingconfiguratie en -versie.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="8f2e1-132">Selecteer in het dialoogvenster **Kolommen beheren** de kop- en regelkolommen die u wilt opnemen in uw aangepaste belastingmaatregel en selecteer vervolgens de juiste pijl-knop om ze toe te voegen aan de lijst **Geselecteerde kolommen**.</span><span class="sxs-lookup"><span data-stu-id="8f2e1-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
