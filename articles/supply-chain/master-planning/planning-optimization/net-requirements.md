---
title: Nettobehoeften en informatie over tracering van de behoefte
description: Dit artikel biedt informatie over berekende nettovereisten en het traceren van informatie.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748433"
---
# <a name="net-requirements-and-pegging-information"></a>Nettobehoeften en informatie over tracering van de behoefte

[!include [banner](../../includes/banner.md)]

Wanneer u de hoofdplanning uitvoert, is het belangrijk dat u de uitvoer begrijpt, hoe de bestaande voorraad de vraag dekt en waarom een bepaalde voorraad is gegenereerd. U kunt de pagina **Nettovereisten** gebruiken om een beter inzicht te krijgen in de berekende behoeften die door de hoofdplanning worden geproduceerd.

Op de pagina **Nettovereisten** worden de nettovereisten weergegeven die voor het product worden berekend in de hoofdplanning. Ook worden de dekkingsinstellingen die zijn toegepast tijdens de hoofdplanning, een opsplitsing van de totale behoeften per transactietype en de tracering van informatie gegeven.

## <a name="open-the-net-requirements-page"></a>Open de pagina Nettovereisten

U kunt de pagina **Nettovereisten** op een van de volgende manieren openen:

- Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**. Selecteer of open een product. Selecteer vervolgens in het deelvenster Actie het tabblad **Plannen** in de groep **Vereiste** en selecteer **Nettovereisten**.
- Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**. Open een verkooporder. Selecteer op de werkbalk in het sneltabblad **Verkooporderregels** vervolgens **Product en voorraad \> Nettovereisten**.
- Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**. Selecteer of open een geplande verkooporder. Selecteer vervolgens in het Actievenster het tabblad **Weergeven** in de groep **Vereisten** en selecteer **Behoefteprofiel**.

## <a name="use-the-net-requirements-page"></a>Gebruik de pagina Nettovereisten

De pagina **Nettovereisten** bestaat uit secties boven en onder. Het actievenster op deze pagina bevat een knop **Bijwerken**. Wanneer deze knop is geselecteerd, verschijnt een menu met opdrachten.

### <a name="select-a-master-plan-to-view"></a>Een hoofdplan selecteren dat u wilt weergeven

Voordat u de nettovereisten van het product controleert, moet u het relevante hoofdplan selecteren in het veld **Plan** boven aan de pagina.

### <a name="upper-section"></a>Bovenste gedeelte

Het bovenste gedeelte van de pagina bevat de volgende tabbladen:

- **Overzicht** – De artikelbehoeften van de productdimenssie weergeven.
- **Artikelbehoefteplanning** – De behoefteberekeningsinstellingen weergeven die zijn gebruikt bij het berekenen van behoeften.
- **Overzicht** – Een uitsplitsing weergeven van de behoeftentotaal per transactietype.
- **Periode** – De ontvangsten, problemen en geschatte beschikbare voorraad weergeven voor elke periode die is gedefinieerd in de periodesjabloon. U kunt ook een grafische weergave bekijken van de geschatte beschikbare voorraad.

### <a name="lower-section"></a>Onderste gedeelte

Het onderste gedeelte van de pagina bevat de volgende tabbladen:

- **Overzicht** – De lijst weergeven met productbehoeften die zijn berekend tijdens de hoofdplanning, samen met uitgifte- en ontvangsttransacties die overeenkomen met de behoeften. De lijst is standaard gesorteerd op behoeftedatum. Wanneer u een behoefte selecteert, wordt op het sneltab **Tracering van behoefte** in het onderste gedeelte de bron van de behoefte of de transacties die aan de behoefte voldoen weergegeven.
- **Algemeen** – Gedetailleerde informatie over de geselecteerde behoefte weergeven.
- **Actie** – Actieberichten voor de behoeften weergeven.

### <a name="the-action-pane"></a>Het actievenster

De volgende opdrachten zijn beschikbaar in het actievenster:

- **Hoofdplanning \> bijwerken** – Hoofdplanning rechtstreeks vanaf de pagina **Nettovereisten** uitvoeren.
- **Prognoseplanning \> bijwerken** – Prognoseplanning rechtstreeks vanaf de pagina **Nettovereisten** uitvoeren. Deze bewerking wordt niet ondersteund door Planningsoptimalisatie.
- **Continuïteitsplanning \> bijwerken** – Continuïteitsplanning rechtstreeks vanaf de pagina **Nettovereisten** uitvoeren. Deze bewerking wordt niet ondersteund door Planningsoptimalisatie.

## <a name="example-scenario"></a>Voorbeeldscenario

In dit voorbeeld wordt weergegeven hoe tracering van informatie wordt weergegeven op de **pagina** Nettovereisten.

### <a name="prerequisites"></a>Vereisten

Voordat u dit scenario doorloopt, moeten de volgende vereisten worden voorbereid:

1. U moet werken aan een systeem waarin de standaard voorbeeldgegevens beschikbaar zijn en u moet de rechtspersoon instellen op *USMF*.
2. In dit voorbeeld wordt product *1000* gebruikt, dat deel uitmaakt van de voorbeeldgegevens van USMF. Zorg ervoor dat dit product beschikbaar is en dat het op de volgende manier is ingesteld:

    - **Standaardordertype:** *Inkooporder*
    - **Voorhanden voorraad:** *10,00*

3. Maak een verkooporder voor een hoeveelheid van *25,00* van product *1000*. Gebruik de opslagdimenssie waar de voorhanden voorraad zich bevindt.
4. Hoofdplanning uitvoeren voor het hoofdplan *DynPlan*.

### <a name="review-the-calculated-requirements"></a>Controleer de berekende behoeften

Vervolgens opent u de pagina **Nettovereisten** voor product *1000* om te controleren hoe berekende behoeften met elkaar overeenkomen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product met een **Artikelnummer** waarde van *1000*.
1. Selecteer in het Actievenster het tabblad **Plannen** in de groep **Vereiste** en selecteer **Nettovereisten**.
1. Stel op de pagina **Nettovereisten** het veld **Plannen** in op *DynPlan*.
1. Controleer op het tabblad **Overzicht** in het onderste deel van de pagina of de volgende behoeften zijn weergegeven als rijen in het raster.

    | Verwijzing | Behoeftehoeveelheid | Samengevoegd |
    |---|---|---|
    | Voorhanden | 10.00 | 10.00 |
    | Geplande inkooporders | 15.00 | 25.00 |
    | Verkooporder | -25,00 | (Leeg) |

    > [!NOTE]
    > Het veld **Behoeftehoeveelheid** vertegenwoordigt de totale hoeveelheid die nodig is voor de behoefte (als de waarde negatief is) of voorraden (als de waarde positief is). Het veld **Samengevoegd** geeft de totale ontvangst- en uitgiftehoeveelheden weer die zijn gecumuleerd tijdens de geselecteerde periode.

1. Selecteer de behoefteregel *Voorhanden* en controleer vervolgens in het sneltabblad **Tracering van de behoefte** de behoeften waarvoor deze voorraad geldt. De volgende rij moet hier worden weergegeven.

    | Verwijzing | Behoeftehoeveelheid | Gedekte hoeveelheid |
    |---|---|---|
    | Verkooporder | -25,00 | -10.00 |

    De bestaande aanwezige voorraad dekt gedeeltelijk de vraag die afkomstig is van de verkooporder.

    ![Informatie traceren voor de voorhanden voorraad](media/pegging-on-hand.png "Informatie voor de voorhanden voorraad traceren")

1. Selecteer de behoefteregel *Geplande inkooporders* en controleer vervolgens in het sneltabblad **Tracering van de behoefte** de behoeften waarvoor deze voorraad geldt. De volgende rij moet hier worden weergegeven.

    | Verwijzing | Behoeftehoeveelheid | Gedekte hoeveelheid |
    |---|---|---|
    | Verkooporder | -25,00 | -15,00 |

    Omdat de verkooporder al gedeeltelijk is gedekt, wordt een geplande inkooporder gemaakt voor de resterende hoeveelheid.

    ![Informatie traceren voor de geplande inkooporder](media/pegging-planned-purchase-order.png "Informatie voor de geplande inkooporder traceren")

1. Selecteer de behoefteregel *Verkooporder* en controleer vervolgens in het sneltabblad **Tracering van de behoefte** de behoeften die deze vraag dekt. De volgende rijen moeten hier worden weergegeven.

    | Verwijzing | Behoeftehoeveelheid | Gedekte hoeveelheid |
    |---|---|---|
    | Voorhanden | 10.00 | 10.00 |
    | Geplande inkooporders | 15.00 | 15.00 |

    ![Informatie traceren voor de verkooporder](media/pegging-planned-purchase-order.png "Informatie voor de verkooporder traceren")

> [!NOTE]
> De vereiste *Veiligheidsvoorraad* is niet opgenomen op de pagina **Nettobehoeften**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
