---
title: U kunt een zending niet bevestigen vanwege een probleem met de kalender
description: U kunt een zending niet bevestigen vanwege een probleem met de kalender
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938450"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="408ac-103">U kunt een zending niet bevestigen vanwege een probleem met de kalender</span><span class="sxs-lookup"><span data-stu-id="408ac-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="408ac-104">Foutcode: TRX2716</span><span class="sxs-lookup"><span data-stu-id="408ac-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="408ac-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="408ac-105">Symptoms</span></span>

<span data-ttu-id="408ac-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="408ac-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="408ac-107">Voor het agendatype %1 moet de afspraak %2 worden in- en uitgecheckt.</span><span class="sxs-lookup"><span data-stu-id="408ac-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="408ac-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="408ac-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="408ac-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="408ac-109">Cause</span></span>

<span data-ttu-id="408ac-110">Er bestaan actieve afspraken voor de lading.</span><span class="sxs-lookup"><span data-stu-id="408ac-110">Active appointments for the load exist.</span></span> <span data-ttu-id="408ac-111">Er is bijvoorbeeld een regel die vereist dat de chauffeur moet inchecken.</span><span class="sxs-lookup"><span data-stu-id="408ac-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="408ac-112">Daarom bevindt de lading zich momenteel in een staat waarbij de verzendingsbevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="408ac-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="408ac-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="408ac-113">Resolution</span></span>

<span data-ttu-id="408ac-114">U moet eventuele problemen onderzoeken en oplossen met de actieve afspraken die aan de lading zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="408ac-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="408ac-115">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="408ac-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="408ac-116">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="408ac-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="408ac-117">Selecteer in het actievenster op het tabblad **Transport** in de groep **Afspraken** de optie **Afspraak plannen**.</span><span class="sxs-lookup"><span data-stu-id="408ac-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="408ac-118">Volg één van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="408ac-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="408ac-119">Controleer of voor de afspraak het in- of uitchecken van de chauffeur is voltooid.</span><span class="sxs-lookup"><span data-stu-id="408ac-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="408ac-120">Voltooi of annuleer de afspraak.</span><span class="sxs-lookup"><span data-stu-id="408ac-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="408ac-121">Schakel de optie **Inchecken van chauffeur vereist** voor de bijbehorende afspraakregel uit.</span><span class="sxs-lookup"><span data-stu-id="408ac-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
