---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (19 maart 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f636dbd3b0ba59ea6cafbc431af46315210dded1
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555244"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (19 maart 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3014. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>De limieten van Human Resources-omgevingen zijn nu gebaseerd op bijgewerkte licentie (394595)

De limiet aan het aantal omgevingen per project in Lifecycle Services (LCS) is gewijzigd. De vorige limiet was twee omgevingen. De limiet aan het aantal productie- en sandbox-omgevingen dat u kunt maken voor Human Resources in LCS is nu gebaseerd op bijgewerkte licenties. U kunt nu zoveel omgevingen maken als u nodig hebt per LCS-project, afhankelijk van het aantal aangeschafte licenties. Met de nieuwe licentie, die op 1 februari 2020 is bijgewerkt, kunnen klanten aanvullende omgevingen kopen. Zie de [licentiehandleiding voor Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources) voor meer informatie over licentievereisten voor aanvullende omgevingen.

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Weergaven van compensatiegegevens voor werknemers en managers tussen bedrijven bieden (403904)

Schakel deze in het werkgebied **Functiebeheer** in. Meer informatie over previewfuncties vindt u in [Preview-functies in- of uitschakelen](hr-admin-manage-features.md#enable-or-disable-preview-features).

Wanneer u deze functie inschakelt, kunnen managers de compensatie van directe en indirecte ondergeschikten zien zonder zich te hoeven aanmelden bij het betreffende bedrijf. De volledige compensatiehistorie is beschikbaar van alle geregistreerde bedrijven waartoe de manager toegang heeft. Zie voor meer informatie [Overzicht van Selfservice werknemer en Selfservice manager](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Functionaliteit voor het samenvoegen van het globale adresboek inschakelen (427189)

U kunt nu dubbele adresboekvermeldingen samenvoegen door de dubbele records te selecteren en **Samenvoegen** te kiezen op de pagina **Globaal adresboek**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Kan het verlofsaldo niet aanpassen voor een plan zonder transitorische posten dat is gemaakt met de ingeschakelde functie voor meerdere verloftypen (419635)

U kunt nu saldi aanpassen voor verlofplannen die zijn gemaakt met de preview-functie **Meerdere verloftypen** ingeschakeld in Functiebeheer.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Het veld Primaire positie in WorkerPositionAssignmentEntity wanneer het dienstverband van een werknemer wordt beëindigd (420774)

Voor werknemers waarvoor het dienstverband wordt beëindigd, wordt in de entiteit de primaire positie weergegeven die actief was op het moment van beëindiging. Voor integraties wordt geen dubbele record meer gemaakt voor de werknemerspositietoewijzing van de werknemer. 

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-oplossing is nu beschikbaar met de volgende wijzigingen:

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
| Nieuwe entiteit **Titel** | <ul><li>**Titel** toegevoegd</li></ul>De nieuwe entiteit **Titel** wordt opgenomen in Common Data Service maar er wordt nu niet naar verwezen in de entiteiten **Taakpositie** of **Functie**. |

> [!NOTE]
> Financiële dimensies voor zowel posities als aanstellingen zorgen voor integratie in één richting voor updates van Human Resources naar Common Data Service. Voor updates van financiële dimensies wordt Common Data Service momenteel niet gesynchroniseerd met Human Resources.

In de komende weken zijn deze entiteitswijzigingen beschikbaar in alle omgevingen. Handmatig de meest recente Common Data Service-oplossing voor Human Resources installeren:

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2.  Selecteer **Omgevingen**.

3.  Zoek de omgeving die u wilt bijwerken. De omgeving moet overeenkomen met **Omgevingsnaam**  in de sectie **Common Data Service-gegevens** in het formulier **Info** in Human Resources.

4.  Selecteer de omgeving waarin u de omgevingsdetails wilt weergeven.

5.  Selecteer **Oplossingen beheren** op de actiebalk bovenaan. Er wordt een nieuw browservenster geopend waarin u naar **Dynamics 365-beheercentrum** gaat in de context van uw omgeving.

6.  Selecteer in de lijst **Oplossing** **Dynamics 365 Human Resources verankeren**.

7.  Selecteer **Upgraden** om de meest recente oplossing toe te passen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-voorbeeld werkt niet in sommige omgevingen

Als het documentvoorbeeld voor documenten opgeslagen in SharePoint niet werkt, voert u de volgende procedure uit:

1. Controleer voor de gebruikersaccount Beheerder of er een e-mailadres is gekoppeld aan de gebruikersrecord. Deze gegevens worden weergegeven op de pagina **Gebruiker**. Als er geen e-mailadres is ingesteld, moet u het e-mailadres en de provider toevoegen met de Excel-invoegtoepassing OData. Standaard is het e-mailadres niet aanwezig in het Excel-ontwerp. U moet het Excel-ontwerp bewerken, alle velden toevoegen, toepassen en vernieuwen. Wanneer u deze stappen hebt voltooid, kunt u de beheerdersaccount bijwerken.

2. Nadat aan de beheerdersaccount een e-mailaccount is gekoppeld, meldt u zich aan bij Human Resources met beheerdersreferenties.

3. Open een bijlage in SharePoint om de voorbeeldweergave van documenten te starten.

4. Meld u aan met een andere gebruikersaccount die toegang heeft tot bijlagen en controleer of het voorbeeld werkt zoals verwacht.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="platform-update-33"></a>Platformupdate 33

- Apps op volledige pagina (preview): met deze preview-functie, waarmee u de opgeslagen weergaven kunt inschakelen, kunnen Power Apps en apps van derden worden toegevoegd en weergegeven op de volledige pagina via het dashboard.

- Opgeslagen weergaven (preview): met deze preview-functie worden opgeslagen weergaven ingeschakeld. Dit is een belangrijke verbetering van het subsysteem voor persoonlijke instellingen. Met deze functie kunnen gebruikers meerdere benoemde sets persoonlijke instellingen per pagina hebben. U kunt ook weergaven publiceren naar beveiligingsrollen.

- De filterfunctie "is één van" is geoptimaliseerd: met de verbeterde filterfunctie "is één van" wordt het invoeren van meerdere filterwaarden eenvoudiger, kunt u sneller afzonderlijke of alle filterwaarden verwijderen en wordt een compacte en intuïtieve visualisatie van filterwaarden mogelijk.

- Aanbevolen velden: gebruikers moeten vaak velden toevoegen aan een raster of pagina. Dit kan moeilijk zijn met zoveel beschikbare velden. In plaats van een grote lijst te hoeven doorzoeken, kan met deze functie het systeem een reeks aanbevolen velden weergeven op basis van wat andere gebruikers meestal in vergelijkbare scenario's toevoegen.

- Standaardplakacties in rasters: deze functie zorgt ervoor dat de standaardactie in een raster wordt gekoppeld aan een specifieke kolom in een raster, ongeacht of die kolom wordt verplaatst of verborgen.

## <a name="new-production-release-cadence"></a>Nieuwe tempo voor productiereleases

Vanaf april wordt het releasetempo voor Human Resources van wekelijks in tweewekelijks gewijzigd. Dit garandeert de afstemming met veilige implementatieprocedures en hoge servicestandaarden voor stabiliteit en betrouwbaarheid. Er worden extra tests en controles uitgevoerd om de implementatie in elke fase van het proces te controleren. Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het releasetempo.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar op 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

## <a name="see-also"></a>Zie ook

[Nieuwe of gewijzigde functies in Human Resources](hr-admin-whats-new.md)</br>
[Overzicht van releasewave 2 van Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Het updateproces](hr-admin-setup-update-process.md)</br>
[Functies beheren](hr-admin-manage-features.md)