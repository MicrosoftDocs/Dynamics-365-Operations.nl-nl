---
title: Budget-overzicht
description: "Dit artikel introduceert budgetbeheer gebruikt en wordt uitgelegd hoe u budgetbeheer configureert in Microsoft Dynamics 365 voor bewerkingen, zodat u kunt financiële middelen beheren."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 04e0c066511c1fedf33784944441326201fc2df8
ms.lasthandoff: 03/31/2017


---

# <a name="budget-control-overview"></a>Budget-overzicht

Dit artikel introduceert budgetbeheer gebruikt en wordt uitgelegd hoe u budgetbeheer configureert in Microsoft Dynamics 365 voor bewerkingen, zodat u kunt financiële middelen beheren.

<a name="overview"></a>Overzicht
--------

Budgetbeheer in Microsoft Dynamics 365 voor bewerkingen ondersteunt beheer van financiële middelen tot en met het rekeningschema, workflows, gebruikersgroepen, brondocumenten en journalen, configureerbare berekening van beschikbare budgetfondsen, budgetcycli en drempelwaarden van een organisatie. Wanneer de juiste controles plaatsvinden, kan een organisatie de financiële middelen het hele fiscale jaar door plannen, meten, beheren en voorspellen. 

Nadat de budgetten in Dynamics 365 voor bewerkingen zijn goedgekeurd, kunt u budgetplannen voor het genereren van budgetregisterregels om vast te leggen van de begroting der uitgaven voor een organisatie. U kunt ook maken, of budgetregisterregels importeren vanuit een programma van derden in plaats van de functie voor het plannen van budgetten. 

Uitgaven kunnen worden geregistreerd met behulp van hoofdrekeningen en financiële dimensies. U kunt de controle van de algehele uitgaven configureren te voldoen aan debeleidsregels en behoeften van de organisatie door combinaties van financiële dimensies en hoofdrekeningen te groeperen. 

De volgende diagram laat de plaats van het budgetbeheer zien in de fasen van een gebruikelijke budgetcyclus.

[![budgetingCycle](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Kunt u budgetbeheer op basis van verschillende factoren:

-   **Financiële dimensies** – Welke financiële dimensies moeten worden gebruikt voor het rapporteren van budget en werkelijke cijfers en welke financiële dimensies zijn vereist voor budgetbeheer? Zijn er specifieke combinaties van dimensies of hoofdrekeningen die speciale aandacht eisen? Is er bijvoorbeeld een vereiste om budget naar werkelijke cijfers bij te houden per kostenplaats en programma? Vereisen reiskosten speciale aandacht?
-   **Tijd** – Welk tijdsbestek (boekperiode, boekperiode tot heden enzovoort) wordt gebruikt om beschikbare budgetfondsen te beoordelen?
-   **Brondocumenten** : welke brondocumenten moeten worden geëvalueerd voor budgetbeheer? Moeten de documenten worden geëvalueerd per regel of per document?
-   **Berekening van beschikbare fondsen** – Moet bij de berekening van beschikbare fondsen rekening worden gehouden met documenten zoals opdrachten tot inkoop (voorvorderingen) en inkooporders (vorderingen)? Moet bij de berekening rekening worden gehouden met documenten in een conceptstatus?
-   **Machtigingen overschrijven** – Wie heeft machtiging om het beschikbare budget te overschrijden?

Budgetbeheer is volledig geïntegreerd met Dynamics 365 voor bewerkingen. Daarom kunt u het beschikbare budget voor zowel geplande als werkelijke inkopen evalueren. Er zijn vragen en rapporten over budgetten beschikbaar. Gebruikers kunnen hierdoor gedurende de hele budgetcyclus het budget beoordelen en vervolgens eventueel benodigde correcties in de vorm van budgetrevisies of overboekingen. Een budgetbeheerder kan ook het budget en werkelijke cijfers exporteren naar Microsoft Excel om deze, indien nodig, beter te analyseren en voorspellen.

## <a name="configuring-budget-control"></a>Budgetbeheer configureren
### <a name="budget-cycle-time-span"></a>Budgetcyclusduur

Nadat u basisbudgettering hebt geconfigureerd, kunt u de tijd of de begin- en eindperioden voor budgettering en budgetbeheer definiëren op de pagina **Budgetcyclusduur**. Budgetcycli komen vaak overeen met fiscale kalenders, maar kunnen fiscale jaren beslaan.

De volgende stappen in de configuratie worden uitgevoerd op de verschillende tabbladen voor de **budgetbeheerconfiguratie** pagina.

### <a name="define-parameters"></a>Parameters definiëren

Op basis van de financiële dimensies die voor het budget zijn ingeschakeld, kunt u alle financiële dimensies of een subset hiervan gebruiken voor budgetbeheer. 

Bovendien kunt u het standaardtijdsinterval (bijvoorbeeld **Boekjaar**, **Boekjaar tot heden** **Boekperiode** of **Driemaandelijks**) waarvoor budgetbeheer wordt uitgevoerd in de gerelateerde budgetcyclusduur. U kunt ook een standaard budgetbeheerder en de drempel opgeven die wordt gebruikt om gebruikers te informeren over wanneer de drempel is bereikt. De waarden in deze velden worden als standaardwaarden gebruikt in elke nieuwe regel voor budgetbeheer of budgetgroep die wordt gemaakt. De standaardwaarden kunnen echter worden gewijzigd voor afzonderlijke groepen of regels. 

De manieren waarop budgetten worden gemaakt en in het budgetregister geregistreerd, helpt bij het vaststellen van de periode die wordt geselecteerd voor het beoordelen van beschikbare budgetfondsen. Als een bedrag op jaarbasis wordt ontwikkeld en gebruikt voor een combinatie van dimensiewaarden, kan keuze voor fiscaal jaar of fiscaal jaar tot heden zinvol lijken. Als een organisatie die budgetten opstelt per boekperiode of toewijst aan boekperioden echter gedetailleerder beheer wil, is het wellicht verstandig boekperiode tot heden of per kwartaal te overwegen. 

Bovendien helpt ook de cultuur van een organisatie een rol bij het vaststellen van de configuratie omdat deze aan budgettering en begrotingscontrole is gekoppeld.

### <a name="over-budget-permissions"></a>Machtigingen om boven het budget te gaan

Vervolgens kunt u op het tabblad **Machtigingen om boven het budget te gaan** gebruikersgroepen opgeven. U kunt ook opgeven of gebruikers die lid zijn van een groep zijn gemachtigd om het budget te overschrijden. U kunt voorkomen dat gebruikers de budgetdrempel boven het budget te overschrijden die op de pagina **Budgetparameters** is ingesteld of u kunt voorkomen dat deze het budget overschrijden met welk bedrag dan ook, ongeacht de drempel. Afhankelijk van hoe proactief een organisatie zijn uitgaven beheert, kunnen deze machtigingen helpen om de financiële middelen te beheren. 

### <a name="budget-funds-available"></a>Beschikbare budgetfondsen

Vervolgens kunt u op het tabblad **Beschikbare budgetfondsen** de formule definiëren die wordt gebruikt om beschikbare budgetfondsen te berekenen. Afhankelijk van hoe conservatief een organisatie zijn financiële middelen beheert, of afhankelijk van de regelgeving of industrievereisten, kan de berekening conceptdocumenten of niet-geboekte documenten bevatten. 

> [!NOTE] 
> Als de berekening wordt gewijzigd tijdens een budgetcyclus, hebben de wijzigingen geen invloed op documenten die het besturingselement budgetcontroles eerder is uitgevoerd en die zijn geboekt of voltooid.

### <a name="documents-and-journals"></a>Documenten en journalen

Vervolgens kunt u op het tabblad **Documenten en journalen** selecteren welke brondocumenten en journalen aan budgetbeheercontroles worden onderworpen en of de controles zullen plaatsvinden op het niveau van de regelinvoer of voor het document in zijn geheel. 

U moet de brondocumenten die zijn geselecteerd vergelijken met de selectievakjes voor saldi die zijn opgenomen in de berekening van beschikbare budgetfondsen. Als u bijvoorbeeld **Budgetreserveringen voor vorderingen** hebt geselecteerd, moet u de optie **Inkooporders** selecteren. Wanneer een budgetcontrole wordt uitgevoerd voor de bedragen en rekeningen op een inkoopregels, dan is de budgetbeheercategorie die aan de reservering wordt toegekend **Vordering**. Wanneer een budgetcontrole wordt uitgevoerd voor de bedragen en rekeningen op een opdracht tot inkoop, is de budgetbeheercategorie die aan de reservering wordt toegekend **Voorvordering**. 

Als **Budgetreserveringen voor vordering** en/of **Budgetreserveringen voor voorvordering** is/zijn opgenomen in de berekening van beschikbare budgetfondsen en moet(en) worden weergegeven in boekingen in het grootboek , moet u de toewijzingsboekhouding inschakelen op de pagina **Grootboekparameters**.  

### <a name="assign-budget-models"></a>Budgetmodellen toewijzen

Vervolgens wijst u, op het tabblad **Budgetmodellen toewijzen** budgetmodellen toe aan de budgetcyclusduren die in het budgetbeheer moeten worden opgenomen.

### <a name="define-budget-control-rules"></a>Regels voor budgetbeheer definiëren

Vervolgens moet u op het tabblad **Regels voor budgetbeheer definiëren** specifieke regels maken op basis van financiële dimensies die zijn ingeschakeld voor budgetbeheer. Als er bijvoorbeeld nadruk ligt op de uitgaven of het bereik van uitgaven voor een afdeling, kunt u de instellingen op dit tabblad gebruiken voor het definiëren en beoordelen van die uitgaven. U kunt vrschillende drempels definiëren voor elke regel voor budgetbeheer. 

> [!Important]
> Budgetbeheer wordt ingeschakeld voor elke hoofdrekening van de **verlies-en**, **onkosten**, **opbrengst, balans, passiva en eigen vermogen** of **activa** type. Als dit tabblad een regel bevat met lege criteria, wordt budgetbeheer ingeschakeld voor **alle **combinaties van financiële dimensies die hoofdrekeningen van deze typen bevatten. Zorg er daarom voor dat u regels voor budgetbeheer maakt die alleen de bereiken definiëren van financiële dimensiecombinaties waarbij het belangrijk is dat budgetbeheer wordt ingeschakeld.  

### <a name="select-main-accounts"></a>Hoofdrekeningen selecteren

Als **Hoofdrekening** niet als budgetbeheerdimensie wordt geselecteerd op de pagina **Parameters definiëren**, maar de specifieke uitgaven worden beheerd, kunt u die uitgaven selecteren op het tabblad **Hoofdrekeningen selecteren**. Als **Hoofdrekening** is geselecteerd als een budgetbeheerdimensie, zijn geen boekingen vereist.  

### <a name="define-budget-groups"></a>Budgetgroepen definiëren

Vervolgens kunt u op het tabblad **Budgetgroepen definiëren** optioneel unieke combinaties van financiële dimensies definiëren waarbij budgetbronnen worden verzameld voor secundaire budgetcontrole. U kunt één registratie maken die de hele organisatie omvat of meerdere groepen definiëren die afzonderlijke afdelingen of kostenplaatsen vertegenwoordigen.  

### <a name="define-message-levels"></a>Berichtniveaus definiëren

Als waarschuwingsberichten voor budgetbeheer moeten worden onderdrukt voor gebruikersgroepen, kunt u die groepen opgeven op de pagina **Berichtniveaus definiëren**. Leden van de gebruikersgroepen blijven foutberichten ontvangen wanneer de beschikbare budgetfondsen worden overschreden, op basis van hun machtigingen voor budgetoverschrijding.

### <a name="activate-budget-control"></a>Budgetbeheer activeren

Nadat budgetbeheer is geconfigureerd, kunt u dit inschakelen en het activeren op het tabblad **Budgetbeheer activeren**. De conceptversie wordt dan van kracht.
> [!Important]
> Nadat budgetbeheer is ingeschakeld en actief en nadat transacties zijn geboekt, moet deze niet worden uitgeschakeld om het midden van het jaar. Wanneer budgetbeheer is uitgeschakeld, worden geen activiteiten geregistreerd ten behoeve van budgetbeheer en worden er geen budgetcontroles meer uitgevoerd. Daarom geven documenten die reeds zijn geboekt mogelijk niet op de juiste wijze ontlastende bedragen of saldi weer in query's en rapporten die verband houden met budgetbeheer. Deze omvatten statistieken voor budgetbeheer voor eventuele downstream of correctiedocumenten en -journalen. 

Bovendien wordt geen rekening gehouden met transacties die zijn geboekt voordat budgetbeheer werd ingeschakeld. Daarom is het raadzaam om budgetbeheer alleen aan het begin van een nieuwe budgetcyclus in te schakelen. Zorg ervoor dat budgetregisterposten die beginbudgetsaldi voor budgetbeheer bevatten alleen worden bijgewerkt nadat budgetbeheer is ingeschakeld. Elk openstaand document (bijvoorbeeld een inkooporder) wordt gecontroleerd op beschikbare budgetfondsen en krijgt een budgetreservering voor budgetbeheer wanneer een gebruiker handmatig een budgetbeheercontrole activeert in het document.

## <a name="using-budget-control"></a>Budgetbeheer gebruiken
Nadat budgetbeheer is ingeschakeld, ontvangen gebruikers waarschuwings- en foutberichten in verband met budgetbeheer in documenten en journalen die voor budgetbeheer zijn geconfigureerd. Onthoud dat u budgetbeheer kunt configureren zodat gebruikers worden gewaarschuwd wanneer ze de budgetfondsen overschrijden, maar nog steeds de transactie kunnen bevestigen of boeken. Gebruikers kunnen de details van mislukte budgetcontroles bekijken op de pagina **Budgetbeheerfouten en waarschuwingen**.   

Gebruikers kunnen op deze pagina inzoomen op de **budgetbeheerstatistieken per periode** pagina beschikbaarheid budgetgegevens weergeven en reserveringen voor geselecteerde budget control dimensiecombinatie. Gebruikers kunnen ook inzoomen op de pagina **Budgetbeheerstatistiek **om de budgetbeschikbaarheid te bekijken voor alle dimensies van financiële dimensies die worden gebruikt in budgetbeheer. 

Als budgetbeheer is ingeschakeld voor inkooporders, kan de budgetbeheerder de werkruimte **Grootboekbudgetten en prognoses** gebruiken om de wachtrij te bekijken van alle niet-bevestigde inkooporders met budgetcontrolewaarschuwingen en -fouten. Als de budgetbeheerder machtigingen om over budget te gaan heeft geconfigureerd, kan hij of zij inkooporders rechtstreeks in de werkruimte bevestigen.    


