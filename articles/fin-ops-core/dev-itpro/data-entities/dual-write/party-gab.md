---
title: Partij en globaal adresboek
description: In dit onderwerp wordt de functionaliteit Partij en globaal adresboek van Twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750783"
---
# <a name="party-and-global-address-book"></a>Partij en globaal adresboek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Partij en globaal adresboek zijn concepten in Finance and Operations-toepassingen. Een partij kan een organisatie of persoon zijn. Het is handig om de eigenschappen van een **partij**, zoals de naam, taal, contactpersonen en adressen, globaal op te slaan en te beheren. Wanneer de waarde van een eigenschap op de ene plaats wordt gewijzigd, wordt deze ook aangepast op alle andere plaatsen waar de **partij** wordt gebruikt.

## <a name="party"></a>Partij

Een *partij* is een persoon of een organisatie die betrokken is bij het bedrijf. Door het concept Partij te gebruiken, kan een persoon of organisatie meer dan één rol (werknemer, klant, leverancier of contactpersoon) in een bedrijf vervullen. De rol is gebaseerd op de context en het doel. Hieronder vindt u enkele voorbeelden van twee fictieve bedrijven, Contoso en Fabrikam.

+ **Werknemer**: een werknemer. Bijvoorbeeld een werknemer van Contoso.
+ **Leverancier**: een leveranciersorganisatie die of eenmansbedrijf dat goederen of diensten levert aan een bedrijf. Als Fabrikam voorraad aan Contoso verkoopt, heeft Fabrikam bijvoorbeeld de rol van leverancier.
+ **Contactpersoon**: een persoon om contact mee op te nemen. Als Contoso voorraden koopt bij Fabrikam, zou een werknemer van Contoso bijvoorbeeld contact opnemen met de contactpersoon bij Fabrikam.
+ **Klant**: een klant is een persoon die of bedrijf dat items koopt van een bedrijf. Als Contoso producten koopt van Fabrikam, is Contoso bijvoorbeeld een klant van Fabrikam.

Het model Partij wordt vaak gebruikt om gemiddelde tot complexe relaties tussen organisaties en mensen weer te geven, met name als een partij meer dan één rol heeft. Hieronder vindt u een aantal gangbare voorbeelden:

+ Een partij kan zowel een klant als leverancier zijn. In Noord-Amerika verkoopt Fabrikam bijvoorbeeld elektrische kabels aan Contoso en koopt Fabrikam samengestelde luidsprekers van Contoso. In Europa verkoopt Fabrikam onderdelen aan Contoso, maar koopt Fabrikam niets van Contoso.
+ Een partij kan zowel een werknemer als klant zijn. Een werknemer van Contoso kan bijvoorbeeld elektronica kopen bij Contoso voor persoonlijk gebruik.
+ Er kan een veel-op-veel-relatie tussen een persoon en een organisatie zijn. Fabrikam levert bijvoorbeeld servicespecialisten en heeft een plaatsingscoördinator in dienst. De coördinator wijst de servicespecialisten toe aan de werkaanvragen van verschillende klanten van Fabrikam. Contoso is een van de klantaccounts. Wanneer Contoso een specialist nodig heeft, neemt Contoso contact op met de coördinator, die de aanvraag vervolgens inwilligt. De coördinator verwerkt aanvragen voor alle klanten en maakt daarbij een veel-op-veel-relatie.

De volgende afbeelding toont het gegevensmodel voor Partij:

![Gegevensmodel voor Partij](media/party-gab-image1.png)

> [!Tip]
> Wanneer u een nieuwe accountrecord wilt maken, gebruikt u het veld Partij om op naam naar de record te zoeken. Voor het geval u de record vindt, hoeft u deze alleen te selecteren. Alle gegevens van de partij worden automatisch ingevuld. U hoeft niet alle verplichte velden handmatig in te voeren. Dit gedrag is standaardgedrag in de formulieren Account, Contactpersoon en Leverancier.

Niet alle partijrollen van Finance and Operations-apps worden ondersteund door Twee keer wegschrijven. Zie [Overzicht van globaal adresboek](../../../fin-ops/organization-administration/overview-global-address-book.md) voor een volledige lijst met partijrollen.

### <a name="global-address-book"></a>Algemeen adresboek

Het globale adresboek is een adreslijst met post- en elektronische adressen van de organisaties en personen die deel uitmaken van een bedrijf.

In het globale adresboek worden zoveel postadressen en elektronische adressen opgeslagen en verwerkt als nodig is. Stel bijvoorbeeld dat Fabrikam tankstations op 50 locaties heeft. Elke locatie heeft een ander postadres, e-mailadres en telefoonnummer. Alle zakelijke aankopen worden gefactureerd aan het hoofdstation van Fabrikam, maar inkopen worden rechtstreeks verzonden naar het specifieke tankstation dat de aankoop heeft aangevraagd. In het globale adresboek wordt het hoofdstation opgeslagen als het factuuradres en elk gasstation als verzendadres opgeslagen voor Fabrikam. De adressen kunnen eenmaal worden opgeslagen en waar nodig worden opgehaald voor offertes en orders.

Een persoon of organisatie kan op basis van de bedrijfscontext meerdere rollen vervullen. In dat geval kunnen hun postadressen en elektronische adressen overeenkomen. In dit geval moet een wijziging van het adres in de ene rol ook voor de andere rol worden weergegeven en omgekeerd. In het globale adresboek worden adressen globaal opgeslagen en verwerkt.

![Gegevensmodel voor globaal adresboek](media/party-gab-image2.png)

## <a name="contacts"></a>Contactpersonen

In apps voor klantbetrokkenheid is een contactpersoon een *persoon*. De tabel **Contactpersoon** werd echter te veel gebruikt en bevatte behalve personen ook portalgebruikers, B2C-klanten of leveranciers. De representatie is impliciet en u kunt het verschil niet zien zonder gerelateerde transacties nader te onderzoeken. De tabel **Contactpersoon** is nu ingesteld om een 1:1-relatie met de tabel **Rekening** te hebben. Als onderdeel van het model voor partijen en het globale adresboek, worden met Twee keer wegschrijven expliciete eigenschappen voor classificatie geïntroduceerd. Twee keer wegschrijven staat N:N-relaties tussen een **contactpersoon** en een organisatie (rekeningentiteit of leveranciersentiteit).

Er zijn twee typen rijen **Contactpersoon**:

+ Gestreepte contactpersoon – De rij Contactpersoon met een verplichte waarde in het veld **Bedrijf**.
+ Niet-gestreepte contactpersoon – De rij Contactpersoon met een leeg veld **Bedrijf**.

In de tabel **Contactpersoon** kunnen de volgende typen rijen worden opgeslagen:

Rijtype | Beschrijving
---|---
Een persoon die een klant is, bijvoorbeeld een verkoopbare contactpersoon of een B2C-klant. | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is en het veld **Is klant** is ingesteld op **Ja**.
Een persoon die een leverancier is, bijvoorbeeld een eenmansbedrijf als leverancier. | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is en het veld **Is leverancier** is ingesteld op **Ja**.
Een persoon die zowel een klant als leverancier is. | Een gestreepte contactpersoonrecord waarbij het veld **Bedrijf** niet leeg is, het veld **Is klant** is ingesteld op **Ja** en het veld **Is leverancier** is ingesteld op **Ja**. Een persoon kan zowel een fabrikant voor een product als een klant voor een ander product zijn. Beide Finance and Operations-apps en Twee keer wegschijven ondersteunen deze relatie.
Een persoon die een contactpersoon is voor een organisatie, maar geen klant of leverancier is. | Een niet-gestreepte contactpersoonrecord waarbij het veld **Bedrijf** leeg is, het veld **Is klant** is ingesteld op **Nee** en het veld **Is leverancier** is ingesteld op **Nee**.

## <a name="contact-for-party"></a>Contactpersoon voor partij

In **Contactpersoon voor partij** worden N:N-relaties tussen rijen in **Rekening** en **Contactpersoon** opgeslagen en verwerkt. De gestreepte rijen **Contactpersoon** kunnen uit de niet-gestreepte rijen worden gefilterd om alleen de niet-gestreepte rijen **Contactpersoon** aan een rij **Rekening** of **Leverancier** te koppelen.

Natasha Jones en Miguel Reyes zijn bijvoorbeeld dierenartsen die zorg bieden aan boerderijen in hun regio's. Natasha is actief in het gebied rond Seattle en Miguel in Kent. In de app voor klantbetrokkenheid worden de boerderijen weergegeven als klanten en de dierenartsen als contactpersonen. Eén record **Contactpersoon** van Natasha is gekoppeld aan alle boerderijen waarmee Natasha werkt. Op dezelfde manier is één record **Contactpersoon** van Miguel gekoppeld aan alle boerderijen waarmee hij werkt.

Deze relaties worden opgeslagen in de tabel **Contactpersoon voor partij**. U vindt de informatie in de kant-en-klare formulieren:

+ Wanneer u zich in het formulier **Rekening** bevindt, is er een tabblad met de naam **Gekoppelde contactpersonen**. Gebruik dit tabblad om een of meer contactpersonen aan de rij **Rekening** te koppelen. In dit formulier wijst u een contactpersoon voor een organisatie toe. Nadat u contactpersonen hebt toegewezen, kunt u er een kiezen als primaire contactpersoon voor die rekening. Via het formulier **Snel maken** kunt u alleen een contactpersoon kiezen. Het gedrag is hetzelfde wanneer u het formulier **Leverancier** gebruikt en het recordtype **Organisatie** is.
+ Wanneer u zich in het formulier **Contactpersoon** bevindt en de rij een klant of leverancier of beide is (een gestreepte contactpersoon), is er een tabblad met de naam **Gekoppelde contactpersonen**. Gebruik dit tabblad om een of meer contactpersonen te koppelen. In dit formulier wijst u een contactpersoon voor de B2C-klant of leverancier toe. Nadat u contactpersonen hebt toegewezen, kunt u er een kiezen als primaire contactpersoon. Via het formulier **Snel maken** kunt u alleen een contactpersoon kiezen.
+ Wanneer u zich in het formulier **Contactpersoon** bevindt en de rij een contactpersoon is (een niet-gestreepte contactpersoon), is er een tabblad met de naam **Gekoppelde organisaties**. Gebruik dit tabblad om een of meer klanten of leveranciers te koppelen. In dit formulier wijst u een contactpersoon of leverancier toe aan de onderliggende contactpersoon. De klant of leverancier kan een organisatie, een persoon of beide zijn. U kunt altijd slechts één waarde kiezen uit de vier velden.

    ![Tabblad Gekoppelde organisaties](media/party-gab-image3.png)

    + Als u **Partij-id** kiest, wordt de onderliggende contactpersoon toegewezen aan alle rollen van de gekozen partij.
    + Als u **Gekoppelde contactpersoon** kiest, selecteert u de gestreepte contactpersoon die van het persoonstype is.
    + Als u **Gekoppeld account** of **Leverancier** kiest, selecteert u een organisatie.

    Ongeacht uw keuze, wordt de koppeling tot stand gebracht op partijniveau en is deze van toepassing op alle rollen van de partij en opgeslagen in de entiteit Contactpersoon voor partij.

> [!Note]
> De weergavenaam voor de tabel **Contactpersoon voor partij** in de app voor klantbetrokkenheid is **Contactpersoon voor klant/leverancier**.

Als u een rij **Contactpersonen** opent waarin **Is klant** op **Nee** is ingesteld en **Is leverancier** op **Nee**, wordt het tabblad **Gekoppelde organisaties** weergegeven. Gebruik dit tabblad om een of meer klant- of leveranciersorganisaties aan de contactpersoon te koppelen.

Als u een rij **Contactpersonen** opent waarin **Is klant** op **Ja** is ingesteld of **Is leverancier** op **Ja**, dan wordt het tabblad **Gekoppelde contactpersonen** weergegeven. Gebruik dit tabblad om een of meer contactpersonen te koppelen.

## <a name="postal-address"></a>Postadres

Er is een nieuw tabblad met de naam **Adressen** beschikbaar in de formulieren **Rekening**, **Contactpersoon** en **Leverancier**. **Adressen** biedt ondersteuning voor N-adressen met behulp van een raster, zoals in deze afbeelding wordt weergegeven:

![Raster voor postadres](media/party-gab-image4.png)

+ In de kolom **Postadresrollen** wordt het doel van het adres weergegeven.
+ In de kolom **Is primair** wordt het primaire adres weergegeven.
+ In de kolom **Adresnummer** wordt de adresvolgorde weergegeven.
+ Met de knop **+ Nieuw adres** kunt u een nieuw adres maken. U kunt zoveel adressen maken als u wilt.

De velden **Adres 1** en **Adres 2** op het tabblad **Overzicht** van het formulier **Rekening** komen overeen met respectievelijk de adressen voor **aflevering** en **facturen**.

![Tabblad Overzicht voor postadres](media/party-gab-image5.png)

De velden **Adres 1**, **Adres 2** en **Adres 3** op het tabblad **Overzicht** van het formulier **Contactpersoon** komen overeen met respectievelijk de adressen voor **bedrijf**, **aflevering** en **facturen**.

## <a name="electronic-address"></a>E-mailadres

Er is een nieuw tabblad met de naam **Elektronische adressen** beschikbaar in de formulieren **Rekening**, **Contactpersoon** en **Leverancier**. **Adressen** biedt ondersteuning voor N-adressen met behulp van een raster, zoals in deze afbeelding wordt weergegeven:

![Raster voor elektronisch adres](media/party-gab-image6.png)

+ In de kolom **Type** wordt het type adres weergegeven.
+ In de kolom **Is primair** wordt het primaire adres weergegeven.
+ In de kolom **Doel** wordt het doel van het elektronische adres weergegeven.
+ Met de knop **+ Nieuw elektronisch adres** kunt u een nieuw adres maken. U kunt zoveel adressen maken als u wilt.

Elektronische adressen zijn alleen beschikbaar in dit raster. In toekomstige releases worden alle velden voor elektronische en postadressen verwijderd van andere tabbladen, bijvoorbeeld de tabbladen **Overzicht** en **Details**.

## <a name="setup-instructions"></a>Instructies voor instellingen

Als u een bestaande klant voor Twee keer wegschijven bent, zijn de volgende installatie-instructies vereist. Anders kunt u deze sectie overslaan.

1. Stop de volgende kaarten, omdat ze niet meer nodig zijn. Voer in plaats daarvan de kaart Contactpersonen V2 (msdyn_contactforparties) uit.

    + CDS-contactpersonen V2 en Contactpersonen (verwijst naar klantcontactpersonen)
    + CDS-contactpersonen V2 en Contactpersonen (verwijst naar leverancierscontactpersonen)

2. De volgende entiteitstoewijzingen worden bijgewerkt voor partijfunctionaliteit, dus de nieuwste versie moet op deze toewijzingen worden toegepast.

Toewijzing | Update naar deze versie | Wijzigingen
---|---|---
Klanten V3 (rekeningen) | 1.0.0.5 |PartyNummer en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
Klant V3 (contacts) | 1.0.0.5 | PartyNummer en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
Leveranciers V2 (msdyn_vendors) | 1.0.0.6 | PartyNummer en andere partijgerelateerde velden, bijvoorbeeld voor de naam, persoonlijke gegevens, postadressen, elektronische contactadressen en dergelijke zijn verwijderd.
CDS-verkoopoffertekopteksten (quotes) | 1.0.0.6 | De contactpersoon is vervangen door de verwijzing ContactforParty.
Kopteksten van verkoopfacturen V2 (invoices) | 1.0.0.4 | De contactpersoon is vervangen door de verwijzing ContactforParty.
CDS-verkooporderkopteksten (salesorders) | 1.0.0.5 | De contactpersoon is vervangen door de verwijzing ContactforParty.
Contactpersonen V2 (msdyn_contactforparties) | 1.0.0.2 | Dit is een nieuwe toewijzing. Als u een eerdere versie van de partijoplossing hebt, moet u deze toewijzing bijwerken naar de nieuwste versie zoals vermeld.
CDS-postadreslocaties partij (msdyn_partypostaladdresses) | 1.0.0.1  | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van de preview-release van de functie voor partijen.
Historie van CDS-postadres V2 (msdyn_postaladdresses) | | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van de preview-release van de functie voor partijen.
CDS-postadreslocaties (msdyn_postaladdresscollections) | | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van de preview-release van de functie voor partijen.
Partijcontacten V3 (msdyn_partyelectronicaddresses) | | Dit is een nieuwe toewijzing die is toegevoegd als onderdeel van deze release.

## <a name="templates"></a>Sjablonen

Een verzameling tabeltoewijzingen werkt samen voor de interactie tussen partij en globaal adresboek, zoals in de volgende tabel wordt weergegeven.

Finance and Operations-app | Customer Engagement-app     | Beschrijving
----------------------------|-----------------------------|------------
[Titels contactpersoon](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Klanten V3](mapping-reference.md#101) | rekeningen |
[Klanten V3](mapping-reference.md#116) | contacten |
[CDS-partijen](mapping-reference.md#220) | msdyn_parties |
[CDS-locaties van postadres van partij](mapping-reference.md#233) | msdyn_partypostaladdresses |
[Historie van CDS-postadres V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS-locaties van postadres](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-verkoopoffertekoptekst](mapping-reference.md#215) | offertes |
[CDS-verkooporderkopteksten](mapping-reference.md#217) | salesorders |
[Afsluitingen](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Contactpersonen V2](mapping-reference.md#221) | msdyn_contactforparties |
[Besluitvormingsrollen](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Taakfuncties dienstverband](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Loyaliteitsniveaus](mapping-reference.md#226) | msdyn_loyaltylevels |
[Contactpersonen partij V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Persoonlijke karaktertypen](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Kopteksten van verkoopfacturen V2](mapping-reference.md#118) | facturen |
[Aanhef](mapping-reference.md#228) | msdyn_salutations |
[Leveranciers V2](mapping-reference.md#202) | msdyn_vendors |

Zie [Toewijzingsverwijzing voor twee keer wegschrijven](mapping-reference.md) voor meer informatie.
