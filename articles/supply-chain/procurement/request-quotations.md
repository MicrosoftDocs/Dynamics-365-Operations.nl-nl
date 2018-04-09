---
title: Offerteaanvragen
description: Dit onderwerp bevat een overzicht van offerteaanvragen. Organisaties geven offerteaanvragen uit wanneer ze concurrerende aanbiedingen van verschillende leveranciers willen ontvangen voor de artikelen of services die ze moeten kopen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b86363004b8702d1a654f2a1da49bba82fc8ff2a
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="requests-for-quotation-rfqs"></a>Offerteaanvragen

[!include[banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van offerteaanvragen. Organisaties geven offerteaanvragen uit wanneer ze concurrerende aanbiedingen van verschillende leveranciers willen ontvangen voor de artikelen of services die ze moeten kopen. In een offerteaanvraag vraagt u leveranciers welke prijzen en leveringstijden ze kunnen bieden voor de hoeveelheid artikelen die u opgeeft. U kunt leveranciers ook vragen om op te geven of er bijkomende kosten zijn, zoals verzendkosten, of kortingen voor grote orders of vroege betaling van de leveranciersfactuur.

Het proces voor offerteaanvragen bestaat uit de volgende taken:

1. Een offerteaanvraag maken en verzenden naar een of meer leveranciers.
2. Antwoorden op de offerteaanvraag ontvangen en registreren (biedingen).
3. Geaccepteerde biedingen overboeken naar een inkooporder, inkoopovereenkomst of opdracht tot inkoop.

De volgende afbeelding biedt een overzicht van het proces voor offerteaanvragen.

[![RFQ-proces](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

U kunt een offerteaanvraag maken op basis van geplande orders, een opdracht tot inkoop of handmatige invoer. De offerteaanvraag die u maakt, wordt een offerteaanvraagcase genoemd. De offerteaanvraagcase is het basisdocument waarmee u een offerteaanvraag uitgeeft aan elke leverancier.

Wanneer u de offerteaanvraagcase hebt voorbereid en leveranciers hebt toegevoegd, selecteert u **Verzenden** voor de offerteaanvraagcase. Er wordt een offerteaanvraagjournaal gemaakt voor elke leverancier waarnaar u een offerteaanvraag verzendt. U kunt instellingen voor afdrukbeheer instellen voor de actie Verzenden om een rapport voor elke leverancier af te drukken naar een archief of om een rapport te verzenden naar het e-mailadres van elke leverancier. Bovendien kunt u het offerteaanvraagjournaal voor elke leverancier gebruiken om een rapport te genereren dat u later kunt verzenden of opnieuw kunt verzenden naar een leverancier. U kunt de actie Verzenden ook zo configureren dat een antwoordblad wordt gegenereerd dat de leverancier kan invullen.

Dit onderwerp behandelt het proces voor het afhandelen van offerteaanvragen wanneer geen gebruik wordt gemaakt van leverancierssamenwerking. Als uw systeem is ingesteld voor leverancierssamenwerking, kunnen leveranciers biedingen rechtstreeks invoeren in Microsoft Dynamics 365 for Finance and Operations. Zie voor meer informatie [Leverancierssamenwerking met klanten](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Als u een offerteaanvraag moet wijzigen nadat u deze hebt verzonden, kunt u de offerteaanvraag na voltooiing opnieuw verzenden naar leveranciers met de twee aanpassingsacties: Maken en Voltooien.

Wanneer u biedingen per e-mail ontvangt, moet u deze invoeren op de pagina **Antwoorden op offerteaanvraag**. Als u de optie **Gegevens kopiëren naar antwoord** selecteert, worden gegevens zoals de hoeveelheid en de datums vanuit de offerteaanvraagcase in het antwoord gekopieerd. U kunt deze gegevens wijzigen om de bieding van de leverancier te reflecteren.

Als een tweede herhaling van een antwoord vereist is voor een specifieke leverancier, selecteert u **Retour** op de pagina **Antwoord offerteaanvraag**. De actie Retour genereert een nieuw journaal en een rapport dat wordt afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor afdrukbeheer.

Als u scoringscriteria aan uw offerteaanvraagcase hebt toegevoegd, heeft het antwoord op de offerteaanvraag een scorepaneel waarin u de scores kunt invoeren. De totale scores worden weergegeven wanneer u de antwoorden op de pagina **Antwoorden vergelijken** vergelijkt. Op deze pagina kunt u tevens andere antwoordgegevens vergelijken, zoals de regelprijs, leverdatum en totale prijs.

Nadat u een beslissing hebt genomen over een bieding of een gedeeltelijke bieding, kunt u deze accepteren en de rest afwijzen. Er worden acceptatiejournalen, afwijzingsjournalen en overeenkomstige rapporten gegenereerd die worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor afdrukbeheer. Als u een bieding of specifieke regels in een bieding accepteert, wordt een inkoopovereenkomst of inkooporder gegenereerd, of wordt een opdracht tot inkoop bijgewerkt, afhankelijk van het inkooptype van de offerteaanvraag. U kunt een handelsovereenkomst maken die u later voor alle antwoorden kunt gebruiken, ongeacht of u deze hebt geaccepteerd of afgewezen.

De status van een offerteaanvraag wordt weergegeven in de koptekst van de offerteaanvraag en hangt af van de status van de offerteaanvraagregels. Met de status wordt aangegeven in hoeverre u de offerteaanvraag hebt verwerkt. Elke offerteaanvraag heeft twee statuswaarden: een laagste en hoogste waarde. De laagste status is het minst vergevorderde stadium van een regel in de offerteaanvraag en de hoogste status is het meest vergevorderde stadium van een regel in de offerteaanvraag. Als bijvoorbeeld het minst vergevorderde stadium in een offerteaanvraag voor een regel is die is gemaakt, is **Gemaakt** de laagste status voor de offerteaanvraag. Als het meest vergevorderde stadium in de offerteaanvraag voor een regel is die is verzonden aan leveranciers, is **Verzonden** de hoogste status voor de offerteaanvraag. De statussen worden automatisch bijgewerkt terwijl u een offerteaanvraag verwerkt.

U kunt de laagste en hoogste status voor de koptekst van een offerteaanvraag bekijken op de pagina **Alle aanvragen voor offertes**. U kunt de laagste en hoogste status voor een regel van een offerteaanvraag bekijken op het tabblad **Regels** op de pagina **Offerteaanvragen**.

Hier volgen de statussen voor het verwerken van offerteaanvragen:

1. **Gemaakt**
2. **Verzonden**
3. **Ontvangen**
4. **Geaccepteerd**, **Geannuleerd** of **Afgewezen**

De statussen worden verderop in dit onderwerp nader beschreven.

## <a name="setting-up-rfq-functionality"></a>Functionaliteit voor offerteaanvragen instellen

Voordat u een offerteaanvraagcase kunt maken, moet u offerteaanvraaggegevens instellen op de pagina **Parameters voor inkoop en sourcing**. Wanneer u een offerteaanvraagcase maakt, kunt u standaardwaarden opgeven die naar de offerteaanvraag worden gekopieerd. U kunt de volgende standaardwaarden opgeven:

- Het inkooptype van nieuwe offerteaanvragen: **Inkooporder** of **Inkoopovereenkomst**
- De vervaldatum en -tijd
- Leveringsgegevens en betalingsvoorwaarden
- Velden die in het antwoord op de offerteaanvraag moeten worden opgenomen

U kunt deze waarden negeren voor een specifieke offerteaanvraagcase.

Configureer tevens het aanpassingsproces. Als onderdeel van deze configuratie, kunt u veldvergrendeling inschakelen. Wanneer veldvergrendeling is ingeschakeld, moet een inkoopmedewerker die een offerteaanvraag wil aanpassen eerst **Maken** selecteren in de sectie **Aanpassing** van het tabblad **Offerte**. Als de offerteaanvraag is bijgewerkt met de aanpassing, moet de inkoopmedewerker het proces uitvoeren door **Voltooien** te selecteren. Door de actie Voltooien wordt een e-mail gegenereerd waarin aan de leveranciers de gewijzigde offerteaanvraag wordt gemeld.

U selecteert de sjabloon voor de e-mailmelding die naar leveranciers wordt verzonden op de pagina **Parameters voor inkoop en sourcing**. Als een sjabloon wordt gemaakt, kan deze de volgende vervangingstokens bevatten:

- %Offerteaanvraagcase%
- %Reden voor retour van bieding%
- %Reden voor aanpassing%
- %Aanpassing voorbereid door%
- %Bedrijf%
- %Naam offerteaanvraagcase%
- %ExpiryDateTime%
- %Datum%

De tokens %Reden voor retour van biedng% en %Reden voor aanpassing% worden vervangen door tekst die de inkoopmedewerker kan invoeren wanneer hij of zij de aanpassing voltooid in de wizard **Aanpassing**. De waarden voor de tokens %Aanpassing voorbereid door% en %Bedrijf% worden automatisch opgehaald uit de offerteaanvraag. De token %Datum% wordt vervangen door de huidige datum.

Een e-mailsjabloon is ook vereist als u een offerteaanvraag annuleert nadat deze is verzonden. Deze e-mailsjabloon wordt gebruikt om de annuleringsmelding te verzenden naar contactpersonen van de leverancier. De sjabloon moet zijn geselecteerd op de pagina **Parameters voor inkoopbeheer**. Als de sjabloon wordt gemaakt, kan deze de volgende vervangingstokens bevatten:

- %Annuleringsreden%
- %Offerteaanvraagcase% 
- %Offerteaanvraag geannuleerd door%
- %Bedrijf%
- %Naam offerteaanvraagcase%
- %Datum%

De token %Annuleringsreden% wordt vervangen door tekst die de inkoopmedewerker kan invoeren in de wizard **Annulering**. De token %Datum% wordt vervangen door de huidige datum.

Als u redencodes wilt gebruiken in een antwoord op een offerteaanvraag om aan te geven waarom een bieding is afgewezen of geaccepteerd, moet u redencodes instellen op de pagina **Leveranciersredenen**.

U kunt het uiterlijk van de afgedrukte of opgeslagen offerteaanvraagdocumenten configureren op de pagina **Formulierinstelling** in Inkoopbeheer.

> [!NOTE]
> Voor een configuratie van de publieke sector is het bij wijzigingen in een reeds verzonden offerteaanvraag vereist om het wijzigingsproces te gebruiken. Wanneer een offerteaanvraag wordt verzonden, worden velden vergrendeld. Als u de offerteaanvraag wilt wijzigen, moet u **Maken** dus selecteren om het wijzigingsproces te starten, zoals eerder beschreven. Het vergrendelingsgedrag wordt bepaald met de optie **Offerteaanvragen vergrendelen wanneer ze zijn verzonden** op de pagina **Parameters voor inkoopbeheer**. Deze parameter is standaard ingesteld op **Ja** en voor de configuratie van de publieke sector kan de standaardinstelling niet worden gewijzigd. Hoewel het aanpassingsproces handmatig kan worden verwerkt in een configuratie voor de niet-publieke sector, moet deze parameter worden gebruikt voor de configuratie van een publieke sector.

Wanneer u een offerteaanvraag voor een inkooporder maakt en een voorraadartikel toevoegt aan de offerteaanvraag, wordt een voorraadtransactie gegenereerd met de ontvangststatus **Offerte-ontvangst**. Alleen regels voor offerteaanvragen die deze status hebben worden in overweging genomen als u een hoofdplan gebruikt om leveringen te berekenen. Als u wilt dat het hoofdplan regels voor offerteaanvragen bevat als verwachte ontvangst, moet u dit gedrag in de instellingen van de hoofdplanning configureren.

Een inkoopmanager of inkoper kan verzoektypen maken en onderhouden om deze af te stemmen op de inkoopvereisten van uw organisatie. Elk verzoektype kan worden gekoppeld aan een scoringsmethode. Scoringsmethoden bestaan uit een set van criteria die kan worden gebruikt bij het toekennen van scores aan biedingen. U moet verzoektypen, scoringsmethoden en scoringscriteria instellen op de pagina's **Verzoektype** en **Scoringsmethode**.

## <a name="creating-and-sending-an-rfq"></a>Een offerteaanvraag maken en verzenden

U maakt een offerteaanvraag, selecteert de leveranciers die op de offerteaanvraag moeten reageren en verzendt de offerteaanvraag vervolgens naar de leveranciers. Met Afdrukbeheer kunt u de route voor het offerteaanvraagrapport instellen en rapporten naar de gewenste bestemming verzenden.

U kunt een offerteaanvraag maken van het inkooptype **Inkooporder** of **Inkoopovereenkomst**.

Als de offerteaanvraag van het type **Inkooporder** is, treedt het volgende gedrag op:

- Wanneer offerteaanvraagregels worden gemaakt, worden voorraadtransacties gegenereerd die een ontvangststatus hebben van **Offerte-ontvangst**.
- Als u een bieding accepteert, wordt een inkooporder gegenereerd.

Als de offerteaanvraag van het type **Inkoopovereenkomst** is, treedt het volgende gedrag op:

- De offerteaanvraag wordt gebruikt voor een overeenkomst voor aankoop van een specifieke hoeveelheid of waarde van een product in een bepaalde periode. U moet het datumbereik selecteren dat van toepassing is op de koopovereenkomst en de naam van de persoon die de koopovereenkomst beheert.
- Als u een bieding accepteert, wordt een inkoopovereenkomst gegenereerd.

Als de offerteaanvraag wordt gegenereerd vanuit een inkoopaanvraag wordt automatisch het type **Opdracht tot inkoop** toegewezen. U kunt geen offerteaanvraag van het type **Opdracht tot inkoop** handmatig maken.

U kunt alleen een offerteaanvraag maken vanuit een opdracht tot inkoop als de status van de opdracht tot inkoop **Wordt gecontroleerd** is en de volgende workflowtaak aan u is toegewezen. De regels in de opdracht tot inkoop worden automatisch bijgewerkt als u regels accepteert van antwoorden op offerteaanvragen (biedingen) die u van leveranciers hebt ontvangen. U kunt de opdracht tot inkoop niet voltooien, afwijzen of goedkeuren of andere handelingen uitvoeren als de offerteaanvraag nog wordt verwerkt.

Wanneer u een offerteaanvraag maakt, kunt u een verzoektype selecteren. Het verzoektype definieert de set van scoringscriteria die wordt gebruikt om antwoorden op de offerteaanvraag van een score te voorzien.

U kunt een vragenlijst toevoegen aan een offerteaanvraagcase. Deze vragenlijst wordt vervolgens op alle antwoorden weergegeven nadat u de offerteaanvraag hebt verzonden.

Er zijn drie manieren om de leveranciers te selecteren die u wilt toevoegen aan een offerteaanvraagcase:

- De leveranciers één voor één toevoegen.
- Zoeken naar alle leveranciers die aan specifieke criteria voldoen.
- Automatisch alle leveranciers toevoegen die zijn goedgekeurd voor de inkoopcategorieën die op de regels van de offerteaanvraag worden gebruikt.

Wanneer de offerteaanvraagcase gereed is, selecteert u **Verzenden**. De actie Verzenden genereert journalen en rapporten die worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor Afdrukbeheer.

Als u tijdens het verzenden van de aanvraag naar leveranciers **Leverancier gebruiken voor herberekenen van prijzen** en **Leverancierspecifieke artikelgegevens gebruiken** op **Ja** instelt op de pagina **Offerteaanvraag verzenden**, wordt bepaalde leverancierspecifieke informatie automatisch ingevoerd. U kunt deze gegevens wijzigen op de pagina **Antwoord offerteaanvraag**.

De volgende tabel laat zien hoe de status van een offerteaanvraag verandert wanneer u een offerteaanvraag maakt en naar leveranciers stuurt.

| Actie                             | Laagste offerteaanvraagstatus | Hoogste offerteaanvraagstatus                        | Laagste offerteaanvraagregelstatus | Hoogste offerteaanvraagregelstatus |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| De koptekst en regel van de offerteaanvraag maken.    | Gemaakt                  | Gemaakt                                          | Gemaakt                | Gemaakt |
| Verzend de offerteaanvraag naar een specifieke leverancier. | Verzonden                     | Verzonden                                             | Verzonden                   | Verzonden |
| Nog een leverancier toevoegen.                | Gemaakt                  | Verzonden (De offerteaanvraag is verzonden aan slechts één leverancier.) | Gemaakt                | Verzonden |
| Verzend de offerteaanvraag naar de tweede leverancier. | Verzonden                     | Verzonden                                             | Verzonden                   | Verzonden |

> [!NOTE]
> U kunt op elk moment meer leveranciers toevoegen aan een offerteaanvraag. De laagste en hoogste status worden bijgewerkt en weerspiegelen de toegevoegde leveranciers. Als u bijvoorbeeld biedingen hebt ontvangen van alle leveranciers en u ten minste één regel van een bieding hebt geaccepteerd, is de laagste status in de koptekst van de offerte **Afgewezen** en de hoogste status **Geaccepteerd**. Als u een nieuwe leverancier toevoegt, is de laagste status van een regel nu **Gemaakt**. Daarom wordt de laagste status van de offerteaanvraag in **Gemaakt** gewijzigd, maar de hoogste status blijft **Geaccepteerd**.

## <a name="amending-an-rfq"></a>Een offerteaanvraag aanpassen

Nu en dan moet u een offerteaanvraag aanpassen nadat u deze hebt verzonden. U kunt een offerteaanvraag bijvoorbeeld wijzigen als de leveringsdatums zijn gewijzigd of als u extra producten of verschillende hoeveelheden producten wilt. U kunt het aanpassingsproces zo configureren dat het meer of minder beperkend is.

Als u het aanpassingsproces zo wilt configureren dat het meer beperkend is, moet u **Maken** in de offerteaanvraagcase selecteren om de velden te kunnen wijzigen in een offerteaanvraagcase die al is verzonden. Wanneer u klaar bent met aanbrengen van wijzigingen, moet u **Voltooien** selecteren. U wordt dan begeleid door het proces om informatie toe te voegen voor de e-mail die wordt verzonden om leveranciers over de aanpassing te informeren. Het bijgewerkte offerteaanvraagrapport, dat een aanpassingsnotitie bevat, wordt automatisch aan de e-mail gekoppeld.

Als u het minder beperkende aanpassingsproces wilt gebruiken, hoeft u **Maken** niet te selecteren voordat u de velden kunt wijzigen in een offerteaanvraagcase die al is verzonden. U moet wel handmatig een aanpassingsnotitie toevoegen aan de offerteaanvraag en de case opnieuw verzenden. Deze benadering kan alleen worden gebruikt als geen van de antwoorden (biedingen) is bewerkt. Als u een antwoord hebt ingevoerd en dit de status **Ontvangen** heeft, is de knop **Verzenden** niet beschikbaar. In dit geval moet u **Maken** en vervolgens **Voltooien** selecteren, zoals in het meer beperkende proces. Het antwoord wordt vervolgens opnieuw ingesteld op basis van de wijzigingen in de offerteaanvraagcase. 

Als leveranciers de interface voor leverancierssamenwerking gebruiken om biedingen in te voeren, moet u het aanpassingsproces altijd gebruiken om leveranciers op de hoogte brengen van wijzigingen in de offerteaanvraagcase. Deze vereiste voorkomt een situatie waarin leveranciers bieden op een verouderde offerteaanvraagcase terwijl hun bod wordt uitgevoerd. Meer informatie over de nieuwe functionaliteit voor leverancierssamenwerking vindt u in [Leverancierssamenwerking met externe leveranciers](vendor-collaboration-work-external-vendors.md). 

Als u extra leveranciers wilt uitnodigen om te bieden en er geen wijzigingen zijn aangebracht in de offerteaanvraagcase, kunt u de knop **Verzenden** gebruiken. De leveranciers die u hebt toegevoegd, worden weergegeven op de pagina **Verzenden** en ontvangen de e-mailuitnodiging.

## <a name="receiving-and-registering-rfq-replies"></a>Antwoorden op een offerteaanvraag ontvangen en registreren

Wanneer u een offerteaanvraag verzendt, wordt automatisch een antwoordblad gegenereerd. Wanneer u antwoorden (biedingen) op een offerteaanvraag ontvangt, moet u de gegevens van elke leverancier invoeren op een leverancierspecifiek antwoordblad voor de offerteaanvraag. Als u scoringscriteria hebt toegevoegd, kunt u de antwoorden van een score voorzien. U vergelijkt vervolgens de biedingen van de leveranciers met elkaar en rangschikt deze op basis van uw scoringscriteria, zoals de beste totaalprijs of de beste totale leveringstijd.

Als een vragenlijst is toegevoegd aan de offerteaanvraagcase, moet u de antwoorden op de vragen handmatig invoeren op het antwoordblad.

U kunt ook alternatieve regels invoeren, als de offerteaanvraagcase alternatieve regels toestaat. Selecteer op het sneltabblad **Inkoopofferteregels** de optie **Regel toevoegen**. Voer vervolgens de productinformatie in, zoals het artikelnummer of de inkoopcategorie, hoeveelheid, prijs en korting.

Als u een antwoord hebt opgegeven maar een nieuwe offerte van de leverancier nodig hebt, kunt u de offerteaanvraag opnieuw verzenden. Er worden nieuwe versies van het journaal en rapport gegenereerd die u kunt gebruiken om de leverancier om wijzigingen te vragen.

U kunt een overzicht bekijken van alle offerteaanvragen en hun antwoordstatussen op de pagina **Opvolging van offerteaanvraag**.

In de volgende tabel wordt weergegeven hoe de offerteaanvraagstatus verandert wanneer u biedingen ontvangt en de informatie registreert op het antwoordblad voor de offerteaanvraag.

| Actie                                         | Laagste biedingsstatus | Hoogste biedingsstatus | Laagste offerteaanvraagstatus | Hoogste offerteaanvraagstatus | Laagste offerteaanvraagregelstatus | Hoogste offerteaanvraagregelstatus |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Registreer een bod van de leverancier en sla dit op.        | Verzonden              | Ontvangen           | Verzonden                     | Ontvangen                  | Verzonden                   | Ontvangen |
| Registreer het bod van de tweede leverancier en sla dit op. | Ontvangen          | Ontvangen           | Ontvangen                 | Ontvangen                  | Ontvangen               | Ontvangen |

> [!NOTE]
> Als u een bod terugstuurt naar een leverancier voor verdere onderhandelingen, blijven de laagste en hoogste status **Ontvangen**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Biedingen accepteren en afwijzen en geaccepteerde biedingen overbrengen naar documenten verderop in het traject

Wanneer u hebt bepaald wat de beste bieding is (bijvoorbeeld het antwoord met de beste totaalprijs), accepteert u de bieding. U kunt bepaalde regels in een bieding accepteren en andere afwijzen. U kunt ook regels van verschillende leveranciers accepteren. Als u bepaalde regels accepteert, wordt u gevraagd alle andere regels af te wijzigen. Als u dus andere regels wilt accepteren, moet u **Annuleren** selecteren als deze vraag wordt weergegeven. De status van het antwoord op de offerteaanvraag voor elke leverancier waarvoor u biedingen of regels accepteert, wordt bijgewerkt naar **Geaccepteerd**. 

Als u een bod of specifieke regels in een bod accepteert, wordt er automatisch een inkooporder of inkoopovereenkomst gegenereerd. Vervolgens kunt u de biedingen van de andere leveranciers afwijzen.

In het antwoord kunt u een redencode toevoegen om uit te leggen waarom u een bieding hebt geaccepteerd of afgewezen.

Wanneer u een offerteaanvraag accepteert met een antwoord van het type **Opdracht tot inkoop**, worden de antwoordregels voor de offerteaanvraag bijgewerkt met de volgende gegevens:

- Eenheidsprijs
- Kortingspercentage
- Kortingsbedrag
- Inkooptoeslagen
- Regelkosten
- Leverancier
- Extern nummer
- Externe omschrijving

De volgende tabel laat zien hoe de offerteaanvraagstatus verandert als u biedingen van leveranciers accepteert en afwijst.

| Actie                      | Laagste biedingsstatus | Hoogste biedingsstatus | Laagste offerteaanvraagstatus | Hoogste offerteaanvraagstatus | Laagste offerteaanvraagregelstatus | Hoogste offerteaanvraagregelstatus |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Accepteer een van de biedingen.     | Ontvangen          | Geaccepteerd           | Ontvangen                 | Geaccepteerd                  | Ontvangen               | Geaccepteerd |
| Wijs alle andere biedingen af.  | Afgewezen          | Geaccepteerd           | Afgewezen                 | Geaccepteerd                  | Afgewezen               | Geaccepteerd |

