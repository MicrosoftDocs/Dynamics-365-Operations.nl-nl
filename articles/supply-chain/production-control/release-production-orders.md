---
title: Productieorders vrijgeven
description: Een vrijgegeven productieorder is een order die is geautoriseerd voor productie. De term Vrijgegeven wordt gebruikt om een status in de levenscyclus van de productieorder te beschrijven, waar de productieorder beschikbaar is voor uitvoering op de productiewerkvloer en voor magazijnprocessen.
author: johanhoffmann
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ee20983209b9900037a46d56b6213d47bf852e4
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487694"
---
# <a name="release-production-orders"></a>Productieorders vrijgeven

[!include [banner](../includes/banner.md)]

Een vrijgegeven productieorder is een order die is geautoriseerd voor productie. De term Vrijgegeven wordt gebruikt om een status in de levenscyclus van de productieorder te beschrijven, waar de productieorder beschikbaar is voor uitvoering op de productiewerkvloer en voor magazijnprocessen.

## <a name="characteristics-of-the-released-state"></a>Kenmerken van de status Vrijgegeven

De status **Vrijgegeven** is een van de statussen in de levenscyclus voor productieorders. Productieorders met de status **Vrijgegeven** zijn beschikbaar voor uitvoering op de productiewerkvloer en voor magazijnprocessen. De status **Vrijgegeven** heeft de volgende kenmerken:

- Een productieorder kan de status **Vrijgegeven** krijgen van de productieorder of via het gebruik van een batchproces. De productieorder kan ook automatisch worden bijgewerkt vanuit geplande productieorders die zijn gefiatteerd door gebruikmaking van het veld **Time fence voor fiattering** op de pagina te **Hoofdplan**.
- De status **Vrijgegeven** is het signaal voor de werkvloeroperators (operators) om de uitvoering van de productietaken op de werkvloer te starten.
- Productiedocumenten, zoals routekaarten, routetaken en takenkaarten bevatten informatie over productietaken en kunnen worden uitgegeven.
- Voor materialen die fysiek zijn gereserveerd, wordt magazijnwerk gegenereerd om materialen voor de productieorder te verzamelen.

## <a name="releasing-jobs-to-the-shop-floor"></a>Taken vrijgeven aan de werkvloer

Nadat een productieorder is vrijgegeven, zijn de productietaken die verband houden met de order zichtbaar en gereed voor registratie. De operators kunnen taakregistraties maken, zoals Starten, Stoppen en Voltooid, op ofwel de pagina **Taakkaartterminal** of op de pagina **Taakkaartapparaat**. De geregistreerde tijd en hoeveelheid worden automatisch overgebracht van de registratiepagina's naar productiejournalen, om de verbruikte tijd en hoeveelheid bij te houden.

## <a name="route-cards"></a>Routekaarten

Met een routekaart beschikt u over een overzicht van informatie uit route- en bewerkingsinstellingen en uit bewerkings- en taakplanningsmethoden.

## <a name="route-jobs"></a>Routetaken

Een routetaak vermeldt elke taak van een bewerking in detail en omvat installatie, proces, wachtrij en transporttijden. Een bewerking, zoals lakken, kan bijvoorbeeld afzonderlijke taken vereisen, zoals instellingstijd, uitvoeringstijd voor het lakproces en wachttijd voor het drogen.

## <a name="job-cards"></a>Taakkaarten

Een taakkaart bevat de afzonderlijke taaknummers van een bepaalde bewerking. Per pagina wordt één taak weergegeven. De taken op een taakkaart en de geschatte tijden worden opgehaald uit de instellingsgegevens voor routes en bewerkingen. Vanaf een taakkaart kunt u de pagina **Productiejournaalregels**, **taakkaart** openen. Personen die bronnen voor bedrijfsactiviteiten beheren, kunnen feedback geven over het productieproces. De kaart bevat velden waarin u verbruiksstatistieken en informatie, zoals de fouthoeveelheid, kunt invoeren.

## <a name="warehouse-work-for-raw-material-picking"></a>Magazijnwerk voor het verzamelen van grondstoffen

Werkzaamheden voor het verzamelen van grondstoffen worden gegenereerd tijdens de vrijgave. Werk wordt alleen gegenereerd voor de hoeveelheid materialen die fysiek werd gereserveerd voor de productieorder voordat de order werd vrijgegeven. De volgende instellingen zijn vereist om magazijnwerk te genereren voor orderverzameling van grondstoffen:

- Een locatierichtlijn voor het verzamelen van grondstoffen die bepaalt op welke magazijnlocatie de materialen moeten worden verzameld
- Een wavesjabloon voor grondstoffen, waarin het beleid voor de uitvoering van magazijnwerkzaamheden is geconfigureerd
- Een productie-invoerlocatie die bepaalt waar de materialen worden geplaatst

Wanneer door nummerplaten beheerde locaties worden gebruikt, kunt u bepalen of de bestelde hoeveelheid of de volledige hoeveelheid die voor het artikel beschikbaar is, moet worden gepickt tijdens de uitvoering van de werkzaamheden voor het verzamelen van grondstoffen. Deze optie instellen:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten** en open het relevante artikel.
1. Vouw het sneltabblad **Magazijn** uit.
1. Selecteer een van de volgende opties voor het veld **Materiaal verzamelen op nummerplaatlocaties**:
    - *Orderverzamelen*: alleen de bestelde hoeveelheid moet worden verzameld.
    - *Fasering*: waar mogelijk, moet de volledige beschikbare hoeveelheid op de nummerplaatlocatie worden verzameld. Een werknemer kan alleen de volledige nummerplaathoeveelheid verzamelen als de nummerplaat geen gemengde artikelen bevat en geen gemengde dimensies heeft. Als de nummerplaat gemengde dimensies of artikelen bevat, gaat het verzamelen door alsof dit is ingesteld op *Orderverzamelen*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]