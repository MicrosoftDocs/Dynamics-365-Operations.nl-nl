---
title: Land van oorsprong
description: Veel organisaties verlenen certificaten aan leveranciers om ervoor te zorgen dat producten voldoen aan specifieke certificeringsnormen. Deze certificaten zijn vaak afhankelijk van het land van oorsprong. Dit artikel biedt informatie over de functie voor het land van oorsprong, waarmee u een product kunt koppelen aan het land van oorsprong en de bijbehorende productcertificaten kunt bijhouden.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 60d5a2067b8e3d311af89fb09cfa3b5c007db219
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882513"
---
# <a name="country-of-origin"></a>Land van oorsprong

[!include [banner](../includes/banner.md)]

Veel organisaties verlenen certificaten aan leveranciers om ervoor te zorgen dat producten voldoen aan specifieke certificeringsnormen. Deze certificaten zijn vaak afhankelijk van het land van oorsprong. Met de functie voor het land van oorsprong kunt u een product koppelen aan het land van oorsprong en de bijbehorende productcertificaten bijhouden.

## <a name="turn-on-the-country-of-origin-feature"></a>De functie voor land van oorsprong inschakelen

Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Beheerders kunnen gebruikmaken van de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in of uit te schakelen. Hier ziet u de functie als:

- **Module:** *Productgegevensbeheer*
- **Functienaam:** *beheerfunctie Land van oorsprong*

## <a name="configure-source-and-destination-countries"></a>Bron- en doellanden configureren

Voordat u een certificaat voor een product uitgeeft, moet u het product koppelen aan het land van bestemming en het land van oorsprong.

1. Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Regels voor land van oorsprong**.
2. Selecteer een bestaande landinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe landinstelling te maken.
3. Stel de volgende waarden in voor het geselecteerde of nieuwe land.

    | Veld | Omschrijving |
    |---|---|
    | artikelnummer | Selecteer het artikelnummer van het product. |
    | Bestemmingsland | Selecteer het land waarnaar u het product wilt verzenden. |
    | Land van oorsprong | Selecteer het land vanwaaruit u het product wilt verzenden. |

Het doel van deze instelling is om een stuklijstrapport te genereren waarin u het land van oorsprong kunt opnemen voor elk onderdeel waarvoor bron- en doellanden zijn opgegeven. Dit rapport geeft een compleet beeld van waar uw onderdelen vandaan komen en waar ze naartoe gaan.

## <a name="keep-track-of-vendor-certificates"></a>Leverancierscertificaten bijhouden

U kunt de pagina **Leverancierscertificaten voor land van oorsprong** gebruiken om certificaten bij te houden die u aan leveranciers geeft.

U moet bepalen welke certificaatdocumenten u wilt uitgeven en hoe u deze aan klanten gaat rapporteren. Met deze functie kunt u uw certificaten bijhouden. U kunt hiermee ook kiezen of de relevante certificaatnummers worden weergegeven op facturen, pakbonnen en/of orderbevestigingen.

Ga als volgt te werk om de certificaatgegevens in te stellen.

1. Ga naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong \> Leverancierscertificaten voor land van oorsprong**.
2. Selecteer een bestaande certificaatinstelling om te bewerken of selecteer **Nieuw** in het actievenster om een nieuwe certificaatinstelling te maken.
3. Stel de volgende instellingen in voor het geselecteerde of nieuwe certificaat.

    | Veld | Omschrijving |
    |---|---|
    | Leverancier | Selecteer de leverancier aan wie u het certificaat hebt uitgegeven. |
    | artikelnummer | Selecteer het artikel waarvoor u het certificaat hebt uitgegeven. |
    | Land/regio | Het land of de regio van bestemming waar u dit certificaat moet gebruiken. |
    | Certificaatnummer | Voer het identificatienummer in van het certificaat dat u hebt uitgegeven. |
    | Geldig | Selecteer de eerste datum waarop het huidige certificaat geldig is.|
    | Vervaldatum | Selecteer de laatste datum waarop het huidige certificaat geldig is. |
    | Afdrukken op factuur | Schakel dit selectievakje in om het certificaatnummer af te drukken op facturen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |
    | Afdrukken op pakbon | Schakel dit selectievakje in om het certificaatnummer af te drukken op pakbonnen die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |
    | Afdrukken op verkooporder | Schakel dit selectievakje in om het certificaatnummer af te drukken op verkooporders die naar het opgegeven land worden verzonden tijdens het opgegeven datumbereik. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Het land van oorsprong opnemen op stuklijstrapporten

Wanneer u een stuklijstrapport genereert, kunt u het land van oorsprong opnemen voor elk onderdeel waarvoor u de bron- en doellanden hebt opgegeven op de pagina **Regels voor land van oorsprong**.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer of maak een product om de pagina **Vrijgegevens productgegevens** te openen.
1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Stuklijst** de optie **Ontwerper**.
1. Selecteer op de pagina die verschijnt in het actievenster **Stuklijst \> Afdrukken**.
1. In het dialoogvenster **Stuklijstregels** stelt u het veld **Bestemmingsland** in op het doelland dat u in het rapport wilt weergeven.
1. Selecteer **OK**.

Er wordt een rapport gegenereerd en weergegeven met informatie over het land van oorsprong voor elk onderdeel. Hier volgt een voorbeeld van het rapport.

![Rapport voor Land van oorsprong.](media/country-of-origin-report.png "Rapport voor Land van oorsprong")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]