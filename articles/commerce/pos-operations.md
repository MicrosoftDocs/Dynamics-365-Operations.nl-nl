---
title: Online en offline verkooppuntbewerkingen (POS)
description: Dit onderwerp bevat meer informatie over POS-bewerkingen (Point Of Sale) in Dynamics 365 Commerce. Hier wordt aangegeven waar in de toepassing de bewerkingen kunnen worden aangeroepen en of deze beschikbaar zijn in de offlinemodus.
author: jblucher
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c62e11cc6d39c351321419bb862a5169b162fb7
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349712"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Online en offline verkooppuntbewerkingen (POS)

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

De meeste acties die gebruikers uitvoeren in POS worden beschouwd als bewerkingen. Bewerkingen worden geconfigureerd en beheerd in de back-office van Dynamics 365 Commerce. Veel bewerkingen kunnen worden toegevoegd aan knoppen in het POS-knoppenraster. Gebruikers kunnen de knoppen vervolgens selecteren om de bewerkingen aan te roepen en hun functie uit te voeren. Andere bewerkingen maken deel uit van de POS-hoofdtoepassing en worden aangeroepen via schermknoppen of als onderdeel van andere workflows of processen.

De volgende tabel bevat informatie over de bewerkingen die beschikbaar zijn in Modern POS en Cloud POS. In de tabel wordt ook aangegeven waar in de toepassing de bewerkingen kunnen worden aangeroepen en of deze beschikbaar zijn als het POS zich in de offlinemodus bevindt.

Bepaalde bewerkingen zijn op dit moment niet beschikbaar in Modern POS of Cloud POS. Sommige van deze bewerkingen zijn landspecifieke bewerkingen die mogelijk extra extensies en configuratie vereisen. Andere bewerkingen zijn functies van Microsoft Dynamics AX 2012 die momenteel niet worden ondersteund.

In de volgende kolommen wordt aangeven waar de bewerkingen kunnen worden aangeroepen:

- **Knoppenraster**: de bewerking kan worden toegewezen aan knoppen in POS-knoppenrasters, die deel uitmaken van een POS-schermindeling.
- **Transactiescherm**: de bewerking kan worden aangeroepen via POS-knoppenrasters die zijn geconfigureerd in het POS-transactiescherm.
- **Welkomstscherm**: de bewerking kan worden aangeroepen via POS-knoppenrasters die zijn geconfigureerd in het POS-welkomstscherm.

> [!NOTE]
> De onderstaande bewerkingen gelden voor de meest recente versie van Commerce. Sommige bewerkingen zijn mogelijk gewijzigd of mogelijk niet beschikbaar in eerdere versies.


| ID | Bewerking | Omschrijving | Knoppenraster | Transactiescherm | Welkomstscherm | Offline beschikbaar | Landspecifiek |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Apparaat activeren | Het huidige apparaat activeren door een geverifieerde gebruiker in staat te stellen verbindingsgegevens op te geven en een apparaat en kassa-id toe te wijzen. | Nee | Nee | Nee | Nee | Nee |
| 134 | Aansluiting toevoegen | Een vooraf geselecteerde aansluiting toevoegen aan een transactie. Selecteer de aansluiting op de pagina **Knopeigenschappen**. | Ja | Ja | Nee | Ja | Nee |
| 135 | Aansluiting toevoegen vanuit lijst | Een aansluiting toevoegen aan een transactie door deze te selecteren in een lijst. | Ja | Ja | Ja | Ja | Nee |
| 137 | Een aansluiting aan een klant toevoegen | Voeg een aansluiting aan een klant toe op de pagina **Details klant**. | Nee | Nee | Nee | Ja | Nee |
| 138 | Aansluiting van klant verwijderen | Verwijder een aansluiting van een klant op de pagina **Details klant**. | Nee | Nee | Nee | Ja | Nee |
| 643 | Couponcode toevoegen | Een coupon toevoegen door de couponcode in te voeren in het POS. | Ja | Ja | Nee | Ja | Nee |
| 141 | Toeslagen koptekst toevoegen | Een toeslag van het type Diversen toevoegen aan de orderkoptekst. | Ja | Ja | Nee | Nee| Nee |
| 141 | Regeltoeslagen toevoegen | Een toeslag van het type Diversen toevoegen aan een geselecteerde verkoopregel. | Ja | Ja | Nee | Nee| Nee |
| 117 | Loyaliteitskaart toevoegen | De gebruiker wordt gevraagd om het nummer van een loyaliteitskaart in te voeren, dat vervolgens wordt toegevoegd aan de huidige transactie. | Ja | Ja | Nee | Ja | Nee |
| 136 | Serienummer toevoegen | Met deze bewerking kan de gebruiker een serienummer voor het geselecteerde product opgeven. | Ja | Ja | Nee | Ja | Nee |
| 1214 | Verzendadres toevoegen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 519 | Toevoegen aan geschenkbon | Voeg geld toe aan de opgegeven geschenkbon. | Ja | Ja | Nee | Nee | Nee |
| 6000 | Overslaan van fiscale registratie toestaan | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 1212 | Bankstorting | Registreer het bedrag dat naar de bank is verzonden en andere gegevens, zoals het nummer van de stortingsenveloppe. | Ja | Ja | Ja | Ja | Nee |
| 923 | Verificatie van banktotalen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 915 | Lege bewerking | Deze bewerking vertegenwoordigt een aanpasbare knop die door een softwareontwikkelaar kan worden geprogrammeerd voor een speciale bewerking die het bedrijf nodig heeft. | Ja | Ja | Ja | Ja | Nee |
| 1053 | Ploeg blind sluiten | De huidige ploeg instellen op blind sluiten en de gebruiker afmelden. Een blind gesloten ploeg is gesloten voor extra transacties, maar is nog wel open voor ladebewerkingen, zoals het verwijderen van de betalingsmethode en kascontrole. | Ja | Ja | Ja | Nee | Nee |
| 310 | Totaal berekenen | Wanneer de berekening van korting is vertraagd, wordt met deze bewerking de berekening voor de huidige transactie geïnitieerd. | Ja | Ja | Nee | Ja | Nee |
| 642 | Alle producten uitvoeren | De leveringsmethode voor alle regels instellen op **Uitvoeren**. | Ja | Ja | Nee | Ja\* | Nee |
| 641 | Geselecteerde producten uitvoeren | De leveringsmethode voor de geselecteerde regels instellen op **Uitvoeren**. | Ja | Ja | Nee | Ja\* | Nee |
| 647 | Leveringsmethode wijzigen | De leveringsmodus voor vooraf geconfigureerde verzendverkoopregels wijzigen. | Ja | Ja | Nee | Nee| Nee |
| 1215 | Wachtwoord wijzigen | Met deze bewerking kan de POS-gebruiker zijn of haar wachtwoord wijzigen. | Ja | Ja | Ja | Nee | Nee |
| 123 | Maateenheid wijzigen | De maateenheid voor het geselecteerde regelartikel wijzigen. | Ja | Ja | Nee | Ja | Nee |
| 639 | Standaard verkoopvertegenwoordiger wissen voor transactie | De provisieverkoopgroep (vertegenwoordiger) verwijderen uit de transactie. | Ja | Ja | Nee | Ja | Nee |
| 106 | Hoeveelheid wissen | De hoeveelheid op de geselecteerde regel opnieuw instellen op **1**. | Ja | Ja | Nee | Ja | Nee |
| 640 | Verkoopvertegenwoordiger wissen op regel | De provisieverkoopgroep (vertegenwoordiger) verwijderen van de geselecteerde regel. | Ja | Ja | Nee | Ja | Nee |
| 121 | Verkoper wissen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 1055 | Ploeg sluiten | De huidige ploeg sluiten, een Z-rapport afdrukken en de gebruiker afmelden bij het systeem. | Ja | Ja | Ja | Nee | Nee |
| 139 | Transactie afsluiten | De gebruiker wordt gevraagd de betalingsmethode te selecteren | Ja | Ja | Nee | Ja | Nee |
| 925 | De bankcheque kopiëren | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 620 | Klantorder maken | De POS-transactie omzetten in een klantorder. | Ja | Ja | Nee | Ja\* | Nee |
| 621 | Offerte maken | De POS-transactie omzetten in een verkoopofferte. | Ja | Ja | Nee | Ja\* | Nee |
| 636 | Detailhandelstransactie maken | Een standaardverkooptransactie maken wanneer het standaardgedrag voor POS het maken van klantorders is. | Ja | Ja | Nee | Ja | Nee |
| 600 | Klant | Voeg de opgegeven klant toe aan de transactie. | Nee | Nee | Nee | Ja | Nee |
| 1100 | Klantrekeningdeposito | Een betaling uitvoeren naar de rekening van een klant. | Ja | Ja | Ja | Ja | Ja |
| 612 | Klant toevoegen | Een nieuwe klantregistratie maken. | Ja | Ja | Ja | Ja† | Nee |
| 603 | Klant wissen | De klant verwijderen uit de huidige transactie. | Ja | Ja | Nee | Ja | Nee |
| 602 | Klant zoeken | Een klantregistratie zoeken door te navigeren naar de pagina voor het zoeken van klanten in het POS. | Ja | Ja | Ja | Ja | Nee |
| 609 | Klanttransacties | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 917 | Status van databaseverbinding | De huidige verbindingsinstellingen weergeven en schakelen tussen online- en offlinemodi. | Ja | Ja | Ja | Ja | Nee |
| 1200 | Beginbedrag declareren | Het bedrag in de kassalade aan het begin van de dag of werktijd registreren. | Ja | Ja | Ja | Ja | Nee |
| 132 | Deposito overschrijven | Het standaard deposito voor orders van klanten negeren. | Ja | Ja | Nee | Ja\* | Nee |
| 913 | Ontwerpmodus uitschakelen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 912 | Ontwerpmodus inschakelen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 1217 | Kits demonteren | Een kit demonteren naar componentproducten. | Ja | Ja | Ja | Ja | Nee |
| 624 | Restitutiebedragen weergeven | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 513 | Totaal weergeven | Het saldo van de transactie in de klantweergave weergeven. | Ja | Ja | Ja | Ja | Nee |
| 623 | Klant bewerken | Details van de huidige klant bewerken. | Ja | Ja | Nee | Nee | Nee |
| 614 | Klantorder bewerken | De geselecteerde order intrekken zodat deze kan worden gewijzigd in het POS. | Nee | Nee | Nee | Nee | Nee |
| 615 | Offerte bewerken | De geselecteerde offerte intrekken zodat deze kan worden gewijzigd in het POS. | Nee | Nee | Nee | Nee | Nee |
| 518 | Uitgavenrekeningen | Het geld registreren dat voor incidentele uitgaven uit de kassalade wordt genomen. | Ja | Ja | Ja | Ja | Nee |
| 919 | Uitgebreide aanmelding | De machtiging voor aanmelding door een streepjescode te scannen of een kaart door de lezer te halen, toewijzen of verwijderen. | Ja | Ja | Ja | Ja | Nee |
| 1201 | Wisselgeldinvoer | Extra geld toevoegen aan de huidige lade of ploeg. | Ja | Ja | Ja | Ja | Nee |
| 1218 | Ontgrendelen van randapparaat forceren | Deze bewerking wordt intern door het systeem gebruikt voor het ontgrendelen van POS-randapparatuur. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 520 | Geschenkbonsaldo | Het huidige saldo van een geschenkbon weergeven. | Ja | Ja | Nee | Nee | Nee |
| 708 | Apparaat deactiveren | Het huidige apparaat uitschakelen zodat het niet kan worden gebruikt als een POS-kassa. | Nee | Nee | Nee | Nee | Nee |
| 804 | inkomende bewerking | Toegang verkrijgen tot de functies van inkomend winkelvoorraadbeheer. | Ja | Nee | Ja | Nee| Nee |
| 517 | Inkomstenrekeningen | Het geld registreren dat om een andere reden dan een verkoop in de kassalade wordt gedaan. | Ja | Ja | Ja | Ja | Nee |
| 801 | Zoeken in voorraad | Beschikbare hoeveelheden, hoeveelheden in bestelling en ATP-hoeveelheden (available-to-promise) voor de huidige winkel en andere beschikbare locaties opzoeken. | Ja | Ja | Ja | Nr. | Nr. |
| 806 | Voorraadcorrectie | Voorraad in of uit het winkelmagazijn aanpassen met behulp van een correctie- of mutatiejournaal. | Ja | Ja | Ja | Nr. | Nr. |
| 807 | Voorraadmutatie | Artikelen verplaatsen van de ene voorraadlocatie naar de andere verplaatsen in een winkelmagazijn. | Ja | Ja | Ja | Nr. | Nr. |
| 122 | Factuuropmerking | Een opmerking over de huidige transactie invoeren. | Ja | Ja | Nee | Ja | Nee |
| 511 | Creditnota uitgeven | Een creditnota uitgeven om een boekstuk op te geven in plaats van een restitutie. | Ja | Ja | Nee | Nee | Nee |
| 512 | Geschenkbon uitgeven | Een nieuwe geschenkbon uitgeven voor het opgegeven bedrag. | Ja | Ja | Nee | Nee | Nee |
| 625 | Loyaliteitskaart uitgeven | Een loyaliteitskaart uitgeven aan een klant, zodat deze kan deelnemen aan het loyaliteitsprogramma van de winkel. | Ja | Ja | Ja | Nee | Nee |
| 300 | Kortingsbedrag voor regelitem | Voer een kortingsbedrag in voor een regelartikel in de transactie. Deze bewerking wordt alleen gebruikt voor kortingsartikelen en alleen binnen de opgegeven kortingslimieten. | Ja | Ja | Nee | Ja | Nee |
| 301 | Kortingspercentage voor regelitem | Voer een kortingspercentage in voor een regelartikel in de transactie. Deze bewerking wordt alleen gebruikt voor kortingsartikelen en alleen binnen de opgegeven kortingslimieten. | Ja | Ja | Nee | Ja | Nee |
| 703 | Kassa vergrendelen | De huidige kassa vergrendelen zodat deze niet kan worden gebruikt, maar de huidige gebruiker niet afmelden. | Nee | Nee | Nee | Ja | Nee |
| 701 | Afmelden | De huidige gebruiker afmelden bij de kassa. | Ja | Ja | Ja | Ja | Nee |
| 521 | Balans van loyaliteitskaartpunten | De balans van punten voor de opgegeven loyaliteitskaart weergeven. | Ja | Ja | Nee | Nee | Nee |
| 142 | Toeslagen beheren | Diverse toeslagen die op de transactie zijn toegepast, weergeven en beheren. | Ja | Ja | Nee | Nee| Nee |
| 918 | Ploegen beheren | Een lijst weergeven met actieve, uitgestelde en blind gesloten ploegen. | Ja | Ja | Ja | Nee | Nee |
| 914 | POS-venster minimaliseren | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 1000 | Lade openen | Een niet-verkoopbewerking uitvoeren en de momenteel geselecteerde kassalade openen. | Ja | Ja | Ja | Ja | Nee |
| 928 | Orderafhandeling | Met deze bewerking kunnen gebruikers orders voor afhalen in de winkel verzamelen, verpakken, verzenden of intrekken. | Ja | Ja | Ja | Nee | Nee |
| 805 | Uitgaande bewerking | Toegang verkrijgen tot functies voor het beheren van zendingen van uitgaande overboekingsorders. | Ja | Nee | Ja | Nee| Nee |
| 129 | Btw voor regelproducten overschrijven | Het btw-tarief voor het geselecteerde regelartikel overschrijven en een ander opgegeven btw-tarief gebruiken. | Ja | Ja | Nee | Ja | Nee |
| 130 | Btw voor regelproducten overschrijven vanuit lijst | Het btw-tarief voor het geselecteerde regelartikel overschrijven en het tarief gebruiken dat de gebruiker selecteert in een lijst. | Ja | Ja | Nee | Ja | Nee |
| 127 | Btw voor transacties overschrijven | Het btw-tarief voor de transactie overschrijven en een ander opgegeven tarief gebruiken. | Ja | Ja | Nee | Ja | Nee |
| 128 | Btw voor transacties overschrijven vanuit lijst | Het btw-tarief voor de transactie overschrijven en het tarief gebruiken dat de gebruiker in een lijst selecteert. | Ja | Ja | Nee | Ja | Nee |
| 131 | Pakbon | Een pakbon voor de geselecteerde order maken. | Nee | Nee | Nee | Nee | Nee |
| 710 | Hardwarestation koppelen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 201 | Betaalkaart | Een kaart als een creditcard of betaalpas accepteren als betaling. | Ja | Ja | Nee | Ja | Nee |
| 200 | Contant betalen | Accepteer een betaling met contant geld. | Ja | Ja | Nee | Ja | Nee |
| 206 | Snel contant betalen | De transactie met één toets voltooien en het verschuldigde bedrag accepteren (gepast geld). | Ja | Ja | Nee | Ja | Nee |
| 204 | Betalen met cheque | Een cheque accepteren als betaling. | Ja | Ja | Nee | Ja | Nee |
| 213 | Betalen met creditnota | Een creditnota accepteren (boekstuk) die door de winkel is uitgegeven. | Ja | Ja | Nee | Nee | Nee |
| 203 | Betalen met valuta | Accepteer een betaling in diverse valuta. | Ja | Ja | Nee | Ja | Nee |
| 202 | Betalen met klantrekening | De transactie in rekening brengen van de rekening van een klant. Deze betalingsmethode is niet geldig voor de klantorderstortingen. | Ja | Ja | Nee | Nee | Nee |
| 214 | Betalen met geschenkbon | Een door de winkel uitgegeven geschenkbon accepteren. | Ja | Ja | Nee | Nee | Nee |
| 207 | Loyaliteitskaart betalen | Een loyaliteitskaart accepteren voor de betaling en punten inwisselen voor in aanmerking komende producten. | Ja | Ja | Nee | Nee | Nee |
| 634 | Betalingsgeschiedenis | De betalingshistorie van de klant voor de huidige klantorder weergeven. | Ja | Ja | Nee | Nee | Nee |
| 803 | Verzamelen en ontvangen | De pagina **Verzamelen en ontvangen** openen waarop u orders kunt selecteren om te verzamelen of te ontvangen in de winkel. | Ja | Ja | Ja | Nee | Nee |
| 632 | Alle producten afhalen | De uitvoermethode instellen op **Afhalen in winkel** voor alle regels. | Ja | Ja | Nee | Ja\* | Nee |
| 631 | Geselecteerde producten afhalen | De uitvoermethode instellen op **Afhalen in winkel** voor geselecteerde regels. | Ja | Ja | Nee | Ja\* | Nee |
| 400 | Pop-upmenu | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 101 | Prijscontrole | Met deze bewerking kan de gebruiker de prijs voor een opgegeven product opzoeken. | Ja | Ja | Ja | Ja | Nee |
| 104 | Prijsaanpassing | De prijs van een product overschrijven als prijsoverschrijvingen zijn toegestaan voor het product. | Ja | Ja | Nee | Ja | Nee |
| 1058 | Fiscale X afdrukken | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 1059 | Fiscale Z afdrukken | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 927 | Artikeletiket afdrukken | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 926 | Planketiket afdrukken | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 1056 | X afdrukken | Een X-rapport afdrukken voor de huidige ploeg. | Ja | Ja | Ja | Nee | Nee |
| 103 | Productopmerking | Voeg een opmerking toe aan het geselecteerde regelartikel in de transactie. | Ja | Ja | Nee | Ja | Nee |
| 100 | Productverkoop | Een opgegeven product toevoegen aan de transactie. | Ja | Ja | Ja | Ja | Nee |
| 108 | Artikel zoeken | Een product zoeken door te navigeren naar de pagina voor het zoeken van producten in het POS. | Ja | Ja | Ja | Ja | Nee |
| 633 | Vervaldatum van offerte | De vervaldatum op een verkoopofferte weergeven of wijzigen. | Ja | Ja | Nee | Ja\* | Nee |
| 627 | Opnieuw berekenen | Alle klantorderregels en btw opnieuw berekenen, op basis van de huidige configuratie. | Ja | Ja | Nee | Ja\* | Nee |
| 143 | Toeslagen opnieuw berekenen | De automatische toeslagen die op de order zijn toegepast, opnieuw berekenen. | Ja | Ja | Nee | Nee| Nee |
| 515 | Order intrekken | Klantorders en verkoopoffertes zoeken en intrekken. | Ja | Ja | Ja | Nee | Nee |
| 504 | Transactie intrekken | Een eerder uitgestelde transactie voor de huidige winkel intrekken. | Ja | Ja | Nee | Ja‡ | Nee |
| 305 | Loyaliteitspunten inwisselen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 635 | Verzendkosten terugbetalen | Verzendkosten voor een geannuleerde order terugbetalen. | Nee | Nee | Nee | Nee | Nee |
| 644 | Couponcode verwijderen | De gebruiker vragen om coupons te verwijderen door ze te selecteren in een lijst met coupons die aan de transactie zijn gekoppeld. | Ja | Ja | Nee | Ja | Nr. |
| 1057 | Z opnieuw afdrukken | Het Z-rapport voor de vorige ploeg opnieuw afdrukken. | Ja | Ja | Ja | Nr. | Nr. |
| 1216 | Voer een nieuw wachtwoord in | Met deze bewerking kan een gebruiker met de machtiging voor het opnieuw instellen van wachtwoorden het wachtwoord van een andere werknemer opnieuw instellen met behulp van een tijdelijk wachtwoord. | Ja | Ja | Ja | Nee | Nee |
| 1219 | URL openen in POS | In POS een URL openen die is geconfigureerd door een beheerder. | Ja | Ja | Ja | Ja | Nee |
| 109 | Product retourneren | Afzonderlijke producten retourneren. Het volgende gescande product wordt weergegeven als een geretourneerd product met een negatieve hoeveelheid en prijs. | Ja | Ja | Nee | Ja | Nee |
| 114 | Retourtransactie | Een eerdere transactie op basis van het ontvangstbewijsnummer intrekken om sommige of alle producten terug te halen. | Ja | Ja | Ja | Ja§ | Nee |
| 1211 | Kluisstorting | Voer een kluisstorting uit om geld van een kassa naar een kluis te verplaatsen. | Ja | Ja | Ja | Ja | Nee |
| 516 | Verkoopfactuur | Met deze bewerking kan de klant betalingen doen voor de geselecteerde verkoopfactuur. | Ja | Ja | Nee | Nee | Nee |
| 502 | Verkoper | De waarde voor **Verkoopafnemer** in een verkooporder instellen voor klantorders in het POS. | Ja | Ja | Nee | Ja\* | Nee |
| 2000 | Beheer plannen | Deze bewerking wordt nog niet ondersteund. | Ja | Ja | Ja | Nee | Nee |
| 2001 | Aanvragen plannen | Deze bewerking wordt nog niet ondersteund. | Ja | Ja | Ja | Nee | Nee |
| 622 | Orders zoeken | Met deze bewerking kunnen gebruikers POS-knoppen vooraf configureren om te zoeken op artikel, klant of categorie. | Ja | Ja | Ja | Ja | Nee |
| 1213 | Verzendadres zoeken | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 709 | Hardwarestation selecteren | Een hardwarestation in een lijst met beschikbare hardwarestations selecteren. | Ja | Ja | Ja | Ja | Nee |
| 637 | Standaard verkoopvertegenwoordiger instellen voor transactie | Een van de in aanmerking komende provisieverkoopgroepen (vertegenwoordigers) selecteren als de standaardvertegenwoordiger voor regels die later worden toegevoegd. | Ja | Ja | Nee | Ja | Nee |
| 105 | Hoeveelheid instellen | Wijzig de hoeveelheid van een regelartikel in de transactie. | Ja | Ja | Nee | Ja | Nee |
| 638 | Verkoopvertegenwoordiger instellen op regel | Een van de in aanmerking komende provisieverkoopgroepen (vertegenwoordigers) selecteren voor de momenteel geselecteerde regel. | Ja | Ja | Nee | Ja | Nee |
| 630 | Alle producten verzenden | De afhandelingsmodus instellen op **Verzenden** voor alle regelartikelen. | Ja | Ja | Nee | Ja\* | Nee |
| 629 | Geselecteerde producten verzenden | De afhandelingsmodus voor de geselecteerde regels instellen op **Verzenden**. | Ja | Ja | Nee | Ja\* | Nee |
| 115 | Journaal weergeven | Het journaal van de winkel weergeven. U kunt transacties weergeven, ontvangstbewijzen en giftontvangsten opnieuw afdrukken en intrekken voor retour. | Ja | Ja | Ja | Ja\*\* | Nee |
| 802 | Voorraadtelling | Voorraadtellingsjournalen maken of wijzigen voor fysieke voorraad of cyclustellingen. | Ja | Ja | Ja | Nee | Nee |
| 401 | Submenu | Met deze bewerking gaat de gebruiker naar een ander gekoppeld knoppenraster. | Ja | Ja | Ja | Ja | Nee |
| 1054 | Ploeg uitstellen | De huidige ploeg uitstellen zodat een nieuwe of andere ploeg kan worden geactiveerd voor het huidige register. | Ja | Ja | Ja | Nee | Nee |
| 503 | Transactie uitstellen | De huidige verkooptransactie uitstellen zodat deze later in de winkel kan worden ingetrokken. | Ja | Ja | Nee | Ja‡ | Nee |
| 1004 | Taakregistratie | Taakregistratie openen om procedurestappen in het POS vast te leggen. | Nee | Nee | Nee | Ja | Nee |
| 1052 | Kascontrole | Het opgegeven geldbedrag in de lade voor elke getelde betalingsmethode opgeven. | Ja | Ja | Ja | Ja | Nee |
| 1210 | Wisselgeld verwijderen | Geld verwijderen uit de huidige lade of ploeg. | Ja | Ja | Ja | Ja | Nee |
| 920 | Tijdklok | In- en uitklokken voor ploegendiensten en pauzes. | Ja | Ja | Ja | Nee | Nee |
| 302 | Totaal kortingsbedrag | Een kortingsbedrag invoeren voor de transactie. Deze bewerking geldt alleen voor kortingsartikelen en alleen binnen de opgegeven kortingslimieten. | Ja | Ja | Nee | Ja | Nee |
| 303 | Totaal kortingspercentage | Een kortingspercentage invoeren voor de transactie. Deze bewerking geldt alleen voor kortingsartikelen en alleen binnen de opgegeven kortingslimieten. | Ja | Ja | Nee | Ja | Nee |
| 501 | Opmerking bij transactie | Een opmerking toevoegen aan de huidige transactie. | Ja | Ja | Nee | Ja | Nee |
| 922 | Productgegevens weergeven | De pagina met productgegevens openen voor het geselecteerde regelartikel. | Ja | Ja | Nee | Ja | Nee |
| 1003 | Rapporten weergeven | De rapporten weergeven die zijn geconfigureerd voor de huidige gebruiker. | Ja | Ja | Ja | Nee | Nee |
| 921 | Registraties tijdklok weergeven | De tijdklokregistraties weergeven voor alle werknemers in de winkel. | Ja | Ja | Ja | Nee | Nee |
| 211 | Ongeldig gemaakte betaling | De geselecteerde betalingsregel uit de transactie annuleren. | Ja | Ja | Nee | Ja | Nee |
| 102 | Ongeldig gemaakt product | Het geselecteerde regelartikel uit de transactie annuleren. | Ja | Ja | Nee | Ja | Nee |
| 500 | Ongeldig gemaakte transactie | De huidige transactie annuleren. | Ja | Ja | Nee | Ja | Nee |
| 916 | Windows Workflow Foundation | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Nee |
| 924 | X-rapport voor bankpassen | Deze bewerking wordt niet ondersteund. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Niet van toepassing | Ja |
| 311 | Systeemkortingen uit transacties verwijderen | Verwijder alle toegewezen systeemkortingen, inclusief couponkortingen, uit de transactie. Hiermee worden handmatige kortingen niet verwijderd. | Ja | Ja | Ja | Ja | Nee |
| 312 | Systeemkortingen opnieuw toepassen | Pas systeemkortingen opnieuw toe op de transactie als deze zijn verwijderd met de bewerking **Systeemkortingen uit transacties verwijderen**. | Ja | Ja | Ja | Ja | Nee |

\* De bewerking is alleen beschikbaar in de offlinemodus als een klantorder of verkoopofferte wordt gemaakt en alleen als het offline maken van klantorders en verkoopoffertes is geconfigureerd in het POS-functionaliteitsprofiel. De bewerking kan niet worden uitgevoerd wanneer orders worden gemaakt met Real-time Service of wanneer orders worden ingetrokken of bewerkt.

† De bewerking kan alleen worden uitgevoerd in de offlinemodus als het POS zo is geconfigureerd dat klanten offline kunnen worden gemaakt in het POS-functionaliteitsprofiel.

‡ Als het POS offline is, kunnen uitgestelde transacties alleen vanuit de offlinedatabase van de huidige kassa worden ingetrokken. Gebruikers kunnen transacties in andere journalen niet uitstellen of intrekken.

§ Als het POS offline is, kunnen alleen transacties in de huidige offlinedatabase worden ingetrokken voor retour.

\*\* Als het POS offline is, kunnen alleen transacties in de huidige kanaaldatabase worden weergegeven in het journaal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
