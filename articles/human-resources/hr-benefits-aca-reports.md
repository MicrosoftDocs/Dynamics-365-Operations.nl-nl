---
title: Rapporten maken voor Affordable Care Act (Amerikaanse wet inzake betaalbare zorg)
description: Rapportage voor de Affordable Care Act (ACA) genereert de formulieren 1095-B en 1095-C ter ondersteuning van het deel **Werkgeversmandaag** van de ACA.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 6682a98bb7241060b035e7da1396ec8f8973bf09
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534148"
---
# <a name="generate-aca-reports"></a>ACA-rapporten genereren


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rapportage voor de Affordable Care Act (ACA) genereert de formulieren 1095-B en 1095-C ter ondersteuning van het deel **Werkgeversmandaag** van de ACA.

> [!NOTE]
> ACA-rapportage is alleen ingeschakeld voor rechtspersonen in de Verenigde Staten.

## <a name="getting-started"></a>Aan de slag

Om informatie te volgen voor de formulieren 1095-B en 1095 C, moet u eerst een of meer ACA-dekkingsgroepen maken. In de ACA-dekkingsgroepen wordt de volgende informatie geregistreerd:

- Het dekkingsaanbod voor een werknemer
- Het werknemersdeel van de maandelijkse premie van de laagste kosten als de kosten hoger zijn dan de federale armoedegrens
- Welke Safe Harbor de werkgever gebruikt, indien van toepassing

Wanneer u ACA-dekkingsgroepen gebruikt, kunt u de informatie voor deze velden beheren zonder dat u elke werknemersrecord hoeft te wijzigen zolang de voorwaarden identiek zijn. U kunt ACA-dekkingsgroepen eenvoudig toewijzen aan een of meerdere werknemers, door middel van de functie **Groepsgewijze toewijzing** op de pagina.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Meerdere versies van een dekkingsgroep onderhouden

U kunt van elke dekkingsgroep meerdere versies onderhouden. Met deze functionaliteit kunt u wijzigingen aanbrengen zonder dat u een nieuwe groep moet maken en werknemers daar weer aan moet toewijzen. 

Nadat u ACA-dekkingsgroepen hebt gemaakt, kunt u deze groepen groepsgewijs toewijzen aan werknemers met de optie **Groepsgewijze toewijzing**. U kunt ook afzonderlijk aangeven of u ACA-gegevens wilt bijhouden en rapporteren, en een werknemer toewijzen aan een ACA-dekkingsgroep.

U hoeft bepaalde ACA-dekkingsgegevens niet bij te houden, bijvoorbeeld voor parttime werknemers. In dit geval stelt u het veld **Dekking rapporteren** in op **Nee**. Hoewel u elke werknemer met bij te houden ACA-gegevens moet toewijzen aan een ACA-dekkingsgroep , kunt u toch de volgende opties wijzigen voor maanden met verschillende waarden:

- **Dekkingsaanbod**
- **Werknemersdeel van kosten**
- **Safe Harbor**

Als u uitzonderingen wilt invoeren voor een of meer van de ACA-dekkingsgroepwaarden, klikt u op de koppeling **Dekking betaalbare zorg** op de pagina **Medewerkergegevens**, die u vindt onder de sectie **Aanvullende gegevens** op het tabblad **Dienstverband**.

## <a name="reporting-health-care-coverage"></a>Gezondheidszorgdekking rapporteren

Niet alleen moet u bijhouden of en zo ja, welke dekking is aangeboden aan full-time werknemers; ook moet, als de werkgever meebetaalt aan interne zorgverzekering waarvoor de werknemer is aangemeld (ongeacht of deze full-time of part-time is), aanvullende informatie worden aangegeven via het formulier 1095-C. Elke werknemer (inclusief gezinsleden) die valt onder door de werkgever gesponsorde vergoedingsschema's moet worden vermeld in het rapport voor de maanden waarin zij verzekerd waren. 

U kunt voor elk vergoedingsschema bepalen of het moet worden aangegeven door het selectievakje **Aan te geven voor ACA** in te schakelen.

Als werknemers er daarnaast voor kiezen om een of meerdere gezinsleden onder een van de vergoedingen te laten vallen, kunt u voor elke werknemer apart aangeven op welke datums de afhankelijke was verzekerd op de pagina **Vergoedingen onderhouden**. Om aan te geven dat de afhankelijke wordt gedekt door de vergoeding, kiest u de knop **Bewerken** in het actievenster van het sneltabblad **Afhankelijken**.

Op de pagina **Datumbeheer dekking afhankelijke** kunt u opgeven op welke datums de afhankelijke is gedekt door de vergoeding. Wanneer u datums op deze pagina invoert, wordt automatisch het selectievakje **Gedekt** op de pagina **Vergoedingen onderhouden** ingeschakeld.

## <a name="generate-1095-b-and-1095-c-forms"></a>Formulieren 1095-B en 1095-C genereren

U kunt ook de formulieren 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers. Het systeem kan ook elektronisch 1095-C-formulieren en de 1094-C IRS-verzendbestanden genereren.  

Bij het genereren van het 1095-C-formulier geeft u het betreffende belastingjaar op en geeft u aan of Social Security-nummers moeten worden gemaskeerd. Als u 1095-C-formulieren voor meer dan 500 werknemers afdrukt, ontvangt u meer dan één PDF-bestand. Het is raadzaam de waarde voor **Maximale bestandsgrootte** in het venster **Parameters voor documentbeheer** te verhogen naar 150 MB.

## <a name="viewing-information"></a>Informatie weergeven

Op de pagina **Dekking betaalbare zorg werknemer** kunt u zien welke werknemers zijn toegewezen aan de verschillende dekkingsgroepen, welke werknemers niet hoeven te worden opgenomen in een rapport en welke werknemers niet zijn toegewezen.

Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde. Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.

U kunt het informatievenster ook gebruiken om te begrijpen welke werknemers zijn gemarkeerd als niet-rapporteerbaar voor de ACA. U hoeft niet bij te houden of de dekking aan hen is aangeboden en u hoeft hen aan het einde van het jaar geen 1095-C te verstrekken. Selecteer **Niet aan te geven onder ACA** in het veld **Filteren op** om een lijst te genereren met alle werknemers die geen 1095-C ontvangen.

Daarnaast kunt u ook alle werknemers zien die niet zijn toegewezen (zonder waarde in het veld **ACA-dekking aangeven**) of die zijn toegewezen aan een ACA-dekkingsgroep die is verlopen voor het jaar dat is geselecteerd in het veld **Jaar**.

U kunt via een van de filteropties gegenereerde lijsten met werknemers naar Excel exporteren.

Als u gedekte personen moet rapporteren omdat u interne verzekering aanbiedt, kunt u alle afhankelijken weergeven die zijn gedekt door vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA**. Selecteer in het actievenster de optie **Gezinsdekking weergeven**.

> [!NOTE]
> Alleen vergoedingsplannen die zijn gemarkeerd als **Aan te geven onder ACA** worden getoond in het informatievenster.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
