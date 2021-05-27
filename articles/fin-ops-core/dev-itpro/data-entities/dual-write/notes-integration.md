---
title: Integratie van notities
description: In dit onderwerp wordt de integratie van notitiesgegevens bij twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018381"
---
# <a name="note-integration"></a><span data-ttu-id="351f7-103">Integratie van notities</span><span class="sxs-lookup"><span data-stu-id="351f7-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="351f7-104">Tijdens bedrijfsprocessen verzamelen Microsoft Dynamics 365-gebruikers vaak informatie over hun klanten.</span><span class="sxs-lookup"><span data-stu-id="351f7-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="351f7-105">Deze informatie wordt geregistreerd als activiteiten en notities.</span><span class="sxs-lookup"><span data-stu-id="351f7-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="351f7-106">In dit onderwerp wordt de integratie van notitiesgegevens bij twee keer wegschrijven beschreven.</span><span class="sxs-lookup"><span data-stu-id="351f7-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="351f7-107">Klantgegevens kunnen op de volgende manieren worden geclassificeerd:</span><span class="sxs-lookup"><span data-stu-id="351f7-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="351f7-108">**Bruikbare informatie die een Dynamics 365-gebruiker namens een klant verwerkt**: Contoso (een Dynamics 365-gebruiker) organiseert bijvoorbeeld een spelprogramma.</span><span class="sxs-lookup"><span data-stu-id="351f7-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="351f7-109">Een van de klanten van Contoso (een klant) wil het spelprogramma bijwonen.</span><span class="sxs-lookup"><span data-stu-id="351f7-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="351f7-110">De klant vraagt een Contoso-werknemer om een plekje in het spelprogramma voor hen te boeken.</span><span class="sxs-lookup"><span data-stu-id="351f7-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="351f7-111">De boeking vindt plaats in de kalender van de gebeurtenisdeelnemer van Contoso.</span><span class="sxs-lookup"><span data-stu-id="351f7-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="351f7-112">**Bruikbare informatie voor een Dynamics 365-gebruiker**: een klant die een Surface-eenheid aanschaft, voert bijvoorbeeld speciale instructies in om aan te geven dat het apparaat als geschenk moet worden ingepakt voordat het wordt afgeleverd.</span><span class="sxs-lookup"><span data-stu-id="351f7-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="351f7-113">Deze instructies zijn bruikbare gegevens die moeten worden verwerkt door de Contoso-werknemer die verantwoordelijk is voor de verpakking.</span><span class="sxs-lookup"><span data-stu-id="351f7-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="351f7-114">**Niet-bruikbare informatie**: een klant bezoekt bijvoorbeeld de Contoso-winkel en toont tijdens het gesprek met een winkelmedewerker interesse in *Halo*-games en gamingaccessoires.</span><span class="sxs-lookup"><span data-stu-id="351f7-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="351f7-115">De winkelmedewerker maakt een notitie van deze informatie.</span><span class="sxs-lookup"><span data-stu-id="351f7-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="351f7-116">De engine voor productaanbevelingen gebruikt deze dan om aanbevelingen te doen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="351f7-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="351f7-117">Bruikbare informatie wordt over het algemeen vastgelegd als *activiteiten* in Finance and Operations-aps en apps voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="351f7-118">Niet-bruikbare informatie wordt over het algemeen vastgelegd als *notities* in Finance and Operations-apps en als *aantekeningen* in apps voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="351f7-119">Hoewel notities zijn bedoeld voor niet-bruikbare informatie, kunnen de apps wel worden gebruikt voor het opslaan en verwerken van bruikbare informatie als u deze op die manier wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="351f7-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="351f7-120">Microsoft brengt momenteel functionaliteit voor integratie van notities uit.</span><span class="sxs-lookup"><span data-stu-id="351f7-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="351f7-121">(Functionaliteit voor activiteitsintegratie wordt later vrijgegeven.) Integratie van notities is beschikbaar voor klanten, leveranciers, verkooporders en inkooporders.</span><span class="sxs-lookup"><span data-stu-id="351f7-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="351f7-122">Een notitie maken in een app voor klantbetrokkenheid</span><span class="sxs-lookup"><span data-stu-id="351f7-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="351f7-123">Volg deze stappen om een notitie te maken in een app voor klantbetrokkenheid en deze vervolgens te synchroniseren met een Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="351f7-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="351f7-124">Open in de app voor klantbetrokkenheid de rekeningrecord voor een klant.</span><span class="sxs-lookup"><span data-stu-id="351f7-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="351f7-125">Selecteer in het deelvenster **Tijdlijn** het plusteken (**+**) en selecteer vervolgens **Notitie** om een notitie te maken.</span><span class="sxs-lookup"><span data-stu-id="351f7-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Een notitie maken in de app voor klantbetrokkenheid](media/notes-ce-1.png)

3. <span data-ttu-id="351f7-127">Voer een titel en beschrijving in en selecteer vervolgens **Notitie toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="351f7-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Een titel en beschrijving invoeren](media/notes-ce-2.png)

    <span data-ttu-id="351f7-129">De nieuwe notitie wordt toegevoegd aan de tijdlijn van de klant.</span><span class="sxs-lookup"><span data-stu-id="351f7-129">The new note is added to the customer timeline.</span></span>

    ![Nieuwe notitie op de tijdlijn van klant](media/notes-ce-3.png)

4. <span data-ttu-id="351f7-131">Meld u aan bij de Finance and Operations-app en open dezelfde klantrecord.</span><span class="sxs-lookup"><span data-stu-id="351f7-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="351f7-132">De knop **Bijlagen** (paperclipsymbool) rechtsboven geeft aan dat de record een bijlage heeft.</span><span class="sxs-lookup"><span data-stu-id="351f7-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Melding over een bijlage](media/notes-ce-4.png)

5. <span data-ttu-id="351f7-134">Selecteer de knop **Bijlagen** om de pagina **Bijlagen** te openen.</span><span class="sxs-lookup"><span data-stu-id="351f7-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="351f7-135">U zou de notitie moeten vinden die u hebt gemaakt in de app voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Notitie vanuit de app voor klantbetrokkenheid](media/notes-ce-5.png)

<span data-ttu-id="351f7-137">Alle updates van de notitie worden heen en weer gesynchroniseerd tussen de Finance and Operations-app en de app voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="351f7-138">Een notitie maken in een Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="351f7-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="351f7-139">U kunt ook een notitie maken in een Finance and Operations-app en deze vervolgens synchroniseren met een app voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="351f7-140">Als u een notitie wilt maken in een Finance and Operations-app en deze wilt synchroniseren met een app voor klantbetrokkenheid, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="351f7-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="351f7-141">Ga naar de Finance and Operations-app en selecteer op de pagina **Bijlagen** de optie **Nieuw** \> **Notitie**.</span><span class="sxs-lookup"><span data-stu-id="351f7-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Een notitie maken in de Finance and Operations-app](media/notes-fo-1.png)

2. <span data-ttu-id="351f7-143">Voer een titel en een korte reeks instructies in en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="351f7-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Een titel en instructies invoeren](media/notes-fo-2.png)

3. <span data-ttu-id="351f7-145">Werk de record bij in de app voor klantbetrokkenheid.</span><span class="sxs-lookup"><span data-stu-id="351f7-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="351f7-146">U zou de nieuwe notitie op de tijdlijn moeten vinden.</span><span class="sxs-lookup"><span data-stu-id="351f7-146">You should find the new note on the timeline.</span></span>

    ![Nieuwe notitie op de tijdlijn in de app voor klantbetrokkenheid](media/notes-fo-3.png)

<span data-ttu-id="351f7-148">U kunt een notitie classificeren als intern of extern.</span><span class="sxs-lookup"><span data-stu-id="351f7-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="351f7-149">Open de notitie in de Finance and Operations-app op de pagina **Bijlagen** en selecteer vervolgens in het veld **Beperking** de optie **Intern** of **Extern**.</span><span class="sxs-lookup"><span data-stu-id="351f7-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Beperkingsveld](media/notes-fo-4.png)

<span data-ttu-id="351f7-151">U kunt ook een URL maken.</span><span class="sxs-lookup"><span data-stu-id="351f7-151">You can also create a URL.</span></span>

1. <span data-ttu-id="351f7-152">Ga naar de Finance and Operations-app en selecteer op de pagina **Bijlagen** de optie **Nieuw** \> **URL**.</span><span class="sxs-lookup"><span data-stu-id="351f7-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="351f7-153">Voer een titel en de URL in.</span><span class="sxs-lookup"><span data-stu-id="351f7-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="351f7-154">Selecteer in het veld **Beperking** de optie **Intern** of **Extern**.</span><span class="sxs-lookup"><span data-stu-id="351f7-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Een URL maken in de Finance and Operations-app](media/notes-fo-5.png)

4. <span data-ttu-id="351f7-156">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="351f7-156">Select **Save**.</span></span>

    <span data-ttu-id="351f7-157">Omdat apps voor klantbetrokkenheid geen URL-type hebben, wordt de URL met twee keer wegschrijven als notitie geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="351f7-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL die wordt weergegeven als notitie maken in de app voor klantbetrokkenheid](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="351f7-159">Bestandsbijlagen worden niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="351f7-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="351f7-160">Sjablonen</span><span class="sxs-lookup"><span data-stu-id="351f7-160">Templates</span></span>

<span data-ttu-id="351f7-161">Integratie van notities omvat een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="351f7-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="351f7-162">Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="351f7-162">Finance and Operations app</span></span> | <span data-ttu-id="351f7-163">Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="351f7-163">Customer engagement app</span></span> | <span data-ttu-id="351f7-164">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="351f7-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="351f7-165">Klantbijlagen</span><span class="sxs-lookup"><span data-stu-id="351f7-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="351f7-166">Aantekeningen</span><span class="sxs-lookup"><span data-stu-id="351f7-166">Annotations</span></span> | <span data-ttu-id="351f7-167">Bedrijven die tekst zonder opmaak en URL's gebruiken om klantspecifieke informatie (voor organisaties en personen) vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="351f7-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="351f7-168">Bijlagen van leveranciersdocument</span><span class="sxs-lookup"><span data-stu-id="351f7-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="351f7-169">Aantekeningen</span><span class="sxs-lookup"><span data-stu-id="351f7-169">Annotations</span></span> | <span data-ttu-id="351f7-170">Bedrijven die tekst zonder opmaak en URL's gebruiken om leverancierspecifieke informatie (voor organisaties en personen) vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="351f7-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="351f7-171">Documentbijlagen van verkooporderkoptekst</span><span class="sxs-lookup"><span data-stu-id="351f7-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="351f7-172">Aantekeningen</span><span class="sxs-lookup"><span data-stu-id="351f7-172">Annotations</span></span> | <span data-ttu-id="351f7-173">Bedrijven die tekst zonder opmaak en URL's gebruiken om specifieke informatie over verkooporders vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="351f7-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="351f7-174">Documentbijlagen van inkooporderkoptekst</span><span class="sxs-lookup"><span data-stu-id="351f7-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="351f7-175">Aantekeningen</span><span class="sxs-lookup"><span data-stu-id="351f7-175">Annotations</span></span> | <span data-ttu-id="351f7-176">Bedrijven die tekst zonder opmaak en URL's gebruiken om specifieke informatie over inkooporders vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="351f7-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="351f7-177">Zie [Toewijzingsverwijzing voor twee keer wegschrijven](mapping-reference.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="351f7-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
