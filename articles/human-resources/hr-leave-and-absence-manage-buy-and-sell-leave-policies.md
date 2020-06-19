---
title: Beleid voor het kopen en verkopen van verlof beheren
description: In Dynamics 365 Human Resources kunt u instellen dat werknemers verlof kunnen kopen en verkopen.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429008"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Beleid voor het kopen en verkopen van verlof beheren

[!include [banner](includes/preview-feature.md)]

U kunt instellen dat werknemers verlof kunnen kopen door een beleid voor het kopen van verlof te maken.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Toestaan dat werknemers verlof kopen en verkopen

1. Op de pagina **Verlof- en verzuimparameters** selecteert u **Ja** voor **Werknemers toestaan om verlof te kopen**. 

## <a name="create-a-buy-leave-policy"></a>Een beleid voor het kopen van verlof maken

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**. 

2. Selecteer **Beleid voor kopen en verkopen van verlof**.

3. Selecteer **Nieuw**.

4. Voer een **naam** en **omschrijving** voor het beleid in onder **Beleid voor kopen en verkopen van verlof**. 

5. Selecteer een **beleidstype**. 

   De beschikbare beleidstypen zijn **Bedrag** en **Uren per week**. Selecteer **Bedrag** om een **vast bedrag** in te voeren voor de maximumbedragen die werknemers kunnen kopen en verkopen. Als u **Uren per week** selecteert, wordt de werktijd die is gedefinieerd in de toegewezen werktijdkalender van de werknemer gebruikt om het maximumbedrag van het beleid te bepalen. 

6. Selecteer een **begindatum** en **einddatum** voor het beleid. Aanvragen om verlof te kopen of verkopen zijn alleen beschikbaar voor verzending tijdens dit tijdsbestek. 

7. Selecteer onder **Beleid voor kopen** de optie **Fulltime-equivalentie** (FTE) om het maximumbedrag te aan te passen aan de gedefinieerde FTE voor de functie van de werknemer. Als het type beleid **Bedrag** is, voert u een **vast maximumbedrag** in. 

8. Selecteer **Toevoegen** om de verloftypen toe te voegen die werknemers kunnen kopen. U kunt meerdere verloftypen aan het beleid toevoegen. 

9. Voer de **servicemaanden** voor het verloftype in om verschillende servicemaanden in te schakelen om het maximumbedrag te bepalen dat een werknemer kan kopen. 

10. Voer het **maximale bedrag** in voor het verloftype. 

11. Hier kunt u de **snelheid** invoeren waarmee de werknemer het verlof koopt. 

12. Voer desgewenst de **inkomstencode** in die moet worden gebruikt voor het kopen van verlof. 

13. U kunt ook instellen of FTE moet worden gebruikt om het maximumbedrag voor het verloftype te bepalen. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Het beleid voor kopen en verkopen van verlof toevoegen aan een plan voor verlof en verzuim

1. Selecteer op de pagina **Verlof en verzuim** een plan voor verlof en verzuim.

2. Selecteer onder **Regels** de optie **Beleid voor kopen en verkopen van verlof**.

## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)</br>
[Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)</br>
[Verlof- en verzuimplannen toerekenen](hr-leave-and-absence-accrue.md)</br>
[Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)

