---
title: Testinstrumenten voor kwaliteitsbeheer
description: In dit onderwerp wordt beschreven hoe u testinstrumenten maakt die kunnen worden gebruikt voor het testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956610"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="26044-103">Testinstrumenten voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="26044-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26044-104">In dit onderwerp wordt beschreven hoe u testinstrumenten maakt die kunnen worden gebruikt voor het testen van kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="26044-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="26044-105">U gebruikt de pagina **Testinstrumenten** voor het definiëren en weergeven van details over de apparaten die worden gebruikt om kwaliteitsorders te testen.</span><span class="sxs-lookup"><span data-stu-id="26044-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="26044-106">Testinstrumenten zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="26044-106">Test instruments are optional.</span></span> <span data-ttu-id="26044-107">Ze kunnen kwaliteitsmedewerkers echter wel helpen om erachter te komen welk apparaat of hulpprogramma ze moeten gebruiken om een specifieke test uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="26044-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="26044-108">Voorbeeld van testinstrument</span><span class="sxs-lookup"><span data-stu-id="26044-108">Test instrument example</span></span>

<span data-ttu-id="26044-109">U voert verschillende tests uit op elektrische onderdelen.</span><span class="sxs-lookup"><span data-stu-id="26044-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="26044-110">Sommige tests zijn bedoeld om het voltage van de onderdelen te testen, één test is er om de temperatuur te testen en één test is er om hun gewicht te testen.</span><span class="sxs-lookup"><span data-stu-id="26044-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="26044-111">Er worden verschillende hulpmiddelen, apparaten of apparatuur gebruikt om elke test uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="26044-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="26044-112">Een voltmeter wordt bijvoorbeeld gebruikt om het voltage te meten, een thermometer wordt gebruikt om de temperatuur te meten en een weegschaal wordt gebruikt om het gewicht te meten.</span><span class="sxs-lookup"><span data-stu-id="26044-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="26044-113">U kunt elk van deze apparaten configureren als een testinstrument en de maateenheid aangeven waarin de testresultaten moeten worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="26044-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="26044-114">Resultaten van de voltmeter worden bijvoorbeeld vastgelegd in volt, resultaten van de thermometer worden vastgelegd in graden Fahrenheit of Celsius en de resultaten van de weegschaal worden vastgelegd in ponden of kilogrammen.</span><span class="sxs-lookup"><span data-stu-id="26044-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="26044-115">Een testinstrument maken</span><span class="sxs-lookup"><span data-stu-id="26044-115">Create a test instrument</span></span>

1. <span data-ttu-id="26044-116">Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Testinstrumenten**.</span><span class="sxs-lookup"><span data-stu-id="26044-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="26044-117">Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.</span><span class="sxs-lookup"><span data-stu-id="26044-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="26044-118">Stel daarna de volgende velden in voor de nieuwe rij:</span><span class="sxs-lookup"><span data-stu-id="26044-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="26044-119">**Testinstrument**: voer een unieke id of naam voor het testinstrument in.</span><span class="sxs-lookup"><span data-stu-id="26044-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="26044-120">**Beschrijving**: voer een gedetailleerde beschrijving voor het testinstrument in.</span><span class="sxs-lookup"><span data-stu-id="26044-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="26044-121">**Eenheid**: selecteer de eenheid waarin het instrument de resultaten meet.</span><span class="sxs-lookup"><span data-stu-id="26044-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="26044-122">Het veld **Precisie** wordt automatisch ingesteld op basis van de eenheid die u selecteert.</span><span class="sxs-lookup"><span data-stu-id="26044-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="26044-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26044-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26044-124">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="26044-124">Additional resources</span></span>

- [<span data-ttu-id="26044-125">Kwaliteitsbeheertests</span><span class="sxs-lookup"><span data-stu-id="26044-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="26044-126">Testgroepen voor kwaliteitsbeheer</span><span class="sxs-lookup"><span data-stu-id="26044-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
