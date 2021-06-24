---
title: Prestatieproblemen in ER-configuraties oplossen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen in ER-configuraties (Elektronische rapportage) kunt vinden en oplossen.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216860"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="b94bf-103">Prestatieproblemen in ER-configuraties oplossen</span><span class="sxs-lookup"><span data-stu-id="b94bf-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="b94bf-104">In dit onderwerp wordt uitgelegd hoe u prestatieproblemen in [ER-configuraties](general-electronic-reporting.md) [(Elektronische rapportage)](general-electronic-reporting.md#Configuration) kunt vinden en oplossen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="b94bf-105">Prestatieonderzoek bestaat meestal uit verschillende stappen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="b94bf-106">[Gegevens](#collecting-data) verzamelen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="b94bf-107">De verzamelde gegevens analyseren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="b94bf-108">Gebruik op basis van de resultaten van de analyse ER-configuraties om [wijzigingen aan te brengen](#making-changes) of besluit meer gegevens te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b94bf-109">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="b94bf-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="b94bf-110">Uitvoeringstijd analyseren</span><span class="sxs-lookup"><span data-stu-id="b94bf-110">Analyze execution time</span></span>

<span data-ttu-id="b94bf-111">De uitvoeringstijd kan afhankelijk zijn van onverwachte factoren, zoals andere taken die worden uitgevoerd in dezelfde omgeving en van caching waarin gegevens worden gebruikt wanneer deze voor de eerste keer worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="b94bf-112">U moet de uitvoering en meting daarom meerdere keren herhalen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="b94bf-113">Soms worden prestatieproblemen niet veroorzaakt door een ER-indelingsconfiguratie die wordt gebruikt voor rapportage.</span><span class="sxs-lookup"><span data-stu-id="b94bf-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="b94bf-114">Deze worden echter veroorzaakt door de X++-code die wordt gebruikt om die configuratie van de ER-indeling te openen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="b94bf-115">Bekijk de uitvoeringstijd van het rapport in het [actiecentrum](#infolog-time) of in het [gebeurtenislogboek](#event-log-time).</span><span class="sxs-lookup"><span data-stu-id="b94bf-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="b94bf-116">Vergelijk de uitvoeringstijd van het rapport met de totale uitvoeringstijd in het scenario.</span><span class="sxs-lookup"><span data-stu-id="b94bf-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="b94bf-117">Als de uitvoeringstijd van het rapport veel kleiner is dan de totale uitvoeringstijd, moet u de hoeveelheid gegevens bekijken die het rapport verwerkt:</span><span class="sxs-lookup"><span data-stu-id="b94bf-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="b94bf-118">Als in het rapport kleine hoeveelheden gegevens worden verwerkt, heeft het probleem mogelijk te maken met de laadtijd van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="b94bf-119">Als het rapport een grote hoeveelheid gegevens verwerkt, kan het probleem X++ voorverwerking omvatten.</span><span class="sxs-lookup"><span data-stu-id="b94bf-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="b94bf-120">Gebruik [Trace parser](#analyze-trace-parser-trace) om deze case te analyseren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="b94bf-121">Zie de volgende gedeelten voor andere cases.</span><span class="sxs-lookup"><span data-stu-id="b94bf-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="b94bf-122">Voer meerdere tests uit waarbij verschillende hoeveelheden gegevens zijn betrokken om te bepalen hoe de uitvoeringstijd afhankelijk is van de hoeveelheid gegevens.</span><span class="sxs-lookup"><span data-stu-id="b94bf-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="b94bf-123">Trace parser-traces analyseren</span><span class="sxs-lookup"><span data-stu-id="b94bf-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="b94bf-124">Bereid een klein voorbeeld voor of verzamel verschillende traces tijdens willekeurige onderdelen van de rapportgeneratie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="b94bf-125">Vervolgens voert u in [Trace parser](#trace-parser) een standaard bottom-to-up analyse uit en beantwoordt u de volgende vragen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="b94bf-126">Wat zijn de belangrijkste methoden in termen van tijdverbruik?</span><span class="sxs-lookup"><span data-stu-id="b94bf-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="b94bf-127">Welk deel van de algehele tijd wordt door deze methoden gebruikt?</span><span class="sxs-lookup"><span data-stu-id="b94bf-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="b94bf-128">Beantwoord dezelfde vragen voor query's.</span><span class="sxs-lookup"><span data-stu-id="b94bf-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="b94bf-129">Als u ziet dat methoden het voorvoegsel 'ER' hebben, gaat u verder naar het volgende gedeelte.</span><span class="sxs-lookup"><span data-stu-id="b94bf-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="b94bf-130">Als u ziet dat methoden of query's afkomstig zijn van de toepassingssuite, moet u rekening houden met algemene optimalisaties (bijvoorbeeld indexen maken).</span><span class="sxs-lookup"><span data-stu-id="b94bf-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="b94bf-131">Analyseer het aantal aanroepen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-131">Analyze the number of calls.</span></span> <span data-ttu-id="b94bf-132">Als het aantal aanzienlijk hoger is dan verwacht, moet u caching overwegen voor de bijbehorende knooppunten van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="b94bf-133">Databaseaanroepen analyseren</span><span class="sxs-lookup"><span data-stu-id="b94bf-133">Analyze database calls</span></span>

<span data-ttu-id="b94bf-134">Bereid een voorbeeld voor met een kleine hoeveelheid gegevens, zodat u een [ER-trace](#electronic-reporting-traces) kunt verzamelen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="b94bf-135">Open vervolgens de trace in de ontwerper van de ER-modeltoewijzing en kijk onderaan de pagina.</span><span class="sxs-lookup"><span data-stu-id="b94bf-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="b94bf-136">Beantwoord de volgende vragen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-136">Answer the following questions:</span></span>

- <span data-ttu-id="b94bf-137">Is er sprake van queryduplicatie?</span><span class="sxs-lookup"><span data-stu-id="b94bf-137">Is there any query duplication?</span></span> <span data-ttu-id="b94bf-138">Als dat het geval is, overweeg dan een van de volgende oplossingen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="b94bf-139">[Gebruik caching](#use-caching) als u denkt dat er meerdere aanroepen in één bovenliggende record zijn.</span><span class="sxs-lookup"><span data-stu-id="b94bf-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="b94bf-140">[Gebruik een veld met parameters in de cache](#cached-parameterized) als u denkt dat er aanroepen voor dezelfde record binnen verschillende records zijn.</span><span class="sxs-lookup"><span data-stu-id="b94bf-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="b94bf-141">[Gebruik een **JOIN**-gegevensbron](#use-join-datasource) als u een groot aantal verschillende records in een database moet lezen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="b94bf-142">Komt het aantal query's en opgehaalde records overeen met de algehele hoeveelheid gegevens?</span><span class="sxs-lookup"><span data-stu-id="b94bf-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="b94bf-143">Als een document bijvoorbeeld 10 regels bevat, geven de statistieken dan aan dat het rapport 10 regels of 1000 regels extraheert?</span><span class="sxs-lookup"><span data-stu-id="b94bf-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="b94bf-144">Als u een groot aantal opgehaalde records hebt, overweeg dan een van de volgden oplossingen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="b94bf-145">[Gebruik de functie **FILTER** in plaats van de functie **WHERE**](#filter) om gegevens aan de SQL Server-zijde te verwerken.</span><span class="sxs-lookup"><span data-stu-id="b94bf-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="b94bf-146">Gebruik caching om te voorkomen dat dezelfde gegevens worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="b94bf-147">[Gebruik functies voor verzamelde gegevens](#collected-data) om te voorkomen dat dezelfde gegevens worden opgehaald voor een samenvatting.</span><span class="sxs-lookup"><span data-stu-id="b94bf-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="b94bf-148">PerfView-traces analyseren</span><span class="sxs-lookup"><span data-stu-id="b94bf-148">Analyze PerfView traces</span></span>

<span data-ttu-id="b94bf-149">[PerfView](#perfview)is een hulpmiddel voor ervaren ontwikkelaars.</span><span class="sxs-lookup"><span data-stu-id="b94bf-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="b94bf-150">Zie [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics) voor gedetailleerdere informatie over de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="b94bf-151">Verzamel een trace met behulp van threadtijd.</span><span class="sxs-lookup"><span data-stu-id="b94bf-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="b94bf-152">Neem alleen stapels op die gebruikmaken van **runUnattended** om alleen de thread te filteren die configuratie-uitvoering heeft.</span><span class="sxs-lookup"><span data-stu-id="b94bf-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="b94bf-153">(Voeg **runUnattended** aan het invoervak **IncPats** toe.)</span><span class="sxs-lookup"><span data-stu-id="b94bf-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="b94bf-154">Vouw CPU's, netwerk en geblokkeerde tijd samen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="b94bf-155">Laad [vooraf ingestelde ER-waarden voor PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="b94bf-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="b94bf-156">Selecteer **ER** \> **Overige vooraf ingestelde waarden**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="b94bf-157">Bekijk de namen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-157">Look at the names:</span></span>

    - <span data-ttu-id="b94bf-158">Waarschijnlijk ziet u de platformcode die de meeste tijd verbruikt.</span><span class="sxs-lookup"><span data-stu-id="b94bf-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="b94bf-159">U kunt dubbeltikken (of dubbelklikken) en omhoog gaan via **aangeroepen**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="b94bf-160">Als u klassen vindt met het voorvoegsel "ERExpression" en dit functies zijn die zijn gerelateerd aan formules, kunt u de functienaam raden op basis van de klassenaam, en kunt u de ER-opslagplaats bekijken om de kenmerken weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b94bf-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="b94bf-161">Oplossingen</span><span class="sxs-lookup"><span data-stu-id="b94bf-161">Fixes</span></span>

- <span data-ttu-id="b94bf-162">Als u ziet dat de meeste CPU-tijd wordt verbruikt door query's, moet u proberen het aantal query's te beperken:</span><span class="sxs-lookup"><span data-stu-id="b94bf-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="b94bf-163">[Controleer de ER-trace](#analyze-database-calls) op dubbele query's.</span><span class="sxs-lookup"><span data-stu-id="b94bf-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="b94bf-164">Bekijk hoeveel records worden opgehaald en evalueer hoeveel gegevens theoretische moeten worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="b94bf-165">Als u ziet dat de meeste CPU-tijd wordt verbruikt door de functies die worden gebruikt, moet u proberen de plaats te vinden in de configuratie die de meeste resources verbruikt.</span><span class="sxs-lookup"><span data-stu-id="b94bf-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="b94bf-166">Als u ziet dat de meeste CPU-tijd wordt verbruikt door functies voor gegevensverzameling, overweeg dan om deze te vervangen met *SQL-groep op* aan de modeltoewijzingszijde.</span><span class="sxs-lookup"><span data-stu-id="b94bf-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="b94bf-167">Gegevens verzamelen</span><span class="sxs-lookup"><span data-stu-id="b94bf-167">Collecting data</span></span>

<span data-ttu-id="b94bf-168">Afhankelijk van uw omgeving zijn er verschillende manieren om beschikbare gegevens te verzamelen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="b94bf-169">De totale uitvoeringstijd verkrijgen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-169">Get the total running time:</span></span>

    - <span data-ttu-id="b94bf-170">In het actiecentrum</span><span class="sxs-lookup"><span data-stu-id="b94bf-170">From the Action center</span></span>
    - <span data-ttu-id="b94bf-171">In het gebeurtenislogboek</span><span class="sxs-lookup"><span data-stu-id="b94bf-171">From the event log</span></span>

- <span data-ttu-id="b94bf-172">Profileer de uitvoering:</span><span class="sxs-lookup"><span data-stu-id="b94bf-172">Profile the execution:</span></span>

    - <span data-ttu-id="b94bf-173">Met behulp van ER-hulpmiddelen</span><span class="sxs-lookup"><span data-stu-id="b94bf-173">By using ER tools</span></span>
    - <span data-ttu-id="b94bf-174">Met behulp van Trace parser</span><span class="sxs-lookup"><span data-stu-id="b94bf-174">By using Trace parser</span></span>
    - <span data-ttu-id="b94bf-175">Met behulp van PerfView</span><span class="sxs-lookup"><span data-stu-id="b94bf-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="b94bf-176">Gegevens verzamelen in een productieomgeving</span><span class="sxs-lookup"><span data-stu-id="b94bf-176">Collecting data in a production environment</span></span>

<span data-ttu-id="b94bf-177">Soms kunnen problemen alleen in een productieomgeving worden gereproduceerd.</span><span class="sxs-lookup"><span data-stu-id="b94bf-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="b94bf-178">Gegevens kunnen op de volgende manieren worden verzameld:</span><span class="sxs-lookup"><span data-stu-id="b94bf-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="b94bf-179">Met behulp van [Trace parser](../perf-test/trace-trace-tutorial.md)-traces</span><span class="sxs-lookup"><span data-stu-id="b94bf-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="b94bf-180">Met behulp van traces van [ER-uitvoering](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="b94bf-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="b94bf-181">Met behulp van de totale uitvoeringstijd</span><span class="sxs-lookup"><span data-stu-id="b94bf-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="b94bf-182">Gegevens verzamelen in een ontwikkelomgeving</span><span class="sxs-lookup"><span data-stu-id="b94bf-182">Collecting data in a development environment</span></span>

<span data-ttu-id="b94bf-183">Naast de hulpmiddelen die kunnen worden gebruikt in een productieomgeving, zijn er verscheidene hulpmiddelen die u kunt gebruiken in een ontwikkelomgeving:</span><span class="sxs-lookup"><span data-stu-id="b94bf-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="b94bf-184">Gebeurtenislogboek (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="b94bf-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="b94bf-185">Dit logboek kan u de totale uitvoeringstijd verschaffen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="b94bf-186">Algemene .NET-hulpprogramma's, zoals PerfView.</span><span class="sxs-lookup"><span data-stu-id="b94bf-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="b94bf-187">Bovendien biedt een ontwikkelomgeving u meer flexibiliteit om te experimenteren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="b94bf-188">U kunt bijvoorbeeld delen van rapporten uitschakelen om te zien wat de invloed van de uitvoeringstijd is.</span><span class="sxs-lookup"><span data-stu-id="b94bf-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="b94bf-189">Hulpmiddelen</span><span class="sxs-lookup"><span data-stu-id="b94bf-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="b94bf-190">Uitvoeringstijd in het actiecentrum</span><span class="sxs-lookup"><span data-stu-id="b94bf-190">Execution time in the Action center</span></span>

<span data-ttu-id="b94bf-191">ER kan de uitvoeringstijd van de configuratie in het actiecentrum tonen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="b94bf-192">Deze optie werkt alleen voor een specifieke gebruiker en een specifiek bedrijf, en alleen voor interactieve sessies.</span><span class="sxs-lookup"><span data-stu-id="b94bf-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="b94bf-193">Voer de volgende stappen uit om deze functie beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="b94bf-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="b94bf-194">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b94bf-195">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="b94bf-196">In het dialoogvenster **Gebruikersparameters** stelt u de optie **Tijd voor genereren van bestanden weergeven** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="b94bf-197">Uitvoeringstijd in het gebeurtenislogboek</span><span class="sxs-lookup"><span data-stu-id="b94bf-197">Execution time in the event log</span></span>

1. <span data-ttu-id="b94bf-198">Open Windows Event Viewer.</span><span class="sxs-lookup"><span data-stu-id="b94bf-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="b94bf-199">Open onder **Logboeken Toepassingen en Services** **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="b94bf-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="b94bf-200">Zoek naar **FormatMapingRun**-gebeurtenissen waarin **EventID=2**, omdat deze gebeurtenissen de informatie over verstreken tijd bevatten.</span><span class="sxs-lookup"><span data-stu-id="b94bf-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="b94bf-201">Trace parser-traces</span><span class="sxs-lookup"><span data-stu-id="b94bf-201">Trace parser traces</span></span> 

<span data-ttu-id="b94bf-202">Omdat ER in X++ is geïmplementeerd, kunt u algemene X++-hulpprogramma's gebruiken om de prestaties te analyseren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="b94bf-203">Zie [Traceren met Trace parser](../perf-test/trace-trace-tutorial.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="b94bf-204">Deze benadering kent enkele beperkingen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="b94bf-205">Omdat een deel van ER is geïmplementeerd in C#, zijn niet alle details beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="b94bf-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="b94bf-206">U kunt de details van het gegevensgebruik echter bekijken.</span><span class="sxs-lookup"><span data-stu-id="b94bf-206">However, you can view the data usage details.</span></span> <span data-ttu-id="b94bf-207">Bovendien kunnen lange rapportuitvoeringen traceopslagbeperkingen overschrijden.</span><span class="sxs-lookup"><span data-stu-id="b94bf-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="b94bf-208">ER-traces</span><span class="sxs-lookup"><span data-stu-id="b94bf-208">ER traces</span></span>

<span data-ttu-id="b94bf-209">Met ER kunnen de eigen traces worden verzameld en ER bevat visualisatie- en analyseprogramma's voor deze traces.</span><span class="sxs-lookup"><span data-stu-id="b94bf-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="b94bf-210">Zie [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="b94bf-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="b94bf-211">PerfView</span></span>

<span data-ttu-id="b94bf-212">Omdat zowel X++ als ER zijn geïmplementeerd boven op het .NET-platform, kunt u algemene .NET-hulpprogramma's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b94bf-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="b94bf-213">U kunt bijvoorbeeld het gratis [PerfView](https://github.com/Microsoft/perfview)-programma gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b94bf-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="b94bf-214">U kunt ook gegevens via de opdrachtregel verzamelen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-214">You can also collect data from the command line.</span></span> <span data-ttu-id="b94bf-215">Met het volgende Windows PowerShell-script verzamelt u bijvoorbeeld de uitvoeringstijd totdat de uitvoering van de indeling op de computer wordt gestopt.</span><span class="sxs-lookup"><span data-stu-id="b94bf-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="b94bf-216">Deze benadering kent enkele beperkingen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="b94bf-217">U moet beheertoegang tot de computer hebben.</span><span class="sxs-lookup"><span data-stu-id="b94bf-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="b94bf-218">Bovendien moet u een ervaren ontwikkelaar zijn, omdat er een heel leerproces aan vast zit.</span><span class="sxs-lookup"><span data-stu-id="b94bf-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="b94bf-219">Wijzigingen aanbrengen</span><span class="sxs-lookup"><span data-stu-id="b94bf-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="b94bf-220">Caching gebruiken</span><span class="sxs-lookup"><span data-stu-id="b94bf-220">Use caching</span></span>

<span data-ttu-id="b94bf-221">Hoewel het met caching minder tijd kost om gegevens opnieuw op te halen, kost het geheugen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="b94bf-222">Gebruik caching in gevallen waarin de hoeveelheid opgehaalde gegevens niet erg groot is.</span><span class="sxs-lookup"><span data-stu-id="b94bf-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="b94bf-223">Zie [De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstrace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) voor meer informatie en een voorbeeld over het gebruik van caching.</span><span class="sxs-lookup"><span data-stu-id="b94bf-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="b94bf-224">Een berekend veld met parameters in de cache gebruiken</span><span class="sxs-lookup"><span data-stu-id="b94bf-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="b94bf-225">Waarden moeten soms herhaaldelijk worden opgezocht.</span><span class="sxs-lookup"><span data-stu-id="b94bf-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="b94bf-226">Voorbeelden zijn rekeningnamen en rekeningnummers.</span><span class="sxs-lookup"><span data-stu-id="b94bf-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="b94bf-227">Om tijd te besparen kunt u een berekend veld maken dat parameters op het bovenste niveau heeft, en het veld vervolgens aan de cache toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="b94bf-228">We raden u aan deze methode alleen te gebruiken als de grootte van de gegevens in de cache klein is.</span><span class="sxs-lookup"><span data-stu-id="b94bf-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="b94bf-229">Zie [De prestaties van ER-oplossingen verbeteren door gegevensbronnen voor een berekend veld met parameters toe te voegen](er-calculated-field-ds-performance.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="b94bf-230">Een JOIN-gegevensbron gebruiken</span><span class="sxs-lookup"><span data-stu-id="b94bf-230">Use a JOIN data source</span></span>

<span data-ttu-id="b94bf-231">Met een **JOIN**-gegevensbron kunnen verschillende verbonden records met één query worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="b94bf-232">Er hoeft geen afzonderlijke query te worden gebruikt om elke verbonden record op te halen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="b94bf-233">Als u bijvoorbeeld 1000 regels hebt en u haalt artikelgegevens op voor elke regel per relatie, hebt u 1001 query's (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="b94bf-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="b94bf-234">Als u een **JOIN**-gegevensbron gebruikt, gebruikt u slechts één query om dezelfde gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="b94bf-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="b94bf-235">Zie [JOIN-gegevensbronnen gebruiken in ER-modeltoewijzingen om gegevens uit meerdere toepassingstabellen op te halen](er-join-data-sources.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="b94bf-236">De functie FILTER gebruiken in plaats van de functie WHERE</span><span class="sxs-lookup"><span data-stu-id="b94bf-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="b94bf-237">Met de functie **[FILTER](er-functions-list-filter.md)** worden voorwaarden uitgevoerd in SQL Server, terwijl met de functie **WHERE** alle gegevens uit de lijst met één record per keer worden opgehaald en de voorwaarde voor elke record wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="b94bf-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="b94bf-238">U wilt bijvoorbeeld één record van 1000 records selecteren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="b94bf-239">Als u **WHERE** gebruikt, worden alle 1000 records opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="b94bf-240">Als u echter **FILTER** gebruikt, wordt precies één record opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="b94bf-241">Met **FILTER** kunnen ook indexen worden gebruikt voor de database.</span><span class="sxs-lookup"><span data-stu-id="b94bf-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="b94bf-242">Functies voor verzamelde gegevens of een samengevoegde gegevensbron gebruiken</span><span class="sxs-lookup"><span data-stu-id="b94bf-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="b94bf-243">Als uw configuratie het onderdeel *groeperen op* heeft waarmee eerder opgehaalde gegevens per rapport worden samengevat, worden alle gegevens opnieuw opgehaald met het onderdeel.</span><span class="sxs-lookup"><span data-stu-id="b94bf-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="b94bf-244">Met behulp van functies voor verzamelde gegevens stelt u ER in staat gegevens samen te voegen tijdens de eerste keer dat de gegevens worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="b94bf-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="b94bf-245">Zie [ER-indeling configureren voor tellen en totaliseren](tasks/er-format-counting-summing-2.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b94bf-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="b94bf-246">Delen van de configuratie in X++ herschrijven</span><span class="sxs-lookup"><span data-stu-id="b94bf-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="b94bf-247">ER ondersteunt aanroepmethoden van tabellen en klassen, waaronder extensies.</span><span class="sxs-lookup"><span data-stu-id="b94bf-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="b94bf-248">Overweeg delen van de modeltoewijzing in X++ beter te herschrijven om de prestaties te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="b94bf-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="b94bf-249">ER kan gegevens verbruiken uit de volgende bronnen:</span><span class="sxs-lookup"><span data-stu-id="b94bf-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="b94bf-250">Klassen (**object**- en **klasse**-gegevensbronnen)</span><span class="sxs-lookup"><span data-stu-id="b94bf-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="b94bf-251">Tabellen (**tabel**- en **tabelrecords**-gegevensbronnen)</span><span class="sxs-lookup"><span data-stu-id="b94bf-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="b94bf-252">De [ER-API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) biedt ook een manier om vooraf berekende gegevens van de aanroepcode te verzenden.</span><span class="sxs-lookup"><span data-stu-id="b94bf-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="b94bf-253">De toepassingssuite bevat vele voorbeelden van deze aanpak.</span><span class="sxs-lookup"><span data-stu-id="b94bf-253">The application suite contains numerous examples of this approach.</span></span>
