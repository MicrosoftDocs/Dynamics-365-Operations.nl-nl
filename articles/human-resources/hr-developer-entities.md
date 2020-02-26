---
title: Entiteiten in Common Data Service
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008667"
---
# <a name="common-data-service-entities"></a>Entiteiten in Common Data Service

Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.

Zie [Wat is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) voor meer informatie over Common Data Service.

De volgende Human Resources-entiteiten zijn beschikbaar in Common Data Service.

## <a name="benefit-entities"></a>Vergoedingsentiteiten

**Frequentie van vergoedingenberekening**

| **Velden**        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------|---------------|--------------|----------------|
| Beschrijving       | Text          |              | X              |
| Frequentieregeling | Optieset    | X            | X              |
| Is onveranderbaar      | Twee opties   |              | X              |
| Naam              | Text          | X            | X              |


**Berekeningstarief vergoeding**

| **Velden**  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------|---------------|--------------|----------------|
| Beschrijving | Text          |              | X              |
| Naam        | Text          | X            | X              |
| TierType    | Optieset    | X            | X              |


**Details berekeningstarief vergoeding**

| **Velden**                             | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|----------------------------------------|----------------|--------------|----------------|
| Nummer details berekeningstarief vergoeding | Text           | X            | X              |
| Berekeningstarief-id                    | Zoekopdracht         | X            | X              |
| Bijdragemethode                    | Optieset     | X            | X              |
| Geldig vanaf                              | Alleen datum      | X            | X              |
| Werkgeversbijdrage                  | Decimaal getal |              | X              |
| Vervaldatum                             | Alleen datum      | X            | X              |
| WorkerDeduction                        | Decimaal getal |              | X              |


**Vergoedingstype**

| **Velden**           | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Optieset    |              | X              |
| Beschrijving          | Text          |              | X              |
| Naam                 | Text          | X            | X              |
| PayrollCategory      | Optieset    |              | X              |


**Vergoedingsplan**

| **Velden**                               | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|------------------------------------------|----------------|--------------|----------------|
| Achterstallige limietmethode                      | Optieset     |              | X              |
| Vergoedingstype                             | Zoekopdracht         | X            | X              |
| Bijdragelimietmethode                | Optieset     |              | X              |
| Bijdragemethode                      | Optieset     |              | X              |
| Valuta                                 | Zoekopdracht         |              | X              |
| Inhoudingsprioriteit                       | Geheel getal   |              | X              |
| Standaardbedrag van bijdragelimiet        | Valuta       |              | X              |
| Standaardbijdragelimietbedrag (basis) | Valuta       |              | X              |
| Standaardperiode van bijdragelimiet        | Optieset     |              | X              |
| Standaardbedrag van inhoudingslimiet           | Valuta       |              | X              |
| Standaardinhoudingslimietbedrag (basis)    | Valuta       |              | X              |
| Standaardperiode van inhoudingslimiet           | Optieset     |              | X              |
| Beschrijving                              | Text           |              | X              |
| Wisselkoers                            | Decimaal getal |              | X              |
| Is extra salarisverwerking                | Twee opties    |              | X              |
| Is aan te geven onder wet Betaalbare zorg        | Twee opties    |              | X              |
| Wordt achterstallig gegenereerd                      | Twee opties    |              | X              |
| Is berekening brutowaarde                              | Twee opties    |              | X              |
| Is primair                               | Twee opties    |              | X              |
| Naam                                     | Text           | X            | X              |
| Gevolgen voor salaris                           | Optieset     |              | X              |
| Type pensionering                          | Optieset     |              | X              |


**Aanstellingsentiteit**

| **Velden**                     | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|--------------------------------|----------------|--------------|----------------|
| Aangepaste begindatum medewerker     | Datum en tijd  |              | X              |
| Bedrijf                        | Zoekopdracht         | X            | X              |
| Bedrag eenheid opzegging werkgever | Decimaal getal |              | X              |
| Eenheid opzegging werkgever        | Optieset     |              | X              |
| Einddatum dienstverband            | Datum en tijd  |              | X              |
| Nummer dienstverband              | Text           | X            | X              |
| Begindatum dienstverband          | Datum en tijd  |              | X              |
| Laatste werkdag              | Datum en tijd  |              | X              |
| Overgangsdatum                | Datum en tijd  |              | X              |
| Geldig vanaf                     | Datum en tijd  | X            | X              |
| Geldig tot                       | Datum en tijd  |              | X              |
| Medewerker                         | Zoekopdracht         | X            | X              |
| Hoeveelheid opzegging medewerker           | Decimaal getal |              | X              |
| Begindatum medewerker             | Datum en tijd  |              | X              |
| Medewerkertype                    | Optieset     | X            | X              |
| Eenheid opzegging medewerker          | Optieset     |              | X              |

## <a name="worker-entities"></a>Entiteiten medewerker

**Etnische afkomst**

| **Velden**         | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|--------------------|---------------|--------------|----------------|
| Beschrijving        | Text          |              | X              |
| Naam etnische afkomst | Text          | X            | X              |


**Taal**

| **Velden**    | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|---------------|---------------|--------------|----------------|
| Beschrijving   | Text          |              | X              |
| Taalnaam | Text          | X            | X              |


**Oorlogsveteraanstatus**

| **Velden**           | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------|---------------|--------------|----------------|
| Beschrijving          | Text          |              | X              |
| Is beschermd veteraan | Twee opties    |              | X              |
| Taalnaam        | Text          | X            | X              |


**Medewerker**

| **Velden**                | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|---------------------------|---------------|--------------|----------------|
| Geboortedatum                 | Alleen datum     |              | X              |
| Beschrijving               | Text          |              | X              |
| E-mailadres 1           | E-mailadres         |              | X              |
| E-mailadres 2           | E-mailadres         |              | X              |
| Facebook-identiteit         | Text          |              | X              |
| Voornaam                | Text          |              | X              |
| Volledige naam                 | Text          |              | X              |
| Geslacht                    | Optieset    |              | X              |
| Generatie                | Text          |              | X              |
| Is contact per e-mail toegestaan  | Twee opties   |              | X              |
| Is telefonisch contact toegestaan  | Twee opties   |              | X              |
| Achternaam                 | Text          |              | X              |
| LinkedIn-identiteit         | Text          |              | X              |
| Manager                   | Zoekopdracht        |              | X              |
| Tweede naam               | Text          |              | X              |
| Mobiele telefoon              | Telefoonnummer         |              | X              |
| Office Graph-id   | Text          |              | X              |
| Primair e-mailadres     | E-mailadres         |              | X              |
| Primair telefoonnummer         | Telefoonnummer         |              | X              |
| Beroep                | Text          |              | X              |
| Sociaal netwerk 1          | Optieset    |              | X              |
| Sociaal netwerk 2          | Optieset    |              | X              |
| Identiteit sociaal netwerk 1 | Text          |              | X              |
| Identiteit sociaal netwerk 2 | Text          |              | X              |
| Bron                    | Optieset    | X            | X              |
| Status                    | Optieset    | X            | X              |
| Telefoonnummer 1               | Telefoonnummer         |              | X              |
| Telefoonnummer 2               | Telefoonnummer         |              | X              |
| Telefoonnummer 3               | Telefoonnummer         |              | X              |
| Twitter-identiteit          | Text          |              | X              |
| Gebruiker                      | Zoekopdracht        |              | X              |
| Website-URL               | URL           |              | X              |
| Werknemernummer             | Text          | X            | X              |
| Medewerkertype               | Optieset    | X            | X              |
| Yomi-voornaam           | Text          |              | X              |
| Yomi volledige naam            | Text          |              | X              |
| Yomi-achternaam            | Text          |              | X              |
| Yomi tweede voornaam          | Text          |              | X              |


**Adres medewerker**

| **Velden**           | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|----------------------|----------------|--------------|----------------|
| Nummer adres       | Text           | X            | X              |
| Adrestype         | Optieset     | X            | X              |
| Plaats                 | Text           |              | X              |
| Land of regio    | Text           |              | X              |
| District               | Text           |              | X              |
| Fax                  | Telefoonnummer          |              | X              |
| Heeft voorkeur         | Twee opties    |              | X              |
| Breedtegraad             | Decimaal getal |              | X              |
| Regel 1               | Text           |              | X              |
| Regel 2               | Text           |              | X              |
| Regel 3               | Text           |              | X              |
| Lengtegraad            | Decimaal getal |              | X              |
| Postcode          | Text           |              | X              |
| Postbus      | Text           |              | X              |
| Code verzendwijze | Geheel getal   |              | X              |
| Staat of provincie    | Text           |              | X              |
| Telefoonnummer 1          | Telefoonnummer          |              | X              |
| Telefoonnummer 2          | Telefoonnummer          |              | X              |
| Telefoonnummer 3          | Telefoonnummer          |              | X              |
| UPS-zone             | Text           |              | X              |
| UTC-verschil           | Geheel getal   |              | X              |
| Medewerker               | Zoekopdracht         | X            | X              |


**Persoonsgegevens van medewerker**

| Velden                             | Gegevenstype    | Vereist | Zoekbaar |
|------------------------------------|--------------|----------|------------|
| Geboorteplaats                         | Text         |          | X          |
| Land of regio van geboorte            | Optieset   |          | X          |
| Geboortedatum                          | Alleen datum    |          | X          |
| Land of regio van burgerschap      | Optieset   |          | X          |
| Datum van overlijden                      | Alleen datum    |          | X          |
| Verificatiedatum veteraan met handicap | Alleen datum    |          | X          |
| Opleiding                          | Text         |          | X          |
| Etnische afkomst                     | Zoekopdracht       |          | X          |
| ExpatriateEndDate                  | Alleen datum    |          | X          |
| ExpatriateStartDate                | Alleen datum    |          | X          |
| Land of regio waar vader is geboren     | Optieset   |          | X          |
| Geslacht                             | Optieset   |          | X          |
| Is uitgeschakeld                        | Twee opties  |          | X          |
| Is veteraan met handicap                | Twee opties  |          | X          |
| Is expatregeling van toepassing    | Twee opties  |          | X          |
| Is fulltimestudent               | Twee opties  |          | X          |
| Burgerlijke staat                     | Optieset   |          | X          |
| Einddatum militaire dienst          | Alleen datum    |          | X          |
| Begindatum militaire dienst        | Alleen datum    |          | X          |
| Land of regio waar moeder is geboren     | Optieset   |          | X          |
| Land of regio nationaliteit      | Optieset   |          | X          |
| Moedertaal                    | Zoekopdracht       |          | X          |
| Aantal gezinsleden               | Geheel getal |          |            |
| Veteraanstatus                     | Zoekopdracht       |          | X          |
| Medewerker                             | Zoekopdracht       | X        | X          |
| Persoonlijk detailnummer medewerker      | Text         | X        | X          |


**Bankrekening medewerker**

| **Velden**                 | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------------|---------------|--------------|----------------|
| Rekeninghouder             | Text          |              | X              |
| Rekening-id     | Text          |              | X              |
| Adresomschrijving        | Text          |              | X              |
| Bankrekeningtype          | Optieset    |              | X              |
| Banklocatiecode         | Text          |              | X              |
| Vestigingsnaam                | Text          |              | X              |
| Vestigingsnummer              | Text          |              | X              |
| Plaats                       | Text          |              | X              |
| Land of regio          | Text          |              | X              |
| District                     | Text          |              | X              |
| Beschrijving                | Text          |              | X              |
| Naam gebied              | Text          |              | X              |
| E-mailadres                      | Text          |              | X              |
| Toestel                  | Text          |              | X              |
| Fax                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Regel 1                     | Text          |              | X              |
| Regel 2                     | Text          |              | X              |
| Regel 3                     | Text          |              | X              |
| Mobiele telefoon               | Text          |              | X              |
| Naam van persoon             | Text          |              | X              |
| Postcode                | Text          |              | X              |
| Postbus            | Text          |              |                |
| Routenummer             | Text          |              | X              |
| Routenummertype        | Optieset    |              | X              |
| Staat of provincie          | Text          |              | X              |
| SWIFT-code                 | Text          |              | X              |
| Telefoon                  | Text          |              | X              |
| Telexnummer               | Text          |              | X              |
| Website-URL                | Text          |              | X              |
| Medewerker                     | Zoekopdracht        | X            | X              |
| Bankrekeningnummer medewerker | Text          |              | X              |
| Bankrekeningnummer medewerker | Text          | X            | X              |

**Vaste compensatie medewerker**

| Velden                                | Gegevenstype      | Vereist | Zoekbaar |
|---------------------------------------|----------------|----------|------------|
| Bedrijf                               | Zoekopdracht         | X        | X          |
| Compensatietype                     | Optieset     |          | X          |
| Valuta                              | Zoekopdracht         |          | X          |
| Begindatum                        | Alleen datum      |          | X          |
| Gebeurtenis                                 | Zoekopdracht         | X        | X          |
| Wisselkoers                         | Decimaal getal |          | X          |
| Vervaldatum                       | Alleen datum      |          | X          |
| Regelnummer                           | Decimaal getal |          | X          |
| Betalingsfrequentie                         | Zoekopdracht         | X        | X          |
| Loontarief                              | Valuta       |          | X          |
| Loontarief (basis)                       | Valuta       |          | X          |
| Plan                                  | Zoekopdracht         | X        | X          |
| Positie                              | Zoekopdracht         | X        | X          |
| Procestype                          | Optieset     | X        | X          |
| Instellingsregel referentiepunt            | Zoekopdracht         |          | X          |
| Medewerker                                | Zoekopdracht         | X        | X          |
| Nummer vaste compensatie medewerker      | Text           | X        | X          |

**Persoonlijk identificatienummer medewerker**

| Velden                 | Gegevenstype   | Vereist | Zoekbaar |
|------------------------|-------------|----------|------------|
| Beschrijving            | Text        |          | X          |
| Invoertype             | Text        |          | X          |
| Vervaldatum        | Alleen datum   |          | X          |
| Identificatienummer  | Text        | X        | X          |
| Identificatietype    | Zoekopdracht      | X        | X          |
| Is primair             | Twee opties |          | X          |
| Uitgiftedatum             | Alleen datum   |          | X          |
| Uitgifte-instantie         | Zoekopdracht      | X        | X          |
| Medewerker                 | Zoekopdracht      | X        | X          |


## <a name="position-entities"></a>Positie-entiteiten

**Functiepositie**

| **Velden**               | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|--------------------------|----------------|--------------|----------------|
| Activering               | Datum en tijd  |              | X              |
| Beschikbaar voor toewijzing | Datum en tijd  |              | X              |
| Departement               | Zoekopdracht         |              | X              |
| Beschrijving              | Text           |              | X              |
| Voltijds equivalent     | Decimaal getal |              | X              |
| Taak                      | Zoekopdracht         | X            | X              |
| Functiepositienummer      | Text           | X            | X              |
| Positie bovenliggende functie      | Zoekopdracht         |              | X              |
| Positietype            | Zoekopdracht         |              | X              |
| Pensionering               | Datum en tijd  |              | X              |
| Titel                    | Optieset     |              | X              |
| Geldig vanaf               | Datum en tijd  | X            | X              |
| Geldig tot                 | Datum en tijd  |              | X              |


**Positietype**

| **Velden**         | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|--------------------|---------------|--------------|----------------|
| Classificatie     | Optieset    |              | X              |
| Beschrijving        | Text          |              | X              |
| Naam positietype | Text          | X            | X              |


**Medewerkertoewijzing voor positie**

| **Velden**                        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------------------------|---------------|--------------|----------------|
| Functiepositie                      | Zoekopdracht        | X            | X              |
| Toewijzingsnummer positie medewerker | Text          | X            | X              |
| Geldig vanaf                        | Text          | X            | X              |
| Geldig tot                          |               |              | X              |
| Medewerker                            |               | X            | X              |

## <a name="job-entities"></a>Functie-entiteiten

**Functie**

| **Velden**                   | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|------------------------------|----------------|--------------|----------------|
| Onbeperkt aantal posities toestaan    | Twee opties    |              | X              |
| Standaard voltijds equivalent | Decimaal getal |              | X              |
| Beschrijving                  | Text           |              | X              |
| Functieomschrijving              | Text           |              | X              |
| Functiepositie                 | Zoekopdracht         |              | X              |
| Functietype                     | Zoekopdracht         |              | X              |
| Maximumaantal posities  | Geheel getal   |              | X              |
| Naam                         | Text           | X            | X              |
| Titel                        | Optieset     |              | X              |
| Geldig vanaf                   | Datum en tijd  | X            | X              |
| Geldig tot                     | Datum en tijd  |              | X              |


**Functiepositie**

| **Velden**        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------|---------------|--------------|----------------|
| Beschrijving       | Text          | X            | X              |
| Naam van functiepositie | Text          | X            | X              |


**Taaktype**

| **Velden**    | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|---------------|---------------|--------------|----------------|
| Beschrijving   | Text          | X            | X              |
| Vrijstellingsstatus | Optieset    | X            | X              |
| Naam functietype | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Entiteiten voor verlof en verzuim

**Verlofinschrijving**

| **Velden**            | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------------|---------------|--------------|----------------|
| Basis toerekendatum    | Alleen datum     | X            | X              |
| Begindatum toerekening    | Alleen datum     | X            | X              |
| Aangepaste datum           | Alleen datum     | X            | X              |
| Is toerekening uitgesteld  | Twee opties   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| Verlofplan            | Zoekopdracht        | X            | X              |
| Begindatum            | Alleen datum     | X            | X              |
| Niveaubasis            | Optieset    | X            | X              |
| Medewerker                | Zoekopdracht        | X            | X              |


**Banktransactie verlof**

| **Velden**                    | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|-------------------------------|----------------|--------------|----------------|
| Bedrag                        | Decimaal getal | X            | X              |
| Bedrijf                       | Zoekopdracht         | X            | X              |
| Nummer banktransactie verlof | Text           | X            | X              |
| Verlofplan                    | Zoekopdracht         |              | X              |
| Verloftype                    | Zoekopdracht         | X            | X              |
| Transactiedatum              | Alleen datum      | X            | X              |
| Transactienummer            | Decimaal getal | X            | X              |
| Transactietype              | Optieset     | X            | X              |
| Medewerker                        | Zoekopdracht         | X            | X              |


**Verlofplan**

| **Velden**        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------|---------------|--------------|----------------|
| Toerekenfrequentie | Optieset    | X            | X              |
| Bedrijf           | Zoekopdracht        | X            | X              |
| Beschrijving       | Text          |              | X              |
| Verloftype        | Zoekopdracht        | X            | X              |
| Naam              | Text          | X            | X              |
| Begindatum        | Alleen datum     | X            | X              |


**Verlofaanvraag**

| **Velden**           | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------|---------------|--------------|----------------|
| Opmerking              | Text          | X            | X              |
| Bedrijf              | Zoekopdracht        | X            | X              |
| Verlofaanvraagnummer | Text          |              | X              |
| Aanvraagdatum         | Datum en tijd | X            | X              |
| Status               | Optieset    | X            | X              |
| Medewerker               | Zoekopdracht        | X            | X              |


**Details verlofaanvraag**

| **Velden**                  | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|-----------------------------|----------------|--------------|----------------|
| Bedrag                      | Decimaal getal | X            | X              |
| Verlofdatum                  | Datum en tijd  | X            | X              |
| Verlofaanvraag               | Zoekopdracht         | X            | X              |
| Detailnummer verlofaanvraag | Text           | X            | X              |
| Verloftype                  | Zoekopdracht         | X            | X              |


**Verloftype**

| **Velden**      | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------|---------------|--------------|----------------|
| Bedrijf         | Zoekopdracht        | X            | X              |
| Beschrijving     | Text          |              | X              |
| Inkomstencode    | Zoekopdracht        |              | X              |
| Naam verloftype | Text          | X            | X              |


**Werkkalender**

| **Velden**  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------|---------------|--------------|----------------|
| Bedrijf     | Zoekopdracht        | X            | X              |
| Beschrijving | Text          |              | X              |
| Naam        | Text          | X            | X              |


**Werkkalenderdag**

| **Velden**               | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|--------------------------|---------------|--------------|----------------|
| Kalenderdatum            | Alleen datum     | X            | X              |
| Bedrijf                  | Zoekopdracht        |              | X              |
| Status                   | Text          |              | X              |
| Werkkalender            | Zoekopdracht        | X            | X              |
| Nummer werkkalenderdag | Text          | X            | X              |


**Feestdag werkkalender**

| **Velden**  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------|---------------|--------------|----------------|
| Naam        | Text          |              | X              |
| Beschrijving | Text          | X            | X              |


**Feestdagregel werkkalender**

| **Velden**                        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------------------------|---------------|--------------|----------------|
| Datum feestdag                      | Alleen datum     | X            | X              |
| Naam                              | Text          |              | X              |
| Feestdag werkkalender             | Zoekopdracht        | X            | X              |
| Feestdagregelnummer werkkalender | Text          | X            | X              |


**Tijdsinterval werkkalender**

| **Velden**                         | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|------------------------------------|---------------|--------------|----------------|
| Bedrijf                            | Zoekopdracht        |              | X              |
| Eindtijd                           | Geheel getal  |              | X              |
| Begintijd                         | Geheel getal  |              | X              |
| Werkkalender                      | Zoekopdracht        | X            | X              |
| Werkkalenderdag                  | Zoekopdracht        | X            | X              |
| Tijdsintervalnummer werkkalender | Text          | X            | X              |

## <a name="organization-entities"></a>Organisatie-entiteiten

**Bedrijf**

| **Velden**   | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|--------------|---------------|--------------|----------------|
| Bedrijfscode | Text          | X            | X              |
| Naam         | Text          | X            | X              |


**Departement**

| **Velden**        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------|---------------|--------------|----------------|
| Afdelingsnummer | Text          | X            | X              |
| Beschrijving       | Text          |              | X              |
| Naam              | Text          | X            | X              |
| Bovenliggende afdeling | Zoekopdracht        |              | X              |


**Valuta**

| **Velden**         | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|--------------------|----------------|--------------|----------------|
| Valutacode      | Text           | X            | X              |
| Naam valuta      | Text           | X            | X              |
| Valutaprecisie | Geheel getal   | X            | X              |
| Valutasymbool    | Text           | X            | X              |
| Entiteitsafbeelding       | Afbeelding          |              |                |
| Wisselkoers      | Decimaal getal | X            | X              |
| Organisatie       | Zoekopdracht         | X            | X              |
| Status             | Optieset     |              | X              |

## <a name="payroll-entities"></a>Entiteiten salarisadministratie

**Betalingscyclus**

| **Velden**  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------|---------------|--------------|----------------|
| Beschrijving | Text          | X            | X              |
| Frequentie   | Optieset    | X            | X              |
| Naam        | Text          | X            | X              |


**Salarisperiode**

| **Velden**           | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------|---------------|--------------|----------------|
| Standaardbetalingsdatum | Alleen datum     |              | X              |
| Beschrijving          | Text          |              | X              |
| Betalingscyclus            | Zoeken          | X            | X              |
| Salarisperiodenummer    | Text          | X            | X              |
| Einddatum periode      | Alleen datum     | X            | X              |
| Begindatum periode    | Alleen datum     | X            | X              |
| Status               | Optieset    |              | X              |


**Inkomstencode salaris**

| **Velden**              | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------------|---------------|--------------|----------------|
| Beschrijving             | Text          | X            | X              |
| Opnemen in betalingstype | Optieset    | X            | X              |
| Is productief           | Twee opties   | X            | X              |
| Naam                    | Text          |              | X              |
| Hoeveelheidseenheid           | Optieset    |              | X              |
| FMLA-uren bijhouden        | Twee opties   |              | X              |


**Belastingregio**

| **Velden**        | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------|---------------|--------------|----------------|
| Plaats              | Text          |              | X              |
| Land of regio | Text          |              | X              |
| District            | Text          |              | X              |
| Naam              | Text          | X            | X              |
| Staat of provincie | Text          |              | X              |


**Salarisperiode vergoedingsberekeningsfrequentie**

| **Velden**                                      | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-------------------------------------------------|---------------|--------------|----------------|
| Frequentie van vergoedingenberekening                   | Zoekopdracht        | X            | X              |
| Salarisperiodenummer vergoedingsberekeningsfrequentie | Text          | X            | X              |
| Salarisperiode                                      | Zoekopdracht        | X            | X              |


**Bankrekeningvoorschot**

| **Velden**                       | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|----------------------------------|----------------|--------------|----------------|
| Bedrag                           | Valuta       |              | X              |
| Bedrag (basis)                    | Valuta       |              | X              |
| Bankrekening                     | Zoekopdracht         | X            | X              |
| Bankrekeningvoorschotnummer | Text           | X            | X              |
| Bedrijf                          | Zoekopdracht         | X            | X              |
| Valuta                         | Zoekopdracht         |              | X              |
| Wisselkoers                    | Decimaal getal |              | X              |
| Is restant                     | Twee opties    |              | X              |
| Prioriteit                         | Geheel getal   |              | X              |

**Instelling die persoonsidentificatie uitgeeft**

| **Velden**           | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|----------------------|---------------|--------------|----------------|
| Adresomschrijving  | Text          |              | X              |
| Adresregel 1       | Text          |              | X              |
| Adresregel 2       | Text          |              | X              |
| Adresregel 3       | Text          |              | X              |
| Plaats                 | Text          |              | X              |
| Land of regio    | Optieset    |              | X              |
| District               | Text          |              | X              |
| Beschrijving          | Text          |              | X              |
| E-mailadres                | Text          |              | X              |
| Toestel            | Text          |              | X              |
| Fax                  | Text          |              | X              |
| Naam uitgifte-instantie  | Text          | X            | X              |
| Mobiele telefoon         | Text          |              | X              |
| Pagina                 | Text          |              | X              |
| Postcode          | Text          |              | X              |
| Postbus      | Text          |              | X              |
| Sms                  | Text          |              | X              |
| Staat of provincie    | Text          |              | X              |
| Telefoon            | Text          |              | X              |
| Telex                | Text          |              | X              |
| Website-URL          | Text          |              | X              |

**Persoonlijk identificatietype medewerker**

| **Velden**                        | **Gegevenstype**  | **Vereist** | **Zoekbaar** |
|-----------------------------------|----------------|--------------|----------------|
| Toegestane waarden                    | Optieset     |              | X              |
| Land of regio                 | Text           |              | X              |
| Beschrijving                       | Text           |              | X              |
| Vaste lengte                      | Geheel getal   |              | X              |
| Indeling identificatienummer      | Text           |              | X              |
| Type                              | Optieset     |              | X              |
| Persoonlijk identificatietype medewerker | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Entiteiten voor vaste compensatie

**Vastecompensatieplan**

| **Velden**                  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------------------|---------------|--------------|----------------|
| Bedrijf                     | Zoekopdracht        | X            | X              |
| Compensatieraster           | Zoekopdracht        |              | X              |
| Valuta                    | Zoekopdracht        | X            | X              |
| Beschrijving                 | Text          | X            | X              |
| Begindatum              | Alleen datum     | X            | X              |
| Vervaldatum             | Alleen datum     | X            | X              |
| Huurregel                   | Optieset    | X            | X              |
| Naam                        | Text          | X            | X              |
| Tolerantie voor buiten bereik      | Optieset    | X            | X              |
| Betalingsfrequentie               | Zoekopdracht        | X            | X              |
| Aanbeveling toegestaan      | Twee opties   | X            | X              |
| Lijninstelling referentiepunt  | Zoekopdracht        |              | X              |
| Type                        | Optieset    | X            | X              |

**Compensatieraster**

| **Velden**                  | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------------------|---------------|--------------|----------------|
| Bedrijf                     | Zoekopdracht        | X            | X              |
| Valuta                    | Zoekopdracht        |              | X              |
| Beschrijving                 | Text          | X            | X              |
| Begindatum              | Alleen datum     |              | X              |
| Vervaldatum             | Alleen datum     |              | X              |
| Naam                        | Text          | X            | X              |
| Ingesteld referentiepunt       | Zoekopdracht        | X            | X              |
| Type                        | Optieset    | X            | X              |

**Compensatieniveau**

| **Velden**      | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------|---------------|--------------|----------------|
| Beschrijving     | Text          |              | X              |
| Naam            | Text          | X            | X              |
| Type            | Optieset     | X            | X              |

**Compensatiebetalingsfrequentie**

| **Velden**                  | **Gegevenstype**   | **Vereist** | **Zoekbaar** |
|-----------------------------|-----------------|--------------|----------------|
| Jaarlijkse conversiefactor    | Decimaal getal  |              | X              |
| Bedrijf                     | Zoekopdracht          | X            | X              |
| Beschrijving                 | Text            |              | X              |
| Uurconversiefactor    | Decimaal getal  |              | X              |
| Maandelijkse conversiefactor   | Decimaal getal  |              | X              |
| Naam                        | Text            | X            | X              |
| Periode                      | Optieset      |              | X              |
| Wekelijkse conversiefactor    | Optieset      |              | X              |


**Instelling van compensatiereferentiepunten**

| **Velden**          | **Gegevenstype**   | **Vereist** | **Zoekbaar** |
|---------------------|-----------------|--------------|----------------|
| Bedrijf             | Zoekopdracht          | X            | X              |
| Compensatietype   | Optieset      | X            | X              |
| Beschrijving         | Text            | X            | X              |
| Naam                | Text            | X            | X              |

**Regel voor instellen van compensatiereferentiepunten**

| **Velden**            | **Gegevenstype**   | **Vereist** | **Zoekbaar** |
|-----------------------|-----------------|--------------|----------------|
| Bedrijf               | Zoekopdracht          | X            | X              |
| Beschrijving           | Text            | X            | X              |
| Regelnummer           | Decimaal getal  | X            | X              |
| Naam                  | Text            | X            | X              |
| Ingesteld referentiepunt | Zoekopdracht          | X            | X              |

**Compensatieregio**

| **Velden**      | **Gegevenstype** | **Vereist** | **Zoekbaar** |
|-----------------|---------------|--------------|----------------|
| Beschrijving     | Text          | X            | X              |
| Naam            | Text          | X            | X              |

**Compensatiestructuur**

| **Velden**                    | **Gegevenstype**   | **Vereist** | **Zoekbaar** |
|-------------------------------|---------------  |--------------|----------------|
| Bedrag                        | Valuta        |              | X              |
| Basisbedrag                   | Valuta        |              | X              |
| Bedrijf                       | Zoekopdracht          | X            | X              |
| Compensatiestructuurnummer | Text            | X            | X              |
| Valuta                      | Zoekopdracht          |              | X              |
| Wisselkoers                 | Decimaal getal  |              | X              |
| Raster                          | Zoekopdracht          | X            | X              |
| Niveau                         | Zoekopdracht          | X            | X              |
| Referentiepunt               | Zoekopdracht          | X            | X              |
| Lijninstelling referentiepunt    | Zoekopdracht          | X            | X              |

**Gebeurtenis voor vaste compensatie**

| **Velden**            | **Gegevenstype**   | **Vereist** | **Zoekbaar** |
|-----------------------|-----------------|--------------|----------------|
| Bedrijf               | Zoekopdracht          | X            | X              |
| Beschrijving           | Text            | X            | X              |
| Gebeurtenistype            | Optieset      | X            | X              |
| Is actief             | Twee opties     | X            |                |
| Naam                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Entiteitsrelatiemodellen

### <a name="worker"></a>Medewerker
![Medewerker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Functie en functiepositie
![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Vergoedingen
![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Compensatie
![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlaten
![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Werkkalender
![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)
