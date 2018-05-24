---
title: Mobiele factuurgoedkeuringen
description: Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's in Dynamics 365 for Finance and Operations, door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc1483285d6ec675637c013af4949b9c7acf92b3
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="f4cdc-103">Mobiele factuurgoedkeuringen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4cdc-104">Met mobiele mogelijkheden in Microsoft Dynamics 365 for Finance and Operations kan een zakelijke gebruiker mobiele ervaringen ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations let a business user design mobile experiences.</span></span> <span data-ttu-id="f4cdc-105">Voor geavanceerde scenario's kunnen ontwikkelaars met het platform de mogelijkheden desgewenst ook uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="f4cdc-106">De meest effectieve manier om een aantal van de nieuwe concepten over mobiele mogelijkheden te leren is het proces voor het ontwerpen van enkele scenario's te doorlopen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="f4cdc-107">Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="f4cdc-108">Aan de hand van dit onderwerp kunt u andere variaties van de scenario's ontwerpen en kunt u de informatie in dit onderwerp ook toepassen op andere scenario's die niet zijn gerelateerd aan facturen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="f4cdc-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="f4cdc-110">Vereiste</span><span class="sxs-lookup"><span data-stu-id="f4cdc-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="f4cdc-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f4cdc-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cdc-112">Vooraf gelezen mobiel handboek</span><span class="sxs-lookup"><span data-stu-id="f4cdc-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="f4cdc-113">Mobiel platform</span><span class="sxs-lookup"><span data-stu-id="f4cdc-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="f4cdc-114">Dynamics 365 for Finance en Operations</span><span class="sxs-lookup"><span data-stu-id="f4cdc-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="f4cdc-115">Een omgeving met Microsoft Dynamics 365 for Operations versie 1611 en Microsoft Dynamics 365 for Operations-platform update 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="f4cdc-116">Installeer hotfix KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="f4cdc-117">Taakrecorder kan onterecht twee Sluiten-opdrachten voor vervolgkeuzelijstdialoogvensters registreren. Dit is opgenomen in het Dynamics 365 for Operations-platform update 3 (update van november 2016).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="f4cdc-118">Installeer hotfix KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="f4cdc-119">Met deze hotfix kunnen bijlagen worden weergegeven op de mobiele client. Dit is opgenomen in het Dynamics 365 for Operations-platform update 3 (update van november 2016).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="f4cdc-120">Installeer hotfix KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="f4cdc-121">De toepassingscode voor de mobiele toepassing voor leveranciersfactuurgoedkeuring. Dit is opgenomen in de Microsoft Dynamics AX-toepassing 7.0.1 (mei 2016).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="f4cdc-122">Een Android of iOS of een Windows-apparaat waarop de mobiele app is geïnstalleerd voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4cdc-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="f4cdc-123">Zoek naar de app in de juiste store voor mobiele apps.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="f4cdc-124">Introductie</span><span class="sxs-lookup"><span data-stu-id="f4cdc-124">Introduction</span></span>
<span data-ttu-id="f4cdc-125">Voor mobiele goedkeuringen van leveranciersfacturen zijn de drie hotfixes vereist die worden vermeld in de sectie 'Vereisten'.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="f4cdc-126">Deze hotfixes verschaffen geen werkgebied voor de factuurgoedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="f4cdc-127">Als u wilt weten wat een werkgebied is in de context van mobiel gebruik, leest u het mobiele handboek dat wordt vermeld in de sectie 'Vereisten'.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="f4cdc-128">Het werkgebied voor factuurgoedkeuringen moet worden ontworpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="f4cdc-129">Elke organisatie organiseert en definieert bedrijfsprocessen op een andere manier.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="f4cdc-130">Voordat u een mobiele ervaring voor leveranciersfactuurgoedkeuringen ontwerpt, moet u rekening houden met de volgende aspecten van het bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="f4cdc-131">Het idee is om deze gegevenspunten zo veel mogelijk te gebruiken om de gebruikerservaring op het apparaat te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="f4cdc-132">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="f4cdc-133">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="f4cdc-134">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="f4cdc-135">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="f4cdc-136">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="f4cdc-137">Als het antwoord op deze vraag ja is, kunt u de volgende vragen overwegen:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="f4cdc-138">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, opsplitsingen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="f4cdc-139">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="f4cdc-140">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="f4cdc-141">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="f4cdc-142">In dit onderwerp wordt niet uitgelegd hoe boekhoudingsverdelingen kunnen worden bewerkt, omdat deze functionaliteit momenteel niet wordt ondersteund voor mobiele scenario's.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="f4cdc-143">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="f4cdc-144">Het ontwerp van de mobiele ervaring voor factuurgoedkeuringen verschilt, afhankelijk van de antwoorden op deze vragen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="f4cdc-145">Het doel is de gebruikerservaring te optimaliseren voor het bedrijfsproces op mobiele apparaten in een organisatie.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="f4cdc-146">In de rest van dit onderwerp bekijken we twee scenariovariaties die zijn gebaseerd op verschillende antwoorden op de voorgaande vragen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="f4cdc-147">Zorg er als algemene richtlijn voor dat u tijdens het werken met de mobiele ontwerper de wijzigingen ´publiceert´ om te voorkomen dat de updates verloren gaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="f4cdc-148">Een eenvoudig factuurgoedkeuringsscenario ontwerpen voor Contoso</span><span class="sxs-lookup"><span data-stu-id="f4cdc-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4cdc-149">Scenariokenmerk</span><span class="sxs-lookup"><span data-stu-id="f4cdc-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="f4cdc-150">Beantwoorden</span><span class="sxs-lookup"><span data-stu-id="f4cdc-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f4cdc-151">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="f4cdc-152">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="f4cdc-152">Vendor name</span></span></li>
<li><span data-ttu-id="f4cdc-153">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="f4cdc-153">Invoice total</span></span></li>
<li><span data-ttu-id="f4cdc-154">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="f4cdc-154">Invoice account</span></span></li>
<li><span data-ttu-id="f4cdc-155">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="f4cdc-155">Invoice number</span></span></li>
<li><span data-ttu-id="f4cdc-156">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-156">Invoice date</span></span></li>
<li><span data-ttu-id="f4cdc-157">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="f4cdc-157">Invoice description</span></span></li>
<li><span data-ttu-id="f4cdc-158">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-158">Due date</span></span></li>
<li><span data-ttu-id="f4cdc-159">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="f4cdc-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-160">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="f4cdc-161">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="f4cdc-161">Procurement category</span></span></li>
<li><span data-ttu-id="f4cdc-162">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="f4cdc-162">Quantity</span></span></li>
<li><span data-ttu-id="f4cdc-163">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="f4cdc-163">Unit price</span></span></li>
<li><span data-ttu-id="f4cdc-164">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="f4cdc-164">Line net amount</span></span></li>
<li><span data-ttu-id="f4cdc-165">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="f4cdc-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-166">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="f4cdc-167">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="f4cdc-168">1</span><span class="sxs-lookup"><span data-stu-id="f4cdc-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-169">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="f4cdc-170">Ja</span><span class="sxs-lookup"><span data-stu-id="f4cdc-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-171">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="f4cdc-172">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="f4cdc-173">Totaalprijs: 2 btw: 0 toeslagen: 0</span><span class="sxs-lookup"><span data-stu-id="f4cdc-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-174">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="f4cdc-175">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="f4cdc-176">Niet gebruikt</span><span class="sxs-lookup"><span data-stu-id="f4cdc-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-177">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="f4cdc-178">Ja</span><span class="sxs-lookup"><span data-stu-id="f4cdc-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="f4cdc-179">Het werkgebied maken</span><span class="sxs-lookup"><span data-stu-id="f4cdc-179">Create the workspace</span></span>

1.  <span data-ttu-id="f4cdc-180">Open in een browser Finance and Operations en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="f4cdc-181">Nadat u bent aangemeld, voegt u **& mode=mobile** toe aan de URL, zoals weergegeven in het volgende voorbeeld, en vernieuwt u de pagina: https://&lt;yoururl&gt;/? cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="f4cdc-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="f4cdc-182">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="f4cdc-183">De ontwerper van de mobiele app moet worden weergegeven meteen wanneer de taakrecorder verschijnt.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="f4cdc-184">Klik op **Toevoegen** om een nieuw werkgebied te maken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="f4cdc-185">Geef voor dit voorbeeld het werkgebied de naam **Mijn goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="f4cdc-186">Voer een omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-186">Enter a description.</span></span>
6.  <span data-ttu-id="f4cdc-187">Selecteer een werkgebiedkleur.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-187">Select a workspace color.</span></span> <span data-ttu-id="f4cdc-188">De kleur van het werkgebied wordt gebruikt voor de algemene stijl van de mobiele ervaring voor dit werkgebied.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="f4cdc-189">Selecteer een pictogram voor het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="f4cdc-190">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-190">Click **Done**</span></span>
9.  <span data-ttu-id="f4cdc-191">Klik op **Werkgebied publiceren** om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="f4cdc-192">Leveranciersfacturen die aan mij zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="f4cdc-193">De eerste mobiele pagina die u moet ontwerpen, is de lijst met facturen die ter beoordeling zijn toegewezen aan de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="f4cdc-194">Als u deze mobiele pagina wilt ontwerpen, gebruikt u de pagina **VendMobileInvoiceAssignedToMeListPage** in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="f4cdc-195">Voordat u deze procedure voltooit, controleert u of er ten minste één leveranciersfactuur ter beoordeling aan u is toegewezen en of de factuurregel twee verdelingen heeft.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="f4cdc-196">Deze instelling voldoet aan de vereisten voor dit scenario.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="f4cdc-197">Vervang in de Finance and Operations-URL de naam van de menuoptie door **VendMobileInvoiceAssignedToMeListPage** om de mobiele versie van de lijstpagina **Aan mij toegewezen leveranciersfacturen in behandeling** in de module **Leveranciers** te openen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="f4cdc-198">Afhankelijk van het aantal facturen dat in uw systeem aan u is toegewezen, worden op deze pagina deze facturen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="f4cdc-199">Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="f4cdc-200">Voor dit voorbeeld is echter geen specifieke factuur vereist.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="f4cdc-201">Er moet alleen een bepaalde factuur aan u zijn toegewezen op basis waarvan u de mobiele pagina kunt ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="f4cdc-202">De nieuwe pagina's die beschikbaar zijn, zijn specifiek ontworpen voor het ontwikkelen van mobiele scenario's voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="f4cdc-203">Daarom moet u deze pagina's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="f4cdc-204">De URL moet lijken op de volgende URL en nadat u deze hebt ingevoerd, moet de pagina die wordt weergegeven in de afbeelding verschijnen: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pagina Aan mij toegewezen leveranciersfacturen in behandeling](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="f4cdc-205">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="f4cdc-206">Selecteer uw werkgebied en klik op **Bewerken**</span><span class="sxs-lookup"><span data-stu-id="f4cdc-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="f4cdc-207">Klik op **Pagina toevoegen** voor het maken van de eerste mobiele pagina.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="f4cdc-208">Voer een naam in, zoals **Mijn leveranciersfacturen**, en een omschrijving, zoals **Ter controle aan mij toegewezen leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="f4cdc-209">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-209">Click **Done**.</span></span>
7.  <span data-ttu-id="f4cdc-210">Klik in de mobiele ontwerper op het tabblad **Velden** op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="f4cdc-211">De kolommen op de lijstpagina moeten lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="f4cdc-212">[![Kolommen op de pagina In behandeling zijnde leveranciersfacturen die aan mij zijn toegewezen](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="f4cdc-213">Voeg de vereiste kolommen toe vanuit de lijstpagina die moet worden weergegeven voor de gebruikers op de mobiele pagina.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="f4cdc-214">De volgorde waarin u toevoegt, is de volgorde waarin de velden worden weergegeven voor de eindgebruiker.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="f4cdc-215">De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="f4cdc-216">Op basis van de vereisten voor dit scenario zijn de volgende acht velden vereist.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="f4cdc-217">Sommige gebruikers vinden mogelijk dat acht velden te veel informatie is voor een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="f4cdc-218">Daarom laten we alleen de belangrijkste velden in de mobiele lijstweergave zien.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="f4cdc-219">De resterende velden worden weergegeven in de detailweergave die wij later ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="f4cdc-220">Op dit moment voegen we de volgende velden toe.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-220">For now, we will add the following fields.</span></span> <span data-ttu-id="f4cdc-221">Klik op het plusteken (**+**) in deze kolommen om aan de mobiele pagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="f4cdc-222">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="f4cdc-222">Vendor name</span></span>
    - <span data-ttu-id="f4cdc-223">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="f4cdc-223">Invoice total</span></span>
    - <span data-ttu-id="f4cdc-224">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="f4cdc-224">Invoice account</span></span>
    - <span data-ttu-id="f4cdc-225">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="f4cdc-225">Invoice number</span></span>
    - <span data-ttu-id="f4cdc-226">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-226">Invoice date</span></span>

    <span data-ttu-id="f4cdc-227">Nadat u de velden zijn toegevoegd, moet de mobiele pagina lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="f4cdc-228">[![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="f4cdc-229">U moet de volgende kolommen nu ook toevoegen, zodat we workflowacties later kunnen inschakelen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="f4cdc-230">Voltooide taak weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-230">Show complete task</span></span>
    - <span data-ttu-id="f4cdc-231">Gedelegeerde taak weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-231">Show delegate task</span></span>
    - <span data-ttu-id="f4cdc-232">Teruggeroepen taak weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-232">Show recall task</span></span>
    - <span data-ttu-id="f4cdc-233">Geweigerde taak weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-233">Show reject task</span></span>
    - <span data-ttu-id="f4cdc-234">Voltooiingstaak aanvraag weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-234">Show request completion task</span></span>
    - <span data-ttu-id="f4cdc-235">Herindieningstaak weergeven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-235">Show resubmit task</span></span>

10. <span data-ttu-id="f4cdc-236">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="f4cdc-237">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="f4cdc-238">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="f4cdc-239">Schakel **Factuurtotaal in lijst met in behandeling zijnde leveranciersfacturen weergeven** in het formulier voor leveranciersparameterformulier in onder **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="f4cdc-240">Houd er rekening mee dat alleen door het inschakelen van deze parameter factuurtotalen worden berekend voor weergave op de lijstpagina met in behandeling zijnde leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="f4cdc-241">Dit is een nieuwe mogelijkheid als onderdeel van de vereiste hotfix 3208224.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="f4cdc-242">Details leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="f4cdc-242">Vendor invoice details</span></span>

<span data-ttu-id="f4cdc-243">Als u de pagina met factuurdetails wilt inschakelen voor mobiele apparaten, gebruikt u de pagina **VendMobileInvoiceHeaderDetails** in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="f4cdc-244">Houd er rekening mee dat, afhankelijk van het aantal facturen dat u in uw systeem hebt, op deze pagina de oudste factuur (de factuur die het eerst is gemaakt) wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="f4cdc-245">Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="f4cdc-246">Voor dit voorbeeld is echter geen specifieke factuur vereist.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="f4cdc-247">We hebben slechts enkele factuurgegevens nodig zodat we de mobiele pagina kunnen ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="f4cdc-248">[![Pagina Workflow](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="f4cdc-249">Vervang in de Finance and Operations-URL de naam van de menuoptie met **VendMobileInvoiceHeaderDetails** om het formulier te openen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="f4cdc-250">Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="f4cdc-251">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="f4cdc-252">Selecteer de pagina **Mijn leveranciersfacturen** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="f4cdc-253">Klik op het tabblad **Velden** op de kolomkop **Raster**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="f4cdc-254">Klik op **Eigenschappen &gt; Pagina toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="f4cdc-255">**Opmerking:** wanneer u klikt op de kop **Raster** en een pagina toevoegt, wordt de relatie met de detailpagina automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="f4cdc-256">Voer een paginatitel in, zoals **Factuurdetails**, en een omschrijving, zoals **Koptekst- en regeldetails factuur weergeven**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="f4cdc-257">Klik op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-257">Click **Select fields**.</span></span> <span data-ttu-id="f4cdc-258">Houd er rekening mee dat de volgorde waarin u toevoegt, de volgorde is waarin de velden worden weergegeven voor de eindgebruiker.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="f4cdc-259">De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="f4cdc-260">Op basis van de vereisten voor dit scenario voegt u de volgende velden uit de koptekst toe:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="f4cdc-261">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="f4cdc-261">Vendor name</span></span>
   - <span data-ttu-id="f4cdc-262">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="f4cdc-262">Invoice total</span></span>
   - <span data-ttu-id="f4cdc-263">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="f4cdc-263">Invoice account</span></span>
   - <span data-ttu-id="f4cdc-264">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="f4cdc-264">Invoice number</span></span>
   - <span data-ttu-id="f4cdc-265">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-265">Invoice date</span></span>
   - <span data-ttu-id="f4cdc-266">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="f4cdc-266">Invoice description</span></span>
   - <span data-ttu-id="f4cdc-267">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-267">Due date</span></span>
   - <span data-ttu-id="f4cdc-268">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="f4cdc-268">Invoice currency</span></span>

10. <span data-ttu-id="f4cdc-269">Voeg de volgende velden uit het regelraster op de pagina toe:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="f4cdc-270">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="f4cdc-270">Procurement category</span></span>
    - <span data-ttu-id="f4cdc-271">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="f4cdc-271">Quantity</span></span>
    - <span data-ttu-id="f4cdc-272">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="f4cdc-272">Unit price</span></span>
    - <span data-ttu-id="f4cdc-273">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="f4cdc-273">Line net amount</span></span>
    - <span data-ttu-id="f4cdc-274">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="f4cdc-274">1099 amount</span></span>

11. <span data-ttu-id="f4cdc-275">Nadat alle velden uit de vorige twee stappen zijn toegevoegd, klikt u op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="f4cdc-276">De pagina moet lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="f4cdc-277">[![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="f4cdc-278">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="f4cdc-279">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="f4cdc-280">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="f4cdc-281">Workflowacties</span><span class="sxs-lookup"><span data-stu-id="f4cdc-281">Workflow actions</span></span>

<span data-ttu-id="f4cdc-282">Als workflowacties wilt toevoegen, gebruikt u de pagina **VendMobileInvoiceHeaderDetails** in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="f4cdc-283">Als u deze pagina wilt openen, vervangt u de naam van de menuoptie in de URL, zoals u eerder hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="f4cdc-284">Open de mobiele ontwerper vervolgens met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="f4cdc-285">Voer de volgende stappen uit om workflowacties op de detailpagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="f4cdc-286">Er moeten dus facturen aan u zijn toegewezen die de correcte status hebben, zodat de workflowacties beschikbaar voor u kunnen worden gemaakt waarvoor u een ontwerp gaat ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="f4cdc-287">Workflowacties opnemen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-287">Record workflow actions</span></span>
1.  <span data-ttu-id="f4cdc-288">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="f4cdc-289">Selecteer de pagina **Factuurdetails** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="f4cdc-290">Klik op het tabblad **Acties** op **Actie toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="f4cdc-291">Voer een actietitel in, zoals **Goedkeuren**, en een omschrijving, zoals **Factuur goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="f4cdc-292">Houd er rekening mee dat de titel van de actie die u hier invoert, de naam wordt van de actie die wordt weergegeven aan de gebruiker in de mobiele toepassing.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="f4cdc-293">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-293">Click **Done**.</span></span>
6.  <span data-ttu-id="f4cdc-294">Klik op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="f4cdc-295">Doorloop het workflowproces op de pagina **VendMobileInvoiceHeaderDetails** en voer de actie uit die u wilt registreren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="f4cdc-296">Zorg dat u workflowopmerkingen tijdens dit proces invoert, zodat er ook een veld met opmerkingen in de mobiele ervaring wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="f4cdc-297">Nadat de workflowactie is uitgevoerd, klikt u op **Gereed** om de taak Velden selecteren te voltooien.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="f4cdc-298">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="f4cdc-299">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="f4cdc-300">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="f4cdc-301">Herhaal de vorige stappen om alle vereiste workflowacties te registreren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="f4cdc-302">Een js-bestand maken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-302">Create a .js file</span></span>
1. <span data-ttu-id="f4cdc-303">Open Kladblok of Microsoft Visual Studio en plak de volgende code.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="f4cdc-304">Sla het rapport als een .js-bestand op.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-304">Save the file as a .js file.</span></span> <span data-ttu-id="f4cdc-305">Deze code voert het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-305">This code does the following:</span></span>
    - <span data-ttu-id="f4cdc-306">De extra workflowgerelateerde kolommen worden verborgen die we eerder op de mobiele lijstpagina hebben toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="f4cdc-307">We hebben deze kolommen toegevoegd zodat de app die informatie in context heeft en de volgende stap kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="f4cdc-308">Op basis van de workflowstap die actief is, wordt deze logica toegepast om slechts twee acties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="f4cdc-309">De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="f4cdc-310">Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren</span><span class="sxs-lookup"><span data-stu-id="f4cdc-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="f4cdc-311">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="f4cdc-312">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="f4cdc-313">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="f4cdc-314">Leveranciersfactuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="f4cdc-315">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="f4cdc-316">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="f4cdc-317">Selecteer de pagina <strong>Factuurdetails** die u eerder hebt gemaakt en klik vervolgens op **Bewerken</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-317">Select the <strong>Invoice details **page that you created earlier, and then click **Edit</strong>.</span></span>
4. <span data-ttu-id="f4cdc-318">Stel de optie **Documentbeheer** in op **Ja** zoals hieronder wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="f4cdc-319">**Opmerking:** als er geen vereisten zijn om bijlagen weer te geven op het mobiele apparaat, kunt u deze optie ingesteld laten op **Nee**. Dit is de standaardinstelling.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="f4cdc-320">![Documentbeheer](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="f4cdc-321">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="f4cdc-322">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="f4cdc-323">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="f4cdc-324">Leveranciersfactuurregelverdelingen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="f4cdc-325">Met vereisten voor dit scenario wordt bevestigd dat er alleen verdelingen op regelniveau zijn en dat een factuur altijd slechts één regel heeft.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="f4cdc-326">Omdat dit scenario eenvoudig is, moet de gebruikerservaring op het mobiele apparaat ook zo eenvoudig zijn dat de gebruiker geen detailanalyse hoeft uit te voeren op verschillende niveaus om de verdelingen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="f4cdc-327">Leveranciersfacturen in Finance and Operations hebben ook de optie om alle verdelingen uit de factuurkoptekst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="f4cdc-328">Deze ervaring is wat we nodig hebben voor het mobiele scenario.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="f4cdc-329">Daarom gebruiken we de pagina **VendMobileInvoiceAllDistributionTree** om dit deel van het mobiele scenario te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="f4cdc-330">Op basis van de vereisten kunnen we bepalen welke specifieke pagina moet worden gebruikt en hoe de mobiele ervaring exact moet worden geoptimaliseerd voor de gebruiker bij het ontwerp van het scenario.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="f4cdc-331">In het tweede scenario gebruiken we een andere pagina om de verdelingen weer te geven, omdat de vereisten voor dat scenario verschillen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="f4cdc-332">Vervang in de URL de naam van de menuoptie, zoals u eerder hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="f4cdc-333">De pagina die verschijnt, moet lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="f4cdc-334">[![Pagina Alle verdelingen](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="f4cdc-335">Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="f4cdc-336">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="f4cdc-337">**Opmerking:** u ziet dat er automatisch twee nieuwe pagina's zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="f4cdc-338">Omdat u documentbeheer in het vorige gedeelte hebt ingeschakeld, worden deze pagina's gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="f4cdc-339">U kunt deze nieuwe pagina's negeren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="f4cdc-340">Klik op **Pagina toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="f4cdc-341">Voer een paginatitel in, zoals **Boekhouding weergeven**, en een omschrijving, zoals **Boekhouding weergeven voor de factuur**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="f4cdc-342">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-342">Click **Done**.</span></span>
7.  <span data-ttu-id="f4cdc-343">Selecteer op het tabblad **Velden** **Velden selecteren**, selecteer de volgende velden op de pagina Verdelingen en klik op **Gereed**:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="f4cdc-344">Bedrag</span><span class="sxs-lookup"><span data-stu-id="f4cdc-344">Amount</span></span>
    2.  <span data-ttu-id="f4cdc-345">Valuta</span><span class="sxs-lookup"><span data-stu-id="f4cdc-345">Currency</span></span>
    3.  <span data-ttu-id="f4cdc-346">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="f4cdc-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="f4cdc-347">We hebben de kolom **Omschrijving** uit het raster Verdelingen niet geselecteerd, omdat de vereisten voor dit scenario hebben bevestigd dat de totaalprijs het enige bedrag is waarvoor er verdelingen zijn.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="f4cdc-348">De gebruiker heeft daarom geen ander veld nodig om het bedragtype te bepalen waarvoor de verdeling is bestemd.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="f4cdc-349">In het volgende scenario gebruiken we echter deze gegevens **wel**, omdat de vereisten voor dat scenario aangeven dat andere bedragtypen verdelingen hebben (bijvoorbeeld btw).</span><span class="sxs-lookup"><span data-stu-id="f4cdc-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="f4cdc-350">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="f4cdc-351">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="f4cdc-352">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="f4cdc-353">De mobiele pagina **Boekhouding weergeven** is nu nog niet gekoppeld aan een van de mobiele pagina's die we tot nu toe hebben ontworpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="f4cdc-354">Omdat de gebruiker moet kunnen navigeren naar de pagina **Boekhouding weergeven** van de pagina **Factuurdetails** op het mobiele apparaat, moeten wij navigatie verschaffen vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="f4cdc-355">We stellen deze navigatie in met behulp van aanvullende logica via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="f4cdc-356">Open het .js-bestand dat u eerder hebt gemaakt en voeg de regels toe die in de volgende code zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="f4cdc-357">Deze code doet twee dingen:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-357">This code does two things:</span></span>
    1.  <span data-ttu-id="f4cdc-358">Dit helpt te garanderen dat gebruikers niet rechtstreeks van het werkgebied naar de pagina **Boekhouding weergeven** kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="f4cdc-359">Er wordt een navigatiebesturingselement ingesteld vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="f4cdc-360">De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="f4cdc-361">Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren om de vorige code te overschrijven</span><span class="sxs-lookup"><span data-stu-id="f4cdc-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="f4cdc-362">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="f4cdc-363">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="f4cdc-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="f4cdc-364">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="f4cdc-365">Validatie</span><span class="sxs-lookup"><span data-stu-id="f4cdc-365">Validation</span></span>

<span data-ttu-id="f4cdc-366">Open op uw mobiele apparaat de app en maak verbinding met uw Finance and Operations-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="f4cdc-367">Zorg ervoor dat u zich aanmeldt bij het bedrijf waar leveranciersfacturen ter controle aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="f4cdc-368">U moet de volgende acties kunnen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="f4cdc-369">Zie het werkgebied **Mijn goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="f4cdc-370">Zoom in op het werkgebied **Mijn goedkeuringen** en bekijk de pagina **Mijn leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="f4cdc-371">Zoom in op de pagina **Mijn leveranciersfacturen** en bekijk de lijst met facturen die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="f4cdc-372">Zoom in op een van de facturen en bekijk de factuurkoptekstdetails en de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="f4cdc-373">Bekijk op de detailpagina een koppeling naar bijlagen en gebruik deze koppeling om naar de lijst met bijlagen te navigeren en de bijlagen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="f4cdc-374">Bekijk op de detailpagina een koppeling naar de pagina **Boekhouding weergeven** en gebruik deze koppeling om naar de pagina met verdelingen te navigeren en geef de verdelingen weer.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="f4cdc-375">Klik op de detailpagina op het menu **Acties** onderaan en voer workflowacties uit die van toepassing op de workflowstap zijn.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="f4cdc-376">Een complex factuurgoedkeuringsscenario ontwerpen voor Fabrikam</span><span class="sxs-lookup"><span data-stu-id="f4cdc-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4cdc-377">Scenariokenmerk</span><span class="sxs-lookup"><span data-stu-id="f4cdc-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="f4cdc-378">Beantwoorden</span><span class="sxs-lookup"><span data-stu-id="f4cdc-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f4cdc-379">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="f4cdc-380">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="f4cdc-380">Vendor name</span></span></li>
<li><span data-ttu-id="f4cdc-381">Factuurbedrag</span><span class="sxs-lookup"><span data-stu-id="f4cdc-381">Invoice amount</span></span></li>
<li><span data-ttu-id="f4cdc-382">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="f4cdc-382">Invoice account</span></span></li>
<li><span data-ttu-id="f4cdc-383">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="f4cdc-383">Invoice number</span></span></li>
<li><span data-ttu-id="f4cdc-384">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-384">Invoice date</span></span></li>
<li><span data-ttu-id="f4cdc-385">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="f4cdc-385">Invoice description</span></span></li>
<li><span data-ttu-id="f4cdc-386">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f4cdc-386">Due date</span></span></li>
<li><span data-ttu-id="f4cdc-387">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="f4cdc-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-388">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="f4cdc-389">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="f4cdc-389">Procurement category</span></span></li>
<li><span data-ttu-id="f4cdc-390">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="f4cdc-390">Quantity</span></span></li>
<li><span data-ttu-id="f4cdc-391">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="f4cdc-391">Unit price</span></span></li>
<li><span data-ttu-id="f4cdc-392">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="f4cdc-392">Line net amount</span></span></li>
<li><span data-ttu-id="f4cdc-393">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="f4cdc-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-394">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="f4cdc-395">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="f4cdc-396">5</span><span class="sxs-lookup"><span data-stu-id="f4cdc-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-397">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="f4cdc-398">Ja</span><span class="sxs-lookup"><span data-stu-id="f4cdc-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-399">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="f4cdc-400">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="f4cdc-401">Totaalprijs: 2 btw: 2 toeslagen: 2</span><span class="sxs-lookup"><span data-stu-id="f4cdc-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4cdc-402">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="f4cdc-403">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="f4cdc-404">Niet gebruikt</span><span class="sxs-lookup"><span data-stu-id="f4cdc-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4cdc-405">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="f4cdc-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="f4cdc-406">Ja</span><span class="sxs-lookup"><span data-stu-id="f4cdc-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="f4cdc-407">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="f4cdc-407">Next steps</span></span>

<span data-ttu-id="f4cdc-408">De volgende variaties kunnen worden uitgevoerd voor scenario 1, op basis van de vereisten voor scenario 2.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="f4cdc-409">U kunt deze sectie gebruiken om de ervaring in uw mobiele app te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="f4cdc-410">Omdat er meer factuurregels worden verwacht in scenario 2, helpen de volgende wijzigingen in het ontwerp de gebruikerservaring op het mobiele apparaat te optimaliseren:</span><span class="sxs-lookup"><span data-stu-id="f4cdc-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="f4cdc-411">In plaats van factuurregels weer te geven op de detailpagina (zoals in scenario 1), kunnen gebruikers ervoor kiezen regels op een aparte mobiele pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="f4cdc-412">Omdat meer dan één factuurregel wordt verwacht in dit scenario als de pagina **VendMobileInvoiceAllDistributionTree** wordt gebruikt voor het ontwerpen van de pagina Verdelingen voor mobiele apparaten (zoals in scenario 1), kan dat verwarrend zijn voor de gebruiker om regels te relateren aan verdelingen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="f4cdc-413">Gebruik daarom de pagina **VendMobileInvoiceLineDistributionTree** om de pagina Verdelingen te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="f4cdc-414">In het ideale geval moeten de verdelingen worden weergegeven in de context van een factuurregel in dit scenario.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="f4cdc-415">Zorg er daarom voor dat de gebruiker kan inzoomen op een regel om de pagina Verdelingen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="f4cdc-416">Gebruik de paginakoppelingmogelijkheid om het inzoomen in te stellen, net als u voor de koptekst en detailpagina's in scenario 1 hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="f4cdc-417">Omdat meer dan één bedragtype wordt verwacht voor de verdelingen in scenario 2 (btw, toeslagen, enzovoort), is het nuttig om de omschrijving van het bedragtype weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f4cdc-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="f4cdc-418">(We hebben deze informatie in scenario 1 weggelaten.)</span><span class="sxs-lookup"><span data-stu-id="f4cdc-418">(We omitted this information in scenario 1.)</span></span>





