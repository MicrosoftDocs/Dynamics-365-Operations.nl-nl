---
title: Problemen oplossen met betrekking tot upgrades van Finance and Operations-apps
description: Dit onderwerp bevat informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172872"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="6c52b-103">Problemen oplossen met betrekking tot upgrades van Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="6c52b-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6c52b-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6c52b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="6c52b-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="6c52b-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c52b-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6c52b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="6c52b-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="6c52b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="6c52b-108">Fouten met databasesynchronisatie</span><span class="sxs-lookup"><span data-stu-id="6c52b-108">Database synchronization errors</span></span>

<span data-ttu-id="6c52b-109">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="6c52b-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="6c52b-110">Er wordt mogelijk een foutbericht van de volgende strekking weergegeven wanneer u probeert de entiteit **DualWriteprojectConfiguration** te gebruiken om een Finance and Operations-app bij te werken naar Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="6c52b-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="6c52b-111">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="6c52b-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="6c52b-112">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6c52b-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="6c52b-113">Open Visual Studio als beheerder en open de Application Object Tree (AOT).</span><span class="sxs-lookup"><span data-stu-id="6c52b-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="6c52b-114">Zoek naar **DualWriteprojectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="6c52b-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="6c52b-115">Klik in de AOT met de rechtermuisknop op **DualWriteprojectConfiguration** en selecteer **Toevoegen aan nieuw project**.</span><span class="sxs-lookup"><span data-stu-id="6c52b-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="6c52b-116">Selecteer **OK** om het nieuwe project te maken waarin standaardopties worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6c52b-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="6c52b-117">Klik in Solution Explorer met de rechtermuisknop op **Projecteigenschappen** en stel **Database synchroniseren op build** in op **True**.</span><span class="sxs-lookup"><span data-stu-id="6c52b-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="6c52b-118">Maak het project en controleer of de build succesvol is.</span><span class="sxs-lookup"><span data-stu-id="6c52b-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="6c52b-119">Selecteer in het menu **Dynamics 365** de optie **Database synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="6c52b-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="6c52b-120">Selecteer **Synchroniseren** om een volledige databasesynchronisatie uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="6c52b-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="6c52b-121">Nadat de synchronisatie van de volledige database is geslaagd, voert u de synchronisatiestap voor de Microsoft Dynamics-database in Lifecycle Services (LCS) opnieuw uit en gebruikt u de handmatige upgradescripts als dat van toepassing is, zodat u kunt doorgaan met de update.</span><span class="sxs-lookup"><span data-stu-id="6c52b-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="6c52b-122">Problemen met ontbrekende entiteitsvelden in toewijzingen</span><span class="sxs-lookup"><span data-stu-id="6c52b-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="6c52b-123">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="6c52b-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="6c52b-124">Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="6c52b-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="6c52b-125">*\<veldnaam\> van bronveld ontbreekt in het schema.*</span><span class="sxs-lookup"><span data-stu-id="6c52b-125">*Missing source field \<field name\> in the schema.*</span></span>

![Voorbeeld van foutbericht met ontbrekende bronvelden](media/error_missing_field.png)

<span data-ttu-id="6c52b-127">Als u het probleem wilt verhelpen, voert u eerst deze stappen uit om te controleren of de velden in de entiteit aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="6c52b-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="6c52b-128">Meld u aan bij de VM voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6c52b-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="6c52b-129">Ga naar **Werkruimten \> Gegevensbeheer**, selecteer de tegel **Raamwerkparameters** en selecteer vervolgens op het tabblad **Entiteitsinstellingen** de optie **Entiteitslijst vernieuwen** om de entiteiten te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="6c52b-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="6c52b-130">Ga naar **Werkruimten \> Gegevensbeheer**, selecteer het tabblad **Gegevensentiteiten** en controleer of de entiteit wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6c52b-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="6c52b-131">Als de entiteit niet wordt weergegeven, meldt u zich aan bij de VM voor de Finance and Operations-app en controleert u of de entiteit beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="6c52b-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="6c52b-132">Open de pagina **Entiteitstoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6c52b-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="6c52b-133">Selecteer **Entiteitslijst vernieuwen** om de velden in de entiteitstoewijzingen automatisch te vullen.</span><span class="sxs-lookup"><span data-stu-id="6c52b-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="6c52b-134">Als het probleem nog steeds niet is opgelost, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="6c52b-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c52b-135">Deze stappen begeleiden u bij het verwijderen van een entiteit en het toevoegen ervan.</span><span class="sxs-lookup"><span data-stu-id="6c52b-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="6c52b-136">U kunt problemen voorkomen door de stappen exact uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="6c52b-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="6c52b-137">Ga in de Finance and Operations-app naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Gegevensentiteiten**.</span><span class="sxs-lookup"><span data-stu-id="6c52b-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="6c52b-138">Zoek de entiteit waarvoor het veld ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="6c52b-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="6c52b-139">Noteer de doelentiteit, de faseringstabel, de naam van de entiteit en andere kolomwaarden.</span><span class="sxs-lookup"><span data-stu-id="6c52b-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="6c52b-140">Als een van uw verwerkingsgroepen afhankelijk is van deze entiteit, neemt u de nodige actie voor de verwerkingsgroepen voordat u de entiteit verwijdert.</span><span class="sxs-lookup"><span data-stu-id="6c52b-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="6c52b-141">Verwijder de entiteit waarvoor het veld ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="6c52b-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="6c52b-142">Selecteer **Nieuw** en voeg de entiteit weer toe.</span><span class="sxs-lookup"><span data-stu-id="6c52b-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="6c52b-143">Geef in stap 2 de waarden op waarvoor u een notitie hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6c52b-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="6c52b-144">Open de pagina **Entiteitstoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="6c52b-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="6c52b-145">Selecteer **Entiteitslijst vernieuwen** om de velden in de entiteitstoewijzingen automatisch te vullen.</span><span class="sxs-lookup"><span data-stu-id="6c52b-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>
