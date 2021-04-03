---
title: Talent uitbreiden met Power Apps en Power Automate
description: In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Human Resources die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.
author: negudava
manager: tfehr
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edc2352fa53ac93c582b608b65fc624ff5dcd2a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467068"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="88f30-103">Uitbreiden met Power Apps en Power Automate</span><span class="sxs-lookup"><span data-stu-id="88f30-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="88f30-104">In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Human Resources die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="88f30-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="88f30-105">U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw Power Apps-omgeving.</span><span class="sxs-lookup"><span data-stu-id="88f30-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="88f30-106">Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="88f30-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88f30-107">Als u de sjablonen en apps die worden beschreven in dit onderwerp, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.</span><span class="sxs-lookup"><span data-stu-id="88f30-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88f30-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="88f30-108">Prerequisites</span></span>

- <span data-ttu-id="88f30-109">Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.</span><span class="sxs-lookup"><span data-stu-id="88f30-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="88f30-110">Als u apps wilt exporteren of importeren, moeten gebruikers een Power Apps Plan 2-licentie of een proeflicentie van Power Apps Plan 2 hebben.</span><span class="sxs-lookup"><span data-stu-id="88f30-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="88f30-111">Integratie met Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="88f30-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="88f30-112">De app **Integratie met Microsoft 365** kan worden gebruikt voor het ophalen van teamgegevens voor aangemelde gebruikers vanuit Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88f30-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="88f30-113">Het verwijst naar werknemers in Human resources om identificatietypen voor werknemers te extraheren.</span><span class="sxs-lookup"><span data-stu-id="88f30-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="88f30-114">Managers kunnen vervaldatums van typen werknemer-id's controleren.</span><span class="sxs-lookup"><span data-stu-id="88f30-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="88f30-115">Ze kunnen ook een herinnering per e-mail verzenden als het type werknemer-id verloopt.</span><span class="sxs-lookup"><span data-stu-id="88f30-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="88f30-116">Power Automate integreert met Power Apps om deze herinnering te verzenden.</span><span class="sxs-lookup"><span data-stu-id="88f30-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="88f30-117">Er wordt een bevestiging teruggestuurd naar Power Apps vanuit Power Automate wanneer de herinnering is verzonden.</span><span class="sxs-lookup"><span data-stu-id="88f30-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="88f30-118">Identificatietypen zijn onder andere rijbewijs, paspoort en andere aanvaardbare vormen van identificatie.</span><span class="sxs-lookup"><span data-stu-id="88f30-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="88f30-119">U kunt deze app uitbreiden voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="88f30-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="88f30-120">U kunt deze bijvoorbeeld gebruiken om teamvakantiegegevens, agenda-items en teamspecifieke gebeurtenissen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="88f30-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="88f30-121">Voor het downloaden van de app **Integratie met Microsoft 365, Power Automate** gaat u naar [Integratie met Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="88f30-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="88f30-122">Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren</span><span class="sxs-lookup"><span data-stu-id="88f30-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="88f30-123">Met de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** wordt verbinding gemaakt met Microsoft SQL Server en kunnen SQL-query's worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="88f30-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="88f30-124">Hoewel met deze sjabloon SQL-tabellen worden gelezen en bijgewerkt, kunt u deze uitbreiden en gebruiken voor andere scenario's.</span><span class="sxs-lookup"><span data-stu-id="88f30-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="88f30-125">Zo kunt u de sjabloon bijvoorbeeld gebruiken voor het vullen van een faseringstabel in Dataverse met records van SQL Server en voor het periodiek synchroniseren van de faseringstabel met behulp van een incrementele push van SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88f30-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="88f30-126">Geavanceerde query is geïntegreerd met Flow om gegevenstransformatie en incrementele push mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="88f30-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="88f30-127">Voor het downloaden van de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** gaat u naar [Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren](https://go.microsoft.com/fwlink/?linkid=2081789) in het Microsoft Downloadcentrum.</span><span class="sxs-lookup"><span data-stu-id="88f30-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88f30-128">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="88f30-128">Additional resources</span></span>

[<span data-ttu-id="88f30-129">Het Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="88f30-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]