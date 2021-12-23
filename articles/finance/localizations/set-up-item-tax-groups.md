---
title: Belastinggroepen voor artikelen instellen
description: In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor artikelen instelt in de service voor belastingberekening.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883851"
---
# <a name="set-up-item-tax-groups"></a>Belastinggroepen voor artikelen instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u belastinggroepen voor artikelen instelt in de service voor belastingberekening. Daarnaast wordt uitgelegd hoe u de matrix voor regels voor toepasbaarheid van de belastinggroep voor artikelen instelt en regels in de matrix configureert.

Het concept van belastinggroepen voor artikelen in de service voor belastingberekening lijkt op het concept van btw-groepen voor artikelen in Microsoft Dynamics 365 Finance. Dit zijn groepen belastingcodes. De service voor belastingberekening gebruikt de doorsnede van een belastinggroep en een artikelbelastinggroep om de belastingcodes te bepalen.

> [!IMPORTANT]
> De instelling van belastinggroepen voor artikelen in de service voor belastingberekening is onafhankelijk van rechtspersoon. U kunt deze configuratie maar één keer voltooien in RCS (Regulatory Configuration Service). Als u de service voor belastingberekening inschakelt in Finance, worden belastinggroepen voor artikelen automatisch gesynchroniseerd voor de geselecteerde rechtspersoon.

## <a name="set-up-an-item-tax-group"></a>Een belastinggroep voor artikelen instellen 

Ga als volgt te werk om een belastinggroep voor artikelen in te stellen:

1. Meld u aan bij [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Ga in naar **Werkruimten** \> **Globaliseringsfuncties** \> **Belastingberekening**.
3. Selecteer de functie en versie die u wilt instellen en selecteer **Bewerken**.
4. Selecteer **Configuratieversie** op het tabblad **Algemeen**.
5. Selecteer **Kolom beheren** op het tabblad **Artikelbelastinggroep**. Als u voor het eerst een artikelbelastinggroep instelt, worden de velden in het dialoogvenster **Kolom beheren** automatisch ingesteld.
6. Vouw in de lijst aan de linkerkant het knooppunt **Regels** uit en schakel het selectievakje voor **Artikelbelastinggroep** in.

    ![Artikelbelastinggroep geselecteerd onder het knooppunt Regels in het dialoogvenster Kolommen beheren.](media/select-item-tax-group.png)

7. Selecteer de pijl-rechts om **Artikelbelastinggroep** toe te voegen aan de lijst **Geselecteerde kolommen** rechts.

    ![Artikelbelastinggroep toegevoegd aan de lijst Geselecteerde kolommen.](media/add-item-tax-group.png)

8. Selecteer **OK**.

## <a name="configure-an-item-tax-group"></a>Een belastinggroep voor artikelen configureren

Nadat u een artikelbelastinggroep hebt ingesteld, wordt de matrix voor regels voor toepasbaarheid van de belastinggroep gemaakt. U kunt regels aan de matrix toevoegen om de artikelbelastinggroep te configureren.

1. Selecteer op het tabblad **Artikelbelastinggroep** de optie **Toevoegen**.
2. Voer in het veld **Artikelbelastinggroep** de naam van de artikelbelastinggroep in.

    > [!IMPORTANT]
    > U wordt aangeraden de naam van de artikelbelastinggroep te beperken tot tien tekens. Deze naam wordt gesynchroniseerd met Finance, dat een limiet van tien tekens kent voor de namen van artikelbelastinggroepen.

3. Schakel in het veld **Belastingcodes** het selectievakje in voor elke belastingcode die u in de artikelbelastinggroep wilt opnemen. U kunt meerdere belastingcodes opnemen in één artikelbelastinggroep.

    ![Meerdere belastingcodes geselecteerd in het veld Belastingcodes.](media/multiple-tax-codes-selection.png)

4. Herhaal stap 1 tot en met 3 als u nog meer artikelbelastinggroepen wilt toevoegen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
