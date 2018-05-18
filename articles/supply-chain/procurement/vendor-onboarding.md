---
title: Leveranciers onboarden
description: In dit onderwerp wordt het proces voor het onboarden van nieuwe leveranciers beschreven. Hier wordt uitgelegd welke acties vereist zijn voor de verschillende rollen tijdens dit proces.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 325cf12345afcf531181f65a41d0e5262798c14f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="onboard-vendors"></a>Leveranciers onboarden
[!include [banner](../includes/banner.md)]

---

Nieuwe leveranciers kunnen worden ingewerkt en geregistreerd als leveranciers in Microsoft Dynamics 365 for Finance and Operations, op basis van gegevens die worden verzameld van een persoon die de leverancier vertegenwoordigt.

Het proces bestaat uit de volgende stappen, waarbij verschillende rollen acties in het systeem uitvoeren.

1. **OData-gegevensbeheer** – Entiteitimport: de eerste aanvraag is de registratieaanvraag van de potentiële leverancier. Deze aanvraag is gewoonlijk afkomstig van een bron die anonieme toegang toestaat, zoals een door een klant gehoste website. Leveranciers kunnen zich aanmelden door algemene gegevens op te geven, zoals de naam van de leverancier, een verantwoording, het organisatienummer en de naam en het e-mailadres van de contactpersoon. De aanvragen worden geïmporteerd via de interface Gegevensbeheer.
2. **Lijstpagina Aanvraag voor registratie van potentiële leverancier**: op basis van de informatie die is opgegeven in de aanvraag voor registratie van de potentiële leverancier, besluit de inkoopmedewerker of de leverancier moet worden ingewerkt. De inkoopmedewerker analyseert de inkomende aanvraag op de lijstpagina **Aanvragen voor registratie van potentiële leverancier** in Finance and Operations.
3. **Workflow Gebruikersbevoegdheden toekennen**: wanneer een inkoopmedewerker de informatie in de inkomende aanvraag heeft geverifieerd en heeft besloten om door te gaan met het onboarding-proces, ontvangt de nieuwe gebruiker gebruikersbevoegdheden op basis van de workflow voor gebruikersaanvragen en wordt per e-mail een uitnodiging verzonden om de contactpersoon als een geverifieerde gebruiker van Microsoft Dynamics 365 te accepteren.
4. **Wizard Leveranciersregistratie**: de contactpersoon van de leverancier meldt zich met de nieuwe gebruikersaccount aan bij Finance and Operations. Hij of zij voltooit een wizard voor het registreren van leveranciers om informatie, zoals adressen, bedrijfsinformatie, inkoopcategorieën en antwoorden op vragenlijst, te verstrekken.
5. **Goedkeuringsworkflow**: er wordt een leverancieraanvraag met de registratie-informatie gemaakt. Deze leverancieraanvraag wordt verzonden naar een workflow en ter controle en goedkeuring doorgestuurd.
6. **Een leveranciermodel maken en gebruikersrol wijzigen**: als de leverancieraanvraag wordt goedgekeurd, wordt er een leveranciersrecord gemaakt. De gebruikersaccount van de contactpersoon van de leverancier krijgt toestemming voor leverancierssamenwerking of wordt uitgeschakeld.

In de volgende tabel worden de stappen en rollen beschreven die betrokken zijn bij het proces.

| Rol en proces       | OData-gegevensbeheer - Entiteitimport | Lijstpagina Aanvraag voor registratie van potentiële leverancier | Workflow Gebruikersbevoegdheden toekennen | Wizard Leveranciersregistratie | Goedkeuringsworkflow | Een leveranciermodel maken en gebruikersrol wijzigen |
|--------------------------|---|---|---|---|---|---|
| System                   | De aanvraag voor een nieuwe leverancier wordt geïmporteerd. | | | | | Als de leverancieraanvraag wordt geaccepteerd, wordt de leveranciersrecord gemaakt. |
| Inkoopmedewerker | | Start het onboarding-proces. | | | Beoordeel en accepteer of weiger de leverancieraanvraag. | |
| Beheerder            | | | Maak een gebruiker in Finance and Operations en Microsoft Azure. | | | |
| Contactpersoon van leverancier    | | | Verzend e-mail naar de contactpersoon. | Registreer leveranciersgegevens. | | |

Bekijk deze korte YouTube-video voor een snelle demonstratie van het onboardingproces voor leveranciers: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>De aanvraag voor registratie van potentiële leveranciers importeren

De aanvraag voor registratie van potentiële leveranciers is een entiteit in Finance and Operations. U kunt het systeem zo instellen dat gegevens via deze eenheid worden geïmporteerd. 

In de volgende tabel ziet u welke gegevens deze entiteit bevat en kunnen worden geïmporteerd.

| Veld                        | Omschrijving |
|------------------------------|-------------|
| Leveranciernaam                  | De naam van de leverancier. |
| Zakelijke reden       | De reden(en) voor de leverancieraanvraag. |
| Nummer van organisatie          | Een officieel bekend registratienummer. |
| Bedrijfstak             | De bedrijfstak waarin de leverancier actief is. |
| Voornaam van contactpersoon  | De voornaam van de persoon die wordt uitgenodigd om leveranciersgegevens te registreren. |
| Tweede voornaam van contactpersoon | De tweede naam van de persoon die wordt uitgenodigd om leveranciersgegevens te registreren. |
| Achternaam van contactpersoon   | De achternaam van de persoon die wordt uitgenodigd om leveranciersgegevens te registreren. |
| E-mail van contactpersoon       | Het e-mailadres dat wordt gebruikt om een nieuwe gebruiker in Finance and Operations te maken en dat wordt geregistreerd in de Azure Active Directory-account (Azure AD) van de tenant. |
| Datum ingediend               | De datum waarop de aanvraag is gemaakt in een extern systeem. |
| Rechtspersoon                 | De rechtspersoon die van de leverancier het verzoek ontvangt om een leverancier te worden. Deze waarde moet een rechtspersooncode zijn die is geregistreerd in Finance and Operations. Als er geen waarde wordt ontvangen via het importproces, wordt een waarde uit de parameters van Inkoopbeheer toegepast. |
| Leverancierstype                  | De leverancier kan een organisatie of persoon zijn. Het leverancierstype bepaalt hoe de leverancier uiteindelijk wordt gemaakt. |

Als de aanvraag voor registratie van potentiële leveranciers is geïmporteerd, verschijnt deze op de lijstpagina **Aanvraag voor registratie van potentiële leverancier**. Via deze lijstpagina kan een inkoopmedewerker de gebruiker uitnodigen. Een gebruikersaanvraag voor het toekennen van de gebruikersbevoegdheden wordt naar een workflow verzonden.

## <a name="submitting-a-prospective-vendor-user-request"></a>Een gebruikersaanvraag voor potentiële leveranciers verzenden

Het doel van een gebruikersaanvraag voor potentiële leverancier is om de persoon die de eerste aanvraag heeft ingediend, te voorzien van gebruikersbevoegdheden zodat hij of zij zich bij Finance and Operations kan aanmelden via het e-mailaccount dat is opgegeven in de aanvraag voor registratie van potentiële leveranciers.

De aanvraag voor registratie van potentiële leveranciers wordt verwerkt door de werkstroom voor gebruikersaanvragen. Deze workflow communiceert door middel van Azure AD B2B-samenwerking. In Finance and Operations wordt een gebruiker gemaakt die over de juiste beveiligingsinstellingen beschikt.

Voor nieuwe gebruikers worden de volgende beveiligingsrollen ingesteld:

- Externe systeemgebruiker
- Potentiële leverancier (extern)

De nieuwe gebruiker ontvangt een e-mailbericht dat wordt gegenereerd door de workflow voor gebruikersaanvragen. Met dit e-mailbericht wordt de gebruiker uitgenodigd om zich aan te melden bij het systeem.

Zie voor informatie over de configuratie van het e-mailbericht en de workflow in het algemeen de omschrijving van een workflow voor gebruikersaanvragen in [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Leveranciersregistratie

Een gebruiker van een potentiële leverancier die zich bij Finance and Operations aanmeldt, krijgt de eerste pagina van een wizard voor leveranciersregistratie te zien waarin hij of zij leveranciersinformatie kan invoeren.

De wizard is aangepast op basis van de configuratie van de leverancieraanvraag. Het land of de regio waar de leverancier zaken doet, bepaalt om welke gegevens in de wizard wordt verzocht en welke gegevens verplicht zijn.

Zie voor meer informatie over de configuratie van leverancieraanvragen [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md). De volgende tabel biedt een overzicht van de pagina's in de wizard en het doel van elke pagina.

| Pagina                       | Omschrijving |
|----------------------------|-------------|
| Land/regio             | Het land of de regio bepaalt de configuratie van de leverancieraanvraag die wordt toegepast op de overige wizardpagina's. Ook de waarden onder **Btw-status** worden hierop gebaseerd. |
| Voorwaarden       | Deze pagina is mogelijk beschikbaar, afhankelijk van de configuratie van de leverancieraanvraag. Als deze beschikbaar is, moet de gebruiker de algemene voorwaarden bevestigen. |
| Leveranciergegevens         | Deze pagina bevat de naam van de leverancier, die automatisch wordt ingevoerd vanuit de oorspronkelijke aanvraag voor registratie van potentiële leveranciers. Daarnaast bevat de pagina het organisatienummer, het telefoonnummer van de leverancier, het faxnummer en e-mailadres, en de leveranciersadressen voor verschillende doeleinden van de leverancier. |
| Gegevens contactpersoon | Deze pagina bevat de naam van de contactpersoon, die automatisch wordt ingevoerd vanuit de oorspronkelijke aanvraag voor registratie van potentiële leveranciers. De pagina bevat ook het telefoonnummer en e-mailadres van de contactpersoon en de verschillende adressen voor verschillende doeleinden van de contactpersoon. |
| Bedrijfsgegevens       | Deze pagina bevat belastingregistratienummers (voor verschillende landen of regio's) en informatie over het aantal werknemers. Daarnaast wordt aangegeven of de eigenaar van het bedrijf tot een minderheidsgroep behoort. |
| Inkoopcategorieën     | Deze pagina bevat de inkoopcategorieën waarvoor de leverancier goedkeuring aanvraagt. De gebruiker kan categorieën in de hiërarchie van inkoopcategorieën selecteren. U kunt configureren hoeveel niveaus worden weergegeven in de hiërarchie bij **Parameters voor inkoopbeheer** &gt; **Leverancierssamenwerking**, onder **Inkoopbeheer** &gt; **Instelling**. |
| Vragenlijsten             | De wizard kan een reeks vragenlijsten bevatten voor de leverancier. Vragenlijsten die worden weergegeven in de wizard zijn geconfigureerd op basis van de leverancieraanvraag of per inkoopcategorie. Als vragenlijsten per inkoopcategorie zijn geconfigureerd, bepalen de inkoopcategorieën waarvoor de leverancier goedkeuring vraagt welke vragenlijsten worden weergegeven in de wizard. Op de pagina **Inkoopcategorieën** kunt u een vragenlijst onder de betreffende categorie toevoegen en het type activiteit instellen op **Onboarding van leveranciers**. |

Wanneer de potentiële leverancier de wizard voor leveranciersregistratie voltooit, wordt een leverancieraanvraag gemaakt.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Een leverancieraanvraag handmatig of automatisch indienen

Een leverancieraanvraag kan worden gemaakt als een concept en handmatig bij een werkstroom worden ingediend. De leverancieraanvraag kan ook automatisch worden ingediend bij een werkstroom wanneer de wizard voor leveranciersregistratie is voltooid. Een aanvraag kan bijvoorbeeld handmatig worden ingediend als een inkoopmedewerker wil beoordelen of de aanvraag een goedkeuringsproces moet doorlopen voordat deze wordt ingediend bij de werkstroom.

- Selecteer **Parameters voor inkoopbeheer** &gt; **Leverancierssamenwerking** en **Automatisch registratie van potentiële leverancier indienen bij werkstroom** om de leverancieraanvraag zo te configureren dat deze automatisch bij een werkstroom wordt ingediend wanneer de wizard voor leveranciersregistratie is voltooid.

## <a name="vendor-requests"></a>Leverancieraanvragen

Leverancieraanvragen zijn beschikbaar op de pagina **Gebruikersaanvragen voor leverancierssamenwerking**.

Een leverancieraanvraag bevat de informatie die de gebruiker van de potentiële leverancier heeft ingevoerd in de wizard voor leveranciersregistratie.

Met de aanvraag kunt u de leveranciersgegevens bekijken en bepalen of de leverancier een geregistreerde leverancier in Finance and Operations moet worden.

De leverancieraanvraag moet bij een werkstroom worden ingediend en worden doorgestuurd naar de relevante revisoren en fiatteurs. Zie [Workflows voor inkoopbeheer](procurement-sourcing-workflows.md) voor algemene informatie over het instellen van werkstromen.

In de volgende tabel wordt aangegeven welke statussen leverancieraanvragen kunnen hebben:

| Status                     | Omschrijving |
|----------------------------|-------------|
| Concept                      | De leverancieraanvraag is nog niet ingediend. |
| Aanvraag ingediend          | De leverancieraanvraag is ingediend en de eerste stap in de workflow wordt verwerkt. |
| In afwachting van controle             | Als er meerdere controleurs in een workflowtaak bestaan, kan een controleur de taak van het controleren van de leverancieraanvraag accepteren en de controle voltooien. Als er slechts één controleur is, kan die deelnemer de controle uitvoeren door **Voltooid** opnieuw te selecteren in de workflowactie. Hij of zij hoeft de taak niet eerst te accepteren. |
| Aanvraag waarvan goedkeuring in behandeling is   | De leverancieraanvraag is ter goedkeuring doorgestuurd naar de deelnemers en er is een optie om meer informatie aan te vragen. Bij een verzoek om aanvullende informatie wordt het werkitem teruggestuurd naar de aanvrager. De leverancieraanvraag kan in deze status ook worden goedgekeurd of afgewezen. |
| Verzoek om wijziging van aanvraag | Er is extra informatie aangevraagd door de fiatteur en de leverancieraanvraag is doorgestuurd naar de persoon die de leverancieraanvraag heeft ingediend. De indiener kan vereiste gegevens toevoegen en de leverancieraanvraag opnieuw indienen. Als een leverancieraanvraag opnieuw wordt ingediend, wordt de status weer gewijzigd in **Aanvraag waarvan goedkeuring in behandeling is**. |
| Aanvraag goedgekeurd           | Deze status is een definitieve status. |
| Aanvraag afgewezen           | Deze status is een definitieve status. |

## <a name="approving-a-vendor-request"></a>Een leverancieraanvraag goedkeuren

Wanneer een leverancieraanvraag is goedgekeurd, wordt een leverancierrekening gemaakt en wordt de status **Goedgekeurd** weergegeven voor de oorspronkelijke registratieaanvraag van de potentiële leverancier en de leverancieraanvraag.

Voordat u een leverancieraanvraag goedkeurt, selecteert u op de pagina **Nieuwe leverancier** op het sneltabblad **Algemeen** de optie **Leveranciersgroep**.

Als de gebruiker van de potentiële leverancier toegang tot Finance and Operations moet hebben als gebruiker voor leverancierssamenwerking die de leverancier vertegenwoordigt, stelt u de machtiging voor toegang tot leverancierssamenwerking in op **Ja**. Als u de gebruikersaccount wilt uitschakelen waarmee de potentiële leverancier zich heeft geregistreerd, stelt u deze machtiging in op **Nee**.

Als de machtiging voor toegang tot leverancierssamenwerking is ingesteld op **Ja** en de leverancieraanvraag wordt goedgekeurd, wordt een aanvraag om de rollen van de gebruiker te wijzigen verzonden zodat de gebruiker de rollen heeft die zijn gedefinieerd voor het type **Leverancier** in **Externe rollen**. Als deze machtiging is ingesteld op **Nee** en de leverancieraanvraag wordt goedgekeurd, wordt er een verzoek ingediend om de gebruiker te deactiveren. In dit geval moet de workflow voor het deactiveren van een gebruikersaanvraag worden ingesteld.

Wanneer een leverancierrekening moet worden gemaakt wanneer de leverancieraanvraag wordt goedgekeurd, moet de nummerreeks voor het maken van leveranciers op basis van leverancieraanvragen worden ingesteld op **Automatisch**.

Zie voor een overzicht van de toegangsrechten van een gebruiker voor leverancierssamenwerking [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Een leverancieraanvraag afwijzen

Als een leverancieraanvraag wordt afgewezen, moet een reden voor afwijzing worden geselecteerd in de leverancieraanvraag.

Wanneer een leverancieraanvraag wordt afgewezen, wordt een verzoek ingediend om de gebruiker te deactiveren. In dit geval moet de workflow voor het deactiveren van een gebruikersaanvraag worden ingesteld. Zie voor meer informatie [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).

Wanneer een leverancieraanvraag wordt afgewezen, wordt de status **Afgewezen** weergegeven voor de oorspronkelijke registratieaanvraag van de potentiële leverancier en de leverancieraanvraag.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Een registratieaanvraag van de potentiële leverancier met diverse statussen verwijderen

De diverse statussen van de registratieaanvraag van een potentiële leverancier bieden een overzicht van de voortgang van de aanvraag.

Met de actie **Verwijderen** in de registratieaanvraag van de potentiële leverancier kunt u de gemaakte keten van records opruimen en verwijderen, en de gebruikersaccount uitschakelen. Het resultaat van de actie **Verwijderen** verschilt, afhankelijk van de status van de registratieaanvraag van de potentiële leverancier, zoals wordt aangegeven in de volgende tabel.


|          Status          |                                                                                     Omschrijving van status                                                                                      |                                                                                                                                                            Resultaat van de actie Verwijderen                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Nieuw            |                                                                         Er zijn acties uitgevoerd op de aanvraag.                                                                          |                                                                                                                                              De aanvraag voor registratie van de potentiële leverancier wordt verwijderd.                                                                                                                                               |
|      Gebruiker aangevraagd      | Wanneer u <strong>Gebruiker uitnodigen</strong> selecteert, wordt de status gewijzigd in <strong>Gebruiker aangevraagd</strong> en wordt er een gebruikersaanvraag voor een potentiële leverancier gemaakt en ingediend bij een workflow voor gebruikersaanvragen. |                                                                                                          U kunt een gebruikersaanvraag voor potentiële leveranciers met deze status niet verwijderen omdat de workflow voor gebruikersaanvragen nog niet is beëindigd.                                                                                                          |
|       Gebruiker uitgenodigd       |                                                               De workflow voor gebruikersaanvragen is goedgekeurd en de gebruiker is gemaakt.                                                               |                                                                                                                      Er wordt een verzoek gemaakt om de gebruiker te deactiveren en de gebruikersaanvraag voor de registratie van een potentiële leverancier wordt verwijderd.                                                                                                                      |
| Registratie in uitvoering |                                                         De nieuwe gebruiker heeft zich aangemeld en heeft de wizard voor leveranciersregistratie gestart.                                                          |                                                                                     Er wordt een verzoek gemaakt om de gebruiker te deactiveren en de aanvraag voor registratie van de potentiële leverancier en de ingevoerde gegevens in de wizard voor leveranciersregistratie worden verwijderd.                                                                                      |
|  Leverancieraanvraag gemaakt  |                                                                     De wizard voor leveranciersregistratie is voltooid.                                                                      | Er wordt een verzoek gemaakt om de gebruiker te deactiveren en de aanvraag voor registratie van de potentiële leverancier, de ingevoerde gegevens in de wizard voor leveranciersregistratie en de leverancieraanvraag worden verwijderd.<blockquote>[!NOTE]<br>U kunt de actie <strong>Verwijderen</strong> niet verwijderen wanneer de leverancieraanvraag zich in een controleproces in de workflow bevindt.</blockquote> |
|         Goedgekeurd         |                                                                               De leverancieraanvraag is goedgekeurd.                                                                               |                                                                                                   De aanvraag voor registratie van de potentiële leverancier, de ingevoerde gegevens in de wizard voor leveranciersregistratie en de leverancieraanvraag worden verwijderd.                                                                                                    |
|         Afgewezen         |                                                                               De leverancieraanvraag is afgewezen.                                                                               |                                                                                                   De aanvraag voor registratie van de potentiële leverancier, de ingevoerde gegevens in de wizard voor leveranciersregistratie en de leverancieraanvraag worden verwijderd.                                                                                                    |


