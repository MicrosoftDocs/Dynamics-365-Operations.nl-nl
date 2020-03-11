---
title: Mobiele factuurgoedkeuringen
description: Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059423"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="23eab-103">Mobiele factuurgoedkeuringen</span><span class="sxs-lookup"><span data-stu-id="23eab-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23eab-104">Met de mobiele mogelijkheden kan een zakelijke gebruiker mobiele ervaringen ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="23eab-105">Voor geavanceerde scenario's kunnen ontwikkelaars met het platform de mogelijkheden desgewenst ook uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="23eab-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="23eab-106">De meest effectieve manier om een aantal van de nieuwe concepten over mobiele mogelijkheden te leren is het proces voor het ontwerpen van enkele scenario's te doorlopen.</span><span class="sxs-lookup"><span data-stu-id="23eab-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="23eab-107">Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen.</span><span class="sxs-lookup"><span data-stu-id="23eab-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="23eab-108">Aan de hand van dit onderwerp kunt u andere variaties van de scenario's ontwerpen en kunt u de informatie in dit onderwerp ook toepassen op andere scenario's die niet zijn gerelateerd aan facturen van leveranciers.</span><span class="sxs-lookup"><span data-stu-id="23eab-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="23eab-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="23eab-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="23eab-110">Vereiste</span><span class="sxs-lookup"><span data-stu-id="23eab-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="23eab-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="23eab-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23eab-112">Vooraf gelezen mobiel handboek</span><span class="sxs-lookup"><span data-stu-id="23eab-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="23eab-113">Mobiel platform</span><span class="sxs-lookup"><span data-stu-id="23eab-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="23eab-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="23eab-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="23eab-115">Een omgeving met versie 1611 en Platformupdate 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="23eab-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="23eab-116">Installeer hotfix KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="23eab-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="23eab-117">Taakrecorder kan onterecht twee Sluiten-opdrachten voor vervolgkeuzelijstdialoogvensters registreren. Dit is opgenomen in Platformupdate 3 (update van november 2016).</span><span class="sxs-lookup"><span data-stu-id="23eab-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="23eab-118">Installeer hotfix KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="23eab-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="23eab-119">Met deze hotfix kunnen bijlagen worden weergegeven op de mobiele client. Dit is opgenomen in Platformupdate 3 (update van november 2016).</span><span class="sxs-lookup"><span data-stu-id="23eab-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="23eab-120">Installeer hotfix KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="23eab-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="23eab-121">De toepassingscode voor de mobiele toepassing voor leveranciersfactuurgoedkeuring. Dit is opgenomen in versie 7.0.1 (mei 2016).</span><span class="sxs-lookup"><span data-stu-id="23eab-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="23eab-122">Een Android of iOS of een Windows-apparaat waarop de mobiele app is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="23eab-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="23eab-123">Zoek naar de app in de juiste store voor mobiele apps.</span><span class="sxs-lookup"><span data-stu-id="23eab-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="23eab-124">Inleiding</span><span class="sxs-lookup"><span data-stu-id="23eab-124">Introduction</span></span>
<span data-ttu-id="23eab-125">Voor mobiele goedkeuringen van leveranciersfacturen zijn de drie hotfixes vereist die worden vermeld in de sectie 'Vereisten'.</span><span class="sxs-lookup"><span data-stu-id="23eab-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="23eab-126">Deze hotfixes verschaffen geen werkgebied voor de factuurgoedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="23eab-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="23eab-127">Als u wilt weten wat een werkgebied is in de context van mobiel gebruik, leest u het mobiele handboek dat wordt vermeld in de sectie 'Vereisten'.</span><span class="sxs-lookup"><span data-stu-id="23eab-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="23eab-128">Het werkgebied voor factuurgoedkeuringen moet worden ontworpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="23eab-129">Elke organisatie organiseert en definieert bedrijfsprocessen op een andere manier.</span><span class="sxs-lookup"><span data-stu-id="23eab-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="23eab-130">Voordat u een mobiele ervaring voor leveranciersfactuurgoedkeuringen ontwerpt, moet u rekening houden met de volgende aspecten van het bedrijfsproces.</span><span class="sxs-lookup"><span data-stu-id="23eab-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="23eab-131">Het idee is om deze gegevenspunten zo veel mogelijk te gebruiken om de gebruikerservaring op het apparaat te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="23eab-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="23eab-132">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="23eab-133">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="23eab-134">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="23eab-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="23eab-135">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="23eab-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="23eab-136">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="23eab-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="23eab-137">Als het antwoord op deze vraag ja is, kunt u de volgende vragen overwegen:</span><span class="sxs-lookup"><span data-stu-id="23eab-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="23eab-138">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, opsplitsingen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="23eab-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="23eab-139">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="23eab-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="23eab-140">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="23eab-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="23eab-141">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="23eab-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="23eab-142">In dit onderwerp wordt niet uitgelegd hoe boekhoudingsverdelingen kunnen worden bewerkt, omdat deze functionaliteit momenteel niet wordt ondersteund voor mobiele scenario's.</span><span class="sxs-lookup"><span data-stu-id="23eab-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="23eab-143">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="23eab-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="23eab-144">Het ontwerp van de mobiele ervaring voor factuurgoedkeuringen verschilt, afhankelijk van de antwoorden op deze vragen.</span><span class="sxs-lookup"><span data-stu-id="23eab-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="23eab-145">Het doel is de gebruikerservaring te optimaliseren voor het bedrijfsproces op mobiele apparaten in een organisatie.</span><span class="sxs-lookup"><span data-stu-id="23eab-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="23eab-146">In de rest van dit onderwerp bekijken we twee scenariovariaties die zijn gebaseerd op verschillende antwoorden op de voorgaande vragen.</span><span class="sxs-lookup"><span data-stu-id="23eab-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="23eab-147">Zorg er als algemene richtlijn voor dat u tijdens het werken met de mobiele ontwerper de wijzigingen ´publiceert´ om te voorkomen dat de updates verloren gaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="23eab-148">Een eenvoudig factuurgoedkeuringsscenario ontwerpen voor Contoso</span><span class="sxs-lookup"><span data-stu-id="23eab-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23eab-149">Scenariokenmerk</span><span class="sxs-lookup"><span data-stu-id="23eab-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="23eab-150">Beantwoorden</span><span class="sxs-lookup"><span data-stu-id="23eab-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23eab-151">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="23eab-152">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="23eab-152">Vendor name</span></span></li>
<li><span data-ttu-id="23eab-153">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="23eab-153">Invoice total</span></span></li>
<li><span data-ttu-id="23eab-154">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="23eab-154">Invoice account</span></span></li>
<li><span data-ttu-id="23eab-155">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="23eab-155">Invoice number</span></span></li>
<li><span data-ttu-id="23eab-156">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="23eab-156">Invoice date</span></span></li>
<li><span data-ttu-id="23eab-157">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="23eab-157">Invoice description</span></span></li>
<li><span data-ttu-id="23eab-158">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="23eab-158">Due date</span></span></li>
<li><span data-ttu-id="23eab-159">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="23eab-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-160">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="23eab-161">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="23eab-161">Procurement category</span></span></li>
<li><span data-ttu-id="23eab-162">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="23eab-162">Quantity</span></span></li>
<li><span data-ttu-id="23eab-163">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="23eab-163">Unit price</span></span></li>
<li><span data-ttu-id="23eab-164">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="23eab-164">Line net amount</span></span></li>
<li><span data-ttu-id="23eab-165">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="23eab-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-166">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="23eab-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="23eab-167">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="23eab-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="23eab-168">1</span><span class="sxs-lookup"><span data-stu-id="23eab-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-169">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="23eab-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="23eab-170">Ja</span><span class="sxs-lookup"><span data-stu-id="23eab-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-171">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="23eab-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="23eab-172">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="23eab-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="23eab-173">Totaalprijs: 2 btw: 0 toeslagen: 0</span><span class="sxs-lookup"><span data-stu-id="23eab-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-174">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="23eab-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="23eab-175">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="23eab-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="23eab-176">Niet gebruikt</span><span class="sxs-lookup"><span data-stu-id="23eab-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-177">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="23eab-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="23eab-178">Ja</span><span class="sxs-lookup"><span data-stu-id="23eab-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="23eab-179">Het werkgebied maken</span><span class="sxs-lookup"><span data-stu-id="23eab-179">Create the workspace</span></span>

1.  <span data-ttu-id="23eab-180">In een browser en meld u aan bij de-toepassing.</span><span class="sxs-lookup"><span data-stu-id="23eab-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="23eab-181">Nadat u bent aangemeld, voegt u **&mode=mobile** toe aan de URL, zoals weergegeven in het volgende voorbeeld, en vernieuwt u de pagina: https://&lt;yoururl&gt;/? cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="23eab-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="23eab-182">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="23eab-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="23eab-183">De ontwerper van de mobiele app moet worden weergegeven meteen wanneer de taakrecorder verschijnt.</span><span class="sxs-lookup"><span data-stu-id="23eab-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="23eab-184">Klik op **Toevoegen** om een nieuw werkgebied te maken.</span><span class="sxs-lookup"><span data-stu-id="23eab-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="23eab-185">Geef voor dit voorbeeld het werkgebied de naam **Mijn goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="23eab-186">Voer een omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="23eab-186">Enter a description.</span></span>
6.  <span data-ttu-id="23eab-187">Selecteer een werkgebiedkleur.</span><span class="sxs-lookup"><span data-stu-id="23eab-187">Select a workspace color.</span></span> <span data-ttu-id="23eab-188">De kleur van het werkgebied wordt gebruikt voor de algemene stijl van de mobiele ervaring voor dit werkgebied.</span><span class="sxs-lookup"><span data-stu-id="23eab-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="23eab-189">Selecteer een pictogram voor het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="23eab-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="23eab-190">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="23eab-190">Click **Done**</span></span>
9.  <span data-ttu-id="23eab-191">Klik op **Werkgebied publiceren** om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="23eab-192">Leveranciersfacturen die aan mij zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="23eab-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="23eab-193">De eerste mobiele pagina die u moet ontwerpen, is de lijst met facturen die ter beoordeling zijn toegewezen aan de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="23eab-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="23eab-194">Als u deze mobiele pagina wilt ontwerpen, gebruikt u de pagina **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="23eab-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="23eab-195">Voordat u deze procedure voltooit, controleert u of er ten minste één leveranciersfactuur ter beoordeling aan u is toegewezen en of de factuurregel twee verdelingen heeft.</span><span class="sxs-lookup"><span data-stu-id="23eab-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="23eab-196">Deze instelling voldoet aan de vereisten voor dit scenario.</span><span class="sxs-lookup"><span data-stu-id="23eab-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="23eab-197">Vervang in de URL de naam van de menuoptie door **VendMobileInvoiceAssignedToMeListPage** om de mobiele versie van de lijstpagina **Aan mij toegewezen leveranciersfacturen in behandeling** in de module **Leveranciers** te openen.</span><span class="sxs-lookup"><span data-stu-id="23eab-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="23eab-198">Afhankelijk van het aantal facturen dat in uw systeem aan u is toegewezen, worden op deze pagina deze facturen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="23eab-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="23eab-199">Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken.</span><span class="sxs-lookup"><span data-stu-id="23eab-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="23eab-200">Voor dit voorbeeld is echter geen specifieke factuur vereist.</span><span class="sxs-lookup"><span data-stu-id="23eab-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="23eab-201">Er moet alleen een bepaalde factuur aan u zijn toegewezen op basis waarvan u de mobiele pagina kunt ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="23eab-202">De nieuwe pagina's die beschikbaar zijn, zijn specifiek ontworpen voor het ontwikkelen van mobiele scenario's voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="23eab-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="23eab-203">Daarom moet u deze pagina's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="23eab-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="23eab-204">De URL moet lijken op de volgende URL en nadat u deze hebt ingevoerd, moet de pagina die wordt weergegeven in de afbeelding verschijnen: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="23eab-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="23eab-205">[![Pagina Aan mij toegewezen leveranciersfacturen in behandeling](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="23eab-206">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="23eab-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="23eab-207">Selecteer uw werkgebied en klik op **Bewerken**</span><span class="sxs-lookup"><span data-stu-id="23eab-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="23eab-208">Klik op **Pagina toevoegen** voor het maken van de eerste mobiele pagina.</span><span class="sxs-lookup"><span data-stu-id="23eab-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="23eab-209">Voer een naam in, zoals **Mijn leveranciersfacturen**, en een omschrijving, zoals **Ter controle aan mij toegewezen leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="23eab-210">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="23eab-210">Click **Done**.</span></span>
7.  <span data-ttu-id="23eab-211">Klik in de mobiele ontwerper op het tabblad **Velden** op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="23eab-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="23eab-212">De kolommen op de lijstpagina moeten lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23eab-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="23eab-213">[![Kolommen op de pagina In behandeling zijnde leveranciersfacturen die aan mij zijn toegewezen](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="23eab-214">Voeg de vereiste kolommen toe vanuit de lijstpagina die moet worden weergegeven voor de gebruikers op de mobiele pagina.</span><span class="sxs-lookup"><span data-stu-id="23eab-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="23eab-215">De volgorde waarin u toevoegt, is de volgorde waarin de velden worden weergegeven voor de eindgebruiker.</span><span class="sxs-lookup"><span data-stu-id="23eab-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="23eab-216">De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren.</span><span class="sxs-lookup"><span data-stu-id="23eab-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="23eab-217">Op basis van de vereisten voor dit scenario zijn de volgende acht velden vereist.</span><span class="sxs-lookup"><span data-stu-id="23eab-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="23eab-218">Sommige gebruikers vinden mogelijk dat acht velden te veel informatie is voor een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="23eab-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="23eab-219">Daarom laten we alleen de belangrijkste velden in de mobiele lijstweergave zien.</span><span class="sxs-lookup"><span data-stu-id="23eab-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="23eab-220">De resterende velden worden weergegeven in de detailweergave die wij later ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="23eab-221">Op dit moment voegen we de volgende velden toe.</span><span class="sxs-lookup"><span data-stu-id="23eab-221">For now, we will add the following fields.</span></span> <span data-ttu-id="23eab-222">Klik op het plusteken (**+**) in deze kolommen om aan de mobiele pagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="23eab-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="23eab-223">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="23eab-223">Vendor name</span></span>
    - <span data-ttu-id="23eab-224">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="23eab-224">Invoice total</span></span>
    - <span data-ttu-id="23eab-225">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="23eab-225">Invoice account</span></span>
    - <span data-ttu-id="23eab-226">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="23eab-226">Invoice number</span></span>
    - <span data-ttu-id="23eab-227">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="23eab-227">Invoice date</span></span>

    <span data-ttu-id="23eab-228">Nadat u de velden zijn toegevoegd, moet de mobiele pagina lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23eab-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="23eab-229">[![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="23eab-230">U moet de volgende kolommen nu ook toevoegen, zodat we workflowacties later kunnen inschakelen.</span><span class="sxs-lookup"><span data-stu-id="23eab-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="23eab-231">Voltooide taak weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-231">Show complete task</span></span>
    - <span data-ttu-id="23eab-232">Gedelegeerde taak weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-232">Show delegate task</span></span>
    - <span data-ttu-id="23eab-233">Teruggeroepen taak weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-233">Show recall task</span></span>
    - <span data-ttu-id="23eab-234">Geweigerde taak weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-234">Show reject task</span></span>
    - <span data-ttu-id="23eab-235">Voltooiingstaak aanvraag weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-235">Show request completion task</span></span>
    - <span data-ttu-id="23eab-236">Herindieningstaak weergeven</span><span class="sxs-lookup"><span data-stu-id="23eab-236">Show resubmit task</span></span>

10. <span data-ttu-id="23eab-237">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="23eab-238">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="23eab-239">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="23eab-240">Schakel **Factuurtotaal in lijst met in behandeling zijnde leveranciersfacturen weergeven** in het formulier voor leveranciersparameterformulier in onder **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="23eab-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="23eab-241">Houd er rekening mee dat alleen door het inschakelen van deze parameter factuurtotalen worden berekend voor weergave op de lijstpagina met in behandeling zijnde leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="23eab-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="23eab-242">Dit is een nieuwe mogelijkheid als onderdeel van de vereiste hotfix 3208224.</span><span class="sxs-lookup"><span data-stu-id="23eab-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="23eab-243">Details leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="23eab-243">Vendor invoice details</span></span>

<span data-ttu-id="23eab-244">Als u de pagina met factuurdetails wilt inschakelen voor mobiele apparaten, gebruikt u de pagina **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="23eab-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="23eab-245">Houd er rekening mee dat, afhankelijk van het aantal facturen dat u in uw systeem hebt, op deze pagina de oudste factuur (de factuur die het eerst is gemaakt) wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="23eab-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="23eab-246">Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken.</span><span class="sxs-lookup"><span data-stu-id="23eab-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="23eab-247">Voor dit voorbeeld is echter geen specifieke factuur vereist.</span><span class="sxs-lookup"><span data-stu-id="23eab-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="23eab-248">We hebben slechts enkele factuurgegevens nodig zodat we de mobiele pagina kunnen ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="23eab-249">[![Pagina Workflow](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="23eab-250">Vervang in de URL de naam van de menuoptie met **VendMobileInvoiceHeaderDetails** om het formulier te openen</span><span class="sxs-lookup"><span data-stu-id="23eab-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="23eab-251">Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="23eab-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="23eab-252">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="23eab-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="23eab-253">Selecteer de pagina **Mijn leveranciersfacturen** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="23eab-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="23eab-254">Klik op het tabblad **Velden** op de kolomkop **Raster**.</span><span class="sxs-lookup"><span data-stu-id="23eab-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="23eab-255">Klik op **Eigenschappen &gt; Pagina toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="23eab-256">**Opmerking:** wanneer u klikt op de kop **Raster** en een pagina toevoegt, wordt de relatie met de detailpagina automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="23eab-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="23eab-257">Voer een paginatitel in, zoals **Factuurdetails**, en een omschrijving, zoals **Koptekst- en regeldetails factuur weergeven**.</span><span class="sxs-lookup"><span data-stu-id="23eab-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="23eab-258">Klik op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="23eab-258">Click **Select fields**.</span></span> <span data-ttu-id="23eab-259">Houd er rekening mee dat de volgorde waarin u toevoegt, de volgorde is waarin de velden worden weergegeven voor de eindgebruiker.</span><span class="sxs-lookup"><span data-stu-id="23eab-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="23eab-260">De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren.</span><span class="sxs-lookup"><span data-stu-id="23eab-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="23eab-261">Op basis van de vereisten voor dit scenario voegt u de volgende velden uit de koptekst toe:</span><span class="sxs-lookup"><span data-stu-id="23eab-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="23eab-262">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="23eab-262">Vendor name</span></span>
   - <span data-ttu-id="23eab-263">Factuurtotaal</span><span class="sxs-lookup"><span data-stu-id="23eab-263">Invoice total</span></span>
   - <span data-ttu-id="23eab-264">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="23eab-264">Invoice account</span></span>
   - <span data-ttu-id="23eab-265">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="23eab-265">Invoice number</span></span>
   - <span data-ttu-id="23eab-266">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="23eab-266">Invoice date</span></span>
   - <span data-ttu-id="23eab-267">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="23eab-267">Invoice description</span></span>
   - <span data-ttu-id="23eab-268">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="23eab-268">Due date</span></span>
   - <span data-ttu-id="23eab-269">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="23eab-269">Invoice currency</span></span>

10. <span data-ttu-id="23eab-270">Voeg de volgende velden uit het regelraster op de pagina toe:</span><span class="sxs-lookup"><span data-stu-id="23eab-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="23eab-271">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="23eab-271">Procurement category</span></span>
    - <span data-ttu-id="23eab-272">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="23eab-272">Quantity</span></span>
    - <span data-ttu-id="23eab-273">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="23eab-273">Unit price</span></span>
    - <span data-ttu-id="23eab-274">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="23eab-274">Line net amount</span></span>
    - <span data-ttu-id="23eab-275">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="23eab-275">1099 amount</span></span>

11. <span data-ttu-id="23eab-276">Nadat alle velden uit de vorige twee stappen zijn toegevoegd, klikt u op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="23eab-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="23eab-277">De pagina moet lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23eab-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="23eab-278">[![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="23eab-279">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="23eab-280">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="23eab-281">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="23eab-282">Workflowacties</span><span class="sxs-lookup"><span data-stu-id="23eab-282">Workflow actions</span></span>

<span data-ttu-id="23eab-283">Voeg workflowacties toe met de pagina **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="23eab-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="23eab-284">Als u deze pagina wilt openen, vervangt u de naam van de menuoptie in de URL, zoals u eerder hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="23eab-285">Open de mobiele ontwerper vervolgens met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="23eab-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="23eab-286">Voer de volgende stappen uit om workflowacties op de detailpagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="23eab-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="23eab-287">Er moeten dus facturen aan u zijn toegewezen die de correcte status hebben, zodat de workflowacties beschikbaar voor u kunnen worden gemaakt waarvoor u een ontwerp gaat ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="23eab-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="23eab-288">Workflowacties opnemen</span><span class="sxs-lookup"><span data-stu-id="23eab-288">Record workflow actions</span></span>
1.  <span data-ttu-id="23eab-289">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="23eab-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="23eab-290">Selecteer de pagina **Factuurdetails** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="23eab-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="23eab-291">Klik op het tabblad **Acties** op **Actie toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="23eab-292">Voer een actietitel in, zoals **Goedkeuren**, en een omschrijving, zoals **Factuur goedkeuren**.</span><span class="sxs-lookup"><span data-stu-id="23eab-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="23eab-293">Houd er rekening mee dat de titel van de actie die u hier invoert, de naam wordt van de actie die wordt weergegeven aan de gebruiker in de mobiele toepassing.</span><span class="sxs-lookup"><span data-stu-id="23eab-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="23eab-294">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="23eab-294">Click **Done**.</span></span>
6.  <span data-ttu-id="23eab-295">Klik op **Velden selecteren**.</span><span class="sxs-lookup"><span data-stu-id="23eab-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="23eab-296">Doorloop het workflowproces op de pagina **VendMobileInvoiceHeaderDetails** en voer de actie uit die u wilt registreren.</span><span class="sxs-lookup"><span data-stu-id="23eab-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="23eab-297">Zorg dat u workflowopmerkingen tijdens dit proces invoert, zodat er ook een veld met opmerkingen in de mobiele ervaring wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="23eab-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="23eab-298">Nadat de workflowactie is uitgevoerd, klikt u op **Gereed** om de taak Velden selecteren te voltooien.</span><span class="sxs-lookup"><span data-stu-id="23eab-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="23eab-299">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="23eab-300">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="23eab-301">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="23eab-302">Herhaal de vorige stappen om alle vereiste workflowacties te registreren.</span><span class="sxs-lookup"><span data-stu-id="23eab-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="23eab-303">Een js-bestand maken.</span><span class="sxs-lookup"><span data-stu-id="23eab-303">Create a .js file</span></span>
1. <span data-ttu-id="23eab-304">Open Kladblok of Microsoft Visual Studio en plak de volgende code.</span><span class="sxs-lookup"><span data-stu-id="23eab-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="23eab-305">Sla het rapport als een .js-bestand op.</span><span class="sxs-lookup"><span data-stu-id="23eab-305">Save the file as a .js file.</span></span> <span data-ttu-id="23eab-306">Deze code voert het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="23eab-306">This code does the following:</span></span>
    - <span data-ttu-id="23eab-307">De extra workflowgerelateerde kolommen worden verborgen die we eerder op de mobiele lijstpagina hebben toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="23eab-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="23eab-308">We hebben deze kolommen toegevoegd zodat de app die informatie in context heeft en de volgende stap kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="23eab-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="23eab-309">Op basis van de workflowstap die actief is, wordt deze logica toegepast om slechts twee acties weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23eab-310">De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="23eab-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```

2.  <span data-ttu-id="23eab-311">Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren</span><span class="sxs-lookup"><span data-stu-id="23eab-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="23eab-312">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="23eab-313">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="23eab-314">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="23eab-315">Leveranciersfactuurbijlagen</span><span class="sxs-lookup"><span data-stu-id="23eab-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="23eab-316">Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.</span><span class="sxs-lookup"><span data-stu-id="23eab-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="23eab-317">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="23eab-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="23eab-318">Selecteer de pagina <strong>Factuurdetails\*\* die u eerder hebt gemaakt en klik vervolgens op \*\*Bewerken</strong>.</span><span class="sxs-lookup"><span data-stu-id="23eab-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="23eab-319">Stel de optie **Documentbeheer** in op **Ja** zoals hieronder wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="23eab-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="23eab-320">**Opmerking:** als er geen vereisten zijn om bijlagen weer te geven op het mobiele apparaat, kunt u deze optie ingesteld laten op **Nee**. Dit is de standaardinstelling.</span><span class="sxs-lookup"><span data-stu-id="23eab-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Documentbeheer](./media/docmanagement-216x300.png)

5. <span data-ttu-id="23eab-322">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="23eab-323">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="23eab-324">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="23eab-325">Leveranciersfactuurregelverdelingen</span><span class="sxs-lookup"><span data-stu-id="23eab-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="23eab-326">Met vereisten voor dit scenario wordt bevestigd dat er alleen verdelingen op regelniveau zijn en dat een factuur altijd slechts één regel heeft.</span><span class="sxs-lookup"><span data-stu-id="23eab-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="23eab-327">Omdat dit scenario eenvoudig is, moet de gebruikerservaring op het mobiele apparaat ook zo eenvoudig zijn dat de gebruiker geen detailanalyse hoeft uit te voeren op verschillende niveaus om de verdelingen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="23eab-328">Leveranciersfacturen hebben ook de optie om alle verdelingen uit de factuurkoptekst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="23eab-329">Deze ervaring is wat we nodig hebben voor het mobiele scenario.</span><span class="sxs-lookup"><span data-stu-id="23eab-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="23eab-330">Daarom gebruiken we de pagina **VendMobileInvoiceAllDistributionTree** om dit deel van het mobiele scenario te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="23eab-331">Op basis van de vereisten kunnen we bepalen welke specifieke pagina moet worden gebruikt en hoe de mobiele ervaring exact moet worden geoptimaliseerd voor de gebruiker bij het ontwerp van het scenario.</span><span class="sxs-lookup"><span data-stu-id="23eab-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="23eab-332">In het tweede scenario gebruiken we een andere pagina om de verdelingen weer te geven, omdat de vereisten voor dat scenario verschillen.</span><span class="sxs-lookup"><span data-stu-id="23eab-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="23eab-333">Vervang in de URL de naam van de menuoptie, zoals u eerder hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="23eab-334">De pagina die verschijnt, moet lijken op de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="23eab-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="23eab-335">[![Pagina Alle verdelingen](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="23eab-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="23eab-336">Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).</span><span class="sxs-lookup"><span data-stu-id="23eab-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="23eab-337">Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.</span><span class="sxs-lookup"><span data-stu-id="23eab-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="23eab-338">**Opmerking:** u ziet dat er automatisch twee nieuwe pagina's zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="23eab-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="23eab-339">Omdat u documentbeheer in het vorige gedeelte hebt ingeschakeld, worden deze pagina's gemaakt.</span><span class="sxs-lookup"><span data-stu-id="23eab-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="23eab-340">U kunt deze nieuwe pagina's negeren.</span><span class="sxs-lookup"><span data-stu-id="23eab-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="23eab-341">Klik op **Pagina toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="23eab-342">Voer een paginatitel in, zoals **Boekhouding weergeven**, en een omschrijving, zoals **Boekhouding weergeven voor de factuur**.</span><span class="sxs-lookup"><span data-stu-id="23eab-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="23eab-343">Klik op **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="23eab-343">Click **Done**.</span></span>

7.  <span data-ttu-id="23eab-344">Selecteer op het tabblad **Velden** **Velden selecteren**, selecteer de volgende velden op de pagina Verdelingen en klik op **Gereed**:</span><span class="sxs-lookup"><span data-stu-id="23eab-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="23eab-345">Bedrag</span><span class="sxs-lookup"><span data-stu-id="23eab-345">Amount</span></span>
    2.  <span data-ttu-id="23eab-346">Valuta</span><span class="sxs-lookup"><span data-stu-id="23eab-346">Currency</span></span>
    3.  <span data-ttu-id="23eab-347">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="23eab-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="23eab-348">We hebben de kolom **Omschrijving** uit het raster Verdelingen niet geselecteerd, omdat de vereisten voor dit scenario hebben bevestigd dat de totaalprijs het enige bedrag is waarvoor er verdelingen zijn.</span><span class="sxs-lookup"><span data-stu-id="23eab-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="23eab-349">De gebruiker heeft daarom geen ander veld nodig om het bedragtype te bepalen waarvoor de verdeling is bestemd.</span><span class="sxs-lookup"><span data-stu-id="23eab-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="23eab-350">In het volgende scenario gebruiken we echter deze gegevens **wel**, omdat de vereisten voor dat scenario aangeven dat andere bedragtypen verdelingen hebben (bijvoorbeeld btw).</span><span class="sxs-lookup"><span data-stu-id="23eab-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="23eab-351">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="23eab-352">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="23eab-353">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="23eab-354">Navigatie toevoegen aan de pagina 'Boekhouding weergeven'</span><span class="sxs-lookup"><span data-stu-id="23eab-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="23eab-355">De mobiele pagina **Boekhouding weergeven** is nu nog niet gekoppeld aan een van de mobiele pagina's die we tot nu toe hebben ontworpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="23eab-356">Omdat de gebruiker moet kunnen navigeren naar de pagina **Boekhouding weergeven** van de pagina **Factuurdetails** op het mobiele apparaat, moeten wij navigatie verschaffen vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="23eab-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="23eab-357">We stellen deze navigatie in met behulp van aanvullende logica via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="23eab-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="23eab-358">Open het .js-bestand dat u eerder hebt gemaakt en voeg de regels toe die in de volgende code zijn gemarkeerd.</span><span class="sxs-lookup"><span data-stu-id="23eab-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="23eab-359">Deze code doet twee dingen:</span><span class="sxs-lookup"><span data-stu-id="23eab-359">This code does two things:</span></span>
    1.  <span data-ttu-id="23eab-360">Dit helpt te garanderen dat gebruikers niet rechtstreeks van het werkgebied naar de pagina **Boekhouding weergeven** kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="23eab-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="23eab-361">Er wordt een navigatiebesturingselement ingesteld vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**.</span><span class="sxs-lookup"><span data-stu-id="23eab-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="23eab-362">De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="23eab-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```
    
2.  <span data-ttu-id="23eab-363">Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren om de vorige code te overschrijven</span><span class="sxs-lookup"><span data-stu-id="23eab-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="23eab-364">Klik op **Gereed** om de bewerkingsmodus af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="23eab-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="23eab-365">Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten</span><span class="sxs-lookup"><span data-stu-id="23eab-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="23eab-366">Klik op **Werkgebied publiceren** om uw werk op te slaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="23eab-367">Validatie</span><span class="sxs-lookup"><span data-stu-id="23eab-367">Validation</span></span>

<span data-ttu-id="23eab-368">Open op uw mobiele apparaat de app en maak verbinding met uw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="23eab-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="23eab-369">Zorg ervoor dat u zich aanmeldt bij het bedrijf waar leveranciersfacturen ter controle aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="23eab-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="23eab-370">U moet de volgende acties kunnen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="23eab-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="23eab-371">Zie het werkgebied **Mijn goedkeuringen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="23eab-372">Zoom in op het werkgebied **Mijn goedkeuringen** en bekijk de pagina **Mijn leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="23eab-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="23eab-373">Zoom in op de pagina **Mijn leveranciersfacturen** en bekijk de lijst met facturen die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="23eab-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="23eab-374">Zoom in op een van de facturen en bekijk de factuurkoptekstdetails en de factuurregeldetails.</span><span class="sxs-lookup"><span data-stu-id="23eab-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="23eab-375">Bekijk op de detailpagina een koppeling naar bijlagen en gebruik deze koppeling om naar de lijst met bijlagen te navigeren en de bijlagen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="23eab-376">Bekijk op de detailpagina een koppeling naar de pagina **Boekhouding weergeven** en gebruik deze koppeling om naar de pagina met verdelingen te navigeren en geef de verdelingen weer.</span><span class="sxs-lookup"><span data-stu-id="23eab-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="23eab-377">Klik op de detailpagina op het menu **Acties** onderaan en voer workflowacties uit die van toepassing op de workflowstap zijn.</span><span class="sxs-lookup"><span data-stu-id="23eab-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="23eab-378">Een complex factuurgoedkeuringsscenario ontwerpen voor Fabrikam</span><span class="sxs-lookup"><span data-stu-id="23eab-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23eab-379">Scenariokenmerk</span><span class="sxs-lookup"><span data-stu-id="23eab-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="23eab-380">Beantwoorden</span><span class="sxs-lookup"><span data-stu-id="23eab-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23eab-381">Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="23eab-382">Leveranciernaam</span><span class="sxs-lookup"><span data-stu-id="23eab-382">Vendor name</span></span></li>
<li><span data-ttu-id="23eab-383">Factuurbedrag</span><span class="sxs-lookup"><span data-stu-id="23eab-383">Invoice amount</span></span></li>
<li><span data-ttu-id="23eab-384">Te factureren rekening</span><span class="sxs-lookup"><span data-stu-id="23eab-384">Invoice account</span></span></li>
<li><span data-ttu-id="23eab-385">Factuurnummer</span><span class="sxs-lookup"><span data-stu-id="23eab-385">Invoice number</span></span></li>
<li><span data-ttu-id="23eab-386">Factuurdatum</span><span class="sxs-lookup"><span data-stu-id="23eab-386">Invoice date</span></span></li>
<li><span data-ttu-id="23eab-387">Factuuromschrijving</span><span class="sxs-lookup"><span data-stu-id="23eab-387">Invoice description</span></span></li>
<li><span data-ttu-id="23eab-388">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="23eab-388">Due date</span></span></li>
<li><span data-ttu-id="23eab-389">Factuurvaluta</span><span class="sxs-lookup"><span data-stu-id="23eab-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-390">Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</span><span class="sxs-lookup"><span data-stu-id="23eab-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="23eab-391">Inkoopcategorie</span><span class="sxs-lookup"><span data-stu-id="23eab-391">Procurement category</span></span></li>
<li><span data-ttu-id="23eab-392">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="23eab-392">Quantity</span></span></li>
<li><span data-ttu-id="23eab-393">Eenheidsprijs</span><span class="sxs-lookup"><span data-stu-id="23eab-393">Unit price</span></span></li>
<li><span data-ttu-id="23eab-394">Nettobedrag per regel</span><span class="sxs-lookup"><span data-stu-id="23eab-394">Line net amount</span></span></li>
<li><span data-ttu-id="23eab-395">1099-bedrag</span><span class="sxs-lookup"><span data-stu-id="23eab-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-396">Hoeveel factuurregels bevat een factuur?</span><span class="sxs-lookup"><span data-stu-id="23eab-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="23eab-397">Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</span><span class="sxs-lookup"><span data-stu-id="23eab-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="23eab-398">5</span><span class="sxs-lookup"><span data-stu-id="23eab-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-399">Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</span><span class="sxs-lookup"><span data-stu-id="23eab-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="23eab-400">Ja</span><span class="sxs-lookup"><span data-stu-id="23eab-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-401">Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel?</span><span class="sxs-lookup"><span data-stu-id="23eab-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="23eab-402">Pas de 80-20-regel opnieuw toe.</span><span class="sxs-lookup"><span data-stu-id="23eab-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="23eab-403">Totaalprijs: 2 btw: 2 toeslagen: 2</span><span class="sxs-lookup"><span data-stu-id="23eab-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23eab-404">Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst?</span><span class="sxs-lookup"><span data-stu-id="23eab-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="23eab-405">In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</span><span class="sxs-lookup"><span data-stu-id="23eab-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="23eab-406">Niet gebruikt</span><span class="sxs-lookup"><span data-stu-id="23eab-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23eab-407">Willen gebruikers bijlagen voor de factuur op het apparaat zien?</span><span class="sxs-lookup"><span data-stu-id="23eab-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="23eab-408">Ja</span><span class="sxs-lookup"><span data-stu-id="23eab-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="23eab-409">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="23eab-409">Next steps</span></span>

<span data-ttu-id="23eab-410">De volgende variaties kunnen worden uitgevoerd voor scenario 1, op basis van de vereisten voor scenario 2.</span><span class="sxs-lookup"><span data-stu-id="23eab-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="23eab-411">U kunt deze sectie gebruiken om de ervaring in uw mobiele app te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="23eab-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="23eab-412">Omdat er meer factuurregels worden verwacht in scenario 2, helpen de volgende wijzigingen in het ontwerp de gebruikerservaring op het mobiele apparaat te optimaliseren:</span><span class="sxs-lookup"><span data-stu-id="23eab-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="23eab-413">In plaats van factuurregels weer te geven op de detailpagina (zoals in scenario 1), kunnen gebruikers ervoor kiezen regels op een aparte mobiele pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="23eab-414">Omdat meer dan één factuurregel wordt verwacht in dit scenario als de pagina **VendMobileInvoiceAllDistributionTree** wordt gebruikt voor het ontwerpen van de pagina Verdelingen voor mobiele apparaten (zoals in scenario 1), kan dat verwarrend zijn voor de gebruiker om regels te relateren aan verdelingen.</span><span class="sxs-lookup"><span data-stu-id="23eab-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="23eab-415">Gebruik daarom de pagina **VendMobileInvoiceLineDistributionTree** om de pagina Verdelingen te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="23eab-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="23eab-416">In het ideale geval moeten de verdelingen worden weergegeven in de context van een factuurregel in dit scenario.</span><span class="sxs-lookup"><span data-stu-id="23eab-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="23eab-417">Zorg er daarom voor dat de gebruiker kan inzoomen op een regel om de pagina Verdelingen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="23eab-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="23eab-418">Gebruik de paginakoppelingmogelijkheid om het inzoomen in te stellen, net als u voor de koptekst en detailpagina's in scenario 1 hebt gedaan.</span><span class="sxs-lookup"><span data-stu-id="23eab-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="23eab-419">Omdat meer dan één bedragtype wordt verwacht voor de verdelingen in scenario 2 (btw, toeslagen, enzovoort), is het nuttig om de omschrijving van het bedragtype weer te geven.</span><span class="sxs-lookup"><span data-stu-id="23eab-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="23eab-420">(We hebben deze informatie in scenario 1 weggelaten.)</span><span class="sxs-lookup"><span data-stu-id="23eab-420">(We omitted this information in scenario 1.)</span></span>




