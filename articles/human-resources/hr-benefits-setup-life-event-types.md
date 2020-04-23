---
title: Typen levensgebeurtenissen configureren
description: Microsoft Dynamics 365 Human Resources gebruikt typen levensgebeurtenissen om gebeurtenissen te definiëren waarbij de inschrijving voor vergoedingen van werknemers kan worden bijgewerkt.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 404979c210993857e35485020d090814b45cc800
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229850"
---
# <a name="configure-life-event-types"></a>Typen levensgebeurtenissen configureren

Microsoft Dynamics 365 Human Resources gebruikt typen levensgebeurtenissen om gebeurtenissen te definiëren waarbij de inschrijving voor vergoedingen van werknemers kan worden bijgewerkt. Bijvoorbeeld trouwen of een kind krijgen. Elke id voor typen levensgebeurtenissen kan aan slechts één type levensgebeurtenis worden gekoppeld. Als u bijvoorbeeld een levensgebeurtenis-id met de naam Adreswijziging hebt gemaakt die is gekoppeld aan het gebeurtenistype Adreswijziging werknemers, kunt u geen andere id maken met Adreswijziging werknemers als type levensgebeurtenis voor werknemers. 

Nadat u typen levensgebeurtenissen hebt gemaakt, moet u deze aan plantypen koppelen. Zie [Plantypen maken](hr-benefits-setup-plan-types.md) voor meer informatie.

   > [!NOTE]
   > Als u een levensgebeurtenis maakt, moet u deze kppelen aan een plantype. Zie [Plantypen maken](hr-benefits-setup-life-event-types.md) voor meer informatie.

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

U kunt een lijst met plannen weergeven die aan het geselecteerde type levensgebeurtenis zijn gekoppeld. Levensgebeurtenissen worden aan een plantype gekoppeld en plantypen worden aan een plan gekoppeld. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Typen levensgebeurtenissen**.

2. Selecteer **Acties**.

3. Selecteer **Gekoppelde plannen**.

## <a name="life-events"></a>Levensgebeurtenissen

U kunt kiezen uit de volgende levensgebeurtenissen wanneer u een type levensgebeurtenis maakt:

| Levensgebeurtenis | Locatie | Trigger |
| --- | --- | --- |
| **Wijziging burgerlijke staat** | Medewerker > Profiel > Persoonlijke informatie > Burgerlijke staat| Wijziging van burgerlijke staat |
| **Statuswijziging aanstelling** | <ul><li>Medewerker > Aanstelling</li><li>Pagina Historie dienstverband</li></ul> | Wijziging van aanstellingsstatus |
| **Adreswijziging werknemer** | <ul><li>Medewerker > Profiel > Adressen </li><li>Medewerker > Persoonlijke informatie > Persoonlijke contactpersonen > Adres</li></ul> Toegevoegd, bewerkt of verwijderd adres |
| **Afhankelijke wijzigen** | <ul><li>Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Een gezinslid toevoegen of verwijderen</li><li>Werknemerselfservice</li></ul> | Toegevoegd of verwijderd gezinslid. De relatie van de persoonlijke contactpersoon moet kind, echtgenoot/echtgenote, samenlevingspartner of ex-echtgenoot/ex-echtgenote zijn. Als de datum voor **Geldig vanaf** wordt bijgewerkt, wordt de levensgebeurtenis geactiveerd. Als u deze datum niet bijwerkt, wordt er geen levensgebeurtenis geactiveerd. |
| **Geboorte of adoptie (gezinslid)** | <ul><li>Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid</li><li>Werknemerselfservice</li></ul> | Veld **Adoptiedatum** ingevuld. De geboortedatum van het kind is vereist. |
| **Dekkingsverlies (echtgeno(o)t(e)/samenlevingspartner)** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Dekkingsverlies | **Dekkingsverlies** geselecteerd voor een persoonlijke contactpersoon, inclusief **Ingangsdatum** |
| Wijziging van aanstelling voor samenlevingspartner | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Aangesteld. | <ul><li>Record met details van gezinslid gemaakt en vak **Persoonlijke contactpersoon aangesteld** = Ja</li><li>Vak **Persoonlijke contactpersoon aangesteld** gewijzigd (Ja of Nee)</li></ul> |
| **Verlof (echtgeno(o)t(e)/samenlevingspartner)** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Verlof | <ul><li>Record met details van gezinslid gemaakt en **EhrLOAEffectiveDate** ingevuld</li><li>**personPrivateDetails.EhrIsLOA** wordt gewijzigd (Ja of Nee)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** wordt gewijzigd</li></ul> |
| **Wijziging in dekking (positie)** | <ul><li>Medewerker > Positietoewijzing > Positietoewijzingen medewerker</li><li>Posities > Posities</li></ul> | <ul><li>Wijzigen in de positie in de toewijzingsrecords voor de positie van de medewerker</li><li>Wijziging van de toewijzing van de medewerker in de positie</li></ul> |
| **Medicare (werknemer/gezinslid)** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Ingangsdatum Medicare | Wordt niet automatisch geactiveerd wanneer een persoonlijke contactpersoon een ingangsdatum invoert. |
| **Rechterlijk bevel tot ondersteuning** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Gezinslid > Rechterlijk bevel tot ondersteuning (QMSCO/QDRO) en ingangsdatums | Activeert geen automatische updates. Het heeft geen effect op de geschiktheid. Er wordt een levensgebeurtenis geregistreerd. |
| **Overleden** | Medewerker > Profiel > Persoonlijke informatie > Datum van overlijden | Er wordt een overlijdensdatum ingevoerd |
| **Verzekeringsbewijs** | <ul><li>Medewerker > Medewerker > Versies > Historie dienstverband > Datumbeheer > Vergoedingsdetails</li><li> Medewerker > Aanstelling > Vergoedingsdetails > Verificatiedatum</li></ul> | <ul><li>Een medewerker voert een verificatiedatum in</li><li>Een medewerker stelt het veld EvidenceOfInsurability in op **Ja**</li></ul> |
| **Begunstigde** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen | Er wordt een persoonlijke contactpersoon toegevoegd en het vak **Begunstigde** en **Ingangsdatum** worden ingevuld. De persoonlijke contactpersoon moet van het type **Kind**, **Echtgenoot/echtgenote**, **Samenlevingspartner**, **Bloedverwant**, **Contactpersoon in familie**, **Andere contactpersoon**, **Ouder**, **Bezit begunstigde**, **Organisatie van begunstigde** of **Vertrouwde positie van begunstigde** zijn. |
| **Medicare werknemer** | Medewerker > Medewerker > Versies > Historie dienstverband > Datumbeheer > Vergoedingsdetails | <ul><li>**EhrMedicareEligibilityDate** wordt gewijzigd</li><li>**MedicareEligibile** is ingesteld op **Ja**</li></ul> |
| **Verjaardag** | Medewerker > Profiel > Persoonlijke informatie > Persoonlijke contactpersonen > Details gezinslid > Geboortedatum | Er wordt een geboortedatum toegevoegd of bijgewerkt (niet na de verwerking van de wijziging van de levensgebeurtenis). Voorbeeld: als **geschiktheidsopties voor persoonlijke contactpersonen** voor een kind zijn ingesteld op Leeftijd: 26 in Instellen > Vergoedingen > Geschiktheidsopties voor persoonlijke contactpersonen en HR-personeel de wijzigingsverwerking voor levensgebeurtenis uitvoert op een willekeurige dag nadat het gezinslid 26 is geworden, wordt er een bericht weergegeven dat het gezinslid niet meer in aanmerking komt voor dekking. |
| **Geschiktheidswijziging van medewerker (niet specifiek VS)** | <ul><li>Medewerker > Aanstelling</li><li>Medewerker > Medewerker >Versies > Historie dienstverband</li></ul> | <ul><li>Werknemertype, Aanstellingscategorie of de vijf door de gebruiker te definiëren geschiktheidsvelden worden gewijzigd</li><li>**HcmEmploymentDetail.EhrEmploymentType** wordt gewijzigd (alleen verwerkt voor *gewijzigde* aanstellingsdetailrecords, niet verwerkt voor *nieuwe* aanstellingsrecords, zoals bij opnieuw aanstellen en ontslag)</li></ul> |
| **Nieuwe geschiktheid negeren (niet specifiek VS)** | Human resources - geavanceerd > Vergoedingen > Plannen > Vergoedingen > Geschiktheidsregel negeren | Verwerking van levensgebeurtenissen gebruiken | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Wijziging bij negeren van geschiktheidsregel (niet specifiek VS)** | Human resources - geavanceerd > Vergoedingen > Plannen > Vergoedingen > Geschiktheidsregel negeren | Verwerking van levensgebeurtenis gebruiken (hiermee worden alleen wijzigingen in velden **ValidFrom** en **ValidTo** verwerkt bij het negeren van de geschiktheidsregel) |
| **Negeren van geschiktheidsregel verlopen (niet specifiek VS)** | Human resources - geavanceerd > Vergoedingen > Plannen > Vergoedingen > Geschiktheidsregel negeren | Bij verwerking van wijziging van levensgebeurtenissen. Als u bijvoorbeeld de vervaldatum voor het negeren van een geschiktheidsregel voor een plan wijzigt in vandaag 17:00 uur, wordt op enig moment na 17:00 uur of in de komende dagen na uitvoering van de verwerking van wijzigingen levensgebeurtenissen een bericht weergegeven dat het negeren van de geschiktheidsregel is verlopen. |
| **Nieuw vergoedingsplan (niet specifiek VS)** | Human resources -geavanceerd > Vergoedingen > Plannen > Nieuw | <ul><li>Geschiktheidsopties worden toegevoegd aan een huidig plan</li><li>Er wordt een nieuw plan met hieraan gekoppelde opties toegevoegd</li></ul></br></br>HR-personeel moet in dit geval de geschiktheidsverwerking voor de levensgebeurtenis uitvoeren. |
| **Wijziging geschiktheidsregel (niet specifiek VS)** | Human resources - geavanceerd > Vergoedingen > Regels/opties > Geschiktheidsregels | Bij verwerking van geschiktheid van levensgebeurtenissen. Dit wordt geregistreerd als in **EhrBenefitEligibilityRule**-records de volgende waarden worden gewijzigd: **UseEmplCategory**, **UseEmplStatus** of **UseEmplType**. Er worden alleen levensgebeurtenistransacties bijgewerkt die al bestaan voor een gewijzigde regel of geschiktheidscriterium. |
