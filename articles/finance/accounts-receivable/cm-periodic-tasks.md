---
title: Periodieke taken voor kredietbeheer
description: In dit onderwerp worden de periodieke taken beschreven die een noodzakelijk onderdeel zijn van het proces voor het beheren van kredietlimieten voor klanten.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: df3b0b239fe542eab80fa92057248328d3f5188f
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015178"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="d743a-103">Periodieke taken voor kredietbeheer</span><span class="sxs-lookup"><span data-stu-id="d743a-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d743a-104">In dit onderwerp worden de periodieke taken beschreven die een noodzakelijk onderdeel zijn van het proces voor het beheren van kredietlimieten voor klanten.</span><span class="sxs-lookup"><span data-stu-id="d743a-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="d743a-105">Risicoscores bijwerken</span><span class="sxs-lookup"><span data-stu-id="d743a-105">Update risk scores</span></span>

<span data-ttu-id="d743a-106">Naarmate bedrijven zich ontwikkelen en omstandigheden veranderen, is het mogelijk dat de kredietrisico's voor een bepaalde klant ook veranderen.</span><span class="sxs-lookup"><span data-stu-id="d743a-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="d743a-107">Om de benodigde kredietlimieten voor uw klanten te onderhouden, moet u regelmatig de criteria voor elke risicoscore controleren en de scores voor elke klant bijwerken.</span><span class="sxs-lookup"><span data-stu-id="d743a-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="d743a-108">U kunt de volgende scores bijwerken op de pagina **Risicoscores bijwerken** (**Crediteringen en aanmaningen \> Periodieke taken \> Kredietbeheer \> Risicoscores bijwerken**).</span><span class="sxs-lookup"><span data-stu-id="d743a-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="d743a-109">Alle door de gebruiker gedefinieerde berekeningen worden ook verwerkt.</span><span class="sxs-lookup"><span data-stu-id="d743a-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="d743a-110">**Gemiddeld aantal betaaldagen**: deze score is het gemiddelde aantal dagen waarop een klant facturen gaat betalen.</span><span class="sxs-lookup"><span data-stu-id="d743a-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="d743a-111">**Klant sinds**: deze score is het aantal jaar dat een klant klant is van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="d743a-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="d743a-112">**Doet zaken sinds**: deze score is het aantal jaar dat een klant zaken doet.</span><span class="sxs-lookup"><span data-stu-id="d743a-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="d743a-113">Hiervoor wordt de waarde van het veld **Begin bedrijf** op de pagina **Klanten** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d743a-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="d743a-114">**Dagen uitstaande verkoop**: deze score is gebaseerd op het saldo van de klant, de omzet en het aantal dagen voor de vorige periode van twaalf maanden.</span><span class="sxs-lookup"><span data-stu-id="d743a-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="d743a-115">**Gemiddeld saldo** : deze score is gebaseerd op het saldo van de klant voor de vorige periode van twaalf maanden.</span><span class="sxs-lookup"><span data-stu-id="d743a-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="d743a-116">**Kredietbeheergroep**, **Rekeningstatus** en **Land** : deze scores gebruiken gegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="d743a-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="d743a-117">Saldostatistieken van klant bijwerken</span><span class="sxs-lookup"><span data-stu-id="d743a-117">Update customer balance statistics</span></span>

<span data-ttu-id="d743a-118">U kunt het proces **Saldostatistieken van klant bijwerken** uitvoeren om de berekening van saldostatistieken bij te werken die worden weergegeven op de pagina **Saldostatistieken opvragen**.</span><span class="sxs-lookup"><span data-stu-id="d743a-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="d743a-119">Deze informatie wordt gebruikt voor het berekenen van risicoscores en de waarden die worden weergegeven in de feitenblokken met kredietstatistieken op de pagina **Klant**.</span><span class="sxs-lookup"><span data-stu-id="d743a-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="d743a-120">Wanneer u het proces uitvoert, worden saldostatistieken voor één klant bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="d743a-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="d743a-121">Als u een batchtaak wilt instellen om het proces uit te voeren voor meerdere klanten, kunt de pagina **Saldostatistieken berekenen** gebruiken (**Kredietbeheer \> Periodieke taken \> Saldostatistieken berekenen**).</span><span class="sxs-lookup"><span data-stu-id="d743a-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
