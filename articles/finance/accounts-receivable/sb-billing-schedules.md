---
title: Overzicht van factureringsplanning
description: In dit onderwerp wordt uitgelegd hoe u factureringsplanningen maakt, verwijdert en bewerkt.
author: JodiChristiansen
ms.date: 02/09/2022
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
ms.openlocfilehash: e42be3f359e96f0861354ebc8e1e9c87478a5d89
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182681"
---
# <a name="billing-schedule-overview"></a>Overzicht van factureringsplanning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Op de pagina **Factureringsplanning** kunt u factureringsplanningen maken, verwijderen of bewerken. U kunt ook de lijst met factureringsplanningen bekijken. Wanneer u een factureringsplanning maakt, worden de standaardwaarden ervan bepaald door de factureringsgroep die hieraan is gekoppeld. U kunt extra informatie instellen op de pagina **Factureringsparameters voor terugkerende contracten**.

## <a name="create-a-billing-schedule"></a>Een factureringsplanning maken

Voer de volgende stappen uit om een factureringsplanning te maken.

1. Selecteer **Nieuw** op de pagina **Factureringsplanning**.
2. Selecteer een factureringsplanningsgroep in het veld **Factureringsplanningsgroep** in het dialoogvenster **Factureringsplanning** maken.
3. Selecteer een klantrekening in het veld **Klantrekening**.
4. Selecteer in het veld **Begindatum** de begindatum en voer vervolgens in het veld **Aantal perioden** het aantal perioden in. Het veld **Einddatum** wordt bijgewerkt op basis van het aantal perioden dat u hebt ingevoerd. Als u het veld **Einddatum voor facturering** bijwerkt, wordt het veld **Aantal perioden** bijgewerkt naar **0** (nul).
5. Selecteer **OK**.
6. Voer op de pagina **Factureringsplanning** op het tabblad **Algemeen** in het veld **Omschrijving** een omschrijving van de factureringsplanning in.
7. Selecteer in het veld **Mijlpaalsjabloon** een mijlpaalsjabloon voor **Facturering van mijlpalen**.

Velden zoals **Factuurrekening** en **Valutacode** worden bijgewerkt met gegevens van de klant.

De velden **Factureringsfrequentie** en **Factureringsinterval** worden automatisch ingesteld op basis van de geselecteerde factureringsplanningsgroep.

8. Als u afzonderlijke facturen wilt maken, stelt u de optie **Afzonderlijk factureren** in op **Ja**.
9. Als u een factureringsplanning na de laatste factureringsperiode automatisch wilt verlengen, stelt u de optie **Automatisch verlengen** in op **Ja** en stelt u vervolgens het veld **Regels om bij vernieuwing toe te voegen** in.

De velden **Parameters** worden automatisch ingesteld op basis van de waarden op de pagina **Factureringsparameters voor terugkerende contracten**.

10. Als u het bedrag van een factureringsplanning evenredig wilt verdelen, stelt u de optie **Gedeeltelijke perioden evenredig verdelen** in op **Ja**.
11. Als u de detailregels van de factureringsplanning wilt afstemmen op het einde van de maand, stelt u de optie **Uitlijnen met maand** in op **Ja**.
12. Voer in de velden **Begindatum van contract** en **Einddatum van contract** de begin- en einddatums van het contract in. Deze datums dienen uitsluitend ter informatie.

Het veld **Betaling** bevat de betalingsgegevens van de klant. Wanneer een regelartikel is geblokkeerd of beëindigd, kan de betalingsinformatie niet worden gewijzigd.

> [!NOTE]
> Wanneer u facturen consolideert per artikel, moet de waarde van de velden **Betalingsvoorwaarden**, **Methode** en **Factureringsplanning** overeenkomen. Anders kunnen de facturen niet worden geconsolideerd.

13. Op het tabblad **Adres** kunt u de velden **Afleveradres** en **Factuuradres** controleren en bijwerken.
14. Op het tabblad **Contactgegevens** kunt u een eindgebruikersrekening koppelen aan de factureringsplanning.
15. In de velden **Contactgegevens** kunt u een contactpersoon, e-mailadres en internetadres invoeren.
16. Als u partnerprovisiegegevens wilt bijhouden, stelt u de velden **Partnerrekening** en **Provisietarief van partner** in. Deze velden dienen uitsluitend ter informatie.
17. Op het tabblad **Totaal** kunt u de verschillende totalen weergeven die zijn berekend voor de factureringsplanning.
18. Op het tabblad **Blokkering** kunt u controlegegevens bekijken over het moment waarop de factureringsplanning is geblokkeerd.
19. Op het tabblad **Beëindiging** kunt u een geschiedenis weergeven van de beëindigingen die op de factureringsplanning zijn toegepast of uit de factureringsplanning zijn verwijderd.
20. Selecteer **Opslaan**.
21. Selecteer **Regel toevoegen** op het sneltabblad **Factureringsplanningsregels**.
22. Selecteer het artikelnummer in het veld **Artikelnummer**. Als het toegevoegde artikel een bovenliggend artikel is in een opbrengstsplitsing, worden de regels automatisch bijgewerkt met de onderliggende artikelen. U kunt alleen het bovenliggende artikel in een opbrengstsplitsing bewerken. Alle onderliggende artikelen worden vervolgens overeenkomstig bijgewerkt.
23. Selecteer het artikeltype in het veld **Artikeltype**.
24. Werk de begin- en einddatum in.
25. Voordat de facturen worden gemaakt, kunt u de factureringsfrequentie wijzigen door het veld **Factureringsfrequentie** bij te werken. Nadat de eerste factuur voor de factureringsplanning is gemaakt, kan de factureringsfrequentie niet worden gewijzigd.
26. Selecteer de maateenheid voor het artikel in het veld **Eenheid**.
27. Selecteer de prijsmethode voor het artikel in het veld **Prijsbepalingsmethode**.

Het veld **Eenheidsprijs** wordt automatisch ingesteld vanuit de voorraad. U kunt de prijsmethode echter bijwerken als u de prijsmethode wijzigt in **Vast**.

## <a name="remove-a-line-item"></a>Een regelartikel verwijderen

Volg deze stappen om een artikel te verwijderen uit een factureringsplanning.

1. Selecteer op de pagina **Factureringsplanning** in het veld **Planningsnummer** het nummer van de factureringsplanning die u wilt bewerken.
2. Selecteer op het sneltabblad **Factureringsplanningsregels** de regel die u wilt verwijderen en selecteer **Verwijderen**.
3. Selecteer **Opslaan**.

In de rest van dit onderwerp worden de acties en details beschreven die beschikbaar zijn voor regels op het sneltabblad **Factureringsplanningsregels**.

## <a name="billing-schedule-line-actions"></a>Acties voor factureringsplanningsregels

Met de knoppen op het sneltabblad **Factureringsplanningsregels** kunt u acties toepassen op afzonderlijke regels.

| Knop | Description |
|--------|-------------|
| Regel toevoegen | Een regel toevoegen aan de planningsfacturering. |
| Toevoegen vanuit artikelenlijst | Meerdere artikelen aan een factureringsplanning toevoegen door deze te selecteren in een lijst. |
| Wissen | <p>De geselecteerde regel verwijderen uit de factureringsplanning.</p><p>Voor artikelen die deel uitmaken van een opbrengstsplitsing kunt u alleen het bovenliggende artikel verwijderen. Alle gekoppelde onderliggende artikelen worden vervolgens automatisch verwijderd.</p> |
| Factureringsdetails weergeven | De factureringsdetails weergeven. |
| Beëindigen | <p>De geselecteerde regels beëindigen. Deze knop is alleen beschikbaar als de geselecteerde regels de status **Actief** hebben.</p><p>Voor artikelen die deel uitmaken van een opbrengstsplitsing kunt u alleen het bovenliggende artikel beëindigen.</p> |
| Beëindiging verwijderen | <p>De beëindiging verwijderen van de geselecteerde regels. Deze knop is alleen beschikbaar als de geselecteerde regels de status **Beëindigd** hebben.</p><p>Voor artikelen die deel uitmaken van een opbrengstsplitsing kunt u de beëindiging alleen uit het bovenliggende artikel verwijderen.</p> |
| Blokkering plaatsen | <p>De details selecteren voor het in blokkeren van de geselecteerde regel.</p><p>Voor artikelen die deel uitmaken van een opbrengstsplitsing kunt u alleen het bovenliggende artikel blokkeren.</p> |
| Blokkering verwijderen | <p>De blokkering van de geselecteerde regel verwijderen.</p><p>Voor artikelen die deel uitmaken van een opbrengstsplitsing kunt u de blokkering alleen uit het bovenliggende artikel verwijderen.</p> |
| Escalatie en korting | Deze knop is niet beschikbaar voor artikelen die deel uitmaken van een opbrengstsplitsing, behalve voor bovenliggende artikelen waarbij de opbrengstsplitsing gebruikmaakt van de toewijzingsmethode **Nulbedrag**. |
| Uitstel | <p>Uitstelopties voor de geselecteerde regel invoeren.</p><p>Deze knop is niet beschikbaar voor bovenliggende artikelen in een opbrengstsplitsing.</p> |
| Mijlpaaltoewijzing | <p>De mijlpaaltoewijzingsgegevens voor de geselecteerde regel controleren en bijwerken.</p><p>Deze knop is alleen beschikbaar wanneer het regelartikel voor factureringsplanningen een mijlpaalartikel is.</p> |
| Ondersteuning en verlenging | <p>De ondersteunings- en verlengingsgegevens voor de geselecteerde regel controleren en bijwerken.</p><p>Deze knop is alleen beschikbaar wanneer het regelartikel voor factureringsplanningen een ondersteunings- of verlengingsartikel is.</p> |
| Dimensies weergeven | De dimensiekolommen weergeven of verbergen die worden weergegeven in het raster **Factureringsplanningsregels**. |
| Prijs per eenheid berekenen | <p>De eenheidsprijs van het artikel berekenen, zodat de klant het contractbedrag in termijnen kan betalen (bijvoorbeeld dagelijks, maandelijks, kwartaal, halfjaarlijks of jaarlijks). U kunt de contractprijs en de prijsfrequentie selecteren.</p><p>U kunt een audittrail weergeven voor de wijzigingen: de oude contractprijs en -frequentie, de nieuwe contractprijs en -frequentie, de gebruiker die de wijziging heeft aangebracht en de datum en tijd van de wijziging.</p> |
| Afstemmingsdatum | <p>De uitlijningsdatum voor verleningsartikelen opgeven.</p><p>Als u een artikelgroep selecteert in het veld **Artikelgroep**, gebruiken alle artikelen de uitlijningsdatum van het eerste artikel in de artikelgroep in de factureringsplanning. Als het veld **Artikelgroep** leeg is, kunt u een uitlijningsdatum opgeven die moet worden gebruikt voor alle artikelen.</p><p>Deze knop is alleen beschikbaar wanneer het veld **Factureringsfrequentie** is ingesteld op **Jaarlijks**.</p> |
| Niet-gefactureerde opbrengst | <p>Het artikel instellen om de functie voor niet-gefactureerde opbrengst te gebruiken. Vervolgens kunt u de niet-gefactureerde opbrengst en niet-gefactureerde kortingsrekeningen voor het artikel opgeven.</p><p>Deze knop is alleen beschikbaar voor artikelen waarvoor het veld **Artikeltype** is ingesteld op **Standaard**. Deze is niet beschikbaar voor bestaande factureringsplanningen of factureringsplanningsregels waarvoor de factuur al is gemaakt.</p> |
| Onderliggende opbrengstsplitsing toevoegen | <p>Een onderliggend artikel selecteren om aan de verkooporder toe te voegen.</p><p>Deze knop is alleen beschikbaar voor bovenliggende artikelen in een opbrengstsplitsing.</p> |
| Opties voor geavanceerde prijscalculatie | De prijsopties voor een artikel bewerken. |

## <a name="billing-schedule-line-details"></a>Factureringsplanningsregels in details

Wanneer u een regel selecteert op het sneltabblad **Factureringsplanningsregels**, kunt u specifieke details voor die regel weergeven. Deze details zijn verdeeld over verschillende tabbladen.

### <a name="general-tab"></a>Tabblad Algemeen

Op het tabblad **Algemeen** is de volgende informatie beschikbaar.

| Veld of sectie | Description |
|------------------|-------------|
| Gebruik | <p>In deze sectie vindt u de volgende informatie over gebruiksartikelen. Deze bevat de volgende velden:</p><ul><li>**Gebruiks-id**: de id van de meter of het gebruiksartikel.</li><li>**Leesoptie**: de optie voor lezen in gebruik: **Lezen** of **Verbruik**.</li><li>**Geraamd verbruik**: het geraamde verbruik opgeven voor een gebruiksartikel dat perioden heeft waarin de factuur niet is gemaakt. Op de pagina **Factureringsdetails** kunt u de factureringsdetailregels voor het geschatte verbruik bekijken.</li></ul> |
| Externe verwijzingen\* | Deze sectie bevat de velden **Extern** en **Regelnummer**, waar u externe verwijzingsinformatie kunt opgeven. |
| Mijlpaal | <p>In deze sectie vindt u de volgende informatie over mijlpaalartikelen. U vindt hier het veld **Geschatte voltooiingsdatum**, waarin de voltooiingsdatum van het artikel wordt weergegeven.</li></ul> |
| Tekst | Een opmerking voor de regel. De tekst wordt vertaald in de standaardtaal van de klant of rechtspersoon. |
| Artikelengroep | De artikelgroep voor het regelartikel. |
| Afstemmingsdatum | De uitlijningsdatum voor de factureringsplanning. |

\* Wanneer u facturen consolideert per artikel op de pagina **Factuur genereren**, moeten de velden **Externe verwijzing** overeenkomen. Als zelfs maar één teken verschilt, worden de artikelen niet geconsolideerd in de factuur. Er worden geen validatiecontroles uitgevoerd op een van de velden in de sectie **Externe verwijzing** en de waarde in het veld **Regelnummer** moet een positief geheel getal zijn.

### <a name="address-tab"></a>Tabblad Adres

Op het tabblad **Adres** is de volgende informatie beschikbaar.

| Veld | Description |
|-------|-------------|
| Afleveradres | <p>Het afleveradres voor het regelartikel selecteren. Het standaardafleveradres is het primaire afleveradres op het sneltabblad **Adres**.</p><p>Wanneer u het adres wijzigt, kunt u de volgende adresopties selecteren:</p><ul><li>**Adressen**: selecteer een adres voor de huidige klant.</li><li>**In gebruik**: selecteer een adres dat momenteel wordt gebruikt voor de huidige klant.</li><li>**Ander adres**: selecteer een adres voor een klantrecord.</li></ul><p>Voor artikelen die gebruikmaken van opbrengstsplitsing kan alleen het adres van het bovenliggende artikel worden bewerkt. Het adres voor de onderliggende artikelen komt overeen met het adres voor de bovenliggende artikelen en kan niet afzonderlijk worden bewerkt.</p> |
| Factuuradres | <p>Het factuuradres voor het regelartikel selecteren. Het standaardafleveradres is het primaire afleveradres op het sneltabblad **Adres**. U kunt het adres zo nodig wijzigen, op basis van het doel van de beschikbare adressen:</p><ul><li>Als geen van de adressen als doel **Factuur** heeft, is het standaard factuuradres het primaire adres voor de klant, ongeacht het doel.</li><li>Als een of meer adressen als doel **Factuur** hebben, is het standaard factuuradres het adres dat het laatst is ingevoerd.</li><li>Als een of meer van de adressen als doel **Factuur** hebben en een van de factuuradressen is ingesteld als het primaire adres, is het standaard factuuradres het adres met het doel **Factuur** en wordt dit ingesteld als het primaire adres.</li><li>Voor artikelen die gebruikmaken van opbrengstsplitsing kan alleen het adres van het bovenliggende artikel worden bewerkt. Het adres voor de onderliggende artikelen komt overeen met het adres voor de bovenliggende artikelen en kan niet afzonderlijk worden bewerkt.</li></ul> |

### <a name="product-tab"></a>Tabblad Product

Op het tabblad **Product** is de volgende informatie beschikbaar.

| Veld of sectie | Description |
|------------------|-------------|
| Opslagdimensies | <p>In deze sectie wordt de opslaginformatie voor het artikel gegeven. Deze sectie bevat het veld **serienummer** met het serienummer van het artikel.</p><p>Het serienummer wordt gekopieerd uit de oorspronkelijke verkooporder tijdens het ondersteunings- en verlengingsproces. Voor artikelen die gebruikmaken van opbrengstsplitsing wordt het serienummer van het bovenliggende artikel gekopieerd naar alle onderliggende artikelen. Het serienummer wordt gekopieerd als de optie **Serienummer kopiëren** is ingesteld op **Ja** op de pagina **Factureringsparameters voor terugkerende contracten**.</li></ul> |
| Productdimensies | De productdetails van het artikel en de waarden worden automatisch bijgewerkt op basis van de geselecteerde waarde voor **Variantnummer** voor de factureringsplanningsregel. |

### <a name="account-tab"></a>Tabblad Rekeningen

Op het tabblad **Rekeningen** is de volgende informatie beschikbaar.

| Veld | Description |
|-------|-------------|
| Hoofdrekening | De hoofdrekening die op de verkoopregel is gemaakt. De standaardwaarde is afkomstig uit de verkooporder. Dit veld mag leeg blijven. |
| Financiële dimensies van artikel | <p>De standaardwaarden voor financiële dimensies, gebaseerd op de klant- en artikelrecord.</p><p>Voor artikelen die gebruikmaken van opbrengstsplitsing gebruiken de onderliggende artikelen de waarden voor financiële dimensies van de klant- en artikelrecords, zoals eerder beschreven. Als u de waarden voor financiële dimensies van onderliggende artikelen moet bijwerken, kunt u de gegevensentiteit importeren.</p> |

### <a name="renewals-tab"></a>Tabblad Verlenging

Op het tabblad **Verlenging** is de volgende informatie beschikbaar.

| Veld | Description |
|-------|-------------|
| Automatisch vernieuwen | <p>Een waarde die aangeeft of de factureringsplanningsregel automatisch wordt verlengd voor de volgende factureringsperiode:</p><ul><li>**Ja**: de factureringsplanningsregel wordt automatisch verlengd voor de volgende factureringsperiode wanneer u een factuur maakt.</li><li>**Nee**: de factureringsplanningsregel wordt niet automatisch verlengd. U moet de factureringsplanning handmatig verlengen.</li></ul> |
| Regels die per verlenging worden toegevoegd | Het aantal regels dat u wilt toevoegen aan de verlenging van een factureringsplanning. |

Daarnaast zijn de volgende knoppen beschikbaar op het tabblad **Verlenging**.

| Knoop | Description |
|--------|-------------|
| Controle van niet-gefactureerde opbrengstjournaalboeking | Alle wijzigingen weergeven voor artikelen die gebruikmaken van de functie voor niet-gefactureerde opbrengsten. |
| Verlengingstermijn toevoegen | Een verlengingstermijn toevoegen voor het artikel. De begindatum van de nieuwe verlengingstermijn is de volgende datum na de einddatum van de vorige termijn. De velden **Einddatum verlenging**, **Uitgestelde begindatum**, **Uitgestelde einddatum**, **Artikelhoeveelheid** en **Eenheidsprijs** kunnen worden bijgewerkt. |
| Verlengingstermijn wijzigen | <p>Een verlengingstermijn wijzigen. Voor de eerste termijn kunt u de uitgestelde begin- en einddatum wijzigen voordat de eerste journaalboeking wordt gemaakt. Voor de volgende termijnen kan de begindatum niet worden gewijzigd. Dit is altijd de volgende datum na het einde van de vorige termijn.</p><p>Als er een verlengingstermijn bestaat na de termijn die u wijzigt, kunnen de datums van de termijn niet worden gewijzigd. In dit geval kunnen alleen de velden **Hoeveelheid** en **Eenheidsprijs** voor het verlengingsartikel worden bijgewerkt.</p><p>Stel dat er drie termijnen bestaan. <ul><li>De eerste termijn kan niet worden gewijzigd omdat deze al is gestart.</li><li>Voor de tweede termijn kunnen alleen de hoeveelheid en eenheidsprijs worden gewijzigd.</li><li>Voor de derde termijn kunnen alle waarden behalve de begindatum worden gewijzigd. Bovendien kunt u met de optie **Plannen op basis van sjabloon** een uitgestelde planning maken die is gebaseerd op de sjabloon voor het niet-gefactureerde opbrengstartikel. Als deze optie is ingesteld op **Ja**, selecteert u de uitstelsjabloon in het veld **Sjabloon** en wijzigt u waar nodig de uitgestelde begin- en einddatum. Voor volgende verleningstermijnen wordt dezelfde uitstelsjabloon gebruikt. De uitstelsjabloon kan echter worden gewijzigd.</p></li></ul> |

### <a name="termination-tab"></a>Tabblad Beëindiging

Op het tabblad **Beëindiging** is de volgende informatie beschikbaar.

| Veld | Description |
|-------|-------------|
| Ontslagdatum | De datum waarop de factureringsplanningsregel wordt beëindigd. De standaardwaarde komt uit het veld **Datum beëindiging** in de koptekst. U kunt deze waarde zo nodig wijzigen. |
| Beëindigingstype | Het beëindigingstype. De standaardwaarde komt uit het veld **Type beëindiging** in de koptekst. |

### <a name="hold-tab"></a>Tabblad Blokkeren

Als er uitgestelde opbrengsten en onkosten worden gebruikt, wordt de uitsteldatum weergegeven op het tabblad **Blokkeren**.

### <a name="escalation-and-discount-tab"></a>Tabblad Escalatie en korting

Op het tabblad **Escalatie en korting** is de volgende informatie beschikbaar.

| Veld | Description |
|-------|-------------|
| Escalatie | <p>Selecteren of escalaties zijn toegestaan voor de factureringsplanningsregel. Elke escalatieregel uit de koptekst wordt toegepast wanneer de factureringsplanningsregel wordt gemaakt.</p><ul><li>**Ja**: escalaties kunnen op de regel worden toegepast. Wanneer deze optie is geselecteerd, kunt u de escalaties voor de factureringsplanningsregels instellen op de pagina **Escalatie en korting**.</li><li>**Nee**: escalaties kunnen niet op de regel worden toegepast.</li></ul><p>De standaardinstelling is gebaseerd op de geselecteerde **factureringsplanningsgroep**.</p> |

### <a name="price-changes-tab"></a>Tabblad Prijswijzigingen

Voor regels die van **Standaard** in **Vast** worden gewijzigd, bevat het raster op het tabblad **Prijswijzigingen** de volgende kolommen:

- Datum wijzigen
- Gewijzigd door gebruiker
- Standaardprijs
- Vaste prijs
- Prijs bijwerken
