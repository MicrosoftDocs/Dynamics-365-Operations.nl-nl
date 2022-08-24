---
title: Staptitels en instructies aanpassen voor de mobiele app Warehouse Management
description: In dit artikel wordt beschreven hoe u aangepaste instructies kunt aanmaken en weergeven voor elke stap van elke taakstroom die u hebt ingesteld voor de mobiele app van Warehouse Management.
author: Mirzaab
ms.date: 08/11/2021
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 40b2115126aae28a41feaec4d3aabd73595107cd
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220144"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Staptitels en instructies aanpassen voor de mobiele app Warehouse Management

> [!IMPORTANT]
> De functies die in dit artikel worden beschreven, zijn alleen van toepassing op de nieuwe mobiele app van Warehouse Management. Deze hebben geen invloed op de oude magazijn-app, die nu is afgeschaft.

In dit artikel wordt beschreven hoe u aangepaste instructies kunt aanmaken en weergeven voor elke stap van elke taakstroom die u hebt ingesteld voor de mobiele app van Warehouse Management. Wanneer magazijnmedewerkers goed geschreven instructies ontvangen, kunnen ze onmiddellijk nieuwe taakstromen gaan gebruiken zonder dat er vooraf training nodig is. Deze functie biedt de volgende verbeteringen:

- **Werknemers sneller maken door ze eenvoudige instructies te laten volgen voor elke taakstap.** Elke stap in een stroom biedt eerstelijnsmedewerkers instructies, waardoor ze de taak begrijpen.
- **Bied instructies die overeenkomen met uw eigen processen.** Schrijf uw eigen instructies die overeenkomen met uw bedrijfs- en magazijnprocessen. U kunt de terminologie bijvoorbeeld geschikt maken voor uw fysieke ruimte en lokale afkortingen.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Schakel de stapinstructiesfunctie van de Warehouse-app in

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Stapinstructies van magazijnapp verwerken* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="step-titles-and-step-instructions-in-the-app"></a>Staptitels en stapinstructies in de app

Elke stap in een taakstroom in de mobiele app van Warehouse Management wordt aangeduid met een stap-ID. Bovendien heeft elke stap een titel, een pictogram en een instructie. (Zie [Stappictogrammen en titels toewijzen voor de mobiele app van Warehouse Management](step-icons-titles.md) voor meer informatie.)

### <a name="step-titles"></a>Staptitels

Een *staptitel* is een korte omschrijving van wat een werknemer tijdens een stap moet doen. Deze wordt als grote tekst bovenaan het scherm weergegeven, zoals in de onderstaande afbeelding te zien is.

![Voorbeeld van een staptitel in de mobiele app van Warehouse Management](media/wma-step-title.png "Voorbeeld van een staptitel in de mobiele app van Warehouse Management")

> [!TIP]
> Vanwege de grote tekstgrootte moet u proberen de staptitels zo kort mogelijk te houden. Anders wordt de tekst mogelijk afgesneden. Voor lange titels kunnen werknemers echter gewoon de titel indrukken en vasthouden om een dialoogvenster te openen waarin de volledige tekst wordt weergegeven.

### <a name="step-instructions"></a>Stapinstructies

Een *stapinstructie* is een langere omschrijving die meer informatie geeft over wat een werknemer tijdens een stap moet doen. Deze verschijnt in een pop-upvenster, zoals in de volgende afbeelding te zien is.

![Voorbeeld van een stapinstructie in de mobiele app van Warehouse Management](media/wma-step-instructions.png "Voorbeeld van een stapinstructie in de mobiele app van Warehouse Management")

De stapinstructie wordt automatisch weergegeven wanneer een stap geopend wordt. Werknemers kunnen dit overslaan door ergens buiten het pop-upvenster te klikken. Daarnaast bevat het dialoogvenster een selectievakje **Niet opnieuw weergeven**. Werknemers kunnen deze selecteren om te voorkomen dat de instructie de volgende keer weer verschijnt wanneer ze dezelfde taak uitvoeren.

## <a name="load-the-default-setup"></a>De standaardinstelling laden

Wanneer u de *stapinstructiesfunctie voor de Warehouse-app* voor de eerste keer gebruikt, bevat het systeem geen aanpasbare staptitels of instructies. Het eerste wat u moet doen, is dus de standaardinstelling laden. De standaardinstellingen bieden teksten in elke ondersteunde taal voor alle beschikbare stap-ID's. Volg deze stappen om de standaardinstelling te laden.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**
1. Selecteer **Standaardinstelling maken** in het actievenster. De pagina wordt met de standaardstappen gevuld.

## <a name="customize-step-titles-and-instructions"></a>Staptitels en instructies aanpassen

Volg deze stappen om de titel en/of instructie van een stap in het gewenste aantal talen aan te passen.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**

    De pagina **Stappen voor mobiele apparaten** geeft elke stap weer die voor uw systeem beschikbaar is. Elke stap-ID kan tussen het gewenste aantal menu-items van een mobiel apparaat worden gedeeld. Als een stap-ID met meerdere menu-items wordt gedeeld, worden voor alle menu-items dezelfde titel en instructie weergegeven. U kunt dit echter overschrijven, zodat u de titel en instructie voor specifieke menu-items kunt aanpassen. (Zie het volgende gedeelte voor meer informatie.)

    Het raster bevat de volgende kolommen:

    - **Naam menu-item**: rijen waarin deze kolom leeg is, gebruiken de standaard staptitel en -instructie die van toepassing zijn op alle menu-items van het mobiele apparaat waarvoor geen overschrijving vastgelegd is. Rijen waarin deze kolom is ingesteld op de naam van een menu-item, hebben overschrijvingen die alleen van toepassing zijn op het gespecificeerde menu-item.
    - **Stap-ID**: de unieke ID van de stap.
    - **Titel voor invoer**: de titel die wordt weergegeven wanneer de app om nieuwe informatie vraagt. Normaal gesproken zijn de velden op de pagina leeg (dat wil zeggen dat ze geen vooraf ingestelde waarden hebben).
    - **Titel voor bevestiging**: de titel die wordt weergegeven wanneer de app om bevestiging van een waarde vraagt die al in het systeem is opgeslagen. Normaal gesproken hebben de velden op de pagina vooraf ingestelde waarden.

1. Zoek de combinatie van de waarden **Stap-ID** en **Naam van het menu-item** die u wilt bewerken, en selecteer de waarde in de kolom **Stap-ID**. Op de pagina die geopend wordt, staan alle beschikbare vertalingen voor de titel en instructie van de geselecteerde stap.
1. Volg een van deze stappen om de tekst voor elke gewenste taal aan te passen. Met beide opties kunt u teksten voor bestaande talen bewerken. Met de eerste optie kunt u echter alleen teksten voor nieuwe talen toevoegen, en uitsluitend met de tweede optie kunt u teksten weergeven en bewerken voor alle bestaande menuspecifieke overschrijvingen van de geselecteerde taal.

    - Op de werkbalk selecteert u **Toevoegen** om een dialoogvenster te openen waarin u teksten voor elke ondersteunde taal kunt toevoegen of bewerken. Stel het veld **Referentietaal** in op de taal waarvoor u waarden wilt weergeven. De waarden worden in de linkerkolom weergegeven. Stel het veld **Taal van de vertalingen** in op de taal die u wilt toevoegen of aanpassen. Bewerk in de rechterkolom de waarden van de velden **Titel voor invoer**, **Instructie voor invoer**, **Titel voor bevestiging** en **Instructie voor bevestiging** zoals u wilt. Selecteer vervolgens **OK**.
    - Zoek in het raster de rij waar het veld **Taal** is ingesteld op de taal die u wilt bewerken en selecteer deze. Selecteer in de werkbalk **Toon &lt;taal&gt; vertalingen van deze stap** om een dialoogvenster te openen waarin u teksten kunt bewerken voor alle beschikbare overschrijvingen voor de geselecteerde taal. Het dialoogvenster bevat een raster met rijen voor beide standaardteksten (waarbij het veld **Naam van het menu-item** leeg is) en voor elk beschikbare overschrijvende tekst (waarbij het veld **Naam van het menu-item** ingesteld is op de naam van het menu-item waarop de overschrijvende tekst van toepassing is). Bewerk de waarden van de velden **Titel voor invoer**, **Instructie voor invoer**, **Titel voor bevestiging** en **Instructie voor bevestiging** zoals u wilt. Selecteer vervolgens **OK**.

1. Ga door met werken, totdat u elke vereiste titel en instructie voor elke vereiste taal vastgelegd hebt.

## <a name="add-menu-specific-overrides"></a>Menuspecifieke overschrijvingen toevoegen

Zoals in het vorige gedeelte genoemd is, kunt u voor elke stap-ID een aantal menuspecifieke overschrijvingen opstellen. U kunt deze mogelijkheid gebruiken om de instructie te bewerken en te wijzigen, zodat deze beter bij uw lokale bedrijfsproces voor een bepaalde menu-item past. Als uw bedrijf zijn werknemers tijdens het verzamelen van verkooporders bijvoorbeeld werk-ID's op een afgedrukt document aanbiedt, kunt u werknemers schriftelijk waarschuwen dat ze moeten beginnen met het scannen van een werk-ID.

Elke overschrijving is van toepassing op een specifiek menu-item van een mobiele apparaat en kan een groot aantal vertalingen bevatten. Als er geen overschrijvingen voor een menu-item zijn, gebruikt het menu-item de standaardteksten. Als er geen overschrijvende vertaling voor een taal vastgelegd is, worden de standaardteksten gebruikt, ook voor menu-items met een overschrijvende tekst voor andere talen.

Voer de volgende stappen uit om een overschrijving te maken en te configureren.

1. Ga naar **Warehouse management \> Instellen \> Mobiel apparaat \> Stappen voor mobiel apparaat**
1. Zoek in het raster naar en selecteer de rij waarvoor een overschrijving gemaakt moet worden.
1. Selecteer **Stapconfiguratie toevoegen** in het actievenster.
1. Stel in het vervolgkeuzedialoogvenster **Stapconfiguratie toevoegen** het veld **Menu-item** in op de naam van het menu-item van het mobiele apparaat waarop uw overschrijving van toepassing is. Selecteer vervolgens **OK**.
1. Op de pagina die verschijnt, worden alle teksten weergegeven die beschikbaar zijn voor de nieuwe overschrijving. In eerste instantie wordt er maar één taal aangemaakt. Alle andere talen blijven de standaardteksten gebruiken, tenzij u deze talen hier toevoegt. Bewerk de teksten en voeg nieuwe talen toe, zoals in de vorige sectie beschreven is.
