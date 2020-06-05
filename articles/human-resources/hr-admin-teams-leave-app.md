---
title: Human resources-app in Teams
description: In dit onderwerp maakt u kennis met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388111"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="edcd6-103">Human resources-app in Teams</span><span class="sxs-lookup"><span data-stu-id="edcd6-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="edcd6-104">Met de Microsoft Dynamics 365 Human Resources-app in Microsoft Teams kunnen werknemers snel verlof aanvragen en informatie over hun verlofsaldo bekijken in Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="edcd6-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="edcd6-105">Werknemers kunnen communiceren met een bot om informatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="edcd6-106">Het tabblad **Verlof** bevat meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="edcd6-106">The **Time off** tab provides more detailed information.</span></span>

![Bot voor verlof-app in Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Tabblad Verlof in verlof-app voor Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="edcd6-109">Installeren en instellen</span><span class="sxs-lookup"><span data-stu-id="edcd6-109">Install and setup</span></span>

<span data-ttu-id="edcd6-110">De Human resources-app is te vinden in het Teams-archief.</span><span class="sxs-lookup"><span data-stu-id="edcd6-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="edcd6-111">Zie [Verlofaanvragen in Teams beheren](hr-teams-leave-app.md) voor meer informatie over het installeren van de Teams-app.</span><span class="sxs-lookup"><span data-stu-id="edcd6-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="edcd6-112">Zie [Machtigingsbeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) voor informatie over het beheren van app-machtigingen in Teams.</span><span class="sxs-lookup"><span data-stu-id="edcd6-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="edcd6-113">Bekende problemen</span><span class="sxs-lookup"><span data-stu-id="edcd6-113">Known issues</span></span>

| <span data-ttu-id="edcd6-114">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="edcd6-114">Issue</span></span> | <span data-ttu-id="edcd6-115">Status</span><span class="sxs-lookup"><span data-stu-id="edcd6-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="edcd6-116">Het saldo is onjuist bij het indienen van verlof voor een toekomstige datum.</span><span class="sxs-lookup"><span data-stu-id="edcd6-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="edcd6-117">Prognose maken is nog niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="edcd6-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="edcd6-118">Het saldo wordt weergegeven voor de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="edcd6-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="edcd6-119">Bij het verminderen van het aantal uren in een bestaande aanvraag gaat het **Resterende saldo** omlaag in plaats van omhoog.</span><span class="sxs-lookup"><span data-stu-id="edcd6-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="edcd6-120">Dit bekende probleem wordt in de toekomst verholpen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="edcd6-121">De weergave is onjuist, maar de juiste bedragen worden aangepast bij het indienen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="edcd6-122">Twee kaarten **Aanstaand verlof** worden weergegeven voor dezelfde datums.</span><span class="sxs-lookup"><span data-stu-id="edcd6-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="edcd6-123">De kaarten vertegenwoordigen afzonderlijke indieningen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-123">The cards represent individual submissions.</span></span> <span data-ttu-id="edcd6-124">We blijven feedback accepteren en wijzigingen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="edcd6-125">Kan een aanvraag **Wordt gecontroleerd** niet annuleren.</span><span class="sxs-lookup"><span data-stu-id="edcd6-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="edcd6-126">Deze functionaliteit wordt momenteel niet ondersteund en wordt in een toekomstige versie toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="edcd6-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="edcd6-127">Saldogegevens worden vanaf vandaag berekend.</span><span class="sxs-lookup"><span data-stu-id="edcd6-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="edcd6-128">Het systeem geeft momenteel geen saldi weer voor de toerekeningsperiode, zelfs als deze is geconfigureerd in de parameters voor verlof en verzuim.</span><span class="sxs-lookup"><span data-stu-id="edcd6-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="edcd6-129">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="edcd6-129">Privacy notice</span></span>

<span data-ttu-id="edcd6-130">Bij de bot voor Dynamics 365 Human Resources in Microsoft Teams wordt de tekstinvoer van de gebruiker geanalyseerd om de onderliggende vraag/intentie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="edcd6-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="edcd6-131">De invoer van de gebruiker, zoals 'Zoek account Contoso', wordt doorgestuurd naar een van de cognitieve services van Microsoft, de zogeheten Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="edcd6-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="edcd6-132">Lees  [hier](https://www.luis.ai/) meer over LUIS.</span><span class="sxs-lookup"><span data-stu-id="edcd6-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="edcd6-133">De LUIS-service maakt de gebruikersinvoer eenduidig of begrijpt de intentie van gebruikersinvoer (in dit geval is de intentie om informatie te vinden) en de doelentiteit (in dit geval is een account met de naam Contoso de bedoelde entiteit).</span><span class="sxs-lookup"><span data-stu-id="edcd6-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="edcd6-134">Deze informatie wordt vervolgens doorgegeven aan het  [Azure-botraamwerk](https://azure.microsoft.com/services/bot-service/)  van Microsoft, dat interacties aangaat met gegevens uit Dynamics 365 Human Resources en de gewenste informatie ophaalt voor de gebruikersquery.</span><span class="sxs-lookup"><span data-stu-id="edcd6-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="edcd6-135">Door de bot het installeren en toestemming te verlenen voor gebruik van de bot stemt u ermee dat de LUIS-service en het Azure-botraamwerk de intentie achter de invoer verwerken, wat resulteert in een betere gesprekservaring voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="edcd6-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="edcd6-136">De LUIS-service en het Azure-botraamwerk hebben mogelijk verschillende conformiteitsniveaus in vergelijking met Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="edcd6-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="edcd6-137">Terwijl de LUIS-service alleen toegang heeft tot de gebruikersquery's en niet is ontworpen om te worden verbonden met de Dynamics 365 Human Resources-gegevens of de account van de gebruiker, kan een gebruiker van de bot in Dynamics 365 Human Resources een query uitvoeren die klantgegevens, persoonlijke gegevens of andere gegevens bevat. Deze query-inhoud kan vervolgens naar de LUIS-service en het Azure-botraamwerk worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="edcd6-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="edcd6-138">De inhoud van de query's en berichten van de gebruiker wordt gedurende maximaal 30 dagen in het LUIS-systeem bewaard, is in rusttoestand versleuteld en wordt niet gebruikt voor training of serviceverbetering.</span><span class="sxs-lookup"><span data-stu-id="edcd6-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="edcd6-139">Lees  [hier](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) meer over Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="edcd6-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="edcd6-140">Als u beheerinstellingen voor apps wilt beheren in Microsoft Teams, gaat u naar het [Microsoft Teams-beheercentrum](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="edcd6-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="edcd6-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="edcd6-141">See also</span></span> 

[<span data-ttu-id="edcd6-142">Microsoft Teams downloaden en installeren</span><span class="sxs-lookup"><span data-stu-id="edcd6-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="edcd6-143">Microsoft Teams-helpcentrum</span><span class="sxs-lookup"><span data-stu-id="edcd6-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="edcd6-144">Verlofaanvragen beheren in Teams</span><span class="sxs-lookup"><span data-stu-id="edcd6-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

