---
title: Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (24 maart 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
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
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83f24dd6f094715f96666c3ae94faa4bdb97a652
ms.sourcegitcommit: fac1d519a85eab0c936b54e0a9247f6a11842871
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2020
ms.locfileid: "3177932"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Human Resources (24 maart 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Human Resources nieuw of gewijzigd zijn. Wijzigingen die van toepassing zijn op buildnummer 8.1.3073. De getallen tussen haakjes in sommige koppen verwijzen ter referentie naar ondersteuningsnummers in Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>De limieten van Human Resources-omgevingen zijn nu gebaseerd op bijgewerkte licentie (394595)

De limiet aan het aantal omgevingen per project in Lifecycle Services (LCS) is gewijzigd. De vorige limiet was twee omgevingen. De limiet aan het aantal productie- en sandbox-omgevingen dat u kunt maken voor Human Resources in LCS is nu gebaseerd op bijgewerkte licenties. U kunt nu zoveel omgevingen maken als u nodig hebt per LCS-project, afhankelijk van het aantal aangeschafte licenties. Met de nieuwe licentie, die op 1 februari 2020 is bijgewerkt, kunnen klanten aanvullende omgevingen kopen. Zie de [licentiehandleiding voor Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources) voor meer informatie over licentievereisten voor aanvullende omgevingen.

## <a name="platform-changes"></a>Platformwijzigingen

- Apps op volledige pagina (preview): met deze preview-functie, waarmee u de opgeslagen weergaven kunt inschakelen, kunnen Power Apps en apps van derden worden toegevoegd en weergegeven op de volledige pagina via het dashboard.

- Opgeslagen weergaven (preview): met deze preview-functie worden opgeslagen weergaven ingeschakeld. Dit is een belangrijke verbetering van het subsysteem voor persoonlijke instellingen. Met deze functie kunnen gebruikers meerdere benoemde sets persoonlijke instellingen per pagina hebben. U kunt ook weergaven publiceren naar beveiligingsrollen.

- De filterfunctie "is één van" is geoptimaliseerd: met de verbeterde filterfunctie "is één van" wordt het invoeren van meerdere filterwaarden eenvoudiger, kunt u sneller afzonderlijke of alle filterwaarden verwijderen en wordt een compacte en intuïtieve visualisatie van filterwaarden mogelijk.

- Aanbevolen velden: gebruikers moeten vaak velden toevoegen aan een raster of pagina. Dit kan moeilijk zijn met zoveel beschikbare velden. In plaats van een grote lijst te hoeven doorzoeken, kan met deze functie het systeem een reeks aanbevolen velden weergeven op basis van wat andere gebruikers meestal in vergelijkbare scenario's toevoegen.

- Standaardplakacties in rasters: deze functie zorgt ervoor dat de standaardactie in een raster wordt gekoppeld aan een specifieke kolom in een raster, ongeacht of die kolom wordt verplaatst of verborgen.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Kan het verlofsaldo niet aanpassen voor een plan zonder transitorische posten dat is gemaakt met de ingeschakelde functie voor "meerdere verloftypen" (419635)

Met deze wijziging kunt u saldi aanpassen voor verlofplannen die zijn gemaakt met de preview-functie Meerdere verloftypen ingeschakeld in Functiebeheer.

## <a name="in-preview"></a>Preview

De volgende voorbeeldfuncties zijn beschikbaar vanaf 3 februari 2020:

- **Preview-functies voor verlof en verzuim** - Zie [Preview-functies voor verlof en verzuim](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) voor meer informatie.

- **Preview-functie voor Vergoedingenbeheer** - Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie, inclusief bekende problemen.

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

## <a name="new-production-release-cadence"></a>Nieuwe tempo voor productiereleases

Vanaf april wordt het releasetempo voor Human Resources van wekelijks in tweewekelijks gewijzigd. De service-updates in alle regio's volgt nu een implementatie per twee weken om een aanpassing met veilige implementatiemethoden en het bijhouden van hoge standaarden voor stabiliteit en betrouwbaarheid in de service te garanderen. Er worden extra tests en controles uitgevoerd om de implementatie in elke fase van het proces te controleren. Zie [Het updateproces](hr-admin-setup-update-process.md) voor meer informatie over het releasetempo.

## <a name="known-issues"></a>Bekende problemen

## <a name="employment-detail-entity"></a>Entiteit Details dienstverband

De entiteit **Details dienstverband** is bijgewerkt met de volgende velden: **Betalingsfrequentie**, **Aanstellingscategorie-id**, **Type dienstverband**, **Type dienstverband-id** en **Status van vergoeding voor aanstelling**. De instellingsgegevens voor deze velden zijn afhankelijk van het vergoedingenbeheer dat is ingeschakeld in Functiebeheer. Vul deze velden niet in of werk ze niet bij in de entiteit **Details dienstverband**, omdat deze tijdens het importeren fouten zullen opleveren.
