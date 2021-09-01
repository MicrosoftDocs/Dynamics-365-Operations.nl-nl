---
title: Een nieuw vergoedingsplan maken
description: Vergoedingsplannen maken in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4219c59141a0664e776f1ab099288a7b2db9139d83e1e5bfab7f7b2fbca128a8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731338"
---
# <a name="create-a-benefit-plan"></a>Een vergoedingsplan maken

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt beschreven hoe u vergoedingsplannen in Dynamics 365 Human Resources instelt.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer **Nieuw**.

3. Geef op het tabblad **Algemeen** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Plan** | Een unieke id voor het plan. |
   | **Beschrijving** | Een omschrijving van het plan. |
   | **Plantype** | Wanneer u een nieuw plan maakt, moet u het plantype opgeven. Een plantype is een groepering op hoog niveau van specifieke typen vergoedingen. Elk plantype geeft aan of een werknemer zich kan inschrijven voor meerdere plannen van dat type en of contactpersonen begunstigden of gezinsleden zijn. In het plantype worden ook de dekkingsopties gedefinieerd. U kunt nieuwe aangepaste plantypen maken die zijn afgestemd op de door u aangeboden vergoedingen. De belangrijkste typen vergoedingsplannen zijn: <ul><li>401K</li><li>ADD</li><li>Dental</li><li>Fitness</li><li>FSA</li><li>Life</li><li>LTD</li><li>Medical</li><li>PTO</li><li>STD</li><li>Vision</li></ul> |
   | **Code van plantype** | De plantypecode van het plantype. |
   | **Programma** | Geeft een programma aan waaraan u het plan desgewenst kunt toewijzen. |
   | **Bundel** | Geeft een bundel aan waaraan u het plan desgewenst kunt toewijzen. |
   | **Master** | Geeft aan of het plan het hoofdplan is binnen de bundel waaraan het is toegewezen. |
   | **Geldig vanaf datum en tijd** | De datum en het tijdstip waarop het plan start. De standaardwaarde is de huidige systeemdatum. |
   | **Geldig tot datum en tijd** | De datum en het tijdstip waarop het plan eindigt. De standaardwaarde is 12/31/2154, wat 'nooit' betekent. |

4. Geef op het tabblad **Configuratie** waarden op voor de volgende velden, afhankelijk van het type plan dat u gaat maken:

   | Plantype | Veld | Beschrijving |
   | --- | --- | --- |
   | Medical (Medical, Dental, Vision, HMO) | COBRA | Geeft aan of het plan in aanmerking komt voor COBRA (Consolidated Omnibus Budget Reconciliation Act). |
   | Medical (Medical, Dental, Vision, HMO) | HIPAA | Geeft aan of het plan in aanmerking komt voor HIPAA is (Health Insurance Portability and Accountability Act). |
   | Medical (Medical, Dental, Vision, HMO)<br><br>Overige (PTO, Fitness)<br><br>Overige<br><br>Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life)<br><br>Pensioenplan (bijvoorbeeld 401(k))<br><br>FSA | In aanmerking komende voorbelasting | Geeft aan of er bijdragen kunnen worden geleverd aan het plan voordat er belasting wordt toegepast. |
   | Medical (Medical, Dental, Vision, HMO)<br><br>Overige (PTO, Fitness)<br><br>Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life)<br><br>Pensioenplan (bijvoorbeeld 401(k))<br><br>FSA | In aanmerking komende belasting boeken | Geeft aan of er bijdragen kunnen worden geleverd aan het plan nadat er belasting is toegepast. |
   | Medical (Medical, Dental, Vision, HMO)<br><br>Overige (PTO, Fitness)<br><br>Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life)<br><br>Pensioenplan (bijvoorbeeld 401(k))<br><br>FSA | Inzender | Geeft aan wie bijdraagt aan het plan: de werknemer, de werkgever of beide. |
   | Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life) | Minimale dekking | Het minimumbedrag aan verzekeringsdekking dat nodig is voor het plan. |
   | Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life) | Maximale dekking | Het maximumbedrag aan verzekeringsdekking dat nodig is voor het plan. |
   | Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life) | Dekkingsverhogingen gebruiken | Geeft aan of moet worden gecontroleerd of het dekkingsbedrag overeenkomt met een geldig incrementeel bedrag. |
   | Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life) | Verhogingsbedrag | Het incrementele bedrag aan verzekeringsdekking dat nodig is voor het plan. Als het incrementele bedrag bijvoorbeeld 1.000 is, kan een werknemer geen verzekering van €200.500 hebben; het bedrag moet naar boven worden afgerond op €201.000 of naar beneden worden afgerond op €200.000. |
   | Langdurige arbeidsongeschiktheid<br><br>ADD (Basic life, Voluntary life) | Verhogingsrichting | Geeft de richting voor afronden aan, omhoog of omlaag, wanneer het dekkingsbedrag niet voldoet aan de waarde van het verhogingsbedrag. |
   | ADD (Basic life, Voluntary life) | Bewijs van verzekerbaarheid | Geeft aan of een werknemer bewijs moet leveren van de verzekerbaarheid. |
   | ADD (Basic life, Voluntary life) | Bedrag | Het bedrag in valuta voor de boekhouding. Dit veld is alleen actief als het selectievakje Bewijs van verzekerbaarheid is ingeschakeld. |
   | Pensioenplan (bijvoorbeeld 401(k))<br><br>FSA | Minimale jaarlijkse bijdrage | Het bedrag van de minimale bijdrage die nodig is voor het plan. |
   | Pensioenplan (bijvoorbeeld 401(k))<br><br>FSA | Maximale jaarlijkse bijdrage | Het bedrag van de maximale bijdrage die nodig is voor het plan. |
   | Pensioenplan (bijvoorbeeld 401(k)) | Maximum jaarlijks bedrag werkgever | Het maximale bedrag dat een werkgever mag bijdragen aan het pensioenplan van een werknemer tijdens een vergoedingsperiode. U moet het selectievakje Match werkgever inschakelen als u dit veld wilt gebruiken. |
   | Pensioenplan (bijvoorbeeld 401(k)) | Werkgeversmatch | Geeft aan of de werkgever bijdraagt aan het pensioenplan van de werknemer. |
   | Pensioenplan (bijvoorbeeld 401(k)) | Matchpercentage werkgever | Het percentage van een werknemersbijdrage dat de werkgever zal matchen. |
   | Pensioenplan (bijvoorbeeld 401(k)) | Limiet werkgeversmatch | Het maximale percentage dat de werkgever zal matchen. Als een werkgever bijvoorbeeld 100% van de werknemersbijdragen matcht tot maximaal 6% van het salaris van de werknemer, is de limiet voor de werkgeversmatch 6%. |

5. Geef op het tabblad **Instellingen** de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Inschrijving toestaan/voortzetten** | Geeft aan of werknemers zich voor het plan kunnen inschrijven als ze voldoen aan de vereisten om in aanmerking te komen.</br></br>Als deze optie is ingesteld op Nee, is het plan niet beschikbaar voor werknemers wanneer u de geschiktheid verwerkt. |
   | **Automatisch inschrijven vanaf voorafgaand jaar** | Geeft aan of een in aanmerking komende werknemer automatisch wordt ingeschreven in het plan bij inschrijving in het vorige jaar. |
   | **Standaard automatisch inschrijven** | Geeft aan of het plan standaard wordt geselecteerd voor inschrijving. Het plan is niet verplicht, zodat de werknemer de standaardselectie kan wijzigen. |
   | **Gesloten voor nieuwe inschrijvingen** | Geeft aan of het plan uitsluitend beschikbaar is voor in aanmerking komende werknemers die zich in het voorgaande jaar hebben ingeschreven. |
   | **Verplicht plan** | Geeft aan of werknemers automatisch voor het plan moeten worden ingeschreven. Werknemers kunnen de inschrijvingsselectie niet wijzigen. |
   | **Begindatum** | De datum waarop het plan is gemaakt in het bedrijf. |
   | **Leverancier** (leverancier vergoedingsplan) | De leverancier aan wie het bedrijf de premies betaalt voor het plan. |
   | **Naam** (leverancier vergoedingsplan) | De naam van de leverancier. |
   | **Leveranciersverwijzing** (leverancier vergoedingsplan) | De verwijzing van de leverancier voor het plan. Bijvoorbeeld het groepsplannummer van het bedrijf. |
   | **Alternatieve verwijzing** (leverancier vergoedingsplan) | De alternatieve verwijzing van de leverancier voor het plan. Bijvoorbeeld het rekeningnummer van het bedrijf. |
   | **Valuta** (leverancier vergoedingsplan) | De valuta die wordt gebruikt om premies aan de leverancier te betalen. |
   | **Onkostenrekening** (leverancier vergoedingsplan) | De grootboekrekening die wordt gebruikt als de onkostenrekening voor planpremies. |
   | **Leverancier** (beheerder vergoedingsplan) | De leverancier die door het bedrijf wordt betaald om het plan te beheren. Als het een zelf beheerd plan is, laat u dit veld leeg. |
   | **Naam** (beheerder vergoedingsplan) | De naam van de leverancier die de beheerder is van het vergoedingsplan. |
   | **Leveranciersverwijzing** (beheerder vergoedingsplan) | De verwijzing voor het plan van de leverancier die de beheerder is. |
   | **Alternatieve verwijzing** (beheerder vergoedingsplan) | De alternatieve verwijzing voor het plan van de leverancier die de beheerder is. |
   | **Valuta** (beheerder vergoedingsplan) | De valuta die wordt gebruikt om de beheerder van het vergoedingsplan te betalen. |
   | **Onkostenrekening** (beheerder vergoedingsplan) | De grootboekrekening die wordt gebruikt als de onkostenrekening voor de kosten die aan het beheer van het plan zijn gekoppeld. |

6. Filter de gegevens via het tabblad **Filters** indien nodig. U kunt filteren op de volgende velden:

   - **Bedrijfseenheid**
   - **Departement**
   - **Rechtspersoon**
   - **Locatie**
   - **Positie**

7. Geef op het tabblad **Geschiktheidsregels** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Regelnummer** | Het regelnummer van de geschiktheidsregel. |
   | **Geschiktheidsregel** | Een geschiktheidsregel die moet worden toegepast op het vergoedingsplan. Deze geschiktheidsregel wordt toegepast op het corresponderende actietype en gekoppeld aan de opgegeven wachttijd voor een dekking en inhoudingen. |
   | **Actietype** | De actie voor het toepassen van de geschiktheidsregel op de inschrijving voor, of de vervaldatum van, een vergoedingsplan. |
   | **Wachtperiode voor dekking** | Een waarde uit het formulier Wachttijden. De wachttijd voor de dekking bepaalt het aantal dagen of maanden dat een werknemer moet wachten voor deze aanspraak kan maken op de dekking van een vergoedingsplan of de vervaldatum van het vergoedingsplan op basis van de criteria in de geschiktheidsregel en het actietype. |
   | **Wachtperiode voor inhouding** | Een waarde uit het formulier Wachttijden. De wachttijd voor inhoudingen bepaalt het aantal dagen of maanden dat een werknemer moet wachten voor inhoudingen op het salaris beginnen voor het vergoedingsplan op basis van de criteria in de geschiktheidsregel en het actietype. |

8. Selecteer **Opslaan**.

## <a name="view-enrolled-workers"></a>Ingeschreven medewerkers weergeven

U kunt de medewerkers weergeven die zich hebben ingeschreven voor een geselecteerd vergoedingsplan.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer op het tabblad **Vergoedingen** in de navigatiebalk de optie **Geregistreerde medewerkers**.

## <a name="attach-coverage-options"></a>Dekkingsopties koppelen

U kunt dekkingsopties toevoegen aan het geselecteerde vergoedingsplan. Door het koppelen van dekkingsopties worden de instellingen voor tarief en inhoudingen voor een dekkingsoptie gecombineerd.  Voorbeeld: voor een medisch plan selecteert de gebruiker een optie voor gezinsdekking.  Vervolgens moet deze gebruiker het gezinstarief selecteren voor het gekoppelde plan (ingesteld bij tariefinstellingen) en de inhouding selecteren voor het gekoppelde plan (ingesteld bij tariefinstellingen). Dit levert de kosten op voor de werkgever en werknemer voor een geselecteerde dekking. Vervolgens herhaalt u het proces voor een werknemer+1-dekking of een werknemersdekking.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer op het tabblad **Vergoedingen** in de navigatiebalk de optie **Dekkingsopties koppelen**.

## <a name="override-eligibility-rules"></a>Geschiktheidsregels overschrijven

U kunt medewerkers aan een plan toevoegen als uitzonderingen op de geschiktheidsregels. Iedere medewerker die u toevoegt, komt in aanmerking voor het vergoedingsplan.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer op het tabblad **Vergoedingen** in de navigatiebalk de optie **Geschiktheidsregel overschrijven**.

## <a name="view-attached-periods"></a>Gekoppelde perioden weergeven

U kunt een lijst met de beschikbare vergoedingsperioden weergeven.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer het tabblad **Perioden** in de navigatiebalk.

## <a name="view-plan-description"></a>Omschrijving van plan weergeven

U kunt een omschrijving opgeven van het plan om werknemers te helpen bij het selecteren van hun vergoedingen. De planbeschrijving die u hier invoert, wordt weergegeven in Werknemerselfservice bij het aanwijzen van het plan in de lijst met dekkingsopties.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer op het tabblad **Vergoedingen** in de navigatiebalk de optie **Planbeschrijving**.

## <a name="view-flex-credit-programs"></a>Programma's voor flexibele kredieten weergeven

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Vergoedingsplannen**.

2. Selecteer op het tabblad **Vergoedingen** in de navigatiebalk de optie **Programma's voor flexibele kredieten**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]