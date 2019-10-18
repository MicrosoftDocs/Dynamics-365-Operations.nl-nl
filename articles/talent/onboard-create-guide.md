---
title: Een onboardinghandleiding maken en verzenden met Dynamics 365 Talent - Onboard
description: In dit onderwerp wordt uitgelegd hoe u de Microsoft-app Dynamics 365 Talent - Onboard gebruikt om een onboardinghandleiding voor uw nieuwe medewerkers te maken. Deze taak is een essentiële eerste stap in een HCM-strategie (Human Capital Management) voor aanstelling tot pensionering.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4dbfcc3b3fd611eea36109a516a7b9361a9f654
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009849"
---
# <a name="create-and-send-an-onboarding-guide"></a>Een onboardinghandleiding maken en verzenden

[!include [banner](includes/banner.md)]

Met Microsoft Dynamics 365 Talent: Onboard kunt u onboardinghandleidingen maken op basis van sjablonen die u zelf hebt gemaakt, van sjablonen die beschikbaar zijn in een galerie of helemaal opnieuw.

Nadat u een onboardinghandleiding hebt gemaakt, kunt u deze verzenden naar een nieuwe medewerker. U kunt deze ook verzenden naar meerdere nieuwe medewerkers die u kunt opgeven in een Microsoft Excel-bestand dat u downloadt vanuit de Onboard-app.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Een onboardinghandleiding maken op basis van een sjabloon en deze verzenden naar een nieuwe medewerker

1. Selecteer **Sjablonen** in het linkermenu.
2. Selecteer onder **Mijn sjablonen** de sjabloon die u wilt instellen als onboardinghandleiding voor de nieuwe medewerker.
3. Bewerk de sjabloon naar wens. Sla uw werk regelmatig op.
4. Wanneer u klaar bent met het bewerken van de sjabloon, selecteert u **Handleiding maken**.

    [![Een onboardinghandleiding maken op basis van een sjabloon](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Voer in het venster **Een handleiding maken** onder **Wie wilt u onboarden** de naam of het e-mailadres van de nieuwe medewerker in. Als de nieuwe medewerker nog niet in het systeem is opgenomen, selecteert u **Nu toevoegen** en voert u de gegevens van de werknemer in.

    ![[Gegevens invoeren voor de onboardinghandleiding](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Selecteer een begindatum onder **Wanneer beginnen ze**.
7. Als de onboardinghandleiding automatisch op een bepaalde datum moet worden verzonden naar de nieuwe medewerker, moet u ervoor zorgen dat de optie **Een automatische verzenddatum plannen** is ingeschakeld en selecteert u vervolgens de automatische verzenddatum. Als u de handleiding onmiddellijk wilt verzenden, schakelt u de optie **Een automatische verzenddatum plannen** uit.
8. Selecteer **Gereed**.
9. Wanneer u klaar bent met het bewerken van de onboardinghandleiding, selecteert u **Verzenden** in de rechterbovenhoek. Voer vervolgens een van deze stappen uit:

    - Als u de nieuwe medewerker een koppeling naar de onboardinghandleiding wilt sturen, selecteert u **kopieer een koppeling** en vervolgens **Kopiëren**.
    - Als u de e-mail voor de onboardinghandleiding wilt aanpassen voordat u deze verzendt, selecteert u **E-mailbericht aanpassen voordat het wordt verzonden** en **Volgende**, past u de e-mail naar wens aan en selecteert u vervolgens **Verzenden**.
    - Als u de e-mail wilt verzenden zonder deze aan te passen, selecteert u **Volgende** en selecteert u vervolgens **Verzenden**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Een onboardinghandleiding maken op basis van een sjabloon en deze verzenden naar meerdere nieuwe medewerkers

Met Onboard kunt u een onboardinghandleiding naar meerdere nieuwe medewerkers tegelijkertijd verzenden.

1. Selecteer **Sjablonen** in het linkermenu.
2. Selecteer onder **Mijn sjablonen** de sjabloon die u wilt instellen als onboardinghandleiding voor de nieuwe medewerkers.
3. Bewerk de sjabloon naar wens. Sla uw werk regelmatig op.
4. Wanneer u klaar bent met het bewerken van de sjabloon, selecteert u **Handleiding maken**.
5. In het venster **Een handleiding maken** selecteert u **Wilt u meerdere mensen tegelijk onboarden**.

    [![Een onboardinghandleiding maken voor meerdere nieuwe medewerkers](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Selecteer **sjabloon voor nieuw aangenomen werknemers**.
7. Nadat het XLSX-bestand is gedownload, selecteert u **Openen**, voert u de gegevens van de medewerkers in de Excel-werkmap in en slaat u de werkmap op.

    [![De Excel-sjabloon downloaden om de onboardinghandleiding naar meerdere nieuwe medewerkers te verzenden](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Voordat u de werkmap kunt bewerken, moet u de optie **Bewerken inschakelen** inschakelen in Excel.
    > 
    > [![Bewerken inschakelen](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Sleep de Excel-werkmap naar het aangewezen gebied in het venster **Meerdere handleidingen maken** of klik op een willekeurige plaats in dat gebied om het bestand op uw computer te zoeken.

    [![De bewerkte werkmap slepen](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Wanneer u klaar bent met het bewerken van de onboardinghandleiding, selecteert u **Verzenden** in de rechterbovenhoek. Voer vervolgens een van deze stappen uit:

    - Als u de nieuwe medewerkers een koppeling naar de onboardinghandleiding wilt sturen, selecteert u **kopieer een koppeling** en vervolgens **Kopiëren**.
    - Als u de e-mail voor de onboardinghandleiding wilt aanpassen voordat u deze verzendt, selecteert u **E-mailbericht aanpassen voordat het wordt verzonden** en **Volgende**, past u de e-mail naar wens aan en selecteert u vervolgens **Verzenden**.
    - Als u de e-mail wilt verzenden zonder deze aan te passen, selecteert u **Volgende** en selecteert u vervolgens **Verzenden**.

## <a name="create-a-guide-without-using-a-template"></a>Een handleiding maken zonder een sjabloon te gebruiken

U hoeft een handleiding niet altijd op basis van een sjabloon te maken. U kunt in plaats hiervan ook zelf een handleiding maken.

1. Selecteer in het linkermenu de optie **Handleidingen** en selecteer vervolgens de knop **Toevoegen** (het plusteken \[**+**\]).
2. Voer in het venster **Een handleiding maken** onder **Wie wilt u onboarden** de naam of het e-mailadres van de nieuwe medewerker in. Als de nieuwe medewerker nog niet in het systeem is opgenomen, selecteert u **Nu toevoegen** en voert u de gegevens van de werknemer in.

    ![[Gegevens invoeren voor de onboardinghandleiding](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Selecteer een begindatum onder **Wanneer beginnen ze**.
4. Als de onboardinghandleiding automatisch op een bepaalde datum moet worden verzonden naar de nieuwe medewerker, moet u ervoor zorgen dat de optie **Een automatische verzenddatum plannen** is ingeschakeld en selecteert u vervolgens de automatische verzenddatum. Als u de handleiding onmiddellijk wilt verzenden, schakelt u de optie **Een automatische verzenddatum plannen** uit.
5. Selecteer **Gereed**.

## <a name="save-a-guide-as-a-template"></a>Een handleiding als een sjabloon opslaan

U kunt een onboardinghandleiding opslaan als een sjabloon. Op deze manier kunt u tijd besparen wanneer u later meer onboardinghandleidingen moet maken.

1. Selecteer **Handleidingen** in het linkermenu.
2. Selecteer de knop **Meer** (het weglatingsteken \[**...**\]) voor de handleiding waarvan u een sjabloon wilt maken en selecteer vervolgens **Opslaan als sjabloon**.

    ![[Een onboardinghandleiding opslaan als een sjabloon](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Voer in het venster **Opslaan als een nieuwe sjabloon** een naam voor de nieuwe sjabloon in en selecteer vervolgens **Opslaan**.

## <a name="next-steps"></a>Volgende stappen

- [Onboardinghandleidingen en -sjablonen bewerken](./onboard-edit-guides-templates.md)
- [Inhoud delen met andere bijdragers](./onboard-share-template.md)
- [De status van taken en onboardingmedewerkers weergeven](./onboard-view-status.md)
- [Aanstellingsteams maken in Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Zie ook

- [De Onboard-app uitproberen of kopen](https://dynamics.microsoft.com/talent/onboard/)
- [Nieuwe functies](./whats-new.md)
- [Opmerkingen bij release](https://docs.microsoft.com/business-applications-release-notes/index)
- [Ondersteuning](./talent-support.md)
