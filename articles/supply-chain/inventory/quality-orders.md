---
title: Kwaliteitsorders
description: In dit onderwerp wordt beschreven hoe u handmatig of automatisch kwaliteitsorders maakt en hoe u hiermee werkt om inspecties uit te voeren en testresultaten vast te leggen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c951716a456101ba753e5c567c80deb4ee7e764f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956616"
---
# <a name="quality-orders"></a>Kwaliteitsorders

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u handmatig of automatisch kwaliteitsorders maakt en hoe u hiermee werkt om inspecties uit te voeren en testresultaten vast te leggen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automatisch gemaakte kwaliteitsorders

U kunt het systeem zo configureren dat kwaliteitsorders automatisch worden gemaakt op basis van artikelbemonsteringsregels. Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie.

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Kwaliteitsorders handmatig maken

Volg deze stappen om handmatig een kwaliteitsorder te maken.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer **Nieuw**.
1. Selecteer in het dialoogvenster **Kwaliteitsorders** in het veld **Verwijzingstype** de voorraadverwijzing waaraan uw kwaliteitsorder wordt gekoppeld. Zie de sectie [Verwijzingstypen voor kwaliteitsorders](#ref-types) verderop in dit onderwerp voor een beschrijving van de verwijzingstypen die kunnen worden geselecteerd.

    > [!NOTE]
    > Voorraad die is gekoppeld aan de geselecteerde verwijzing, moet beschikbaar zijn. Als er geen voorraad beschikbaar is voor de combinatie van het verwijzingstype, de hoeveelheid en de voorraaddimensie die u selecteert, wordt er een foutbericht weergegeven.

1. Voer een van de volgende stappen uit, afhankelijk van de waarde die u hebt geselecteerd in het veld **Verwijzingstype**:

    - Als u **Voorraad** hebt geselecteerd, hoeft u verder geen verwijzingsinformatie in te vullen.
    - Als u **Verkoop** of **Inkoop** hebt geselecteerd, geeft u de volgende informatie op:

        - **Rekening selecteren**: verwijs naar het rekeningnummer van de klant of de leverancier.
        - **Verwijzingsnummer**: verwijs naar het nummer van de verkooporder of inkooporder.
        - **Verwijzingspartij**: verwijs naar de specifieke verkooporderregel of inkooporderregel.

    - Als u **Productie**, **Quarantaine** of **Productie van coproducten** hebt geselecteerd, verwijst u in het veld **Verwijzingsnummer** naar het nummer van de productieorder, batchorder of quarantaineorder.
    - Als u **Routebewerking** hebt geselecteerd, geeft u de volgende informatie op:

        - **Verwijzingsnummer**: verwijs naar het nummer van de productieorder of de batchorder.
        - **Bewerkingsnummer** : verwijs naar het specifieke routebewerkingsnummer.
        - **Bewerking**: verwijs naar de specifieke routebewerking.
        - **Bron**: verwijs naar de specifieke bron die moet worden gebruikt voor de routebewerking.

1. Selecteer in het veld **Testgroep** de groep met tests die moet worden uitgevoerd.
1. Voer in het veld **Hoeveelheid** in hoeveel artikelen er moeten worden getest.
1. Voer in de sectie **Voorraaddimensie** eventuele extra voorraaddimensies in die zijn vereist voor het geselecteerde artikel.
1. Selecteer **OK**.

Nadat er een kwaliteitsorder is gemaakt, kunt u beginnen met het inspecteren van de voorraad en het vastleggen van de testresultaten. Zie [De kwaliteit van goederen inspecteren](tasks/inspect-quality-goods.md) voor meer informatie over het vastleggen en valideren van testresultaten.

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Verwijzingstypen voor kwaliteitsorders

Kwaliteitsorders worden gebruikt om details over inspecties en testresultaten voor specifieke voorraad in uw magazijn bij te houden. Een kwaliteitsorder moet een verwijzing bevatten die de bron van de voorraad vertegenwoordigt die wordt getest. Kwaliteitsorders kunnen worden gekoppeld aan de volgende verwijzingstypen:

- **Voorraad**: dit verwijzingstype geeft aan dat u voorraad controleert die voorhanden is. Inspecties van dit type zijn doorgaans willekeurig of niet-gepland en vinden plaats wanneer een magazijnmedewerker een probleem identificeert.
- **Verkoop:** dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een bepaalde verkooporder. Inspecties van dit type zijn meestal gekoppeld aan klantspecificaties of het genereren van een analysecertificaat (CoA) dat aan een klant moet worden verstrekt als onderdeel van een zending. (Een analysecertificaat wordt ook wel een nalevingscertificaat genoemd \[CoC\].)
- **Aankoop**: dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een verkooporder. Inspecties van dit type worden vaak gebruikt om inkomende goederen te controleren voordat ze in de voorraad worden geplaatst of worden verbruikt in productieprocessen.
- **Productie**: dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een productieorder. Inspecties van dit type worden vaak gebruikt om eindproducten te controleren voordat ze in de voorraad worden geplaatst.
- **Quarantaine**: dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een quarantaineorder. Quarantaineorders zijn een speciaal ordertype waarmee voorraad in een gescheiden magazijn of een gescheiden locatie in het magazijn wordt bijgehouden. Inspecties van dit type worden vaak gebruikt om goederen te controleren die een klant heeft geretourneerd of die in quarantaine zijn geplaatst voor een nadere analyse. Quarantaineorders kunnen worden gegenereerd vanuit kwaliteitsorders. Ze kunnen ook worden gegenereerd vanuit andere bronnen en kwaliteitsorders kunnen vervolgens aan de quarantaineorders worden gekoppeld.
- **Routebewerking**: dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een specifieke stap van de route voor een productieorder. Inspecties van dit type worden meestal gebruikt om het onderhanden werk van een product te analyseren voordat het naar de volgende stap in het productieproces gaat.
- **Productie van coproducten**: dit verwijzingstype geeft aan dat u voorraad controleert die is gekoppeld aan een coproduct van een productieorder. Inspecties van dit type worden meestal gebruikt om het coproduct van een batchorder te controleren voordat het coproduct aan de voorraad wordt toegevoegd.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Kwaliteitsorders vanuit verschillende delen van het systeem weergeven en maken

Kwaliteitsorders kunnen handmatig worden gemaakt. Deze orders kunnen ook automatisch worden gemaakt op basis van de kwaliteitskoppelingen die u definieert. Zie [Kwaliteitskoppelingen](quality-associations.md) voor meer informatie over het automatisch maken en beheren van kwaliteitsorders.

U kunt de pagina Kwaliteitsorders gebruiken om handmatig een nieuwe kwaliteitsorder te maken of de status van een kwaliteitsorder weer te geven die aan een andere record is gekoppeld. U kunt de pagina Kwaliteitsorder op verschillende manieren openen.

### <a name="from-the-quality-orders-page"></a>Vanaf de pagina Kwaliteitsorders

Als u de kwaliteitsorder handmatig wilt maken en alle bestaande kwaliteitsorders wilt weergeven, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**. De resterende secties van dit onderwerp bevatten meer informatie over het werken met de pagina **Kwaliteitsorders**.

### <a name="from-sales-orders"></a>Van verkooporders

Als u wilt werken met kwaliteitsorders die aan uw verkooporders zijn gekoppeld, gaat u naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders** en volgt u een van de volgende stappen:

- Open een verkooporder of selecteer deze in het raster. Selecteer vervolgens in het actievenster op het tabblad **Verzamelen en inpakken** in de groep **Kwaliteitsbeheer** de optie **Kwaliteitsorders** om de pagina **Kwaliteitsorders** te openen. Hier kunt u kwaliteitsorders die zijn gekoppeld aan de verkooporder, weergeven, maken of bijwerken.
- Open een verkooporder en selecteer vervolgens op het tabblad **Koptekst** het sneltabblad **Algemeen**. In het veld **Status van kwaliteitsorder** wordt de algehele status weergegeven van alle kwaliteitsorders die zijn gekoppeld aan de verkooporder.
- Open een verkooporder en selecteer vervolgens op het tabblad **Regels** het sneltabblad **Verkooporderregels**. In de kolom **Status van kwaliteitsorder** wordt de status van elke regel van de verkooporder weergeven.

### <a name="from-purchase-orders"></a>Van inkooporders

Als u wilt werken met kwaliteitsorders die aan uw inkooporders zijn gekoppeld, gaat u naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders** en volgt u een van de volgende stappen:

- Open een inkooporder of selecteer deze in het raster. Selecteer vervolgens in het actievenster op het tabblad **Ontvangen** in de groep **Kwaliteitsbeheer** de optie **Kwaliteitsorders** om de pagina **Kwaliteitsorders** te openen. Hier kunt u kwaliteitsorders die zijn gekoppeld aan de inkooporder, weergeven, maken of bijwerken.
- Open een inkooporder en selecteer vervolgens op het tabblad **Koptekst** het sneltabblad **Algemeen**. In het veld **Status van kwaliteitsorder** wordt de algehele status weergegeven van alle kwaliteitsorders die zijn gekoppeld aan de inkooporder.
- Open een inkooporder en selecteer vervolgens op het tabblad **Regels** het sneltabblad **Inkooporderregels**. In de kolom **Status van kwaliteitsorder** wordt de status van elke regel van de inkooporder weergeven.

### <a name="from-production-orders"></a>Van productieorders

Als u wilt werken met kwaliteitsorders die aan uw productieorders zijn gekoppeld, gaat u naar **Productiebeheer \> Productieorders \> Alle productieorders** en volgt u een van de volgende stappen:

- Open een productieorder of selecteer deze in het raster. Selecteer vervolgens in het actievenster op het tabblad **Weergeven** in de groep **Kwaliteitsbeheer** de optie **Kwaliteitsorders** om de pagina **Kwaliteitsorders** te openen. Hier kunt u kwaliteitsorders die zijn gekoppeld aan de productieorder, weergeven, maken of bijwerken.
- Open een productieorder of selecteer deze in het raster. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Productiedetails** de optie **Route** om de pagina **Productieroute** te openen. Volg een van de volgende stappen om de kwaliteitsorders weer te geven die zijn gekoppeld aan een routebewerking:

    - Selecteer de doelroutebewerking in het raster. Selecteer vervolgens in het actievenster de optie **Query's \> Kwaliteitsorders**.
    - Selecteer de waarde in het veld **Bewerkingsnummer** voor de doelroutebewerking om de pagina nmet details van de **Productieroute** te openen. Op het sneltabblad **Algemeen** wordt in het veld **Status van kwaliteitsorder** de status van de kwaliteitsorders weergegeven die zijn gekoppeld aan de routebewerking.

- Open een productieorder en selecteer het sneltabblad **Algemeen**. In het veld **Status van kwaliteitsorder** wordt de status weergegeven van de kwaliteitsorders die zijn gekoppeld aan de productieorder.

### <a name="from-quarantine-orders"></a>Van quarantaineorders

Als u wilt werken met kwaliteitsorders die aan uw quarantaineorders zijn gekoppeld, gaat u naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Quarantaineorders** en volgt u een van de volgende stappen:

- Controleer de waarden in de kolom **Status van kwaliteitsorders**. Op deze manier kunt u de algehele status van alle kwaliteitsorders te weten komen die aan elke quarantaineorder in het raster zijn gekoppeld.
- Selecteer een quarantaineorder in het raster en selecteer vervolgens in het actievenster **Kwaliteitsorders** om kwaliteitsorders weer te geven, te maken of bij te werken die aan de quarantaineorder zijn gekoppeld.

## <a name="advanced-actions-for-quality-orders"></a>Geavanceerde acties voor kwaliteitsorders

U kunt verschillende acties op kwaliteitsorders uitvoeren om de status te beheren, documenten te genereren en informatie over extra gegevens op te vragen.

### <a name="reopen-a-quality-order"></a>Een kwaliteitsorder opnieuw openen

Standaard kunt u een kwaliteitsorder niet meer bewerken of bijwerken nadat deze is gevalideerd en de tests zijn geslaagd. In sommige gevallen moet u een kwaliteitsorder mogelijk opnieuw openen nadat deze is voltooid.

Volg deze stappen om een kwaliteitsorder opnieuw te openen.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Open de gevalideerde kwaliteitsorder of selecteer deze in het raster.
1. Selecteer **Kwaliteitsorder opnieuw openen** in het actievenster.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Een analysecertificaat voor een kwaliteitsorder maken

Een analysecertificaat is een rapport dat wordt gegenereerd door het kwaliteitsgarantieteam van een organisatie. Het rapport geeft aan dat een product voldoet aan bepaalde regels of vereisten. Uw klanten of regelgevende instanties op uw geopolitieke locatie vereisen mogelijk analysecertificaten. Deze certificaten zijn mogelijk ook vereist op basis van uw bedrijfstak en het type producten dat u verwerkt, inkoopt, produceert of verkoopt.

Met Supply Chain Management kunt u een analysecertificaat genereren van een kwaliteitsorder. Het rapport bevat de resultaten van tests die de kwaliteitsorder heeft ondergaan en waarin de optie **Analysecertificaatrapport** is ingesteld op *Ja*. Deze optie kan standaard worden ingesteld op basis van de test die u op de pagina **Tests** definieert. U kunt de instelling echter overschrijven voor specifieke tests voor een specifieke kwaliteitsorder.

Volg deze stappen om een analysecertificaat voor een kwaliteitsorder te genereren.

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer de kwaliteitsorder waarvoor u een analysecertificaat wilt maken.
1. Selecteer **Query's \> Analysecertificaat** in het actievenster.
1. Selecteer **Nieuw** op de pagina **Analysecertificaat** in het actievenster.
1. Optioneel: selecteer in het veld **Contact** de contactpersoon aan wie het certificaat moet worden geadresseerd.
1. Selecteer **Afdrukken** in het actievenster.
1. Definieer in het dialoogvenster **Analysecertificaat** hoe het rapport moet worden afgedrukt. Selecteer vervolgens **OK** om het rapport af te drukken naar een printer, weer te geven op het scherm, op te slaan naar een bestand of als e-mailbericht te verzenden.
1. Sluit de pagina's.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Voorraad voor een kwaliteitsorder blokkeren of deblokkeren

Wanneer een kwaliteitsorder automatisch wordt gegenereerd op basis van een kwaliteitskoppeling, kan de artikelbemonstering die aan de kwaliteitskoppeling is toegewezen, zo worden geconfigureerd dat de volledige voorraadhoeveelheid van de verwijzing die wordt getest, wordt geblokkeerd. Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie over artikelbemonstering.

Als u geen volledige blokkering gebruikt of als u handmatig een kwaliteitsorder maakt, wordt automatisch een voorraadblokkeringsrecord gemaakt voor de hoeveelheid van het artikel die in de kwaliteitsorder wordt getest. In de record die is gemaakt op de pagina **Voorraadblokkering**, wordt het veld **Type voorraadblokkering** ingesteld op *Kwaliteitsorder*.

Als u de voorraadblokkering wilt weergeven en bewerken voor een kwaliteitsorder die is geselecteerd op de pagina **Voorraadblokkering**, selecteert u **Query's \> Voorraadblokkering** in het actievenster. Zie [Voorraadblokkering](inventory-blocking.md) voor meer informatie.

### <a name="inquire-about-the-details-of-a-quality-order"></a>Informatie opvragen over de details van een kwaliteitsorder

Gebruik de volgende knoppen in het actievenster van de pagina **Kwaliteitsorders** om meer informatie weer te geven over een kwaliteitsorder of die betrekking heeft op de order:

- **Query's \> Werkgegevens**: open een pagina waarop u magazijnwerk kunt weergeven dat gekoppeld is aan de kwaliteitsorder.
- **Query's \> Niet-conformeringen**: open een pagina waarop u niet-conformeringen kunt weergeven die gekoppeld zijn aan de kwaliteitsorder.
- **Voorraad:** de opdrachten in dit menu worden bij alle voorraadtransacties gebruikt. U kunt deze gebruiken om details, zoals transacties, voorhanden voorraad, reserveringen en markering weer te geven of bij te werken.

### <a name="create-cases-related-to-quality-orders"></a>Cases maken die zijn gekoppeld aan kwaliteitsorders

U kunt cases maken die zijn gekoppeld aan kwaliteitsorders. Op deze manier kunt u details bijhouden over problemen en een oplossing zoeken. Vervolgens kunt u met de werkstroomfuncties van casebeheer gebruiken om een case via een vooraf gedefinieerd bedrijfsproces te routeren om aanvullende goedkeuringen of meer informatie te krijgen over een specifiek probleem. U kunt ook de functie kennisartikelen gebruiken om een knowledge base van oplossingen voor veelvoorkomende problemen te maken.

## <a name="case-management-examples-for-quality-management"></a>Voorbeelden van casebeheer voor kwaliteitsbeheer

### <a name="example-1"></a>Voorbeeld 1

U werkt voor een productiebedrijf dat zich moet houden aan strenge regels die betrekking hebben op de productie van gereguleerde producten, zoals voeding. Kwaliteitsorders worden gebruikt voor het registreren en bijhouden van details over de kwaliteit van artikelen in het gehele productieproces. Als een kwaliteitsorder niet aan specifieke testen voldoet, kan er een probleem zijn met de apparatuur. Cases worden gebruikt om een bedrijfsproces te volgen en het probleem naar de juiste technici te escaleren zodat de hoofdoorzaak kan worden bepaald. Om bedrijfsprocessen gemakkelijker te kunnen volgen, houdt het bedrijf een knowledge base bij van veelvoorkomende problemen met betrekking tot kwaliteitsorders en problemen met apparatuur.

### <a name="example-2"></a>Voorbeeld 2

U werkt voor een distributiebedrijf dat producten verzendt die kunnen worden aangepast voor verschillende landen en regio's. Sommige klanten hebben strenge specificaties die moeten worden opgevolgd. Als deze niet worden opgevolgd, leidt dit mogelijk tot kosten en retouren of terugboekingen. U gebruikt kwaliteitsorders om de details bij te houden van elke test en de resultaten die overeenkomen met de vereisten van klanten. Cases worden gebruikt om de gegevens voor het analysecertificaat te controleren en goed te keuren voordat het document wordt gegenereerd en gekoppeld aan andere verzendingsdocumenten.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Processen voor kwaliteitsbeheer](quality-management-processes.md)
- [Kwaliteitstest](quality-tests.md)
- [Kwaliteitstestgroepen](quality-test-groups.md)
- [Kwaliteitskoppelingen](quality-associations.md)
- [Processen voor kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
