---
title: Configuraties leverancieraanvraag
description: In dit onderwerp worden de velden beschreven die moeten worden ingevuld in een nieuwe leverancieraanvraag.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 61ef9ba4eb683fea030f06b3bacf687d7f146de4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246568"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="bd06c-103">Configuraties leverancieraanvraag</span><span class="sxs-lookup"><span data-stu-id="bd06c-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd06c-104">Om een leverancieraanvraag te voltooien, moet de contactpersoon van de leverancier de wizard voor registratie van een potentiële leverancier uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="bd06c-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="bd06c-105">In het formulier **Configuraties leverancieraanvraag** kunt u profielen maken waarmee verplichte en zichtbare velden in de wizard voor registratie van een potentiële leverancier worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="bd06c-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="bd06c-106">In de wizard voor leveranciersregistratie wordt eerst gevraagd in welk land of welke regio de gebruiker van de potentiële leverancier actief is.</span><span class="sxs-lookup"><span data-stu-id="bd06c-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="bd06c-107">Deze gegevens bepalen de toepasselijke configuratie.</span><span class="sxs-lookup"><span data-stu-id="bd06c-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="bd06c-108">Als er geen specifieke configuratie voor een land/regio wordt gedefinieerd, wordt een standaardconfiguratie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bd06c-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="bd06c-109">Een configuratie voor leverancieraanvragen instellen</span><span class="sxs-lookup"><span data-stu-id="bd06c-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="bd06c-110">Standaard is er een leveranciersconfiguratie beschikbaar in het formulier Configuraties leverancieraanvraag.</span><span class="sxs-lookup"><span data-stu-id="bd06c-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="bd06c-111">Het is niet mogelijk om landen/regio's voor de standaardconfiguratie te selecteren, dus het gedeelte **Landen/regio's** kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="bd06c-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="bd06c-112">Klik op **Inkoopbeheer** > **Instelling** > **Leveranciers** en **Configuraties leverancieraanvraag**.</span><span class="sxs-lookup"><span data-stu-id="bd06c-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="bd06c-113">Klik op het tabblad **Velden** om de status van de weergegeven velden in te stellen.</span><span class="sxs-lookup"><span data-stu-id="bd06c-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="bd06c-114">Verborgen (niet zichtbaar)</span><span class="sxs-lookup"><span data-stu-id="bd06c-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="bd06c-115">Weergegeven (zichtbaar, maar niet verplicht)</span><span class="sxs-lookup"><span data-stu-id="bd06c-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="bd06c-116">Vereist (zichtbaar en verplicht)</span><span class="sxs-lookup"><span data-stu-id="bd06c-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="bd06c-117">Klik op het tabblad **Inhoud** om op te geven of er tekst moeten worden weergegeven in de wizard en of de gebruiker van de potentiële leverancier iets moet accepteren voordat deze naar de volgende stap in de wizard gaat.</span><span class="sxs-lookup"><span data-stu-id="bd06c-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="bd06c-118">De bevestiging wordt gevraagd voor alle voorwaarden die de gebruiker moet accepteren om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="bd06c-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="bd06c-119">U kunt ook een bevestigingsbericht opgeven dat wordt weergegeven zodra de wizard is voltooid en u kunt een of meer vragenlijsten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="bd06c-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="bd06c-120">Een leveranciersconfiguratie maken voor een bepaald land of een bepaalde regio</span><span class="sxs-lookup"><span data-stu-id="bd06c-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="bd06c-121">Klik op **Inkoopbeheer** > **Instelling** > **Leveranciers** en **Configuraties leverancieraanvraag**.</span><span class="sxs-lookup"><span data-stu-id="bd06c-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="bd06c-122">Klik op **Nieuw** om een nieuwe configuratie te maken en geef een naam op voor de configuratie.</span><span class="sxs-lookup"><span data-stu-id="bd06c-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="bd06c-123">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bd06c-123">Click **Save**.</span></span>
4.  <span data-ttu-id="bd06c-124">Open het tabblad **Land/regio's** om het land of de regio te selecteren waarvoor de configuratie moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bd06c-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="bd06c-125">Voltooi de configuratie door de richtlijnen voor de standaardconfiguratie te volgen.</span><span class="sxs-lookup"><span data-stu-id="bd06c-125">Complete the configuration by following the guidelines for the default configuration.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]