---
title: Orderverwerkingsopties instellen
description: 'Dit onderwerp bevat informatie over het verwerken van orders voor callcenter is erg met behulp van Microsoft Dynamics 365 voor bewerkingen: Retail.'
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>Orderverwerkingsopties instellen

Dit onderwerp bevat informatie over het verwerken van orders voor callcenter is erg met behulp van Microsoft Dynamics 365 voor bewerkingen: Retail. 

Ondersteunt meerdere detailhandelkanalen, zoals onlinewinkels, markering en fysieke winkels en callcenter is erg detailhandel en commerce in Dynamics 365 voor bewerkingen. In een callcenter nemen de werknemers via de telefoon klantenorders aan en maken ze verkooporders. Dit onderwerp beschrijft hoe u een call center kunt maken en de opties van het call center kunt configureren. Elk call center kan eigen gebruikers, betalingsmethoden, prijsgroepen, financiële dimensies en leveringsmethoden hebben. U kunt deze opties configureren wanneer u het call center maakt. **Belangrijk:** Voordat callcenterworkflows kunnen worden gebruikt wanneer de huidige Dynamics AX-gebruiker verkooporders maakt, moet de gebruiker aan het callcenter worden toegewezen als een callcentergebruiker. U kunt de pagina **Callcenter** gebruiken om groepen of functies in te schakelen of uit te schakelen die uniek voor callcenters. De volgende groepen functies kunnen worden ingeschakeld:

-   **Ordervoltooiing**: deze groep bevat functies die aan betalingen en ordervoltooiing in de **Verkooporder** zijn gekoppeld.
-   **Geleide verkoop:** deze groep bevat functies die aan broncodes, scripts en catalogusaanvragen worden gekoppeld.

Wanneer u deze functies in de instellingen van het call center inschakelt, worden ze beschikbaar in de pagina **Verkooporder** voor gebruikers die aan het call center worden gekoppeld. De meeste van deze functies vereisen aanvullende instellingen voordat ze gebruikt kunnen worden. Afbeeldingen en scripts worden ingeschakeld als onderdeel van de rechtstreekse verkoopinstelling voor het specifieke callcenter. Als deze functies zijn ingeschakeld, worden de scripts en de productafbeeldingen weergegeven in het feitenvak van de pagina **Verkooporder**. De standaardafbeelding die voor een product is ingesteld wordt weergegeven. De scripts kunnen voor een artikel, een catalogus, een klant, of artikel in de context van een catalogus worden geconfigureerd. Callcenterorders kunnen aanvullende details weergeven over hoe de prijs voor een specifieke orderregel is afgeleid. De orders tonen bijvoorbeeld welke kortingen zijn toegepast. Inschakelen van deze functionaliteit op **klanten**&gt;**Setup**&gt;**parameters van module klanten**&gt;**prijzen**&gt;**prijs details**. U kunt de pagina **Prijsgegevens** vanuit de vervolgkeuzelijst **Verkooporderregel**. U kunt ordergebeurtenissen volgen gebruiken voor controledoeleinden, om de acties te bekijken die worden toegepast op een order tijdens de levenscyclus van de order, of om de acties van een bepaalde gebruiker te volgen. U kunt bijvoorbeeld steeds de actie registreren wanneer een gebruiker een verkooporder maakt, deze in de wacht zet, een toeslag overschrijft of een orderregel bijwerkt. U kunt ordergebeurtenissen instellen om acties te traceren voor specifieke gebruikers, groepen gebruikers, of alle gebruikers in een specifieke periode. U kunt de acties bekijken die op een document zijn ondernomen door de pagina **Ordergebeurtenissen** in het actievenster te openen op de pagina voor dat document. Kunt u gebeurtenissen van de order op **verkoop en marketing**&gt;**Setup**&gt;**gebeurtenissen**&gt;**bestellen gebeurtenissen**. Wanneer een klantorder niet op tijd kan worden verzonden, kan een bedrijf automatisch e-mailmeldingen naar de klant verzenden om de orderstatus te melden en de klant de kans te geven een order te annuleren. Als de vertraging langer is dan een bepaalde duur, kan de order automatisch worden geannuleerd. Er kunnen tot drie e-mailberichten met bepaalde intervallen worden verzonden:

1.  **Eerste annuleringsmelding** – De klant kan de order annuleren.
2.  **Tweede annuleringsmelding** – De klant kan de order annuleren.
3.  **Definitieve annuleringsmelding** – Het systeem annuleert de order en de klant wordt geïnformeerd over de annulering.

U kunt afzonderlijke klanten en producten vrijstellen van het proces met automatische meldingen en annuleringen. Een margewaarschuwing wordt geactiveerd wanneer u een artikel aan een order toevoegt. De waarschuwing bevat belangrijke informatie over het artikel, zoals de prijsmarge van het artikel en winstgevendheid. U kunt deze informatie gebruiken om te bepalen of een prijs overschrijving van toepassing is wanneer u een artikel toevoegt aan de verkooporder. U stelt bijvoorbeeld drempels in voor de handelsmarges, om op te geven dat een drempel van 40% of meer boven de kosten acceptabel is voor een artikel, maar een drempel van 20 to 39% boven de kosten is dubieus. In dit geval activeert elk artikel dat een drempel tussen 20 en 39 procent heeft, een waarschuwing. Elk artikel dat een drempel van minder dan 20 procent boven kosten heeft, kan niet worden verkocht en de artikelprijs kan niet worden gecorrigeerd. U kunt waarschuwingen marge op **klanten**&gt;**instellingen**&gt;**parameters van module klanten**&gt;**marges waarschuwingen**. Wanneer kunt u de btw-overeenkomst instelt op basis van standaardregels, kunt u een overeenstemmende prioriteit bepalen voor adreselementen. U kunt bijvoorbeeld opgeven dat het afstemmen van een btw-groep op postcode een hogere prioriteit heeft dan het afstemmen van een btw-groep op staat. Als u nieuwe klantadresrecords invoert, wordt de btw-groep automatisch toegewezen op basis van hoe het adres van de klant overeenkomt met de standaardregels en prioriteitmatching die u hebt gedefinieerd. U kunt deze functionaliteit configureren op de pagina **Grootboekparameters**.


