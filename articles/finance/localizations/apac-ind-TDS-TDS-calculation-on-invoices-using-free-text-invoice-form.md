---
title: TDS-berekening op facturen van de pagina Vrije-tekstfactuur
description: In dit onderwerp wordt uitgelegd hoe u TDS-belasting op facturen berekent met behulp van de pagina Vrije-tekstfactuur.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5a1960974dff90ef5f0cc8eab018351a9e412858
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725172"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS-berekening op facturen van de pagina Vrije-tekstfactuur

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u TDS-belasting op facturen berekent met behulp van de pagina **Vrije-tekstfactuur**.

1. Ga naar **Klanten \> Facturen \> Alle vrije-tekstfacturen**.

    [![Pagina Vrije-tekstfactuur.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Selecteer **Nieuw** om een vrije-tekstfactuur te maken en voer de vereiste gegevens in.
3. Selecteer het tabblad **Factuur**. In de sectie **Bronbelastinggroep** wordt in het veld **Soort belastingplichtige** de soort belastingplichtige weergegeven waar de leverancier of klant toe hoort.
4. Controleer of wijzig in het veld **TDS-groep** de standaard-TDS-groep die voor de klant is gedefinieerd.

    > [!NOTE]
    > Wanneer u een waarde selecteert in het veld **TDS-groep**, is het veld **TCS-groep** niet meer beschikbaar. TDS wordt alleen berekend als de optie **Bronbelasting berekenen** is ingesteld op **Ja** voor de klant op de pagina **Alle klanten**.

5. Selecteer op het tabblad **Belastinginformatie** kunt u in de sectie **Bedrijfsgegevens** in het veld **Naam** de bedrijfsnaam voor een alternatief adres dat voor het bedrijf is ingesteld.

    In de sectie **Bronbelasting** staat in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer van het geselecteerde bedrijf.

6. Maak op het tabblad **Factuurregels** factuurregels en voer de vereiste gegevens in.

    In de sectie **Bronbelastinggroep** staat in het veld **Belastingrekeningnummer (TAN)** het belastingrekeningnummer en in het veld **TDS-groep** wordt de TDS-groep getoond.

7. Selecteer **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen. Het bovenste deel van deze pagina heeft de volgende velden:

    - **Totaalbedrag bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.
    - **Waarde** het totale percentage dat is gebruikt om TDS voor de transactie te berekenen. Het totale percentage is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes en is gekoppeld aan de TDS-groep.
    - **Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.
    - **TDS**: een ingeschakeld selectievakje geeft aan dat er een TDS-groep aan de transactie is gekoppeld.

    De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.

8. Selecteer **Drempel** om de pagina **Drempel** te openen, waar u de drempellimiet kunt bekijken die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld.
9. Selecteer **Formuleontwerper** om de pagina **Formuleontwerper** te openen. Hier kunt u de formule bekijken die voor een specifieke TDS-belastingcode is gedefinieerd.
10. Boek de vrije-tekstfactuur. Het TDS-bedrag dat is berekend voor de vrije-tekstfactuur wordt geboekt naar de klantrekening die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep. De klantenrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.
11. Selecteer **Bronbelasting geboekt** om de pagina **Bronbelastingtransacties** te openen. In het veld **Waarde** wordt het totale percentage weergegeven dat is gebruikt om TDS voor de transactie te berekenen.

    De velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** geven de TDS-bedragen weer die zijn berekend op de factuurregels.

12. Controleer de TDS-berekeningsgegevens voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.
