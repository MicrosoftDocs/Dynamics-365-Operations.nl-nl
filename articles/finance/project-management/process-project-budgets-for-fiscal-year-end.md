---
title: Projectbudgetten aan het einde van het fiscale jaar overboeken
description: Dit artikel bevat informatie over het overboeken van resterende budgetbedragen naar toekomstige jaren en het maken van budgetregisterdetails.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172325"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projectbudgetten aan het einde van het fiscale jaar overboeken

[!include [banner](../includes/banner.md)]

Wanneer u aan een meerjarig project werkt, hebt u mogelijk resterend budget aan het einde van het fiscale jaar. U kunt de resterende budgetbedragen naar een toekomstig jaar overboeken en budgetregisterdetails voor de bedragen maken in de bijbehorende grootboekrekeningen. Voordat u de resterende bedragen transporteert, kunt u de resterende budgetbedragen controleren en analyseren.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Resterende budgetbedragen controleren en analyseren

Voltooi de volgende stappen als u de budgetbedragen aan het einde van het jaar voor projecten wilt controleren, maar de bedragen niet wilt transporteren.

1. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Budgetten** > **Budgetten transporteren**. 
2. Controleer op de pagina **Transportproces van het projectbudget** op het tabblad **Opties voor jaareinde** of **Resterende projectbudgetbedragen overboeken** niet is ingeschakeld.
3. Selecteer op het tabblad **Parameters** in het veld **Projectbudgetjaar** het fiscale jaar waarvoor u het resterende budgetbedrag wilt weergeven. 
4. Selecteer in het veld **Boekjaar openen** het fiscale jaar waarvoor u het resterende budgetbedrag wilt weergeven. 
5. Selecteer in het veld **Van prognosemodel** de optie **Resterend budget**. 
6. Als u projecten wilt opnemen die aan de geselecteerde criteria voldoen en geen resterend budget hebben, selecteert u **Nul rest weergeven** weergeven.  
7. Selecteer op het tabblad **Budgetten selecteren** de optie **Alle budgetten ophalen** om alle budgetten te laden die met uw geselecteerde criteria overeenkomen en selecteer vervolgens **Verwerken**. 
8. Als u een databasequery wilt ontwerpen die een specifieke reeks budgetten in het deelvenster laadt, selecteert u **Geselecteerde budgetten ophalen**.

Voor meer informatie over een specifieke regel in het deelvenster selecteert u de regel en vervolgens selecteert u **Budgetdetails weergeven** of **Rekeningen weergeven**.

## <a name="carry-forward-remaining-budget-amounts"></a>Resterende budgetbedragen transporteren 

Wanneer u resterende budgetbedragen verwerkt, kunt u transacties in het grootboek maken voor de bedragen die u transporteert. Als u grootboektransacties wilt maken, voert u de stappen in de sectie [Budgetbedragen transporteren en grootboektransacties maken](#carry-forward) uit. 

> [!NOTE]
> Budgetbedragen die worden getransporteerd, worden overgeboekt naar een prognosemodel dat als transportprognosemodel is geselecteerd op de pagina **Prognosemodellen**.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budgetbedragen transporteren en grootboektransacties maken

1.  Selecteer **Projectbeheer en boekhouding** > **Periodiek** > **Budgetten** > **Budgetten transporteren**. 
2. Selecteer op de pagina **Transportproces van het projectbudget** de optie **Jaarafsluiting** en schakel **Resterende projectbudgetbedragen overboeken** en **Budgetregisterposten in grootboek maken**. 
3. Selecteer op het tabblad **Parameters** in de veldgroep **Projectparameters** het volgende:

   - **Projectbudgetjaar**: selecteer de start van het fiscale jaar waarvoor u de resterende budgetbedragen wilt weergeven. 
   - **Winst en verlies**: maak winst- en verliestransacties in het grootboek. 
   -  **OHW**: maak OHW-transacties (onderhanden werk) in het grootboek.
   -  **Salaris**: maak salaristoewijzingstransacties in het groot boek. 

5. Voer in de veldengroep **Grootboek** de volgende gegevens in: 

   - Selecteer in het veld **Boekjaar openen** het fiscale jaar waarnaar u de resterende budgetbedragen voor de projecten wilt overboeken. De standaardwaarde is één jaar na de waarde van het veld **Projectbudgetjaar**.
   -  Selecteer in het veld **Overboekingsperiode** de periode waarvoor u de budgetregisterdetails in het grootboek wilt maken. Dit is normaal gezien de eerste periode in het nieuwe fiscaal jaar.

6. Voer in de veldengroep **Kopiëren van/naar** de volgende gegevens in:

   - Selecteer in het veld **Van prognosemodel** het projectbudgetprognosemodel dat gekoppeld is aan de resterende budgetbedragen die u voor de projecten wilt overboeken. 
   - Selecteer in het veld **Naar grootboekbudgetmodel** het grootboekbudgetmodel dat is gekoppeld aan de resterende budgetbedragen die u naar het grootboek wilt overboeken. 
   -  Vink het selectievakje **Verkoopvaluta overboeken** aan om de verkoopvaluta van het project te gebruiken voor de grootboektransacties die worden gemaakt wanneer u de budgetbedragen voor de projecten overboekt. Als de optie niet is geselecteerd, worden voor de transacties de valuta voor boekhouding gebruikt. 
   -  Selecteer **Nul rest weergeven** als u projecten wilt opnemen waarvoor geen resterende budgetbedragen zijn, maar die voldoen aan de andere criteria die u selecteert in de projecten die in het onderste deelvenster worden weergegeven.

7. Selecteer op het tabblad **Budgetten selecteren** de optie **Alle budgetten ophalen** om alle budgetten te laden die met uw geselecteerde criteria overeenkomen. Als u liever een databasequery ontwerpt die een specifieke reeks projectbudgetten in het deelvenster laadt, selecteert u **Geselecteerde budgetten ophalen**.
8. Selecteer de optie voor elk project dat u wilt verwerken aan het begin van de regel voor het project.

    > [!TIP]
    > Als u alle of de meeste projecten wilt selecteren, schakelt u het selectievakje in de linkerbovenhoek in. Als u de verwerking van een project wilt uitsluiten, schakelt u het selectievakje voor dat project uit.

9. Selecteer **Verwerken** om de resterende budgetbedragen voor de geselecteerde projecten naar het geselecteerde boekjaar over te boeken en budgetregisterdetails in het grootboek te maken.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budgetbedragen transporteren zonder grootboektransacties te maken

1. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Budgetten** > **Budgetten transporteren**.
2. Selecteer op de pagina **Transportproces van het projectbudget** in het veld **Opties voor jaareinde** de optie **Resterende projectbudgetbedragen overboeken**.
3. Selecteer in de groep **Parameters** in het veld **Projectbudgetjaar** het fiscale jaar waarvoor u de resterende budgetbedragen wilt weergeven.
4. Voer in de groep **Kopiëren van/naar** de volgende gegevens in:

   - Selecteer in het veld **Van prognosemodel** het projectbudgetprognosemodel dat gekoppeld is aan de resterende budgetbedragen die u voor de projecten wilt overboeken. 
   - Als u projecten wilt opnemen die aan de geselecteerde criteria voldoen en geen resterende budgetbedragen hebben, selecteert u **Nul rest weergeven** weergeven.
   - Selecteer in de groep **Budgetten selecteren** de optie **Alle budgetten ophalen** om alle budgetten te laden die met uw geselecteerde criteria overeenkomen. Als u een databasequery wilt ontwerpen die een specifieke reeks projectbudgetten in het deelvenster laadt, selecteert u **Geselecteerde budgetten ophalen**.

5. Selecteer de optie voor elk project dat u wilt verwerken aan het begin van de regel voor het project. 
6. Selecteer **Verwerken** om de resterende budgetbedragen voor de geselecteerde projecten naar het geselecteerde boekjaar te transporteren.

