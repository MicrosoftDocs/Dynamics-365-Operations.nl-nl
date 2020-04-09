---
title: Uitzonderingen onderzoeken of oplossen
description: Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 995d68f6224b6dfbb1928c907ad991b86fc47668
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140347"
---
# <a name="research-or-resolve-exceptions"></a>Uitzonderingen onderzoeken of oplossen

[!include [banner](../../includes/banner.md)]

Beleidsregels voor leveranciersfacturen worden uitgevoerd wanneer u een leveranciersfactuur boekt met behulp van de pagina Leveranciersfactuur en wanneer u de leveranciersfactuurpagina Beleidsovertredingen opent. U kunt tevens de workflow van de leveranciersfactuur configureren, om iedere keer wanneer u een factuur naar de workflow verzendt, leveranciersfactuurbeleid uit te voeren. 

Beleidsregels voor leveranciersfacturen gelden niet voor facturen die in het facturenregister of facturenjournaal gemaakt zijn. 

Valideren van factuurvereffening maakt geen gebruik van beleidsregels voor leveranciersfacturen, maar is in plaats daarvan ingesteld in de pagina Parameters van module Leveranciers.

Bij deze registratie wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Voorbereiden op het maken van leveranciersfactuurbeleid
1. Ga naar Leveranciers > Instellingen > Parameters van module Leveranciers.
2. Klik op het tabblad Factuurvalidatie.
3. Selecteer het selectievakje Status factuurkoptekst automatisch bijwerken in of uit.
4. Klik op OK.
5. Selecteer een optie in het veld Factuur met verschillen boeken.
6. Sluit de pagina.
7. Ga naar Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid.
8. Klik op Parameters.
9. Klik op btnAdd.
10. Sluit de pagina.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Typen beleidsregels voor leveranciersfacturen maken
1. Ga naar Leveranciers > Beleidsinstelling > Beleidsregeltypen voor leveranciersfactuur.
2. Klik op Nieuw.
3. Typ een waarde in het veld Regelnaam.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Querynaam op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik op Opslaan.
9. Sluit de pagina.

## <a name="define-a-vendor-invoice-policy"></a>Een leveranciersfactuurbeleid definiëren
1. Ga naar Leveranciers > Beleidsinstelling > Leveranciersfactuurbeleid.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ een waarde in het veld Omschrijving.
5. Vouw de sectie Beleidorganisaties uit of samen.
6. In de structuur selecteert u "Contoso-entertainmentsysteem USA".
7. Klik op Toevoegen.
8. Vouw de sectie Beleidsregels uit of samen.
9. Klik op Beleidsregel maken.
10. Typ een waarde in het veld Beschrijving beleidsregel.
11. Klik op Filter.
12. Klik op Toevoegen.
13. Markeer in de lijst de geselecteerde rij.
14. Klik in het veld Tabel op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
16. Klik in het veld Afgeleide tabel op de vervolgkeuzeknop om de zoekopdracht te openen.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik in het veld Veld op de vervolgkeuzeknop om de zoekopdracht te openen.
19. Typ een waarde in het veld Veld.
20. Sluit de pagina.
21. Typ een waarde in het veld Criteria.
22. Klik op OK.
23. Klik op OK.
24. Sluit de pagina.
25. Sluit de pagina.

