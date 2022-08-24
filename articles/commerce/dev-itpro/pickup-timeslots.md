---
title: Tijdvakken voor het ophalen door klanten maken en bijwerken
description: In dit artikel wordt beschreven hoe u tijdvakken voor kunt maken, configureren en bijwerken in Commerce Headquarters.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: 319b2ac2a652e633bc70c477dab52e2676c17001
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282828"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Tijdvakken voor het ophalen door klanten maken en bijwerken

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u tijdvakken voor kunt maken, configureren en bijwerken in Commerce Headquarters.

Met de tijdvakfunctie kan een detailhandelaar een tijdvak definiëren voor artikelen waarbij de klanten ervoor kunnen kiezen dit op te halen. Met tijdvakken kunnen detailhandelaren de dagen en tijden definiëren wanneer orders kunnen worden opgehaald uit een winkel. Detailhandelaren kunnen ook het aantal orders definiëren dat tijdens een bepaalde periode kan worden opgehaald. Op deze manier kunnen detailhandelaren het aantal orders beperken dat op een bepaalde dag en op een bepaalde tijd kan worden opgehaald. Het resultaat is een betere kwaliteitservaring voor klanten.

> [!NOTE]
> De tijdvakfunctie is beschikbaar in Microsoft Dynamics 365 Commerce versie 10.0.15 en hoger.

In de volgende afbeelding ziet u een voorbeeld van de tijdvakselectie tijdens e-commerce afhandeling.

![Voorbeeld van een tijdvakselectie tijdens e-commerce afhandeling.](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Eigenschappen van tijdvak

Een tijdvak is een specifieke interval waarop een klant kan kiezen om een order op te halen uit een specifieke winkel of locatie. De tijdvakfunctie is alleen beschikbaar wanneer de leveringsmethode voor klanten is geconfigureerd in Dynamics 365 Commerce.

Een tijdvak wordt gedefinieerd met behulp van de volgende eigenschappen:

- **Leverings methode** : Geef de leveringsmethode op waarop het tijdvak van toepassing is.
- **Minimum aantal dagen** en **Maximum aantal dagen** – de eerste en laatste datum opgeven die u kunt selecteren voor ophalen in relatie tot de datum waarop de order is geplaatst. 

    De eigenschap **Minimum aantal dagen** zorgt ervoor dat de detailhandelaar voldoende tijd heeft om de order te verwerken voordat deze kan worden opgehaald. De eigenschap **Maximum aantal dagen** zorgt ervoor dat de gebruiker geen datum kan selecteren die te ver in de toekomst ligt. Als de minimale waarde bijvoorbeeld is ingesteld op **1** en een order op 20 september is geplaatst, is de eerste dag dat de order kan worden opgehaald de volgende dag (21 september). Op vergelijkbare wijze kunt u, door een maximale waarde in te stellen, het maximum aantal dagen definiëren waarbinnen een order kan worden opgehaald. Wanneer de minimale en maximale waarden zijn gedefinieerd, kunnen sitegebruikers alleen een bepaalde set dagen zien en selecteren bij de kassa.

    U kunt de minimale waarde instellen op een decimale waarde die kleiner is dan 1. Als ophalen bijvoorbeeld vier uur na het plaatsen van de order beschikbaar is, stelt u de minimale waarde in op **0,17** (= 4 ÷ 24, tot op twee decimalen). Als u de minimumwaarde echter instelt op een decimale waarde van meer dan 1, wordt deze altijd afgerond op het dichtstbijgelegen hele getal. De waarde **1,2** wordt bijvoorbeeld naar boven afgerond op **2**. Ook als u de maximumwaarde instelt op een decimale waarde, wordt deze altijd afgerond op het dichtstbijgelegen hele getal. 

- **Begindatum** en **Einddatum** : Geef de begin- en einddatum van het tijdvak op. Elke tijdvakvermelding heeft een begin- en eind datum. Daarom hebt u de flexibiliteit om gedurende het hele jaar verschillende tijdvakken toe te voegen (bijvoorbeeld ophalen tijdens vakantieuren). Als de begin- en einddatum van een tijdvak wordt gewijzigd nadat een order is geplaatst, zijn de wijzigingen niet van toepassing op die order. Wanneer u begin- en einddatums definieert, moet u rekening houden met sluitingsdatums van winkels (bijvoorbeeld Kerstmis) en ervoor zorgen dat er voor deze dagen geen tijdvakken worden gedefinieerd.
- **Actieve uren voor ophalen** - Geef de periode op wanneer ophalen is toegestaan. De ophaaltijd kan bijvoorbeeld elke dag tussen 14.00 en 17.00 uur zijn. Met deze eigenschap kunnen de ophaaltijden onafhankelijk zijn van winkeluren. Daarom kan de detailhandelaar de ophaaltijden configureren zodat ze aan de specifieke bedrijfsvereisten voldoen. Wanneer u de actieve uren voor ophalen definieert, moet u rekening houden met de winkeluren en zorgen dat de ophaaltijden niet worden gedefinieerd voor momenten waarop de winkel is gesloten.

    > [!NOTE]
    > De uren voor ophalen in de winkel moeten worden gedefinieerd in de tijdzone van de toepasselijke winkel.

- **Tijdvakinterval** : Geef de duur op die aan elk tijdvak kan worden toegewezen. De duur van elk tijdvak kan bijvoorbeeld 15 minuten, 30 minuten of één uur zijn. Als het tijdvak 0 is, is het tijdvak beschikbaar voor de gehele duur tussen de begin- en eindtijd.
- **Tijdvakken per interval** : Geef het aantal klanten of orders op dat kan worden geselecteerd voor ophalen tijdens elk tijdvak. Voer bijvoorbeeld **1**, **2**, **3** of een ander geheel getal in.
- **Actieve dagen** : specificeer de dagen van de week wanneer de tijdvakken voor ophalen actief zijn. Met deze eigenschap kan de detailhandelaar de dagen definiëren waarop het ophalen van orders wordt ondersteund.
- **Detailhandelkanalen** : Geef de detailhandelkanalen op. Elk tijdvak kan aan een of meer detailhandelwinkels worden gekoppeld. Afhankelijk van de openingstijden van elke winkel kunnen een of meer tijdvakvermeldingen worden gemaakt en aan een kanaal worden gekoppeld. 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

U kunt slechts één tijdvaksjabloon per kanaal configureren. Tot deze kanalen behoren fysieke winkels, callcenters, mobiele apparaten en e-Commerce-sites.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>De functie tijdvak configureren in Commerce Headquarters

Er moeten tijdvakken worden gedefinieerd voor elke leveringsmethode in Commerce Headquarters, zodat deze kunnen worden gebruikt door POS-kanalen (Point of Sale) en e-commercekanalen.

- U kunt slechts één tijdvaksjabloon voor openingstijden aan elke winkel of kanaal koppelen.
- Elk tijdvak dat wordt gemaakt, moet uniek zijn voor elke leveringsmethode in elk sjabloon.
- Nadat de tijdvakfunctie is geconfigureerd, is de tijdvakkalender beschikbaar voor de geselecteerde winkels of winkelketens. Het is ook zichtbaar op het POS, ter referentie.

Volg deze stappen om de tijdvakfunctie te configureren in Commerce Headquarters

1. Ga naar **Commerce** \> **Kanalen instellen** \> **Tijdvakken voor ophalen in de winkel**.
1. Selecteer **Nieuw** om een nieuwe tijdvaksjabloon te maken. Als u een bestaande sjabloon wilt gebruiken, selecteert u de sjabloon in het linkerdeelvenster.
1. Geef waarden op in de velden **Tijdvak-id** en **Beschrijving**.
1. Selecteer **Ophalen order - tijdinstellingen** sneltab en vervolgens **Toevoegen**.
1. Definieer in het dialoogvenster **Ophalen order - tijdinstellingen** het datumbereik, de leveringsmethode, de actieve leveringstijd, de actieve dagen, het tijdvakinterval, de vakken per interval en andere instellingen.

    Als tijdvakken statisch zijn voor de nabije toekomst, stelt u het veld **Einddatum** in op **Nooit**.

    > [!NOTE]
    > U kunt meerdere sjablonen maken, maar slechts één sjabloon kan aan een kanaal of winkel worden gekoppeld.

    ![Het dialoogvenster Ophalen order - tijdinstellingen.](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Wanneer u klaar bent, selecteert u **OK**.
1. Als de tijdvakken op een dag variëren, maakt u extra vermeldingen op het sneltabblad **Ophalen order - tijdinstellingen** om ervoor te zorgen dat de datums en tijden elkaar niet overlappen.
1. Selecteer op het sneltabblad **Detailhandelkanalen** de optie **Toevoegen** om het tijdvaksjabloon te koppelen aan de winkels of kanalen waar deze wordt gebruikt.
1. Gebruik de pijltjestoetsen om in het dialoogvenster **Organisatieknooppunten kiezen** de winkels, regio's en organisaties waaraan de sjabloon moet worden gekoppeld te selecteren (of de selectie daarvan te wissen).

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Wanneer u klaar bent, selecteert u **OK**.
1. Voer op de pagina **Distributieplanning** de taken **1070** en **1135** uit om de gegevens te synchroniseren met de kanalen.

## <a name="time-slot-selection-for-pos-orders"></a>Selectie van tijdvak voor POS-orders

Wanneer op de POS een order of orderregel wordt geïdentificeerd voor ophalen, kan de kassamedewerker de winkel of locatie voor ophalen en een datum en een tijdvak selecteren. Als een klant een ophaalorder voor een andere winkel heeft, kan de kassamedewerker datums selecteren wanneer het artikel kan worden opgehaald in die winkel. Het zoekresultaat van de winkel bevat een verwijzing naar de datums en openingstijden.

In de volgende afbeelding ziet u een voorbeeld van de tijdvakselectie voor een POS-order.

![Een voorbeeld van een tijdvakselectie voor een POS-order.](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Selectie van tijdvak voor e-commerce-orders

Zie de [Module ophaalinformatie](../pickup-info-module.md) voor meer informatie over het beschikbaar stellen van tijdvakken voor e-commerce-orders.

> [!NOTE]
> Gebruikers kunnen tijdvakken op de uitcheckpagina van een commercesite alleen weergeven of bewerken als de Ophaalinformatiemodule is toegevoegd aan die pagina. Als de uitcheckpagina niet de Ophaalinformatiemodule bevat, worden de orders geplaatst zonder dat gebruikers de tijdvakgegevens kunnen opgeven of weergeven.

In de volgende afbeelding ziet u een voorbeeld van een e-commerce-order waar een tijdvak voor ophalen is geselecteerd.

![Voorbeeld van een e-commerce-order waarvoor een tijdvak voor ophalen is geselecteerd.](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Selectie van tijdvak voor callcenterorders

In de callcenter-app kunnen callcentermedewerkers de ophaalwinkel of -locatie selecteren, evenals een datum en een tijdvak, zoals in de volgende afbeelding is aangegeven.

![Voorbeeld van een callcenterorder waarvoor een tijdvak voor ophalen is geselecteerd.](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Module met afhaalinformatie](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
