---
title: Een Azure-opslagaccount en een sleutelkluis maken
description: In dit onderwerp wordt uitgelegd hoe u een Azure-opslagaccount en een sleutelkluis maakt.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104224"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="24aa4-103">Een Azure-opslagaccount en een sleutelkluis maken</span><span class="sxs-lookup"><span data-stu-id="24aa4-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="24aa4-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="24aa4-104">Prerequisites</span></span>

<span data-ttu-id="24aa4-105">Voordat u de stappen in dit onderwerp kunt voltooien, moet u controleren of de volgende zijn uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="24aa4-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="24aa4-106">Maak een sleutelkluis-resource in Azure.</span><span class="sxs-lookup"><span data-stu-id="24aa4-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="24aa4-107">Zie [Over Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="24aa4-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="24aa4-108">Maak een Azure-opslagaccount (Blob-opslag).</span><span class="sxs-lookup"><span data-stu-id="24aa4-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="24aa4-109">Zie [Azure-opslagaccount onderhouden](https://docs.microsoft.com/azure/storage/blobs/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="24aa4-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="24aa4-110">Overzicht</span><span class="sxs-lookup"><span data-stu-id="24aa4-110">Overview</span></span>

<span data-ttu-id="24aa4-111">In dit onderwerp voert u twee belangrijke stappen uit:</span><span class="sxs-lookup"><span data-stu-id="24aa4-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="24aa4-112">Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen.</span><span class="sxs-lookup"><span data-stu-id="24aa4-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="24aa4-113">Stel de sleutelkluis in om de URI van het opslagaccount op te slaan.</span><span class="sxs-lookup"><span data-stu-id="24aa4-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="24aa4-114">Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen</span><span class="sxs-lookup"><span data-stu-id="24aa4-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="24aa4-115">Open het opslagaccount dat u wilt gebruiken met de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="24aa4-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="24aa4-116">Ga naar **Blob-service** \> **Containers** en maak een nieuwe container.</span><span class="sxs-lookup"><span data-stu-id="24aa4-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="24aa4-117">Voer een naam in voor de container en stel het veld **Openbaar toegangsniveau** in op **Privé (geen anonieme toegang)**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="24aa4-118">Open de container en ga naar **instellingen \> Toegangsbeleid**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="24aa4-119">Selecteer **Beleid toevoegen** om een opgeslagen toegangsbeleid toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="24aa4-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="24aa4-120">Stel de velden **ID** en **Machtigingen** naar wens in.</span><span class="sxs-lookup"><span data-stu-id="24aa4-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="24aa4-121">In het veld **Machtigingen** moet u alle machtigingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="24aa4-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Machtiging voor Blob-opslag verlenen](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="24aa4-123">Voer de begin- en vervaldatum in.</span><span class="sxs-lookup"><span data-stu-id="24aa4-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="24aa4-124">De vervaldatum moet in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="24aa4-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="24aa4-125">Selecteer **OK** om het beleid op te slaan en sla uw wijzigingen vervolgens op in de container.</span><span class="sxs-lookup"><span data-stu-id="24aa4-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="24aa4-126">Ga terug naar het opslagaccount en open **Opslagverkenner (Preview)**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="24aa4-127">Klik met de rechtermuisknop op de container en selecteer **Shared Access Signature ophalen**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="24aa4-128">Kopieer in het dialoogvenster **Shared Access Signature** de waarde in het veld **URI** en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="24aa4-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="24aa4-129">Deze waarde wordt in de volgende procedure gebruikt en wordt de *Shared Access Signature-URI* genoemd.</span><span class="sxs-lookup"><span data-stu-id="24aa4-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![De URI-waarde selecteren en kopiëren](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="24aa4-131">Stel de sleutelkluis in om de URI van het opslagaccount op te slaan</span><span class="sxs-lookup"><span data-stu-id="24aa4-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="24aa4-132">Open de sleutelkluis die u wilt gebruiken met de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="24aa4-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="24aa4-133">Ga naar **instellingen** \> **Geheimen** en selecteer **Genereren/importeren** om een nieuw geheim te maken.</span><span class="sxs-lookup"><span data-stu-id="24aa4-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="24aa4-134">Selecteer op de pagina **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="24aa4-135">Voer de naam van het geheim in.</span><span class="sxs-lookup"><span data-stu-id="24aa4-135">Enter the name of the secret.</span></span> <span data-ttu-id="24aa4-136">Deze naam wordt gebruikt tijdens de installatie van de service in Regulatory Configuration Service (RCS) en wordt de *geheime naam van de sleutelkluis* genoemd.</span><span class="sxs-lookup"><span data-stu-id="24aa4-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="24aa4-137">Selecteer in het veld **Waarde** de **Shared Access Signature URI** en selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="24aa4-138">Stel het toegangsbeleid in om de invoegtoepassing voor elektronische facturering het juiste niveau van beveiligde toegang te verlenen tot het geheim dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="24aa4-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="24aa4-139">Ga naar **Instellingen \> Toegangsbeleid** en selecteer **Toegangsbeleid toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="24aa4-140">Stel de geheime machtigingen voor de bewerkingen **Get** en **List** in.</span><span class="sxs-lookup"><span data-stu-id="24aa4-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Toegang tot de service verlenen](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="24aa4-142">Stel de certificaatmachtigingen voor de bewerkingen **Get** en **List** in.</span><span class="sxs-lookup"><span data-stu-id="24aa4-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Certificaatmachtiging verlenen](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="24aa4-144">Selecteer in het veld **Principal** de principal door **Invoegtoepassing voor elektronische facturering** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="24aa4-144">In the **Principal** dialog box, select the principal by adding **Electronic invoicing add-on**.</span></span>
10. <span data-ttu-id="24aa4-145">Selecteer **Toevoegen** en selecteer **Sleutelkluiswijzigingen opslaan**.</span><span class="sxs-lookup"><span data-stu-id="24aa4-145">Select **Add**, and then select **Save Key Vault changes**.</span></span>
11. <span data-ttu-id="24aa4-146">Kopieer op de pagina **Overzicht** de **DNS-naam**-waarde voor de sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="24aa4-146">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="24aa4-147">Deze waarde wordt gebruikt tijdens de installatie van de service in RCS en wordt de *sleutel-kluis-URI* genoemd.</span><span class="sxs-lookup"><span data-stu-id="24aa4-147">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>
