---
title: Gebruikersinstellingen mobiel apparaat
description: In dit onderwerp wordt uitgelegd hoe u gebruikersinstellingen voor mobiele apparaten beheert voor magazijnmedewerkers.
author: MarkusFogelberg
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 77b4276cec5e046a19d6d001acf41fc410052fba
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049287"
---
# <a name="mobile-device-user-settings"></a>Gebruikersinstellingen mobiel apparaat

[!include [banner](../../includes/banner.md)]

De nieuwe mobiele app Magazijnbeheer beschikt over een reeks app-specifieke instellingen waarmee een gebruikerservaring op maat kan worden gemaakt. Omdat de app kan worden gebruikt op apparaten met verschillende schermgrootten en -configuraties (zoals een tablet, telefoon of apparaat om je arm), kan het handig zijn deze instellingen centraal in Microsoft Dynamics 365 Supply Chain Management te beheren.

Met de functie voor *gebruikersinstellingen voor mobiele apparaten* kunt u algemene gebruikersinstellingen definiëren die op alle apparaten worden gebruikt. U kunt ook gedetailleerdere gebruikersinstellingen definiëren voor afzonderlijke apparaatmerken, apparaatmodellen en/of werknemers. Wanneer een werknemer zich aanmeldt bij de mobiele app Magazijnbeheer, wordt het meest specifieke instellingenprofiel opgehaald en toegepast dat is opgeslagen in Supply Chain Management voor het overeenkomende merk of apparaat of de overeenkomende gebruikers-id.

Deze functie kan werknemers sneller helpen aan de slag te gaan wanneer ze een nieuw apparaat in gebruik nemen. Hieronder volgen een aantal voorbeelden:

- Beheerders kunnen een standaardset voorkeuren instellen die het beste werken voor apparaten van een specifieke fabrikant en/of voor specifieke apparaatmodellen. Werknemers kunnen dus aan de slag met een nieuw apparaat zonder dat ze noodzakelijkerwijs de instellingen hoeven te wijzigen.
- Als uw bedrijf een pool met identieke apparaten heeft die door werknemers worden gedeeld, krijgen werknemers telkens wanneer ze zich aanmelden hun voorkeursinstellingen te zien, zelfs als ze het specifieke fysieke apparaat dat ze op een bepaalde dag selecteren, nog nooit hebben gebruikt.
- In Supply Chain Management kunnen beheerders alle opgeslagen instellingen weergeven en bewerken, zelfs voor afzonderlijke werknemers. Deze mogelijkheid kan ze helpen bij het oplossen van problemen of bij het afstemmen van nieuwe functies.

> [!IMPORTANT]
> De functie voor *gebruikersinstellingen voor mobiele apparaten* is alleen aanwezig in de nieuwe mobiele app Magazijnbeheer. Deze functie werkt niet met de oude magazijn-app.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>De functie voor gebruikersinstellingen voor mobiele apparaten in- of uitschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *gebruikersinstellingen, pictogrammen en staptitels voor de nieuwe magazijnapp*

## <a name="create-and-manage-user-settings"></a>Gebruikersinstellingen maken en beheren

Gebruik de pagina met **gebruikersinstellingen voor mobiele apparaten** om instellingenprofielen te maken, weer te geven en te beheren op alle detailniveaus. De eerste keer dat een werknemer zijn of haar gebruikersinstellingen bewerkt op een nieuw apparaat, wordt automatisch een nieuw profiel op deze pagina toegevoegd als dit nog niet bestaat. Dit profiel wordt vervolgens telkens bijgewerkt wanneer de werknemer een wijziging aanbrengt.

U kunt ook een instellingenprofiel definiëren dat van toepassing is op alle apparaatmerken, apparaatmodellen en/of werknemers. U kunt vervolgens de gedetailleerdheid vergroten door specifiekere instellingen toe te passen voor afzonderlijke merken, modellen en/of werknemers.

Volg deze stappen om gebruikersinstellingen voor uw mobiele apparaten te maken en te beheren.

1. Ga naar **Magazijnbeheer \> Mobiel apparaat \> Gebruikersinstellingen voor mobiele apparaten**.
1. Selecteer een bestaand gebruikersinstellingenprofiel in het lijstvenster om de record ervan te openen. U kunt ook **Nieuw** selecteren in het actievenster om een nieuw profiel te maken.

    Elk profiel in het lijstvenster wordt gelabeld met het merk, het model en/of de gebruikers-id waarop het profiel van toepassing is. Meer algemene profielen hebben de waarde *Alle* voor een aantal van deze kenmerken of al deze kenmerken.

1. Stel in de headersectie van de record voor het nieuwe of geselecteerde instellingenprofiel de volgende velden in:

    - **Merknaam van apparaat**: Selecteer de naam van het apparaatmerk waarop het profiel moet worden toegepast. Laat dit veld leeg als het profiel op alle merken moet worden toegepast. De lijst met waarden bevat alle merken die in uw systeem zijn gedefinieerd. Zie de volgende sectie voor informatie over het definiëren van de lijst met merken.
    - **Model-id van apparaat**: Selecteer het apparaatmodel waarop het profiel moet worden toegepast. Laat dit veld leeg als het profiel op alle modellen van het geselecteerde merk moet worden toegepast. De lijst met waarden bevat alle modellen die zijn gedefinieerd voor het merk dat is geselecteerd in het veld **Merknaam van apparaat**. Zie de volgende sectie voor informatie over het definiëren van de lijst met modellen voor elk merk.
    - **Gebruikers-id:** Selecteer de gebruikers-id van de magazijnwerker op wie het instellingsprofiel moet worden toegepast. Laat dit veld leeg als het profiel op alle werknemers moet worden toegepast.

1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Knoppositie**: Geef op hoe de knoppen op het apparaat moeten worden geplaatst. Elementen in de app kunnen worden verplaatst naar wens van de gebruiker of om ze beter af te stemmen op de links- of rechtshandigheid van de werknemer. De beschikbare opties zijn: *Rechtsonder (standaard)*, *Linksonder*, *Rechtsboven* en *Linksboven*.
    - **Schermstand**: Selecteer de schermstand die standaard moet worden toegepast in de app.
    - **Scannen met camera**: Stel deze optie in op *Ja* om de camera van het apparaat te gebruiken om invoervelden te scannen wanneer de voorkeursmodus voor invoer is ingesteld op *Scannen*. Als uw apparaat een ingebouwde scanner heeft, stelt u deze optie in op *Nee* om in plaats daarvan de scanner te gebruiken.
    - **Productfoto weergeven**: Geef op of er productfoto's moeten worden weergegeven als deze beschikbaar zijn voor het uitgebrachte product. Zie [Een afbeelding aan een product toevoegen](../pim/tasks/add-image-product.md) voor meer informatie over het toevoegen van productafbeeldingen.
    - **Kleurenthema weergeven**: Selecteer een kleurenthema voor het apparaat.
    - **Geluidsniveau**: Selecteer het geluidsniveau voor het apparaat. Selecteer een waarde tussen 0 (nul) en 10. De waarde *0* betekent geen geluid en de waarde *10* is het maximumvolume. De standaardwaarde is *4*.
    - **Vibratieniveau**: Selecteer het vibratieniveau voor het apparaat. Selecteer een waarde tussen 0 (nul) en 5. De waarde *0* betekent geen vibratie en de waarde *5* is maximale vibratie. De standaardwaarde is *1*.
    - **Tekstschaalpercentage**: Geef de tekstgrootte op als percentage van de standaardgrootte. Voer een waarde in tussen de 70 en 400. De waarde *70* is de kleinste tekstschaal en de waarde *400* is de grootste tekstschaal. De standaardwaarde is *100*.
    - **Knopschaalpercentage**: Geef de knopgrootte op als percentage van de standaardgrootte. Voer een waarde in tussen de 50 en 200. De waarde *50* is de kleinste knopschaal en de waarde *200* is de grootste knopschaal. De standaardwaarde is *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Merken van mobiele apparaten maken en beheren

Gebruik de pagina Pagina **Merken van mobiele apparaten** om de merken en modellen van apparaten die in uw instellingenprofielen kunnen worden gebruikt, weer te geven, te maken en te beheren. De mobiele app haalt de lokale merknaam en model-id automatisch op en verstuurt deze wanneer een werknemer de instellingen op een bepaald apparaat de eerste keer bewerkt. Daarom worden de meeste records gewoonlijk automatisch gegenereerd. U kunt echter ook alle records op deze pagina beheren. U kunt bijvoorbeeld voor elk merk en model betere beschrijvingen geven om op elkaar lijkende of cryptische model-id's van elkaar te onderscheiden.

Volg deze stappen om merken en modellen van uw mobiele apparaten te maken en te beheren.

1. Ga naar **Magazijnbeheer \> Mobiel apparaat \> Merken van mobiele apparaten**.
1. Selecteer een merk van een mobiel apparaat in het lijstdeelvenster om de bijbehorende record te openen. U kunt ook **Nieuw** selecteren in het actievenster om een nieuw merk te maken.
1. Stel in de headersectie van de record voor het nieuwe of geselecteerde apparaatmerk de volgende velden in:

    - **Merknaam van apparaat**: de merknaam van het apparaat, zoals *Microsoft Corporation*.
    - **Beschrijving**: u kunt een beschrijving invoeren om merknamen van elkaar te kunnen onderscheiden.

1. Op het sneltabblad **Modellen van mobiele apparaten** worden alle modellen voor het geselecteerde apparaatmerk weergegeven. Gebruik de knoppen op de werkbalk om rijen aan het raster toe te voegen of uit het raster te verwijderen. U kunt voor elke rij de volgende velden instellen:

    - **Apparaatmodel-id:** de apparaatmodel-id, zoals *Surface Book 2*.
    - **Beschrijving**: u kunt een beschrijving invoeren om model-id's van elkaar te kunnen onderscheiden.

## <a name="additional-resources"></a>Aanvullende bronnen

- [De mobiele app Magazijnbeheer installeren en verbinden](install-configure-warehouse-management-app.md)
- [Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management](step-icons-titles.md)