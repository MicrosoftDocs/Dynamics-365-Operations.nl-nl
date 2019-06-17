<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="nl-NL">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Uitvoering van ER-indeling traceren om prestatieproblemen op te lossen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Dit onderwerp bevat informatie over het gebruik van de functie voor prestatietracering in Elektronische rapportage (ER) om prestatieproblemen op te lossen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Als onderdeel van het proces van het ontwerpen van configuraties voor Elektronische rapportage om elektronische documenten te genereren, definieert u de methode die wordt gebruikt om gegevens uit Microsoft Dynamics 365 for Finance and Operations te halen en deze in te voeren in de gegenereerde uitvoer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Met de functie voor ER-prestatietracering kunt u aanzienlijk besparen op de tijd en kosten van het verzamelen van gegevens over de uitvoering van ER-indelingen zodat u deze kunt investeren in het oplossen van prestatieproblemen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In deze zelfstudie vindt u richtlijnen voor het traceren van prestaties voor uitgevoerde ER-indelingen in Finance and Operations. Daarnaast wordt aangegeven hoe u de informatie uit deze traceringen gebruikt om de prestaties te verbeteren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Vereisten</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Om de voorbeelden in deze zelfstudie te kunnen voltooien, moet u toegang tot het volgende hebben:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Toegang verkrijgen tot Finance and Operations voor een van de volgende rollen:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ontwikkelaar elektronische rapportage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Functioneel consultant elektronische rapportage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Systeembeheerder</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Toegang tot het exemplaar van Regulatory Configuration Services (RCS) dat is ingericht voor dezelfde tenant als Finance and Operations, voor een van de volgende rollen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ontwikkelaar elektronische rapportage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Functioneel consultant elektronische rapportage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Systeembeheerder</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">U moet ook de volgende bestanden downloaden en lokaal opslaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bestand</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Inhoud</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Versie 1 prestatietraceringsmodel</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Voorbeeldconfiguratie van model voor ER-gegevens<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Versie 1 metagegevens voor prestatietracering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Voorbeeldconfiguratie van ER-metagegevens<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Versie 1.1 Toewijzing voor prestatietracering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Voorbeeldconfiguratie van ER-modeltoewijzing<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Versie 1.1 Indeling voor prestatietracering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Voorbeeldconfiguratie van ER-indeling<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ER-parameters configureren</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Elke ER-prestatietracering die wordt gegenereerd in Finance and Operations, wordt opgeslagen als een bijlage van de uitvoeringslogboekrecord.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het raamwerk voor documentbeheer van Finance and Operations wordt gebruikt om deze bijlagen te beheren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">U moet ER-parameters vooraf configureren om het documenttype voor documentbeheer op te geven dat moet worden gebruikt voor het bijvoegen van prestatietraceringen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In Finance and Operations selecteert u in de werkruimte <bpt id="p1">**</bpt>Elektronische rapportage<ept id="p1">**</ept> de optie <bpt id="p2">**</bpt>Parameters van elektronische rapportage<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer vervolgens op de pagina <bpt id="p1">**</bpt>Parameters van elektronische rapportage<ept id="p1">**</ept> op het tabblad <bpt id="p2">**</bpt>Bijlagen<ept id="p2">**</ept> in het veld <bpt id="p3">**</bpt>Andere<ept id="p3">**</ept> het documenttype voor documentbeheer dat voor prestatietraceringen moet worden gebruikt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Parameters van elektronische rapportage in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Om beschikbaar te zijn in het opzoekveld <bpt id="p1">**</bpt>Andere<ept id="p1">**</ept> moet een documenttype voor documentbeheer op de volgende manier worden geconfigureerd op de pagina <bpt id="p2">**</bpt>Documenttypen<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Documentbeheer <ph id="ph2">\&gt;</ph> Documenttypen<ept id="p3">**</ept>):</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Klasse:<ept id="p1">**</ept> Bestand koppelen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Groep:<ept id="p1">**</ept> Bestand</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Documenttypen in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het geselecteerde documenttype moet beschikbaar zijn in elk bedrijf van het huidige Finance and Operations-exemplaar omdat bijlagen voor documentbeheer bedrijfsspecifiek zijn.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">RCS-parameters configureren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ER-prestatietraceringen die zijn gegenereerd in Finance and Operations, worden geïmporteerd in RCS voor analyse met behulp van de ER-indelingsontwerper en de ER-toewijzingsontwerper.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Omdat ER-prestatietraceringen worden opgeslagen als bijlagen van de uitvoeringslogboekrecord die is gerelateerd aan de ER-indeling, moet u RCS-parameters vooraf configureren om het documenttype voor documentbeheer op te geven dat moet worden gebruikt voor het koppelen van prestatietraceringen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In het exemplaar van RCS dat is ingericht voor uw bedrijf selecteert u in de werkruimte <bpt id="p1">**</bpt>Elektronische rapportage<ept id="p1">**</ept> de optie <bpt id="p2">**</bpt>Parameters van elektronische rapportage<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Selecteer vervolgens op de pagina <bpt id="p1">**</bpt>Parameters van elektronische rapportage<ept id="p1">**</ept> op het tabblad <bpt id="p2">**</bpt>Bijlagen<ept id="p2">**</ept> in het veld <bpt id="p3">**</bpt>Andere<ept id="p3">**</ept> het documenttype voor documentbeheer dat voor prestatietraceringen moet worden gebruikt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Parameters van elektronische rapportage in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Om beschikbaar te zijn in het opzoekveld <bpt id="p1">**</bpt>Andere<ept id="p1">**</ept> moet een documenttype voor documentbeheer op de volgende manier worden geconfigureerd op de pagina <bpt id="p2">**</bpt>Documenttypen<ept id="p2">**</ept> (<bpt id="p3">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Documentbeheer <ph id="ph2">\&gt;</ph> Documenttypen<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Klasse:<ept id="p1">**</ept> Bestand koppelen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Groep:<ept id="p1">**</ept> Bestand</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Een ER-oplossing ontwerpen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Stel dat u bent begonnen met het ontwerpen van een nieuwe ER-oplossing om een nieuw rapport te genereren waarin leverancierstransacties worden gepresenteerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Op dit moment kunt u de transacties voor een geselecteerde leverancier vinden op de pagina <bpt id="p1">**</bpt>Leveranciertransacties<ept id="p1">**</ept> (ga naar <bpt id="p2">**</bpt>Leveranciers <ph id="ph1">\&gt;</ph> Leveranciers <ph id="ph2">\&gt;</ph> Alle leveranciers<ept id="p2">**</ept>, selecteer een leverancier en selecteer in het actievenster op het tabblad <bpt id="p3">**</bpt>Leverancier<ept id="p3">**</ept> in de groep <bpt id="p4">**</bpt>Transacties<ept id="p4">**</ept> de optie <bpt id="p5">**</bpt>Transacties<ept id="p5">**</ept>).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">U wilt echter alle leverancierstransacties tegelijk in één elektronisch document in XML-indeling hebben.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Deze oplossing bestaat uit verschillende ER-configuraties met het vereiste gegevensmodel en de vereiste metagegevens, modeltoewijzing en indelingscomponenten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Meld u aan bij het exemplaar van RCS dat is ingericht voor uw bedrijf.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In deze zelfstudie maakt en wijzigt u configuraties voor het voorbeeldbedrijf <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Zorg er daarom voor dat deze configuratieprovider is toegevoegd aan RCS en als actief is geselecteerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Zie de procedure <bpt id="p1">[</bpt>Aanbieders van configuraties maken en deze als actief markeren<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> voor instructies.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer in het werkgebied <bpt id="p1">**</bpt>Elektronische rapportage<ept id="p1">**</ept> de tegel <bpt id="p2">**</bpt>Rapportconfiguraties<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Importeer op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> de ER-configuraties die u als vereiste hebt gedownload in RCS, in de volgende volgorde: gegevensmodel, metagegevens, modeltoewijzing, indeling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Volg deze stappen voor elke configuratie:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In het actievenster selecteert u <bpt id="p1">**</bpt>Uitwisselen <ph id="ph1">\&gt;</ph> Laden uit XML-bestand<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Bladeren<ept id="p1">**</ept> om het juiste bestand voor de vereiste ER-configuratie in XML-indeling te selecteren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Configuraties in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De ER-oplossing uitvoeren om de uitvoering te traceren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Stel dat u klaar bent met het ontwerpen van de eerste versie van de ER-oplossing.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">U wilt deze nu testen in uw Finance and Operations-exemplaar en de uitvoeringsprestaties analyseren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Een ER-configuratie uit RCS importeren in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Meld u aan bij uw Finance en Operations-exemplaar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voor deze zelfstudie importeert u configuraties vanuit uw RCS-exemplaar (waarin u de ER-onderdelen ontwerpt) in uw exemplaar van Finance and Operations (waar u ze test en uiteindelijk gebruikt).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Daarom moet u ervoor zorgen dat alle vereiste artefacten zijn voorbereid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Zie voor meer instructies de procedure <bpt id="p1">[</bpt>Configuraties voor Elektronische rapportage (ER) importeren uit Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer de volgende stappen uit om de configuraties uit RCS in Finance and Operations te importeren:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in het werkgebied <bpt id="p1">**</bpt>Elektronische rapportage<ept id="p1">**</ept> op de tegel voor de configuratieprovider <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> de optie <bpt id="p3">**</bpt>Opslagplaatsen<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in het raster op de pagina <bpt id="p1">**</bpt>Opslagplaats van configuraties<ept id="p1">**</ept> de opslagplaats van het type <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> en selecteer vervolgens <bpt id="p3">**</bpt>Openen<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op het sneltabblad <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> de configuratie <bpt id="p2">**</bpt>Indeling voor prestatietracering<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op het sneltabblad <bpt id="p1">**</bpt>Versies<ept id="p1">**</ept> versie <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> van de geselecteerde configuratie en selecteer vervolgens <bpt id="p3">**</bpt>Importeren<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Opslagplaats van configuraties in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De bijbehorende versies van de gegevensmodel- en modeltoewijzingsconfiguraties worden automatisch geïmporteerd als vereisten voor de geïmporteerde ER-indelingsconfiguratie.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De ER-prestatietracering inschakelen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ga in Finance and Operations naar <bpt id="p1">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Elektronische rapportage <ph id="ph2">\&gt;</ph> Configuraties<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> in het actievenster op het tabblad <bpt id="p2">**</bpt>Configuraties<ept id="p2">**</ept> in de groep <bpt id="p3">**</bpt>Geavanceerde instellingen<ept id="p3">**</ept> de optie <bpt id="p4">**</bpt>Gebruikersparameters<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer de volgende stappen uit in de sectie <bpt id="p1">**</bpt>Uitvoeringstracering<ept id="p1">**</ept> van het dialoogvenster <bpt id="p2">**</bpt>Gebruikersparameters<ept id="p2">**</ept>:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in het veld <bpt id="p1">**</bpt>Opmaak van uitvoeringstracering<ept id="p1">**</ept> de optie <bpt id="p2">**</bpt>Fouten oplossen met traceringsopmaak<ept id="p2">**</ept> om te beginnen met het verzamelen van de details van de uitvoering van de ER-indeling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Wanneer deze waarde wordt geselecteerd, wordt met de prestatietracering informatie verzameld over de tijd die wordt besteed aan de volgende acties:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het uitvoeren van elke gegevensbron in de modeltoewijzing die wordt aangeroepen om gegevens op te halen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het verwerken van elk indelingsitem om gegevens in te voeren in de gegenereerde uitvoer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">U gebruikt het veld <bpt id="p1">**</bpt>Opmaak van uitvoeringstracering<ept id="p1">**</ept> om de indeling op te geven van de gegenereerde prestatietracering waarin de uitvoeringsdetails worden opgeslagen voor de ER-indelingselementen en ER-toewijzingselementen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Door <bpt id="p1">**</bpt>Fouten oplossen met traceringsopmaak<ept id="p1">**</ept> als waarde te selecteren, kunt u de inhoud van de tracering analyseren in de ER Operations-ontwerper en de ER-indelingselementen of ER-toewijzingselementen weergeven die worden genoemd in de tracering.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Stel de volgende opties in op <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> om specifieke details te verzamelen over de uitvoering van de ER-modeltoewijzing en ER-indelingsonderdelen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Statistieken voor query's verzamelen<ept id="p1">**</ept>: wanneer deze optie is ingeschakeld, wordt met de prestatietracering de volgende informatie verzameld:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het aantal databaseaanroepen door gegevensbronnen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het aantal dubbele aanroepen naar de database</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Details van de SQL-instructies die zijn gebruikt voor databaseaanroepen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Toegang tot caching traceren<ept id="p1">**</ept>: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het cachegebruik van de ER-modeltoewijzing.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Gegevenstoegang traceren<ept id="p1">**</ept>: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het aantal aanroepen naar de database voor uitgevoerde gegevensbronnen van het recordlijsttype.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Opsomming traceringslijst<ept id="p1">**</ept>: wanneer deze optie is ingeschakeld, wordt bij de prestatietracering informatie verzameld over het aantal records dat is aangevraagd vanuit gegevensbronnen van het recordlijsttype.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De parameters in het dialoogvenster <bpt id="p1">**</bpt>Gebruikersparameters<ept id="p1">**</ept> zijn specifiek voor de gebruiker en het huidige bedrijf.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het dialoogvenster Gebruikersparameters in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>De ER-indeling uitvoeren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer het bedrijf <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> in Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ga naar <bpt id="p1">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Elektronische rapportage <ph id="ph2">\&gt;</ph> Configuraties<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> in de configuratiestructuur het item <bpt id="p2">**</bpt>Indeling voor prestatietracering<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Uitvoeren<ept id="p1">**</ept> in het actievenster.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het bestand dat wordt gegenereerd, bevat informatie over 265 transacties voor zes leveranciers.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De uitvoeringstracering controleren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>De gegenereerde tracering exporteren vanuit Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Prestatietraceringen worden losgekoppeld van de ER-bronindeling en kunnen worden geserialiseerd naar een extern zipbestand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ga in Finance and Operations naar <bpt id="p1">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Elektronische rapportage <ph id="ph2">\&gt;</ph> Foutopsporingslogboeken voor configuraties<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op de pagina <bpt id="p1">**</bpt>Uitvoeringslogboeken voor elektronische rapportage<ept id="p1">**</ept> in het linkerdeelvenster in het veld <bpt id="p2">**</bpt>Configuratienaam<ept id="p2">**</ept> de optie <bpt id="p3">**</bpt>Indeling voor prestatietracering<ept id="p3">**</ept> om de logboekrecords te vinden die zijn gegenereerd door de uitvoering van de configuratie <bpt id="p4">**</bpt>Indeling voor prestatietracering<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer de knop <bpt id="p1">**</bpt>Bijlagen<ept id="p1">**</ept> (de paperclip) in de rechterbovenhoek van de pagina of druk op <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Knop Bijlagen op de pagina Uitvoeringslogboeken voor elektronische rapportage in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Op de pagina <bpt id="p1">**</bpt>Bijlagen voor uitvoeringslogboeken voor elektronische rapportage<ept id="p1">**</ept> selecteert u in het actievenster de optie <bpt id="p2">**</bpt>Openen<ept id="p2">**</ept> om de prestatietracering als een zipbestand te ontvangen en lokaal op te slaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Pagina Bijlagen voor uitvoeringslogboeken voor elektronische rapportage in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De tracering die wordt gegenereerd, bevat een verwijzing naar het ER-bronrapport via een unieke rapport-id in de <bpt id="p1">**</bpt>GUID-indeling<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Er wordt geen rekening gehouden met de versienummers van de indeling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De koppeling tussen de prestatietracering die is gegenereerd voor de uitgevoerde ER-indeling en de ER-modeltoewijzing is gebaseerd op de gebruikte basisdescriptor en het gemeenschappelijke gegevensmodel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Er wordt geen rekening gehouden met de versienummers van de indelings- en modeltoewijzing.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ook de instelling van de markering <bpt id="p1">**</bpt>Standaard voor modeltoewijzing<ept id="p1">**</ept> voor de modeltoewijzing wordt niet in overweging genomen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>De gegenereerde tracering in RCS importeren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in RCS in het werkgebied <bpt id="p1">**</bpt>Elektronische rapportage<ept id="p1">**</ept> de tegel <bpt id="p2">**</bpt>Rapportconfiguraties<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vouw op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> in de configuratiestructuur het item <bpt id="p2">**</bpt>Prestatietraceringsmodel<ept id="p2">**</ept> uit en selecteer het item <bpt id="p3">**</bpt>Indeling voor prestatietracering<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Ontwerper<ept id="p1">**</ept> in het actievenster.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer op de pagina <bpt id="p1">**</bpt>Indelingsontwerper<ept id="p1">**</ept> in het actievenster de optie <bpt id="p2">**</bpt>Prestatietracering<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in het dialoogvenster <bpt id="p1">**</bpt>Instellingen voor resultaat van prestatietracering<ept id="p1">**</ept> de optie <bpt id="p2">**</bpt>Prestatietracering importeren<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Bladeren<ept id="p1">**</ept> om het zipbestand te selecteren dat u eerder hebt geëxporteerd uit Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Dialoogvenster Instellingen voor resultaat van prestatietracering in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De prestatietracering gebruiken voor analyse in RCS – Uitvoering van indeling</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Selecteer in RCS op de pagina <bpt id="p1">**</bpt>Indelingsontwerper<ept id="p1">**</ept> de optie <bpt id="p2">**</bpt>Uitvouwen/samenvouwen<ept id="p2">**</ept> om de inhoud van alle indelingsitems uit te vouwen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">U ziet dat voor sommige items van de huidige indeling aanvullende informatie wordt weergegeven:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De werkelijke tijd die is besteed aan het invoeren van gegevens in de gegenereerde uitvoer met behulp van het indelingsitem</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het genereren van de gehele uitvoer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Pagina Indelingsontwerper in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Sluit de pagina <bpt id="p1">**</bpt>Indelingsontwerper<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Selecteer in RCS op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> in de configuratiestructuur het item <bpt id="p2">**</bpt>Toewijzing voor prestatietracering<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Selecteer <bpt id="p1">**</bpt>Ontwerper<ept id="p1">**</ept> in het actievenster.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Ontwerper<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Selecteer op de pagina <bpt id="p1">**</bpt>Ontwerper modeltoewijzing<ept id="p1">**</ept> in het actievenster de optie <bpt id="p2">**</bpt>Prestatietracering<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Selecteer de tracering die u eerder hebt geïmporteerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">U ziet dat nieuwe informatie beschikbaar wordt voor bepaalde gegevensbronitems van de huidige modeltoewijzing:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De werkelijke tijd die is besteed aan het ophalen van gegevens met behulp van de gegevensbron</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het uitvoeren van de gehele modeltoewijzing</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Er verschijnt een bericht met de mededeling dat de huidige modeltoewijzing databaseaanvragen dupliceert terwijl de gegevensbron VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum wordt uitgevoerd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Deze duplicatiefout doet zich voor omdat de lijst met leveranciertransacties twee keer wordt aangeroepen voor elke herhaalde leveranciersrecord:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Eén aanroep wordt uitgevoerd om details in te voeren van elke transactie in het gegevensmodel, op basis van de geconfigureerde bindingen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Eén oproep wordt uitgevoerd om het berekende aantal transacties per leverancier in het gegevensmodel in te voeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Bericht over dubbele databaseaanvragen op de pagina Ontwerper modeltoewijzing in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De waarde <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> geeft aan dat de VendTrans-tabel 530 keer is aangeroepen om een record uit die tabel te retourneren naar de gegevensbron VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De waarde <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> geeft aan dat de gegevensbron VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum 530 keer is aangeroepen om een record uit die gegevensbron te retourneren en de details op te geven in het gegevensmodel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">We raden u aan cache te gebruiken voor de gegevensbron VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum om het aantal aanroepen te beperken en de details van 265 transacties te verkrijgen en de prestaties van de modeltoewijzing te verbeteren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het kan ook handig zijn om het aantal aanroepen naar de gegevensbron LedgerTransTypeList te beperken.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Deze gegevensbron wordt gebruikt om elke waarde van de opsomming <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> te koppelen aan het label.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Door deze gegevensbron te gebruiken, kunt u een geschikt label zoeken en in het gegevensmodel invoeren voor elke leverancierstransactie.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Het huidige aantal aanroepen naar deze gegevensbron (9.027) is zeer hoog voor 265 transacties.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De pagina Ontwerper modeltoewijzing in RCS met 9027 aanroepen naar de gegevensbron</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstracering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">De logica van de modeltoewijzing wijzigen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer deze stappen uit om caching te gebruiken om dubbele aanroepen naar de database te voorkomen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">In RCS selecteert u op de pagina <bpt id="p1">**</bpt>Ontwerper modeltoewijzing<ept id="p1">**</ept> in het deelvenster <bpt id="p2">**</bpt>Gegevensbronnen<ept id="p2">**</ept> het item <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vouw het item <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> uit, vouw de lijst met één-op-veel-relaties uit voor de gegevensbron VendTable(het item <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relaties<ept id="p2">**</ept>) en selecteer het item <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Cache-instellingen om dubbele aanroepen te voorkomen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer de volgende stappen uit om de gegevensbron LedgerTransTypeList in het bereik van de gegevensbron VendTable te brengen:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vouw in het deelvenster <bpt id="p1">**</bpt>Typen gegevensbronnen<ept id="p1">**</ept> het item <bpt id="p2">**</bpt>Functies<ept id="p2">**</ept> uit en selecteer het item <bpt id="p3">**</bpt>Berekend veld<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer in het deelvenster <bpt id="p1">**</bpt>Gegevensbronnen<ept id="p1">**</ept> het item <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Toevoegen<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer in het veld <bpt id="p1">**</bpt>Naam<ept id="p1">**</ept> de tekst <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept> in.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Formule bewerken<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Typ in het veld <bpt id="p1">**</bpt>Formule<ept id="p1">**</ept> de tekst <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Opslaan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sluit de pagina <bpt id="p1">**</bpt>Formule-editor<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Klik op <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voer de volgende stappen uit om de caching van het veld <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> uit te voeren:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer het item <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer het item <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Selecteer <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Cache-instellingen voor het veld $TransType</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Voer de volgende stappen uit om het veld <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> zo te wijzigen dat het veld <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> in cache wordt gebruikt:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="0" state="translated">Vouw in het deelvenster <bpt id="p1">**</bpt>Gegevensbronnen<ept id="p1">**</ept> de items <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>, <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> en <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> uit en selecteer vervolgens het item <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Bewerken<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Selecteer <bpt id="p1">**</bpt>Formule bewerken<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Zoek in het veld <bpt id="p1">**</bpt>Formule<ept id="p1">**</ept> de volgende expressie:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Voer in het veld <bpt id="p1">**</bpt>Formule<ept id="p1">**</ept> de volgende expressie in:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Opslaan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Sluit de pagina <bpt id="p1">**</bpt>Formule-editor<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Selecteer <bpt id="p1">**</bpt>Opslaan<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Sluit de pagina <bpt id="p1">**</bpt>Ontwerper modeltoewijzing<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Sluit de pagina <bpt id="p1">**</bpt>Modeltoewijzingen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De gewijzigde versie van de ER-modeltoewijzing voltooien</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In RCS selecteert u op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> op het sneltabblad <bpt id="p2">**</bpt>Versies<ept id="p2">**</ept> versie <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> van de configuratie <bpt id="p4">**</bpt>Toewijzing voor prestatietracering<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Selecteer <bpt id="p1">**</bpt>Status wijzigen<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Selecteer <bpt id="p1">**</bpt>Voltooien<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De gewijzigde configuratie voor ER-modeltoewijzing vanuit RCS in Finance and Operations importeren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>Een ER-configuratie uit RCS importeren in Finance and Operations<ept id="p1">](#import-configuration)</ept> eerder in dit onderwerp om versie 1.2 van de configuratie <bpt id="p2">**</bpt>Toewijzing voor prestatietracering<ept id="p2">**</ept> te importeren in Finance and Operations.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">De gewijzigde ER-oplossing uitvoeren om de uitvoering te traceren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">De ER-indeling uitvoeren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>De ER-indeling uitvoeren<ept id="p1">](#run-format)</ept> eerder in dit onderwerp om een nieuwe prestatietracering te genereren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">De uitvoeringstracering controleren</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">De gegenereerde tracering exporteren vanuit Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>De gegenereerde tracering exporteren vanuit Finance and Operations<ept id="p1">](#export-trace)</ept> eerder in dit onderwerp om een nieuwe prestatietracering lokaal op te slaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">De gegenereerde tracering in RCS importeren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>De gegenereerde tracering in RCS importeren<ept id="p1">](#import-trace)</ept> eerder in dit onderwerp om de nieuwe prestatietracering in RCS te importeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>De prestatietracering gebruiken voor analyse in RCS – Modeltoewijzing<ept id="p1">](#use-trace)</ept> eerder in dit onderwerp om de meest recente prestatietracering te analyseren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Door uw aanpassingen in de modeltoewijzing worden er geen dubbele query's meer uitgevoerd in de database.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Het aantal aanroepen naar databasetabellen en gegevensbronnen voor deze modeltoewijzing is ook beperkt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hierdoor zijn de prestaties van de hele ER-oplossing verbeterd.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="0" state="translated">Traceringsgegevens voor de gegevensbron VendTable op de pagina Ontwerper modeltoewijzing in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">In de traceringsgegevens geeft de waarde <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> voor de gegevensbron VendTable aan dat deze gegevensbron 12 maal is aangeroepen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De waarde <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> geeft aan dat er zes aanroepen zijn omgezet in databaseaanroepen naar de tabel VendTable.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De waarde <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> geeft aan dat de records die uit de database zijn opgehaald in de cache zijn opgeslagen en zes andere aanroepen zijn verwerkt met behulp van de cache.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Het aantal aanroepen naar de gegevensbron LedgerTransTypeList is van 9027 verlaagd naar 240.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Traceringsgegevens voor de gegevensbron LedgerTransTypeList op de pagina Ontwerper modeltoewijzing in RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="0" state="translated">De uitvoeringstracering controleren in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Naast RCS bieden sommige versies van Finance and Operations mogelijk functies voor het ontwerpen van een ER-raamwerk.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Deze versies van Finance and Operations bevatten een optie <bpt id="p1">**</bpt>Ontwerpmodus inschakelen<ept id="p1">**</ept> die kan worden ingeschakeld.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Deze optie is te vinden op het tabblad <bpt id="p1">**</bpt>Algemeen<ept id="p1">**</ept> van de pagina <bpt id="p2">**</bpt>Parameters van elektronische rapportage<ept id="p2">**</ept>, die u kunt openen vanuit het werkgebied <bpt id="p3">**</bpt>Elektronische rapportage<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De optie Ontwerpmodus inschakelen op de pagina Parameters van elektronische rapportage in Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Als u een van deze versies van Finance and Operations gebruikt, kunt u de details van gegenereerde prestatietraceringen direct in Finance and Operations analyseren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">U hoeft deze niet vanuit Finance and Operations te exporteren en in RCS te importeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De uitvoeringstracering via externe hulpprogramma's controleren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Gebruikersparameters configureren</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ga in Finance and Operations naar <bpt id="p1">**</bpt>Organisatiebeheer <ph id="ph1">\&gt;</ph> Elektronische rapportage <ph id="ph2">\&gt;</ph> Configuraties<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Selecteer op de pagina <bpt id="p1">**</bpt>Configuraties<ept id="p1">**</ept> in het actievenster op het tabblad <bpt id="p2">**</bpt>Configuraties<ept id="p2">**</ept> in de groep <bpt id="p3">**</bpt>Geavanceerde instellingen<ept id="p3">**</ept> de optie <bpt id="p4">**</bpt>Gebruikersparameters<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Selecteer in het dialoogvenster <bpt id="p1">**</bpt>Gebruikersparameters<ept id="p1">**</ept> in de sectie <bpt id="p2">**</bpt>Uitvoeringstracering<ept id="p2">**</ept> in het veld <bpt id="p3">**</bpt>Opmaak van uitvoeringstracering<ept id="p3">**</ept> de optie <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">De ER-indeling uitvoeren</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Herhaal de stappen uit het gedeelte <bpt id="p1">[</bpt>De ER-indeling uitvoeren<ept id="p1">](#run-format)</ept> eerder in dit onderwerp om een nieuwe prestatietracering te genereren.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">U ziet dat de webbrowser een zipbestand voor downloaden biedt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dit bestand bevat de prestatietracering in PerfView-indeling.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vervolgens kunt u het PerfView-hulpprogramma voor prestatieanalyse gebruiken om de details van de ER-indelingsuitvoering te analyseren.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>