---
title: Activa vanuit Leveranciers maken en aanschaffen
description: Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27ccc3b4c4f5470d3a5b8ed7347e269c6793b87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976036"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Activa vanuit Leveranciers maken en aanschaffen

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding doorloopt het maken en bijboeken van vaste activa met het inkoopproces.  Het gebruikt de accountant en Leveranciersmedewerker en het demobedrijf USMF.


## <a name="set-fixed-assets-parameters"></a>Parameters voor vaste activa instellen
1. Ga in het **navigatievenster** naar **Modules > Vaste activa > Instellingen > Parameters vaste activa**.
2. Vouw het sneltabblad **Inkooporders** uit.
3. Schakel het selectievakje **Bijboekingen van activa vanuit Inkoop toestaan** in.
4. Schakel het selectievakje **Activum maken tijdens boeken van productontvangstbon of factuur** in.

## <a name="create-a-new-vendor-invoice"></a>Een nieuwe leveranciersfactuur maken
1. Ga in het **navigatievenster** naar **Modules > Leveranciers > Werkgebieden > Leveranciersfactuurregistratie**.
2. Klik op **Nieuwe leveranciersfactuur**.
3. Klik in het veld **Factuurrekening** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een waarde in het veld **Nummer**.
6. Voer in het veld **Boekingsdatum** een datum in.
7. Klik op **Regel toevoegen**.
8. Klik in het veld **Artikelnummer** op de vervolgkeuzeknop om de zoekopdracht te openen. Of de niet-opgeslagen artikelen of de inkoopcategorieën kunnen worden gebruikt voor bijboeking van vaste activa.  
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Voer een getal in het veld **Hoeveelheid** in. Eén factuurregel maakt slechts één vast activum, ongeacht de hoeveelheid. De waarde van het veld voor de factuurhoeveelheid wordt overgebracht naar de vaste-activahoeveelheid.  
11. Voer een nummer in het veld **Eenheidsprijs** in.
12. Vouw het sneltabblad **Regeldetails** uit.
13. Klik op het tabblad **Vaste activa**.
14. Schakel het selectievakje **Een nieuw vast activum maken** in.
15. Klik in het veld **Groep vaste activa** op de vervolgkeuzeknop om de zoekopdracht te openen.
16. Selecteer in de lijst de groep vaste activa die moet worden gebruikt als de nieuwe vaste activa worden gemaakt.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik op **Boeken**. Het vaste activum wordt gemaakt en bijgeboekt wanneer de factuur wordt geboekt.  

