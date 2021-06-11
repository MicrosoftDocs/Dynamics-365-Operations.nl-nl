---
title: Procesautomatiseringsstromen aanroepen om kwaliteitsorders te maken
description: Dit onderwerp biedt resources om met Power Automate bedrijfsprocessen te automatiseren aan de hand van het voorbeeld van kwaliteitsorders.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115174"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="c9ebd-103">Procesautomatiseringsstromen aanroepen om kwaliteitsorders te maken</span><span class="sxs-lookup"><span data-stu-id="c9ebd-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="c9ebd-104">Bij organisaties bestaat steeds meer de behoefte om standaardbedrijfsprocessen te automatiseren, handigere interacties voor het personeel te verschaffen en gebruik te maken van verschillende gegevenssignaleringen en systemen om bedrijfsprocessen automatisch aan te sturen.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="c9ebd-105">Met Robotic Process Automation (RPA) en Microsoft Power Automate kunnen bedrijven gebruikmaken van een ervaring zonder code om herhalende processen te automatiseren, waardoor efficiëntie en nauwkeurigheid worden verbeterd.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="c9ebd-106">De sjabloon voor downloadbare automatiseringsoplossingen voor Supply Chain Management laat zien hoe u met Power Automate bedrijfsprocessen kunt automatiseren door kwaliteitsorders als voorbeeld te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="c9ebd-107">U kunt de sjabloon voor automatiseringsoplossingen [hier](https://aka.ms/D365SCMQualityOrderRPASolution) downloaden.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="c9ebd-108">Zie de volgende video voor een overzicht van deze functie en de mogelijkheden: [RPA gebruiken om kwaliteitsorders te maken in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="c9ebd-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="c9ebd-109">![Automatiseringsopties met RPA](media/rpa-automation-options.png "Automatiseringsopties met RPA")</span><span class="sxs-lookup"><span data-stu-id="c9ebd-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="c9ebd-110">De oplossingssjabloon van Power Automate bevat een cloudautomatiseringsstroom en een desktopautomatiseringsstroom waarmee het maken van kwaliteitsorders in Supply Chain Management wordt geautomatiseerd.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="c9ebd-111">De automatisering kan worden gestart als reactie op een groot aantal gebeurtenissen en signalen, waaronder gebruikersinvoer of machinesignalen (inclusief Internet of Things (IoT)).</span><span class="sxs-lookup"><span data-stu-id="c9ebd-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="c9ebd-112">Het voorbeeld van de *Q-Order* Power Application is opgenomen in de oplossingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="c9ebd-113">Hiermee kan de gebruiker een QR-code voor een artikel scannen, hoeveelheid invoeren en foto's met een camera bijvoegen.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="c9ebd-114">Oplossingsparameters zijn opgenomen voor het configureren van de automatisering voor een specifieke use case in een productiefaciliteit.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="c9ebd-115">![Kwaliteitsorder maken](media/rpa-create-quality-roder.png "Kwaliteitsorder maken")</span><span class="sxs-lookup"><span data-stu-id="c9ebd-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="c9ebd-116">Raadpleeg [Maken van kwaliteitsorders automatiseren in Dynamics 365 Supply Chain Management met behulp van Robotic Process Automation met Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa) voor een volledige stapsgewijze ondersteuning bij het downloaden, installeren en gebruiken van de voorbeeldoplossing voor het automatiseren van het maken van kwaliteitsorders.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

