---
title: LTL-klassen (Less than truckload)
description: In dit onderwerp wordt beschreven wat LTL-klassen (Less Than Truckload, 'geen volledige vrachtwagen') zijn en wordt beschreven hoe u deze in instelt in Microsoft Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a6e05ea7534ee081778a899d5956e6ca7cd104cb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678061"
---
# <a name="less-than-truckload-ltl-classes"></a>LTL-klassen (Less than truckload)

[!include [banner](../includes/banner.md)]

Een LTL-klasse (less than truckload, 'geen volledige vrachtwagen') is een vrachtverzendingsklasse die wordt gebruikt om artikelen te classificeren die kunnen worden verzonden. Over het algemeen heeft elk type product of goed een NMFC-code (National Motor Freight Classification) die overeenkomt met een specifiek vrachtklassenummer voor LTL-zendingen. LTL-vrachtklassen staan voor categorieën artikelen, terwijl NMFC-codes zijn gerelateerd aan specifieke goederen in elk van de achttien vrachtklassen.

Met deze functie kunt in uw systeem de volgende taken uitvoeren:

- De LTL-vrachtklassen definiëren die in uw bedrijf worden gebruikt.
- Aan elke LTL-klasse een NMFC-code toewijzen op de pagina **NMFC-codes**. Meer informatie over dit onderwerp vindt u in [NMFC-codes (National Motor Freight Classification)](nmfc-codes.md).
- Een NMFC-code (en daarmee de bijbehorende LTL-code) toewijzen aan elk product op de pagina **Producten**.
- Precies de LTL-klasse beoordelen van elk product waaraan een NMFC-code is toegewezen.
- De verpakkingsvereisten bepalen voor elke LTL-klasse door de internationale LTL-standaarden te bekijken. Hiermee borgt u dat uw producten goed beschermd worden en veilig worden verzonden.
- Nauwkeurige schattingen van transportkosten maken, gebaseerd op de LTL-vrachtklasse voor elk product.

In dit onderwerp wordt beschreven hoe u LTL-klassen maakt in Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Een LTL-klasse maken

U maakt als volgt een LTL-klasse.

1. Volg één van deze stappen:

    - Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> LTL-klassen**.
    - Ga naar **Transportbeheer \> Instellingen \> Transportstandaard \> LTL-klassen**.

2. Selecteer in het actievenster **Nieuw** om een LTL-klasse te maken. Stel daarna de volgende velden in:

    - **LTL-klasse**: Voer de interne LTL-klasse-id van uw bedrijf in voor het goederentype. De meeste bedrijven gebruiken de internationale standaard. In dat geval komt de waarde van dit veld overeen met de waarde van het veld **Klasse**. Als uw bedrijf echter een eigen standaard gebruikt, voert u een code in die aan die standaard voldoet.
    - **Naam**: voer een beschrijvende naam in die u en andere gebruikers helpen de juiste LTL-klasse te selecteren voor elke NMFC-code.
    - **Klasse**: Voer de internationale standaard-LTL-klasse-id voor het type goederen in. De code die u hier invoert, moet voldoen aan de officiële standaard.

## <a name="example-set-up-ltl-classes"></a>Voorbeeld: LTL-klassen instellen

In het volgende voorbeeld ziet u hoe u twee verschillende LTL-klassen kunt instellen die u kunt gebruiken bij verschillende typen producten.

1. Ga naar **Magazijnbeheer \> Instellen \> Voorraad \> LTL-klassen**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **LTL-klasse**: *92.5*
    - **Naam**: *Computers, beeldschermen, koelkasten*
    - **Klasse:** *92.5*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer **Nieuw** in het actievenster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **LTL-klasse**: *125*
    - **Naam**: *Kleine huishoudelijke apparaten*
    - **Klasse:** *125*

1. Selecteer **Opslaan** in het actievenster.

## <a name="additional-resources"></a>Aanvullende bronnen

- [NMFC-codes (National Motor Freight Classification)](nmfc-codes.md)
- [Een vrachtbrief maken](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
