---
title: Een Excel-werkmap maken om detailhandelstransacties te bewerken
description: In dit onderwerp wordt beschreven hoe u een Excel-werkmap maakt zodat u detailhandelstransacties in Microsoft Dynamics 365 Commerce kunt bewerken.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: bfc3f6898087445e0276994ceeb52c178785bf3604fa163939327e99a0564f64
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753103"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Een Excel-werkmap maken om detailhandelstransacties te bewerken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een Excel-werkmap maakt zodat u detailhandelstransacties in Microsoft Dynamics 365 Commerce kunt bewerken.

## <a name="overview"></a>Overzicht

Er is een vooraf gedefinieerde Excel-sjabloon die door klanten kan worden geopend vanuit verschillende delen van het systeem en waarmee detailhandelstransacties kunnen worden bewerkt en gecontroleerd. Klanten kunnen echter ook een aangepaste Excel-werkmap maken voor dit doeleinde.

## <a name="create-and-configure-an-excel-workbook"></a>Een Excel-werkmap maken en configureren

Voer de volgende stappen uit om een Excel-werkmap te maken en te configureren zodat u detailhandelstransacties kunt bewerken.

1. Open Excel en maak een lege werkmap.
1. Selecteer **Mijn invoegtoepassingen** op het tabblad **Invoegen**.
1. Selecteer in het rechterdeelvenster de koppeling **Serverinformatie toevoegen**.
1. Voer de server-URL in en selecteer vervolgens **OK**.
1. Als het foutbericht Geen appletregistraties gevonden wordt weergegeven, voert u de volgende stappen uit om het probleem op te lossen:

    1. Ga in Commerce naar **Systeembeheer \> Instellen \> Parameters voor Office-app**.
    1. Selecteer **App-parameters initialiseren** op het sneltabblad **Parameters voor app**.
    1. Selecteer **OK** in het vak met het bevestigingsbericht.
    1. Selecteer op het sneltabblad **Geregistreerde applets** de optie **Registratie van applet initialiseren**.
    1. Herhaal indien nodig de vorige drie stappen.

1. Selecteer **Ontwerpen** en vervolgens **Tabel toevoegen**.
1. Selecteer op basis van de gegevens die moeten worden gewijzigd, de entiteiten die voor bewerking moeten worden toegevoegd aan de Excel-werkmap. Gebruik de volgende tabel als verwijzing.

    | Transactietype | Te gebruiken gegevensentiteiten |
    |------------------|----------------------|
    | Contante transacties, online orders, asynchrone klantorders, asynchrone klantoffertes | Transactie (controleerbaar), verkooptransactie (controleerbaar), betalingstransacties (controleerbaar), btw-transacties (controleerbaar), kortingstransacties (controleerbaar), toeslagentransacties (controleerbaar) |
    | Bankstorting | Transactie (controleerbaar), bankstortingstransacties (controleerbaar) |
    | Kluisstorting | Transactie (controleerbaar), kluisstortingstransacties (controleerbaar) |
    | Kascontrole | Transactie (controleerbaar), kascontroletransacties (controleerbaar) |
    | Inkomsten, onkosten | Transactie (controleerbaar), inkomsten-/onkostentransacties (controleerbaar), betalingstransacties (controleerbaar) |
    | Beginbedrag declareren, betalingsmethode verwijderen, wisselgeldinvoer, betalingsmethode wijzigen, factuurbetaling, klantstorting | Transactie (controleerbaar), betalingstransacties (controleerbaar) |

    > [!NOTE]
    > Het is belangrijk dat u slechts één gegevensentiteit toevoegt aan elke Excel-werkmap. Bovendien moeten alle velden die met een sleutelsymbool zijn gemarkeerd, aan de desbetreffende werkmap worden toegevoegd.

1. Nadat de werkmap is geconfigureerd, past u de vereiste filters toe. Zorg ervoor dat u dezelfde filters toepast op alle werkbladen in het bestand. Vermijd het laden van zeer grote hoeveelheden gegevens in het Excel-bestand. Anders kan dit gevolgen hebben voor de prestaties en kunnen Excel en het systeem trager worden. Het is raadzaam om altijd Bedrijf en Overzichtsnummer of Transactienummer te gebruiken als filters voor uw bestand.
1. Nadat de filters zijn geconfigureerd, selecteert u **Vernieuwen** om de gegevens te laden.
1. Bewerk de vereiste gegevens en publiceer ze. Als de knop **Publiceren** niet beschikbaar is, zijn sommige belangrijke velden waarschijnlijk niet toegevoegd aan de Excel-werkmap.

## <a name="additional-resources"></a>Aanvullende bronnen

[Beheer van contante transacties bewerken en controleren](edit-cash-trans.md)

[Online orders en asynchrone ordertransacties van klanten bewerken en controleren](edit-order-trans.md)

[Financiële dimensies voor detailhandelstransacties bewerken](edit-financial-dim.md)

[Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]