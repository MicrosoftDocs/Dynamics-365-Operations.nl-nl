---
title: Leveranciersfactuurbeleid instellen
description: In dit onderwerp wordt uitgelegd u beleidsregels instelt voor leveranciersfacturen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441981"
---
# <a name="set-up-vendor-invoice-policies"></a>Leveranciersfactuurbeleid instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd u beleidsregels instelt voor leveranciersfacturen. Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent. U kunt tevens de workflow van de leveranciersfactuur configureren, om iedere keer wanneer u een factuur naar de workflow verzendt, leveranciersfactuurbeleid uit te voeren. 

- Beleidsregels voor leveranciersfacturen gelden niet voor facturen die in het facturenregister of facturenjournaal gemaakt zijn.  
- Valideren van factuurvereffening maakt geen gebruik van beleidsregels voor leveranciersfacturen, maar is in plaats daarvan ingesteld in de pagina Parameters van module Leveranciers.  
- Bij deze registratie wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.


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

