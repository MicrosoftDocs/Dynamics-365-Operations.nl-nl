---
title: Partij- en globaal adresboek
description: In dit artikel wordt de functionaliteit Adresboek van partij en globaal adresboek van Twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 08/02/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 7f06b6e69b76bf12092fdceca5b45a6750b52233
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228985"
---
# <a name="party-and-global-address-book"></a>Partij en globaal adresboek

[!include [banner](../../includes/banner.md)]



*Partij* en *Globaal adresboek* zijn concepten in toepassingen voor financiële en bedrijfsactiviteiten. Een partij kan een organisatie of persoon zijn. Het is handig om de eigenschappen van een partij, zoals de naam, taal, contactpersonen en adressen, globaal op te slaan en te beheren. Als de waarde van een eigenschap op de ene plaats wordt gewijzigd, wordt deze wijziging ook doorgevoerd op alle andere plaatsen waar de partij wordt gebruikt.

## <a name="party"></a>Partij

Een partij is een persoon of een organisatie die betrokken is bij een bedrijf. Door het concept partij te gebruiken, kan een persoon of organisatie meer dan één rol (bijvoorbeeld medewerker, klant, leverancier of contactpersoon) vervullen in een bedrijf. De rol is gebaseerd op de context en het doel. Hieronder vindt u enkele voorbeelden van rollen in twee fictieve bedrijven, Contoso en Fabrikam:

+ **Medewerker**: een werknemer. Een voorbeeld is een werknemer van Contoso.
+ **Leverancier**: Een leveranciersorganisatie die of eenmansbedrijf dat goederen of diensten levert aan een bedrijf. Als Fabrikam bijvoorbeeld goederen verkoopt aan Contoso, is Fabrikam een leverancier van Contoso.
+ **Contactpersoon**: Een persoon om contact mee op te nemen. Als Contoso bijvoorbeeld producten koopt bij Fabrikam, nemen werknemers van Contoso contact op met de contactpersoon bij Fabrikam.
+ **Klant**: Een klant is een persoon die of bedrijf dat goederen koopt van een bedrijf. Als Contoso bijvoorbeeld producten koopt van Fabrikam, is Contoso een klant van Fabrikam.

Het partijmodel wordt vaak gebruikt om gemiddelde tot complexe relaties tussen organisaties en mensen weer te geven, met name als een partij meer dan één rol heeft. Hieronder vindt u een aantal gangbare voorbeelden:

+ Een partij kan zowel een klant als leverancier zijn. In Noord-Amerika verkoopt Fabrikam bijvoorbeeld elektrische kabels aan Contoso en koopt Fabrikam geassembleerde luidsprekers van Contoso. In Europa verkoopt Fabrikam onderdelen aan Contoso, maar koopt Fabrikam niets van Contoso.
+ Een partij kan zowel een werknemer als klant zijn. Een werknemer van Contoso kan bijvoorbeeld elektronica kopen bij Contoso voor persoonlijk gebruik.
+ Er kan een veel-op-veel-relatie (N:N) tussen een persoon en een organisatie bestaan. Fabrikam levert bijvoorbeeld servicespecialisten en heeft een plaatsingscoördinator in dienst. De plaatsingscoördinator wijst de servicespecialisten toe aan de werkaanvragen van verschillende klanten van Fabrikam. Contoso is een van de klanten van Fabrikam. Wanneer Contoso een servicespecialist nodig heeft, neemt het bedrijf contact op met de plaatsingscoördinator die de aanvraag vervolgens inwilligt. Omdat de plaatsingscoördinator aanvragen voor alle klanten verwerkt, spreken we hier van een N:N-relatie.

De volgende afbeelding toont het gegevensmodel voor Partij.

![Gegevensmodel voor partij.](media/party-gab-image1.png)

> [!TIP]
> Wanneer u een nieuwe accountrecord wilt maken, gebruikt u het veld **Partij** om op naam naar de record te zoeken. Op deze manier hoeft u de record alleen maar te selecteren nadat u deze hebt gevonden. Alle gegevens van de partij worden vervolgens automatisch ingevuld. U hoeft niet alle verplichte velden handmatig in te stellen. Dit gedrag is standaardgedrag op de pagina's **Account**, **Contactpersoon** en **Leverancier**.

Niet alle partijrollen van apps voor financiële en bedrijfsactiviteiten worden ondersteund door Twee keer wegschrijven. Zie [Overzicht van globaal adresboek](../../../fin-ops/organization-administration/overview-global-address-book.md) voor een volledige lijst met partijrollen.

### <a name="global-address-book"></a>Algemeen adresboek

Het globale adresboek is een adreslijst met post- en elektronische adressen van de organisaties en personen die deel uitmaken van een bedrijf.

In het globale adresboek worden zoveel postadressen en elektronische adressen opgeslagen en verwerkt als nodig is. Stel bijvoorbeeld dat Fabrikam tankstations heeft op 50 locaties. Elke locatie heeft een ander postadres, e-mailadres en telefoonnummer. Alle zakelijke aankopen worden gefactureerd aan het hoofdstation van Fabrikam, maar rechtstreeks verzonden naar het specifieke tankstation dat de aankoop heeft aangevraagd. In het globale adresboek wordt het hoofdstation opgeslagen als het factuuradres voor Fabrikam en elk tankstation opgeslagen als verzendadres. De adressen kunnen eenmalig worden opgeslagen en worden opgehaald voor offertes en orders wanneer dat nodig is.

Afhankelijk van de zakelijke context kan een persoon of organisatie meer dan één rol spelen, en voor alle rollen kunnen hetzelfde postadres en elektronisch adres worden gebruikt. In dit geval moet een adreswijziging in de ene rol ook voor de andere rol worden weergegeven. In het globale adresboek worden adressen globaal opgeslagen en verwerkt.

In de volgende afbeelding wordt het gegevensmodel voor het globale adresboek getoond.

![Gegevensmodel voor het globale adresboek.](media/party-gab-image2.png)

## <a name="contact"></a>Contact

In Customer Engagement-apps is een contactpersoon een persoon. De tabel **Contactpersoon** werd echter te veel gebruikt en bevatte behalve personen ook portalgebruikers, B2C-klanten (business-to-consumer) of leveranciers. De representatie is impliciet en je kunt het verschil niet zien zonder gerelateerde transacties nader te onderzoeken. De tabel **Contactpersoon** is nu ingesteld om een 1:1-relatie te hebben met de tabel **Account**. Als onderdeel van het model voor partijen en het globale adresboek, worden met Twee keer wegschrijven expliciete eigenschappen voor classificatie geïntroduceerd. Twee keer wegschrijven staat N:N-relaties toe tussen een contactpersoon die een echte persoon is en een organisatie (entiteit **Account** of **Leverancier**).

Er zijn twee typen rijen **Contactpersoon**:

+ **Gestreepte contactpersoon**: Een **Contactpersoon**-rij waarin het veld **Bedrijf** een verplichte waarde heeft.
+ **Niet-gestreepte contactpersoon**: Een **Contactpersoon**-rij waarin het veld **Bedrijf** leeg is.

In de tabel **Contactpersoon** kunnen de volgende typen rijen worden opgeslagen:

| Rijtype | Beschrijving |
|----------|-------------|
| Een persoon die een klant is (bijvoorbeeld een verkoopbare contactpersoon of een B2C-klant). | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is en het veld **Is klant** is ingesteld op **Ja**. |
| Een persoon die een leverancier is (bijvoorbeeld een eenmansbedrijf zoals een leverancier). | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is en het veld **Is leverancier** is ingesteld op **Ja**. |
| Een persoon die zowel een klant als leverancier is. | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is, het veld **Is klant** is ingesteld op **Ja** en het veld **Is leverancier** is ingesteld op **Ja**. Een persoon kan zowel een fabrikant voor een product als een klant voor een ander product zijn. Beide apps voor financiële en bedrijfsactiviteiten en Twee keer wegschijven ondersteunen deze relatie. |
| Een persoon die een contactpersoon is voor een organisatie, maar geen klant of leverancier is. | Een niet-gestreepte contactpersoonrecord waarbij het veld **Bedrijf** leeg is, het veld **Is klant** is ingesteld op **Nee** en het veld **Is leverancier** is ingesteld op **Nee**. |

## <a name="contact-for-party-table"></a>Contactpersoon voor de tabel Partij

In de tabel **Contactpersoon voor partij** worden N:N-relaties tussen rijen in **Account** en **Contactpersoon** opgeslagen en verwerkt. De gestreepte rijen **Contactpersoon** kunnen uit de niet-gestreepte rijen worden gefilterd om alleen de niet-gestreepte rijen **Contactpersoon** te koppelen aan een rij **Account** of **Leverancier**.

Natasha Jones en Miguel Reyes zijn bijvoorbeeld dierenartsen die zorg bieden aan boerderijen in hun regio's. Natasha is actief in het gebied rond Seattle en Miguel is actief rondom Kent. In de Customer Engagement-app worden de boerderijen weergegeven als klanten en de dierenartsen als contactpersonen. Eén record **Contactpersoon** van Natasha is gekoppeld aan alle boerderijen waarmee Natasha werkt. Op dezelfde manier is één **Contactpersoon**-record van Miguel gekoppeld aan alle boerderijen waarmee hij werkt.

Deze relaties worden opgeslagen in de tabel **Contactpersoon voor partij**. U kunt de informatie vinden op de pagina's **Account**, **Contactpersoon** en **Leverancier**:

+ Op de pagina **Account** kunt u het tabblad **Gekoppelde contactpersonen** gebruiken om een of meer contactpersonen te koppelen aan de rij **Account**. Zo wijst u contactpersonen toe voor een organisatie. U kunt vervolgens één contactpersoon selecteren als de primaire contactpersoon voor de account. Als u de pagina **Snel maken** gebruikt, kunt u slechts één contactpersoon selecteren. Het gedrag is hetzelfde wanneer u de pagina **Leverancier** gebruikt en het recordtype **Organisatie** is.
+ Wanneer de rij op de pagina **Contactpersoon** een klant, een leverancier of beide is (een gestreepte contactpersoon), kunt u het tabblad **Gekoppelde contactpersonen** gebruiken om een of meer contactpersonen te koppelen. Zo wijst u contactpersonen toe voor een B2C-klant of -leverancier. U kunt vervolgens één contactpersoon selecteren als de primaire contactpersoon. Als u de pagina **Snel maken** gebruikt, kunt u slechts één contactpersoon selecteren.
+ Wanneer de rij op de pagina **Contactpersoon** een contactpersoon is (een niet-gestreepte contactpersoon), kunt u het tabblad **Gekoppelde organisaties** gebruiken om een of meer klanten of leveranciers te koppelen. Zo wijst u een klanten of leveranciers toe aan de onderliggende contactpersoon. De klant of leverancier kan een organisatie, een persoon of beide zijn. U kunt altijd slechts een waarde selecteren in één van de vier velden:

    + Als u een waarde selecteert in het veld **Partij-id**, wordt de onderliggende contactpersoon toegewezen aan alle rollen van de geselecteerde partij.
    + Als u een waarde selecteert in het veld **Gekoppelde contactpersoon**, selecteert u de gestreepte contactpersoon van het type **Persoon**.
    + Als u een waarde selecteert in het veld **Gekoppelde account** of **Gekoppelde leverancier**, selecteert u een organisatie.

    ![Tabblad Gekoppelde organisaties op de pagina Contactpersoon.](media/party-gab-image3.png)

    Ongeacht uw selectie wordt de koppeling tot stand gebracht op partijniveau en toegepast op alle rollen van de partij en opgeslagen in de entiteit **Contactpersoon voor partij**.

> [!NOTE]
> De weergavenaam voor de tabel **Contactpersoon voor partij** in de Customer Engagement-apps is **Contactpersoon voor klant/leverancier**.

Wanneer u een **Contactpersoon**-rij opent waarin zowel het veld **Is Klant** als het veld **Is Leverancier** is ingesteld op **Nee**, wordt het tabblad **Gekoppelde organisaties** getoond. Op dit tabblad kunt u één of meer klant- of leveranciersorganisaties koppelen aan de contactpersoon.

Wanneer u een **Contactpersoon**-rij opent waarin of het veld **Is Klant** of het veld **Is Leverancier** is ingesteld op **Ja**, wordt het tabblad **Gekoppelde contactpersonen** getoond. Gebruik dit tabblad om een of meer contactpersonen te koppelen.

## <a name="postal-addresses"></a>Postadressen

Er is een nieuw tabblad **Adressen** beschikbaar op de pagina's **Account**, **Contactpersoon** en **Leverancier**. Op dit tabblad worden meerdere postadressen ondersteund door middel van een raster, zoals in de onderstaande afbeelding wordt getoond.

![Raster voor postadressen.](media/party-gab-image4.png)

Het raster bevat de volgende kolommen:

+ **Postadresrollen**: het doel van het postadres.
+ **Is primair**: een waarde die aangeeft of het adres het primaire adres is.
+ **Nummer adres**: geeft de plaats in de volgorde van adressen aan.

Met de knop **Nieuw adres** boven het raster kunt u zoveel postadressen maken als u wilt.

Wanneer een gebruiker in toepassingen voor **klantcontacten** de adressen invoer op het tabblad **Overzicht** van de pagina Accounts, komen de velden **Adres 1** en **Adres 2** overeen met de adressen voor **Levering** en **Factuur**. Wanneer een gebruiker echter een postadres aanmaakt in de toepassingen voor Financiën en bewerkingen, worden de eerste twee adressen van de klantrecord weergegeven in de velden **Adres1** en **Adres2** en heeft de gebruiker de mogelijkheid om het doel van het adres te wijzigen in **Levering** en **Factuur**.

![Tabblad Overzicht voor postadressen.](media/party-gab-image5.png)

Vergelijkbaar komen de velden **Adres 1**, **Adres 2** en **Adres 3** op het tabblad **Overzicht** van de pagina **Contactpersoon** overeen met respectievelijk de adressen voor **Bedrijf**, **Levering** en **Factuur**.

## <a name="electronic-addresses"></a>Elektronische adressen

Er is een nieuw tabblad **Elektronische adressen** beschikbaar op de pagina's **Account**, **Contactpersoon** en **Leverancier**. Dit tabblad ondersteunt meerdere elektronische adressen door middel van een raster, zoals in de onderstaande afbeelding wordt getoond.

![Raster voor elektronisch adressen.](media/party-gab-image6.png)

Het raster bevat de volgende kolommen:

+ **Type**: het type elektronisch adres.
+ **Is primair**: een waarde die aangeeft of het adres het primaire adres is.
+ **Doel**: het doel van het elektronische adres.

Met de knop **Nieuw elektronisch adres** boven het raster kunt u zoveel postadressen maken als u wilt.

Tijdens het kwalificatieproces voor de lead kunt u zowel een bedrijfstelefoonnummer als een mobiel telefoonnummer opgeven. Het zakelijke telefoonnummer wordt beschouwd als de primair telefoonnummer als **IsMobile=Nee** en het mobiele telefoonnummer wordt beschouwd als secundair telefoonnummer als **IsMobile=Ja**.

> [!TIP]
> Gebruik de tabbladen **Adressen** en **Elektronische adressen** in de formulieren **Account** en **Contactpersoon** om post- en elektronische adressen te beheren. Hiermee wordt ervoor gezorgd dat adresgegevens met apps voor financiële en bedrijfsactiviteiten worden gesynchroniseerd.

## <a name="setup"></a>Instelling

1. Omgeving van de Customer Engagement-app openen.

2. Installeer alle vereiste oplossingen, zoals wordt beschreven in [Afzonderlijk Application Orchestration-pakket voor twee keer wegschrijven](separated-solutions.md).

3. Installeer [de oplossingen voor twee keer wegschrijven voor Partij en Globaal adresboek](https://aka.ms/dual-write-gab).

4. Open de app voor financiële en bedrijfsactiviteiten. Navigeer naar de module Gegevensbeheer en selecteer het tabblad Twee keer wegschrijven. De pagina voor beheer van twee keer wegschrijven wordt geopend.

5. Pas beide oplossingen toe die in stap 2 en 3 zijn geïnstalleerd met behulp van de functie [Oplossing toepassen](link-your-environment.md).

6. Stop de volgende toewijzingen, omdat ze niet meer nodig zijn. Voer in plaats daarvan de toewijzing `Contacts V2 (msdyn_contactforparties)` uit.

    + CDS-contactpersonen V2 en Contactpersonen (verwijst naar klantcontactpersonen)
    + CDS-contactpersonen V2 en Contactpersonen (verwijst naar leverancierscontactpersonen)

7. De volgende entiteitstoewijzingen worden bijgewerkt voor partijfunctionaliteit, dus de nieuwste versie moet op deze toewijzingen worden toegepast.

    Toewijzen | Update naar deze versie | Wijzigingen
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Customers V3 (accounts)` | 1.0.0.5 |`PartyNumber` en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
    `Customer V3 (contacts)` | 1.0.0.5 | `PartyNumber` en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | `PartyNumber` en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | De contactpersoon is vervangen door de verwijzing `ContactforParty`.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | De contactpersoon is vervangen door de verwijzing `ContactforParty`.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | De contactpersoon is vervangen door de verwijzing `ContactforParty`.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.

8. Voordat u de bovenstaande toewijzingen gaat uitvoeren, moet u de integratiesleutels handmatig bijwerken zoals beschreven in de volgende stappen. Selecteer **Save**.

    | Toewijzing | Sleutels |
    |-----|------|
    | Account |  accountnumber [Accountnummer]<br>msdyn_company.cdm_companycode [Bedrijf (Bedrijfscode)] |
    | Contact | msdyn_contactpersonid [Accountnummer/Contactpersoon-id]<br>msdyn_company.cdm_companycode [Bedrijf (Bedrijfscode)] |
    | Contactpersoon voor klant/leverancier | msdyn_contactforpartynumber [Nummer contactpersoon voor partij]<br>msdyn_associatedcompanyid.cdm_companycode [Gekoppeld bedrijf (Bedrijfscode)] |
    | Leverancier | msdyn_vendoraccountnumber [Accountnummer leverancier]<br>msdyn_company.cdm_companycode [Bedrijf (Bedrijfscode)]|

9. In Dataverse zijn de tekenlimieten van de regels voor duplicatendetectie verhoogd van 450 tot 700 tekens. Met deze limiet kunt u een of meer sleutels toevoegen aan de regels voor duplicatendetectie. Breid de regel voor duplicatendetectie uit voor de tabel **Accounts** door de volgende velden in te stellen.

    | Veld | Waarde |
    |-------|-------|
    | Naam | Accounts met dezelfde accountnaam. |
    | Beschrijving | Detecteert accountrecords met dezelfde waarde in het kenmerk Accountnaam. |
    | Type basisrecord | Account |
    | Overeenkomend recordtype | Account |
    | Accountnaam (veld) | Exacte overeenkomst |
    | Bedrijf (veld) | Exacte overeenkomst |
    | Relatietype (veld) | Exacte overeenkomst |
    | Partij-id (veld) | Exacte overeenkomst |
    | Selecteren (veld) | (leeg) |

    ![Duplicatenregel voor Accounts.](media/duplicate-rule-1.PNG)

10. Breid de regel voor duplicatendetectie uit voor de tabel **Contactpersonen** door de volgende velden in te stellen.

    | Veld | Waarde |
    |-------|-------|
    | Naam | Contactpersonen met dezelfde voornaam en achternaam. |
    | Beschrijving | Detecteert contactpersonenrecords met dezelfde waarden in de velden Voornaam en Achternaam. |
    | Type basisrecord | Contact |
    | Overeenkomend recordtype | Contact |
    | Voornaam (veld) | Exacte overeenkomst |
    | Achternaam (veld) | Exacte overeenkomst |
    | Bedrijf (veld) | Exacte overeenkomst |
    | Partij-id (veld) | Exacte overeenkomst |
    | Selecteren (veld) | (leeg) |

    ![Duplicatenregel voor Contactpersonen.](media/duplicate-rule-2.PNG)

11. Als u een bestaande gebruiker van Twee keer wegschrijven bent, volgt u de instructies in [Bijwerken naar het model voor partij en globaal adresboek](upgrade-party-gab.md) om uw gegevens te upgraden. **Ga niet door naar stap 12 zonder deze stap te voltooien.** Als u een nieuwe gebruiker van twee keer wegschrijven bent, gaat u verder met stap 12.

12. Als u een bestaande gebruiker van twee keer wegschrijven bent, voltooit u stap 11. Vervolgens kunt u de toewijzingen in de volgende volgorde uitvoeren. Als u een nieuwe klant van twee keer wegschrijven bent, kunt u rechtstreeks doorgaan. Als u een fout krijgt met het bericht "Projectvalidatie mislukt. Doelveld ontbreekt...", open dan de toewijzing, selecteer **Tabellen vernieuwen** en voer de toewijzing uit.

    App voor financiële en bedrijfsactiviteiten | Customer Engagement-app  
    ----------------------------|------------------------
    [CDS-partijen](mapping-reference.md#220) | msdyn_parties
    [CDS-locaties van postadres](mapping-reference.md#234) | msdyn_postaladdresscollections
    [Historie van CDS-postadres V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS-locaties van postadres van partij](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Contactpersonen partij V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Klanten V3](mapping-reference.md#101) | rekeningen
    [Klanten V3](mapping-reference.md#116) | contacten
    [Leveranciers V2](mapping-reference.md#202) | msdyn_vendors
    [Titels contactpersoon](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Afsluitingen](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Aanhef](mapping-reference.md#228) | msdyn_salutations
    [Besluitvormingsrollen](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Taakfuncties dienstverband](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Loyaliteitsniveaus](mapping-reference.md#226) | msdyn_loyaltylevels
    [Persoonlijke karaktertypen](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Contactpersonen V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-verkoopoffertekoptekst](mapping-reference.md#215) | offertes
    [CDS-verkooporderkopteksten](mapping-reference.md#217) | salesorders
    [Kopteksten van verkoopfacturen V2](mapping-reference.md#118) | facturen
    [CDS-adresrollen](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> De toewijzing `CDS Contacts V2 (contacts)` is de toewijzing die u hebt gestopt in stap 1. Als u andere toewijzingen probeert uit te voeren, worden deze twee toewijzingen mogelijk weergegeven in de lijst met afhankelijke toewijzingen. Voer deze toewijzingen niet uit.
>
> Als de oplossing voor partij en globaal adresboek is geïnstalleerd, moet u de invoegtoepassing `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` uitschakelen. Als u de oplossing voor partij en globaal adresboek verwijdert, moet u de invoegtoepassing opnieuw inschakelen.
>
> Het veld `msdyn_*partynumber` (een tekstveld van één regel) in de tabellen **Account**, **Contactpersoon** en **Leverancier** moet u in de toekomst niet meer gebruiken. Voor de duidelijkheid heeft de labelnaam het voorvoegsel **(Afgeschaft)** gekregen. Gebruik in plaats daarvan het veld **msdyn_partyid**. Dit veld is een opzoekveld voor de tabel **msdyn_party**.
>
> Tabelnaam | Oud veld | Nieuw veld
> --------|-------|--------
> Account | `msdyn_partynumber` | `msdyn_partyid`
> Contact | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Sjablonen

Een verzameling tabeltoewijzingen werkt samen voor de interactie tussen partij en globaal adresboek, zoals in de volgende tabel wordt weergegeven.

| App voor financiële en bedrijfsactiviteiten | Customer Engagement-app | Description |
|----------------------------|-------------------------|-------------|
| [Titels contactpersoon](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Klanten V3](mapping-reference.md#101) | rekeningen |
| [Klanten V3](mapping-reference.md#116) | contacten |
| [CDS-partijen](mapping-reference.md#220) | msdyn\_parties |
| [CDS-locaties van postadres van partij](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [Historie van CDS-postadres V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS-locaties van postadres](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-verkoopoffertekoptekst](mapping-reference.md#215) | offertes |
| [CDS-verkooporderkopteksten](mapping-reference.md#217) | salesorders |
| [Afsluitingen](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Contactpersonen V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Besluitvormingsrollen](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Taakfuncties dienstverband](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Loyaliteitsniveaus](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Contactpersonen partij V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Persoonlijke karaktertypen](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Kopteksten van verkoopfacturen V2](mapping-reference.md#118) | facturen |
| [Aanhef](mapping-reference.md#228) | msdyn\_salutations |
| [Leveranciers V2](mapping-reference.md#202) | msdyn\_vendors |
| [CDS-adresrollen](mapping-reference.md#301) |msdyn\_addressroles|

Zie [Toewijzingsverwijzing voor twee keer wegschrijven](mapping-reference.md) voor meer informatie.

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Adresrollen als een vervolgkeuzelijst met meerdere selecties
Een postadres of elektronisch adres kan meer dan één doel dienen. Een postadres kan bijvoorbeeld fungeren als factuuradres en afleveradres. In deze gevallen kan een gebruiker zowel **Factuur** als **Levering** selecteren in de vervolgkeuzelijst, zoals in de onderstaande afbeelding wordt weergegeven. 

![De vervolgkeuzelijst Doel/rol.](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Bekende problemen en beperkingen

+ Wanneer u in apps voor financiële en bedrijfsactiviteiten een klant maakt met een adres en deze opslaat, wordt het adres mogelijk niet gesynchroniseerd met de tabel **Adres**. Dit komt door een probleem in de volgordeverwerking op het platform voor Twee keer wegschrijven. Een tijdelijke oplossing is om eerst de klant aan te maken en deze op te slaan. Voeg daarna pas het adres toe.
+ Wanneer in apps voor financiële en bedrijfsactiviteiten een klantrecord een primair adres heeft en u een nieuwe contactpersoon voor die klant maakt, neemt de contactpersoonrecord een primair adres over van de bijbehorende klantrecord. Dit gebeurt ook bij contactpersoon van een leverancier. Dataverse ondersteunt dit gedrag momenteel niet. Als Twee keer wegschrijven is ingeschakeld, wordt een contactpersoon van een klant die is overgenomen met een primair adres uit de app voor financiële en bedrijfsactiviteiten samen met het adres gesynchroniseerd naar Dataverse.
+ In apps voor financiële en bedrijfsactiviteiten kunt u een contactpersoonrecord maken vanuit het formulier **Contactpersoon toevoegen**. Wanneer u een nieuwe contactpersoon probeert te maken vanuit het formulier **Contactpersonen weergeven**, mislukt de actie. Dit is een bekend probleem.

    ![Bekend probleem met Contactpersoon toevoegen.](media/party-gab-contact-issue.png)

+ **Initiële synchronisatie** ondersteunt niet de tijdvelden **Beschikbaar vanaf** en **Beschikbaar tot** op **ContactForParty**, omdat DIXF de waarde converteert naar een tekenreeks (string) in plaats van een geheel getal (integer). De conversie activeert de fout `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32`.
+ U kunt geen vooruitgedateerd postadres invoeren met een app voor financiële en bedrijfsactiviteiten met twee keer wegschrijven, omdat Dataverse niet de ingangsdatum ondersteunt. Als u een vooruitgedateerd postadres invoert via een app voor financiële en bedrijfsactiviteiten, wordt dit volledig met Dataverse gesynchroniseerd en wordt het adres direct in de gebruikersinterface gebruikt. Updates van deze record resulteren in een fout, aangezien dit adres in de toekomst wordt gebruikt en nog niet wordt gebruikt in de app voor financiële en bedrijfsactiviteiten.
