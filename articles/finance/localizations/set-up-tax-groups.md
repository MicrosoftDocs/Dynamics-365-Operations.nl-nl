---
title: Belastinggroepen instellen
description: In dit onderwerp wordt uitgelegd hoe u belastinggroepen instelt in de service voor belastingberekening.
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
ms.openlocfilehash: 50abafb958edfb8476434ff5842cd84cb186962f
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883853"
---
# <a name="set-up-tax-groups"></a>Belastinggroepen instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u belastinggroepen instelt in de service voor belastingberekening. Daarnaast wordt uitgelegd hoe u de matrix voor regels voor toepasbaarheid van de belastinggroep instelt en regels in de matrix configureert.

Het concept van belastinggroepen in de service voor belastingberekening lijkt op het concept van btw-groepen in Microsoft Dynamics 365 Finance. Dit zijn groepen belastingcodes. De service voor belastingberekening gebruikt de doorsnede van een belastinggroep en een artikelbelastinggroep om de belastingcodes te bepalen.

Belastinggroepen in de service voor belastingberekening verschillen echter van btw-groepen in Finance omdat er geen aanvullende parameters voor bestaan, zoals **Gebruiksbelasting** en **Vrijstellingsbelasting**. In plaats daarvan zijn deze parameters beschikbaar op het niveau van de belastingcode.

> [!IMPORTANT]
> De instelling van belastinggroepen in de service voor belastingberekening is onafhankelijk van rechtspersoon. U kunt deze configuratie maar één keer voltooien in RCS (Regulatory Configuration Service). Als u de service voor belastingberekening inschakelt in Finance, worden belastinggroepen automatisch gesynchroniseerd voor de geselecteerde rechtspersoon.

## <a name="set-up-a-tax-group"></a>Een belastinggroep instellen

Ga als volgt te werk om een belastinggroep in te stellen.

1. Meld u aan bij [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Ga in naar **Werkruimten** \> **Globaliseringsfuncties** \> **Belastingberekening**.
3. Selecteer de functie en versie die u wilt instellen en selecteer **Bewerken**.
4. Selecteer **Configuratieversie** op het tabblad **Algemeen**.
5. Selecteer **Kolom beheren** op het tabblad **Belastinggroep**. Als u voor het eerst een belastinggroep instelt, worden de velden in het dialoogvenster **Kolom beheren** automatisch ingesteld.
6. Vouw in de lijst aan de linkerkant het knooppunt **Regels** uit en schakel het selectievakje voor **Belastinggroep** in.

    ![Belastinggroep geselecteerd onder het knooppunt Regels in het dialoogvenster Kolommen beheren.](media/select-tax-group.png)

7. Selecteer de pijl-rechts om **Belastinggroepen** toe te voegen aan de lijst **Geselecteerde kolommen** rechts.

    ![Belastinggroep toegevoegd aan de lijst Geselecteerde kolommen.](media/add-tax-group.png)

8. Selecteer **OK**.

## <a name="configure-a-tax-group"></a>Een belastinggroep configureren

Nadat u een belastinggroep hebt ingesteld, wordt de matrix voor regels voor toepasbaarheid van de belastinggroep gemaakt. U kunt regels aan de matrix toevoegen om de belastinggroep te configureren.

1. Selecteer op het tabblad **Belastinggroep** de optie **Toevoegen**.
2. Voer in het veld **Belastinggroep** de naam van de belastinggroep in.

    > [!IMPORTANT]
    > U wordt aangeraden de naam van de belastinggroep te beperken tot tien tekens. Deze naam wordt gesynchroniseerd met Finance, dat een limiet van tien tekens kent voor de namen van belastinggroepen.

3. Schakel in het veld **Belastingcodes** het selectievakje in voor elke belastingcode die u in de belastinggroep wilt opnemen. U kunt meerdere belastingcodes opnemen in één belastinggroep.

    ![Meerdere belastingcodes geselecteerd in het veld Belastingcodes.](media/multiple-tax-codes-selection.png)

4. Herhaal stap 1 tot en met 3 als u nog meer belastinggroepen wilt toevoegen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
