---
title: TDS-facturen berekenen met inkooporderformulier en verkooporderformulier
description: Dit artikel geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen.
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
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853280"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>TDS-facturen berekenen met inkooporderformulier en verkooporderformulier

[!include [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van de stappen voor het berekenen van TDS (belasting ingehouden op bron) op verschillende typen facturen met behulp van de pagina's **Inkooporder**, **Inkoopjournaal**, **Afroeporder** en **Verkooporder**.

1. Maak een inkooporder, inkoopjournaal, afroeporder voor inkoop of een verkooporder op de weergegeven pagina. Voer de vereiste gegevens in.

2. Op het tabblad **Instellingen** kunt u de soort belastingplichtige van de leverancier of klant. Deze gegevens worden vermeld in het veld **Soort belastingplichtige**, onder de veldgroep **Bronbelastinggroep**.

3. Bekijk of wijzig in het veld **TDS-groep** de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd.

   > [!NOTE]
   > Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, is het veld **TCS-groep** niet meer beschikbaar. TDS wordt alleen berekend als het selectievakje **Bronbelasting berekenen** is ingeschakeld voor de leverancier of klant op de pagina **Alle leveranciers** of **Alle klanten**.  

4. Maak op het tabblad **Regels** artikelrregels en voer de vereiste gegevens in.

5. Selecteer het tabblad **Instellingen** (regelniveau) om de TDS-groep weer te geven of te wijzigen die is gedefinieerd op koptekstniveau. De TDS-groep wordt weergegeven in het veld **TDS-groep**, dat zich onder de veldgroep **Bronbelastinggroep** valt.

6. Selecteer het tabblad **Belastinginformatie** en selecteer alternatieve adressen die zijn ingesteld voor de bedrijfsnaam die in dit veld wordt weergegeven. De bedrijfsnaam wordt weergegeven in het veld **Naam**, dat onder de veldgroep **Bedrijfsgegevens** valt. 

   De TAN van de geselecteerde bedrijfsnaam wordt weergegeven in het veld **Belastingrekeningnummer** (**TAN**) onder de veldgroep **Bronbelasting**. 

7. Selecteer **Bronbelasting** om de pagina **Tijdelijke bronbelastingtransacties** te openen. Bekijk de volgende velden in het bovenste deelvenster van de pagina **Tijdelijke bronbelastingtransacties**.

   - **Totaalbedrag** **bronbelasting**: het totale TDS-bedrag dat voor de transactie voor de TDS-groep is berekend.

   - **Waarde**: het totale percentage dat is gebruikt om TDS voor de transactie te berekenen. Het totale percentage is gebaseerd op de formule die is gedefinieerd voor TDS-belastingcodes gekoppeld aan de TDS-groep.

   - **Totaal gecorrigeerd bronbelastingbedrag**: het totale gecorrigeerde TDS-bedrag voor alle belastingcodes in de TDS-groep.

   - **TDS**: als deze optie is geselecteerd, is er een TDS-groep aan de transactie gekoppeld.

De velden op de tabbladen **Overzicht**, **Algemeen** en **Correctie** op de pagina **Tijdelijke bronbelastingtransacties** geven het berekende TDS-bedrag en details weer van het gecorrigeerde TDS-bedrag voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.

8. Selecteer **Drempel** om de pagina **Drempel** te openen. Bekijk de drempellimiet die is gedefinieerd voor de TDS-belastingcomponent die aan een specifieke TDS-belastingcode is gekoppeld op deze pagina.

9. Selecteer **Formuleontwerper** om de pagina **Formuleontwerper** te openen. Bekijk de formule die is gedefinieerd voor een specifieke TDS-belastingcode op deze pagina. 

10. Boek de factuur. Het TDS-bedrag dat op inkoopfacturen is berekend, wordt naar de leveranciersrekening geboekt en het TDS-bedrag dat op verkoopfacturen is berekend, wordt geboekt naar de klantrekening die voor elke TDS-belastingcode in de TDS-groep is gedefinieerd. De leveranciers- of klantrekeningen voor TDS-belastingcodes worden gedefinieerd op de pagina **Bronbelastingcodes**.

11. Selecteer de **Opvraag**-knop **> Factuur > Geboekt met bronbelasting**-knop om de pagina **Bronbelastingtransacties** te openen. U kunt in het veld **Waarde** het totale percentage weergeven dat is gebruikt om TDS voor de transactie te berekenen.

In de velden op de tabbladen **Overzicht**, **Algemeen** en **Bedrag** op de pagina **Bronbelastingtransacties** wordt de informatie weergegeven van TDS-gegevens die voor de transactie zijn berekend. Bekijk de TDS-berekeningsgegevens voor elke TDS-belastingcode die aan de TDS-groep is gekoppeld.
