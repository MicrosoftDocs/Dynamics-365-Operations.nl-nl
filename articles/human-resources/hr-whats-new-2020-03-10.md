---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (10 maart 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources voor 10 maart 2020.
author: andreabichsel
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6e4d93f89721bd722de523fbba7adfd2ee3f786
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061146"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (10 maart 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.2985. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in LCS ter referentie.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Kan geen toegang krijgen tot hiaatanalyserapport (394460)

Dit rapport wordt niet ondersteund in Dynamics 365 Human Resources. De menuopdracht voor het afdrukken van het SSRS-rapport wordt verwijderd.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Onjuist bericht bij toegang tot de pagina aan de slag (417950)

Bij deze wijziging wordt deze menuoptie vanwege de beveiliging verborgen als u geen toegang hebt tot het formulier.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Gestroomlijnd taakonderhoud voor werknemers (380538)

Het formulier Taakonderhoud werknemer geeft een overzicht van alle taken voor een werknemer voor onboarding, offboarding, overplaatsingen en bedrijfsprocessen. U kunt de status van de taken verwijderen, opnieuw toewijzen of bijwerken.

Voorbeeld: Benjamin Martin is een vergoedingenbeheerder. Tijdens het onboarden van werknemers worden er taken voor Benjamin gemaakt om de vergoedingenselectie van de nieuwe werknemer te controleren. Benjamin heeft taken in het verleden die hij voltooid heeft en toekomstige taken die hij moet voltooien. Benjamin besluit het bedrijf te verlaten, zodat zijn taken opnieuw moeten worden toegewezen of moeten worden verwijderd. In het formulier Taakonderhoud (in het actievenster van het formulier **Werknemer**) kunnen alle taken van Benjamin opnieuw aan een andere werknemer worden toegewezen of worden verwijderd.  

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse-oplossing is nu beschikbaar met de volgende wijzigingen:

| Omschrijving | Wisselgeld |
| --- | --- |
| Wijzigingen in de entiteit **Functie/positie** | <ul><li>**Compensatieregio** toegevoegd</li>|
| Entiteit **Dimensie van taakpositie** toegevoegd | <ul><li>**Financiële dimensies** toegevoegd</li>
| Wijzigingen in entiteit **Medewerker** | <ul><li>**Naamsvolgorde** toegevoegd</li><li>**Werkt thuis** toegevoegd</li><li>**Taal** toegevoegd</li><li>**Anciënniteitsdatum** toegevoegd</li><li>**Jubileumdatum** toegevoegd</li><li>**Oorspronkelijke datum indiensttreding** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Aanstelling** | <ul><li>**Financiële dimensies** toegevoegd</li><li>**Reden van ontslag** toegevoegd</li><li>**Ontslagdatum** gewijzigd van **Overgangsdatum**</li><li>**Proeftijddatum** toegevoegd</li></ul> |
| Wijzigingen in entiteit **Adres medewerker** | <ul><li>**Adres** toegevoegd</li><li>**Adresregel 1**, **Adresregel 2** en **Adresregel 3** gemarkeerd voor afschaffing</li></ul> |
| Entiteiten voor nieuwe instellingen voor variabele compensatie | <ul><li>**Type variabelecompensatieplan**</li><li>**Variabelecompensatieplan**</li><li>**Vestigingsregels**</li><li>**Niveau variabelecompensatieplan**</li></ul> |
| Nieuwe entiteit **Medewerkerkalender aanstelling** | <ul><li>Entiteit **Werkkalender** toegevoegd</li></ul> |
| Nieuwe entiteit **Salarispositiedetail** | <ul><li>**Salarispositiedetail** toegevoegd</li></ul> |
| Nieuwe entiteit **Titel** | <ul><li>**Titel** toegevoegd</li></ul> De nieuwe entiteit **Titel** wordt opgenomen in Dataverse maar er wordt nu niet naar verwezen in de entiteiten **Taakpositie** of **Functie**. |

> [!NOTE]
> Financiële dimensies voor zowel posities als aanstellingen zorgen voor integratie in één richting voor updates van Human Resources naar Dataverse. Voor updates van financiële dimensies wordt Dataverse momenteel niet gesynchroniseerd met Human Resources.

In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen. Handmatig de meest recente Dataverse-oplossing voor Human Resources installeren:

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2.  Selecteer **Omgevingen**.

3.  Zoek de omgeving die u wilt bijwerken. De omgeving moet overeenkomen met **Omgevingsnaam**  in de sectie **Dataverse-gegevens** in het formulier **Info** in Human Resources.

4.  Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.

5.  Selecteer **Oplossingen beheren** op de actiebalk bovenaan. Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.

6.  Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.

7.  Selecteer **Upgraden** om de meest recente oplossing toe te passen.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar op 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="platform-update-33"></a>Platformupdate 33

- Apps op volledige pagina (preview): met deze preview-functie, waarmee u de opgeslagen weergaven kunt inschakelen, kunnen Power Apps en apps van derden worden toegevoegd en weergegeven op de volledige pagina via het dashboard.

- Opgeslagen weergaven (preview): met deze preview-functie worden opgeslagen weergaven ingeschakeld. Dit is een belangrijke verbetering van het subsysteem voor persoonlijke instellingen. Met deze functie kunnen gebruikers meerdere benoemde sets persoonlijke instellingen per pagina hebben. U kunt ook weergaven publiceren naar beveiligingsrollen.

- De filterfunctie "is één van" is geoptimaliseerd: met de verbeterde filterfunctie "is één van" wordt het invoeren van meerdere filterwaarden eenvoudiger, kunt u sneller afzonderlijke of alle filterwaarden verwijderen en wordt een compacte en intuïtieve visualisatie van filterwaarden mogelijk.

- Aanbevolen velden: gebruikers moeten vaak velden toevoegen aan een raster of pagina. Dit kan moeilijk zijn met zoveel beschikbare velden. In plaats van een grote lijst te hoeven doorzoeken, kan met deze functie het systeem een reeks aanbevolen velden weergeven op basis van wat andere gebruikers meestal in vergelijkbare scenario's toevoegen.

- Standaardplakacties in rasters: deze functie zorgt ervoor dat de standaardactie in een raster wordt gekoppeld aan een specifieke kolom in een raster, ongeacht of die kolom wordt verplaatst of verborgen.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]