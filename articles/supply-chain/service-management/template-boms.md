---
title: Sjabloonstuklijsten
description: Met een sjabloonstuklijst beschikt u over een gestandaardiseerde lijst onderdelen voor serviceobjecten die regelmatig worden onderhouden.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/21/2018

---

# <a name="template-boms"></a><span data-ttu-id="71334-103">Sjabloonstuklijsten</span><span class="sxs-lookup"><span data-stu-id="71334-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="71334-104">Met een sjabloonstuklijst beschikt u over een gestandaardiseerde lijst onderdelen voor serviceobjecten die regelmatig worden onderhouden.</span><span class="sxs-lookup"><span data-stu-id="71334-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="71334-105">De onderdelen die in de sjabloonstuklijst worden vermeld, vertegenwoordigen de afzonderlijke subonderdelen van het serviceobject.</span><span class="sxs-lookup"><span data-stu-id="71334-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="71334-106">Door een sjabloonstuklijst op een serviceobject toe te passen, kunt u een record van de subonderdelen bijhouden die voor het serviceobject zijn vervangen.</span><span class="sxs-lookup"><span data-stu-id="71334-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="71334-107">Als u een sjabloonstuklijst wilt toepassen op een serviceovereenkomst of een serviceorder, koppelt u deze aan een serviceobjectrelatie.</span><span class="sxs-lookup"><span data-stu-id="71334-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="71334-108">U kunt slechts één sjabloonstuklijst toepassen op een serviceobject.</span><span class="sxs-lookup"><span data-stu-id="71334-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="71334-109">Een sjabloonstuklijst maken</span><span class="sxs-lookup"><span data-stu-id="71334-109">Create a template BOM</span></span>

<span data-ttu-id="71334-110">De volgende tabel bevat informatie over de verschillende methoden die u kunt gebruiken om een sjabloonstuklijst te maken.</span><span class="sxs-lookup"><span data-stu-id="71334-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71334-111">Methode</span><span class="sxs-lookup"><span data-stu-id="71334-111">Method</span></span></p></th>
<th><p><span data-ttu-id="71334-112">Omchrijving</span><span class="sxs-lookup"><span data-stu-id="71334-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71334-113">Productie</span><span class="sxs-lookup"><span data-stu-id="71334-113">Production</span></span></p></td>
<td><p><span data-ttu-id="71334-114">De sjabloonstuklijst is gebaseerd op een productieorder.</span><span class="sxs-lookup"><span data-stu-id="71334-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="71334-115">Deze optie is alleen van toepassing als u in een productieomgeving werkt.</span><span class="sxs-lookup"><span data-stu-id="71334-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="71334-116">Het voordeel is dat u een actuele, gedetailleerde lijst hebt van de onderdelen van een item.</span><span class="sxs-lookup"><span data-stu-id="71334-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71334-117">Artikel BOM</span><span class="sxs-lookup"><span data-stu-id="71334-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="71334-118">De sjabloonstuklijst is gebaseerd op de stuklijst van een artikel.</span><span class="sxs-lookup"><span data-stu-id="71334-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="71334-119">Het onderdeel stuklijst, in tegenstelling tot de productiestuklijst is een statische lijst van de onderdelen van een item.</span><span class="sxs-lookup"><span data-stu-id="71334-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71334-120">Bestaande sjabloon</span><span class="sxs-lookup"><span data-stu-id="71334-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="71334-121">De sjabloon is gebaseerd op een bestaande sjabloonstuklijst.</span><span class="sxs-lookup"><span data-stu-id="71334-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71334-122">Handmatig</span><span class="sxs-lookup"><span data-stu-id="71334-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="71334-123">Als u weet welke onderdelen worden meestal vervangen op serviceobject, kunt u uw sjabloonstuklijst handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="71334-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="71334-124">Deze methode zorgt ervoor dat de onderdelen die zijn opgenomen in de sjabloon overeenkomen met de werkelijke behoeften van uw werkplek.</span><span class="sxs-lookup"><span data-stu-id="71334-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="71334-125">De sjabloonstuklijst toepassen op een serviceovereenkomst of een serviceorder</span><span class="sxs-lookup"><span data-stu-id="71334-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="71334-126">U kunt een sjabloonstuklijst toepassen op een serviceovereenkomst, een serviceorder of allebei.</span><span class="sxs-lookup"><span data-stu-id="71334-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="71334-127">De serviceovereenkomst betreft meestal een langdurige relatie met een klant.</span><span class="sxs-lookup"><span data-stu-id="71334-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="71334-128">De historie van vervangingen die is vastgelegd in de servicestuklijst, is nuttige informatie om op te nemen in de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="71334-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="71334-129">U kunt ook een sjabloonstuklijst op een serviceorder toepassen om de historie van de service te registreren die is uitgevoerd op een serviceobject.</span><span class="sxs-lookup"><span data-stu-id="71334-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="71334-130">De historie van een servicestuklijst kopiëren</span><span class="sxs-lookup"><span data-stu-id="71334-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="71334-131">U kunt de historie van een servicestuklijstregel verplaatsen van de ene serviceovereenkomst naar de andere.</span><span class="sxs-lookup"><span data-stu-id="71334-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="71334-132">Door de servicehistorie te kopiëren tussen serviceovereenkomsten, kunt u de vervangingen bijhouden voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="71334-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="71334-133">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="71334-133">**Example**</span></span>

<span data-ttu-id="71334-134">U hebt een serviceovereenkomst van drie jaar afgesloten voor de auto van een klant.</span><span class="sxs-lookup"><span data-stu-id="71334-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="71334-135">Tijdens die periode wordt de klant gewend aan de goede service die het bedrijf levert.</span><span class="sxs-lookup"><span data-stu-id="71334-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="71334-136">Dus na het verlopen van de overeenkomst wil de klant een nieuwe instellen.</span><span class="sxs-lookup"><span data-stu-id="71334-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="71334-137">Nu kunt u onderhandelen over een gunstigere overeenkomst voor het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="71334-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="71334-138">Aangezien de historie van vervangen onderdelen in de toekomst handig van pas kan komen, kopieert u de historie van de servicestuklijst naar de nieuwe overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="71334-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="71334-139">De sjabloonstuklijst aanpassen</span><span class="sxs-lookup"><span data-stu-id="71334-139">Modify the template BOM</span></span>

<span data-ttu-id="71334-140">Als een sjabloonstuklijst niet aan een serviceobject is gekoppeld, kunt u de regels erin wijzigen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="71334-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="71334-141">Nadat de sjabloonstuklijst aan een serviceobject is gekoppeld, kunt u alleen de lokale versie van de stuklijst nog aanpassen.</span><span class="sxs-lookup"><span data-stu-id="71334-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="71334-142">Als u de instelling van een lokale versie van een sjabloonstuklijst wilt dupliceren, kunt u een nieuwe sjabloonstuklijst maken op basis van de lokale versie.</span><span class="sxs-lookup"><span data-stu-id="71334-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="71334-143">Zie voor meer informatie [Een servicestuklijst wijzigen](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="71334-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="71334-144">Als u een artikel in de stuklijst vervangt, kunt u de vervanging registreren op de stuklijstregel in de stuklijstontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="71334-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="71334-145">U kunt desgewenst een serviceorderregel maken voor een vervangingsobject.</span><span class="sxs-lookup"><span data-stu-id="71334-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="71334-146">Als u een serviceorderregel hebt gemaakt, kunt u het vervangingsartikel factureren.</span><span class="sxs-lookup"><span data-stu-id="71334-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="71334-147">Als u geen serviceorderregel maakt voor een vervanging, wordt de vervanging geregistreerd om de historie van het serviceobject bij te houden.</span><span class="sxs-lookup"><span data-stu-id="71334-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="71334-148">Wijzigen hoe gegevens in de stuklijstregel worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="71334-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="71334-149">U kunt de manier wijzigen waarop stuklijstregelinformatie wordt weergegeven voor alle sjabloon- en servicestuklijsten.</span><span class="sxs-lookup"><span data-stu-id="71334-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="71334-150">De wijzigingen worden toegepast op alle sjabloonstuklijsten en servicestuklijsten.</span><span class="sxs-lookup"><span data-stu-id="71334-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="71334-151">Dit omvat de lijsten die zijn gekoppeld aan serviceobjecten.</span><span class="sxs-lookup"><span data-stu-id="71334-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="71334-152">Nummerreeksen instellen voor sjabloonstuklijsten</span><span class="sxs-lookup"><span data-stu-id="71334-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="71334-153">Om sjabloonstuklijsten te gebruiken, moet u twee nummerreeksen instellen.</span><span class="sxs-lookup"><span data-stu-id="71334-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="71334-154">Stel één nummerreeks in voor de sjabloonstuklijst en één voor het stuklijstregelnummer.</span><span class="sxs-lookup"><span data-stu-id="71334-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="71334-155">Nummerreeksen worden gebruikt om id's toe te wijzen aan records die deze vereisen.</span><span class="sxs-lookup"><span data-stu-id="71334-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="71334-156">Voordat u een nummerreeks aan een sjabloonstuklijst of een regelnummer stuklijstgeschiedenis kunt toewijzen, moet u nummerreekscodes instellen.</span><span class="sxs-lookup"><span data-stu-id="71334-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="71334-157">Nummerreeksen instellen</span><span class="sxs-lookup"><span data-stu-id="71334-157">Set up number sequences</span></span>

1.  <span data-ttu-id="71334-158">Op de pagina **Nummerreeksen** kunt u nummerreeksen maken voor sjabloonstuklijsten en het regelnummer voor de stuklijstgeschiedenis.</span><span class="sxs-lookup"><span data-stu-id="71334-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="71334-159">Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.</span><span class="sxs-lookup"><span data-stu-id="71334-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="71334-160">Klik op **Nummerreeksen** en selecteer vervolgens een nummerreekscode voor de nummerreeksverwijzingen die u hebt gemaakt in het formulier **Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="71334-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="71334-161">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="71334-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="71334-162">Het regelnummer stuklijstgeschiedenis wordt gebruikt om de transacties in de stuklijstgeschiedenis aan een serviceovereenkomst of serviceorder te koppelen.</span><span class="sxs-lookup"><span data-stu-id="71334-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="71334-163">Het nummer wordt niet weergegeven in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="71334-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="71334-164">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71334-164">See also</span></span>

[<span data-ttu-id="71334-165">Een sjabloonstuklijst maken</span><span class="sxs-lookup"><span data-stu-id="71334-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="71334-166">Sjabloonstuklijsten in objectrelaties beheren</span><span class="sxs-lookup"><span data-stu-id="71334-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="71334-167">Een servicestuklijst wijzigen</span><span class="sxs-lookup"><span data-stu-id="71334-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


