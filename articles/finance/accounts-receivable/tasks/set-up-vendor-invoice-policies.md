---
title: Leveranciersfactuurbeleid instellen
description: In dit artikel wordt uitgelegd hoe u beleidsregels instelt voor leveranciersfacturen.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049b38b6feba5f4369d79b89b4c81a8195dd7758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904725"
---
# <a name="set-up-vendor-invoice-policies"></a>Leveranciersfactuurbeleid instellen

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u beleidsregels instelt voor leveranciersfacturen. Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina **Leveranciersfactuur** en wanneer u de leveranciersfactuurpagina **Beleidsovertredingen** opent. U kunt tevens de workflow van de leveranciersfactuur configureren, om iedere keer wanneer u een factuur naar de workflow verzendt, leveranciersfactuurbeleid uit te voeren. 

- Beleidsregels voor leveranciersfacturen gelden niet voor facturen die in het facturenregister of facturenjournaal gemaakt zijn.  
- Valideren van factuurvereffening maakt geen gebruik van beleidsregels voor leveranciersfacturen, maar is in plaats daarvan ingesteld in de pagina **Parameters van module Leveranciers**.  
- Bij deze registratie wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren. Controleer voordat u begint of de configuratiesleutel **Factuurvereffening** is geselecteerd.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Voorbereiden op het maken van leveranciersfactuurbeleid
1. Ga naar **Navigatievenster > Modules > Leveranciers > Instellen > Parameters voor Leveranciers**.
2. Selecteer het tabblad **Factuurvalidatie**.
3. Schakel het selectievakje met de status **Factuurkoptekst automatisch bijwerken** in of uit.
4. Selecteer **OK**.
5. Selecteer een optie in het veld **Factuur met verschillen boeken**.
6. Sluit de pagina.
7. Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid**.
8. Selecteer **Parameters**.
9. Selecteer **Toevoegen**.
10. Sluit de pagina om terug te keren naar de startpagina.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Typen beleidsregels voor leveranciersfacturen maken
1. Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Beleidsregeltypen voor leveranciersfactuur**.
2. Selecteer **Nieuw**.
3. Typ waarden in de velden **Regelnaam** en **Beschrijving**.
4. Selecteer in het veld **Querynaam** de vervolgkeuzeknop om de zoekopdracht te openen en selecteer de gewenste record.
5. Selecteer **Opslaan**.
6. Sluit de pagina om terug te keren naar de startpagina.

## <a name="define-a-vendor-invoice-policy"></a>Een leveranciersfactuurbeleid definiëren
1. Ga naar **Navigatievenster > Modules > Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid**.
2. Selecteer **Nieuw**.
3. Typ waarden in de velden **Naam** en **Beschrijving**.
4. Vouw de sectie **Beleidorganisaties** uit of samen.
5. In de structuur selecteert u **Contoso Entertainment System USA**.
6. Selecteer **Toevoegen**.
7. Vouw de sectie **Beleidsregels** uit of samen.
8. Selecteer **Beleidsregel maken**.
9. Typ een waarde in het veld **Beschrijving beleidsregel**.
10. Selecteer **Filter**.
11. Selecteer **Toevoegen**. Selecteer de gewenste record.
12. Typ of selecteer in de vervolgkeuzemenu's opties voor de velden **Tabel**, **Afgeleide tabel** en **Veld**.
13. Sluit de pagina.
14. Typ een waarde in het veld **Criteria**.
15. Selecteer **OK**.
16. Selecteer **OK**.
17. Sluit de pagina's om terug te keren naar de startpagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
