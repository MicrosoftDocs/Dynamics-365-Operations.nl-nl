---
title: Uitsteltransacties in Facturering van abonnementen
description: In dit onderwerp worden de verschillende transacties beschreven die in uitsteltransacties kunnen worden gebruikt als onderdeel van uitgestelde opbrengsten en onkosten in Facturering van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2022
ms.locfileid: "8558089"
---
# <a name="deferral-default-transactions"></a>Standaardtransacties voor uitstel

In dit onderwerp worden de transacties beschreven waarmee opbrengsten en onkosten kunnen worden uitgesteld. Uitstelplanningen zijn altijd gebaseerd op en afhankelijk van een oorspronkelijk document of factureringsplanning. Uitstelplanningen worden gemaakt op basis van standaardwaarden en kunnen niet afzonderlijk worden ingevoerd of gemaakt.

## <a name="sales-order-transaction-deferral"></a>Uitstel van verkoopordertransactie

Gebruik de pagina **Uitstel** of **Creditnota maken** om de uitstelparameters voor een verkooporderregel in te voeren of te bewerken.

> [!NOTE]
> Wanneer een verkooporder wordt gemaakt op basis van een factureringsplanning, zijn alle waarden op de pagina **Uitstel** of **Creditnota maken** alleen-lezen en kunnen de uitstelparameters niet worden bewerkt. Gebruik de pagina **Planning wijzigen** om de waarden te bewerken.

### <a name="edit-deferral-options"></a>Opties voor uitstel bewerken

Als u de uitstelopties voor een regel wilt bewerken, gaat u als volgt te werk.

1. Maak een verkoopordertransactie.
2. Selecteer de regel en selecteer vervolgens **Uitstel**.
3. Op de pagina **Transactie-uitstel** moet de optie **Uitgesteld** op **Ja** worden ingesteld. Bewerk zo nodig andere velden.
4. Selecteer **Voorbeeld** om de uitstelplanning te bekijken.
5. Als u wijzigingen hebt aangebracht in de transactie-uitstel, selecteert u **OK** en keert u terug naar de transactiepagina.
6. Voer de transactie door en boek deze.

Als de transactie is geboekt, opent u de pagina **Alle uitstelplanningen** om de uitstelplanning weer te geven.

### <a name="create-a-credit-note"></a>Een creditnota maken

Volg deze stappen om een creditnota te maken.

1. Maak een verkoopordertransactie.
2. Selecteer in het gedeelte **Verkooporderregels** het artikel waarvoor u een creditnota wilt maken.
3. Selecteer **Verkooporderregel** \> **Nieuw** en selecteer **Creditnota**.
4. Selecteer **Uitstel**.
5. Stel op de pagina **Verkoopordertransactie** de optie **Bestaande planning aanpassen** in op **Ja** voor het artikel.
6. Selecteer in het veld **Aangepaste planning** de uitstelplanning waarop u de creditnota wilt toepassen.
7. Werk de velden **Datum opnieuw berekenen** en **Einddatum** naar wens bij.
8. Selecteer **OK**.
9. Voltooi de boeking van de verkoopordertransactie.

### <a name="purchase-orders-and-purchase-invoices"></a>Inkooporders en -facturen

Als u de uitstelfunctionaliteit voor een inkooporder wilt gebruiken, genereert u eerst de factuur. Vervolgens kunt u de pagina **Leveranciersfacturen in behandeling** gebruiken om uitstelartikelen te bewerken of toe te voegen. U kunt uitstel niet rechtstreeks in een inkooporder bewerken of toevoegen.

1. Gebruik de pagina **Leveranciersfacturen in behandeling** om een leveranciersfactuur in te voeren.

    Wanneer u een regel invoert, wordt uitstel automatisch ingesteld voor een artikel of aanschaffingscategorie die u selecteert. Dit uitstel is gebaseerd op de uitstelconfiguratie op de pagina **Standaardinstellingen voor uitstel**. Uitstel kan worden bewerkt of toegevoegd op verdelingsniveau.

3. Selecteer op de inkoopregel **Financiële items \> Bedragen verdelen**.
4. Selecteer **Uitstel** voor elk verdelingsbedrag. Wanneer de factuur wordt geboekt, wordt een uitstelplanning gemaakt voor elke verdeling waarvoor een uitstel is ingesteld.

### <a name="tax"></a>Belastingen

In sommige gevallen kan het belastingbedrag volledig of gedeeltelijk niet terug te vorderen zijn. Als het belastingbedrag van een regel die kan worden uitgesteld een niet terug te vorderen bedrag bevat, wordt het niet terug te vorderen belastingbedrag opgenomen in het uitstelbare planningsbedrag wanneer de factuur wordt geboekt.

### <a name="variance"></a>Variantie

Als het bedrag op de leveranciersfactuurregel afwijkt van het bedrag op de inkooporderregel, worden afwijkingsverdelingen gemaakt. Als de regel wordt uitgesteld, wordt de grootboekrekening voor deze verdelingen ingesteld op de uitstelrekening en worden de bedragen opgenomen in het uitstelbare planningsbedrag wanneer de factuur wordt geboekt. Deze verdelingen krijgen de namen **Prijsafwijking** en **Kostenafwijking**.

### <a name="general-journals-and-invoice-journals"></a>Algemene journalen en factuurjournalen

Gebruik de pagina **Uitstel** om de uitstelparameters in te voeren voor een journaalboekstukregel. U kunt ook een voorbeeld van de uitstelplanning bekijken voor lineaire uitstel. Wanneer u een regel invoert, wordt het uitstel automatisch ingesteld op basis van de instelling van uitstelrekeningen op de pagina **Standaardinstellingen voor uitstellen**. U kunt de uitstelopties handmatig wijzigen voor elke regel. Wanneer het journaalboekstuk wordt geboekt, wordt de uitstelplanning gemaakt.

#### <a name="post-and-transfer"></a>Boeken en overboeken

Gebruik de opdracht **Boeken en overboeken** om het journaalboekstuk te boeken. De uitstelopties volgen de regel waarop het boekstuk van toepassing is. Voor boekstukken zonder fouten wordt een uitstelplanning gemaakt als deze is uitgesteld. Voor een boekstuk met een fout dat wordt overgeboekt, worden ook alle uitstelopties voor overgeboekt.

#### <a name="tax"></a>Belastingen

In sommige gevallen kan het belastingbedrag volledig of gedeeltelijk niet terug te vorderen zijn. Als het belastingbedrag van een regel die kan worden uitgesteld een niet terug te vorderen bedrag bevat, wordt het niet terug te vorderen belastingbedrag opgenomen in het uitstelbare planningsbedrag wanneer de factuur wordt geboekt.

## <a name="free-text-invoice-transaction-deferral"></a>Uitstel van vrije-tekstfactuurtransactie

Gebruik de pagina **Uitstel** om de uitstelparameters in te voeren voor de verdeling van een vrije-tekstfactuurregel. Wanneer een verdeling wordt ingevoerd, wordt het uitstel automatisch ingesteld op basis van de uitstelinstellingen op de pagina **Standaardinstellingen voor uitstellen**.

## <a name="fields"></a>Velden

De pagina **Transactie-uitstel** bevat de volgende velden.

| Veld | Description |
|-------|-------------|
| Uitgesteld | <p>Geef op of de regel een uitstel is:</p><ul><li>**Ja**: de regel is een uitstel.</li><li>**Nee**: de regel is geen uitstel.</li></ul><p>Als deze optie is ingesteld op **Ja**, is de optie **Bestaande planning aanpassen** niet beschikbaar. Voor artikelen en toeslagen die al zijn ingesteld als uitgesteld, is deze optie ingesteld op **Ja**. Voor artikelen en toeslagen die niet standaard zijn ingesteld als uitgesteld, stelt u deze optie in op **Ja**.</p> |
| Bestaande planning aanpassen | <p>Geef op of de regel een correctie van een bestaande uitstelplanning is:</p><ul><li>**Ja**: de nieuwe verkoopregel is een correctie van een bestaande uitstelplanning. In dit geval kunt u een uitstelplanning selecteren in het veld **Aangepaste planning**.</li><li>**Nee**: de nieuwe verkoopregel is geen correctie van een bestaande uitstelplanning.</li></ul><p>Als deze optie is ingesteld op **Ja**, is de optie **Uitgesteld** niet beschikbaar.</p> |
| Aangepaste planning | <p>Selecteer de uitstelplanning die door de regel wordt aangepast. Alle waarden op de pagina worden vervolgens bijgewerkt met de waarden uit de oorspronkelijke uitstelplanning. Deze waarden kunnen niet worden bewerkt.</p><p>Dit veld is alleen beschikbaar als de optie **Bestaande planning aanpassen** is ingesteld op **Ja**.</p> |
| Herberekeningsdatum | <p>Geef de begindatum op van de periode op basis waarvan u het resterende bedrag opnieuw wilt berekenen. De standaarddatum is de datum van de volgende niet-toegerekende periode.</p><p>Dit veld is alleen beschikbaar als de optie **Bestaande planning aanpassen** is ingesteld op **Ja**.</p> |
| Einddatum | <p>Afhankelijk van het type uitstel kan de einddatum al dan niet worden bijgewerkt:</p><ul><li>Geef voor een lineair uitstel de nieuwe einddatum van de planning op. De bestaande einddatum van de uitstelplanning is de standaardwaarde.</li><li>Geef voor een op gebeurtenissen gebaseerd uitstel de einddatum van de creditgebeurtenisregel op. Deze datum mag leeg blijven.</li></ul><p>Dit veld is alleen beschikbaar als de optie **Bestaande planning aanpassen** is ingesteld op **Ja**.</p> |
| Nummer factureringsplanning | <p>Het nummer van de factureringsplanning.</p><p>Dit veld is alleen beschikbaar voor factureringsplanningen voor terugkerende contracten.</p> |
| Correctiemethode voor uitstel | <p>De methode voor uitgestelde correctie. De waarde komt overeen met de waarde op de pagina **Massale beëindigingsverwerking** voor de factureringsplanning voor terugkerende contracten.</p><p>Dit veld is alleen beschikbaar voor factureringsplanningen voor terugkerende contracten.</p> |
| **Rekeningen - Opbrengst** | |
| Uitstelrekening | <p>De uitstelrekening. Dit is de boekingsrekening op de pagina **Verkooporder**.</p><p>Als de regel niet wordt uitgesteld, is dit veld leeg. In dit geval is de boekingsrekening de standaardopbrengstrekening.</p> |
| Rekening voor toerekening | <p>Geef de rekening op die wordt gebruikt wanneer een uitstel wordt toegerekend. Deze rekening moet verschillen van de uitstelrekening.</p><p>Wanneer de optie **Uitgesteld** in eerste instantie is ingesteld op **Ja**, worden de dimensiewaarden in de uitstelrekening gekopieerd naar de toerekeningsrekening. Als de dimensie in de uitstelrekening niet bestaat voor de toerekeningsrekening, wordt deze genegeerd.</p> |
| Rekening voor initiële toerekening | <p>Selecteer de rekening voor de eerste opbrengsttoerekening. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| Tegenrekening voor toerekening | <p>Selecteer de rekening voor de compenserende opbrengsttoerekening. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| **Rekeningen - Korting** | Deze sectie wordt alleen weergegeven voor uitgestelde artikelen. Deze wordt verborgen voor uitgestelde toeslagen. |
| Uitstelrekening | <p>Geef het nummer van de uitstelrekening voor korting op. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Optie voor kortingsuitstel** is ingesteld op **Afzonderlijke planning voor korting** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** en er een korting is toegepast op de regel.</p> |
| Rekening voor toerekening | <p>Geef het nummer van de toerekeningsrekening voor korting op. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Optie voor kortingsuitstel** is ingesteld op **Afzonderlijke planning voor korting** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** en er een korting is toegepast op de regel.</p> |
| Rekening voor initiële toerekening | <p>Selecteer de rekening voor de eerste kortingstoerekening. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** en er een korting is toegepast op de regel.</p> |
| Tegenrekening voor toerekening | <p>Selecteer de rekening voor de compenserende opbrengsttoerekening. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** en er een korting is toegepast op de regel.</p> |
| **Rekeningen - Verbruik** | Deze sectie wordt alleen weergegeven voor uitgestelde artikelen. Deze wordt verborgen voor uitgestelde toeslagen. |
| Uitstelrekening | <p>Geef het nummer van de uitstelrekening voor verbruik op.</p><p>Voor standaardproducten worden twee uitstelplanningen gemaakt:</p><ul><li>**Standaardverkoop**: een opbrengstenplanning met een creditsaldo. Selecteer in dit geval de uitstelrekening voor verbruik.</li><li>**Verbruik**: een onkostenplanning voor verbruik (kosten van verkochte goederen \[COGS\]) met een debetsaldo. Selecteer in dit geval de toerekeningsrekening voor verbruik.</li></ul><p>Wanneer de factuur wordt geboekt, wordt het verbruiksbedrag geboekt naar de opgegeven uitstelrekening voor verbruik. Deze velden zijn niet beschikbaar voor serviceartikelen.</p> |
| Rekening voor toerekening | Geef het nummer van de toerekeningsrekening voor verbruik op. |
| Rekening voor initiële toerekening | <p>Geef de rekening voor het eerste bedrag voor verbruikstoerekening op. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| Tegenrekening voor toerekening | <p>Geef de rekening voor het tegenbedrag voor verbruikstoerekening op. De standaardwaarde komt van de pagina **Standaardinstellingen voor uitstellen**.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Uitgestelde boekingsmethode** is ingesteld op **Winst en verlies** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| **Plannen** | |
| Planningstype | <p>Selecteer het type uitstelplanning: **Lineair** (standaard) of **Op gebeurtenissen gebaseerd**.</p><p>De opties die op de pagina worden weergegeven, zijn gebaseerd op het type uitstelplanning dat u selecteert.</p><p>Als de standaardsjabloon op de pagina **Standaardinstellingen voor uitstellen** is ingesteld voor de transactieregel, wordt het type uitstelplanning gebaseerd op het geselecteerde sjabloontype.</p> |
| **Planning - Lineair** | |
| Eerdere perioden consolideren | <p>Geef op of u uitstelplanningsregels voor eerdere perioden wilt consolideren:</p><ul><li>**Ja**: de uitstelplanningsregels voor eerder perioden worden geconsolideerd.</li><li>**Nee**: de uitstelplanningsregels voor eerder perioden worden niet geconsolideerd.</li></ul><p>De standaardwaarde is afkomstig van de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| Gelijk per periode | <p>Geef op of het aantal dagen in elke periode gelijk moet zijn of per periode moet verschillen:</p><ul><li>**Ja**: elke periode heeft hetzelfde aantal dagen.</li><li>**Nee**: perioden hebben niet hetzelfde aantal dagen.</li></ul><p>Als deze optie is ingesteld op **Nee**, wordt er rekening gehouden met het aantal dagen in een periode wanneer het bedrag in elke periode voor een uitstelplanning wordt berekend.</p><p>De standaardwaarde is afkomstig van de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</p> |
| Planning van sjabloon | <p>Geef op of de uitstelplanning wordt gemaakt op basis van een sjabloon of een einddatum:</p><ul><li>**Ja**: de uitstelplanning wordt gemaakt op basis van een sjabloon.</li><li>**Nee**: de uitstelplanning wordt gemaakt op basis van een einddatum.</li></ul> |
| Sjabloon | Selecteer de uitstelsjabloon. |
| Begindatum overschrijven | <p>Geef op of u de begindatum wilt overschrijven:</p><ul><li>**Ja**: de begindatum wordt overschreven door de datum die u invoert in het veld **Begindatum**.</li><li>**Nee**: de begindatum is de regel **Standaardbegindatum voor uitstel** die wordt toegepast op de factuurdatum die op de pagina **Factuur boeken** is opgegeven. Deze regel kan worden ingesteld op de pagina **Parameters voor uitgestelde opbrengsten en onkosten**.</li></ul> |
| Begindatum voor uitstel | Geef de begindatum van het uitstel op. De transactiedatum is de standaardwaarde. |
| Einddatum van uitstel | <p>De einddatum van het uitstel.</p><p>Deze datum wordt automatisch berekend op basis van de uitstelsjabloon. Als geen sjabloon is geselecteerd, moet u de datum handmatig invoeren.</p> |
| **Planning - Op gebeurtenissen gebaseerd** | |
| Sjabloon | <p>Selecteer de op gebeurtenissen gebaseerde sjabloon. Dit veld is optioneel.</p><p>Als u een sjabloon selecteert, worden alle op gebeurtenissen gebaseerde gegevens en gebeurtenisregels overschreven door de waarden in de sjabloon.</p> |
| Toewijzingstype | <p>Selecteer het toewijzingstype voor de gebeurtenisregels:</p><ul><li>**Variabele bedragen**: een specifiek toewijzingsbedrag wordt ingevoerd voor elke regel.</li><li>**Gelijke bedragen**: het bedrag wordt gelijkmatig verdeeld over alle regels.</li><li>**Percentage**: er wordt een bedrag toegewezen dat is gebaseerd op de percentagewaarde die voor elke regel wordt ingevoerd.</li><li>**Voltooiingspercentage:** voor elke regel wordt een cumulatieve voltooiingswaarde ingevoerd.</li><p>**Variabele hoeveelheid**: voor elke regel wordt een specifieke toewijzingshoeveelheid ingevoerd.</li></ul><p>**Opmerking:** als u **Voltooiingspercentage** wilt selecteren, moeten de datums in oplopende volgorde zijn.</p> |
| **Afzonderlijke gebeurtenissen per eenheid maken** | |
| Description | <p>Geef op of u gebeurtenissen per eenheid wilt scheiden:</p><ul><li>**Ja**: scheid de gebeurtenisregels, zodat er één regel per hoeveelheid wordt gebruikt.<p>Stel dat er drie gebeurtenisregels zijn en voor de factuur een hoeveelheid van vier is ingesteld. In dit geval heeft de resulterende uitstelplanning twaalf regels.</p></li><li>**Nee**: de gebeurtenisregels worden niet gescheiden.</li></ul> |
| Vervalrekening | <p>Selecteer de rekening die wordt gebruikt voor toegerekende verlopen regels. U kunt de rekening selecteren nadat de uitstelplanning is gemaakt.</p><p>Als een vervaldatum is ingesteld voor een gebeurtenis, gaat tijdens het toerekeningsproces het toerekeningsbedrag naar de verlooprekening in plaats van naar de toerekeningsrekening.</p> |
| **Planning - Op gebeurtenissen gebaseerde regels** | |
| Description | Een beschrijving van de gebeurtenis. |
| Einddatum van uitstel | <p>Selecteer de einddatum van de gebeurtenis.</p><p>**Opmerking:** als u een einddatum selecteert, wordt het veld **Vervaldatum** gewist. U kunt niet zowel een einddatum als een vervaldatum gebruiken.</p> |
| Vervaldatum | <p>Selecteer de vervaldatum van de gebeurtenis.</p><p>**Opmerking:** als u een einddatum selecteert, wordt het veld **Vervaldatum** gewist. U kunt niet zowel een einddatum als een vervaldatum gebruiken.</p> |
| Quantity | <p>Geef de toewijzingshoeveelheid op. De standaardwaarde voor alle regels is **0** (nul). Als u de hoeveelheid bijwerkt, moet de totale hoeveelheid van alle regels gelijk aan of kleiner zijn dan de hoeveelheid die is opgegeven voor het regelartikel op de verkooporder.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Toewijzingstype** is ingesteld op **Variabele hoeveelheid**.</p><p>Als de hoeveelheid van het regelartikel op de verkooporder wordt gewijzigd zodat deze kleiner is dan de oorspronkelijke hoeveelheid en de factuur wordt gemaakt, worden er minder regels op basis van gebeurtenissen gemaakt. De totale toegewezen hoeveelheid overschrijdt niet de hoeveelheid die is opgegeven in de oorspronkelijke verkooporder of factureringsplanning.</p> |
| Toewijzingspercentage | <p>Geef het toewijzingspercentage op. Als het veld **Toewijzingstype** is ingesteld op **Percentage** of **Voltooiingspercentage**, kunt u handmatig een percentage invoeren. Anders wordt het automatisch berekend.</p><p>Als het veld **Toewijzingstype** is ingesteld op **Percentage**, moet het totaal van het percentage gelijk zijn aan 100.</p> |
| Bedrag | <p>Geef het toewijzingsbedrag op. Als het veld **Toewijzingstype** is ingesteld op **Variabele bedragen** of **Voltooiingspercentage**, kunt u handmatig een bedrag invoeren.</p><p>Als het veld **Toewijzingstype** is ingesteld op **Voltooiingspercentage** en u hier een bedrag invoert, wordt de waarde van het veld **Voltooiingspercentage** automatisch berekend.</p><p>Vanwege afronding komt het berekende bedrag mogelijk niet exact overeen met wat handmatig is ingevoerd. Als u een exact bedrag nodig hebt, stelt u het veld **Toewijzingstype** in op **Variabele bedragen**.</p> |
| Voltooiingspercentage | <p>Geef het voltooiingspercentage op. De waarde moet tussen 0 en 100 liggen.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Toewijzingstype** is ingesteld op **Voltooiingspercentage**.</p> |
| Voltooiingsbedrag | <p>Het berekende totaal voor alle regels in de uitstelplanning.</p><p>Als het veld **Toewijzingstype** is ingesteld op **Voltooiingspercentage**, kunt u handmatig een bedrag invoeren. In dit geval wordt de waarde van het veld **Voltooiingspercentage** berekend op basis van het bedrag dat u invoert.</p><p>Vanwege afronding komt het berekende bedrag mogelijk niet exact overeen met wat handmatig is ingevoerd.</p><p>Dit veld is alleen beschikbaar wanneer het veld **Toewijzingstype** is ingesteld op **Voltooiingspercentage**.</p> |
| Toerekenen bij boeken | <p>Geef op of de regel automatisch wordt toegerekend zodra de transactie wordt geboekt:</p><ul><li>**Ingeschakeld**: de regel wordt automatisch toegerekend zodra de transactie wordt geboekt.</li><li>**Uitgeschakeld**: de regel wordt niet automatisch toegerekend zodra de transactie wordt geboekt.</li></ul> |
| Rekening voor toerekening | <p>Geef de toerekeningsrekening voor de gebeurtenis op als deze afwijkt van de rekening die wordt gebruikt voor de uitstelplanning.</p><p>U kunt dit veld gebruiken in combinatie met de optie **Toerekenen bij boeken**.</p> |
