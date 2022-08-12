---
title: Ondersteuning voor belastingfunctie voor transferorders
description: In dit artikel wordt de ondersteuning voor de nieuwe belastingfunctie met behulp van de service voor belastingberekening uitgelegd.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b611abb2d68d93178d0c26ba40b22f1b8d26b191
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203104"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Ondersteuning voor belastingfunctie voor transferorders

[!include [banner](../../includes/banner.md)]

In dit artikel vindt u informatie over belastingberekening en boekingsintegratie in transferorders. Met deze functionaliteit kunt u belastingberekening en boekingen in transferorders instellen voor voorraadtransfers. Volgens de btw-regelgeving van de Europese Unie (EU) worden voorraadtransfers beschouwd als intracommunautaire leveringen en intracommunautaire verwervingen.

Als u deze functionaliteit wilt configureren en gebruiken, moet u drie hoofdstappen uitvoeren:

1. **RCS-instellingen**: stel in Regulatory Configuration Service de belastingfunctie, belastingcodes en toepasbaarheid van belastingcodes in die moeten worden gebruikt voor de bepaling van belastingcodes in transferorders.
2. **Dynamics 365 Finance instellen:** schakel in Finance de functie **Belasting in transferorder** in, stel de serviceparameters voor belastingberekening voor voorraad in en stel kernbelastingparameters in.
3. **Voorraadinstellingen**: stel de voorraadconfiguratie in voor transferordertransacties.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>RCS instellen voor belasting- en transferordertransacties

Volg deze stappen om de belasting voor een transferorder in te stellen. In het voorbeeld dat hier wordt weergegeven, gaat het om een transferorder van Nederland naar België.

1. Selecteer op de pagina **Belastingfuncties** op het tabblad **Versies** de conceptfunctieversie en selecteer vervolgens **Bewerken**.

2. Selecteer **Toevoegen** op het tabblad **Belastingcodes** op de pagina **Belastingfuncties instellen** om nieuwe belastingcodes te maken. Voor dit voorbeeld worden drie belastingcodes gemaakt: **NL-Vrijgesteld**, **BE-RC-21** en **BE-RC+21**.

    - Wanneer een transferorder vanuit een magazijn in Nederland wordt verzonden, wordt de Nederlandse code voor vrijgestelde btw (**NL-Vrijgesteld**) toegepast.
      
        Maak de belastingcode **NL-Vrijgesteld**.
        1. Selecteer **Toevoegen** en voer **NL-Vrijgesteld** in het veld **Belastingcode** in.
        2. Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.
        3. Selecteer **Opslaan**.
        4. Selecteer **Toevoegen** in de tabel **Tarief**.
        5. Stel **Is vrijgesteld** in op **Ja** in de sectie **Algemeen**.
        6. Voer in het veld **Vrijstellingscode** de waarde **EC** in.

    - Wanneer een transferorder wordt ontvangen in een Belgisch magazijn, wordt het terugboekingsmechanisme toegepast op basis van de belastingcodes **BE-RC-21** en **BE-RC+21**.
        
        Maak de belastingcode **BE-RC-21**.      
        1. Selecteer **Toevoegen** en voer **BE-RC-21** in het veld **Belastingcode** in.
        2. Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.
        3. Selecteer **Opslaan**.
        4. Selecteer **Toevoegen** in de tabel **Tarief**.
        5. Voer **-21** in het veld **Belastingtarief** in.
        6. Stel **Is terugboeking** in op **Ja** in de sectie **Algemeen**.
        7. Selecteer **Opslaan**.
        
        Maak de belastingcode **BE-RC+21**.
        1. Selecteer **Toevoegen** en voer **BE-RC-21** in het veld **Belastingcode** in.
        2. Selecteer **Op nettobedrag** in het veld **Belastingcomponent**.
        3. Selecteer **Opslaan**.
        4. Selecteer **Toevoegen** in de tabel **Tarief**.
        5. Voer **21** in het veld **Belastingtarief** in.
        6. Selecteer **Opslaan**.

3. Definieer de belastinggroep.
    1. Selecteer **Kolommen beheren** en selecteer vervolgens het regelveld **Btw-groep**.
    2. Selecteer **->** en vervolgens **OK**.
    3. Selecteer **Toevoegen** om een btw-groep toe te voegen.
    4. Voer in de kolom **Btw-groep** de optie **AR-EU** in en selecteer vervolgens de belastingcode **NL-Vrijstelling**.
    5. Selecteer **Toevoegen** om een btw-groep toe te voegen.
    6. Voer in de kolom **Btw-groep** de optie **RC-VAT** in en selecteer de belastingcodes **BE-RC-21** en **BE-RC+21**.
4. Definieer de artikelbelastinggroep.
    1. Selecteer **Kolommen beheren** en selecteer vervolgens het regelveld **Artikelbelastinggroep**.
    2. Selecteer **->** en **OK**.
    3. Selecteer **Toevoegen** om een artikelbelastinggroep toe te voegen.
    4. Geef **VOLLEDIG** op in de kolom **Artikelbelastinggroep**. Selecteer belastingcodes **BE-RC-21**, **BE-RC+21** en **NL-Vrijgesteld**.
5. Definieer de toepasbaarheid van de belastinggroep.

    1. Selecteer **Kolommen beheren** en selecteer vervolgens kolommen die moeten worden gebruikt om de toepasbaarheidstabel te maken.

        > [!NOTE]
        > Zorg ervoor dat u de kolommen **Bedrijfsproces** en **Belastingrichtingen** aan de tabel toevoegt. Beide kolommen zijn essentieel voor de belastingfunctionaliteit in transferorders.

    2. Voeg toepasbaarheidsregels toe. Laat het veld **Belastinggroep** niet leeg.
        
        Voeg een nieuwe regel toe voor de transferorderzending.
        1. Selecteer **Toevoegen** in de tabel **Toepasbaarheidsregels**.
        2. Selecteer **Voorraad** in het veld **Bedrijfsproces** om de regel van toepassing te maken voor een transferorder.
        3. Voer **NLD** in het veld **Land/regio van oorsprong** in.
        4. Voer **BEL** in het veld **Land/regio van verzending** in.
        5. Selecteer **Uitvoer** in het veld **Belastingrichting** om de regel van toepassing te maken op de verzending van transferorders.
        6. Selecteer in het veld **Belastingroep** de optie **AR-EU**.
        
        Voeg nog een regel toe voor de transferorderontvangst.
        
        1. Selecteer **Toevoegen** in de tabel **Toepasbaarheidsregels**.
        2. Selecteer **Voorraad** in het veld **Bedrijfsproces** om de regel van toepassing te maken voor een transferorder.
        3. Voer **NLD** in het veld **Land/regio van oorsprong** in.
        4. Voer **BEL** in het veld **Land/regio van verzending** in.
        5. Selecteer **Invoer** in het veld **Belastingrichting** om de regel van toepassing te maken op de ontvangst van transferorders.
        6. Selecteer in het veld **Belastingroep** de optie **RC-VAT**.

6. Definieer de toepasbaarheid van de artikelbelastinggroep.

    1. Selecteer **Kolommen beheren** en selecteer vervolgens kolommen die moeten worden gebruikt om de toepasbaarheidstabel te maken.
    2. Voeg toepasbaarheidsregels toe.
        
       > [!NOTE]
       > Als de standaard btw-groep voor artikelen op de regels van uw belastbare documenten correct is, laat u deze matrix leeg. 
        
        Voeg een nieuwe regel toe voor de transferorderzending en -ontvangst.
        1. Selecteer op de pagina **Toepasbaarheidsregels** de optie **Toevoegen**.
        2. Selecteer in het veld **Bedrijfsproces** de optie **Voorraad** om de regel van toepassing te maken voor de transferorder.
        3. Selecteer in het veld **Artikelbelastingroep** de optie **VOLLEDIG**.
7. Voltooi en publiceer de nieuwe versie van de belastingfunctie.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Finance instellen voor belasting- en transferordertransacties

Voer de volgende stappen uit om belastingen voor transferorders in te stellen.

1. Ga in Finance naar **Werkruimten** > **Functiebeheer**.
2. Selecteer de functie **Belasting in transferorder** in de lijst en selecteer **Nu inschakelen** om deze in te schakelen.

    > [!IMPORTANT]
    > De functie **Belasting in transferorder** is volledig afhankelijk van de belastingberekeningsservice. Daarom kan deze alleen worden ingeschakeld als u de belastingberekeningsservice hebt geïnstalleerd.

    ![De functie Belasting in transferorder.](../media/image7.png)

3. Schakel de belastingberekeningsservice in en selecteer het bedrijfsproces **Voorraad**.

    > [!IMPORTANT]
    > U moet deze stap voltooien voor elke rechtspersoon in Finance waarvoor de belastingberekeningsservice en de functionaliteit voor belasting in transferorders beschikbaar moeten zijn.

    1. Ga naar **Belasting** > **Instellingen** > **Belastingconfiguratie** > **Parameters voor belastingberekening**.
    2. Selecteer **Voorraad** in het veld **Bedrijfsproces**.

4. Controleer of het teruboekingsmechanisme is ingesteld. Ga naar **Grootboek** \> **Instellingen** \> **Parameters** en controleer vervolgens op het tabblad **Terugboeking** of de optie **Terugboeking inschakelen** is ingesteld op **Ja**.

    ![De optie Terugboeking inschakelen.](../media/image9.png)

5. Controleer of de gerelateerde belastingcodes, belastinggroepen, artikelbelastinggroepen en btw-registratienummers in Finance zijn ingesteld volgens de richtlijnen van de belastingberekeningsservice.
6. Stel een tussentijdse transitrekening in. Deze stap is alleen vereist wanneer de belasting die wordt toegepast op een overdrachtsorder niet van toepassing is op een mechanisme voor vrijgestelde belastingen of terugboeking.

    1. Ga naar **Belasting** > **Instellingen** > **Btw** > **Grootboekboekingsgroepen**.
    2. Selecteer een grootboekrekening in het veld **Tussentijds transit**.

       ![Een tussentijdse transitrekening selecteren.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Basisvoorraad instellen voor belasting- en transferordertransacties

Volg deze stappen om basisvoorraad in te stellen om transferordertransacties mogelijk te maken.

1. Maak verzend- en doellocaties in verschillende landen of regio's voor uw magazijnen en voeg het primaire adres voor elke locatie toe.

    1. Ga naar **Magazijnbeheer** > **Instellingen** > **Magazijn** > **Vestigingen**.
    2. Selecteer **Nieuw** om de vestiging te maken die u later aan een magazijn toewijst.
    3. Herhaal stap 2 voor alle andere vestigingen die u moet maken.

    > [!NOTE]
    > Een van de vestigingen die u maakt, moet **Transit** heten. In latere stappen van deze procedure wijst u deze vestiging toe aan het transitmagazijn, zodat btw-gerelateerde voorraadboekstukken kunnen worden geboekt in verzend- en ontvangsttransacties voor transferorders. Het adres van de transitvestiging is niet relevant voor belastingberekening. U kunt dit veld daarom leeg laten.

    ![Vestigingen instellen.](../media/image11.png)

2. Maak verzend-, transit- en doelmagazijnen. Alle adresgegevens die in een magazijn worden bijgehouden, overschrijven het vestigingsadres tijdens de belastingberekening.

    1. Ga naar **Magazijnbeheer** > **Instellen** > **Magazijn** > **Magazijnen**.
    2. Selecteer **Nieuw** om een magazijn te maken en deze aan de bijbehorende vestiging toe te wijzen.
    3. Herhaal stap 2 om naar behoefte een magazijn voor elke vestiging te maken.

       ![Magazijnen instellen.](../media/image12.png)

    > [!NOTE]
    > Voor een verzendmagazijn moet een transitmagazijn worden geselecteerd in het veld **Transitmagazijn** voor transferordertransacties.
    >
    > ![Een transitmagazijn selecteren.](../media/image13.png)

3. Verifieer of de voorraadboekingsconfiguratie is ingesteld voor transferordertransacties.

    1. Ga naar **Voorraadbeheer** > **Instellen** > **Boeken** > **Boeken**.
    2. Controleer op het tabblad **Voorraad** of er een grootboekrekening is ingesteld voor de boekingen **Voorraaduitgifte** en **Voorraadontvangst**.

        ![De boeking van voorraaduitgifte en voorraadontvangst instellen.](../media/image14.png)

    3. Controleer of er een grootboekrekening is ingesteld voor de boeking **Inter-unit te betalen**.

        ![De boeking Inter-unit te betalen instellen.](../media/image15.png)

    4. Controleer of er een grootboekrekening is ingesteld voor de boeking **Inter-unit te ontvangen**.

        ![De boeking Inter-unit te ontvangen instellen.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
