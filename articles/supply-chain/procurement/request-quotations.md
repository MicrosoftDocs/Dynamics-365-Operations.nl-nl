---
title: Offerteaanvragen (RFQ's)
description: In dit onderwerp wordt een overzicht gegeven van offerteaanvragen, die organisaties uitgeven wanneer ze artikelen of services moeten aanschaffen en daarvoor concurrerende aanbiedingen van verschillende leveranciers willen ontvangen.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b817ffd905f1d3e99befc149416006e1a51f5e2
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="request-for-quotations-rfqs"></a>Offerteaanvragen (RFQ's)

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt een overzicht gegeven van offerteaanvragen, die organisaties uitgeven wanneer ze artikelen of services moeten aanschaffen en daarvoor concurrerende aanbiedingen van verschillende leveranciers willen ontvangen. In een offerteaanvraag vraagt u leveranciers welke prijzen en leveringstijden ze kunnen bieden voor de hoeveelheid artikelen die u opgeeft. U kunt leveranciers ook vragen om op te geven of er bijkomende kosten zijn, zoals verzendkosten, of kortingen voor grote orders of vroege betaling van de leveranciersfactuur.

Het proces van offerteaanvraag omvat de volgende taken:

-   Een offerteaanvraag maken en verzenden naar een of meer leveranciers.
-   Antwoorden op de offerteaanvraag (biedingen) ontvangen en registreren.
-   Geaccepteerde biedingen overboeken naar een inkooporder, inkoopovereenkomst of opdracht tot inkoop.

De volgende afbeelding geeft een overzicht van het proces voor offerteaanvragen.  

[![Offerteaanvraagproces](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

U kunt een offerteaanvraag maken op basis van geplande orders, een opdracht tot inkoop of een handmatige invoer. De offerteaanvraag die u maakt wordt een offerteaanvraagcase genoemd, en dit is het basisdocument dat u gebruikt om een offerteaanvraag aan elke leverancier uit te geven. Nadat u de offerteaanvraagcase hebt voorbereid en leveranciers hebt toegevoegd, klik u op **Verzenden** in de offerteaanvraagcase. Er wordt nu een offerteaanvraagjournaal gegenereerd voor elke leverancier die u de offerteaanvraag hebt toegestuurd. U kunt instellingen voor afdrukbeheer instellen voor de actie Verzenden om een rapport voor elke leverancier af te drukken naar een archief of om een rapport te verzenden naar het e-mailadres van elke leverancier. Bovendien kan het offerteaanvraagjournaal voor elke leverancier worden gebruikt om een rapport te genereren dat u later naar een leverancier kunt verzenden of opnieuw verzenden. U kunt ook de actie Verzenden zodanig configureren dat een antwoordblad wordt gegenereerd dat de leverancier kan invullen.  

Als u een offerteaanvraag moet wijzigen nadat u deze hebt verzonden, kunt u de offerteaanvraag opnieuw verzenden naar leveranciers wanneer u klaar bent.  

Wanneer u biedingen ontvangt, moet u deze invoeren op de pagina **Antwoorden op offerteaanvraag**. Als u de optie **Gegevens kopiëren naar antwoord** selecteert, worden gegevens zoals de hoeveelheid en de datums vanuit de offerteaanvraagcase in het antwoord gekopieerd. U kunt deze gegevens wijzigen om de bieding van de leverancier te reflecteren.  

Als een tweede herhaling van een antwoord is vereist voor een specifieke leverancier, klikt u op **Retour** op de pagina **Antwoord offerteaanvraag**. De actie Retour genereert een nieuw journaal en een rapport dat wordt afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor afdrukbeheer.  

Als u scoringscriteria aan uw offerteaanvraagcase hebt toegevoegd, heeft het antwoord op de offerteaanvraag een scorepaneel waarin u de scores kunt invoeren. De totale scores worden weergegeven wanneer u de antwoorden op de pagina **Antwoorden vergelijken** vergelijkt. Hier kunt u tevens andere antwoordgegevens vergelijken, zoals de regelprijs, leverdatum en totale prijs.  

Nadat u een beslissing hebt genomen over een bieding of een gedeeltelijk bieding, kunt u deze accepteren en de rest afwijzen. Er worden acceptatiejournalen, afwijzingsjournalen en overeenkomstige rapporten gegenereerd. Deze worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor afdrukbeheer. Als u een bieding of specifieke regels in een bieding accepteert, wordt een inkoopovereenkomst of inkooporder gegenereerd, of wordt een opdracht tot inkoop bijgewerkt, afhankelijk van het inkooptype van de offerteaanvraag. U kunt een handelsovereenkomst maken die u later voor alle antwoorden kunt gebruiken, ongeacht of u deze hebt geaccepteerd of afgewezen.  

De status van een offerteaanvraag wordt weergegeven in de koptekst van de offerteaanvraag en hangt af van de status van de offerteaanvraagregels. De status geeft aan in hoeverre u de offerteaanvraag hebt verwerkt. Elke offerteaanvraag heeft twee waarden voor de status: laagste en hoogste. De laagste status is het minst vergevorderde stadium van een regel in de offerteaanvraag en de hoogste status is het meest vergevorderde stadium van een regel in de offerteaanvraag. Als bijvoorbeeld het minst vergevorderde stadium in een offerteaanvraag voor een regel is die is gemaakt, is **Gemaakt** de laagste status voor de offerteaanvraag. Als het meest vergevorderde stadium in de offerteaanvraag voor een regel is die is verzonden aan leveranciers, is **Verzonden** de hoogste status voor de offerteaanvraag. De statussen worden automatisch bijgewerkt terwijl u een offerteaanvraag verwerkt.  

U kunt de laagste en hoogste status voor de koptekst van een offerteaanvraag bekijken op de pagina **Alle aanvragen voor offertes**. U kunt de laagste en hoogste status voor een regel van een offerteaanvraag bekijken op het tabblad **Regels** op de pagina **Offerteaanvragen**.  

Hier volgen de statussen voor het verwerken van offerteaanvragen:

1.  **Gemaakt**
2.  **Verzonden**
3.  **Ontvangen**
4.  **Geaccepteerd**/**Geannuleerd**/**Afgewezen**

De statussen worden nader beschreven in volgende onderdelen van dit onderwerp.

## <a name="setting-up-rfq-functionality"></a>Functionaliteit voor offerteaanvragen instellen
Voordat u een offerteaanvraagcase kunt maken, moet u offerteaanvraaggegevens instellen op de pagina **Parameters voor inkoop en sourcing**. Wanneer u een offerteaanvraagcase maakt, kunt u standaardwaarden opgeven die naar de offerteaanvraag worden gekopieerd. U kunt de volgende standaardwaarden opgeven:

-   Het inkooptype van nieuwe offerteaanvragen: **Inkooporder** of **Inkoopovereenkomst**.
-   Instellingen voor vervaldatum en -tijd.
-   Leveringsgegevens en betalingsvoorwaarden.
-   Velden die in het antwoord op de offerteaanvraag moeten worden opgenomen.

U kunt deze waarden negeren voor een specifieke offerteaanvraagcase. Configureer tevens het aanpassingsproces. Als onderdeel van deze configuratie, kunt u veldvergrendeling inschakelen. Wanneer veldvergrendeling is ingeschakeld, moet een inkoopmedewerker die een offerteaanvraag wil aanpassen eerst op **Maken** in de sectie **Aanpassing** van het tabblad **Offerte** klikken. Nadat de offerteaanvraag is bijgewerkt met de aanpassing, moet de inkoopmedewerker het proces uitvoeren door op **Voltooien** te klikken. Door de actie **Voltooien** wordt een e-mailbericht gegenereerd waarin aan de leveranciers de gewijzigde offerteaanvraag wordt gemeld. U selecteert de sjabloon voor de e-mailmelding die naar leveranciers wordt verzonden op de pagina **Parameters voor inkoop en sourcing**. Als een sjabloon wordt gemaakt, kan deze de volgende vervangingstokens bevatten:

-   %Reden voor retour van bieding%
-   %Reden voor aanpassing%
-   %Aanpassing voorbereid door%
-   %Bedrijf%

De tokens %Reden voor retour van biedng% en %Reden voor aanpassing% worden vervangen door tekst die de inkoopmedewerker kan invoeren wanneer hij of zij de aanpassing voltooid in de wizard **Aanpassing**. De waarden voor de tokens %Aanpassing voorbereid door% en %Bedrijf% worden automatisch opgehaald uit de offerteaanvraag.  

Als u redencodes wilt gebruiken in een antwoord op een offerteaanvraag om aan te geven waarom een bieding is afgewezen of geaccepteerd, moet u redencodes instellen op de pagina **Leveranciersredenen**.  

U kunt het uiterlijk van de afgedrukte of opgeslagen offerteaanvraagdocumenten configureren op de pagina **Formulierinstelling** in Inkoop en sourcing. 

**Opmerking:** voor een configuratie van de publieke sector is het bij wijzigingen in een reeds verzonden offerteaanvraag vereist om het wijzigingsproces te gebruiken. Wanneer de offerteaanvraag wordt verzonden, worden de velden vergrendeld. U moet dus op **Maken** klikken om het wijzigingsproces zoals hierboven is beschreven, te gebruiken bij wijzigingen in de offerteaanvraag.
Dit wordt bepaald door de vergrendelingsparameter **Offerteaanvragen vergrendelen wanneer ze zijn verzonden** in **Parameters voor inkoopbeheer**. Deze parameter is ingesteld op **Ja** en voor de configuratie van de publieke sector is dit een standaardinstelling die niet worden gewijzigd. Het wijzigingsproces kan dus handmatig worden verwerkt in een configuratie voor de niet-publieke sector, maar voor de publieke sector is het verplicht om de velden te vergrendelen nadat de offerteaanvraag is verzonden.

Wanneer u een offerteaanvraag voor een inkooporder maakt en een voorraadartikel toevoegt aan de offerteaanvraag, wordt een voorraadtransactie gegenereerd met de ontvangststatus **Offerte-ontvangst**. Alleen regels voor offerteaanvragen die deze status hebben worden in overweging genomen als u een hoofdplan gebruikt om leveringen te berekenen. Als u wilt dat het hoofdplan regels voor offerteaanvragen bevat als verwachte ontvangst, moet u dit gedrag in de instellingen van de hoofdplanning configureren.  

Als inkoopmanager of inkoper, kunt u verzoektypen maken en onderhouden om af te stemmen op de inkoopvereisten van uw organisatie. Elk verzoektype kan scoringsmethoden aansturen. Scoringsmethoden bestaan uit een set van criteria die kan worden gebruikt bij het toekennen van scores aan biedingen. U moet verzoektypen, scoringsmethoden en scoringscriteria instellen op de pagina's **Verzoektype** en **Scoringsmethode**.

## <a name="creating-and-sending-an-rfq"></a>Een offerteaanvraag maken en verzenden
U maakt een offerteaanvraag, selecteert de leveranciers die op de offerteaanvraag moeten reageren en verzendt de offerteaanvraag vervolgens naar de leveranciers. Met afdrukbeheer kunt u de route voor het offerteaanvraagrapport instellen en rapporten naar de gewenste bestemming verzenden.  

U kunt een offerteaanvraag maken voor het inkooptype **Inkooporder** of **Inkoopovereenkomst**.  

Als de offerteaanvraag wordt gegenereerd vanuit een inkoopaanvraag wordt automatisch het type **Opdracht tot inkoop** toegewezen. U kunt geen offerteaanvraag van het type **Opdracht tot inkoop** handmatig maken. Als de offerteaanvraag van het type **Inkooporder** is:

-   Wanneer offerteaanvraagregels worden gemaakt, worden voorraadtransacties gegenereerd die een ontvangststatus hebben van **Offerte-ontvangst**.
-   Als u een bieding accepteert, wordt een inkooporder gegenereerd.

Als de offerteaanvraag van het type **Inkoopovereenkomst** is:

-   De offerteaanvraag wordt gebruikt voor een overeenkomst voor aankoop van een specifieke hoeveelheid of waarde van een product in een bepaalde periode. U moet het datumbereik selecteren dat van toepassing is op de koopovereenkomst en de naam van de persoon die de koopovereenkomst beheert.
-   Als u een bieding accepteert, wordt een inkoopovereenkomst gegenereerd.

U kunt alleen een offerteaanvraag maken vanuit een opdracht tot inkoop als de status van de opdracht tot inkoop **Wordt gecontroleerd** is en de volgende workflowtaak aan u is toegewezen. De regels in de opdracht tot inkoop worden automatisch bijgewerkt als u regels accepteert van antwoorden op offerteaanvragen (biedingen) die u van leveranciers hebt ontvangen. U kunt de opdracht tot inkoop niet voltooien, afwijzen of goedkeuren of andere handelingen uitvoeren als de offerteaanvraag nog wordt verwerkt.  

Wanneer u een offerteaanvraag maakt, kunt u een specifiek verzoektype selecteren. Het verzoektype definieert de set van scoringscriteria die wordt gebruikt om antwoorden op de offerteaanvraag van een score te voorzien.  

U kunt een vragenlijst toevoegen aan een offerteaanvraagcase. Deze vragenlijst wordt vervolgens op alle antwoorden weergegeven nadat u de offerteaanvraag hebt verzonden.  

Er zijn drie manieren om de leveranciers te selecteren die u wilt toevoegen aan een offerteaanvraagcase:

-   De leveranciers één voor één toevoegen.
-   Zoeken naar alle leveranciers die aan specifieke criteria voldoen.
-   Automatisch alle leveranciers toevoegen die zijn goedgekeurd voor de inkoopcategorieën die op de regels van de offerteaanvraag worden gebruikt.

Wanneer de offerteaanvraagcase gereed is, klikt u op **Verzenden**. De actie Verzenden genereert journalen en rapporten die worden afgedrukt, gearchiveerd en verzonden, afhankelijk van uw instellingen voor afdrukbeheer.  

Als u de selectievakjes **Leverancier gebruiken voor herberekenen van prijzen** en **Leverancierspecifieke artikelgegevens gebruiken** hebt ingeschakeld op de pagina **Offerteaanvraag verzenden** tijdens het verzenden van de aanvraag naar leveranciers, wordt bepaalde leverancierspecifieke informatie automatisch ingevoerd. U kunt deze gegevens wijzigen op de pagina **Antwoord offerteaanvraag**.  

De volgende tabel laat zien hoe de status van een offerteaanvraag verandert wanneer u een offerteaanvraag maakt en naar leveranciers stuurt.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Actie**                         | **Laagste offerteaanvraagstatus** | **Hoogste offerteaanvraagstatus**                   | **Laagste offerteaanvraagregelstatus** | **Hoogste offerteaanvraagregelstatus** |
| De koptekst en regel van de offerteaanvraag maken.    | Gemaakt                      | Gemaakt                                         | Gemaakt                    | Gemaakt                     |
| Verzend de offerteaanvraag naar een specifieke leverancier. | Verzonden                         | Verzonden                                            | Verzonden                       | Verzonden                        |
| Nog een leverancier toevoegen.                | Gemaakt                      | Verzonden (De offerteaanvraag is verzonden aan slechts één leverancier.) | Gemaakt                    | Verzonden                        |
| Verzend de offerteaanvraag naar de tweede leverancier. | Verzonden                         | Verzonden                                            | Verzonden                       | Verzonden                        |

**Opmerking:** U kunt op elk gewenst moment meer leveranciers toevoegen aan een offerteaanvraag. De laagste en hoogste status veranderen en weerspiegelen de nieuwe leveranciers. Als u bijvoorbeeld biedingen hebt ontvangen van alle leveranciers en u ten minste één regel van een bieding hebt geaccepteerd, is de laagste status in de koptekst van de offerte **Afgewezen** en de hoogste status **Geaccepteerd**. Als u een nieuwe leverancier toevoegt, is de laagste status van een regel nu **Gemaakt**. Daarom wijzigt de laagste status van de offerteaanvraag naar **Gemaakt** en de hoogste status blijft **Geaccepteerd**.

## <a name="amending-an-rfq"></a>Een offerteaanvraag aanpassen
Nu en dan moet u een offerteaanvraag aanpassen nadat u deze hebt verzonden. Dit kan bijvoorbeeld gebeuren als de leveringsdatums zijn gewijzigd of u extra producten of verschillende hoeveelheden producten wilt. U kunt het aanpassingsproces configureren zodat het of meer of minder beperkend is.  

Als u het aanpassingsproces beperkter wilt maken, moet u op **Maken** op de offerteaanvraagcase klikken om een aanpassing te starten voordat u de velden op de offerteaanvraagcase kunt wijzigen. Wanneer u klaar bent met aanbrengen van wijzigingen, moet u op **Voltooien** klikken. U wordt dan begeleid door het proces om informatie toe te voegen voor het e-mailbericht dat wordt verzonden om leveranciers over de aanpassing te informeren. Het bijgewerkte offerteaanvraagrapport, dat een aanpassingsnotitie bevat, wordt automatisch aan het bericht gekoppeld.  

Als u het minder beperkende aanpassingsproces gebruikt, hoeft u geen aanpassing te maken voordat u de velden op een offerteaanvraagcase kunt wijzigen die al is verzonden. U moet echter handmatig een aanpassingsnotitie toevoegen aan de offerteaanvraag.

## <a name="receiving-and-registering-rfq-replies"></a>Antwoorden op een offerteaanvraag ontvangen en registreren
Wanneer u een offerteaanvraag verzendt, wordt automatisch een antwoordblad gegenereerd. Wanneer u antwoorden (biedingen) op een offerteaanvraag ontvangt, moet u de gegevens van elke leverancier invoeren op een leverancierspecifiek antwoordblad voor de offerteaanvraag. Als u scoringscriteria hebt toegevoegd, kunt u de antwoorden van een score voorzien. U vergelijkt vervolgens de biedingen van de leveranciers met elkaar en rangschikt deze op basis van uw scoringscriteria, zoals de beste totaalprijs of de beste totale leveringstijd.  

Als een vragenlijst is toegevoegd aan de offerteaanvraagcase, moet u de antwoorden op de vragen handmatig invoeren op het antwoordblad.  

Als u alternatieve regels moet invoeren, en de offerteaanvraagcase dit toestaat, klikt u op het sneltabblad **Inkoopofferteregels** op **Regel toevoegen**. Voer vervolgens de productinformatie in, zoals het artikelnummer of de inkoopcategorie, hoeveelheid, prijs en korting.  

Als u een antwoord hebt opgegeven maar een nieuwe offerte van de leverancier nodig hebt, kunt u de offerteaanvraag opnieuw verzenden. Hierbij wordt een nieuwe versie gegenereerd van het journaal en van het rapport dat u kunt gebruiken om de leverancier om wijzigingen te vragen.  

U kunt een overzicht bekijken van alle offerteaanvragen en hun antwoordstatussen op de pagina **Opvolging van offerteaanvraag**.  

In de volgende tabel wordt weergegeven hoe de offerteaanvraagstatus verandert wanneer u biedingen ontvangt en de informatie registreert op het antwoordblad voor de offerteaanvraag.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Actie**                                     | **Laagste biedingsstatus** | **Hoogste biedingsstatus** | **Laagste offerteaanvraagstatus** | **Hoogste offerteaanvraagstatus** | **Laagste offerteaanvraagregelstatus** | **Hoogste offerteaanvraagregelstatus** |
| Registreer een bod van de leverancier en sla dit op.        | Verzonden                  | Ontvangen               | Verzonden                         | Ontvangen                      | Verzonden                       | Ontvangen                    |
| Registreer het bod van de tweede leverancier en sla dit op. | Ontvangen              | Ontvangen               | Ontvangen                     | Ontvangen                      | Ontvangen                   | Ontvangen                    |

**Opmerking:** Als u een bieding terugstuurt naar een leverancier voor verdere onderhandelingen, blijven de laagste en hoogste status **Ontvangen**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Biedingen accepteren en afwijzen en geaccepteerde biedingen overbrengen naar documenten verderop in het traject

Wanneer u hebt bepaald wat de beste bieding is (bijvoorbeeld het antwoord met de beste totaalprijs), accepteert u de bieding. De status van het leverancierspecifieke antwoord op de offerteaanvraag wordt bijgewerkt in **Geaccepteerd**. Als u een bieding of specifieke regels in een bieding accepteert, wordt er automatisch een inkooporder of inkoopovereenkomst gegenereerd en kunt u de biedingen van de andere leveranciers afwijzen.  

Wanneer u een offerteaanvraag accepteert met een antwoord van het type **Opdracht tot inkoop**, worden de antwoordregels voor de offerteaanvraag bijgewerkt met de volgende gegevens:

-   Eenheidsprijs
-   Kortingspercentage
-   Kortingsbedrag
-   Inkooptoeslagen
-   Regelkosten
-   Leverancier
-   Extern nummer
-   Externe omschrijving

In het antwoord kunt u een redencode toevoegen om uit te leggen waarom u een bieding hebt geaccepteerd of afgewezen.  

U kunt bepaalde regels in een bieding accepteren en andere afwijzen. U kunt ook regels van verschillende leveranciers accepteren. Houd er rekening mee dat, als u bepaalde regels accepteert, u wordt gevraagd alle andere regels af te wijzigen. Als u dus andere regels wilt accepteren, moet u op **Annuleren** klikken als u de prompt ontvangt.  

De volgende tabel laat zien hoe de offerteaanvraagstatus verandert als u biedingen van leveranciers accepteert en afwijst.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Actie**              | **Laagste biedingsstatus** | **Hoogste biedingsstatus** | **Laagste offerteaanvraagstatus** | **Hoogste offerteaanvraagstatus** | **Laagste offerteaanvraagregelstatus** | **Hoogste offerteaanvraagregelstatus** |
| Accepteer een van de biedingen. | Ontvangen              | Geaccepteerd               | Ontvangen                     | Geaccepteerd                      | Ontvangen                   | Geaccepteerd                    |
| Wijs de andere biedingen af.  | Geweigerd              | Geaccepteerd               | Geweigerd                     | Geaccepteerd                      | Geweigerd                   | Geaccepteerd                    |






