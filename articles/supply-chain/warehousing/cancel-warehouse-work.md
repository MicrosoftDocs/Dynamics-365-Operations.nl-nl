---
title: Magazijnwerk voor afhandeling van uitzonderingen annuleren
description: In dit onderwerp wordt de functie Werk annuleren beschreven waarmee magazijnsupervisors geblokkeerd werk kunnen verwerken.
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625855"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="c79bd-103">Magazijnwerk voor afhandeling van uitzonderingen annuleren</span><span class="sxs-lookup"><span data-stu-id="c79bd-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c79bd-104">Met de functie Werk annuleren in Microsoft Dynamics 365 Supply Chain Management kan de beheerdergebruiker specifieke magazijnwerkzaamheden annuleren die momenteel worden uitgevoerd, maar die worden geblokkeerd door het systeem of niet kunnen worden voltooid vanwege uitzonderlijke omstandigheden.</span><span class="sxs-lookup"><span data-stu-id="c79bd-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="c79bd-105">Deze functionaliteit is een aantrekkelijk en veilig alternatief voor SQL-herstelscripts waarmee inconsistente gegevens worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="c79bd-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="c79bd-106">Terwijl deze scripts echter meestal worden aangevraagd bij IT-professionals, kan de functie Werk annuleren worden gebruikt door gebruikers in het bedrijf die beheerdersrechten hebben.</span><span class="sxs-lookup"><span data-stu-id="c79bd-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="c79bd-107">U kunt toegang krijgen tot de functie Werk annuleren via **Magazijnbeheer** \> **Periodieke taken** \> **Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="c79bd-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="c79bd-108">Geef in het dialoogvenster **Werk annuleren** de werk-id op van de werkzaamheden die u wilt annuleren en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79bd-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="c79bd-109">Magazijnwerk dat kan worden geannuleerd</span><span class="sxs-lookup"><span data-stu-id="c79bd-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="c79bd-110">Tijdens orderverzameling in magazijnen kan een werknemer situaties tegenkomen waarbij hoeveelheden die afkomstig zijn van een opslaglocatie zijn geregistreerd naar hun gebruikerlocatie, maar de wegzetbewerking niet kan worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="c79bd-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="c79bd-111">Inconsistente magazijngegevens zijn vaak, maar niet altijd, de reden waarom werk wordt geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c79bd-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="c79bd-112">In tegenstelling tot de normale annuleringsfunctionaliteit die toegankelijk is via de knop **Annuleren** in de werkkoptekst, hoeft bij de functie Werk annuleren de als laatste voltooide werkregel geen werkregel van het type **wegzetten** te zijn.</span><span class="sxs-lookup"><span data-stu-id="c79bd-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="c79bd-113">Met andere woorden, bij de functie Werk annuleren kan de annuleringslogica ook worden uitgevoerd als de artikelhoeveelheid op een werkregel zich op een gebruikerslocatie bevindt.</span><span class="sxs-lookup"><span data-stu-id="c79bd-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="c79bd-114">Voor werk dat om operationele redenen moet worden geannuleerd, moeten magazijngebruikers de normale annuleringsfunctionaliteit op de werkpagina blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c79bd-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="c79bd-115">Alleen werk van het type **Verkoop**, **Overboekingsuitgifte**, **Orderverzameling van grondstoffen** of **Aanvulling** kan worden geannuleerd met de functie Werk annuleren.</span><span class="sxs-lookup"><span data-stu-id="c79bd-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="c79bd-116">De annuleringslogica wordt niet uitgevoerd voor orderverzameling van bevroren grondstoffen of werk dat kan worden geannuleerd met behulp van de normale functie Annuleren (zie de voorgaande opmerking).</span><span class="sxs-lookup"><span data-stu-id="c79bd-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="c79bd-117">Om het werk te deblokkeren, worden eventuele resterende werkregels door het systeem geannuleerd en worden de magazijngegevens hersteld die aan de werk-id zijn gekoppeld die de gebruiker heeft opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c79bd-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="c79bd-118">Normale magazijnverwerkingsactiviteiten voor de desbetreffende artikelhoeveelheid kunnen vervolgens worden hervat.</span><span class="sxs-lookup"><span data-stu-id="c79bd-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="c79bd-119">Als u het desbetreffende artikel op een specifieke locatie wilt neerzetten nadat het werk is geannuleerd, moet de gebruiker een voorraadmutatie of hoeveelheidcorrectie gebruiken op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="c79bd-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
