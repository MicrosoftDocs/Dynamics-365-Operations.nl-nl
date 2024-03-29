---
title: Leverancierssamenwerking met externe leveranciers
description: In dit artikel wordt uitgelegd hoe aankoopbemiddelaars met externe leveranciers kunnen samenwerken om informatie over inkooporders en consignatievoorraad uit te wisselen.
author: GalynaFedorova
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 25561802996514f6f60fc9400c22dc61a30ef1c8
ms.sourcegitcommit: bad64015da0c96a6b5d81e389708281406021d4f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023783"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Leverancierssamenwerking met externe leveranciers

[!include [banner](../includes/banner.md)]

De module **Leverancierssamenwerking** is bedoeld voor leveranciers die geen EDI-integratie (Electronic Data Interchange) met Microsoft Dynamics 365 Supply Chain Management hebben. Hiermee kunnen leveranciers werken met inkooporders (IO's), facturen, consignatievoorraadgegevens en offerteaanvragen, en toegang krijgen tot delen van de modelgegevens van hun leveranciers. In dit artikel wordt beschreven hoe u kunt samenwerken met externe leveranciers die de interface voor leverancierssamenwerking gebruiken om met inkooporders, offerteaanvragen en consignatievoorraad te werken. Daarnaast wordt beschreven hoe u een specifieke leverancier in staat stelt om leverancierssamenwerking te gebruiken en hoe u de gegevens definieert die alle leveranciers te zien krijgen wanneer ze reageren op een inkooporder.

Meer informatie over wat externe leveranciers kunnen doen in de interface voor leverancierssamenwerking vindt u in [Leverancierssamenwerking met klanten](vendor-collaboration-work-customers-dynamics-365-operations.md).

Meer informatie over hoe leveranciers leverancierssamenwerking kunnen gebruiken in factureringsprocessen vindt u in [Werkgebied voor samenwerkingsfacturering van leveranciers](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md) Meer informatie over hoe u nieuwe gebruikers van leverancierssamenwerking inricht, vindt u in [Leverancierssamenwerkingsgebruikers beheren](manage-vendor-collaboration-users.md)

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>De gegevens definiëren die voor leveranciers te zien zijn wanneer ze reageren op inkooporders

Als leveranciers reageren op een inkooporder die u verzendt, moeten ze in een van de drie berichtvensters bevestigen of ze de inkooporder accepteren, afwijzen of accepteren met wijzigingen. Omdat de informatie die de leverancier op dat moment moet zien specifiek kan zijn voor uw bedrijf, kunt u de tekst opgeven die in elk van de drie bevestigingsberichten moet worden weergeven. Met de tekst kan de leverancier bijvoorbeeld worden geïnformeerd over de volgende stappen in het proces of over de voorwaarden.

Ga als volgt te werk om de tekst op te geven die moet worden weergegeven in de reactie op een inkooporder:

1. Selecteer op de pagina **Informatie voor leveranciers die reageren op inkooporders** het antwoordtype en selecteer vervolgens **Bewerken**.
2. Voer in het vak **Informatiebericht** de gegevens in die voor leveranciers moeten worden weergegeven in het berichtvenster.

Als u berichten in meerdere talen moet toevoegen, maakt u afzonderlijke berichten en geeft u voor elk daarvan de relevante taalcode op. Het bericht dat voor elke leverancier wordt weergegeven, is dan in de taal die de leverancier zelf gebruikt.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>De opties voor leverancierssamenwerking voor een specifieke leverancier instellen

Een beheerder configureert de algemene instellingen voor leverancierssamenwerking, zoals de beveiligingsrollen die beschikbaar zijn voor alle leveranciers waarmee u samenwerkt. Er zijn echter ook instellingen die voor elke leveranciersaccount kunnen verschillen. U moet deze instellingen configureren.

- Schakel leverancierssamenwerking in.
- Geef op of de leverancier prijsinformatie te zien moet krijgen.

### <a name="enabling-vendor-collaboration"></a>Leverancierssamenwerking inschakelen

Voordat gebruikersaccounts kunnen worden gemaakt voor een externe leverancier, moet u de leveranciersaccount zo configureren dat de leverancier kan gebruikmaken van leverancierssamenwerking. Stel op de pagina **Leveranciers** op het tabblad **Algemeen** het veld **Samenwerkingsactivering** in. De volgende opties zijn beschikbaar:

- **Actief (IO wordt automatisch bevestigd)**: inkooporders worden automatisch bevestigd wanneer de leverancier deze zonder wijzigingen accepteert. Als u deze optie gebruikt, moet u de taak *Geaccepteerde inkooporders van leverancierssamenwerking bevestigen* plannen, die verantwoordelijk is voor de verwerking van de bevestigingen. Zie het volgende onderdeel voor instructies.
- **Actief (IO wordt niet automatisch bevestigd)**: uw organisatie moet inkooporders handmatig bevestigen nadat de leverancier ze heeft geaccepteerd.

### <a name="scheduling-the-auto-confirmation-batch-job"></a>De batchtaak voor automatische bevestiging plannen

Als u de optie **Actief (inkooporder is automatisch bevestigd)** gebruikt voor een of meer leveranciers (zoals is beschreven in de vorige sectie), moet u de batchtaak *Geaccepteerde inkooporders van leverancierssamenwerking bevestigen* plannen. Deze taak is verantwoordelijk voor het verwerken en bevestigen van uw inkooporders. Anders vinden automatische bevestigingen nooit plaats. Voer de volgende procedure uit om deze taak te plannen.

1. Ga naar Inkoop **Inkoopbeheer \> Inkooporders \> Inkooporderbevestiging \> Geaccepteerde inkooporders van leverancierssamenwerking bevestigen**.
1. In het dialoogvenster **Geaccepteerde inkooporders van leverancierssamenwerking bevestigen** selecteert u op het sneltabblad **Op de achtergrond uitvoeren** de optie **Terugkeerpatroon**.
1. Definieer de planning voor de taak in het dialoogvenster **Terugkeerpatroon definiëren**. Houd rekening met het volgende wanneer u uw planning kiest:

    - Als uw systeem een groot gegevensvolume verwerkt en er veel batchtaken worden uitgevoerd, kan er een probleem zijn. In dat geval moet u de taak waarschijnlijk niet elke 10 minuten uitvoeren (afhankelijk van uw andere behoeften). Als de prestaties geen probleem voor u zijn, kunt u de taak zo vaak als elke 1 tot 2 minuten uitvoeren als dat nodig is.
    - Als uw leveranciers doorgaans snel (binnen een dag nadat ze akkoord zijn gegaan) goederen willen leveren, moet het terugkeerpatroon vaak (elke 10 tot 30 minuten of zo) zijn. Op deze manier kunnen magazijnmedewerkers de goederen voor de bevestigde IO ontvangen na de bevestiging.
    - Als de leveranciers vaak een lange doorlooptijd (meer dan 24 uur) hebben, kunt u instellen dat deze taak slechts één keer per dag wordt uitgevoerd.

1. Selecteer **OK** om uw planning toe te passen en terug te keren naar het dialoogvenster **Geaccepteerde inkooporders van leverancierssamenwerking bevestigen**.
1. Stel zo nodig extra achtergrondopties in. Het dialoogvenster biedt de gebruikelijke opties voor het instellen van batchtaken in Supply Chain Management.

Zie voor meer informatie over batchtaken [Overzicht van batchverwerking](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Opgeven of de leverancier prijsinformatie te zien moet krijgen

Als u prijsgegevens voor IO's via de interface voor leverancierssamenwerking wilt delen, moet u de optie **Prijzen/bedrag van inkooporder** op het tabblad **Details over inkooporders** voor de leveranciersaccount instellen op **Ja**. Deze prijsgegevens omvatten de prijs per eenheid, kortingen en toeslagen.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Werken met inkooporders bij het gebruik van leverancierssamenwerking

### <a name="sending-a-po-to-a-vendor"></a>Een inkooporder verzenden naar een leverancier

Inkooporders worden voorbereid in Supply Chain Management. Wanneer een inkooporder de status **Goedgekeurd** heeft, kunt u deze naar de leverancier verzenden door **Verzenden voor bevestiging** op de pagina **Inkooporder** te selecteren. De status van de inkooporder wordt in dat geval gewijzigd in **Externe controle.** Nadat de inkooporder is verzonden, kan de leverancier deze zien op de pagina **Inkooporders ter beoordeling** in de interface voor leverancierssamenwerking. De leverancier kan de inkooporder vervolgens accepteren, weigeren of wijzigingen erin voorstellen. De leverancier kan ook opmerkingen toevoegen om informatie zoals wijzigingen in de inkooporder door te geven. Als u de aandacht van de leverancier naar de nieuwe inkooporder wilt trekken, kunt u de inkooporder ook per e-mail verzenden via het afdrukbeheersysteem.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Bevestiging en acceptatie van een inkooporder door een leverancier

Als een leverancier een inkooporder accepteert, kan de inkooporder automatisch worden bevestigd of moet deze wellicht handmatig worden bevestigd. Het gedrag is afhankelijk van of het veld **Samenwerkingsactivering** voor de leverancier is ingesteld op **Actief (IO wordt automatisch bevestigd)** of **Actief (IO wordt niet automatisch bevestigd)**.

In de onderstaande tabel wordt de typische uitwisseling van informatie weergegeven, afhankelijk van hoe de leverancier antwoordt als u deze een inkooporder voor bevestiging toestuurt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Leveranciersantwoord</th>
<th>Resultaat</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>De leverancier <strong>accepteert</strong> de order en Supply Chain Management wordt zo geconfigureerd dat door de leverancier geaccepteerde inkooporders automatisch worden bevestigd.</td>
<td>De status van de order verandert in <strong>Bevestigd</strong>. Als de order om een of andere reden niet kan worden bijgewerkt, wordt het antwoord van de leverancier wel geregistreerd als <strong>Geaccepteerd</strong>, maar blijft de inkooporder de status <strong>Externe controle</strong> behouden. 

De inkooporder die naar de leverancier is verzonden en de status <strong>Externe controle</strong> heeft, wordt bijgewerkt met bevestigde leveringsdatums op de regels. Met deze update wordt een nieuwe versie gestart die automatisch de status <strong>Bevestigd</strong> krijgt. Wanneer de inkooporder is bevestigd, wordt deze weergegeven in de samenwerkingsinterface van de leverancier.</td>
</tr>
<tr class="odd">
<td>De leverancier <strong>accepteert</strong> de order, maar Supply Chain Management is niet zodanig geconfigureerd dat door de leverancier geaccepteerde inkooporders automatisch worden bevestigd.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Geaccepteerd</strong>, maar de inkooporder behoudt de status <strong>Externe controle</strong>.

De inkooporder die naar de leverancier is verzonden en de status <strong>Externe controle</strong> heeft, wordt bijgewerkt met bevestigde leveringsdatums op de regels. Met deze update wordt een nieuwe versie gestart die automatisch de status <strong>Externe controle</strong> krijgt. U kunt de inkooporder vervolgens handmatig bevestigen.</td>
</tr>
<tr class="even">
<td>De leverancier <strong>wijst de order af</strong>.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Afgewezen</strong>, maar de inkooporder behoudt de status <strong>Externe controle</strong>. De afwijzing wordt ontvangen met de leveranciersnotitie.</td>
</tr>
<tr class="odd">
<td>De leverancier <strong>accepteert</strong> de order <strong>met wijzigingen</strong>. Wijzigingen worden voorgesteld op regelniveau. De leverancier kan afzonderlijke regels accepteren of afwijzen. Hier volgen enkele andere wijzigingen die de leverancier kan voorstellen:
<ul>
<li>Wijzig datums of hoeveelheden.</li>
<li>Splits regels op voor verschillende leveringsdatums of -hoeveelheden.</li>
<li>Vervang een item.</li>
</ul>
Prijsgegevens en toeslagen kunnen niet door de leverancier worden gewijzigd. De leverancier kan deze wijzigingen echter wel voorstellen met notities.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Geaccepteerd met wijzigingen</strong>, en de inkooporder behoudt de status <strong>Externe controle</strong>. De statuswaarden geven weer welke typen wijzigingen de leverancier heeft voorgesteld. Zie voor informatie over de automatische verwerking van de wijzigingen de sectie &quot;De inkooporder bijwerken wanneer een leverancier wijzigingen voorstelt&quot; verderop in dit artikel. </td>
</tr>
</tbody>
</table>

U kunt het werkgebied **Voorbereiding van inkooporder** gebruiken om te controleren op welke inkooporders de leverancier heeft gereageerd. Dit werkgebied bevat twee lijsten die inkooporders met de status **Externe controle** bevatten:

- Bij externe herziening is actie vereist
- Bij externe herziening in afwachting van antwoord van leverancier

### <a name="changing-a-po"></a>Een inkooporder wijzigen

Als u een inkooporder wilt wijzigen waarop al is gereageerd, moet u een nieuwe versie van de inkooporder naar de leverancier verzenden. De nieuwe inkooporder heeft een versieachtervoegsel om aan te geven dat het om een gewijzigde versie van een inkooporder gaat die eerder is verzonden. Op de pagina **Historie van leveranciersbevestigingen van inkooporders** kunnen u en uw leveranciers de historie van elke order volgen. De eerder bevestigde versie van de IO blijft in de lijst met bevestigde IO's tot de nieuwe IO is bevestigd.

### <a name="canceling-a-po"></a>Een inkooporder annuleren

Wanneer u een inkooporder annuleert, wordt de status gewijzigd in **Goedgekeurd**. U moet de IO terugzenden naar de leverancier, zodat deze de annulering kan bevestigen of afwijzen. Nadat de annulering is bevestigd, wordt de inkooporder in de lijst met bevestigde PO´s van de leverancier weergegeven als **Geannuleerd**.

### <a name="adding-attachments-to-a-po"></a>Bijlagen toevoegen aan een inkooporder

U kunt bijlagen, zoals bestanden, afbeeldingen en notities, aan de inkooporder toevoegen via het documentbeheersysteem. Bijlagen met het type **Extern** worden zichtbaar voor de leverancier wanneer u deze de inkooporder toestuurt.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Een inkooporder bijwerken wanneer een leverancier wijzigingen voorstelt

Als een leverancier heeft gereageerd op een inkooporder en wijzigingen voorstelt, is de volgende stap om de reactie te verwerken.

In het werkgebied **Voorbereiding van inkooporder** in de lijst **Bij externe herziening is actie vereist** kunt u inkooporders identificeren die een leverancier heeft geaccepteerd met wijzigingen. Vanuit deze lijst kunt u ook navigeren naar de reactie van de leverancier.

In een reactie kan een leverancier de volgende informatie in de koptekst wijzigen:
 
- Documentverwijzing van leverancier
- Leveringsmethode
- Leveringsvoorwaarden
- Bevestigde leveringsdatum

De leverancier kan ook een notitie of bijlage toevoegen.

Op de regels kan de leverancier de hoeveelheid en de leveringsdatums wijzigen, notities en bijlagen toevoegen, een regel afwijzen, een regel vervangen door een ander product dat is ingevoerd als tekst en een regel splitsen in meerdere leveringen. De status van een regel varieert, afhankelijk van de wijzigingen die de leverancier heeft voorgesteld:
    
- **Geaccepteerd met wijzigingen**
- **Afgewezen**
- **Vervangen**: in dit geval wordt een extra regel toegevoegd met de status **Vervanging**.
- **Bevestigd**
- **Opsplitsen tot planning**: in dit geval worden extra regels met de status **Planningsregels** toegevoegd.

Als een regel geen wijzigingen bevat, is de regelstatus **Geaccepteerd**.

In de reactie laten de regelstatussen zien welke typen wijzigingen de leverancier heeft aangebracht. Bovendien worden alle gewijzigde velden vet weergegeven, zodat u de wijzigingen makkelijk herkent.

U kunt een inkooporder bijwerken door **Update van inkooporder verwerken** in de reactie of voor één regel tegelijk te selecteren. In het veld **Is update van inkooporder verwerkt?** in de koptekst en de regels wordt aangegeven of het systeem de koptekst of regels heeft verwerkt om alle mogelijke wijzigingen in de inkooporder door te voeren die voortkomen uit de reactie. U kunt de actie **Update van inkooporder verwerken** slechts één keer per kop of regel verwerken.

Niet alle voorgestelde wijzigingen kunnen worden doorgevoerd op een inkooporder. Alleen updates in de koptekst en van datums en hoeveelheden op regels kunnen automatisch worden bijgewerkt op de inkooporder. Voor andere wijzigingen moet u de inkooporder handmatig bijwerken. In dit geval is **Handmatige update** de waarde van het veld **Is update van inkooporder verwerkt**. Als een leverancier voorstelt dat een regel in een schema wordt gesplitst, moet deze wijziging bijvoorbeeld handmatig worden doorgevoerd.

Elke regel met de status **Geaccepteerd** heeft een bevestigde leveringsdatum. Wanneer u de actie **Update van inkooporder verwerken** uitvoert, wordt deze datum bijgewerkt op de inkooporder. Notities en bijlagen worden niet automatisch overgebracht naar de huidige inkooporder. Wanneer u de huidige inkooporder bijwerkt via de actie **Update van inkooporder verwerken**, worden handelsovereenkomsten niet opnieuw beoordeeld op de inkooporderregels.

## <a name="po-statuses-and-versions"></a>Statussen en versies van inkooporders

In deze sectie worden de verschillende statussen beschreven die een inkooporder kan hebben tot het tijdstip waarop deze wordt bevestigd. Daarnaast wordt beschreven wanneer nieuwe versies van een inkooporder beschikbaar worden gesteld voor de leverancier. Het gedrag verschilt, al naargelang of u wijzigingsbeheer voor inkooporders gebruikt. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versies en status als u geen wijzigingsbeheer gebruikt

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat.

| Actie | Status en versie |
|--------|--------------------|
| De oorspronkelijke versie van de inkooporder wordt gemaakt in Supply Chain Management. | De status is **Goedgekeurd**. |
| De IO wordt verzonden naar de leverancier. | Er wordt een versie geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**. |
| De leverancier verzendt een antwoord **Geaccepteerd met wijzigingen**. | De status is nog steeds **Externe controle**. |
| U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd. | De status wordt gewijzigd in **Goedgekeurd**. |
| U verzendt de nieuwe versie van de IO naar de leverancier. | Er wordt een nieuwe versie geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**. |
| De leverancier accepteert de nieuwe versie van de inkooporder. | De status is nog steeds **Externe controle**, tenzij de leveranciersaccount zo is geconfigureerd dat IO's bij acceptatie automatisch de status **Bevestigd** krijgen. |

Leveranciers hoeven een inkooporder niet te bevestigen via de interface voor leverancierssamenwerking. Ze kunnen ook een e-mail verzenden of hun acceptatie van een inkooporder via andere kanalen doorgeven. U kunt de order vervolgens handmatig bevestigen. In dit geval ontvangt u een waarschuwing dat de order wordt bevestigd, zelfs als er geen antwoord van de leverancier is. De inkooporder wordt vervolgens in de bevestigingshistorie weergegeven als een openstaande bevestigde order die geen antwoorden heeft. Op dat punt heeft de leverancier niet meer de mogelijkheid om de inkooporder te bevestigen of af te wijzen.

> [!NOTE]
> De versie van de inkooporder die beschikbaar is voor andere processen in Supply Chain Management is altijd de laatste versie, ook als deze versie nog niet is geregistreerd in de interface voor leverancierssamenwerking.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versies en status als u wijzigingsbeheer gebruikt

Als wijzigingsbeheer is ingeschakeld voor inkooporders, doorloopt de inkooporder een goedkeuringsworkflow om de status **Goedgekeurd** te bereiken. Dit proces is niet zichtbaar voor de leverancier.

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat als wijzigingsbeheer is ingeschakeld. Een versie wordt geregistreerd wanneer de inkooporder wordt goedgekeurd, niet wanneer de inkooporder naar de leverancier wordt verzonden of wordt bevestigd.

| Actie | Status en versie |
|--------|--------------------|
| De oorspronkelijke versie van de inkooporder wordt gemaakt in Supply Chain Management. | De status is **Concept**. |
| De IO wordt verzonden naar het goedkeuringsproces. (Het goedkeuringsproces is een intern proces waarbij de leverancier niet betrokken is.) | De status wordt gewijzigd van **Concept** in **Wordt gecontroleerd** in **Goedkeuring** als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. De goedgekeurde inkooporder wordt geregistreerd als een versie. | 
| De IO wordt verzonden naar de leverancier. | De versie wordt geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**. |
| U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd, handmatig dan wel door middel van de actie **Update van inkooporder verwerken** op de reactie, om zo de inkooporder bij te werken. | De status wordt weer gewijzigd in **Concept**. |
| De IO wordt weer naar het goedkeuringsproces verzonden. | De status wordt gewijzigd van **Concept** in **Wordt gecontroleerd** in **Goedkeuring** als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. Het systeem kan ook zo worden geconfigureerd dat voor bepaalde veldwijzigingen geen nieuwe goedkeuring is vereist. In dit geval wordt de status eerst gewijzigd in **Concept** en vervolgens automatisch bijgewerkt in **Goedgekeurd**. De goedgekeurde inkooporder wordt geregistreerd als een nieuwe versie. |
| U verzendt de nieuwe versie van de IO naar de leverancier. | De nieuwe versie wordt geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**. |
| De leverancier keurt de nieuwe versie van de inkooporder goed | De status wordt gewijzigd in **Bevestigd**. Dit gebeurt automatisch of wanneer u het antwoord van de leverancier ontvangt en vervolgens de inkooporder bevestigt. |

## <a name="sharing-information-about-consignment-inventory"></a>Informatie over consignatievoorraad delen

Als u consignatievoorraad gebruikt, kunnen leveranciers de interface voor leverancierssamenwerking gebruiken om informatie op de volgende pagina's te bekijken:

- **Inkooporders die consignatievoorraad verbruiken**: inkooporders voor consignatievoorraad worden gegenereerd wanneer het eigendom van de voorraad van de leverancier naar uw bedrijf overgaat. Tegelijkertijd wordt een productontvangstbon geboekt. Deze consignatie-inkooporders worden alleen weergegeven op de pagina **Inkooporders die consignatievoorraad verbruiken**. Ze worden niet opgenomen op de pagina **Alle bevestigde inkooporders** in de module **Leverancierssamenwerking**.
- **Producten ontvangen uit consignatievoorraad**: deze pagina bevat een overzicht van alle transacties waarvan het eigendom van producten van de leverancier is overgedragen aan uw bedrijf. Leveranciers kunnen deze informatie gebruiken om de klant te factureren.
- **Voorhanden consignatievoorraad**: op deze pagina wordt de voorhanden consignatievoorraad weergegeven die het eigendom is van de leverancier en is ontvangen in uw magazijn.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Werken met offerteaanvragen bij het gebruik van leverancierssamenwerking

In deze sectie wordt de interactie tussen klanten en leveranciers tijdens het proces voor offerteaanvragen beschreven. Ook wordt uitgelegd hoe informatie wordt overgebracht naar de leveranciers. Zie voor een algemeen overzicht van ondersteuning voor het proces voor offerteaanvragen [Overzicht van Offerteaanvragen](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternatieven, bijlagen, wijzigingen en retouren

- **Alternatieven**: in de koptekst van een offerteaanvraagcase kunt u opgeven dat alternatieven zijn toegestaan voor niet-catalogusartikelregels. Wanneer alternatieven zijn ingeschakeld, kunnen leveranciers een alternatieve regel voor elke aangevraagde regel toevoegen.
- **Bijlagen**: bijlagen kunnen worden toegevoegd op koptekst- en regelniveau van een offerteaanvraagcase. Bijlagen kunnen als intern of extern worden geclassificeerd. Interne bijlagen kunnen alleen aan de klantzijde worden weergegeven terwijl leveranciers externe bijlagen wel kunnen bekijken nadat ze zijn verzonden.

    Leveranciers kunnen ook bijlagen toevoegen in hun antwoord op een bieding. Deze bijlagen kunnen aan de klantzijde worden weergegeven nadat het antwoord op een bieding is ingediend door een leverancier. Bijlagen die leveranciers toevoegen, worden altijd geclassificeerd als extern. Als u een bijlage wilt openen die een leverancier met een bieding heeft ingediend, selecteert u **Bijlagen bij biedingen** of **Bijlagen bij biedingsregels**.
    
    Als u bijlagen wilt openen die zijn verzonden met de offerteaanvraagcase, gebruikt u het symbool van de paperclip voor documentafhandeling in het antwoord.

- **Aanpassingen**: wanneer een aanpassing is voltooid, worden de bestaande antwoorden op biedingen verwijderd, zodat deze kunnen worden vervangen door bijgewerkte waarden. Informatie zoals de regelprijs en hoeveelheid uit vorige antwoorden op biedingen kan worden weergegeven via de journalen in de offerteaanvraagcase.

    Om de verwerking van aanpassingen af te dwingen, stelt u op de pagina **Parameters voor inkoopbeheer** op het sneltabblad **Offerteaanvragen** de optie **Offerteaanvragen vergrendelen wanneer ze zijn verzonden** in op **Ja**. (Deze optie is ingesteld en vereist voor de publieke sector.)

- **Retouren**: als een leverancier een bieding heeft ingediend, maar er meer of gewijzigde informatie vereist is voor de offerteaanvraagcase, kan de klant de bieding retourneren naar de leverancier. De gegevens uit het eerder ingediende bod blijven behouden en de leverancier kan de gevraagde wijzigingen doorvoeren zonder het biedingsproces opnieuw te hoeven starten.

## <a name="public-sector-extensions"></a>Uitbreidingen voor de publieke sector

Voor de publieke sector kan een offerteaanvraagcase dankzij de uitgebreide functionaliteit naar leveranciers worden verzonden en worden gepubliceerd. Wanneer u een offerteaanvraagcase publiceert, kan iedereen die de gegevens opvraagt het werk bekijken dat voldoet aan de voorschriften van de meeste publieke sectoren. Al het beschikbare werk wordt weergegeven op de lijstpagina **Gepubliceerde offerteaanvragen openen** en de geannuleerde offerteaanvragen, offerteaanvragen in behandeling of toegekende offerteaanvragen kunnen worden bekeken op de lijstpagina **Gesloten gepubliceerde offerteaanvragen**. Deze documenten kunnen ook op een site buiten Supply Chain Management worden bekeken via integraties met de volgende gegevensentiteiten:

- Gepubliceerde offerteaanvragen
- Gepubliceerde regel van offerteaanvragen
- Gepubliceerde bijlagen voor kopteksten van offerteaanvragen

Met deze entiteiten kunnen personen die geen geconfigureerde gebruikers in Supply Chain Management zijn, maar wel anoniem toegang hebben tot de externe site, het beschikbare en afgesloten werk bekijken. Daarnaast kan de gebruiker die parameters instelt voor het offerteaanvraagproces met de uitgebreide functionaliteit in **Verzenden en publiceren** een e-mailsjabloon definiëren. Wanneer inkoopmedewerkers de offerteaanvraagcase vervolgens maken, moeten ze de e-mailsjabloon selecteren om de vereiste gegevens te verzenden naar de leveranciers in de offerteaanvraagcase. 

De gebruiker die parameters voor het proces voor offerteaanvragen instelt, kan meerdere e-mailsjablonen maken. Deze e-mailsjablonen kunnen zowel statische tekst als de volgende vervangingstokens bevatten. Wanneer een e-mailbericht wordt gemaakt, worden de tokens vervangen door contextuele waarden.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Als een aanpassing vereist is en wordt verzonden nadat de offerteaanvraag is verzonden, wordt de offerteaanvraag opnieuw verzonden naar alle uitgenodigde leveranciers. Het gepubliceerde document wordt ook bijgewerkt op de pagina **Gepubliceerde offerteaanvragen openen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
