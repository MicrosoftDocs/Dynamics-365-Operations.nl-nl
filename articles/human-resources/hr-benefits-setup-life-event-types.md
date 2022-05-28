---
title: Typen levensgebeurtenissen configureren
description: Microsoft Dynamics 365 Human Resources gebruikt typen levensgebeurtenissen om gebeurtenissen te definiëren voor het bijwerken van de inschrijving voor vergoedingen van werknemers.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64e536bad996e9a1948dad18437ec6f98ad27033
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691717"
---
# <a name="configure-life-event-types"></a>Typen levensgebeurtenissen configureren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In Dynamics 365 Human Resources worden **Typen levensgebeurtenissen** gebruikt om gebeurtenissen te definiëren waarbij de inschrijving voor vergoedingen van werknemers kan worden bijgewerkt, zoals trouwen of een kind krijgen. Elke id voor typen levensgebeurtenissen kan aan slechts één type levensgebeurtenis worden gekoppeld. Als u bijvoorbeeld een **Levensgebeurtenis-id** met de naam **Adreswijziging** maakt die is gekoppeld aan het levensgebeurtenistype **Adreswijziging werknemers**, kunt u geen andere id met het label **Adreswijziging werknemers** maken en koppelen aan het type levensgebeurtenis **Adreswijziging werknemers**. Als een type levensgebeurtenis niet aan een plantype is gekoppeld, wordt een levensgebeurtenis niet door het levensgebeurtenistype getriggerd. Zie [Plantypen maken](hr-benefits-setup-plan-types.md) voor meer informatie.

## <a name="create-a-life-event-type"></a>Een type levensgebeurtenis maken

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Typen levensgebeurtenissen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Type-id van levensgebeurtenis** | De unieke id voor het type levensgebeurtenis. |
   | **Beschrijving** | Een beschrijving van het type levensgebeurtenis. |
   | **Type levensgebeurtenis** | Een katalysator om de inschrijving van een werknemer voor vergoedingen bij te werken. Zie [Levensgebeurtenissen](hr-benefits-setup-payment-frequencies.md?life-events) hieronder voor een lijst met levensgebeurtenissen. |

4. Selecteer **Opslaan**.

## <a name="view-attached-plans"></a>Gekoppelde plannen weergeven

U kunt een lijst met plannen weergeven die aan het geselecteerde **Type levensgebeurtenis** zijn gekoppeld. Levensgebeurtenissen worden aan een plantype gekoppeld en plantypen worden aan een plan gekoppeld.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Typen levensgebeurtenissen**.

2. Selecteer **Acties**.

3. Selecteer **Gekoppelde plannen**.

## <a name="life-events"></a>Levensgebeurtenissen

U kunt kiezen uit de volgende levensgebeurtenissen wanneer u een type levensgebeurtenis maakt:

| Levensgebeurtenis | Locatie | Trigger |
| --- | --- | --- |
| **Wijziging burgerlijke staat** | **Medewerker > Profiel > Persoonlijke informatie > Burgerlijke staat**| Wijziging van burgerlijke staat |
| **Statuswijziging aanstelling** |**Medewerker > Dienstverband > Pagina historie dienstverband** | Voor een medewerken met een bestaand dienstverband wordt een levensgebeurtenis getriggerd door het maken van een nieuw dienstverbanddetail met een andere dienstverbandstatus.  Bijwerken van een bestaand dienstverbanddetail met een andere dienstverbandstatus triggert ook een levensgebeurtenis.  |
| **Adreswijziging werknemer** |**Medewerker > Profiel > Adressen**</li><li>**Medewerker > Persoonlijke informatie > Persoonlijke contactpersonen > Adres**</li></ul> | Adreswijziging. Adres moet **primair** zijn om een levensgebeurtenis te triggeren. |
| **Afhankelijke wijzigen** |<br><ul><li>**Medewerker > Profiel > Persoonlijke gegevens > Persoonlijke contactpersonen**</li><li>**Werknemerselfservice**</li></ul> | Een persoonlijke contactpersoon toevoegen en deze opgeven als afhankelijke en **Geldig vanaf** definiëren. De informatie voor **Geldig tot** van afhankelijke van een contactpersoon bijwerken. De relatie van de persoonlijke contactpersoon moet kind, echtgenoot/echtgenote, samenlevingspartner of ex-echtgenoot/ex-echtgenote zijn.  |
| **Geboorte of adoptie (gezinslid)** |<br><ul><li>**Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen**</li><li>**Selfservice werknemer > Persoonlijke gegevens bewerken > Persoonlijke contactpersonen**</li></ul>| **Geboortedatum** of **Adoptiedatum** worden toegevoegd of bijgewerkt. De **geboortedatum** van het kind is vereist. |
| **Dekkingsverlies (echtgeno(o)t(e)/samenlevingspartner)** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Dekkingsverlies | **Dekkingsverlies** geselecteerd voor een persoonlijke contactpersoon, inclusief **Ingangsdatum** |
| Wijziging van aanstelling voor samenlevingspartner | **Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Aangesteld** | Een persoonlijke contactpersoon maken en **Aangesteld** instellen op **Ja**. Een persoonlijke contactpersoon bijwerken en **Aangesteld** wijzigen.  |
| **Verlof (echtgeno(o)t(e)/samenlevingspartner)** | **Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Verlof** | Een persoonlijke contactpersoon wordt gemaakt en **Ingangsdatum voor verlof** is gedefinieerd. **Verlof** voor de persoonlijke contactpersoon wordt bijgewerkt. **Ingangsdatum voor verlof** voor de persoonlijke contactpersoon wordt bijgewerkt.  |
| **Wijziging in dekking (positie)** |<br><ul><li>**Medewerker > Positietoewijzing > Positietoewijzingen medewerker**</li><li>**Posities > Posities**</li></ul>| Wijziging in de positie in de toewijzingsrecords voor de positie van de medewerker. Wijziging van de toewijzing van de medewerker in de positie. |
| **Wijziging in dekking (salaris)** |<br><ul><li>**Medewerker > Compensatie > Vast plan**</li><li>**Medewerker > Persoonlijke gegevens > Vergoedingen jaarsalaris**</li></ul>| Als **Vergoedingenbeheer > Gedeelde Human Resources-parameters > Vergoedingen > Jaarlijks salarisbedrag voor vergoedingen** niet is ingeschakeld, wordt er een levensgebeurtenis gemaakt als **Medewerker > Compensatie > Vast plan** wordt bijgewerkt. Als **Vergoedingenbeheer > Gedeelde Human Resources-parameters > Vergoedingen > Jaarlijks salarisbedrag voor vergoedingen** is ingeschakeld, wordt er een levensgebeurtenis gemaakt als **Medewerker > Persoonlijke gegevens > Jaarlijks salarisbedrag voor vergoedingen** wordt bijgewerkt. |
| **Medicare (werknemer/gezinslid)** | **Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Ingangsdatum Medicare** | Door **Ingangsdatum Medicare** toe te voegen of bij te werken voor een persoonlijke contactpersoon, wordt deze levensgebeurtenis gemaakt. |
| **Rechterlijk bevel tot ondersteuning** | **Medewerker > Profiel > Persoonlijke gegevens > Persoonlijke contactpersonen > Gezinslid > Rechterlijk bevel tot ondersteuning** (QMSCO/QDRO) en ingangsdatums | Wanneer u een persoonlijke contactpersoon maakt, wordt een levensgebeurtenis gemaakt als **Rechterlijk bevel tot ondersteuning** is ingesteld op **Ja**. Als **Rechterlijk bevel tot ondersteuning** of **Vervaldatum rechterlijk bevel** wordt bijgewerkt, wordt ook een levensgebeurtenis getriggerd. |
| **Overleden** | **Medewerker > Profiel > Persoonlijke informatie > Datum van overlijden** | Een **overlijdensdatum** wordt ingevoerd of bijgewerkt. |
| **Verzekeringsbewijs** | **Medewerker > Medewerker > Versies > Historie dienstverband > Datumbeheer > Vergoedingsdetails** | **Bewijs van verzekerbaarheid** wordt ingesteld op **Ja**. **Verificatiedatum van bewijs van verzekerbaarheid** wordt gedefinieerd. |
| **Begunstigde** | **Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen** | Er wordt een persoonlijke contactpersoon toegevoegd en de velden **Begunstigde** en **Ingangsdatum** worden ingevuld. De persoonlijke contactpersoon moet van het type **Kind**, **Echtgenoot/echtgenote**, **Samenlevingspartner**, **Bloedverwant**, **Contactpersoon in familie**, **Andere contactpersoon** of **Ouder** zijn. |
| **Medicare werknemer** | **Medewerker > Medewerker > Versies > Historie dienstverband > Datumbeheer > Vergoedingsdetails** | **Geschikt voor Medicare** is ingesteld op **Ja**. **Datum Geschikt voor Medicare** wordt gewijzigd. |
| **Verjaardag** | **Vergoedingenbeheer > Verwerking van wijziging van levensgebeurtenis** | Deze levensgebeurtenissen worden gemaakt op basis van **Verwerking van wijziging van levensgebeurtenis**. Het proces analyseert de gekozen periode en rechtspersoon en zoekt gekoppelde medewerkers. Het berekent hun laatste verjaardag en maakt een levensgebeurtenis voor de verjaardag als deze nog niet is gemaakt. |
| **Geschiktheidswijziging van medewerker (niet specifiek VS)** |<br><ul><li>**Medewerker > Aanstelling**</li><li>**Medewerker > Medewerker >Versies > Historie dienstverband**</li></ul>| Maakt een levensgebeurtenis in de volgende situaties:<br><ul><li>Een nieuw dienstverband maken, er is een eerder dienstverband en het werknemertype wijzigt.</li><li>Een nieuw dienstverbanddetail maken, er is een eerder dienstverbanddetail en het dienstverbandtype of de dienstverbandcategorie wijzigt.</li><li>Een dienstverbandrecord wordt bijgewerkt en een ander medewerkertype wordt gedefinieerd.</li><li>Een dienstverbanddetailrecord wordt bijgewerkt en een ander dienstverbandtype of een andere dienstverbandcategorie wordt opgegeven.</li></ul> |
| **Nieuwe geschiktheid negeren (niet specifiek VS)** | **Human resources - geavanceerd > Vergoedingen > Plannen > Vergoedingen > Geschiktheidsregel negeren** | Verwerking van levensgebeurtenissen gebruiken<br>Het maken van een overschrijving voor geschiktheid voor een vergoedingenplan voor een medewerker triggert deze levensgebeurtenis.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Wijziging bij negeren van geschiktheidsregel (niet specifiek VS)** | **Human resources - geavanceerd > Vergoedingen > Plannen > Vergoedingen > Geschiktheidsregel negeren** | Het bijwerken van **Geldig vanaf** of **Geldig tot** in de geschiktheid voor een vergoedingenplan triggert deze levensgebeurtenis. |
| **Negeren van geschiktheidsregel verlopen (niet specifiek VS)** | Vergoedingenbeheer > Verwerking van wijziging van levensgebeurtenis  | Deze levensgebeurtenissen worden gemaakt op basis van **Verwerking van wijziging van levensgebeurtenis**. Het proces analyseert de gekozen periode en rechtspersoon en zoekt gekoppelde overschrijvingen voor geschiktheid voor het vergoedingenplan. Er worden levensgebeurtenissen gemaakt als de overschrijvingen zijn verlopen. |
| **Nieuw vergoedingsplan (niet specifiek VS)** | **Human resources -geavanceerd > Vergoedingen > Plannen > Nieuw** | Geschiktheidsopties worden toegevoegd aan een actueel plan. Een nieuw plan met hieraan gekoppelde opties voor geschiktheid wordt toegevoegd.</br></br>HR-personeel moet in dit geval de geschiktheidsverwerking voor de levensgebeurtenis uitvoeren. |
| **Wijziging geschiktheidsregel (niet specifiek VS)** | **Vergoedingenbeheer > Geschiktheidsregels** | Bij verwerking van geschiktheid van levensgebeurtenissen. Dit wordt geregistreerd als in **BenefitEligibilityRule**-records de volgende waarden worden gewijzigd: **UseEmplCategory**, **UseEmplStatus** of **UseEmplType**. Er worden alleen levensgebeurtenistransacties bijgewerkt die al bestaan voor een gewijzigde regel of geschiktheidscriterium. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
