---
title: Werkstroom voor opdrachten tot inkoop
description: Het workflowproces verplaatst opdrachten tot inkoop door het beoordelingsproces, vanaf de beginstatus Concept tot de laatste status Goedgekeurd. Wanneer een opdracht tot inkoop ter controle wordt ingediend, wordt het workflowproces gestart. Nadat een opdracht tot inkoop is goedgekeurd, kan een inkooporder worden gegenereerd voor de regels van de opdracht tot inkoop en kunnen ze bij de leverancier worden ingediend om te worden voltooid.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6069e2ab93e1ce4299669850bdae37e82b17428
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021975"
---
# <a name="purchase-requisition-workflow"></a>Werkstroom voor opdrachten tot inkoop

[!include [banner](../includes/banner.md)]

Het workflowproces verplaatst opdrachten tot inkoop door het beoordelingsproces, vanaf de beginstatus Concept tot de laatste status Goedgekeurd. Wanneer een opdracht tot inkoop ter controle wordt ingediend, wordt het workflowproces gestart. Nadat een opdracht tot inkoop is goedgekeurd, kan een inkooporder worden gegenereerd voor de regels van de opdracht tot inkoop en kunnen ze bij de leverancier worden ingediend om te worden voltooid.

Voordat een opdracht tot inkoop ter controle kan worden ingediend, moet u een workflow configureren. Het workflowproces kan een of meer controlestappen in een willekeurige volgorde bevatten. Het workflowproces kan ook zo worden geconfigureerd dat het de controletaken overslaat en de opdracht tot inkoop automatisch goedkeurt. U kunt de workflow configureren om de opdracht tot inkoop als één document te routeren of u kunt afzonderlijke inkoopopdrachtsregels naar de juiste controleurs routeren. U kunt ook een scenario maken waarbij de opdracht tot inkoop als een enkel document wordt gerouteerd naar bepaalde controleurs en waarbij een selectie van regels in de opdracht tot inkoop naar andere controleurs wordt gerouteerd.  

Als de regels van de opdracht tot inkoop afzonderlijk worden gecontroleerd, moet het controleproces voor alle regels van de opdracht tot inkoop worden uitgevoerd voordat het werkstroomproces naar de volgende stap kan gaan, en voordat het controleproces voor de opdracht tot inkoop als geheel kan worden voltooid. Wanneer het controleproces voor de opdracht tot inkoop en alle regels is voltooid, wordt de algemene status van de opdracht tot inkoop bijgewerkt naar **Goedgekeurd**.  

U kunt uw workflow configureren voor om het bedrijfsproces voor opdrachten tot inkoop in uw organisatie voor te stellen. Houd rekening met de volgende vragen wanneer u uw workflowproces voor opdrachten tot inkoop configureert:

-   Welke uitgaven moeten worden gecontroleerd?
-   Welke uitgaven kunnen automatisch worden goedgekeurd?
-   Wie moet uitgavenverzoeken controleren en goedkeuren? Aan welke rol worden deze gebruikers toegewezen?
-   Welk proces moet worden gevolgd wanneer een controleur niet beschikbaar is?

De volgende voorbeelden geven een voorbeeld van twee manieren waarop u een workflow voor opdrachten tot inkoop kunt configureren.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Voorbeeld 1: Een opdracht tot inkoop als één document voor revisie verzenden
De volgende afbeelding geeft aan hoe een opdracht tot inkoop als één document door het workflowcontroleproces kan stromen. De regels van de opdracht tot inkoop worden niet afzonderlijk gerouteerd. De volgende rollen zijn in het workflowproces opgenomen voor dit voorbeeld:

-   **Aanvrager** – De gebruiker die de artikelen of services bestelt. De aanvrager kan de opdracht tot inkoop voorbereiden of een andere werknemer kan de opdracht tot inkoop namens de aanvrager voorbereiden. Deze werknemer is de voorbereider. De voorbereider is verantwoordelijk voor het beheren van de opdracht tot inkoop in het hele controleproces. Alleen de voorbereider van de opdracht tot inkoop kan deze wijzigen.

**Opmerking:** Een werknemer moet de juiste machtigingen krijgen om een opdracht tot inkoop te maken namens iemand anders. Gebruik de pagina **Machtiging voor inkoopbestelopdrachten** om deze machtigingen in te stellen.

-   **Inkoper** – De gebruiker die een aanschaffingscontrole uitvoert en het document kan goedkeuren.
-   **De manager van de aanvrager** – De gebruiker die een managercontrole uitvoert en het document kan goedkeuren.

![Werkstroom controleproces voor opdrachten tot inkoop](./media/purchreqworkflowoverview_submission.gif)  
In dit voorbeeld omvat het workflowproces voor de opdracht tot inkoop de volgende stappen:

1.  De voorbereider dienst een opdracht tot inkoop ter controle in.
2.  De inkoper ontvangt een melding. De inkoper ontvangt een melding die vraagt om de informatie in de opdracht tot inkoop te controleren. Als vereiste informatie ontbreekt, kan de inkoper de informatie toevoegen of de opdracht tot inkoop terugsturen naar de voorbereider om de info te laten toevoegen. Wanneer alle vereiste info is ingevuld, kan de opdracht tot inkoop naar de volgende stap gaan in het controleproces.
3.  De manager van de aanvrager controleert de opdracht tot inkoop. De opdracht tot inkoop kan bijvoorbeeld naar de manager van de aanvrager worden gerouteerd als het bedrag van de opdracht tot inkoop de uitgavenlimiet van de aanvrager voor opdrachten tot inkoop heeft overschreden. De manager van de aanvrager kan de opdracht tot inkoop goedkeuren of afwijzen of deze terugsturen naar de voorbereider voor wijzigingen.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Voorbeeld 2: De individuele regels in de opdracht tot inkoop ter controle routeren
De volgende afbeelding geeft aan hoe de individuele regels in een opdracht tot inkoop door een workflow kunnen worden gerouteerd. Het proces voor elke regel is in het algemeen hetzelfde als het proces voor een opdracht tot inkoop die als één document wordt gecontroleerd. Elke regel moet het workflowproces afzonderlijk voltooien voordat de workflow voor de hele opdracht tot inkoop kan worden voltooid.  

In dit voorbeeld voert een werknemer een aanvraag in voor posters en t-shirts voor een marketingcampagne. De kosten van de posters wordt tussen de marketingafdeling en de verkoopafdeling opgesplitst. Als de kosten van de posters of t-shirts de ondertekeningslimiet voor afdelingsmanagers overschrijdt, moet de opdracht tot inkoop ook door de groepsmanager worden gecontroleerd.  

De volgende rollen zijn in het workflowproces opgenomen voor dit voorbeeld:

-   **Aanvrager** – De gebruiker die de artikelen of services bestelt. De aanvrager kan de opdracht tot inkoop voorbereiden of een andere werknemer kan de opdracht tot inkoop namens de aanvrager voorbereiden. Deze werknemer is de voorbereider. De voorbereider is verantwoordelijk voor het beheren van de opdracht tot inkoop in het hele controleproces. Alleen de voorbereider van de opdracht tot inkoop kan deze wijzigen.

**Opmerking:** Een werknemer moet de juiste machtigingen krijgen om een opdracht tot inkoop te maken namens iemand anders. Gebruik de pagina **Machtiging voor inkoopbestelopdrachten** om deze machtigingen in te stellen.

-   **Inkoper** – De gebruiker die een aanschaffingscontrole uitvoert en het document kan goedkeuren.
-   **De manager van de aanvrager** – De gebruiker die een managercontrole uitvoert en het document kan goedkeuren.
-   **Afdelingsmanager** – De gebruiker die een uitgavencontrole uitvoert en het document kan goedkeuren.
-   **Groepsmanager** – De gebruiker die een handtekeningsbevoegdheidscontrole uitvoert en het document kan goedkeuren.

![Workflowcontroleproces voor regel van opdracht tot inkoop](./media/purchreqlineworkflowoverview.gif)  
In dit voorbeeld omvat het workflowproces voor de regels in de opdracht tot inkoop de volgende stappen:

1.  De voorbereider dienst een opdracht tot inkoop ter controle in. Elke regel wordt naar de controleur gerouteerd die in het workflowproces is geconfigureerd om deze te ontvangen.
2.  De inkoper ontvangt een melding. De inkoper ontvangt een melding die de inkoper vraagt om de informatie in de opdracht tot inkoop en regels in de opdracht tot inkoop te controleren. Wanneer de opdracht tot inkoop wordt geopend door de inkoper, worden alle regels weergegeven, maar geeft een visuele indicator aan welke regels voor revisie naar de inkoper zijn verzonden. Als vereiste informatie ontbreekt, kan de inkoper de informatie toevoegen of een regel in een opdracht tot inkoop terugsturen naar de voorbereider om de info toe te voegen. Wanneer alle vereiste info is ingevuld, kan de regel in de opdracht tot inkoop naar de volgende stap gaan in het controleproces. Regels in een opdracht tot inkoop kunnen het controleproces onafhankelijk van elkaar doorlopen.
3.  De lijnmanager van de aanvrager controleert de regels in de opdracht tot inkoop en keurt deze goed. De goedkeuring kan naar de manager van de aanvrager worden gerouteerd als het bedrag op een regel in de opdracht tot inkoop de uitgavenlimiet van de aanvrager voor regels in een opdracht tot inkoop overschrijdt. De manager kan een van de of beide regels in de opdracht tot inkoop goedkeuren of afwijzen.
4.  De afdelingsmanager voor de marketingafdeling controleert de regels in de opdracht tot inkoop voor zowel de posters als de t-shirts. De afdelingsmanager voor de verkoopafdeling controleert de regel in de opdracht tot inkoop alleen voor de posters, omdat dit de enige kost is die aan de verkoopafdeling wordt toegerekend.
5.  De regel in de opdracht tot inkoop voor de t-shirts wordt alleen door de groepsmanager gecontroleerd en goedgekeurd als goedkeuring van de groepsmanager vereist is, bijvoorbeeld als het bedrag op de regel in de opdracht tot regel de goedkeuringslimiet van de afdelingsmanager overschrijdt. De groepmanager hoeft de regel in de opdracht tot inkoop voor de posters niet goed te keuren.

> [!NOTE]
> De systeemvaluta moet worden ingesteld als de koptekstworkflow voor een opdracht tot inkoop goedkeuringen vereist die zijn gerelateerd aan ondertekeningslimieten.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Een workflow voor opdrachten tot inkoop configureren
Om een opdracht tot inkoop ter controle te routeren, moet u de workflowprocessen voor de opdracht tot inkoop configureren. Het workflowproces dat u definieert, controleert de interactie tussen de gebruiker die de artikelen heeft aangevraagd (de aanvrager) en de controleur en goedkeurder in de workflow. De route van de opdracht tot inkoop is afhankelijk van de voorwaarden die in de workflowconfiguratie zijn opgegeven. Bijvoorbeeld: deze voorwaarden definiëren wanneer de opdracht tot inkoop moet worden doorgestuurd, de gebruiker of rol waarnaar het moet worden doorgestuurd, en de acties die gebruikers kunnen uitvoeren.  

De voorbeelden in dit onderwerp beschrijven hoe een opdracht tot inkoop kan worden gerouteerd via een workflow als één document of als individuele regels in een opdracht tot inkoop. U kunt ook een workflow voor opdrachten tot inkoop configureren die de interne controle van opdrachten tot inkoop weerspiegelt die voor uw organisatie is gedefinieerd.  

De deelnemers of controleurs aan wie een taak in een werkstroom wordt toegewezen kunnen lid zijn van een bepaalde gebruikersgroep, gebruikers zijn die een bepaalde beveiligingsrol hebben, gebruikers zijn die gekoppeld zijn aan de indiener in een managementhiërarchie of benoemde gebruikers of gebruikers die specifieke uitgavenverantwoordelijkheden hebben.

### <a name="purchase-requisition-expenditure-reviewers"></a>Controleurs van uitgaven voor opdrachten tot inkoop

U kunt met configuraties voor uitgavencontroleurs uitgaven dynamisch ter beoordeling routeren op basis van de gebruiker die aan een projectrol is toegewezen of een financiële dimensie waar de uitgave in rekening wordt gebracht. Het workflowproces gebruikt de opgegeven projectrol of eigenaar van de financiële dimensie om te bepalen naar wie de uitgave moet worden doorgestuurd.  

U kunt een of meer configuraties voor uitgavencontroleurs definiëren en vervolgens een configuratie selecteren wanneer u een workflow maakt. U kun de waarden voor de uitgavencontroleurs configureren voor elke rechtspersoon in uw organisatie. Nadat u de configuraties voor uitgavencontroleurs hebt gedefinieerd, wijst u een configuratie aan uw workflowtaak toe.  

U hoeft geen configuraties voor uitgavencontroleurs te definiëren. U kunt in plaats daarvan specifieke gebruikers of gebruikersgroepen toewijzen als controleurs wanneer u uw workflow definieert. Als u echter een complexe organisatie hebt, kunnen uitgavencontroleurs de efficiëntie van uw goedkeuringsproces verhogen. Bovendien hoeft u bij het instellen van uitgavencontroleurs niet telkens toewijzingen van workflowcontroleurs bij te werken telkens als een controleur een andere taakrol krijgt.  

U kunt de uitgavencontroleurs op de pagina **Controleurs van uitgaven voor opdrachten tot inkoop** instellen. Maak een configuratie van de uitgavencontroleur en voer waarden in voor elke rechtspersoon in uw organisatie. Voor opdrachten die aan een project zijn toegewezen, kunt u de rol opgeven die voor het controleren van de opdrachten verantwoordelijk is: Projectmanager, Projectcontroleur of Projectverkoopmanager. Uitgaven worden naar de gebruiker gerouteerd die aan de opgegeven rol is toegewezen. U kunt ook de uitgaven naar de eigenaar van de financiële dimensie routeren door het correcte selectievakje van de financiële dimensie aan te vinken op het tabblad **Organisatieverdelingen**.  

Als u een van de uitgavencontroleurs wilt gebruiken die u in een workflow instelt, moet u de optie **Type deelnemer** instellen op **Uitgavendeelnemers** in de eigenschappen **Toewijzing** voor het relevante workflowelement.

<a name="additional-resources"></a>Aanvullende resources
--------

[Een bestelaanvraag voor verbruik maken](tasks/create-requisition-consumption.md)

[Bedrijfsprocesworkflows voor opdrachten tot inkoop definiëren](https://www.microsoft.com/download/details.aspx?id=101821)

[Workflows voor inkoop en sourcing](procurement-sourcing-workflows.md)

[Overzicht van opdrachten tot inkoop](purchase-requisitions-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]