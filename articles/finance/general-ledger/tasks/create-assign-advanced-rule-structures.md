---
title: Geavanceerde regelstructuren maken en toewijzen
description: In dit onderwerp wordt uitgelegd hoe u een geavanceerde regelstructuur maakt en toewijst aan een rekeningstructuur.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769f3cb44830a4bc9ef48e5bcfda5a47b87954c20f65d1d3eef5d02af9ed5bd1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750407"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Geavanceerde regelstructuren maken en toewijzen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een geavanceerde regelstructuur maakt en toewijst aan een rekeningstructuur. Deze taakbegeleiding gebruikt het demobedrijf USMF.

## <a name="create-an-advanced-rule-structure"></a>Een geavanceerde regelstructuur maken
1. Ga naar **Navigatievenster > Modules > Grootboek > Rekeningschema > Structuren > Geavanceerde regelstructuren**.
2. Selecteer **Nieuw** om het uitklapvenster te openen.
3. Typ in het veld **Geavanceerde regelstructuur** een naam om de regelstructuur te beschrijven.
4. Selecteer **OK**.
5. Selecteer **Segment toevoegen**.
6. Selecteer een financiële dimensie in de lijst van segmenten. Bijvoorbeeld **Opslag**.  
7. Selecteer **Segment toevoegen**.
8. Selecteer **Activeren**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Een geavanceerde regel toepassen op een rekeningstructuur
1. Ga naar **navigatievenster > Modules > Grootboek > Rekeningschema > Structuren > Regelstructuren configureren**.
2. Zoek en selecteer in de lijst de rekeningstructuur waarop u de geavanceerde regel wilt toepassen.
3. Selecteer **Bewerken**. U kunt ook **Geavanceerde regels** selecteren, waarna u wordt gevraagd om de rekeningstructuur in de **Conceptmodus** te plaatsen.  
4. Selecteer **Geavanceerde regels**.
5. Selecteer **Nieuw** om het uitklapvenster te openen.
6. Typ een waarde in het veld **Geavanceerde regel**.
7. Typ een waarde in het veld **Naam**.
8. Selecteer **Maken**.
9. Selecteer **Nieuwe criteria toevoegen**.
10. Selecteer een hoofdrekening of financiële dimensie in het veld **Waar**.
11. Selecteer in het veld **Operator** een optie, zoals **ligt tussen** en **bevat**.
12. Typ een waarde in het veld **Waarde**.
13. Typ een waarde in het veld **Tot en met**.
14. Selecteer **Toevoegen** om het uitklapvenster te openen.
15. Zoek in de lijst de geavanceerde regelstructuur die u wilt gebruiken wanneer aan de criteria zijn voldaan.
16. Selecteer **Toevoegen**.
17. Sluit de pagina.
18. Selecteer **Activeren**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]