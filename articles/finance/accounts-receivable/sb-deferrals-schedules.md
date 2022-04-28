---
title: Uitstelplanningen in uitgestelde opbrengsten en onkosten
description: In dit onderwerp worden uitstelplanningen in uitgestelde opbrengsten en onkosten beschreven.
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
ms.openlocfilehash: 953347500f83a4a16f43331b572d2029027a5f59
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2022
ms.locfileid: "8558088"
---
# <a name="deferral-schedules"></a>Uitstelplanningen

Uitstelplanningen worden gemaakt nadat een transactie is geboekt.

U kunt de pagina **Alle uitstelplanningen** of **Actieve uitstelplanningen** gebruiken om de details van een uitstelplanning te bekijken. Welke informatie wordt weergegeven, is afhankelijk van het type uitstelplanning (lineair of op gebeurtenissen gebaseerd) en het transactietype. De informatie omvat de regels van de uitstelplanning en de totaalbedragen voor de uitstelplanning. Gebruik de pagina om de uitstelplanning te wijzigen.

## <a name="recognize-revenue"></a>Opbrengst toerekenen

> [!NOTE]
> - Begin bij stap 1 om opbrengsten voor één uitstelplanning toe te rekenen.
> - Begin bij stap 2 om opbrengsten voor meerdere planningen toe te rekenen.

1. Selecteer op de pagina **Alle uitstelplanningen** in het raster **Planningsregels** de regels die u wilt toerekenen en selecteer vervolgens **Toerekenen**.
2. Stel op de pagina **Verwerking van toerekening** het veld **Toerekeningsactie** in op **Toerekeningsjournaal maken**.
3. Selecteer in het veld **Afsluitdatum** de afsluitdatum. De verwerking omvat alleen regels waarbij de einddatum voor of op de geselecteerde afsluitdatum valt.
4. Selecteer **Filter** en voeg gegevensfilters toe, zodat in de lijst alleen het bereik van records wordt weergegeven dat u wilt.
5. Selecteer **Voorbeeld weergeven** om de regels weer te geven.
6. Selecteer in de lijst met regels de regels die u niet wilt verwerken en selecteer vervolgens **Verwijderen**.
7. Geef op of u de journaalpost voor toerekening wilt samenvatten.
8. In de sectie **Transactiedatum** kunt u de transactiedatum overschrijven met een specifieke datum om de transactie te verwerken. U kunt de transactiedatum voor afgesloten perioden opgeven.
9. Als u de verwerking wilt uitvoeren als onderdeel van een batch, selecteert u **Batch**. Stel in het dialoogvenster **Batchverwerking** de parameters voor de batch in en selecteer **OK** om terug te gaan naar de pagina **Verwerking van toerekening**. De opbrengsttoerekening wordt later verwerkt, wanneer de batch wordt verwerkt.
10. Selecteer **Verwerken**. Als u de transactie niet hebt toevoegen aan een batch, worden alle regels onmiddellijk verwerkt. Anders worden de regels verwerkt wanneer de batch wordt verwerkt.

## <a name="modify-a-schedule"></a>Een planning wijzigen

Voer de volgende stappen uit om een uitstelplanning te wijzigen.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen** en selecteer vervolgens **Boekhouding \> Planning wijzigen**.
2. Bewerk op de pagina **Planning wijzigen** de opties die u wilt wijzigen. U kunt niet alle opties bewerken, afhankelijk van de uitstelplanning.
3. Selecteer **Voorbeeld** om de wijzigingen in de uitstelplanning te bekijken.
4. Selecteer **OK**.

### <a name="straight-line-deferral-schedules"></a>Lineaire uitstelplanningen

Als de uitstelplanning geen toegerekende of extern geboekte regels bevat, kunt u de hele uitstelplanning wijzigen, inclusief de begindatum.

Als de uitstelplanning toegerekende of extern geboekte regels bevat en u de uitstelplanning wijzigt, is het resulterende gedrag van de uitstelplanning afhankelijk van de herberekeningsdatum en de einddatum voor uitstel van toegerekende regels. De einddatum voor uitstel wordt standaard bepaald door de eerste periode die niet is toegerekend.

Als u de datum van toerekening wilt gebruiken, selecteert u een van de volgende waarden in het veld **Begin van planning**: 
- **Inlopen**: het bedrag nadat alle toegerekende regels opnieuw zijn berekend.
- **Omkering** : alle regels na de herberekeningsdatum worden teruggeboekt op basis van de opgegeven journaalnaam en boekingsdatum. Het bedrag na de herberekeningsdatum wordt vervolgens opnieuw berekend.

Als een sjabloon wordt gebruikt, worden de overgeslagen perioden genegeerd en wordt de sjabloon alleen gebruikt om de einddatum te berekenen.

### <a name="event-based-deferral-schedules"></a>Op gebeurtenissen gebaseerde uitstelplanningen

Voor een op gebeurtenissen gebaseerde uitstelplanning kunt u alle niet-toegerekende regels wijzigen.

Als de uitstelplanning toegerekende of extern geboekte regels bevat, kunt u de sjabloon en het toewijzingstype voor de uitstelplanning niet wijzigen. Wanneer u een bestaande uitstelplanning wijzigt, kunt u de waarde van het veld **Afzonderlijke gebeurtenissen per eenheid maken** niet wijzigen.

Als een regel wordt toegerekend of extern wordt geboekt, wordt het selectievakje **Toegerekend** ingeschakeld.

## <a name="modify-a-deferral-or-recognition-account"></a>Een uitstel- of toerekeningsrekening wijzigen

Volg deze stappen om de uitstel- of toerekeningsrekening voor een uitstelplanning te wijzigen.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen** en selecteer vervolgens **Boekhouding \> Rekening wijzigen**.
2. Selecteer op de pagina **Rekening wijzigen** de rekening die u wilt wijzigen (uitstel, korte termijn of toerekening).
3. Selecteer de nieuwe rekening in het veld **Nieuwe rekening**.
4. Geef op of er bij wijzigingen in de rekening correctiejournaalboekingen moeten worden gemaakt.
5. Als u de optie op **Ja** heb ingesteld in de vorige stap, selecteert u de journaalnaam in het veld **Journaalnaam** en geeft u de transactiedatum op in het veld **Transactiedatum**.
6. Selecteer **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Een uitstelplanning blokkeren

Voer de volgende stappen uit om een uitstelplanning te blokkeren.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen** en selecteer vervolgens **Blokkeren \> Blokkering plaatsen**.
2. Geef op de pagina **Blokkering plaatsen** op of u het saldo van de uitstelrekening of de blokkeerrekening wilt overboeken.
3. Als u ervoor hebt gekozen het saldo over te boeken, selecteert u de journaalnaam in het veld **Journaalnaam**, selecteert u de geblokkeerde rekening in het veld **Rekening geblokkeerd** en geeft u de transactiedatum op in het veld **Transactiedatum**.
4. Selecteer **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Een blokkering verwijderen uit een uitstelplanning

Volg deze stappen om een uitstelplanning te verwijderen uit een blokkering.

1. Selecteer de uitstelplanning in de lijst **Alle uitstelplanningen** en selecteer vervolgens **Blokkeren \> Blokkering verwijderen**.
2. Selecteer de journaalnaam in het veld **Journaalnaam**.
3. Voer in het veld **Transactiedatum** de transactiedatum in.
4. Selecteer **OK**.

## <a name="cancel-unrecognized-amounts"></a>Niet-toegerekende bedragen annuleren

> [!NOTE]
> De regels die al zijn toegerekend of extern zijn geboekt, worden van dit proces uitgesloten.

Voer de volgende stappen uit om niet-toegerekende bedragen in een uitstelplanning te annuleren.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen** en selecteer vervolgens **Annuleren \> Niet-toegerekende bedragen**.
2. Geef op de pagina **Niet-toegerekend bedrag** op of u annuleringsposten wilt maken.
3. Als u ervoor hebt gekozen annuleringsposten te maken, selecteert u de journaalnaam in het veld **Journaalnaam**, selecteert u de annuleringsrekening in het veld **Annuleringsrekening** en geeft u de transactiedatum op in het veld **Transactiedatum**.
4. Selecteer **OK**.

## <a name="cancel-a-completed-schedule"></a>Een voltooide planning annuleren

Gebruik de pagina **Alle uitstelplanningen** om de toegerekende of extern geboekte bedragen om te keren en de uitstelplanning te annuleren om verdere toerekening te voorkomen.

Voer de volgende stappen uit om een hele uitstelplanning te annuleren.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen** en selecteer vervolgens **Annuleren \> Volledige planning**.
2. Geef op de pagina **Volledige planning annuleren** op of u annuleringsposten wilt maken.
3. Als u ervoor hebt gekozen annuleringsposten te maken, selecteert u de journaalnaam in het veld **Journaalnaam**, selecteert u de rekening in het veld **Annuleringsrekening** en geeft u de transactiedatum op in het veld **Transactiedatum**.
4. Selecteer **OK**.

## <a name="reverse-transactions"></a>Transacties terugboeken

> [!NOTE]
> - Begin bij stap 1 om opbrengsterkenning voor één uitstelplanning om te keren.
> - Begin bij stap 2 om opbrengsterkenning voor meerdere planningen om te keren.

1. Selecteer op de pagina **Alle uitstelplanningen** in het raster **Planningsregels** de regels waarvoor u de toerekening ongedaan wilt maken en selecteer vervolgens **Omkeren**.
2. Stel op de pagina **Verwerking van toerekening** het veld **Toerekeningsactie** in op **Toerekeningsjournaal omkeren**.
3. Selecteer in het veld **Afsluitdatum** de afsluitdatum. De verwerking omvat alleen regels waarbij de einddatum voor of op de opgegeven afsluitdatum valt.
4. Selecteer **Filter** en voeg gegevensfilters toe, zodat in de lijst alleen het bereik van records wordt weergegeven dat u wilt.
5. Selecteer **Voorbeeld weergeven** om de regels weer te geven.
6. Selecteer in de lijst met regels de regels die u niet wilt verwerken en selecteer vervolgens **Verwijderen**.
7. De velden **Naam** en **Beschrijving** worden automatisch bijgewerkt met de standaardjournaalnaam en -beschrijving. U kunt deze waarden zo nodig wijzigen. U kunt ook opgeven of u de journaalpost voor toerekening wilt samenvatten.
8. In de sectie **Transactiedatum** kunt u de transactiedatum overschrijven met een specifieke datum om de transactie te verwerken. U kunt de transactiedatum voor afgesloten perioden opgeven.
9. Als u de verwerking wilt uitvoeren als onderdeel van een batch, selecteert u **Batch**. Stel in het dialoogvenster **Batchverwerking** de parameters voor de batch in en selecteer **OK** om terug te gaan naar de pagina **Verwerking van toerekening**. De omgekeerde opbrengsttoerekening wordt later verwerkt, wanneer de batch wordt verwerkt.
10. Selecteer **OK**. Als u de transactie niet hebt toevoegen aan een batch, worden alle regels onmiddellijk verwerkt. Anders worden de regels verwerkt wanneer de batch wordt verwerkt.

## <a name="apply-or-unapply-a-credit-note"></a>Een creditnota toepassen of afkeuren

Volg deze stappen om een creditnota toe te passen.

> [!NOTE]
> Wanneer u een creditnota maakt op de pagina **Uitstel van verkoopordertransactie** en de optie **Bestaande planning aanpassen** op **Ja** instelt, wordt de creditnota automatisch toegepast op de planning wanneer de creditnota wordt geboekt.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen**.
2. Selecteer in de lijst **Creditcorrecties** een regel en vervolgens **Toepassen**.
3. Geef op de pagina **Creditnota toepassen (uitstel)** de herberekeningsdatum op in het veld **Herberekeningsdatum** en de einddatum in het veld **Einddatum**.
4. Selecteer in de lijst **Header** de **verkooporder** met creditnota's.
5. Selecteer de regel in de lijst **Regels**.
6. Selecteer **OK**.
7. Selecteer **Ja**.

> [!NOTE]
> Als u een creditnota wilt toepassen op verschillende afzonderlijke artikelen uit verschillende facturen, moet u deze stappen herhalen.

Volg deze stappen om de toepassing van een creditnota ongedaan te maken.

1. Selecteer de uitstelplanning op de pagina **Alle uitstelplanningen**.
2. Selecteer in de lijst **Creditcorrecties** de factuur en vervolgens **Toepassing ongedaan maken**.
3. Selecteer **Ja**.

## <a name="fields"></a>Velden

De pagina **Alle uitstelplanningen** bevat de volgende velden.

| Velden | Description |
|--------|-------------|
| **Koptekst** | |
| **Plannen** | |
| Toewijzingstype | Het toewijzingstype, voor op gebeurtenissen gebaseerde uitstel: **Percentage** of **Bedrag**. |
| Datum nieuwe classificatie | <p>De meest recente datum waarop de herclassificatie op korte termijn voor een uitstelplanning is verwerkt. Deze datum wordt bijgewerkt wanneer de **herclassificatie op korte termijn** wordt gebruikt voor de uitstelplanning.</p>Dit veld is alleen beschikbaar wanneer de uitstelmethode Vast jaar voor de korte termijn wordt gebruikt. |
| **Rekening** | |
| Uitstelrekening | De rekening die wordt gebruikt voor het uitstelbedrag. |
| Rekening voor toerekening | De rekening die wordt gebruikt voor het toerekeningsbedrag. |
| Toerekeningstype | Het toerekeningstype. |
| Distributietype | Het distributietype. |
| **Transactie** | |
| Aanmaakbron | De bron op basis waarvan de transactie is gemaakt. |
| Transactietype | Het transactietype. |
| Verkooporder | Het verkoopordernummer. |
| Factuur | Het factuurnummer. |
| Item | Het artikelnummer. |
| **Factureringsplanning** | |
| Nummer factureringsplanning | Het nummer van de bijbehorende factureringsplanning. |
| Status factureringsregel | De status van het bijbehorende regelartikel in de factureringsplanning. |
| Externe verwijzingen | Informatie over externe verwijzingen vanuit de factureringsplanning: **Extern** en **Regelnummer**. |
| Totalen | <p>Totaalbedragen voor de uitstelplanning:</p><ul><li>**Lange termijn**: de som van de langlopende uitgestelde bedragen. Deze waarde is alleen beschikbaar wanneer het veld **Uitstelmethode korte termijn** is ingesteld op **Geen** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** of als het kortetermijnbedrag meer dan 0 (nul) is.</li><li>**Korte termijn**: de som van de kortlopende uitgestelde bedragen. Deze waarde is alleen beschikbaar wanneer het veld **Uitstelmethode korte termijn** is ingesteld op **Geen** op de pagina **Parameters voor uitgestelde opbrengsten en onkosten** of als het kortetermijnbedrag meer dan 0 (nul) is.</li><li>**Niet-toegerekend**: de som van niet-toegerekende bedragen voor alle regels.</li><li>**Stub**: de som van extern geboekte bedragen voor alle regels.</li><li>**Toegerekend**: de som van toegerekende bedragen voor alle regels.</li><li>**Extern geboekt en toegerekend**: de som van extern geboekte en toegerekende bedragen voor alle regels.</li><li>**Totaalbedrag**: de som van bedragen voor alle regels.</li></ul> |
| **Planningsregels** | |
| Regel | Het artikelreeksnummer. |
| Begindatum voor uitstel | De begindatum van de uitstelplanning. |
| Einddatum van uitstel | De einddatum van de uitstelplanning. |
| Bedrag | Het uitstelbedrag. |
| Extern geboekt | Een waarde die aangeeft of de regel extern is geboekt. |
| Toegerekend | Een waarde die aangeeft of de regel is toegerekend. |
| Batchnummer journaal | Het batchnummer waarin het bedrag is toegerekend. |
| Gebeurtenisbeschrijving | Een beschrijving van de gebeurtenis. Dit veld is alleen beschikbaar voor uitstelplanningen op basis van gebeurtenissen. |
| **Correcties krediet** | |
| Factuur | <p>Het factuurnummer.</p><p>De waarde geeft de factuur aan voor de creditnotacorrectie die al is toegepast op de uitstelplanning.</p> |
| Toegepast bedrag | Het bedrag van de creditcorrectie die al is toegepast op de uitstelplanning. |
| Toegepaste datum | De datum waarop de creditcorrectie is toegepast. |
| **Correctie** | De correctiewaarden worden alleen weergegeven als een creditnota is verwerkt voor de uitstelplanning. Als er geen creditnota is verwerkt, worden deze waarden verborgen. |
| Correctiebedrag | Het totale correctiebedrag, berekend als *Oorspronkelijk bedrag* – *Gepland bedrag*. |
| Oorspronkelijke einddatum | De oorspronkelijke einddatum van de uitstelplanning. |
| Oorspronkelijk planningsbedrag | Het totaal van de oorspronkelijke uitstelplanning. |
