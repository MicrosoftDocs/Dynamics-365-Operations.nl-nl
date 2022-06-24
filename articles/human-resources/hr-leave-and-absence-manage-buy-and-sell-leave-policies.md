---
title: Beleid voor het kopen en verkopen van verlof beheren
description: In Dynamics 365 Human Resources kunt u instellen dat werknemers verlof kunnen kopen en verkopen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9db86f2a482e7a1c1eee854958cb3f097d6baf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888812"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Beleid voor verlof inkopen/verkopen beheren

>[!Important]
>De functionaliteit die in dit artikel wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt werknemers in staat stellen om verlof te kopen en te verkopen door een beleid voor het kopen en verkopen van verlof te maken. U kunt dit beleid configureren om een werkstroom voor goedkeuringen te gebruiken, maximumbedragen en -tarieven in te stellen en tarieven voor kopen en verkopen in te stellen. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Toestaan dat werknemers verlof kopen en verkopen

1. Op de pagina **Verlof- en verzuimparameters** selecteert u **Ja** voor **Werknemers toestaan om verlof te kopen** en **Werknemers toestaan om verlof te verkopen**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Een beleid voor het kopen en verkopen van verlof maken

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**. 

2. Selecteer **Beleid voor kopen en verkopen van verlof**.

3. Selecteer **Nieuw**.

4. Voer een **naam** en **omschrijving** voor het beleid in onder **Beleid voor kopen en verkopen van verlof**. 

5. Selecteer een **beleidstype**. 

   De beschikbare beleidstypen zijn **Bedrag** en **Uren per week**. Selecteer **Bedrag** om een **vast bedrag** in te voeren voor de maximumbedragen die werknemers kunnen kopen en verkopen. Als u **Uren per week** selecteert, wordt de werktijd die is gedefinieerd in de toegewezen werktijdkalender van de werknemer gebruikt om het maximumbedrag van het beleid te bepalen. 

6. Selecteer een **begindatum** en **einddatum** voor het beleid. Aanvragen om verlof te kopen of verkopen zijn alleen beschikbaar voor verzending tijdens dit tijdsbestek. 

7. Selecteer een **Werkstroom-id** voor het beleid. Bij koop- en verkoopaanvragen wordt deze werkstroom gebruikt voor controle en goedkeuring. 

8. Selecteer onder **Beleid voor kopen** de optie **Fulltime-equivalentie** (FTE) om het maximumbedrag te aan te passen aan de gedefinieerde FTE voor de functie van de werknemer. Als het type beleid **Bedrag** is, voert u een **vast maximumbedrag** in. 

9. Selecteer **Toevoegen** om de verloftypen toe te voegen die werknemers kunnen kopen. U kunt meerdere verloftypen aan het beleid toevoegen. 

10. Voer de **servicemaanden** voor het verloftype in om verschillende servicemaanden in te schakelen om het maximumbedrag te bepalen dat een werknemer kan kopen. 

11. Voer het **maximale bedrag** in voor het verloftype. 

12. Hier kunt u de **snelheid** invoeren waarmee de werknemer het verlof koopt. 

13. Voer desgewenst de **inkomstencode** in die moet worden gebruikt voor het kopen van verlof. 

14. U kunt ook instellen of FTE moet worden gebruikt om het maximumbedrag voor het verloftype te bepalen. 

15. Volg de stappen 8 tot en met 14 onder **Verkoopbeleid** om een verkoopbeleid te maken. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Het beleid voor kopen en verkopen van verlof toevoegen aan een plan voor verlof en verzuim

1. Selecteer op de pagina **Verlof en verzuim** een plan voor verlof en verzuim.

2. Selecteer onder **Regels** de optie **Beleid voor kopen en verkopen van verlof**.

## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)</br>
[Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)</br>
[Verlof- en verzuimplannen toerekenen](hr-leave-and-absence-accrue.md)</br>
[Verlof inkopen en verkopen](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
