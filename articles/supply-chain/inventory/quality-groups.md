---
title: Artikelkwaliteitsgroepen
description: In dit artikel wordt beschreven hoe u artikelkwaliteitsgroepen gebruikt en maakt om producten op een logische manier te groepen, zodat ze kunnen worden toegewezen aan kwaliteitskoppelingen voor het automatisch genereren van kwaliteitsorders.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf1ce49fa58fd1a8a5aa07636e0b2bd7e2fc10e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875360"
---
# <a name="item-quality-groups"></a>Artikelkwaliteitsgroepen

[!include [banner](../includes/banner.md)]

Een kwaliteitsgroep bevat algemene testvereisten voor artikelen. In dit artikel wordt beschreven hoe u artikelkwaliteitsgroepen gebruikt en maakt om producten op een logische manier te groepen, zodat ze kunnen worden toegewezen aan kwaliteitskoppelingen voor het automatisch genereren van kwaliteitsorders.

Als u de artikelen wilt instellen, bewerken en weergeven die aan een kwaliteitsgroep zijn toegewezen of als de kwaliteitsgroepen zijn toegewezen aan een artikel, gaat u naar **Voorraadbeheer \> Instellingen \> Kwaliteitsgroepen**. Wanneer u de testvereisten hebt gedefinieerd op de pagina **Testgroepen**, kunt u de regels voor het automatisch genereren van kwaliteitsorders definiëren. Om het proces te vereenvoudigen, definieert u geen regels voor afzonderlijke artikelen. In plaats daarvan kunt u de regels definiëren voor een kwaliteitsgroep op de pagina **Kwaliteitskoppelingen**.

## <a name="example-of-an-item-quality-group"></a>Voorbeeld van een artikelkwaliteitsgroep

Een bedrijf dat artikelen vervaardigt koopt verschillende grondstoffen in waarvoor testvereisten gelden voor een op handen zijnde inspectie. Het bedrijf definieert daarom een kwaliteitsgroep en wijst vervolgens de artikelnummers die aan de grondstoffen zijn gekoppeld, aan deze groep toe. Later koopt het bedrijf een nieuw grondstoftype in waarop dezelfde testvereisten van toepassing zijn. In plaats van nieuwe testvereisten voor de nieuwe grondstof in te stellen, voegt het bedrijf het artikelnummer voor de nieuwe grondstof aan de bestaande kwaliteitsgroep toe.

Hetzelfde bedrijf produceert tevens artikelen met dezelfde productietestvereisten en verzendt artikelen met dezelfde vereisten door voor tests die worden uitgevoerd voordat er een verzending plaatsvindt. Het bedrijf definieert daarom twee extra kwaliteitsgroepen en wijst vervolgens de relevante artikelnummers aan elke groep toe.

## <a name="create-a-quality-group"></a>Een kwaliteitsgroep maken

Volg deze stappen om een kwaliteitsgroep te maken.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Kwaliteitsgroep**: voer een unieke id of naam op voor de kwaliteitsgroep in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de kwaliteitsgroep in.

1. Sluit de pagina.

## <a name="manually-add-items-to-a-quality-group"></a>Handmatig artikelen toevoegen aan een kwaliteitsgroep

Volg deze stappen om handmatig artikelen aan een kwaliteitsgroep toe te voegen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.
1. Selecteer de kwaliteitsgroep waaraan u artikelen wilt toevoegen.
1. Selecteer **Artikelen** in het actievenster.
1. Selecteer op de pagina **Artikelen in kwaliteitsgroepen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel vervolgens voor de nieuwe rij het veld **Artikelnummer** in op het artikelnummer dat u wilt toevoegen.
1. Herhaal de vorige stap voor elk extra artikel dat moet worden toegevoegd.
1. Sluit de pagina's.

## <a name="add-multiple-items-to-a-quality-group"></a>Meerdere artikelen toevoegen aan een kwaliteitsgroep

Volg deze stappen om meerdere artikelen aan een kwaliteitsgroep toe te voegen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Kwaliteitsgroepen**.
1. Maak of selecteer de kwaliteitsgroep waaraan u artikelen wilt toevoegen.
1. Selecteer **Artikelen toevoegen** in het actievenster.
1. Voer in het dialoogvenster **Query** de filtercriteria in voor de artikelen die u wilt toevoegen. U kunt bijvoorbeeld filteren op alle artikelen in een specifieke artikelengroep.
1. Selecteer **OK**.
1. In het dialoogvenster **Artikelen toevoegen** wordt een raster weergegeven met alle artikelen die met de query overeenkomen. Controleer de resultaten.

    Als u wijzigingen moet aanbrengen, selecteert u **Selecteren** om terug te keren naar het dialoogvenster **Query** en past u de query aan.

1. Wanneer de resultaten alle artikelen bevatten die u wilt toevoegen, selecteert u **OK**.
1. Sluit de pagina.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Een artikel handmatig aan een kwaliteitsgroep koppelen

Volg deze stappen om handmatig een artikel aan een kwaliteitsgroep toe te voegen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Artikelkwaliteitsgroepen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Artikelnummer**: selecteer het artikelnummer dat u wilt toevoegen.
    - **Kwaliteitsgroep**: selecteer de kwaliteitsgroep die u aan het artikel wilt toewijzen.

1. Herhaal de vorige stap voor elke extra combinatie van een artikel en een kwaliteitsgroep die moet worden toegevoegd.
1. Sluit de pagina's.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Handmatig een kwaliteitsgroep toevoegen vanaf de pagina Vrijgegeven producten

Volg deze stappen om handmatig een kwaliteitsgroep toe te voegen vanaf de pagina **Vrijgegeven producten**.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product waaraan u een kwaliteitsgroep wilt toewijzen.
1. Selecteer in het actievenster op het tabblad **Voorraad beheren** in de groep **Kwaliteit** de optie **Artikelkwaliteitsgroepen**.
1. Selecteer op de pagina **Artikelen in kwaliteitsgroepen** in het actievenster **Nieuw** om een rij aan het raster toe te voegen. Stel vervolgens voor de nieuwe rij het veld **Kwaliteitsgroep** in op de kwaliteitsgroep die u aan het product wilt toewijzen.
1. Herhaal de vorige stap voor elke extra kwaliteitsgroep die u aan het product wilt toewijzen.
1. Sluit de pagina's.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Testinstrumenten voor kwaliteitsbeheer](quality-test-instruments.md)
- [Kwaliteitsbeheertests](quality-tests.md)
- [Testgroepen voor kwaliteitsbeheer](quality-test-groups.md)
- [Testvariabelen voor kwaliteitsbeheer](quality-test-variables.md)
- [Kwaliteitskoppelingen](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
