---
title: NMFC-codes (National Motor Freight Classification)
description: In dit onderwerp wordt beschreven hoe u werkt met NMFC-codes (National Motor Freight Classification) in Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8e6aac6b3a8b730b6adc5c3d4410b98c3e8d5090eac866c337ed1d03409ba765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731146"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>NMFC-codes (National Motor Freight Classification)

[!include [banner](../includes/banner.md)]

Met NMFC-codes (National Motor Freight Classification) kunt u artikelen classificeren die kunnen worden verzonden. De NMFC-code is een aanduiding die wordt gebruikt om goederen te groeperen. Transportbedrijven kunnen hiermee goederen beoordelen voor verzending, door artikelen te classificeren op basis van overwegingen zoals hoe ze in de vrachtwagen passen, eventuele problemen bij laden en hanteren en de bederfelijkheid. Goederen worden geklassificeerd in een van 18 vrachtklassen met een nummer tussen 50 en 500. De klasse waar een goed in is gegroepeerd, is gebaseerd op een evaluatie van vier transportkenmerken: dichtheid, stapelbaarheid, hanteerbaarheid en aansprakelijkheid. Deze kenmerken bepalen samen de transporteerbaarheid van het goed.

Aan elk LTL-verzendartikel (Less Than Truckload, 'geen volledige vrachtwagen') wordt een NMFC-code gekoppeld. Een laptop kan bijvoorbeeld een NMFC van 2.5 worden toegewezen, terwijl aan stroomkabels een NMFC van 65 wordt toegewezen.

Dit kenmerk kan werknemers helpen om NMFC-codes te gebruiken om LTL-verzendartikelen te classificeren. Hieronder volgen een aantal voorbeelden:

- Als uw bedrijf een vrachtbeschrijving op de vrachtbrief opneemt, heeft de vervoerder een idee van wat de vracht is. Vracht is een belangrijke classificatie, omdat veel transportbedrijven hun hele bedrijfsmodel baseren op de typen vracht die ze transporteren.
- Deze classificatie kan essentieel zijn voor uw bedrijf, omdat deze wordt gebruikt om de kosten van een bepaalde lading te bepalen.
- Uw bedrijf kan de winstgevendheid van een bedrijf dat werkt met LTL-logistiek en transport identificeren.

In dit onderwerp wordt beschreven hoe u werkt met NMFC-codes in Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Vereisten

Voordat u NMFC-codes kunt maken, moet u alle LTL-vrachtklassen instellen die daaraan moeten worden toegewezen. LTL-vrachtklassen staan voor categorieën artikelen, terwijl NMFC-codes zijn gerelateerd aan specifieke goederen in elk van de achttien vrachtklassen. Meer informatie over het werken met LTL-klassen vindt u in [LTL-klassen (Less than truckload)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Een NMFC-code maken

U maakt als volgt een NMFC-code.

1. Volg één van deze stappen:

    - Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> NMFC-codes**.
    - Ga naar **Transportbeheer \> Instellingen \> Transportstandaard \> NMFC-codes**.

1. Selecteer **Nieuw** om een NMFC-code te maken. Stel daarna de volgende velden in:

    - **NMFC-code**: voer de NFMC-code voor het goederentype in.
    - **Naam**: voer een naam in voor de NMFC-code.
    - **LTL-klasse**: selecteer de LTL-klasse die aan de NMFC-code is gekoppeld.
    - **Vrachtbriefverwerkingseenheid**: definieer het standaardverwerkingstype voor de zending.

## <a name="example-set-up-nmfc-codes"></a>Voorbeeld: NMFC-codes instellen

In het volgende voorbeeld ziet u hoe u twee verschillende NMFC-codes kunt instellen die bij verschillende producten kunnen worden gebruikt.

1. Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> NMFC-codes**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **NMFC-code:** *92.5*
    - **Naam**: *Computers*
    - **LTL-klasse**: *92.5*
    - **Vrachtbriefverwerkingseenheid**: *Eenheid*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer **Nieuw** in het actievenster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **NMFC-code:** *125*
    - **Naam**: *Telefoons*
    - **LTL-klasse**: *125*
    - **Vrachtbriefverwerkingseenheid**: *Eenheid*

1. Selecteer **Opslaan** in het actievenster.

## <a name="additional-resources"></a>Aanvullende bronnen

- [LTL-klassen (Less than truckload)](ltl-class.md)
- [Een vrachtbrief maken](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
