---
title: Controlebeleid voor brondocumenten definiëren
description: In dit artikel wordt beschreven hoe u controlebeleidsregels instelt en uitvoert.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8aa106cd5a5596f6b9a6663390e03ebc3f91a7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872523"
---
# <a name="define-audit-policies-for-source-documents"></a>Controlebeleid voor brondocumenten definiëren

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u controlebeleidsregels instelt en uitvoert. Het voorbeeld gebruikt onkostennota's met het type hotelkosten. Bij deze procedure wordt het demobedrijf USMF gebruikt. De auditorrol bevat de juiste machtigingen om deze taken uit te voeren.

1. Ga in het navigatievenster naar **Modules > Controleworkbench > Instellingen > Beleidsregeltype**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Regelnaam**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Onkostennotaregel** in het veld **Querynaam**.
6. Selecteer **Samenvoegen** in het veld **Querytype**.
7. Selecteer **Rechtspersoon** in het veld **Rechtspersoon**.
8. Selecteer **Wijzigingsdatum en -tijd** in het veld **Referentie documentdatum**.
9. Selecteer **Opslaan**.
10. Ga in het navigatievenster naar **Modules > Controleworkbench > Instellingen > Controlebeleid**.
11. Selecteer **Nieuw**.
12. Typ een waarde in het veld **Naam**.
13. Vouw de sectie **Beleidorganisaties** uit.
14. In de structuur selecteert u **Contoso Entertainment System USA** en vervolgens selecteert u **Toevoegen**.
15. In de structuur selecteert u **Contoso Consulting USA** en vervolgens selecteert u **Toevoegen**.
16. In de structuur selecteert u **Contoso Retail USA** en vervolgens selecteert u **Toevoegen**.
17. Vouw de sectie **Beleidorganisaties** samen.
18. Vouw de sectie **Beleidsregels** uit.
19. Zoek en selecteer in de lijst de Beleidsregel die eerder is gemaakt.
20. Selecteer **Beleidsregel maken**.
21. Voer in het veld **Ingangsdatum** een datum en tijd in.
22. Selecteer **Filter**.
23. Selecteer in de lijst de rij voor **Onkostencategorie** en stel de details in op **Hotel**.
24. Typ of selecteer een waarde in het veld **Criteria**.
25. Selecteer het tabblad **Samenvoegen**.
26. Selecteer **Toevoegen**.
27. Selecteer in de lijst een veldwaarde **Transactiebedrag**.
28. Typ of selecteer een waarde in het veld **Veld**.
29. Selecteer **Som** in het veld **AggregateFunction**.
30. Selecteer het tabblad **Groeperen op**.
31. Selecteer **Toevoegen**.
32. Selecteer een waarde voor **Werknemer** in de lijst.
33. Selecteer **Toevoegen**.
34. Selecteer een waarde voor **Onkostencategorie** in de lijst.
35. Typ of selecteer een waarde in het veld **Veld**.
36. Selecteer het tabblad **Met**.
37. Selecteer **Toevoegen**.
38. Selecteer **Transactiebedrag**.
39. Typ of selecteer een waarde in het veld **Veld**.
40. Selecteer **Som** in het veld **AggregateFunction**.
41. Typ `>2000` in het veld **Criteria**.
42. Selecteer **OK**.
43. Selecteer **Testen**.
44. Voer in het veld **Begindatum documentselectie** een datum en tijd in.
45. Voer in het veld **Einddatum documentselectie** een datum en tijd in.
46. Selecteer **Test uitvoeren**.
47. Selecteer **Controlebeleid** in het actievenster.
48. Selecteer **Aanvullende opties**.
49. Typ in het veld **Begindatum** de datum en een tijd.
50. Typ in het veld **Einddatum** de datum en een tijd.
51. Selecteer **Batch**.
52. Vouw de sectie **Op de achtergrond uitvoeren** uit.
53. Selecteer **Ja** in het veld **Batchverwerking**.
54. Selecteer **OK**.
55. Ga in het navigatievenster naar **Modules > Controleworkbench > Controlecases**.
56. Zoek en selecteer de gewenste record in de lijst.
57. Vouw de sectie **Koppelingen** uit.
58. Zoek en selecteer de gewenste record in de lijst.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
