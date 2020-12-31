---
title: Regels maken voor Optimization advisor
description: In dit onderwerp wordt uitgelegd hoe u nieuwe regels toevoegt aan Optimization advisor.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7052aeb4154cefe30a1935dfdca53085a035deb6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687606"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="190f3-103">Regels maken voor Optimization advisor</span><span class="sxs-lookup"><span data-stu-id="190f3-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="190f3-104">In dit onderwerp wordt uitgelegd hoe u nieuwe regels maakt voor **Optimization advisor**.</span><span class="sxs-lookup"><span data-stu-id="190f3-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="190f3-105">U kunt bijvoorbeeld een nieuwe regel maken die aangeeft welke offerteaanvragen een lege titel hebben.</span><span class="sxs-lookup"><span data-stu-id="190f3-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="190f3-106">Met behulp van titels op aanvragen worden ze gemakkelijk herkenbaar en zoekbaar.</span><span class="sxs-lookup"><span data-stu-id="190f3-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="190f3-107">Dit voorbeeld is heel eenvoudig maar toont wat met regels voor optimalisatie kan worden bereikt.</span><span class="sxs-lookup"><span data-stu-id="190f3-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="190f3-108">Een *regel* is een controle van toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="190f3-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="190f3-109">Als aan de voorwaarde die door de regel wordt geëvalueerd, wordt voldaan, worden verkoopkansen gecreëerd om processen te optimaliseren of gegevens te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="190f3-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="190f3-110">De verkoopkansen kunnen worden gebruikt en optioneel kan het effect van de acties worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="190f3-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="190f3-111">Als u een nieuwe regel voor de **Optimization advisor** wilt maken, voegt u een nieuwe klasse toe die de abstracte klasse **SelfHealingRule** uitbreidt, de **IDiagnosticsRule**-interface implementeert en is voorzien van het kenmerk **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="190f3-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="190f3-112">De klasse moet ook beschikken over een methode die is voorzien van het kenmerk **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="190f3-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="190f3-113">Volgens afspraak wordt dat gedaan in de methode **opportunityTitle**, die later zal worden besproken.</span><span class="sxs-lookup"><span data-stu-id="190f3-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="190f3-114">Deze nieuwe klasse kan worden toegevoegd aan een aangepast model met een afhankelijkheid van het model **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="190f3-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="190f3-115">In het volgende voorbeeld wordt de regel die wordt geïmplementeerd, **RFQTitleSelfHealingRule** genoemd.</span><span class="sxs-lookup"><span data-stu-id="190f3-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="190f3-116">De abstracte klasse **SelfHealingRule** heeft abstracte methoden die moeten worden geïmplementeerd in overnemende klassen.</span><span class="sxs-lookup"><span data-stu-id="190f3-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="190f3-117">De kern is de methode **evaluate**, die resulteert in een lijst van de verkoopkansen geïdentificeerd door de regel.</span><span class="sxs-lookup"><span data-stu-id="190f3-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="190f3-118">Verkoopkansen kunnen per rechtspersoon zijn of kunnen gelden voor het gehele systeem.</span><span class="sxs-lookup"><span data-stu-id="190f3-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="190f3-119">De bovenstaande methode omvat bedrijven en selecteert offerteaanvraaggevallen met lege titels in de methode **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="190f3-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="190f3-120">Als ten minste één zo'n aanvraag wordt gevonden, wordt een bedrijfsspecifieke verkoopkans gemaakt met de methode **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="190f3-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="190f3-121">Merk op dat het veld **Gegevens** in de tabel **SelfHealingOpportunity** van het type **Container** is, en daarom gegevens kan bevatten die relevant zijn voor de logica die specifiek is voor deze regel.</span><span class="sxs-lookup"><span data-stu-id="190f3-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="190f3-122">Instellen van **OpportunityDate** met de huidige tijdstempel registreert het tijdstip van de laatste evaluatie van de verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="190f3-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="190f3-123">Verkoopkansen kunnen ook voor meerdere bedrijven zijn.</span><span class="sxs-lookup"><span data-stu-id="190f3-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="190f3-124">In dit geval is het omvatten van bedrijven niet nodig en moet de verkoopkans worden gemaakt met de methode **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="190f3-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="190f3-125">De volgende code toont de methode **findRFQCasesWithEmptyTitle**, die de id's van de offerteaanvraaggevallen retourneert die lege titels hebben.</span><span class="sxs-lookup"><span data-stu-id="190f3-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="190f3-126">Twee meer methoden die moeten worden geïmplementeerd zijn **opportunityTitle** en **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="190f3-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="190f3-127">De eerste geeft een korte titel voor de verkoopkans als resultaat. De laatste geeft een gedetailleerde omschrijving van de verkoopkans als resultaat, die ook gegevens kan bevatten.</span><span class="sxs-lookup"><span data-stu-id="190f3-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="190f3-128">De titel die wordt geretourneerd door **opportunityTitle** wordt weergegeven onder de kolom **Optimalisatie verkoopkans** in de werkruimte **Optimization advisor**.</span><span class="sxs-lookup"><span data-stu-id="190f3-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="190f3-129">Het verschijnt ook als de koptekst van het zijdeelvenster met meer informatie over de verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="190f3-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="190f3-130">Volgens conventie is deze methode voorzien van het kenmerk **DiagnosticRuleSubscription**, dat de volgende argumenten gebruikt:</span><span class="sxs-lookup"><span data-stu-id="190f3-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="190f3-131">**Diagnostisch gebied**: een opsomming van het type **DiagnosticArea** die beschrijft tot welk gebied van de toepassing de regel behoort, zoals **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="190f3-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="190f3-132">**Regelnaam**: een tekenreeks met de regelnaam.</span><span class="sxs-lookup"><span data-stu-id="190f3-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="190f3-133">Deze verschijnt onder de kolom **Regelnaam** op het formulier **Diagnosevalidatieregel** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="190f3-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="190f3-134">**Uitvoeringsfrequentie**: een opsomming van het type **DiagnosticRunFrequency** die beschrijft hoe vaak de regel moet worden uitgevoerd, bijvoorbeeld **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="190f3-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="190f3-135">**Regelbeschrijving**: een tekenreeks met een meer gedetailleerde omschrijving van de regel.</span><span class="sxs-lookup"><span data-stu-id="190f3-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="190f3-136">Deze verschijnt onder de kolom **Regelbeschrijving** op het formulier **Diagnosevalidatieregel** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="190f3-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="190f3-137">Het kenmerk **DiagnosticRuleSubscription** is vereist om de regel te laten werken.</span><span class="sxs-lookup"><span data-stu-id="190f3-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="190f3-138">Wordt meestal gebruikt op **opportunityTitle**, maar methoden van elke klasse kunnen ermee worden voorzien.</span><span class="sxs-lookup"><span data-stu-id="190f3-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="190f3-139">Hier volgt een voorbeeld van de implementatie.</span><span class="sxs-lookup"><span data-stu-id="190f3-139">The following is an example implementation.</span></span> <span data-ttu-id="190f3-140">Onbewerkte tekenreeksen worden gebruikt ter vereenvoudiging, maar een juiste implementatie vereist labels.</span><span class="sxs-lookup"><span data-stu-id="190f3-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="190f3-141">De omschrijving die wordt geretourneerd door **opportunityDetails**, wordt weergegeven in het zijvenster met meer informatie over de verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="190f3-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="190f3-142">Dit gebruikt het argument **SelfHealingOpportunity**, dat een **Gegevens**-veld is dat kan worden gebruikt voor meer informatie over de verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="190f3-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="190f3-143">In het voorbeeld retourneert de methode de id's van de offerteaanvraaggevallen met een lege titel.</span><span class="sxs-lookup"><span data-stu-id="190f3-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="190f3-144">De twee resterende te implementeren abstracte methoden zijn **provideHealingAction** en **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="190f3-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="190f3-145">**provideHealingAction** retourneert true als een herstelactie wordt verschaft, anders wordt het resultaat false.</span><span class="sxs-lookup"><span data-stu-id="190f3-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="190f3-146">Als true wordt geretourneerd, moet de methode **performAction** worden geïmplementeerd, anders wordt een fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="190f3-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="190f3-147">De methode **performAction** gebruikt een argument **SelfHealingOpportunity** waarin de gegevens kunnen worden gebruikt voor de actie.</span><span class="sxs-lookup"><span data-stu-id="190f3-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="190f3-148">In het voorbeeld opent de actie de **PurchRFQCaseTableListPage**, voor handmatige correctie.</span><span class="sxs-lookup"><span data-stu-id="190f3-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="190f3-149">Afhankelijk van de bijzonderheden van de regel, is het mogelijk een automatische actie te gebruiken met de verkoopkansgegevens.</span><span class="sxs-lookup"><span data-stu-id="190f3-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="190f3-150">In dit voorbeeld kan het systeem titels voor offerteaanvraaggevallen automatisch genereren.</span><span class="sxs-lookup"><span data-stu-id="190f3-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="190f3-151">**securityMenuItem** retourneert de naam van een actiemenuopdracht zodanig zijn dat de regel alleen zichtbaar is voor gebruikers die toegang hebben tot de actiemenuopdracht.</span><span class="sxs-lookup"><span data-stu-id="190f3-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="190f3-152">Beveiliging vereist mogelijk dat bepaalde regels en mogelijkheden alleen toegankelijk voor geautoriseerde gebruikers zijn.</span><span class="sxs-lookup"><span data-stu-id="190f3-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="190f3-153">In het voorbeeld kunnen alleen gebruikers met toegang tot **PurchRFQCaseTitleAction** de verkoopkans weergeven.</span><span class="sxs-lookup"><span data-stu-id="190f3-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="190f3-154">U ziet dat dit actiemenu-item voor dit voorbeeld is gemaakt en is toegevoegd als een invoerpunt voor de beveiligingsbevoegdheid **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="190f3-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="190f3-155">De menuopdracht moet een actiemenuopdracht zijn voor een correcte beveiliging.</span><span class="sxs-lookup"><span data-stu-id="190f3-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="190f3-156">Andere typen menuopdrachten, zoals **weergavemenuopdrachten**, werken niet goed.</span><span class="sxs-lookup"><span data-stu-id="190f3-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="190f3-157">Nadat de regel is gecompileerd, de volgende taak uitvoeren om het te laten weergeven in de gebruikersinterface (UI).</span><span class="sxs-lookup"><span data-stu-id="190f3-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="190f3-158">De regel wordt weergegeven in het formulier de **Diagnosevalidatieregel** dat beschikbaar is vanuit **Systeembeheer** > **Periodieke taken** > **Validatieregel van diagnose onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="190f3-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="190f3-159">Als u het wilt laten evalueren, gaat u naar **Systeembeheer** > **Periodieke taken** > **Validatieregel van diagnose plannen** en selecteert u de frequentie van de regel, zoals **Dagelijks**.</span><span class="sxs-lookup"><span data-stu-id="190f3-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="190f3-160">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="190f3-160">Click **OK**.</span></span> <span data-ttu-id="190f3-161">Ga naar **Systeembeheer** > **Optimization advisor** om de nieuwe verkoopkans weer te geven.</span><span class="sxs-lookup"><span data-stu-id="190f3-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="190f3-162">Het volgende voorbeeld is een codefragment met het geraamte van een regel, met inbegrip van alle vereiste methoden en kenmerken.</span><span class="sxs-lookup"><span data-stu-id="190f3-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="190f3-163">Hiermee kunt u aan de slag gaan met het schrijven van nieuwe regels.</span><span class="sxs-lookup"><span data-stu-id="190f3-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="190f3-164">De labels en actiemenuopdrachten in het voorbeeld worden alleen voor demonstratiedoeleinden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="190f3-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="190f3-165">Bekijk voor meer informatie de korte YouTube-video: [Optimalisatie-advies in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="190f3-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
