---
title: Problemen met betrekking tot upgrades van Finance and Operations-apps oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754033"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="560e6-103">Problemen met betrekking tot upgrades van Finance and Operations-apps oplossen</span><span class="sxs-lookup"><span data-stu-id="560e6-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="560e6-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="560e6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="560e6-105">Dit onderwerp bevat specifieke informatie over het oplossen van problemen met betrekking tot upgrades van Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="560e6-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="560e6-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="560e6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="560e6-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="560e6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="560e6-108">Fouten met databasesynchronisatie</span><span class="sxs-lookup"><span data-stu-id="560e6-108">Database synchronization errors</span></span>

<span data-ttu-id="560e6-109">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="560e6-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="560e6-110">Er wordt mogelijk een foutbericht van de volgende strekking weergegeven wanneer u probeert de tabel **DualWriteprojectConfiguration** te gebruiken om een Finance and Operations-app bij te werken naar Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="560e6-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="560e6-111">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="560e6-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="560e6-112">Meld u aan bij de virtuele machine (VM) voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="560e6-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="560e6-113">Open Visual Studio als beheerder en open de Application Object Tree (AOT).</span><span class="sxs-lookup"><span data-stu-id="560e6-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="560e6-114">Zoek naar **DualWriteprojectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="560e6-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="560e6-115">Klik in de AOT met de rechtermuisknop op **DualWriteprojectConfiguration** en selecteer **Toevoegen aan nieuw project**.</span><span class="sxs-lookup"><span data-stu-id="560e6-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="560e6-116">Selecteer **OK** om het nieuwe project te maken waarin standaardopties worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="560e6-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="560e6-117">Klik in Solution Explorer met de rechtermuisknop op **Projecteigenschappen** en stel **Database synchroniseren op build** in op **True**.</span><span class="sxs-lookup"><span data-stu-id="560e6-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="560e6-118">Maak het project en controleer of de build succesvol is.</span><span class="sxs-lookup"><span data-stu-id="560e6-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="560e6-119">Selecteer in het menu **Dynamics 365** de optie **Database synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="560e6-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="560e6-120">Selecteer **Synchroniseren** om een volledige databasesynchronisatie uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="560e6-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="560e6-121">Nadat de synchronisatie van de volledige database is geslaagd, voert u de synchronisatiestap voor de Microsoft Dynamics-database in Lifecycle Services (LCS) opnieuw uit en gebruikt u de handmatige upgradescripts als dat van toepassing is, zodat u kunt doorgaan met de update.</span><span class="sxs-lookup"><span data-stu-id="560e6-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="560e6-122">Probleem met ontbrekende tabelkolommen in toewijzingen</span><span class="sxs-lookup"><span data-stu-id="560e6-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="560e6-123">**Vereiste rol om de fout op te lossen:** systeembeheerder</span><span class="sxs-lookup"><span data-stu-id="560e6-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="560e6-124">Op de pagina **Twee keer wegschrijven** kan een foutbericht van de volgende strekking worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="560e6-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="560e6-125">*Ontbrekend bronveld \<field name\> in het schema.*</span><span class="sxs-lookup"><span data-stu-id="560e6-125">*Missing source field \<field name\> in the schema.*</span></span>

![Voorbeeld van foutbericht over ontbrekende bronkolommen](media/error_missing_field.png)

<span data-ttu-id="560e6-127">Als u het probleem wilt verhelpen, voert u eerst deze stappen uit om te controleren of de kolommen in de tabel aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="560e6-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="560e6-128">Meld u aan bij de VM voor de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="560e6-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="560e6-129">Ga naar **Werkruimten \> Gegevensbeheer**, selecteer de tegel **Raamwerkparameters** en selecteer vervolgens op het tabblad **Tabelinstellingen** de optie **Tabellijst vernieuwen** om de tabellen te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="560e6-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="560e6-130">Ga naar **Werkruimten \> Gegevensbeheer**, selecteer het tabblad **Gegevenstabellen** en controleer of de tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="560e6-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="560e6-131">Als de tabel niet wordt weergegeven, meldt u zich aan bij de VM voor de Finance and Operations-app en controleert u of de tabel beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="560e6-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="560e6-132">Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="560e6-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="560e6-133">Selecteer **Tabellijst vernieuwen** om de kolommen in de tabeltoewijzingen automatisch te vullen.</span><span class="sxs-lookup"><span data-stu-id="560e6-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="560e6-134">Als het probleem nog steeds niet is opgelost, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="560e6-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="560e6-135">Deze stappen begeleiden u bij het verwijderen van een tabel en het toevoegen ervan.</span><span class="sxs-lookup"><span data-stu-id="560e6-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="560e6-136">U kunt problemen voorkomen door de stappen exact uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="560e6-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="560e6-137">Ga in de Finance and Operations-app naar **Werkruimten \> Gegevensbeheer** en selecteer de tegel **Gegevenstabellen**.</span><span class="sxs-lookup"><span data-stu-id="560e6-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="560e6-138">Zoek de tabel waarvoor het kenmerk ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="560e6-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="560e6-139">Klik op **Doeltoewijzing aanpassen** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="560e6-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="560e6-140">Klik in het deelvenster **Fasering aan doel toewijzen** op **Toewijzing genereren**.</span><span class="sxs-lookup"><span data-stu-id="560e6-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="560e6-141">Open de pagina **Tabeltoewijzing** op de pagina **Twee keer wegschrijven** in de Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="560e6-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="560e6-142">Als het kenmerk niet automatisch wordt ingevuld op de toewijzing, voegt u dit handmatig toe door te klikken op de knop **Kenmerk toevoegen** en vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="560e6-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="560e6-143">Selecteer de toewijzing en klik op **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="560e6-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]