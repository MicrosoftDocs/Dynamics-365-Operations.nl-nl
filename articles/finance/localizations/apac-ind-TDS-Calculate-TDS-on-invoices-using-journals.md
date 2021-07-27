---
title: TDS op facturen berekenen met behulp van journalen
description: Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.journalen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: bc1a8570e60e2b17f27c3e63c5ff847b3cb7a2dd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358453"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>TDS op facturen berekenen met behulp van journalen

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.journalen.

Open om te beginnen de pagina **Algemene journalen** (**Grootboek > Journaalboekingen > Algemene journalen**).

[![Algemene journalen.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Maak journaalregels met de journaalformulieren die in de tabel staan. Selecteer het rekeningtype en het tegenrekeningtype en voer het bedrag voor de transactie in. 

   > [!NOTE]
   > Op de pagina **Factuurgoedkeuringsjournaal** selecteert u **Boekstukken zoeken** en selecteert u facturen waarop u TDS wilt berekenen. Bekijk de facturen die zijn gemaakt op de pagina **Facturenregister** of de pagina **Boekstukken zoeken**.  

2. Bekijk of wijzig op het tabblad **Algemeen** van de pagina **Journaalboekstuk** in het veld **TDS-groep** de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd. Het TDS-bedrag dat op journaalregels wordt berekend, is gebaseerd op de formule die is gedefinieerd voor de TDS-belastingcodes in het veld **TDS-groep**. 

   > [!NOTE]
   > Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, zijn de velden **Bronbelastinggroep** en **TCS-groep** niet meer beschikbaar. Het veld **Bronbelastinggroep** is alleen beschikbaar op de pagina **Algemeen journaal**. TDS wordt alleen berekend als het selectievakje **Bronbelasting berekenen** is ingeschakeld voor de leverancier of klant op de pagina **Alle leveranciers** of de pagina **Alle klanten**.   

3. Selecteer het tabblad **Belastinggegevens**. Selecteer de alternatieve adressen van een bedrijf die zijn ingesteld voor het bedrijf in dit veld, indien nodig. U kunt de bedrijfsnaam bekijken in het veld **Naam**, dat onder de veldgroep **Bedrijfsgegevens** valt. 

4. Bekijk de soort belastingplichtige waar de leverancier of klant toe hoort in het veld **Soort belastingplichtige** dat onder de veldgroep **Bronbelasting** valt. In het veld **Belastingrekeningnummer** (**TAN**) kunt u de TAN van de geselecteerde bedrijfsnaam weergeven die wordt weergegeven.  

5. Selecteer **Bronbelasting** in het menu **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen. De volgende velden worden weergegeven in het bovenste deelvenster van de pagina **Tijdelijke bronbelastingtransacties**.

   - **Totaalbedrag bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.

   - **Waarde**: het totale percentage dat is gebruikt om TDS voor de transactie te berekenen. Het totale percentage is gebaseerd op de formule die is gedefinieerd voor TDS-belastingcodes gekoppeld aan de TDS-groep.

   - **Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.

   - **TDS**: als deze optie is geselecteerd, is er een TDS-groep aan de transactie gekoppeld.

  De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** op de pagina **Tijdelijke bronbelastingtransacties** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.

6. Selecteer **Drempel** om de pagina **Drempel** te openen. Bekijk de drempellimiet en uitzonderingsdrempellimiet die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld op deze pagina.

   Selecteer **Formuleontwerper** om het formulier **Formuleontwerper** te openen. Bekijk de formule die is gedefinieerd voor een specifieke TDS-belastingcode in deze pagina. Sluit de pagina's **Formuleontwerper** en **Tijdelijke bronbelastingtransacties** om terug te keren naar de pagina **Journaalboekstuk**.

8. Voer de andere vereiste gegevens in. Valideer en boek het journaal. Het TDS-bedrag dat op inkoopfacturen is berekend, wordt naar de leveranciersrekening geboekt. Het TDS-bedrag dat is berekend op verkoopfacturen wordt geboekt naar de klantrekening die is gedefinieerd voor elke TDS-belastingcode in de TDS-groep. De leveranciers- of klantrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.

9. Selecteer **Bronbelasting geboekt** om de pagina **Bron****belasting****transacties** te openen. In het veld **Waarde** wordt het totale percentage weergegeven dat is gebruikt om TDS voor de transactie te berekenen.

   De velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** op de pagina Tijdelijke bronbelastingtransacties geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.
