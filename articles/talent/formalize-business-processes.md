---
title: Bedrijfsprocessen formaliseren
description: "In dit onderwerp wordt uitgelegd hoe u de functie Bedrijfsproces kunt gebruiken om een sjabloon voor bedrijfsprocessen te maken voor processen die moeten worden voltooid in uw organisatie."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ee4035f3156a91faecdecba45289dbb1ca6e947a
ms.openlocfilehash: fd538677d897c1e7d3103cd714c688373aab8d29
ms.contentlocale: nl-nl
ms.lasthandoff: 06/19/2018

---
# <a name="formalize-business-processes"></a>Bedrijfsprocessen formaliseren

[!include[banner](includes/banner.md)]

Met de functie Bedrijfsproces kunt u een sjabloon voor bedrijfsprocessen maken voor processen die moeten worden voltooid in uw organisatie. Uw bedrijf voert bijvoorbeeld elk jaar een HR-controle uit. In dit geval kunt u een sjabloon maken om alle taken bij te houden waaruit het controleproces bestaat. Met deze sjabloon kan er vervolgens voor worden gezorgd dat bij elke controle alle taken worden uitgevoerd. Als de taken in een bepaalde volgorde moeten worden uitgevoerd, kan de sjabloon helpen garanderen dat ze worden uitgevoerd in de juiste volgorde.

Sjablonen kunnen worden hergebruikt voor terugkerende processen. Ze kunnen ook worden gekopieerd en gebruikt als uitgangspunt voor het maken van nieuwe sjablonen.

Nadat u een sjabloon voor bedrijfsprocessen hebt gemaakt, kunt u een proces starten en bijhouden in het werkgebied **Bedrijfsproces**. Als een bedrijfsproces wordt gestart, worden de taken met een vervaldatum toegewezen aan de juiste mensen.

## <a name="business-process-templates"></a>Bedrijfsprocessjablonen
Een sjabloon voor bedrijfsprocessen bevat een groep taken die een bedrijfsproces vormen. HR-managers en -assistenten kunnen standaard bedrijfsprocessen maken. U kunt echter wijzigen welke rollen bedrijfsprocessen kunnen maken door de functie **Onderhoud algemene bedrijfsprocessen** in de beveiligingsconfiguratie te wijzigen.

Voor elk bedrijfsproces kunt u een proceseigenaar opgeven. De eigenaar van het proces heeft inzicht in alle taken voor het proces en kan taken opnieuw toewijzen of vervaldatums wijzigen. Stel dat de HR-directeur een sjabloon voor bedrijfsprocessen maakt om een overzicht van de vergoedingen te krijgen en de manager Compensatie en vergoedingen aanwijst als de eigenaar van het proces. De manager Compensatie en vergoedingen heeft in dat geval inzicht in de taken die moeten worden uitgevoerd als onderdeel van de controle.

De eigenaar van een proces kan geen nieuwe bedrijfsprocessen of sjablonen voor bedrijfsprocessen maken of actieve bedrijfsprocessen of sjablonen voor bedrijfsproces verwijderen.

## <a name="tasks"></a>Opdrachten
Een bedrijfsproces bestaat vaak uit meerdere taken. Sommige taken, zoals het beoordelen van het interne cursusaanbod, kunnen worden uitgevoerd in Microsoft Dynamics 365 for Talent. In dit geval is een optie geselecteerd in het veld **Taakkoppeling**. Bij andere taken kan het gaan om het controleren of invullen van pagina's op een website. In dit geval is **URL** geselecteerd in het veld **Taakkoppeling** en kan het webadres worden ingevoerd. U kunt URL's invoeren voor externe en interne locaties. U kunt ook taken maken voor activiteiten die u handmatig uitvoert, zoals een controle van de toegankelijkheid van alle structuren. In dit geval is een taakkoppeling niet vereist. Dankzij deze flexibiliteit kunt u meerdere soorten taken volgen in een uitgebreid proces.

Taken kunnen worden toegewezen aan een specifieke werknemer of aan een positie. De manager Compensatie en vergoedingen is bijvoorbeeld altijd de persoon die een controle van verzekeringspremies uitvoert. Selecteer bij het maken van deze taak daarom **Positie** bij **Toewijzingstype** en selecteer vervolgens **Manager Compensatie en vergoedingen** in de lijst **Positie**. Wanneer het bedrijfsproces wordt gestart, wordt de taak toegewezen aan de werknemer die de positie **Manager Compensatie en vergoedingen** bekleedt. Als u een taak aan een specifieke werknemer wilt toewijzen, selecteert u **Werknemer** in het veld **Toewijzingstype** en selecteert u de betreffende persoon.

Vervaldatums van taken zijn afhankelijk van de streefdatum die aan het begin van het bedrijfsproces is ingevoerd. Sommige taken moeten worden voltooid voor de streefdatum en sommige na de streefdatum. Wanneer u een taak definieert, moet u in het veld **Verschuiving van vervaldatum vanaf doeldatum** een vervaldatum invoeren die samenhangt met de streefdatum. Stel bijvoorbeeld dat de manager Compensatie en vergoedingen een controle van verzekeringspremies moet uitvoeren 10 dagen voordat de HR-controle wordt voltooid. In dat geval wordt voor de taak die is gemaakt voor de controle bij **Verschuiving van vervaldatum vanaf doeldatum** een waarde van **-10** ingesteld. Als het bedrijfsproces wordt gestart op 13 mei, vervalt de taak dus op 3 mei.

> [!NOTE]
> Vervaldatums kunnen ook worden aangepast nadat het bedrijfsproces is gestart.

Complexe taken vereisen mogelijk meerdere stappen of de personen die de taken uitvoeren moeten mogelijk extra informatie opgeven. Voor deze scenario's kunt u instructies toevoegen aan een taak. De instructies kunnen aanvullende informatie voor het voltooien van de taak bevatten voor de persoon die is toegewezen om deze te voltooien. U kunt zelfs tekst met opmaak in de instructies opnemen.

## <a name="starting-a-business-process"></a>Een bedrijfsproces beginnen
In een sjabloon voor bedrijfsprocessen kunt u een bedrijfsproces starten door **Proces starten** te selecteren. Als een proces wordt gestart, worden taken gemaakt voor de geselecteerde werknemers of de posities die zijn gedefinieerd in de taken die zijn opgenomen in de sjabloon. Er wordt ook een vervaldatum toegewezen aan elke taak door het aantal verschildagen op te tellen bij of af te trekken van de streefdatum, zoals wordt uitgelegd in de sectie Taken. U kunt actieve bedrijfsprocessen weergeven in het werkgebied **Bedrijfsprocessen**.

## <a name="employee-self-service"></a>Selfservice werknemer
Nadat een taak is toegewezen aan een werknemer, kan de werknemer deze en al zijn of haar andere toegewezen taken bekijken op de pagina **Selfservice werknemer**. Voor elke bedrijfsprocestaak die aan hem of haar is toegewezen, kan de werknemer de naam en omschrijving van de taak, instructies voor het voltooien van de taak en de naam van een contactpersoon weergeven. Vanaf de pagina **Selfservice werknemer** kan de werknemer ook de gekoppelde pagina in Microsoft Dynamics 365 of de bijbehorende webpagina openen en taken als in uitvoering, geannuleerd of voltooid markeren.

## <a name="business-process-workspace"></a>Werkgebied Bedrijfsproces
HR-professionals kunnen de actieve bedrijfsprocessen weergeven in het werkgebied **Bedrijfsprocessen**. In dit werkgebied worden alle actieve processen en taken vermeld die aan elk proces zijn gekoppeld. De uitgebreide takenlijst kan worden gefilterd op vervaldatum. Het werkgebied bevat ook achterstallige taken en taken die specifiek zijn toegewezen aan de HR-medewerker. De HR-professional kan ook de status van alle taken bijwerken en indien nodig taken opnieuw toewijzen om de voortgang van het bedrijfsproces te waarborgen.

## <a name="my-business-processes-workspace"></a>Werkgebied Mijn bedrijfsprocessen
Proceseigenaren kunnen de actieve bedrijfsprocessen die aan hen zijn toegewezen, weergeven in werkgebied **Mijn bedrijfsprocessen**. In het werkgebied worden alle actieve processen waarvan de gebruiker de eigenaar is en de bijbehorende taken weergegeven. De uitgebreide takenlijst kan worden gefilterd op vervaldatum. Het werkgebied bevat ook taken die specifiek zijn toegewezen aan de HR-medewerker. De proceseigenaar kan ook de status van alle taken bijwerken en taken opnieuw toewijzen.

## <a name="navigating-business-processes"></a>Navigeren in bedrijfsprocessen
Als u een sjabloon voor bedrijfsprocessen wilt maken of kopiëren, of een bedrijfsproces wilt starten, navigeert u naar Bedrijfsprocessen - Koppelingen - Beheer van bedrijfsprocessen. Vervolgens kunt u de volgende acties uitvoeren:

- Selecteer **Nieuw** om een nieuwe sjabloon voor bedrijfsprocessen te maken.
- Selecteer **Kopiëren uit sjabloon** om de geselecteerde sjabloon naar een nieuwe sjabloon te kopiëren.
- Selecteer **Proces starten** om het geselecteerde bedrijfsproces te starten, taken toe te wijzen en vervaldatums te berekenen.

Als u actieve processen en bijbehorende taken wilt weergeven, opent u het werkgebied **Bedrijfsprocessen**.


