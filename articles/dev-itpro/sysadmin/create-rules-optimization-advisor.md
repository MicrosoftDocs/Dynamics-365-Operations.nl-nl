---
title: Regels maken voor Optimization advisor
description: In dit onderwerp wordt uitgelegd hoe u nieuwe regels toevoegt aan Optimization advisor.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: a18fac31b5acb7d2a1ec40203122d4eb9d94a439
ms.contentlocale: nl-nl
ms.lasthandoff: 05/23/2018

---

# <a name="create-rules-for-optimization-advisor"></a>Regels maken voor Optimization advisor

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u nieuwe regels maakt voor **Optimization advisor**. U kunt bijvoorbeeld een nieuwe regel maken die aangeeft welke offerteaanvragen een lege titel hebben. Met behulp van titels op aanvragen worden ze gemakkelijk herkenbaar en zoekbaar. Dit voorbeeld is heel eenvoudig maar toont wat met regels voor optimalisatie kan worden bereikt. 

Een *regel* is een controle van toepassingsgegevens. Als aan de voorwaarde die door de regel wordt geëvalueerd, wordt voldaan, worden verkoopkansen gecreëerd om processen te optimaliseren of gegevens te verbeteren. De verkoopkansen kunnen worden gebruikt en optioneel kan het effect van de acties worden gemeten. 

Als u een nieuwe regel voor de **Optimization advisor** wilt maken, voegt u een nieuwe klasse toe die de abstracte klasse **SelfHealingRule** uitbreidt, de **IDiagnosticsRule**-interface implementeert en is voorzien van het kenmerk **DiagnosticRule**. De klasse moet ook beschikken over een methode die is voorzien van het kenmerk **DiagnosticsRuleSubscription**. Volgens afspraak wordt dat gedaan in de methode **opportunityTitle**, die later zal worden besproken. Deze nieuwe klasse kan worden toegevoegd aan een aangepast model met een afhankelijkheid van het model **SelfHealingRules**. In het volgende voorbeeld wordt de regel die wordt geïmplementeerd, **RFQTitleSelfHealingRule** genoemd.

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

De abstracte klasse **SelfHealingRule** heeft abstracte methoden die moeten worden geïmplementeerd in overnemende klassen. De kern is de methode **evaluate**, die resulteert in een lijst van de verkoopkansen geïdentificeerd door de regel. Verkoopkansen kunnen per rechtspersoon zijn of kunnen gelden voor het gehele systeem.

```
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

De bovenstaande methode omvat bedrijven en selecteert offerteaanvraaggevallen met lege titels in de methode **findRFQCasesWithEmptyTitle**. Als ten minste één zo'n aanvraag wordt gevonden, wordt een bedrijfsspecifieke verkoopkans gemaakt met de methode **getOpportunityForCompany**. Merk op dat het veld **Gegevens** in de tabel **SelfHealingOpportunity** van het type **Container** is, en daarom gegevens kan bevatten die relevant zijn voor de logica die specifiek is voor deze regel. Instellen van **OpportunityDate** met de huidige tijdstempel registreert het tijdstip van de laatste evaluatie van de verkoopkans.  

Verkoopkansen kunnen ook voor meerdere bedrijven zijn. In dit geval is het omvatten van bedrijven niet nodig en moet de verkoopkans worden gemaakt met de methode **getOpportunityAcrossCompanies**. 

De volgende code toont de methode **findRFQCasesWithEmptyTitle**, die de id's van de offerteaanvraaggevallen retourneert die lege titels hebben.

```
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

Twee meer methoden die moeten worden geïmplementeerd zijn **opportunityTitle** en **opportunityDetails**. De eerste geeft een korte titel voor de verkoopkans als resultaat. De laatste geeft een gedetailleerde omschrijving van de verkoopkans als resultaat, die ook gegevens kan bevatten.

De titel die wordt geretourneerd door **opportunityTitle** wordt weergegeven onder de kolom **Optimalisatie verkoopkans** in de werkruimte **Optimization advisor**. Het verschijnt ook als de koptekst van het zijdeelvenster met meer informatie over de verkoopkans. Volgens conventie is deze methode voorzien van het kenmerk **DiagnosticRuleSubscription**, dat de volgende argumenten gebruikt: 

* **Diagnostisch gebied**: een opsomming van het type **DiagnosticArea** die beschrijft tot welk gebied van de toepassing de regel behoort, zoals **DiagnosticArea::SCM**. 

* **Regelnaam**: een tekenreeks met de regelnaam. Deze verschijnt onder de kolom **Regelnaam** op het formulier **Diagnosevalidatieregel** (**DiagnosticsValidationRuleMaintain**). 

* **Uitvoeringsfrequentie**: een opsomming van het type **DiagnosticRunFrequency** die beschrijft hoe vaak de regel moet worden uitgevoerd, bijvoorbeeld **DiagnosticRunFrequency::Daily**. 

* **Regelbeschrijving**: een tekenreeks met een meer gedetailleerde omschrijving van de regel. Deze verschijnt onder de kolom **Regelbeschrijving** op het formulier **Diagnosevalidatieregel** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Het kenmerk **DiagnosticRuleSubscription** is vereist om de regel te laten werken. Wordt meestal gebruikt op **opportunityTitle**, maar methoden van elke klasse kunnen ermee worden voorzien.

Hier volgt een voorbeeld van de implementatie. Onbewerkte tekenreeksen worden gebruikt ter vereenvoudiging, maar een juiste implementatie vereist labels. 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

De omschrijving die wordt geretourneerd door **opportunityDetails**, wordt weergegeven in het zijvenster met meer informatie over de verkoopkans. Dit gebruikt het argument **SelfHealingOpportunity**, dat een **Gegevens**-veld is dat kan worden gebruikt voor meer informatie over de verkoopkans. In het voorbeeld retourneert de methode de id's van de offerteaanvraaggevallen met een lege titel. 

```
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

De twee resterende te implementeren abstracte methoden zijn **provideHealingAction** en **securityMenuItem**. 

**provideHealingAction** retourneert true als een herstelactie wordt verschaft, anders wordt het resultaat false. Als true wordt geretourneerd, moet de methode **performAction** worden geïmplementeerd, anders wordt een fout gegenereerd. De methode **performAction** gebruikt een argument **SelfHealingOpportunity** waarin de gegevens kunnen worden gebruikt voor de actie. In het voorbeeld opent de actie de **PurchRFQCaseTableListPage**, voor handmatige correctie. 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Afhankelijk van de bijzonderheden van de regel, is het mogelijk een automatische actie te gebruiken met de verkoopkansgegevens. In dit voorbeeld kan het systeem titels voor offerteaanvraaggevallen automatisch genereren. 

**securityMenuItem** retourneert de naam van een actiemenuopdracht zodanig zijn dat de regel alleen zichtbaar is voor gebruikers die toegang hebben tot de actiemenuopdracht. Beveiliging vereist mogelijk dat bepaalde regels en mogelijkheden alleen toegankelijk voor geautoriseerde gebruikers zijn. In het voorbeeld kunnen alleen gebruikers met toegang tot **PurchRFQCaseTitleAction** de verkoopkans weergeven. U ziet dat dit actiemenu-item voor dit voorbeeld is gemaakt en is toegevoegd als een invoerpunt voor de beveiligingsbevoegdheid **PurchRFQCaseTableMaintain**. 

> [!NOTE]
> De menuopdracht moet een actiemenuopdracht zijn voor een correcte beveiliging. Andere typen menuopdrachten, zoals **weergavemenuopdrachten**, werken niet goed.

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Nadat de regel is gecompileerd, de volgende taak uitvoeren om het te laten weergeven in de gebruikersinterface (UI).

```
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

De regel wordt weergegeven in het formulier de **Diagnosevalidatieregel** dat beschikbaar is vanuit **Systeembeheer** > **Periodieke taken** > **Validatieregel van diagnose onderhouden**. Als u het wilt laten evalueren, gaat u naar **Systeembeheer** > **Periodieke taken** > **Validatieregel van diagnose plannen** en selecteert u de frequentie van de regel, zoals **Dagelijks**. Klik tot slot op **OK**. Ga naar **Systeembeheer** > **Optimization advisor** om de nieuwe verkoopkans weer te geven. 

Het volgende voorbeeld is een codefragment met het geraamte van een regel, met inbegrip van alle vereiste methoden en kenmerken. Hiermee kunt u aan de slag gaan met het schrijven van nieuwe regels. De labels en actiemenuopdrachten in het voorbeeld worden alleen voor demonstratiedoeleinden gebruikt.

```
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

Voor meer informatie bekijkt u de korte YouTube-video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

