---
title: TDS-belastingcodes koppelen aan TDS-belastinggroepen en de formule voor het berekenen van TDS definiëren
description: In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor TDS (belasting ingehouden op bron) kunt instellen en TDS-belastingcodes kunt koppelen aan TDS-belastinggroepen. Als u TDS voor een TDS-belastinggroep wilt berekenen, moet u de formule definiëren voor TDS-belastingcodes die eraan zijn gekoppeld.
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
ms.openlocfilehash: 81aac53cca91a75cde811c314bd6f7039852d32505fe6540921e17f3d1bbc7ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739305"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>TDS-belastingcodes koppelen aan TDS-belastinggroepen en de formule voor het berekenen van TDS definiëren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor TDS (belasting ingehouden op bron) kunt instellen en TDS-belastingcodes kunt koppelen aan TDS-belastinggroepen. Als u TDS voor een TDS-belastinggroep wilt berekenen, moet u de formule definiëren voor TDS-belastingcodes die eraan zijn gekoppeld.

Volg deze stappen om een TDS-belastinggroep in te stellen, hier TDS-belastingcodes aan te koppelen en de formule voor het berekenen van TDS te definiëren.

1. Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Bronbelastinggroepen**.

    [![Pagina Bronbelastinggroepen.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Selecteer in het actievenster **Nieuw** om een bronbelastinggroep voor TDS te maken en voer de vereiste gegevens in.
3. Selecteer in het veld **Belastingtype** de optie **TDS**.
4. Selecteer op het sneltabblad **Instellingen** de optie **Toevoegen** om een regel te maken.
5. Selecteer in het veld **Bronbelastingcode** de TDS-belastingcode voor de TDS-belastinggroep. In het veld **Bronbelastingnaam** wordt de naam van de TDS-belastingcode en de waarde in het veld **Waarde** weergegeven.
6. Schakel het selectievakje **Drempel overslaan** in als u de drempellimiet en uitzonderingsdrempellimiet wilt negeren die zijn gedefinieerd voor de TDS-belastingcomponent die is gekoppeld aan de TDS-belastingcode in TDS-transacties.
7. Schakel het selectievakje **Vrijstelling** in om te voorkomen dat de belastinggroep wordt berekend in transacties.
8. Selecteer in het actievenster **Ontwerper** om de formuleontwerper te openen, zodat u de formule kunt definiëren voor het berekenen van TDS voor de TDS-belastinggroep. Op de pagina **Ontwerper** worden op het tabblad **Belastingen** de TDS-belastingcodes weergegeven die zijn geselecteerd voor de TDS-belastinggroep.

    [![Pagina Ontwerper.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Selecteer **Alt+N** op het tabblad **Berekening** om een regel te maken. Het veld **Id** geeft de automatisch gegenereerde prioriteits-id weer voor de TDS-berekening.
10. Selecteer in het veld **Belastingcode** de TDS-belastingcode waarvoor u de formule wilt definiëren. Alle TDS-belastingcodes die zijn geselecteerd voor de TDS-belastinggroep kunnen in dit veld worden geselecteerd.
11. Selecteer in het veld **Belastbare basis** de basis voor het berekenen van de TDS:

    - **Brutobedrag**: TDS berekenen op basis van het brutotransactiebedrag (dat wil zeggen het factuurbedrag) met behulp van de berekeningsexpressie die voor de belastingcode is gedefinieerd.
    - **Excl. brutobedrag**: TDS berekenen op basis van de berekeningsexpressie die voor de belastingcode is gedefinieerd.

    > [!NOTE]
    > Het veld **Belastbare basis** kan niet worden ingesteld op **Excl. brutobedrag** voor de TDS-belastingcode met prioriteits-id **1**.

12. De TDS-berekening is gebaseerd op de formule die is gedefinieerd in het veld **Berekeningsexpressie** voor elke belastingcode die is gekoppeld aan de TDS-belastinggroep. Selecteer de knop met het plusteken (**+**), minteken (**-**), vermenigvuldigingsteken (**\**_) of deelteken (_*/**) om de berekeningsexpressie in te voeren voor de geselecteerde belastingcode in het veld **Berekeningsexpressie**.

    > [!NOTE]
    > Er kan geen berekeningsexpressie worden gedefinieerd voor de TDS-belastingcode met prioriteits-id **1**.

13. Als u de berekeningsexpressie voor de TDS-belastingcode wilt definiëren in het veld **Berekeningsexpressie**, voegt u TDS-belastingcodes toe die beschikbaar zijn op het tabblad **Belastingen**. Als u TDS-belastingcodes wilt toevoegen aan het veld **Berekeningsexpressie**, kunt u een van de volgende methoden gebruiken:

    - Sleep de vereiste belastingcode van het tabblad **Belastingen** naar het veld **Berekeningsexpressie**.
    - Dubbelklik op de vereiste belastingcode op het tabblad **Belastingen** of dubbelklik erop.
    - Selecteer de vereiste belastingcode op het tabblad **Belastingen** en houd deze vast (of klik met de rechtermuisknop) en selecteer **Belastingcode toevoegen**.

    > [!NOTE]
    > Een berekeningsexpressie invoegen vóór elke TDS-belastingcode. De TDS-belastingcodes die aan de berekeningsexpressie zijn toegevoegd, worden tussen haakjes weergegeven (\[...\]).

14. Als u de berekeningsexpressie wilt verwijderen die is gedefinieerd voor een belastingcode in het veld **Berekeningsexpressie**, selecteert u de knop **C**.
15. Als u een record op het tabblad **Berekening** wilt verwijderen, selecteert u **Verwijderen**.
16. Sluit de pagina.
