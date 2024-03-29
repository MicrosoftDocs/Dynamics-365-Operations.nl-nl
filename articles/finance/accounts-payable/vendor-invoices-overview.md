---
title: Overzicht van leveranciersfacturen
description: Dit artikel geeft algemene informatie over het leveranciersfacturen.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 565e45a1c396b9144b4a6437056a0040b2fbde1d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228746"
---
# <a name="vendor-invoices-overview"></a>Overzicht van Leveranciersfacturen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Dit artikel geeft algemene informatie over het leveranciersfacturen. Leveranciersfacturen zijn betalingsverzoeken voor producten en services. Leveranciersfacturen kunnen een rekening voor lopende services voorstellen of kunnen zijn gebaseerd op inkooporders voor specifieke artikelen en services.

## <a name="vendor-invoices"></a>Leveranciersfacturen

Een leveranciersfactuur op basis van een inkooporder wordt gegenereerd wanneer producten of services worden ontvangen op basis van een inkooporder die bij een leverancier is geplaatst. De leveranciersfactuur bevat een koptekst en één of meer regels voor artikelen of services. Een leveranciersfactuur voltooit de cyclus die loopt van inkooporder via productontvangstbon tot leveranciersfactuur.

Hoewel sommige leveranciersfacturen aan een inkooporder zijn gekoppeld, kunnen leveranciersfacturen ook regels bevatten die niet overeenkomen met inkooporderregels. U kunt ook leveranciersfacturen maken die niet aan inkooporders zijn gekoppeld. Deze leveranciersfacturen kunnen voor lopende services staan, zoals een rekening van een energiebedrijf. U hoeft niet naar een inkooporder te verwijzen wanneer u deze toevoegt.

Er zijn verschillende manieren om een leveranciersfactuur op te geven:

- Via het leveranciersfactuurregister kunt u snel facturen invoeren die niet naar een inkooporder verwijzen, zodat u de onkosten kunt samenvoegen. Door het goedkeuringsjournaal voor leveranciersfacturen te gebruiken, kunt u deze facturen selecteren en naar het leveranciersaldo boeken om de transitorische bedragen terug te boeken.
- Met het leveranciersfactuurjournaal kunt u in één stap snel facturen invoeren die niet naar een inkooporder verwijzen.
- In combinatie met de pool van leveranciersfacturen kunt u met het leveranciersfactuurregister snel facturen invoeren om onkosten samen te voegen. U kunt de bijbehorende inkooporders later openen om de factuur voor de onkostenrekening te boeken.
- Op de pagina's **Openstaande leveranciersfacturen** en **Leveranciersfacturen in behandeling** kunt u leveranciersfacturen maken van bevestigde inkooporders.

De volgende discussie biedt meer informatie over het gebruik van de pagina **Openstaande leveranciersfacturen** of **Leveranciersfacturen in behandeling** om een leveranciersfactuur van een inkooporder te maken.

## <a name="understanding-invoice-line-quantities"></a>Factuurregelhoeveelheden begrijpen

Wanneer u een leveranciersfactuur opent vanuit een gerelateerde inkooporder, worden factuurregels gemaakt op basis van de inkooporder. Standaard worden de hoeveelheden gebaseerd op de hoeveelheid van de productontvangstbon. U kunt echter de volgende standaardgedragingen gebruiken:

- **Hoeveelheid nu ontvangen** - Gebruik deze optie voor gedeeltelijke zendingen. De standaardwaarde in het veld **Hoeveelheid** wordt ingesteld op de hoeveelheid uit het veld **Nu ontvangen** in de inkooporder.
- **Bestelde hoeveelheid** - Gebruik deze optie voor volledige zendingen. De standaardwaarde in het veld **Hoeveelheid** wordt ingesteld op de hoeveelheid in het veld **Besteld** in de inkooporder.
- **Geregistreerde hoeveelheid** - Gebruik deze optie als het artikel moet worden geregistreerd, zoals opgegeven op de pagina **Artikelmodelgroepen**. De standaardwaarde in het veld **Hoeveelheid** is de fysieke updatehoeveelheid die is geregistreerd.
- **Hoeveelheid productontvangstbon** – Gebruik deze optie als al een productontvangstbon voor de order is ontvangen. De standaardwaarde in het veld **Hoeveelheid** is de totale hoeveelheid aan beschikbare productontvangstbonnen.
- **Geregistreerde hoeveelheid en services** – Gebruik deze optie als hoeveelheden in aankomstjournalen zijn geregistreerd voor artikelen in voorraad of artikelen die niet in voorraad zijn opgeslagen. Deze optie omvat ook al dan niet geregistreerde services.

Als uw rechtspersoon factuurvereffening gebruikt, kunt u de resultaten van de hoeveelheidsvereffening in de kolom **Overeenkomst van hoeveelheid van productontvangstbon** bekijken. U kunt ook de knop **Overeenkomende gegevens** op het tabblad **Controleren** van het actievenster gebruiken om de resultaten van de hoeveelheidsvereffening te bekijken.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Een regel toevoegen die niet bestaat in de inkooporder

U kunt aan de leveranciersfactuur een regel toevoegen die niet in de inkooporder is opgenomen. U moet een artikelnummer of een aanschaffingscategorie selecteren. Vervolgens kunt u hoeveelheden, prijzen en bedragen aan de regel toevoegen. De regel wordt alleen in overeenstemmingsbeleid voor factuurtotalen opgenomen.

## <a name="submitting-a-vendor-invoice-for-review"></a>Een leveranciersfactuur ter beoordeling indienen

Uw organisatie gebruikt mogelijke workflows om het controleproces voor leveranciersfacturen te beheren. Workflowcontrole kan vereist zijn voor de factuurkoptekst, de factuurregel of voor beide. De besturingselementen voor de workflow zijn van toepassing op de koptekst of op de regel, afhankelijk van waar de focus zich bevindt als u het besturingselement selecteert. In plaats van de knop **Boeken** wordt met de knop **Verzenden** de leveranciersfactuur door het controleproces verzonden.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Voorkomen dat een factuur wordt ingediend bij de workflow 

U kunt op de volgende manieren voorkomen dat een factuur wordt ingediend bij een workflow.

- **Het factuurtotaal en het geregistreerde totaal komen niet overeen.** De gebruiker die de factuur heeft ingediend, ontvangt een waarschuwing dat de totalen niet gelijk zijn. Deze waarschuwing geeft de gebruiker de mogelijkheid om de saldi te corrigeren alvorens de factuur opnieuw in te dienen bij het workflowsysteem. Deze functie is beschikbaar als de parameter **Indienen bij werkstroom verhinderen wanneer het factuurtotaal en geregistreerd factuurtotaal niet gelijk zijn** op de pagina **Feature Management** en de parameter **Werkstroomoptie wanneer factuur en geregistreerd totaal niet gelijk zijn** op de pagina **Parameters van module Leveranciers** zijn ingeschakeld. 
- **Factuur bevat niet-toegewezen toeslagen.** De gebruiker die de factuur heeft ingediend, ontvangt een waarschuwing dat de factuur niet-toegewezen toeslagen bevat. Op deze manier kan de gebruiker de factuur corrigeren voordat deze opnieuw bij het workflowsysteem wordt aangeboden. Deze functie is beschikbaar als de parameter **Indienen bij werkstroom niet toestaan als een leveranciersfactuur niet-toegewezen toeslagen bevat** op de pagina **Functiebeheer** en de parameter **Werkstroomoptie wanneer er niet-toegewezen toeslagen bestaan** op de pagina **Parameters van module Leveranciers** zijn ingeschakeld.
- **Factuur bevat hetzelfde factuurnummer als een andere geboekte factuur.** De gebruiker die de factuur heeft ingediend, ontvangt een waarschuwing dat er een factuur met een dubbel nummer is gevonden. De gebruiker kan het dubbele nummer corrigeren voordat de factuur opnieuw bij het workflowsysteem wordt aangeboden. De waarschuwing wordt getoond als de parameter **Gebruikt factuurnummer controleren** in Leveranciers is ingesteld op **Duplicatie afwijzen**. Deze functie is beschikbaar als de parameter **Indiening bij workflow voorkomen als het factuurnummer al bestaat op een geboekte factuur en het systeem dubbele factuurnummers niet toestaat** op de pagina **Functiebeheer** is ingeschakeld.
- **De factuur bevat een regel waarop de factuurhoeveelheid kleiner is dan de gematchte hoeveelheid op de productontvangstbon.** De gebruiker die de factuur indient of probeert te posten, ontvangt een bericht dat de hoeveelheden niet gelijk zijn. Dit bericht geeft de gebruiker de mogelijkheid om de waarden te corrigeren alvorens de factuur opnieuw in te dienen bij het workflowsysteem. Deze functie is beschikbaar als de parameter **Boeken en verzenden van leveranciersfacturen naar workflow blokkeren** op de pagina **Functiebeheer** en de parameter **Boeken en verzenden indienen bij workflow blokkeren** op de pagina **Parameters van module Leveranciers** zijn ingeschakeld.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Leveranciersfacturen vereffenen met productontvangstbonnen

U kunt gegevens voor leveranciersfacturen invoeren en opslaan en u kunt factuurregels vergelijken met productontvangstbonregels. U kunt ook gedeeltelijke hoeveelheden voor een regel vergelijken.

U kunt een leveranciersfactuur maken op basis van de artikelen op de productontvangstbonregel die tot op heden zijn ontvangen, zelfs als nog niet alle artikelen voor een bepaalde inkooporder zijn ontvangen. U kunt dit bijvoorbeeld doen als een leverancier één factuur per maand stuurt die alle leveringen dekt die de leverancier in die maand verzendt. Elke productontvangstbon staat voor een gedeeltelijke of volledige levering van de artikelen op de inkooporder.

Wanneer een factuur zich in de workflow bevindt, kan de fiatteur factuurhoeveelheden bijwerken zodat deze overeenkomen met de waarde in het veld **Te matchen hoeveelheid productontvangstbonnen**. Selecteer om dit te doen **De factuurhoeveelheden bijwerken om deze af te stemmen op de hoeveelheden van de productontvangsten in de werkstroom** in de werkruimte **Functiebeheer** en selecteer **Inschakelen**. Als een fiatteur in het werkstroomproces alle overeenkomsten heeft verwijderd uit alle productontvangsten van de factuurregel, wordt de factuurregel verwijderd. Wanneer deze functie niet is ingeschakeld, worden factuurhoeveelheden niet bijgewerkt voor facturen in workflows.

Wanneer u de factuur boekt, wordt de hoeveelheid bij **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de ontvangen hoeveelheden van de geselecteerde productontvangstbonnen. Als de hoeveelheid voor **Resterend gedeelte van factuur** en de hoeveelheid voor **Nog te leveren** voor alle artikelen op de inkooporder 0 (nul) zijn, wordt de status van de inkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid voor **Resterend gedeelte van factuur** niet gelijk is aan 0 (nul), blijft de status van de inkooporder ongewijzigd en kunnen hiervoor extra facturen worden ingevoerd.

Bij deze optie wordt ervan uitgegaan dat er minimaal één productontvangstbon is geboekt voor de inkooporder. De leveranciersfactuur is gebaseerd op deze productontvangstbonnen en hieruit worden de hoeveelheden overgenomen. De financiële gegevens voor de factuur zijn gebaseerd op de gegevens die worden ingevoerd wanneer u de factuur boekt.

Zie [Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md) voor meer informatie.

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Een geautomatiseerde taak voor de workflow voor leveranciersfacturen configureren om de leveranciersfactuur te boeken met een batchtaak

U kunt een geautomatiseerde boekingstaak toevoegen aan de workflow Leveranciersfactuur, zodat facturen in een batch worden verwerkt. Als u facturen in een batch boekt, wordt het workflowproces voortgezet zonder dat u hoeft te wachten tot de boeking is voltooid. Hierdoor worden de algehele prestaties verbeterd van alle taken die bij de workflow worden ingediend.

Als u een leveranciersfactuur in een batch wilt boeken, schakelt u op de pagina **Functiebeheer** de parameter **Leveranciersfacturen in batch boeken** in. Leveranciersfactuurworkflows worden geconfigureerd via **Leveranciers > Instellingen > Leveranciersworkflows**.

U kunt de taak **De leveranciersfactuur boeken met een batch** in de workfloweditor zien, ongeacht of de functieparameter **Leveranciers in batch boeken** is ingeschakeld. Als de functieparameter niet is ingeschakeld, wordt een factuur met de taak **De leveranciersfactuur boeken met een batch** pas verwerkt in de workflow als de parameter is ingeschakeld. De taak **De leveranciersfactuur boeken met een batch** moet niet worden gebruikt in dezelfde workflow als de geautomatiseerde taak **Leveranciersfacturen boeken**. Bovendien moet de taak **De leveranciersfactuur boeken met een batch** het laatste element in de workflowconfiguratie zijn.

U kunt het aantal facturen opgeven dat in de batch moet worden opgenomen en het aantal uren dat moet worden gewacht voordat een batch opnieuw wordt gepland. Ga hiervoor naar **Leveranciers > Instellingen > Leveranciersparameters > Factuur > Factuurworkflow**. 

## <a name="working-with-multiple-invoices"></a>Werken met meerdere facturen

U kunt met meerdere facturen tegelijkertijd werken en ze allemaal op hetzelfde moment boeken. Als u meerdere facturen moet maken, gebruikt u de pagina **Leveranciersfacturen in behandeling**. Als u meerdere leveranciersfacturen moet boeken en afdrukken, gebruikt u het **Factuurgoedkeuringsjournaal**. Als u het **Factuurgoedkeuringsjournaal** gebruikt, moet er minimaal één productontvangstbon worden geboekt voor de inkooporder en moet er een factuur voor de inkooporder worden geboekt in een facturenregister. De financiële gegevens voor de factuur komen uit de factuur die is geboekt in het register.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Leveranciersfacturen herstellen die worden gebruikt

Wanneer een leveranciersfactuur wordt gebruikt, kan deze niet worden bewerkt door een andere gebruiker. De status van een factuur kan echter soms aangeven dat de factuur wordt gebruikt, zelfs als deze niet actief wordt bewerkt. De toepassing reageert mogelijk niet meer tijdens de bewerking van de factuur, of een gebruiker kan per ongeluk de factuur open hebben gelaten in de toepassing.

U kunt de pagina **Leveranciersfacturen herstellen** gebruiken om leveranciersfacturen die voor meer dan vier uur in gebruik waren, te herstellen of vrij te geven zodat ze kunnen worden bewerkt. U kunt deze pagina openen via de navigatie of tegel **Periodieke taak** in het werkgebied **Leveranciersfactuurregistratie**. Nadat een factuur is hersteld, kan deze worden bewerkt op de pagina **Leveranciersfactuur**.

U kunt toegang krijgen tot de pagina **Leveranciersfacturen herstellen** als de beveiligingsfunctie en -bevoegdheid **Leveranciersfacturen in gebruik herstellen** aan u zijn toegewezen. Bovendien moet de parameter **Herstellen van leveranciersfactuur toestaan** op de pagina **Leveranciersparameters** worden ingeschakeld.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>De workflowstatus voor leveranciersfacturen van Onherstelbaar wijzigen in Concept

Een workflowexemplaar dat is gestopt vanwege een onherstelbare fout, heeft een workflowstatus **Onherstelbaar**. Wanneer de status van een werkstroom voor leveranciersfacturen **Onherstelbaar** is, kunt u deze weer instellen op **Concept** door **Intrekken** te selecteren. Vervolgens kunt u de leveranciersfactuur bewerken. Deze functie is beschikbaar als de parameter **De workflowstatus voor leveranciersfacturen van Onherstelbaar wijzigen in Concept** op de pagina **Functiebeheer** is ingeschakeld.

U kunt de pagina **Workflowhistorie** voor leveranciersfacturen gebruiken om de workflowstatus in te stellen op **Concept**. U kunt deze pagina openen vanuit **Leveranciersfactuur** of vanuit de navigatie **Algemeen > Query's > Werkstroom**. Als u de workflowstatus terug wilt zetten op **Concept**, selecteert u **Intrekken**. U kunt de workflowstatus ook terugzetten op Concept door de actie **Intrekken** te selecteren op de pagina **Leveranciersfactuur** of **Leveranciersfacturen in behandeling**. Als de workflowstatus is ingesteld op **Concept**, wordt deze beschikbaar voor bewerking op de pagina **Leveranciersfactuur**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Het factuurtotaal weergeven op de pagina Leveranciersfacturen in behandeling

U kunt het factuurtotaal weergeven op de pagina **Leveranciersfacturen in behandeling** door de parameter **Factuurtotaal in lijst met in behandeling zijnde leveranciersfacturen weergeven** in te schakelen op de pagina **Parameters van module Leveranciers**. 

## <a name="vendor-open-transactions-report"></a>Rapport voor openstaande leverancierstransacties

Het rapport **Openstaande transacties leverancier** bevat gedetailleerde informatie over de openstaande transacties voor elke leverancier vanaf de datum die u opgeeft. Dit rapport wordt vaak gebruikt tijdens de controleprocedure voor het controleren van saldi tussen leveranciersboektransacties en grootboekrekeningtransacties.

Voor elke transactie bevat het rapport de volgende details:

- Factuurnummer
- Transactiedatum
- Boekstuknummer
- Transactiebedrag in de transactievaluta en valuta voor boekhouding
- Creditsaldo in de transactievaluta en valuta voor boekhouding
- Debitsaldo in de transactievaluta en valuta voor boekhouding
- Subtotaalbedrag in de valuta voor boekhouding
- Vervaldatum betaling

### <a name="filter-the-data-on-the-report"></a>De gegevens in het rapport filteren

Wanneer u het rapport **Open transacties leverancier** genereert, zijn de volgende standaardparameters beschikbaar. U kunt deze gebruiken om de gegevens te filteren die in het rapport worden opgenomen.

- **Toekomstige vereffening uitsluiten**: schakel dit selectievakje in om transacties uit te sluiten die worden vereffend na de datum die is ingevoerd in het veld **Openstaande transacties per**.
- **Openstaande transacties per** – Voer een datum in om transacties op te nemen die vanaf die datum openstaan. Als u geen datum invoert, wordt dit veld ingesteld op de maximumdatum. (De maximum datum is de laatste datum die door het systeem wordt geaccepteerd, 31 december 2154.) De volgende keer dat het rapport wordt uitgevoerd, wordt dit veld standaard ingesteld op de laatste datum die erin is ingevoerd.

Met de filters onder het veld **Op te nemen record** kunt u de transactiegegevens die in het rapport worden opgenomen, verder beperken.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Leveranciersfactuurbeleid instellen](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Belangrijke factuurgegevens in leverancierssysteem met leveranciersfactuur](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Een leveranciersfactuur in het factuurjournaal registreren](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
