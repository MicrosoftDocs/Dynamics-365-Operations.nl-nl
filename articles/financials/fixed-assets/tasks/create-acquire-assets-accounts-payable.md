---
title: Activa vanuit Leveranciers maken en aanschaffen
description: Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562456"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Activa vanuit Leveranciers maken en aanschaffen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.  Het gebruikt de accountant en Leveranciersmedewerker en het demobedrijf USMF.


## <a name="set-fixed-assets-parameters"></a>Parameters voor vaste activa instellen
1. Ga naar Vaste activa > Instellen > Parameters vaste activa.
2. Vouw de sectie Inkooporders uit of samen.
3. Schakel het selectievakje Bijboekingen van activa vanuit Inkoop toestaan in.
4. Schakel het selectievakje Activum maken tijdens boeken van productontvangstbon of factuur in.

## <a name="create-a-new-vendor-invoice"></a>Een nieuwe leveranciersfactuur maken
1. Ga naar Leveranciers > Werkruimten > Leveranciersfactuurregistratie.
2. Klik op Nieuwe leveranciersfactuur.
3. Klik in het veld Factuurrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een waarde in het veld Nummer.
6. Voer in het veld Boekingsdatum een datum in.
7. Klik op Regel toevoegen.
8. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Of de niet-opgeslagen artikelen of de inkoopcategorieën kunnen worden gebruikt voor bijboeking van vaste activa.  
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Voer in het veld Hoeveelheid een getal in.
    * Eén factuurregel maakt slechts één vast activum, ongeacht de hoeveelheid.  De waarde van het veld voor de factuurhoeveelheid wordt overgebracht naar de vaste-activahoeveelheid.  
11. Voer in het veld Eenheidsprijs een getal in.
12. Vouw de sectie Regeldetails uit of samen.
13. Klik op het tabblad Vaste activa.
14. Schakel het selectievakje Een nieuw vast activum maken in.
15. Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.
16. Selecteer in de lijst de groep vaste activa die moet worden gebruikt als de nieuwe vaste activa worden gemaakt.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik op Boeken.
    * Het vaste activum wordt gemaakt en bijgeboekt wanneer de factuur wordt geboekt.  

