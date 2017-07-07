---
title: Rapporten voor de Wet Betaalbare zorg maken
description: Er is functionaliteit beschikbaar om werkgevers te helpen die de gegevens moeten bijhouden die wordt gemeld via de formulieren 1095-B en 1095-C, ter ondersteuning van het Employer Mandate-gedeelte van van de Wet Betaalbare zorg (Affordable Care Act, ACA). Houd er rekening mee dat deze functionaliteit alleen beschikbaar is voor rechtspersonen in de Verenigde Staten.
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 61fa5dd3580c769457ea2cfdc669f68bd3b30980
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---
# <a name="generate-affordable-care-act-reports"></a>Rapporten voor de Wet Betaalbare zorg maken
Er is functionaliteit beschikbaar om werkgevers te helpen die de gegevens moeten bijhouden die wordt gemeld via de formulieren 1095-B en 1095-C, ter ondersteuning van het **Employer Mandate**-gedeelte van van de Wet Betaalbare zorg (Affordable Care Act, ACA). Houd er rekening mee dat deze functionaliteit alleen beschikbaar is voor rechtspersonen in de Verenigde Staten.

## <a name="getting-started"></a>Aan de slag
Wanneer u begint informatie aan te geven via de formulieren 1095-B en 1095 C, moet u eerst een of meer ACA-dekkingsgroepen maken. Deze ACA-dekkingsgroepen worden gebruikt om het dekkingsaanbod aan te geven dat aan een werknemer is verstrekt, het werknemersgedeelte van de laagste maandelijkse premie (als de kosten boven de federale armoedegrens ligt), evenals de Safe Harbor (indien toepasselijk) waar de werkgever gebruik van maakt. Wanneer u ACA-groepen gebruikt, kunt u de informatie voor deze velden beheren zonder dat u elk werknemersdossier hoeft door te werken, zolang de omstandigheden identiek zijn. Daarnaast kunnen ACA-dekkingsgroepen eenvoudig worden toegewezen aan een of meerdere werknemers, door middel van de functie Groepsgewijze toewijzing op de pagina.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Meerdere versies van een dekkingsgroep onderhouden
U kunt meerdere versies van een dekkingsgroep aanhouden, zodat u wijzigingen kunt aanbrengen die de informatie van de groep actueel houdt zonder dat u een nieuwe groep hoeft te maken en werknemers daaraan toewijst, wanneer iets wijzigt in uw organisatie of in secundaire arbeidsvoorwaarden die u aanbiedt. 

Nadat u de benodigde ACA-dekkingsgroepen hebt gemaakt, kunt u de groepen in bulk toewijzen aan werknemers die met behulp van de functie **Groepsgewijze toewijzing** op de pagina, of u kunt voor iedere werknemer aangeven of ACA-informatie moet worden getraceerd en gerapporteerd en ook de werknemer toewijzen aan een ACA-dekkingsgroep.

Als u ACA-dekkingsinformatie niet hoeft bij te houden of te rapporteren voor een werknemer, bijvoorbeeld als deze een parttime-werknemer is, kunt u het veld **Dekking rapporteren** instellen op Nee. Hoewel elke werknemer waarvoor u ACA-gegevens moet bijhouden, moet worden toegewezen aan een ACA-dekkingsgroep, kunt u nog steeds de opties **Dekkingsaanbod**, **Werknemersdeel van kosten** en **Safe Harbor** wijzigen voor elke maand (of alle maanden) waarin andere waarden nodig zijn dan de waarden die zijn ingevoerd in de ACA-dekkingsgroep.

Als u uitzonderingen wilt invoeren voor een of meer van de ACA-dekkingsgroepwaarden, klikt u op de koppeling Dekking betaalbare zorg op de pagina Medewerkergegevens, die u vindt onder de sectie Aanvullende gegevens op het tabblad Dienstverband.

## <a name="reporting-health-care-coverage"></a>Gezondheidszorgdekking rapporteren
Niet alleen moet u bijhouden of en zo ja, welke dekking is aangeboden aan een full-time werknemer; ook moet, als de werkgever meebetaalt aan interne zorgverzekering waarvoor de werknemer is aangemeld (ongeacht of deze full-time of part-time is), aanvullende informatie worden aangegeven via het formulier 1095-C. Elke werknemer (inclusief gezinsleden) die valt onder door de werkgever gesponsorde vergoedingsschema's moet worden vermeld in het rapport voor de maanden waarin zij verzekerd waren. 

U kunt voor elk vergoedingsschema bepalen of het moet worden aangegeven door het selectievakje **Aan te geven voor ACA** in te schakelen.

Als werknemers er daarnaast voor kiezen om een of meerdere gezinsleden onder een van de vergoedingen te laten vallen, kunt u voor elke werknemer apart aangeven op welke datums het gezinslid was verzekerd op de pagina Vergoedingen onderhouden. Om aan te geven dat het gezinslid wordt gedekt door de vergoeding, kiest u de knop bewerken in het actievenster van het sneltabblad Afhankelijken.

Op de pagina **Datumbeheer dekking afhankelijke** kunt u opgeven op welke datums de afhankelijke is gedekt door de vergoeding. Wanneer u datums op deze pagina invoert, wordt automatisch het selectievakje **Gedekt** op de pagina **Vergoedingen onderhouden** ingeschakeld.

## <a name="generate-1095b-and-1095c-forms"></a>De formulieren 1095-B en 1095-C genereren
U kunt ook de formulier 1095-B en 1095-C genereren in het product en distribueren naar uw werknemers. U kunt ook vanuit het systeem het formulier 1095-C en de bijbehorende 1094-C-verzendbestanden elektronisch genereren, waarmee u het geheel naar de IRS kunt verzenden.  

Wanneer u het formulier 1095-C genereert, voer dan eveneens het betreffende kalenderjaar of fiscale jaar in, net als wanneer u het formulier van twee of drie pagina's wilt printen. Het formulier met drie pagina's is alleen nodig als de werkgever interne verzekering aanbiedt en een werknemer meer dan zes gedekte afhankelijken heeft, met inbegrip van zichzelf. Bij het genereren van het formulier met twee pagina's detecteert het systeem automatisch of een werknemer meer dan 6 gedekte afhankelijken heeft en slaat die werknemer over tijdens het genereren van het formulier. Wanneer u het formulier van drie pagina's genereert, neemt het systeem ook alleen de werknemers op die meer dan zes gedekte afhankelijken hebben.

## <a name="viewing-information"></a>Informatie weergeven
Op de pagina **Dekking betaalbare zorg werknemer** kunt u zien welke werknemers zijn toegewezen aan de verschillende dekkingsgroepen, welke werknemers niet hoeven te worden opgenomen in een rapport en welke werknemers niet zijn toegewezen.

Als een van de standaardwaarden van de ACA-dekkingsgroep is overschreven, wordt dit aangegeven met een asterisk naast de gewijzigde waarde. Als de waarden voor alle twaalf maanden hetzelfde zijn en niet zijn overschreven, wordt de waarde weergegeven in de kolom **Alle 12 maanden**.

In het informatievenster kunt u ook zien welke werknemers zijn gemarkeerd als niet te rapporteren volgens de ACA, wat inhoudt dat u niet hoeft bij te houden of dekking is aangeboden en hen ook geen formulier 1095-C hoeft te verstrekken aan het einde van het jaar. Als u **Niet aan te geven onder ACA** selecteert in het veld **Filteren op**, kunt u een lijst met alle werknemers genereren die zijn gemarkeerd om geen 1095-C te ontvangen.

Naast een lijst met werknemers die u niet onder de ACA hoeft aan te geven, kunt u ook alle werknemers zien die niet zijn toegewezen (zonder waarde in het veld **ACA-dekking aangeven**) of die zijn toegewezen aan een ACA-dekkingsgroep die is verlopen voor het jaar dat is geselecteerd in het veld **Jaar**.

U kunt via een van de filteropties gegenereerde lijsten met werknemers naar Excel exporteren.

Als u gedekte personen moet aangeven omdat u als werkgever interne verzekering aanbiedt, kunt u ook alle afhankelijken zien die zijn gedekt onder vergoedingsplannen die zijn gemarkeerd als **Aan te geven voor ACA**, door de actie Gezinsdekking weergeven in de actievensterstrook te kiezen.

**Opmerking**: Alleen vergoedingen waarvan het plan is gemarkeerd als **Aan te geven voor ACA** worden weergegeven in het informatievenster.
