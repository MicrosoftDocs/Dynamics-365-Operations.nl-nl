---
title: Leverancierskortingen
description: Dit onderwerp biedt een overzicht van de meest voorkomende taken die u kunt uitvoeren wanneer u met leverancierskortingen werkt. Met leverancierskortingen kunnen bedrijven hun kortingsprogramma's voor leveranciers beter beheren door taken te automatiseren die vereist zijn om verdiende kortingen te beheren, bij te houden en te claimen.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: 44c8f3ed76698bb4b70d767d9c8881024699552f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203440"
---
# <a name="vendor-rebates"></a>Leverancierskortingen
[!include [banner](../includes/banner.md)]

Met leverancierskortingen kunnen bedrijven hun kortingsprogramma's voor leveranciers beter beheren door taken te automatiseren die vereist zijn om verdiende kortingen te beheren, bij te houden en te claimen.

Dit onderwerp biedt een overzicht van de meest voorkomende taken die u kunt uitvoeren wanneer u met leverancierskortingen werkt. In het overzicht komen de volgende taken aan bod:

- Controleer de gegevens van een kortingsovereenkomst.
- Identificeer orders die in aanmerking voor kortingen en genereer kortingsclaims.
- Controleer claims en keur deze goed.

## <a name="audience-and-purpose"></a>Doelgroep en doel

De informatie in dit onderwerp is bedoeld voor de besluitvormers in ondernemingen, bijvoorbeeld inkoopmanagers, CFO's (Chief Financial Officer) en accountmanagers, die de volgende verantwoordelijkheden hebben:

- Onderhandelen over leveranciersprijzen, kortingen en kortingsovereenkomsten.
- Leiding geven aan medewerkers die kortingsclaims verwerken en betalingen verzamelen.
- Voorraad bestellen tegen de best mogelijke prijzen.

Mensen in deze posities zijn op zoek naar manieren om verschillende doelstellingen te halen. Hieronder vindt u enkele voorbeelden:

- Op flexibele wijze mogelijkheden bieden voor verschillende typen promotieprogramma's voor leveranciers en kortingsvoorwaarden.
- De administratieve last en fouten gerelateerd aan het bewaken van de promotieprestaties en het verwerken van claims verminderen.
- Cashflowprognoses verbeteren door toekomstige tegoeden toe te rekenen.
- Een gekwantificeerde basis voor lopende en toekomstige onderhandelingen met leveranciers over kortingen hebben.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>De gegevens van een kortingsovereenkomst voor een leverancier controleren
Een kortingsovereenkomst voor een leverancier is een record van een contract met een leverancier met de overeengekomen voorwaarden waaronder het bedrijf in aanmerking komt voor een monetaire compensatie als tegenprestatie voor het halen van vooraf gestelde aankoopdoelen. Kortingsovereenkomsten voor leveranciers worden vastgelegd op de pagina **Kortingsovereenkomsten**.

U opent de pagina **Kortingsovereenkomsten van leverancier** door **Inkoopbeheer** &gt; **Leverancierskortingen** &gt; **Kortingsovereenkomsten** te selecteren.

![Inkoopovereenkomst](media/purchase-agreement.PNG)

Op de pagina **Kortingsovereenkomsten van leverancier** kunt u details over de afgesproken voorwaarden van de leveranciersovereenkomst weergeven.

De koptekst van de overeenkomst bevat de algemene voorwaarden op basis waarvan een bedrijf in aanmerking komt voor kortingen. In feite wordt in de koptekst aangegeven dat een leverancier korting geeft wanneer een bepaald product in een bepaalde hoeveelheid wordt gekocht. In de koptekst geeft u ook de optie voor de maateenheid van de korting en het berekeningsdatumtype op.

- Op het tabblad **Algemeen** kunt u in het veld **Maateenheidoptie voor korting** opgeven of een maateenheid een voorwaarde voor de inkooporderregel moet zijn om in aanmerking te komen voor een kortingsclaim. 

    - **Omzetten**: een inkooporderregel komt in aanmerking voor een leverancierskorting volgens de kortingsovereenkomst. U ontvangt een korting, ongeacht de maateenheid die wordt toegepast op de regel.
    - **Exacte overeenkomst**: om in aanmerking te komen voor een korting, moet een inkoopregel de maateenheid bevatten die is opgegeven in de overeenkomst.

- Op het tabblad **Algemeen** selecteert u in het veld **Berekeningsdatumtype** de datum die wordt gebruikt om te bepalen of de inkoop plaatsvindt in de geldigheidsperiode van de kortingsovereenkomst.

    - **Gemaakt**: gebruik de aanmaakdatum van de inkooporder.
    - **Gewenste levering**: gebruik de gevraagde leveringsdatum.

U kunt meer informatie over de kortingsovereenkomst voor leveranciers opgeven in de overeenkomstregels.

- In het veld **Inkopen cumuleren volgens** kunt u de berekening van de kortingsclaim instellen. Het bedrag kan worden ingesteld op basis van een periode (week, maand, jaar, levensduur of een aangepaste periode). Met de waarde **Factuur** wordt aangegeven dat bij elke facturering van een inkooporderregel een kortingsclaim wordt vastgesteld.
- In het veld **Opgehaald uit** kunt u de basis voor de berekening van korting opgeven.

    - **Bruto**: de korting wordt berekend op basis van de brutoprijs van het artikel.
    - **Netto**: de korting wordt berekend op basis van de nettoprijs van het artikel (de prijs nadat andere kortingen zijn toegepast).

- In de velden **Toenamerekening van kortingsprogramma** en **Onkostenrekening van kortingsprogramma** geeft u de rekeningnummers op waarnaar samengevoegde kortingsbedragen worden geboekt in de fase tussen goedkeuring en verwerking.
- Wanneer de optie **Goedkeuring vereist** is ingesteld op **Ja**, moet de kortingsclaim worden goedgekeurd voordat deze kan worden toegerekend of uitbetaald.
- Het veld **Regelafbrekingstype van korting** bevat de basis voor de kortingen.

    - **Hoeveelheid**: de kortingen zijn gebaseerd op volume.
    - **Bedrag**: de kortingen zijn gebaseerd op bedrag.

- Op het sneltabblad **Regels** kunt u zien hoe verschillende hoeveelheidsniveaus kunnen worden ingesteld om verschillende kortingen te verlenen. In de bovenstaande afbeelding wordt bijvoorbeeld in de velden **Vanaf waarde** en **Tot waarde** aangegeven dat een producthoeveelheid tussen 10 en 19 eenheden in aanmerking komt voor een korting van USD 15 per eenheid.

    > [!NOTE]
    > De waarde bij **Vanaf waarde** is inclusief, de waarde bij **Tot waarde** is exclusief. Stel dat het veld **Regelafbrekingstype van korting** is ingesteld op **Hoeveelheid** en u **1** invoert in het veld **Vanaf waarde** en **3** in het veld **Tot waarde**. In dit geval geldt het kortingsbedrag wanneer u een of twee artikelen inkoopt, maar niet wanneer u drie artikelen inkoopt.

- In het veld **Goedkeuringsstatus workflow** wordt met de waarde **Goedgekeurd** aangegeven dat de overeenkomst kan worden toegepast op inkooporders die voldoen aan de voorwaarden van de overeenkomst.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Orders identificeren die in aanmerking voor kortingen en kortingsclaims genereren

Wanneer inkooporders worden geplaatst bij een leverancier waarmee het bedrijf een kortingsovereenkomst heeft afgesloten, identificeert het programma alle toekomstige leveranciersbetalingen. Als de inkooporders in aanmerking komen voor korting, wordt een kortingsclaim voor elke orderregel gegenereerd zodra een inkoopfactuur is geboekt. Dit is een automatisch proces. Later kunt u de verwachte kortingen bekijken en zien wat het effect van deze kortingen is op de kosten en winstmarge van het product.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Gegevens van kortingen weergeven die op basis van de kortingsovereenkomst voor de leverancier worden toegepast op een inkooporderregel
1. Selecteer op de pagina **Inkooporder** een orderregel en selecteer vervolgens **Inkooporderregel** &gt; **Weergeven** &gt; **Prijsgegevens**.
2. Selecteer op de pagina **Prijsgegevens** het sneltabblad **Kortingen**.

De kortingsgegevens worden ook weergegeven in het veld **Leverancierskorting** in de sectie **Margeschatting** van de pagina **Prijsgegevens**.

> [!NOTE]
> Controleer op de pagina **Parameters voor inkoopbeheer** op tabblad **Prijzen** of de optie **Prijsdetails inschakelen** is ingesteld op **Ja**. Als de optie is ingesteld op **Nee**, kunt u de kortingen niet weergeven.

## <a name="review-and-approve-claims"></a>Claims controleren en goedkeuren
Gegenereerde kortingsclaims vertegenwoordigen de toekomstige betalingen die van de leverancier kunnen worden verwacht. Voordat een creditnota wordt verstuurd naar de leverancier, wil de eigenaar van de overeenkomst normaal gesproken de claims controleren en goedkeuren. De status van een claim bepaalt echter of de claim gereed is voor het goedkeuringsproces.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>De status van claims en het effect op het goedkeuringsproces
Wanneer een claim wordt gegenereerd, wordt de status ingesteld op **Te berekenen** als de korting op cumulatieve basis wordt verleend of **Berekend** als de korting wordt verleend per factuur. Als de status van een claim **Te berekenen** is, moet de claim een berekeningsproces doorlopen dat wordt afgehandeld door de functie Cumuleren. Alleen claims met de status **Berekend** kunnen worden opgenomen in het goedkeuringsproces.

> [!NOTE]
> Als de optie **Goedkeuring vereist** voor een kortingsovereenkomst van een leverancier is ingesteld op **Nee**, krijgen gegenereerde claims de status **Goedgekeurd**. De goedkeuring is verplicht voor claims die op cumulatieve basis worden verleend.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Claims goedkeuren en boekingen en factuurgegevens weergeven
Wanneer claims zijn goedgekeurd, kunnen ze worden verwerkt door Leveranciers. Een creditnota (leveranciersfactuur) voor het kortingsbedrag van de claim wordt automatisch gegenereerd. Het krediet kan vervolgens worden toegevoegd aan het saldo van de leverancier en de betaling kan vervolgens worden opgenomen in de normale vereffeningsprocedure.

1. Selecteer **Inkoopbeheer** &gt; **Leverancierskortingen** &gt; **Kortingsclaims** om een kortingsclaim te openen.
2. Sluit de kortingsclaim.
3. Markeer de claim en selecteer **Goedkeuren** in het actievenster.
4. Selecteer in het veld **Leverancier** op de aanvraagpagina de leverancier waarvoor u gemachtigd bent om een korting te ontvangen en selecteer vervolgens **OK**.

    Er wordt een kortingstoenamejournaal voor het bedrag van de claim geboekt. Met deze boeking wordt de rekening voor te ontvangen verzamelde leverancierskortingen gedebiteerd voor het verwachte leverancierskrediet en wordt de tussentijdse rekening voor ontvangen verzamelde leverancierskortingen gecrediteerd voor de verwachte winst.

    ![Bericht](media/message.png)

5. Selecteer de regel in de lijst met kortingen en selecteer in het actievenster de optie **Kortingstransacties** om naar het journaalbatchnummer voor deze kortingstoenameboeking te gaan.

    Om de claims naar het normale crediteurenproces te verplaatsen, moet de crediteurenmedewerker de afhandeling van de kortingsclaim voltooien door de functie Verwerken uit te voeren.

6. Selecteer **Proces** in het actievenster en selecteer vervolgens **Filter**. In het veld **Criteria** voor het veld **Leveranciersrekening** selecteert u de leverancier waarvoor u kortingsclaims wilt verwerken. Vervolgens selecteert u andere relevante filters en vervolgens **OK**.

    De berichtbalken en het feit dat de status is gewijzigd in **Voltooid** wijzen erop dat de volgende gebeurtenissen hebben plaatsgevonden:

    - Met een kortingstoenamejournaalboeking zijn de vorige tussentijdse bedragen op ontvangst- en onkostenrekeningen omgekeerd.
    - Er is een leveranciersfactuur (creditnota) voor het kortingsbedrag gemaakt.

        > [!NOTE]
        > De instelling van de optie **Handmatige factuurboeking** op het tabblad **Kortingsprogramma** van de pagina **Parameters voor inkoopbeheer** bepaalt of een leveranciersfactuur handmatig of automatisch wordt geboekt als onderdeel van de claimverwerking.

    - Wanneer de leveranciersfactuur wordt geboekt, automatisch of handmatig, is de betaalrekening van de leverancier gedebiteerd en de rekening voor ontvangen kortingen en vergoedingen gecrediteerd.

        > [!NOTE] 
        > Het nummer van de rekening voor ontvangen kortingen en vergoedingen wordt opgegeven voor de aanschaffingscategorie die voor de korting wordt gebruikt op de inkoopfactuurregel. De aanschaffingscategorie wordt ingesteld op het tabblad **Kortingsprogramma** van de pagina **Parameters voor inkoopbeheer**.

7. Selecteer de regel in de lijst met kortingen en selecteer in het actievenster de optie **Kortingstransacties** om naar het journaalbatchnummer voor deze kortingstoenameboeking en het nummer van de leveranciersfactuur te gaan.
8. Selecteer de regel voor de leveranciersfactuurtransactie en selecteer **Leveranciersfactuur** in het actievenster. Als de leveranciersfactuur is geboekt, ziet u het factuurjournaal. Anders ziet u de leveranciersfactuur als een leveranciersfactuur in behandeling die handmatig moet worden geboekt.

    Op de factuurregel worden de details van de leveranciersfactuur voor de aanschaffingscategorie **Kortingen en vergoedingen** opgegeven.

9. Op de pagina **Alle leveranciers** selecteert u de leverancier waarvan u een korting ontvangt en selecteer vervolgens **Transacties** in het actievenster. Vind de regel voor de factuur. Het kortingsbedrag is nu toegevoegd aan het leverancierssaldo.

## <a name="summary"></a>Overzicht
Het proces voor het verwerken van leverancierskortingen omvat meerdere, vaak saaie handmatige traceringstaken. Door deze taken te automatiseren, kan de functie voor het beheer van leveringskorting u helpen de volgende processen te doorlopen:

- Nauwkeurige kortingsclaims genereren
- De verwachte te ontvangen en tussentijdse winst boeken in het grootboek
- Het saldo van de leverancier en het inkomstenoverzicht bijwerken met de vergoeding die verschuldigd is
