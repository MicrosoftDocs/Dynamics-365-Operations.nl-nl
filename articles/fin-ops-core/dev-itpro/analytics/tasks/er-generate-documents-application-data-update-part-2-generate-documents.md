---
title: Configuraties ontwerpen voor het genereren van documenten die toepassingsgegevens bevatten
description: Dit onderwerp laat zien hoe u configuraties voor elektronische rapportage (ER) ontwerpt voor het genereren van elektronische documenten. (Deel 1 - Configuraties importeren).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751077"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="4c5f7-104">Configuraties ontwerpen voor het genereren van documenten die toepassingsgegevens bevatten</span><span class="sxs-lookup"><span data-stu-id="4c5f7-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c5f7-105">Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 1: configuraties importeren)' voltooien.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="4c5f7-106">De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="4c5f7-107">In deze procedure voert u de geïmporteerde ER-indelingsconfiguraties uit die zijn gemaakt voor het voorbeeldbedrijf, Litware, Inc. om elektronische documenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="4c5f7-108">Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4c5f7-109">Deze stappen kunnen worden voltooid met de DEMF-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="4c5f7-110">Voordat u begint, moet u de context van het land/de regio wijzigen voor het DEMF-bedrijf, van DEU (Duitsland) naar BEL (België).</span><span class="sxs-lookup"><span data-stu-id="4c5f7-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="4c5f7-111">Klik op Organisatiebeheer > Organisaties > Rechtspersonen om de land/regio-code bij te werken in het primaire adres van de rechtspersoon DEMF.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="4c5f7-112">Start uw toepassing opnieuw.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="4c5f7-113">Geïmporteerde ER-indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="4c5f7-113">Run imported ER format</span></span>
1. <span data-ttu-id="4c5f7-114">Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4c5f7-115">Vouw in de structuur 'Intrastat (model)' uit.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="4c5f7-116">Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="4c5f7-117">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-117">Click Run.</span></span>
    * <span data-ttu-id="4c5f7-118">Voer de conceptversie van de ER-indelingsconfiguratie uit om het Intrastat-rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="4c5f7-119">Typ in het veld Invoeren 'intrastat.xml'.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="4c5f7-120">Geef de naam van het bestand op.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="4c5f7-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-121">Click OK.</span></span>
    * <span data-ttu-id="4c5f7-122">Bekijk het gegenereerde XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="4c5f7-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-123">Close the page.</span></span>
8. <span data-ttu-id="4c5f7-124">Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="4c5f7-125">Open dit formulier om de Intrastat-transacties weer te geven die zijn opgenomen in het gegenereerde elektronische document.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="4c5f7-126">Klik op Intrastat-archief.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="4c5f7-127">Omdat de uitgevoerde ER-indeling geen instellingen voor het bijwerken van toepassingsgegevens bevat, zijn de details van het voltooide Intrastat-rapport niet gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="4c5f7-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-128">Close the page.</span></span>
11. <span data-ttu-id="4c5f7-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4c5f7-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]