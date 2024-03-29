---
title: Compensatieproces definiëren en resultaten berekenen
description: Compensatieprocessen worden gebruikt om nieuwe compensatiebedragen en toekenningen voor werknemers te definiëren die in vaste en variabele compensatieplannen zijn ingeschreven.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687046"
---
# <a name="define-compensation-process-and-calculate-results"></a>Compensatieproces definiëren en resultaten berekenen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Compensatieprocessen worden gebruikt om nieuwe compensatiebedragen en toekenningen voor werknemers te definiëren die in vaste en variabele compensatieplannen zijn ingeschreven. Compensatieprocessen kunnen meerdere keren worden uitgevoerd om een 'wat-als'-analyse uit te voeren, om te controleren of alle wijzigingen en instellingen correct zijn. Deze procedure maakt een compensatieproces, voert het proces uit en bekijkt de resultaten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-compensation-process"></a>Een compensatieproces maken
1. Ga naar **Compensatiebeheer** > **Proces** > **Compensatieprocessen**.
2. Klik op **Nieuw compensatieproces**.
3. Typ een waarde in het **Proces-veld**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer een optie in het veld **Procestype**.
    * Een cyclus geeft de periode aan die wordt geëvalueerd om compensatie te bepalen. De evaluatie bepaalt welke posities de werknemers hadden, welke prestatiesbeoordelingen moeten worden opgenomen, de berekening van het percentage van tijd waarin de werknemer tijdens de cyclus was aangesteld en meer. Een voorbeeld van een begindatum van een cyclus zou de eerste dag van het boekjaar kunnen zijn.  
6. Voer in het veld **Begin cyclus** een datum in.
    * De einddatum van cyclus is belangrijk omdat deze datum wordt gebruikt om te bepalen welke werknemers actief in dienst waren en in een of meerdere compensatieplannen geregistreerd waren.  
7. Voer in het veld **Einde cyclus** een datum in.
    * De actieve datum van transactie is de datum waarop de nieuwe compensatietarieven van kracht moeten worden. Veel bedrijven nemen een paar maanden op tussen het einde van een cyclus en de tijd waarop de nieuwe compensatietarieven van kracht gaan. De extra tijd wordt gebruikt voor de verwerking en controle van de nieuwe compensatie.  
8. Voer in het veld **Actieve datum van transactie** een datum in.
    * De tijdsgebonden datum wordt gebruikt voor variabele compensatieplannen die het toekenningsbedrag van een werknemer bepalen op basis van de compensatietarief op dat moment.  
    * De aanstellingsdatum voor omgeslagen vast loon wordt gebruikt met vaste compensatieplannen met als aanstellingsregel **Percentage**. Werknemers die tussen de begindatum van cyclus en de huurdatum omgeslagen vast loon in dienst worden genomen, krijgen 100% van hun berekende compensatieverhoging in plaats van het omgeslagen percentage.  
9. Voer in het veld **Huurdatum omgeslagen vast loon** een datum in.
    * De deadline voor controle is de datum waarop alle procesresultaten moeten zijn gecontroleerd zodat deze in de compensatierecord van een werknemer kunnen worden geladen vóór de actieve datum van transactie. Dit veld is alleen ter informatie.  
10. Voer in het veld **Deadline beoordelen** een datum in.
11. Klik op **Opslaan**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>De compensatieplannen en -acties voor een compensatieproces instellen
1. Klik op **Instellen**.
    * De pagina **Instellingen** wordt gebruikt om te selecteren welk plan wordt verwerkt als onderdeel van dit compensatieproces en welke acties voor elk plan moeten worden uitgevoerd.  
2. Typ of selecteer een waarde in het veld **Plannen**.
3. Klik op **Opslaan**.
4. Klik op **Toevoegen**.
5. Selecteer in het veld **Actie** een actietype **Eigen vermogen**.
6. Klik op **Toevoegen**.
7. Selecteer in het veld **Actie** een actietype **Verdienste**.
    * Compensatieacties kunnen aan elkaar worden 'geketend' met het veld **Vorig resultaat gebruiken** om aan te geven of de geselecteerde actie het basisloon van de werknemer of het resultaat van de vorige actie moet gebruiken als beginpunt voor de berekening van deze actie.  
8. Selecteer **Ja** in het veld **Vorig resultaat gebruiken**.
9. Klik op **Toevoegen**.
10. Selecteer in het veld **Actie** een actietype **Algemeen**.
    * Verschillende compensatieactietypen schakelen andere velden in. Voor het compensatieactietype Algemeen kunt u een verhogingspercentage of een verhogingsbedrag opgeven.  
11. Selecteer de optie **Verhogingsbedrag selecteren**.
12. Voer in het veld **Verhogingsbedrag** een getal in.
13. Klik op **Toevoegen**.
14. Selecteer in het veld **Actie** een actietype **Promotie**.
    * Met de actietypen Promotie en Andere niveauwijziging kunnen gebruikers handmatige aanpassingen uitvoeren aan de werknemerscompensatie. Aanbevelingen kunnen worden ingeschakeld voor deze actietypen, net als andere actietypen om u de mogelijkheid te bieden om een nieuwe aanbevolen compensatiewaarde voor een werknemer in te voeren.  
15. Klik op **Toevoegen**.
16. Selecteer een optie in het veld **Type**.
    * Vaste en variabele compensatieplannen kunnen in hetzelfde compensatieproces worden uitgevoerd.  
17. Typ of selecteer een waarde in het veld **Plannen**.
    * Gebruik het selectievakje **Prestatieloon inschakelen** om te bepalen of vaste en variabele compensatiebedragen moeten worden gecorrigeerd op basis van de prestatiesbeoordeling van de werknemer.  
    * Hefboomwerking kan worden overschreven op variabele compensatieplannen.  
18. Klik op **Opslaan**.
19. Klik op **Toevoegen**.
20. Sluit de pagina.

## <a name="run-the-compensation-process"></a>Het compensatieproces uitvoeren
1. Klik op **Proces uitvoeren**.
    * Met het bedieningselement **Resultaten van verwerking weergeven** kunt u de verwerking van berichten weergeven voor het volledige compensatieproces wanneer de verwerking is voltooid.  
2. Selecteer **Ja** in het veld **Resultaten van verwerking weergeven**.
3. Klik op **OK**.

## <a name="view-the-results"></a>De resultaten weergeven
1. Klik op **Procesresultaten**.
2. Klik op **Werknemersresultaten**.
3. Zoek en selecteer de gewenste record in de lijst.
4. Vouw de sectie **Vaste compensatie** uit.
    * Vouw de sneltabbladen uit om de resultaten van het proces weer te geven. Als voor een compensatieactie **Aanbevelingen inschakelen** is gemarkeerd, worden de velden voor **Aanbeveling** ingeschakeld voor die actie.  
5. Zoek en selecteer de gewenste record in de lijst.
    * U kunt de resultaten voor één werknemer bekijken door op de knop **Resultaten weergeven** te klikken.  
    * U kunt het berekende compensatiebedrag overschrijven door het percentage of het verhogingsbedrag in de velden voor **Aanbeveling** aan te passen.  
6. Voer in het veld **Aanbevolen percentage** een getal in.
7. Zoek en selecteer de gewenste record in de lijst.
8. Voer in het veld **Aanbevolen percentage** een getal in.
    * U kunt Herberekenen gebruiken om eventuele wijzigingen te negeren die op de bestaande record werden toegepast en voor de geselecteerde werknemer een nieuwe compensatieresultaat genereren.  
    * Wanneer alle wijzigingen voor een werknemer zijn voltooid, wijzigt u de status in **Goedgekeurd**.  
9. Klik op **Status wijzigen**.
10. Klik op **Goedgekeurd**.
    * Nadat de record is goedgekeurd, kan deze naar de officiële compensatierecord van de werknemer worden geladen. De nieuwe compensatie is van kracht vanaf de transactiedatum die in het compensatieproces werd ingesteld.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
