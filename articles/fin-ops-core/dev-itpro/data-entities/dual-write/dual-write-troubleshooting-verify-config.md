---
title: Controleer of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse
description: In dit onderwerp wordt uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685534"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="aebf8-103">Controleer of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse</span><span class="sxs-lookup"><span data-stu-id="aebf8-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="aebf8-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="aebf8-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="aebf8-105">In dit onderwerp wordt specifiek uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="aebf8-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="aebf8-106">Controleren of Twee keer wegschrijven is geconfigureerd in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="aebf8-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="aebf8-107">Om te bepalen of de fouten die worden weergegeven wanneer u rijen voor de update probeert op te slaan, afkomstig zijn van Twee keer wegschrijven, controleert u eerst of Twee keer wegschrijven is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="aebf8-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="aebf8-108">Als u beheerdersrechten hebt in de Finance and Operations-app, gaat u naar **Werkruimten \> Gegevensbeheer** en selecteert u de tegel voor **Twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="aebf8-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="aebf8-109">Als de details van de gekoppelde omgevingen en de lijst met actieve tabeltoewijzingen worden weergegeven, wordt Twee keer wegschrijven geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="aebf8-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt](media/verify_fin_ops_1.png)

+ <span data-ttu-id="aebf8-111">Als u geen beheerdersbevoegdheden hebt, wordt er een foutbericht weergegeven: *Kan geen gegevens schrijven naar entiteit \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="aebf8-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="aebf8-112">In het voorbeeld in de volgende afbeelding kunt u geen klantrij in de Finance and Operations-app maken, omdat Twee keer wegschrijven is geconfigureerd, maar de verwijzingsgegevens voor de klantengroep en de betalingsvoorwaarden zijn niet aanwezig in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="aebf8-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt](media/verify_fin_ops_2.png)

<span data-ttu-id="aebf8-114">Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Finance and Operations-apps leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="aebf8-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="aebf8-115">Controleren of Twee keer wegschrijven is geconfigureerd in Dataverse</span><span class="sxs-lookup"><span data-stu-id="aebf8-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="aebf8-116">Wanneer u gegevens maakt en u het veld **Bedrijf** ziet op pagina's in Dataverse, is Twee keer wegschrijven geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="aebf8-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![De Dataverse-verbinding controleren](media/verify_cds.png)

<span data-ttu-id="aebf8-118">Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Dataverse leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="aebf8-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="aebf8-119">Voor informatie over het weergeven van foutdetails als u fouten tegenkomt bij het maken van gegevens in Dataverse, raadpleegt u [Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="aebf8-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
