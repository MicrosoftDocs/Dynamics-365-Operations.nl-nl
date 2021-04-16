---
title: Een Azure-opslagaccount en een sleutelkluis maken
description: In dit onderwerp wordt uitgelegd hoe u een Azure-opslagaccount en een sleutelkluis maakt.
author: gionoder
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b7df4933c1373893e00f48ea3a21bd5af40719a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840215"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="38729-103">Een Azure-opslagaccount en een sleutelkluis maken</span><span class="sxs-lookup"><span data-stu-id="38729-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="38729-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="38729-104">Prerequisites</span></span>

<span data-ttu-id="38729-105">Voordat u de stappen in dit onderwerp kunt voltooien, moet u controleren of de volgende zijn uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="38729-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="38729-106">Maak een sleutelkluis-resource in Azure.</span><span class="sxs-lookup"><span data-stu-id="38729-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="38729-107">Zie [Over Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="38729-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="38729-108">Maak een Azure-opslagaccount (Blob-opslag).</span><span class="sxs-lookup"><span data-stu-id="38729-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="38729-109">Zie [Azure-opslagaccount onderhouden](https://docs.microsoft.com/azure/storage/blobs/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="38729-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="38729-110">Overzicht</span><span class="sxs-lookup"><span data-stu-id="38729-110">Overview</span></span>

<span data-ttu-id="38729-111">In dit onderwerp voert u twee belangrijke stappen uit:</span><span class="sxs-lookup"><span data-stu-id="38729-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="38729-112">Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen.</span><span class="sxs-lookup"><span data-stu-id="38729-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="38729-113">Stel de sleutelkluis in om de URI van het opslagaccount op te slaan.</span><span class="sxs-lookup"><span data-stu-id="38729-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="38729-114">Stel het Azure-opslagaccount in om de URI van het opslagaccount op te halen</span><span class="sxs-lookup"><span data-stu-id="38729-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="38729-115">Open het opslagaccount dat u wilt gebruiken met Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="38729-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="38729-116">Ga naar **Blob-service** \> **Containers** en maak een nieuwe container.</span><span class="sxs-lookup"><span data-stu-id="38729-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="38729-117">Voer een naam in voor de container en stel het veld **Openbaar toegangsniveau** in op **Privé (geen anonieme toegang)**.</span><span class="sxs-lookup"><span data-stu-id="38729-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="38729-118">Open de container en ga naar **instellingen \> Toegangsbeleid**.</span><span class="sxs-lookup"><span data-stu-id="38729-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="38729-119">Selecteer **Beleid toevoegen** om een opgeslagen toegangsbeleid toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="38729-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="38729-120">Stel de velden **ID** en **Machtigingen** naar wens in.</span><span class="sxs-lookup"><span data-stu-id="38729-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="38729-121">In het veld **Machtigingen** moet u alle machtigingen selecteren.</span><span class="sxs-lookup"><span data-stu-id="38729-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Machtiging voor Blob-opslag verlenen](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="38729-123">Voer de begin- en vervaldatum in.</span><span class="sxs-lookup"><span data-stu-id="38729-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="38729-124">De vervaldatum moet in de toekomst liggen.</span><span class="sxs-lookup"><span data-stu-id="38729-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="38729-125">Selecteer **OK** om het beleid op te slaan en sla uw wijzigingen vervolgens op in de container.</span><span class="sxs-lookup"><span data-stu-id="38729-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="38729-126">Ga terug naar het opslagaccount en open **Opslagverkenner (Preview)**.</span><span class="sxs-lookup"><span data-stu-id="38729-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="38729-127">Klik met de rechtermuisknop op de container en selecteer **Shared Access Signature ophalen**.</span><span class="sxs-lookup"><span data-stu-id="38729-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="38729-128">Kopieer in het dialoogvenster **Shared Access Signature** de waarde in het veld **URI** en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="38729-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="38729-129">Deze waarde wordt in de volgende procedure gebruikt en wordt de *Shared Access Signature-URI* genoemd.</span><span class="sxs-lookup"><span data-stu-id="38729-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![De URI-waarde selecteren en kopiëren](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="38729-131">Stel de sleutelkluis in om de URI van het opslagaccount op te slaan</span><span class="sxs-lookup"><span data-stu-id="38729-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="38729-132">Open de sleutelkluis die u wilt gebruiken met Elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="38729-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="38729-133">Ga naar **instellingen** \> **Geheimen** en selecteer **Genereren/importeren** om een nieuw geheim te maken.</span><span class="sxs-lookup"><span data-stu-id="38729-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="38729-134">Selecteer op de pagina **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="38729-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="38729-135">Voer de naam van het geheim in.</span><span class="sxs-lookup"><span data-stu-id="38729-135">Enter the name of the secret.</span></span> <span data-ttu-id="38729-136">Deze naam wordt gebruikt tijdens de installatie van de service in Regulatory Configuration Service (RCS) en wordt de *geheime naam van de sleutelkluis* genoemd.</span><span class="sxs-lookup"><span data-stu-id="38729-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="38729-137">Selecteer in het veld **Waarde** de **Shared Access Signature URI** en selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="38729-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="38729-138">Stel het toegangsbeleid in om Elektronische facturering het juiste niveau van beveiligde toegang te verlenen tot het geheim dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="38729-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="38729-139">Ga naar **Instellingen \> Toegangsbeleid** en selecteer **Toegangsbeleid toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="38729-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="38729-140">Stel de geheime machtigingen voor de bewerkingen **Get** en **List** in.</span><span class="sxs-lookup"><span data-stu-id="38729-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Toegang tot de service verlenen](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="38729-142">Stel de certificaatmachtigingen voor de bewerkingen **Get** en **List** in.</span><span class="sxs-lookup"><span data-stu-id="38729-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Certificaatmachtiging verlenen](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="38729-144">Selecteer **Geen geselecteerd** in het veld **Principal selecteren**.</span><span class="sxs-lookup"><span data-stu-id="38729-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="38729-145">Selecteer in het dialoogvenster **Principal** de principal door **e-Factureringsservice** toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="38729-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="38729-146">Selecteer **Toevoegen** en selecteer **Sleutelkluiswijzigingen opslaan**.</span><span class="sxs-lookup"><span data-stu-id="38729-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="38729-147">Kopieer op de pagina **Overzicht** de **DNS-naam**-waarde voor de sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="38729-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="38729-148">Deze waarde wordt gebruikt tijdens de installatie van de service in RCS en wordt de *sleutel-kluis-URI* genoemd.</span><span class="sxs-lookup"><span data-stu-id="38729-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

