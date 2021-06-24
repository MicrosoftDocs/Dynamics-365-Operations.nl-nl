---
title: Vaardigheden invoeren
description: Werknemers en managers kunnen vaardigheden invoeren in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193972"
---
# <a name="enter-skills"></a>Vaardigheden invoeren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt gewenste vaardigheden of werkelijke vaardigheden voor werknemers, sollicitanten of contactpersonen invoeren in Dynamics 365 Human Resources. Een gewenste vaardigheid is een vaardigheid die een persoon van plan is te verwerven. Een werkelijke vaardigheid is een vaardigheid die iemand op dat moment heeft.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Een werkstroom maken voor het automatisch goedkeuren van vaardigheden

Als u vaardigheden wilt invoeren zonder dat deze hoeven te worden goedgekeurd, moet u een werkstroom maken om vaardigheden automatisch goed te keuren.

> [!NOTE]
> Vaardigheden die door werknemers worden ingevoerd, moeten altijd door de manager worden goedgekeurd. Met deze werkstroom worden alleen vaardigheden automatisch goedgekeurd die door managers zijn ingevoerd namens hun werknemers.

1. In de werkruimte **Personeelsbeheer** selecteert u **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Werkstromen voor Human resources**.

3. Selecteer **Nieuw**.

4. Selecteer **Werknemersvaardigheden** in het deelvenster **Werkstroom maken**.

   [![Werkstroom voor werknemersvaardigheden selecteren](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Selecteer **Openen** in het dialoogvenster **Dit bestand openen?**. Voer uw inloggegevens in wanneer dit gevraagd wordt.

6. Selecteer in de werkstroomeditor het element van de werkstroom **Vaardigheden goedkeuren** en sleep het naar het canvas.

   [![Element van werkstroom Vaardigheden goedkeuren selecteren](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Koppel het element **Begin** aan het element **Vaardigheden goedkeuren 1** en koppel het element **Vaardigheden goedkeuren 1** aan het element **Einde**. U moet mogelijk naar beneden bladeren om het element **Einde** te zien. U kunt dit element dichter naar de andere elementen slepen.

   [![Werkstroomelementen koppelen](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Dubbelklik op het element van de werkstroom **Vaardigheden goedkeuren 1** en klik vervolgens met de rechtermuisknop op het element **Stap 1**. Klik met de rechtermuisknop op het element **Stap 1** en selecteer vervolgens **Eigenschappen**.

9. Selecteer **Voorwaarde** op de linkernavigatiebalk in het venster **Eigenschappen**.

10. Selecteer **Deze stap alleen uitvoeren als aan de volgende voorwaarde wordt voldaan**.

11. Selecteer **Voorwaarde toevoegen**. Na **Waar** selecteert u **Vaardigheden selfservice werknemers** en vervolgens selecteert u **Vaardigheden selfservice werknemers.Persoon**. Na **is** selecteert u **veld** en vervolgens selecteert u **Relatie van gebruiker tot persoon.Persoon**.

    [![Voorwaarde opgeven](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Selecteer **Toewijzing** op de linkernavigatiebalk.

13. Selecteer **Hiërarchie** op het tabblad **Toewijzingstype**.

14. Selecteer **Managementhiërarchie** in het veld **Hiërarchietype:** op het tabblad **Hiërarchie selecteren**.

    [![Managementhiërarchie opgeven](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Selecteer **Sluiten**, selecteer **Werkstroom** in de canvas-breadcrumb en selecteer vervolgens **Opslaan en sluiten**.

Zie [Overzicht van werkstroomsysteem](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json) voor meer informatie over het maken van werkstromen.

## <a name="enter-skills-for-a-worker"></a>Vaardigheden voor een werknemer invoeren

1. Selecteer een werknemer.

2. Selecteer **Persoon** op de actiebalk van de pagina **Werknemer** en selecteer vervolgens **Vaardigheden**.

3. Vul op de pagina **Vaardigheden** de volgende velden in voor elke vaardigheid:

   - **Vaardigheid**: selecteer een vaardigheid.
   - **Niveautype**: selecteer **Werkelijk** voor een vaardigheid die de werknemer al heeft of selecteer **Doel** voor een vaardigheid waar de werknemer aan werkt.
   - **Niveau**: selecteer een niveau voor de vaardigheid van de werknemer.
   - **Niveaudatum**: selecteer een datum in de kalenderfunctie.
   - **Examinator**: selecteer indien van toepassing een examinator in de lijst. U kunt de zoekopdracht filteren.
   - **Jaren ervaring**: voer de jaren aan ervaring in.
   - **Geverifieerd**: als de vaardigheid is geverifieerd, schakelt u het selectievakje in.
   - **Geverifieerd door**: voer de naam van de controleur in.

4. Wanneer u klaar bent met het invoeren van vaardigheden, selecteert u **Opslaan**.

## <a name="see-also"></a>Zie ook

[Vaardigheden configureren](hr-develop-skills.md)<br>
[Vaardigheden toewijzen](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]