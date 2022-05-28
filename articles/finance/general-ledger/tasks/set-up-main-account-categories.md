---
title: Categorieën van hoofdrekening instellen
description: In dit onderwerp wordt uitgelegd hoe u hoofdrekeningcategorieën instelt in Dynamics 365 Finance.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb41f1b7200363f8846c406d5c20338f6ea242bd
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721977"
---
# <a name="set-up-main-account-categories"></a>Categorieën van hoofdrekening instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u hoofdrekeningcategorieën instelt. De categorieën van hoofdrekening worden gebruikt voor de standaardrapporten in de financiële rapportage en in Power BI. U kunt de categorieën van hoofdrekening die standaard zijn gemaakt een andere naam geven maar niet verwijderen. De categorieën van aanvullende rekening kunnen worden gemaakt en gebruikt voor rapportage- en analysedoeleinden. In dit onderwerp wordt het demobedrijf USMF gebruikt.

## <a name="create-a-main-account-category"></a>Een categorie van hoofdrekening maken
1. Ga in het navigatievenster naar **Modules > Grootboek > Rekeningschema > Rekeningen > Categorieën van hoofdrekening**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Categorie van hoofdrekening** een unieke naam in.
4. Typ in het veld **Beschrijving** een beschrijving voor de categorie van de hoofdrekening.
5. Selecteer in het veld **Hoofdrekeningtype** het hoofdrekeningtype dat u aan de categorie wilt koppelen.

## <a name="link-main-accounts-to-account-category"></a>Hoofdrekeningen aan een rekeningcategorie koppelen
1. Klik op **Hoofdrekeningen koppelen**.
2. Selecteer in de lijst de hoofdrekeningen die u aan de hoofdrekeningcategorie wilt toewijzen door de selectievakjes in de kolom **Gekoppeld** in te schakelen. Door het toewijzen van hoofdrekeningen aan een categorie van hoofdrekening worden de saldi van de rekeningen samengevoegd wanneer die categorie voor financiële rapportage en analyse wordt gebruikt.  
3. Schakel de optie **Gekoppeld** in of uit om de hoofdrekeningen te kiezen.
4. Selecteer **OK**.
5. Selecteer **Ja**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
