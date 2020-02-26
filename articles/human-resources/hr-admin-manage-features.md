---
title: Functies beheren
description: Informatie over het in- of uitschakelen van nieuwe functies in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008589"
---
# <a name="manage-features"></a>Functies beheren

Als onderdeel van onze doorlopende implementatie van nieuwe mogelijkheden voor Microsoft Dynamics 365 Human Resources willen we klanten zo snel mogelijk laten kennismaken met nieuwe functies. We bieden previews-functies die bijna gereed zijn voor algemene beschikbaarheid en die uitgebreid zijn getest. Het enige wat we nog willen doen is een definitieve ronde van feedback van klanten en validatie voordat we de functies algemeen vrijgeven.

Ga voor meer informatie over nieuwe functies in Human Resources naar [Nieuw in Human Resources](hr-admin-whats-new.md) en [Releaseplan voor Dynamics 365 en Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Het werkgebied **Functiebeheer** bevat een lijst met functies die in elke versie worden geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven. Zie [Overzicht Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)voor meer informatie over Functiebeheer.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied **Functiebeheer** ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.

Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied **Functiebeheer** geeft aan wanneer een preview-functie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

## <a name="enable-or-disable-preview-features"></a>Preview-functies in- of uitschakelen

Als u toegang tot preview-functies wilt hebben, moet u deze eerst in uw omgeving inschakelen. Het in- of uitschakelen van voorbeeldfuncties is omgevingsspecifiek.

> [!IMPORTANT]
> Preview-functies zijn alleen beschikbaar in **Sandbox**-omgevingen. Als u een preview-functie inschakelt, schakelt u deze in voor alle gebruikers in uw organisatie die zich in die omgeving bevinden. Als u de preview-functie uitschakelt, wordt deze ontoegankelijk voor uw gebruikers. Preview-functies hebben beperkte ondersteuning in Human Resources. Ze gebruiken mogelijk minder privacy- en beveiligingsmaatregelen en zijn niet opgenomen in de serviceovereenkomst voor Human Resources. U moet de voorbeeldfuncties niet gebruiken voor de verwerking van persoonsgegevens (dat wil zeggen informatie die uw identiteit aangeeft) of andere gegevens die onderworpen zijn aan wettelijke of bestuursrechtelijke conformiteitsvereisten.

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Selecteer de tegel **Functiebeheer**.

3. Als u een preview-functie wilt inschakelen, selecteert u deze in de lijst en selecteert u **Inschakelen**. Als u een preview-functie wilt uitschakelen, selecteert u deze in de lijst en selecteert u **Uitschakelen**.

## <a name="preview-feature-benefits-management"></a>Preview-functie: Vergoedingenbeheer

Vergoedingenbeheer biedt een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt, samen met een gebruiksvriendelijke werknemerservaring waarmee uw aanbiedingen worden gepresenteerd. Zie het [overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie over de configuratie en het gebruik van Vergoedingenbeheer.

Vergoedingenbeheer vervangt functionaliteit in het werkgebied **Vergoedingen**. Wanneer u de preview-functie van Vergoedingenbeheer inschakelt, kunt u de volgende formulieren niet meer openen in het werkgebied **Vergoedingen**:

- **Vergoedingen**
- **Vergoedingselementen**
- **Tarieven bijdrageberekening**
- **Resultaten inschrijving op vergoedingen**
- **Resultaten van vergoedingen laten vervallen en verlengen**
- **Regeltypen van beleid om in aanmerking te komen voor een vergoeding**
- **Beleid inzake geschiktheid voor vergoedingen**
- **Geschiktheidsgebeurtenissen**

U kunt de informatie in deze formulieren in de alleen-lezenmodus weergeven. Als u de gegevens wilt bewerken, moet u eerst de preview-functie voor Vergoedingenbeheer uitschakelen.

### <a name="benefits-management-known-issues"></a>Bekende problemen met Vergoedingenbeheer

#### <a name="life-events"></a>Levensgebeurtenissen

Bij het verwerken van levensgebeurtenissen ontvangt de gebruiker een foutmelding:

De begindatum van de dekking moet liggen tussen *begin van planperiode* en *einde van planperiode*. 

De verwerking van de levensgebeurtenis blijft naar verwachting doorgaan.

#### <a name="eligibility-processing"></a>Geschiktheidscontroleproces

Bij het uitvoeren van een geschiktheidscontrole voor vergoedingen met een dekkingsbedrag van 1-5X het salaris, % van salaris en een vast bedrag, moet de datum voor de vergoedingsdetails worden ingesteld op de begindatum van de werknemer in **Historie dienstverband**, met gewerkte uren, betalingsfrequentie en jaarlijks salarisbedrag voor vergoedingen. Als er vaste compensatie voor de medewerker bestaat, voert u de gewerkte uren in samen met de betalingsfrequentie en wordt het jaarlijkse salarisbedrag berekend. Als de werknemer een vast salaris heeft, zijn de gewerkte uren niet nodig. Het is raadzaam eerst de vaste compensatie in te voeren wanneer u nieuwe medewerkers maakt. U werkt de record met de vergoedingsdetails als volgt bij: ga naar **Medewerker > Medewerkershistorie > Dienstverbandgegevens**. Pas datum aan en stel de begindatum van de medewerkers in.

#### <a name="employee-self-service"></a>Werknemerselfservice

Werknemers kunnen een plan selecteren waarvoor ze niet zijn gekwalificeerd en uitchecken. Bijvoorbeeld: een werknemer heeft geen gezinsleden, maar kan een medisch plan selecteren met gezinsdekking.

Het bedrag van de werknemer wordt niet berekend wanneer het dekkingsbedrag voor de levensverzekering wordt bijgewerkt. Als aan een werknemer bijvoorbeeld een levensverzekeringsplan wordt aangeboden, kan deze maximaal €50.000 aan dekking selecteren tegen een kostprijs van €0,36 per €1.000 aan dekking.  Wanneer de werknemer het dekkingsbedrag bijwerkt, blijven de gekoppelde kosten van de werknemer nul.

Voor een vergoedingsplan dat slechts één selectie van dat plantype toestaat, krijgt de gebruiker een foutmelding als deze een plan probeert af te wijzen na het selecteren van een plan. Een gebruiker selecteert bijvoorbeeld een medisch plan en plaatst dit in zijn of haar winkelwagen. De gebruiker selecteert vervolgens **Afwijzen** voor een ander medisch plan. De gebruiker krijgt een foutmelding.

## <a name="preview-features-in-leave-and-absence"></a>Preview-functies voor verlof en verzuim

Tot de preview-functies voor verlof en verzuim behoren:

- **Verlof- en verzuimkalender** - verlof- en verzuimparameters zijn verplaatst van **Parameters personeel** naar een nieuw scherm met de naam **Parameters verlof en verzuim**. Het nieuwe scherm bevat een nieuw tabblad **Kalender**. In deze preview wordt alleen een subset van de parameters ingeschakeld. U kunt het nieuwe scherm openen via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**. De kalenders omvatten:
  - **Bedrijfskalender**: hierin worden alle verlofaanvragen voor werknemers weergegeven. Personen met de **Human resources**-rol hebben toegang tot deze kalender via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**.
  - **Managerteamkalender** - hier worden alle verlofaanvragen van ondergeschikten weergegeven. Managers hebben toegang tot de kalender via het tabblad **Mijn team** in Werknemerselfservice onder **Verlof en verzuim**. 

- **Vakantiekalenders voor verlof en verzuim** - tot de typen verlof behoort de nieuwe optie **Vakantie** die in combinatie met de werktijdkalender wordt gebruikt. Dagen die worden gedefinieerd als feestdagen en sluitingsdagen, worden nu aangemerkt als **Vakantie** wanneer werkdagen worden gegenereerd. Wanneer de opbouw van verlofdagen wordt verwerkt, worden correcties aangebracht in werknemers die aan de kalender zijn toegewezen voor vakantiedagen die op een werkdag vallen.

- **Controle van verlofopbouw** - op een nieuw scherm kunt u controleren wanneer de verlofopbouw is verwerkt en verwijderd, zowel door alle werknemers als door individuele werknemers. U kunt dit nieuwe scherm openen via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**.

- **Verwijdering van verlofopbouw** - u kunt nu verlofopbouwrecords voor bepaalde verlofplannen verwijderen. U kunt toegang krijgen tot deze nieuwe optie via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**. Voor afzonderlijke werknemers wordt deze optie weergegeven in de groep **Verlof en verzuim** in het werknemersprofiel. 

- **Verlofopbouw afronden** - nieuwe opties voor **Verloftype** bepalen welk type afronding voor verlofopbouw moet worden gebruikt, plus de decimale nauwkeurigheid van de afronding tijdens het verlofopbouwproces. Wanneer de verlofopbouw wordt verwerkt, worden de afronding en de precisie toegepast op de verlofopbouwrecords. 

- **Meerdere verloftypen configureren voor één verlofplan** - met een nieuwe kolom in het verlofopbouwschema kunt u meerdere verloftypen voor een verlof- en verzuimplan met verschillende verlofopbouwschema's definiëren. Het vorige veld **Verloftype** is verwijderd. Bij de inschrijving van de werknemers worden de saldi voor de typen verlof nu weergegeven in een tabel in plaats van boven aan het scherm.

  > [!IMPORTANT]
  > U kunt deze functie niet uitschakelen nadat u deze hebt ingeschakeld.

- **De voltijdsequivalent (FTE) van een werknemer gebruiken voor verlofopbouw** : een nieuwe kolom in het verlofopbouwschema maakt het gebruik van de FTE voor de verlofopbouw mogelijk. Wanneer de verlofopbouw wordt verwerkt, gebruikt de toepassing de primaire positie van de werknemer en de ingestelde FTE om het van de evenredige bedrag van de verlofopbouw te bepalen.

  > [!NOTE]
  > Deze functie is alleen beschikbaar als u **Meerdere verloftypen per verlofplan configureren** inschakelt. 

## <a name="feedback"></a>Feedback

Wij horen graag over uw ervaringen met deze preview-functies. We raden u aan uw feedback regelmatig op de volgende websites te plaatsen wanneer u deze of andere functies gebruikt:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) : deze site is een goede bron waar gebruikers gebruikstoepassingen kunnen bespreken, vragen kunnen stellen en hulp van de community kunnen krijgen.
- Laat ons weten welke functies u wilt zien in het product en ook eventuele wijzigingen die volgens u in de bestaande functies moeten worden aangebracht. Ideeën voor producten op [Human Resources-ideeën](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Let op: vermeld geen persoonlijke gegevens (gegevens die uw identiteit vrijgeven) als u feedback of een productbeoordeling indient. Verzamelde gegevens worden mogelijk verder geanalyseerd en worden niet gebruikt om verzoeken te beantwoorden krachtens van toepassing zijnde privacywetgeving. Persoonlijke gegevens die afzonderlijk voor deze programma's worden verzameld, zijn onderworpen aan de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Zie ook

- [Nieuw in Human Resources](hr-admin-whats-new.md)
- [Releaseplan voor Dynamics 365 en Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)