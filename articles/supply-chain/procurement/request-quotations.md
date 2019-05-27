---
title: Offerteaanvragen
description: Dit onderwerp bevat een overzicht van offerteaanvragen. Organisaties geven offerteaanvragen uit wanneer ze concurrerende aanbiedingen van verschillende leveranciers willen ontvangen voor de artikelen of services die ze moeten kopen.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 714715ccfbdd57e4450c301f5302e008c0c136b1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571997"
---
# <a name="requests-for-quotation-rfqs"></a>Offerteaanvragen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van offerteaanvragen. Organisaties geven offerteaanvragen uit wanneer ze concurrerende aanbiedingen van verschillende leveranciers willen ontvangen voor de artikelen of services die ze moeten kopen. In een offerteaanvraag vraagt u leveranciers welke prijzen en leveringstijden ze kunnen bieden voor de hoeveelheid artikelen die u opgeeft.
U kunt leveranciers ook vragen om op te geven of er bijkomende kosten zijn, zoals verzendkosten, of kortingen voor grote orders of vroege betaling van de leveranciersfactuur.

Het proces voor offerteaanvragen bestaat uit de volgende taken:

1.  Een offerteaanvraag maken en verzenden naar een of meer leveranciers.

2.  Biedingen ontvangen en registreren (antwoorden op de offerteaanvraag).

3.  Geaccepteerde biedingen overboeken naar een inkooporder, inkoopovereenkomst of opdracht tot inkoop.

De volgende afbeelding biedt een overzicht van het proces voor offerteaanvragen.

[![RFQ-proces](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

U kunt een offerteaanvraagcase maken op basis van geplande orders, een opdracht tot inkoop of handmatige invoer. De offerteaanvraagcase is het basisdocument waarmee u een offerteaanvraag uitgeeft aan elke leverancier.+

Nadat u de offerteaanvraagcase hebt voorbereid en leveranciers hebt toegevoegd, selecteert u **Verzenden** (**Verzenden en publiceren** voor de openbare sector) op de offerteaanvraagcase. Er wordt een offerteaanvraagjournaal gemaakt voor elke leverancier waarnaar u een offerteaanvraag verzendt. U kunt afdrukopties configureren voor de actie Verzenden om een rapport voor elke leverancier af te drukken naar een archief of om een rapport te verzenden naar het e-mailadres van elke leverancier. Bovendien kunt u het offerteaanvraagjournaal voor elke leverancier gebruiken om een rapport te genereren dat u later kunt verzenden of opnieuw kunt verzenden naar een leverancier. U kunt de actie Verzenden ook zo configureren dat een antwoordblad wordt gegenereerd dat de leverancier kan invullen.

Dit onderwerp behandelt het proces voor het afhandelen van offerteaanvragen wanneer geen gebruik wordt gemaakt van leverancierssamenwerking. Als uw systeem is ingesteld voor leverancierssamenwerking, kunnen leveranciers rechtstreeks biedingen invoeren in Microsoft Dynamics 365 for Finance and Operations. Meer informatie vindt u in [Leverancierssamenwerking met klanten](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) en [Leverancierssamenwerking met externe leveranciers](vendor-collaboration-work-external-vendors.md).

Als u een offerteaanvraag moet wijzigen nadat u deze hebt verzonden, kunt u de offerteaanvraag na voltooiing opnieuw verzenden naar leveranciers met de twee aanpassingsacties: Maken en Voltooien.+

Wanneer u biedingen per e-mail ontvangt, moet u deze biedingen verwerken via de pagina **Offerteaanvragen**.

Als een tweede herhaling van een antwoord vereist is van een leverancier, selecteert u **Retour** op de pagina **Reactie offerteaanvraag**. De actie Retour genereert een nieuw journaal en een rapport dat wordt afgedrukt, gearchiveerd en verzonden, afhankelijk van uw afdrukinstellingen.

> [!NOTE]
> De naam van de pagina **Offerteaanvraag** is gewijzigd. In eerdere versies van Dynamics 365 for Finance and Operations heet deze pagina **Aanvraag voor offerteantwoord**.

Als u scoringscriteria aan uw offerteaanvraagcase hebt toegevoegd, heeft de offerteaanvraag een scorepaneel waarin u de scores kunt invoeren. De totale scores op de offerteaanvraag worden weergegeven wanneer u de antwoorden op de pagina **Antwoorden vergelijken** vergelijkt. Op de pagina **Antwoorden vergelijken** kunt u tevens andere antwoordgegevens vergelijken, zoals de regelprijs, leverdatum en totale prijs.

Nadat u een bod of een aantal regels in een bod hebt gekozen, kunt u alle of alleen bepaalde regels accepteren en de rest weigeren. Er worden acceptatiejournalen, afwijzingsjournalen en overeenkomstige rapporten gegenereerd die worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw afdrukinstellingen. Als u een bieding of specifieke regels in een bieding accepteert, wordt een inkoopovereenkomst of inkooporder gegenereerd, of wordt een opdracht tot inkoop bijgewerkt, afhankelijk van het inkooptype van de offerteaanvraag. U kunt een handelsovereenkomst maken die u later voor alle antwoorden kunt gebruiken, ongeacht of u deze hebt geaccepteerd of afgewezen.

Een offerteaanvraag heeft twee statuswaarden: laagste en hoogste. U kunt de status bekijken op de lijstpagina **Alle aanvragen voor offertes**. De laagste status is het minst vergevorderde stadium van een regel in de offerteaanvraagcase en de hoogste status is het meest vergevorderde stadium van een regel in de offerteaanvraagcase. Stel bijvoorbeeld dat een offerteaanvraagcase met drie regels naar twee leveranciers is verzonden, zodat er twee offerteaanvragen met drie regels zijn. Alle regels zijn **verzonden**. Nu wordt een bod ingevoerd van een van de leveranciers en de regels in de offerteaanvraag krijgen de status **Ontvangen**. Dit betekent dat de drie regels in de offerteaanvraagcase allemaal zijn **verzonden** voor een offerteaanvraag en zijn **ontvangen** voor een andere offerteaanvraag. De laagste status is **verzonden,** en de hoogste status is **ontvangen.**

De statussen worden verderop in dit onderwerp nader beschreven.

## <a name="setting-up-rfq-functionality"></a>Functionaliteit voor offerteaanvragen instellen

Voordat u een offerteaanvraagcase kunt maken, moet u offerteaanvraaggegevens instellen op de pagina **Parameters voor inkoop en sourcing**. Wanneer u een offerteaanvraagcase maakt, kunt u standaardwaarden opgeven die naar de offerteaanvraag worden gekopieerd. U kunt de volgende standaardwaarden opgeven:

-   Het inkooptype van nieuwe offerteaanvragen: **Inkooporder** of **Inkoopovereenkomst**

-   De verschuiving van vervaldatum en -tijd ten opzichte van de dag waarop de offerteaanvraagcase wordt gemaakt.

-   Aanvraag voor dit type, die standaard wordt ingesteld op een specifieke scoremethode voor de offerteaanvraagcase

-   Leveringsgegevens en betalingsvoorwaarden

-   Velden die in het antwoord op het bod moeten worden opgenomen.

U kunt deze waarden negeren voor een specifieke offerteaanvraagcase.

Configureer tevens het aanpassingsproces. Als onderdeel van deze configuratie, kunt u veldvergrendeling inschakelen. Wanneer veldvergrendeling is ingeschakeld, moet een inkoopmedewerker die een offerteaanvraag wil aanpassen, eerst **Maken** selecteren in de sectie **Aanpassing** van het tabblad **Offerte** van de offerteaanvraagcase. Nadat de offerteaanvraagcase is bijgewerkt met de wijziging, beëindigt de inkoper het proces door **Voltooien**  te selecteren. Door de actie Voltooien wordt een e-mail gegenereerd waarin aan de leveranciers de gewijzigde offerteaanvraag wordt gemeld.

U selecteert de sjabloon voor de e-mailmelding die naar leveranciers wordt verzonden op de pagina **Parameters voor inkoop en sourcing**. Als een sjabloon wordt gemaakt in **E-mailsjablonen**, kan deze de volgende vervangingstokens bevatten:

-   %Offerteaanvraagcase%

-   %Reden voor retour van bieding%

-   %Reden voor aanpassing%

-   %Aanpassing voorbereid door%

-   %Bedrijf%

-   %Naam offerteaanvraagcase%

-   %Vervaldatum/-tijd%

-   %Datum%

De tokens %Reden voor retour van biedng% en %Reden voor aanpassing% worden vervangen door tekst die de inkoopmedewerker kan invoeren wanneer hij of zij de aanpassing voltooid in de wizard **Aanpassing**. De waarden voor de tokens %Aanpassing voorbereid door% en %Bedrijf% worden automatisch opgehaald uit de offerteaanvraag. De token %Datum% wordt vervangen door de huidige datum.

Als u een offerteaanvraag annuleren wilt nadat deze verzonden, kunt u dat doen vanuit de offerteaanvraagcase. Voor het annuleren moet de e-mailsjabloon de annuleringsmelding verzenden naar contactpersonen van de leverancier. De sjabloon moet zijn geselecteerd op de pagina **Parameters voor inkoopbeheer**. Als de sjabloon wordt gemaakt, kan deze de volgende vervangingstokens bevatten:

-   %Annuleringsreden%

-   %Offerteaanvraagcase%

-   %Offerteaanvraag geannuleerd door%

-   %Bedrijf%

-   %Naam offerteaanvraagcase%

-   %Datum%

De token %Annuleringsreden% wordt vervangen door tekst die de inkoopmedewerker kan invoeren in de wizard **Annulering**. De token %Datum% wordt vervangen door de huidige datum.

Als u redencodes wilt gebruiken in een bieding om aan te geven waarom deze is afgewezen of geaccepteerd, moet u redencodes instellen op de pagina **Leveranciersredenen**.

U kunt het uiterlijk van de afgedrukte of opgeslagen offerteaanvraagdocumenten configureren op de pagina **Formulierinstelling** in Inkoopbeheer.

> [!NOTE]
> Voor een configuratie van de publieke sector is het bij wijzigingen in een reeds verzonden offerteaanvraag vereist om het wijzigingsproces te gebruiken. Wanneer een offerteaanvraag wordt verzonden, worden velden vergrendeld.
Als u de offerteaanvraag wilt wijzigen, moet u **Maken** dus selecteren om het wijzigingsproces te starten, zoals eerder beschreven. Het vergrendelingsgedrag wordt bepaald met de optie **Offerteaanvragen vergrendelen wanneer ze zijn verzonden** op de pagina **Parameters voor inkoopbeheer**. Deze parameter is standaard ingesteld op **Ja** en voor de configuratie van de publieke sector kan de standaardinstelling niet worden gewijzigd. Hoewel het aanpassingsproces handmatig kan worden verwerkt in een configuratie voor de niet-publieke sector, moet deze parameter worden gebruikt voor de configuratie van een publieke sector.

Wanneer u een offerteaanvraagcase van het type inkooporder maakt en een voorraadartikel toevoegt aan de offerteaanvraag, wordt een voorraadtransactie gegenereerd met de ontvangststatus **Offerte-ontvangst**. Alleen regels voor offerteaanvraagcase die deze status hebben worden in overweging genomen als u een hoofdplan gebruikt om leveringen te berekenen. Als u wilt dat het hoofdplan regels voor offerteaanvraagcases bevat als verwachte ontvangst, moet u dit gedrag in de instellingen van de hoofdplanning configureren.

Een inkoopmanager of inkoper kan verzoektypen maken en onderhouden om deze af te stemmen op de inkoopvereisten van uw organisatie. Elk verzoektype kan worden gekoppeld aan een scoringsmethode. Scoringsmethoden bestaan uit een set van criteria die kan worden gebruikt bij het toekennen van scores aan biedingen. U moet verzoektypen, scoringsmethoden en scoringscriteria instellen op de pagina's **Verzoektype** en **Scoringsmethode**.

## <a name="creating-and-sending-an-rfq"></a>Een offerteaanvraag maken en verzenden

U maakt een offerteaanvraagcase, selecteert de leveranciers die op de offerteaanvraagcase moeten reageren en verzendt de offerteaanvraag vervolgens naar de leveranciers. Met afdrukinstellingen kunt u de route voor het offerteaanvraagrapport instellen en rapporten naar de gewenste bestemming verzenden.

U kunt handmaitg een offerteaanvraagcase maken van het inkooptype **Inkooporder** of **Inkoopovereenkomst**.

Als de offerteaanvraagcase van het type **inkooporder** is, gebeurt het volgende wat afwijkt van andere soorten offerteaanvraagcases:

-   Wanneer regels voor een offerteaanvraagcase worden gemaakt, worden voorraadtransacties gegenereerd die een ontvangststatus hebben van **Offerte-ontvangst**.

-   Als u een bieding accepteert, wordt een inkooporder gegenereerd.

Als de offerteaanvraagcase van het type **inkoopovereenkomst** is, gebeurt het volgende wat afwijkt van andere soorten offerteaanvraagcases:

-   De offerteaanvraagcase wordt gebruikt voor een overeenkomst voor aankoop van een specifieke hoeveelheid of waarde van een product in een bepaalde periode. U moet het datumbereik selecteren dat van toepassing is op de koopovereenkomst en de naam van de persoon die de koopovereenkomst beheert.

-   Als u een bieding accepteert, wordt een inkoopovereenkomst gegenereerd.

Als de offerteaanvraagcase wordt gegenereerd vanuit een inkoopaanvraag wordt automatisch het type **Opdracht tot inkoop** toegewezen. U kunt geen offerteaanvraagcase van het type **Opdracht tot inkoop** handmatig maken.

U kunt alleen een offerteaanvraagcase maken vanuit een opdracht tot inkoop als de status van de opdracht tot inkoop **Wordt gecontroleerd** is en de volgende workflowtaak aan u is toegewezen. De regels in de opdracht tot inkoop worden automatisch bijgewerkt als u regels accepteert van biedingen (antwoorden op offerteaanvragen) die u van leveranciers hebt ontvangen. U kunt niet andere acties voltooien, afwijzen, goedkeuren of uitvoeren op de opdracht tot inkoop, totdat de inkoopregel wordt bijgewerkt met een geaccepteerde offerteaanvraagregel of tot de offerteaanvraagcase wordt geannuleerd.

Wanneer u een offerteaanvraagcase maakt, kunt u een verzoektype selecteren. Het verzoektype definieert de set van scoringscriteria die wordt gebruikt om antwoorden op de offerteaanvraagcase van een score te voorzien.

U kunt een vragenlijst toevoegen aan een offerteaanvraagcase. Deze vragenlijst wordt vervolgens op alle antwoorden op de offerteaanvraag weergegeven nadat u de offerteaanvraag hebt verzonden. De voltooiing van de vragenlijst is een verplichte taak voordat het bod kan worden aangeboden.


Er zijn drie manieren om de leveranciers te selecteren die u wilt toevoegen aan een offerteaanvraagcase:

- De leveranciers één voor één toevoegen.
- Zoeken naar alle leveranciers die aan specifieke criteria voldoen.
- Automatisch alle leveranciers toevoegen die zijn goedgekeurd voor de inkoopcategorieën die op de regels van de offerteaanvraagcase worden gebruikt.

Wanneer de offerteaanvraagcase gereed is, selecteert u **Verzenden**. De actie Verzenden genereert journalen en rapporten die worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw afdrukinstellingen.

Als u tijdens het verzenden van de aanvraag naar een leverancier **Leverancier gebruiken voor herberekenen van prijzen** en **Leverancierspecifieke artikelgegevens gebruiken** op **Ja** instelt op de pagina **Offerteaanvraag verzenden**, wordt bepaalde leverancierspecifieke informatie automatisch ingevoerd in de offerteaanvraag voor die leverancier.


## <a name="amending-an-rfq-case"></a>Een offerteaanvraagcase aanpassen

Nu en dan moet u een offerteaanvraagcase aanpassen nadat u deze hebt verzonden. U kunt een offerteaanvraagcase bijvoorbeeld wijzigen als de leveringsdatums zijn gewijzigd of als u extra producten of verschillende hoeveelheden producten wilt. U kunt het aanpassingsproces zo configureren dat het meer of minder beperkend is.

Als u het aanpassingsproces zo wilt configureren dat het meer beperkend is, moet u **Maken** in de offerteaanvraagcase selecteren om de velden te kunnen wijzigen in een offerteaanvraagcase die al is verzonden. Wanneer u klaar bent met aanbrengen van wijzigingen, moet u **Voltooien** selecteren. U wordt dan begeleid door het proces om informatie toe te voegen voor de e-mail die wordt verzonden om leveranciers over de aanpassing te informeren. Het bijgewerkte offerteaanvraagrapport, dat een aanpassingsnotitie bevat, wordt automatisch aan de e-mail gekoppeld.

Als u het minder beperkende aanpassingsproces wilt gebruiken, hoeft u **Maken** niet te selecteren voordat u de velden kunt wijzigen in een offerteaanvraagcase die al is verzonden. U moet wel handmatig een aanpassingsnotitie toevoegen aan de offerteaanvraag en de case opnieuw verzenden. Deze benadering kan alleen worden gebruikt als geen van de antwoorden (biedingen) is bewerkt. Als u een antwoord hebt ingevoerd en dit de status **Ontvangen** heeft, is de knop **Verzenden** niet beschikbaar. In dit geval moet u **Maken** en vervolgens **Voltooien** selecteren, zoals in het meer beperkende proces. Het antwoord wordt vervolgens opnieuw ingesteld op basis van de wijzigingen in de offerteaanvraagcase.

Als leveranciers de interface voor leverancierssamenwerking gebruiken om biedingen in te voeren, moet u het aanpassingsproces altijd gebruiken om leveranciers op de hoogte brengen van wijzigingen in de offerteaanvraagcase. Dit proces voorkomt een situatie waarin leveranciers bieden op een verouderde offerteaanvraagcase terwijl hun bod wordt uitgevoerd. Meer informatie over de nieuwe functionaliteit voor leverancierssamenwerking vindt u in [Leverancierssamenwerking met externe leveranciers](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Als u extra leveranciers wilt uitnodigen om te bieden en er geen wijzigingen zijn aangebracht in de offerteaanvraagcase, kunt u de knop **Verzenden** gebruiken. De leveranciers die u hebt toegevoegd, worden weergegeven op de pagina **Verzenden** en ontvangen de e-mailuitnodiging.


## <a name="receiving-and-registering-rfq-replies"></a>Antwoorden op een offerteaanvraag ontvangen en registreren

Wanneer u een offerteaanvraag verzendt, wordt automatisch een antwoordblad gegenereerd. Als u biedingen op een offerteaanvraag ontvangt, moet u deze via de pagina **Offerteaanvraag** invoeren door te klikken op de actie **Antwoord op offerteaanvraag bewerken.** Hier kunt u de biedingsgegevens invoeren op een specifieke biedingsformulier. In eerste instantie staat **Voortgang van reactie** op **Niet gestart**. Wanneer u op **Reactie op offerteaanvraag bewerken** klikt, is de voortgangsstatus **Inkoper is bezig met bijwerken** totdat de bieding is verzonden. Klik op **Indienen** wanneer u de biedingsinformatie hebt ingevoerd. De voortgangsstatus van het antwoord wordt gewijzigd in **Ingediend door de inkoper.** Als leverancierssamenwerking is ingeschakeld, wordt op dezelfde manier **Voortgang van reactie** bijgewerkt als de leverancier reageert op de bieding. De status wordt vervolgens gewijzigd van **Leverancier is bezig met bijwerken** naar **Ingediend door leverancier**. Wanneer het bod wordt ingediend, wordt een journaal gemaakt als **Ontvangen**. De reactie (bieding) moet worden ingediend om te worden geregistreerd als ontvangen en kan dan pas verder worden verwerkt als geaccepteerd of afgewezen.

Als u de bieding wilt bijwerken, moet u hetzelfde proces als hierboven doorlopen en opnieuw indienen.

Houd er rekening mee dat bewerken van het formulier **Offerteaanvraag** alleen is toegestaan voor informatie met betrekking tot het verwerken van het bod, niet voor het invoeren van het bod. Als u het boed wilt invoeren of wijzigen, klikt u op **Reactie op offerteaanvraag bewerken.**

Wanneer u de biedingsinformatie invoert en de offerteaanvraagcase alternatieve regels toestaat, kunt u alternatieve regels toevoegen voor regels met alleen een aanschaffingscategorie en geen catalogusartikel. Klik op **Alternatief toevoegen** om alternatieve regels toe te voegen.

Als u een antwoord hebt opgegeven maar een nieuwe offerte van de leverancier nodig hebt, kunt u de offerteaanvraag terugsturen. Er worden een nieuw journaal en een nieuw rapport gegenereerd, die naar de leverancier kunnen worden verzonden.

U kunt een overzicht bekijken van alle offerteaanvragen en hun statussen (**verzonden, ontvangen, geaccepteerd, afgewezen, geannuleerd, geweigerd**) op de pagina **Opvolging van offerteaanvraag**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Biedingen accepteren en afwijzen en geaccepteerde biedingen overbrengen naar documenten verderop in het traject

Wanneer u hebt bepaald wat de beste bieding is (bijvoorbeeld het antwoord met de beste totaalprijs), accepteert u de bieding. U kunt bepaalde regels in een bieding accepteren en andere afwijzen.
U kunt ook regels van verschillende leveranciers accepteren. Als u bepaalde regels accepteert, wordt u gevraagd alle andere regels af te wijzigen. Als u dus andere regels wilt accepteren, moet u **Annuleren** selecteren als deze vraag wordt weergegeven. De status van het antwoord op de offerteaanvraag voor elke leverancier waarvoor u biedingen of regels accepteert, wordt bijgewerkt naar **Geaccepteerd**.

Als u tijdens het voorbereiden van de inkooporder of inkoopovereenkomst een extra regel moet toevoegen aan de offerteaanvraag, kunt u dat doen door te klikken op **Regel toevoegen** op het regelraster op de pagina **Offerteaanvraag** . U kunt deze regel alleen weergeven en bewerken op de pagina **Offerteaanvraag**. De regel wordt weergegeven op de biedingspagina wanneer deze is geaccepteerd.

Als u een bod of een of meer regels in een bod accepteert, wordt er automatisch een inkooporder of inkoopovereenkomst gegenereerd. Vervolgens kunt u de biedingen van de andere leveranciers afwijzen.

In het antwoord kunt u een redencode toevoegen om uit te leggen waarom u een bieding hebt geaccepteerd of afgewezen.

Wanneer u een bod accepteert van het type **Opdracht tot inkoop**, worden de regels van de opdracht tot inkoop bijgewerkt met de volgende informatie die de gegevens van het geaccepteerde bod weergeven:

-   Eenheidsprijs

-   Kortingspercentage

-   Kortingsbedrag

-   Toeslagen op inkoop

-   Regelkosten

-   Leverancier

-  Extern nummer

-   Externe omschrijving


De volgende tabel laat zien hoe de offerteaanvraagstatus verandert als u biedingen van leveranciers accepteert en afwijst.

<a name="statuses--highest-and-lowest"></a>Status: hoogste en laagste.
-----------------------------

Op het tabblad Leverancier van de offerteaanvraagcase ziet u de regels met de hoogste en laagste status voor een bepaalde leverancier. Wanneer de leverancier wordt toegevoegd en er nog geen regels zijn verzonden, zijn de laagste en hoogste status beide <strong>Gemaakt</strong>. Wanneer de offerteaanvraag wordt verzonden naar de leverancier met alle regels, is de status van de twee regels <strong>Verzonden</strong>. Als sommige regels in een bod van een leverancier worden geaccepteerd en andere worden geweigerd, krijgen de afgewezen regels de laagste status van <strong>Afgewezen</strong> en krijgen de geaccepteerde regels de hoogste status <strong>Geaccepteerd</strong>.

Op de regels van de offerteaanvraagcase ziet u de hoogste en de laagste status per regel voor alle leveranciers. Als u een regel hebt verzonden naar alle leveranciers in de offerteaanvraagcase en nog niemand heeft gereageerd, is de laagste en de hoogste status **Verzonden.** Wanneer ten minste één leverancier reageert, wordt de hoogste status gewijzigd in **Ontvangen**. Als u een nieuwe leverancier aan de case toevoegt, wordt de laagste status gewijzigd in **Gemaakt**

De hoogste en de laagste status op de offerteaanvraagcase is een samenvoeging van de status van de \<tabbladen Leverancier en Regels.

De statussen zijn gerangschikt in de volgende manier van laag naar hoog: gemaakt, verzonden, ontvangen, afgewezen, geaccepteerd, geweigerd, geannuleerd.

De volgende tabel laat zien hoe de status van een offerteaanvraagcase verandert wanneer u een offerteaanvraagcase met regels maakt en deze naar leveranciers stuurt.

| **Actie**                                | **Laagste status van offerteaanvraagcase** | **Hoogste status van offerteaanvraagcase** | **Laagste status van regel van offerteaanvraagcase** | **Hoogste status van regel van offerteaanvraagcase** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| De koptekst en regel van de offerteaanvraagcase maken.      | Gemaakt op                    | Gemaakt op                     | Gemaakt op                         | Gemaakt op                          |
| Offerteaanvragen naar alle leveranciers in de offerteaanvraagcase verzenden. | Verzonden                       | Verzonden                        | Verzonden                            | Verzonden                             |
| Nog een leverancier toevoegen.                       | Gemaakt op                    | Verzonden                        | Gemaakt op                         | Verzonden                             |
| Verzend de offerteaanvraag naar de tweede leverancier.        | Verzonden                       | Verzonden                        | Verzonden                            | Verzonden                             |

Alle regels van de offerteaanvragen die zijn gerelateerd aan de offerteaanvraagcase, hebben de status **Cerzonden**.

In de volgende tabel wordt weergegeven hoe de offerteaanvraagstatus verandert wanneer u biedingen ontvangt en de informatie registreert op het antwoordblad voor de offerteaanvraag.

| **Actie**                                               | **Laagste status voor alle regels op alle offerteaanvragen** | **Hoogste status voor alle regels op alle offerteaanvragen** | **Laagste koptekststatus van offerteaanvraag** | **Hoogste koptekststatus van offerteaanvraag** | **Laagste status van regel van offerteaanvraagcase** | **Hoogste status van regel van offerteaanvraagcase** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Registreer een bod van de leverancier in een offerteaanvraag en sla dit op.        | Verzonden                                           | Ontvangen                                        | Verzonden                              | Ontvangen                           | Verzonden                            | Ontvangen                         |
| Registreer het bod van de tweede leverancier in een offerteaanvraag en sla dit op. | Ontvangen                                       | Ontvangen                                        | Ontvangen                          | Ontvangen                           | Ontvangen                        | Ontvangen                         |


In het voorbeeld hieronder ziet u de hoogste en laagste status op de offerteaanvraagcase waarbij één bod is ontvangen en het andere bod is aanvaard. Wanneer een ontvangen bod wordt afgewezen, wordt de laagste status gewijzigd van ontvangen in afgewezen in de koptekst en de regel van de offerteaanvraagcase.


|            <strong>Actie</strong>             | <strong>Laagste status voor alle regels op alle offerteaanvragen</strong> | <strong>Hoogste status voor alle regels op alle offerteaanvragen</strong> | <strong>Laagste koptekststatus van offerteaanvraag</strong> | <strong>Hoogste koptekststatus van offerteaanvraag</strong> | <strong>Laagste status van regel van offerteaanvraagcase</strong> | <strong>Hoogste status van regel van offerteaanvraagcase</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Accepteer een van de biedingen. (of ten minste één regel) |                          Ontvangen                           |                           Geaccepteerd                           |                    Ontvangen                    |                    Geaccepteerd                     |                   Ontvangen                   |                   Geaccepteerd                    |
|           Wijs alle andere biedingen af.           |                          Afgewezen                           |                           Geaccepteerd                           |                    Afgewezen                    |                    Geaccepteerd                     |                   Afgewezen                   |                   Geaccepteerd                    |

