---
title: Grootboekvereffeningen
description: In dit onderwerp wordt uitgelegd hoe u de grootboekvereffeningspagina gebruikt om grootboektransacties te vereffenen en vereffeningen om te keren.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977114"
---
# <a name="ledger-settlements"></a>Grootboekvereffeningen

[!include [banner](../includes/banner.md)]

Met grootboekvereffeningen kunt u debet- en credittransacties in het grootboek afstemmen en markeren als vereffend. Op deze manier kunt u ervoor zorgen dat verwante transacties zijn gewist. U kunt ook vereffeningen omkeren als deze per ongeluk zijn aangebracht.

## <a name="enable-advanced-ledger-settlements"></a>Geavanceerde grootboekvereffeningen inschakelen

De pagina geavanceerde grootboekvereffeningen biedt extra mogelijkheden voor filteren en selecteren van transacties. Als u geavanceerde grootboekvereffeningen wilt inschakelen, volgt u deze stappen.

1. Selecteer **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**. 
2. Stel op het tabblad **Grootboekvereffeningen** de optie **Geavanceerde grootboekvereffening** in op **Ja** om de geavanceerde grootboekvereffening in te schakelen. De pagina **Geavanceerde grootboekvereffeningen** wordt gebruikt wanneer u **Grootboekvereffeningen** selecteert in de **periodieke taken**. 
3. U moet de lijst met rekeningen invoeren die moeten worden gebruikt voor grootboekvereffeningen voor elk rekeningschema. Deze lijst wordt gebruikt voor het filteren van de transacties die worden weergegeven op de pagina **Grootboekvereffeningen**. Selecteer in de lijst **Rekeningschema's** een rekeningschema en selecteer vervolgens **Nieuw** om nieuwe rekeningen aan de lijst toe te voegen.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Transacties vereffenen met behulp van de pagina Geavanceerde grootboekvereffeningen

Als u grootboektransacties wilt vereffenen, voert u de volgende stappen uit.

1. Selecteer **Grootboek** \> **Periodieke taken** \> **Grootboekvereffeningen**.
2. Stel de filters bovenaan de pagina in:

    - Selecteer een datumbereik of selecteer **Datumintervalcode** om automatisch het datumbereik in te vullen.
    - Wijzig de boekingslaag desgewenst.
    - Als u de grootboekrekening en dimensies afzonderlijk wilt weergeven, selecteert u een financiële dimensieset.

3. Selecteer **Transacties weergegeven** om alle transacties weer te geven die overeenkomen met de filters die u hebt ingesteld, en de lijst met rekeningen die u hebt opgegeven toen u het rekeningschema instelde in de vorige sectie. Als u een van de filters of de dimensiesets wijzigt, moet u **Transacties weergegeven** opnieuw selecteren.
4. Selecteer een of meer regels die u voor vereffening overweegt. De waarde van het veld **Geselecteerd bedrag** boven aan de pagina wordt verhoogd of verlaagd met het totale bedrag op de regels die u hebt geselecteerd.
5. Nadat u klaar bent met het selecteren van transacties, selecteert u **Selectie markeren**. Er wordt een vinkje weergegeven in de kolom **Gemarkeerd** voor elke transactie die u hebt geselecteerd. De waarde van het veld **Gemarkeerd bedrag** boven aan het raster wordt bovendien verhoogd of verlaagd met het totale bedrag op de regels die u hebt gemarkeerd.
6. Wanneer de waarde **Gemarkeerd bedrag** **0** (nul) is, selecteert u **Gemarkeerde transacties vereffenen**. De status van de gemarkeerde transacties wordt bijgewerkt in **Vereffend**.

## <a name="make-transactions-easier-to-find"></a>Transacties eenvoudiger te vinden maken

De pagina **Grootboekvereffeningen** bevat mogelijkheden waardoor het gemakkelijker wordt om de transacties te zien die u nodig hebt voor vereffening.

- De knop **Markering van selectie opheffen** wist het veld **Gemarkeerd** voor alle regels die zijn geselecteerd.
- Met het filter **Gemarkeerd** kunt u transacties filteren op basis van de vraag of het veld **Gemarkeerd** voor hen is geselecteerd of gewist.
- Met het filter **Status** kunt u transacties filteren op de vraag of de status ervan **Vereffend** of **Niet vereffend** is.
- Met de knop **Sorteren op absoluut bedrag** sorteert u de bedragen op absolute waarde, zodat u debet- en creditbedragen kunt groeperen die dezelfde waarde hebben.

## <a name="reverse-a-settlement"></a>Een vereffening omkeren

U kunt een vereffening omkeren die ten onrechte is aangebracht.

1. Volg stap 1 tot en met 3 in de sectie 'Transacties vereffenen met behulp van de pagina Geavanceerde grootboekvereffeningen' om de transacties weer te geven die u zoekt.
2. Selecteer in het filter **Status** **Vereffend**.
3. Selecteer een of meer regels die u voor omkering overweegt. De waarde van het veld **Geselecteerd bedrag** boven aan de pagina wordt verhoogd of verlaagd met het totale bedrag op de regels die u hebt geselecteerd.
4. Nadat u klaar bent met het selecteren van transacties, selecteert u **Selectie markeren**. Er wordt een vinkje weergegeven in de kolom **Gemarkeerd** voor elke transactie die u hebt geselecteerd. De waarde van het veld **Gemarkeerd bedrag** boven aan de pagina wordt bovendien verhoogd of verlaagd met het totale bedrag op de regels die u hebt gemarkeerd.
5. Wanneer de waarde **Gemarkeerd bedrag** **0** (nul) is, selecteert u **Gemarkeerde transacties omkeren**. De status van de gemarkeerde transacties wordt bijgewerkt in **Niet vereffend**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>De lijst met rekeningen bijwerken die zijn opgenomen in de lijst met transacties

Selecteer **Rekeningen voor grootboekvereffeningen** om een dialoogvenster te openen waarin u de rekeningen kunt bewerken die zijn opgenomen in de lijst met transacties. Selecteer **Nieuw** om nieuwe rekeningen aan de lijst toe te voegen. Deze lijst wordt gebruikt voor het filteren van de transacties die worden weergegeven op de pagina **Grootboekvereffeningen**.
