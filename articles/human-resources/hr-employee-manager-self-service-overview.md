---
title: Overzicht van Selfservice werknemer en Selfservice manager
description: Dit artikel bevat een overzicht van de werkgebieden Selfservice werknemer en Selfservice manage.
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 116c85c53b0ec2fe1e1fd2d1fbc2738f5b6351fb
ms.sourcegitcommit: 1fdca917e01470fbd5d3051adb85fd63e8624b47
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4418060"
---
# <a name="employee-and-manager-self-service-overview"></a>Overzicht van Selfservice werknemer en Selfservice manager

Dit artikel bevat een overzicht van de werkgebieden Selfservice werknemer en Selfservice manage.

## <a name="edit-personal-details"></a>Persoonlijke gegevens bewerken

Zie [Persoonlijke gegevens bewerken](hr-employee-manager-self-service-edit-personal-information.md) als u persoonlijke gegevens wilt toevoegen of wijzigen.

## <a name="user-not-assigned-to-a-worker-record"></a>Gebruiker is niet toegewezen aan een medewerkersrecord

Als u de gebruiker op de pagina **Gebruikers** niet aan een **Medewerker** srecord hebt gekoppeld, wordt het volgende bericht weergegeven:

**Uw gebruikers-id is niet gekoppeld aan uw werknemerregistratie in het systeem. U kunt uw gegevens niet weergeven of bijwerken tot dit wel is gekoppeld. Neem contact op met uw manager of ondersteuningsteam voor assistentie.**

Als u een gebruiker aan een **Medewerker** srecord wilt koppelen, gaat u naar **Gebruikers** en selecteert u de gebruiker. Selecteer **Bewerken**, voeg de bijbehorende medewerker toe aan het veld **Persoon** op het formulier en selecteer **Opslaan**. U zou nu toegang moeten hebben tot selfservice voor werknemers.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Beveiligingsvereisten voor Selfservice voor werknemers en manager

Voor Selfservice voor werknemers en manager zijn twee beveiligingsrollen vereist:

- Werknemers hebben de rol van Werknemer nodig.
- Managers hebben zowel de rol van Werknemer als van Manager nodig.

>[!NOTE]
>U kunt aangepaste rollen ook gebruiken voor toegang tot de Selfservice voor werknemers en managers zolang deze toegang hebben tot werkruimten voor werknemer en manager.<br>
>De toegang van een manager tot werknemersgegevens is gebaseerd op de huidige positieregelhiërarchie die is gedefinieerd in Human Resources.

## <a name="employee-self-service"></a>Selfservice werknemer

Op het tabblad **Mijn gegevens** wordt de volgende informatie weergegeven voor de selfservice voor werknemers.  

### <a name="summary"></a>Overzicht

In **Werkitems die aan mij zijn toegewezen** worden alle goedkeuringen en werkstroomitems weergegeven die aan de werknemer zijn toegewezen. U kunt werkstroomitems configureren om e-mailberichten te verzenden naar de gebruiker.

In **Aan mij toegewezen vragenlijsten** worden alle geplande vragenlijsten weergegeven die rechtstreeks aan de werknemer of groep zijn toegewezen.

In **Adresboek van bedrijf** kunnen werknemers informatie opzoeken over personen in de organisatie. Openbare contactgegevens zijn beschikbaar voor alle werknemers. Het adresboek van het bedrijf is beperkt tot het bedrijf waarbij de werknemer zich heeft aangemeld.

In **Teamagenda** worden de agendagegevens van uw team weergegeven. Zie [Team- en bedrijfsagenda's weergeven](hr-employee-self-service-calendar.md) voor meer informatie.

### <a name="my-career-information"></a>Informatie over mijn loopbaan

De sectie **Mijn loopbaangegevens** van Selfservice werknemer bevat kaarten met betrekking tot verlof en verzuim, prestatiebeheer, competenties, vergoedingen, taken en bijlagen.

De kaart **Verlofsaldi** bevat de saldi voor de geregistreerde plannen. Uw saldo wordt voorspeld op basis van uw toerekeningsmethode. U kunt verlofaanvragen invoeren en indienen, waarna een goedkeuringswerkstroomproces wordt uitgevoerd. Zie [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md) voor meer informatie over verlof en verzuim.

Op de kaart **Taken** worden de taken weergegeven die aan u zijn toegewezen en u kunt u deze weergeven en beheren.

Op de kaart **Volgende ingeschreven cursus** wordt de volgende cursus weergegeven waarvoor u bent ingeschreven. U kunt alle open cursussen weergeven en u hiervoor inschrijven. Op deze kaart worden alle cursussen weergegeven die zijn geopend voor inschrijving met de status **Begonnen** en waarvoor werknemers zichzelf kunnen registreren. Afhankelijk van de instellingen van uw organisatie, moet uw cursusregistratie mogelijk worden goedgekeurd.

Op de kaart **Certificaten** worden het certificaat en de vervaldatum weergegeven voor het certificaat waarvan de vervaldatum het dichtst bij de huidige datum ligt. U kunt certificaten bijwerken, toevoegen of verwijderen. Afhankelijk van de instellingen van uw organisatie, moeten certificaatupdates mogelijk worden goedgekeurd.

Op de kaart **Volgende geplande beoordeling** wordt uw volgende prestatiebeoordeling weergegeven. U kunt een nieuwe beoordeling starten vanaf deze kaart. Uw manager of HR-vertegenwoordiger kan ook beoordelingen starten. Afhankelijk van de instellingen van uw organisatie, kunt u via deze kaart mogelijk ook beoordelingen weergeven, bijwerken en verzenden.

U kunt uw doelstellingen beheren met de kaart **Prestatiedoelstellingen**. Op deze kaart wordt het aantal doelstellingen weergegeven dat u voor elke status hebt (**Niet gestart**, **Op schema** en **Moet worden verbeterd**). U kunt doelstellingen maken, bijwerken en verwijderen, afhankelijk van uw toegewezen beveiliging op basis van rollen. U kunt desgewenst nieuwe doelstellingen toevoegen vanuit groepen of sjablonen. Managers en HR kunnen ook doelstellingen maken namens werknemers en bepalen hoe gedetailleerd elke doelstelling is. Managers en werknemers kunnen samenwerken aan doelstellingen en activiteiten, metingen en statussen bijwerken. U kunt ook bijlagen toevoegen.

U kunt uw bestaande vaardigheden weergeven op de kaart **Vaardigheden**. U kunt vaardigheden bijwerken, nieuwe vaardigheden toevoegen of vaardigheden verwijderen die u niet meer relevant vindt. Afhankelijk van de instellingen van uw organisatie, moeten wijzigingen in uw vaardigheden mogelijk worden goedgekeurd.

U kunt uw huidige compensatie weergeven op de kaart **Compensatie**. Selecteer **Weergeven** om uw jaarsalaris en laatste verhoging weer te geven. Als u voor meerdere bedrijven werkt, wordt elk jaarbedrag op de kaart weergegeven. Als u uw gedetailleerde compensatiegeschiedenis wilt weergeven, selecteert u het jaarsalaris om het formulier **Geschiedenis van vaste en variabele compensatie** te openen. Toekomstige compensatie wordt niet weergegeven in dit formulier. Als u meerdere dienstverbanden hebt, kunt u schakelen tussen bedrijven in dit formulier om uw compensatiegeschiedenis weer te geven zonder u bij elk bedrijf te hoeven registreren.

U kunt documenten weergeven en beheren met de kaart **Bijlagen**. U kunt alle **externe** bijlagen beheren. Zowel HR als werknemers kunnen bijlagen toevoegen via Selfservice werknemer of het formulier **Medewerker**. Bijlagen zijn standaard ingesteld op **Extern**.

### <a name="additional-information"></a>Aanvullende gegevens

Deze sectie bevat koppelingen naar andere gebieden van Selfservice werknemer en is vergelijkbaar met de sectie **Mijn loopbaangegevens**.

Meld u aan voor vergoedingen via de koppeling **Vergoedingen**. Zie [Overzicht van vergoedingen](hr-benefits-management-overview.md) voor meer informatie over Vergoedingenbeheer.

Onder **Prestaties** kunt u **Prestatiejournalen** selecteren om prestatiejournaalitems te maken die u kunt gebruiken voor prestatiedoelstellingen en -beoordelingen. U kunt **Feedback verzenden** selecteren om feedback te geven voor andere werknemers in uw organisatie. Afhankelijk van de instellingen van uw organisatie worden e-mails mogelijk naar de ontvanger, de afzender en managers verzonden. U kunt feedback verzenden naar alle werknemers binnen de organisatie. Het verzenden van feedback is niet beperkt per bedrijf.

Onder **Competenties** kunt u wijzigingen aanbrengen in **Cursussen**, **Opleiding**, **Vertrouwensposities** en **Beroepservaring.** Afhankelijk van de instellingen van uw organisatie, moeten updates voor deze vaardigheden mogelijk worden goedgekeurd.

U kunt taakdetails weergeven onder **Organisatie**. Functiedetails zijn onder andere vaardigheden, certificaten en verantwoordelijkheidsgebieden voor uw primaire positie. U kunt ook alle geleende uitrustingen bekijken die naar u is uitgecheckt. Afhankelijk van de instellingen van uw organisatie, moeten wijzigingen in geleende uitrusting mogelijk worden goedgekeurd.

Onder **Vragenlijst** ziet u ingevulde vragenlijsten. U kunt ook vragenlijsten voor het hele bedrijf bekijken die nog niet zijn ingevuld. U kunt ervoor kiezen om een vragenlijst op elk gewenst moment te kunnen invullen. De auteur van de vragenlijst kan het tijdsbestek bepalen en instellen voor wie de vragenlijst van toepassing is.

U kunt door de gebruiker gedefinieerde koppelingen configureren in **Parameters personeel**. U kunt bijvoorbeeld koppelingen definiëren naar salarisoverzichten, eindejaarsdocumentatie of externe oplossingen. Deze koppelingen worden onder in deze sectie weer gegeven, maar u kunt ze verplaatsen met behulp van personalisatie.

U kunt ook extra tabbladen maken door Power Apps in te sluiten in het werkgebied Selfservice werknemer. Gebruik het menu **Instellingen** om de pagina te personaliseren met Power Apps. In het menu **Instellingen** kunt u kiezen om een Power App toe te voegen, de details te voltooien en de app in te voegen. Power Apps wordt standaard weergegeven als het eerste tabblad in de reeks. U kunt de volgorde wijzigen met standaardbewerkingen voor aanpassen.

## <a name="my-team"></a>Mijn team

Op het tabblad **Mijn team** wordt de volgende informatie weergegeven voor de selfservice voor managers. Alleen managers hebben toegang tot het tabblad **Mijn team**.

### <a name="personnel-actions"></a>Personeelsacties

Personeelsacties worden weergegeven op basis van de configuratieopties in **Gedeelde HRM-parameters** en **Parameters personeel**. Indien ingeschakeld voor **Medewerkers**, kunnen personeelsacties nieuwe menuopties instellen, waaronder:

- **Nieuwe werknemer aanvragen**
- **Nieuwe contractant aanvragen**
- **Hernieuwde toewijzing van medewerker aanvragen**
- **Ontslag aanvragen**
- **Wijziging compensatie aanvragen**

U kunt deze opties configureren om een optionele werkstroom voor beoordeling en goedkeuring te doorlopen.

Als u **Positieacties** inschakelt, worden de volgende opties ingeschakeld:

- **Nieuwe positie aanvragen**
- **Wijziging van positiedetails aanvragen**

U kunt deze opties ook configureren om een optionele werkstroom voor beoordeling en goedkeuring te doorlopen.

### <a name="summary"></a>Overzicht

De informatie in de sectie **Overzicht** is afhankelijk van de opties die HR heeft geselecteerd in **Parameters personeel**. Op het tabblad **Selfservice manager** van de pagina **Parameters personeel** kunt u opties configureren voor het weergeven van verlopende records en openstaande posities. Door deze opties in te schakelen, bepaalt u wat managers kunnen zien in de sectie **Overzicht**.

U kunt de volgende tegels configureren voor managers:

- **Certificaten die verlopen voor mijn team**
- **Id's die verlopen voor mijn team**
- **Proeftijd die verloopt voor mijn team**
- **Screenings die verlopen voor mijn team**
- **Testen die verlopen voor mijn team**
- **Openstaande posities voor directe en/of indirecte ondergeschikten**
- **Uitstaande verlofaanvragen voor mijn team**
- **Beoordeling van teamvaardigheden**
- **Vaardigheidshiaatanalyse**
- **Teamprestatiejournalen**
- **Teamprestatiedoelstellingen**
- **Beoordelingen van teamprestaties**
- **Vertrekkende medewerkers**

U kunt de volgende opties configureren voor managers om wijzigingen aan te brengen of verlofaanvragen toe te voegen namens hun directe ondergeschikten:

- Getuigschriften
- Cursussen
- Leenartikelen
- Vaardigheden
- Aanvragen voor verlof en verzuim

### <a name="my-team-information"></a>Gegevens van mijn team

Met mijn teamgegevens kunnen managers directe en indirecte ondergeschikten weergeven en bijwerken. Als u toegang tot indirecte ondergeschikten wilt krijgen, selecteert u de werknemer met directe ondergeschikten en kiest u **Team weergeven** op de kaart. Op indirecte ondergeschikten zijn dezelfde opties van toepassing als op directe ondergeschikten. 

#### <a name="summary-tab"></a>Het tabblad Overzicht

Het tabblad **Overzicht** biedt een snel overzicht van uw directe ondergeschikten. Als een directe ondergeschikte ook weer directe ondergeschikten heeft, wordt in het bovenste gedeelte het aantal directe ondergeschikten weergegeven, met de knop **Team weergeven**. De opties boven elke kaart zijn van toepassing op de geselecteerde werknemer. Als u bijvoorbeeld een verlofaanvraag namens een werknemer wilt invoeren, selecteert u de werknemer en kiest u **Verlof aanvragen** boven de kaarten. 

Als u de knop **Details** selecteert nadat u een werknemer hebt geselecteerd, worden de volgende opties weergegeven:

- **Getuigschriften**
- **Compensatie**
- **Cursussen**
- **Controles**
- **verlof**
- **Geleende artikelen**
- **Prestatiedoelstellingen**
- **Geregistreerde cursussen**
- **Vaardigheden**
- **Feedback verzenden**

Afhankelijk van de instellingen van uw organisatie kunt u alleen wijzigingen aanbrengen of een weergave maken.

#### <a name="position-tab"></a>Het tabblad Posities

Op het tabblad **Posities** vindt u een overzicht van werknemers op hun primaire positie. Naam, tegel en afdeling worden weergegeven in het koptekstgebied van elke kaart. Deze kaart bevat:

- **Anciënniteitsdatum**: wordt weergegeven uit de sectie met het medewerkersoverzicht van het medewerkersformulier.
- **Dienstjaren**: wordt berekend op basis van de begindatum van het dienstverband van de werknemer
- **Aantal eerdere posities**: op basis van de positiegeschiedenis wordt bij selectie van deze waarde het gedetailleerde overzicht van alle eerder beklede posities.
- **Geboortedatum**: de maand en dag van de geboortedatum van de werknemer.

U kunt positiegegevens voor directe en indirecte ondergeschikten weergeven.

#### <a name="compensation-tab"></a>Het tabblad Compensatie

Op het tabblad **Compensatie** wordt het jaarsalaris van de werknemer weergegeven. Er wordt een bedrijfs-id weer gegeven onder het salarisbedrag. Als een werknemer meerdere dienstverbanden heeft en door meerdere rechts personen wordt betaald, heeft de werknemer meerdere compensatieplannen. Als u alle compensatieplannen voor rechtspersonen wilt weergeven zonder van bedrijf te wisselen, moet u compensatie voor meerdere bedrijven inschakelen onder **Human Resources > Gedeelde parameters > Geavanceerde toegang > Compensatie voor meerdere bedrijven inschakelen**.

Als u de compensatiegeschiedenis wilt weergeven, selecteert u het salarisbedrag om het formulier **Details** te openen. Alleen huidige en historische records voor vaste en variabele compensatie worden weergegeven in het formulier **Compensatie**. Als een werknemer meer dan één dienstverband heeft, kunt u tussen bedrijven schakelen om de compensatiehistorie in elk bedrijf weer te geven of om compensatie voor meerdere bedrijven in te schakelen in Gedeelde parameters voor Human Resources om alle compensatieplannen weer te geven.

U kunt de compensatie voor directe en indirecte ondergeschikten weergeven.

#### <a name="leave-and-absence-tab"></a>Het tabblad Verlof en verzuim

Op het tabblad **Verlof en verzuim** worden de bovenste saldi weergegeven voor werknemers met activiteit. Selecteer **Details** en selecteer vervolgens **Verlof** om een actie te ondernemen of een volledige lijst met activiteiten weer te geven. In het formulier **Verlof** kunt u saldi, aanvragen, goedgekeurde vrije tijd en prognosesaldi weergeven zodat werknemers hun tijd beter kunnen beheren. Afhankelijk van de instellingen van uw organisatie kunt u ook verlof aanvragen voor uw directe en indirecte ondergeschikten.

#### <a name="performance-goals-tab"></a>Het tabblad Prestatiedoelstellingen

Op het tabblad **Prestatiedoelstellingen** wordt een overzicht van de prestatiedoelstellingen per status weergegeven. Selecteer een waarde voor een status of selecteer prestatiedoelstellingen in **Details** om alle doelstellingen voor een werknemer te bekijken. Managers en werknemers kunnen indien nodig doelstellingen bijwerken gedurende de looptijd van de doelstelling.

Managers kunnen alle doelstellingen voor hun team bekijken via de tegel **Teamprestatiedoelstellingen** in de sectie **Overzicht** van **Mijn team**.

#### <a name="reviews-tab"></a>Het tabblad Recensies

Het tabblad **Recensies** bevat een overzicht van de recensies die de werknemer in elke staat heeft: **In uitvoering**, **Gereed voor beoordeling** en **Eindbeoordeling**. Als u de recensie van een werknemer wilt openen, selecteert u de knop **Details** en vervolgens recensies om samen aan te werken. Afhankelijk van waar een recensie zich in het werkstroomproces bevindt, kunt u zien of de recensie beschikbaar is om te worden bijgewerkt. 

U kunt alle recensies voor uw team bekijken via de tegel **Beoordelingen van teamprestaties** in de sectie **Overzicht** van **Mijn team**.