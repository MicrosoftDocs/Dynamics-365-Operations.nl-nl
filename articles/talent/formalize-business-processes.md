---
title: Bedrijfsprocessen formaliseren
description: Met de functie Bedrijfsproces kunt u een sjabloon voor bedrijfsprocessen maken voor processen die moeten worden voltooid binnen uw organisatie.
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
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: nl-nl
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Bedrijfsprocessen formaliseren
Met de functie Bedrijfsproces kunt u een sjabloon voor bedrijfsprocessen maken voor processen die moeten worden voltooid binnen uw organisatie. Uw bedrijf kan bijvoorbeeld elk jaar een HR-controle uitvoeren. Er kan een sjabloon worden gemaakt voor het bijhouden van alle taken van de audit om ervoor te zorgen dat ze elke keer worden uitgevoerd. Ook worden de taken in de juiste volgorde uitgevoerd. Sjablonen kunnen worden hergebruikt voor terugkerende processen of worden gekopieerd als u ze wilt gebruiken als beginpunt voor nieuwe processen.

Nadat u een sjabloon hebt gemaakt, kunt u een proces starten en bijhouden in het werkgebied Bedrijfsproces.  Als een bedrijfsproces wordt gestart, worden de taken toegewezen aan de juiste mensen en wordt een vervaldatum ingesteld. Deze functies worden hieronder uitvoerig beschreven.

## <a name="business-process-template"></a>Bedrijfsprocessjabloon
Een sjabloon voor bedrijfsprocessen bevat een groep taken die een bedrijfsproces vormen. HR-managers en assistenten kunnen standaard bedrijfsprocessen maken.  Dit kan echter worden gewijzigd in de beveiligingsconfiguratie door de functie Onderhoud algemene bedrijfsprocessen te bewerken.

Voor elk proces kan de eigenaar van een proces worden gedefinieerd.  De eigenaar van het proces heeft inzicht in alle taken voor het proces en kan taken opnieuw toewijzen of vervaldatums wijzigen.  De directeur HR kan bijvoorbeeld een sjabloon voor bedrijfsprocessen maken voor een overzicht van de vergoedingen.  De manager voor compensatie en vergoedingen kan worden ingesteld als eigenaar van een proces, zodat hij of zij inzicht heeft in de taken die moeten worden voltooid als onderdeel van de controle.  De eigenaar van een proces kan niet actieve bedrijfsprocessen of sjablonen voor bedrijfsproces maken of verwijderen.

## <a name="task"></a>Taak
Een bedrijfsproces bestaat meestal uit meerdere taken. Sommige taken kunnen worden uitgevoerd in Dynamics 365 for Talent, zoals het beoordelen van het interne cursusaanbod. In dit geval wordt een menu-item geselecteerd in het veld Taakkoppeling. Bij andere taken kan het gaan om het controleren of invullen van formulieren op een website. Als u de URL selecteert in het veld Taakkoppeling, kan het webadres worden ingevoerd. U kunt in dit veld URL's invoeren voor externe en interne locaties. U kunt ook taken maken voor activiteiten die u handmatig uitvoert, zoals het controleren van de toegankelijkheid van alle structuren. In dit geval is een taakkoppeling niet vereist. Dankzij deze flexibiliteit kunt u meerdere soorten taken volgen in een uitgebreid proces.

Taken kunnen worden toegewezen aan een specifieke werknemer of aan een positie. De manager Compensatie en vergoedingen is bijvoorbeeld altijd de persoon die een controle van verzekeringspremies uitvoert.   Selecteer bij het maken van deze taak Positie als Toewijzingstype en selecteer vervolgens manager Compensatie en vergoedingen in de lijst met posities. Wanneer het proces wordt gestart, wordt de taak toegewezen aan de werknemer die de positie manager Compensatie en vergoedingen bekleedt. U kunt ook een taak toewijzen aan een specifieke werknemer door de werknemer te selecteren in het veld Toewijzingstype en vervolgens te klikken op de juiste persoon.

Vervaldatums van taken zijn afhankelijk van de streefdatum die aan het begin van het proces is ingevoerd. Sommige taken moeten worden voltooid voor de beoogde datum en sommige na de streefdatum.  Wanneer u een taak definieert, moet u een vervaldatum invoeren die samenhangt met de streefdatum in het veld Verschuiving van vervaldatum vanaf doeldatum. Stel bijvoorbeeld dat de manager Compensatie en vergoedingen een controle van de verzekeringspremies moet uitvoeren 10 dagen voordat de HR-controle is voltooid. De gemaakte taak heeft een vervaldatum ten opzichte van de streefdatum van-10. Als het proces is gestart op 13 mei, vervalt de taak dus op 3 mei. Opmerking: vervaldatums kunnen ook worden aangepast nadat het proces is gestart.

Complexe taken vereisen mogelijk meerdere stappen of de persoon die de taken uitvoert, moet extra informatie opgeven. U kunt instructies toevoegen aan de taak en tekst met opmaak opnemen voor de instructies. De instructies kunnen aanvullende informatie bevatten voor het voltooien van de taak voor de persoon die is toegewezen om deze te voltooien.

Starten van een proces U kunt een proces starten in een sjabloon voor bedrijfsprocessen door Proces starten te selecteren.  Als een proces wordt gestart, worden taken gemaakt voor de geselecteerde werknemers en/of de posities die zijn gedefinieerd in de taken die zijn opgenomen in de sjabloon Bedrijfsprocessen. Er wordt ook een vervaldatum toegewezen aan elke taak door de verschildagen op te tellen bij of af te trekken van de streefdatum (zie de informatie met betrekking tot de verschildagen in de sectie taak). De actieve bedrijfsprocessen kunnen worden weergegeven in het werkgebied Bedrijfsprocessen. 

## <a name="employee-self-service"></a>Selfservice werknemer
Wanneer een taak wordt toegewezen aan een werknemer, kunnen de toegewezen taken worden bekeken op de selfservicepagina van de werknemer. Werknemers aan wie een bedrijfsprocestaak is toegewezen, zien de taak, de beschrijving, instructies voor het voltooien en de naam van een contactpersoon, Ze kunnen de bijbehorende Dynamics 365-pagina of webpagina openen vanuit selfserviceportal voor werknemers. Taken kunnen worden gemarkeerd als in uitvoering, geannuleerd of voltooid.

## <a name="business-process-workspace"></a>Werkgebied Bedrijfsproces
HR-professionals kunnen de actieve bedrijfsprocessen weergeven in het werkgebied Bedrijfsprocessen. In het werkgebied worden alle actieve processen en taken vermeld die aan elk proces zijn gekoppeld. De uitgebreide takenlijst kan worden gefilterd op vervaldatum. De pagina bevat ook achterstallige taken en taken die specifiek zijn toegewezen aan de HR-medewerker. Ze kunnen ook de status van alle taken bijwerken en indien nodig taken opnieuw toewijzen om de voortgang van het bedrijfsproces te waarborgen.

## <a name="my-business-processes-workspace"></a>Werkgebied Mijn bedrijfsprocessen
Eigenaren kunnen de actieve bedrijfsprocessen die aan hen zijn toegewezen, weergeven via het werkgebied Mijn bedrijfsprocessen. In het werkgebied worden alle actieve processen en bijbehorende taken vermeld waarvan de gebruiker eigenaar is.  De uitgebreide takenlijst kan worden gefilterd op vervaldatum. De pagina bevat ook taken die specifiek zijn toegewezen aan de proceseigenaar. De proceseigenaar kan de status van alle taken bijwerken en taken opnieuw toewijzen.

## <a name="navigating-business-processes"></a>Navigeren in bedrijfsprocessen
1.   Als u een sjabloon voor bedrijfsprocessen wilt toevoegen, gaat u naar Bedrijfsprocessen - koppelingen - Beheer van bedrijfsprocessen.
 - a.   Met Nieuw maakt u een nieuwe sjabloon.
 - b.   Met Kopiëren uit sjabloon wordt de geselecteerde sjabloon gekopieerd naar een nieuwe.
 - c.   Met Proces starten wordt het geselecteerde bedrijfsproces gestart, taken toegewezen en vervaldatums berekend.  
2.  Als u actieve processen en bijbehorende taken wilt weergeven, navigeert u naar het werkgebied Bedrijfsprocessen.

