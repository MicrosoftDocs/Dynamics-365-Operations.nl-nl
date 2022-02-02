---
title: ER-configuraties uitvoeren in RCS en deze uploaden naar de algemene opslagplaats
description: In dit onderwerp wordt uitgelegd hoe u een configuratie voor elektronische rapportage (ER) kunt maken in Microsoft Regulatory Configuration Services (RCS) en deze kunt uploaden naar de algemene opslagplaats.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: eb04362d6d7261af56d2940b085fbc8d43c9d662
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965084"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-configuraties uitvoeren in Regulatory Configuration Services (RCS) en deze uploaden naar de algemene opslagplaats

[!include [banner](../includes/banner.md)]

U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te ontwerpen en deze zo te publiceren dat ze in uw organisatie kunnen worden gebruikt.

In de volgende procedures wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een afgeleide versie van een ER-configuratie kan maken die is geconfigureerd in een RCS-exemplaar en vervolgens de afgeleide configuratie uploaden naar de algemene opslagplaats. 

Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:

- Krijg toegang tot een RCS-omgeving voor uw organisatie.
- Een configuratieprovider maken en deze actief maken. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.

U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw organisatie. Als u geen RCS-instantie hebt ingericht voor uw organisatie, kunt u dit doen met behulp van de volgende stappen:

1. Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer in **Gerelateerde/externe koppelingen** **Regulatory services - configuratie** en volg de instructies om u **aan te melden** om deze in te richten.

Als er al een RCS-omgeving is ingericht voor uw organisatie, gebruikt u de pagina-URL om deze te openen en de **aanmeldingsoptie** te selecteren.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Een afgeleide versie van een configuratie maken in RCS

> [!NOTE]
> Als u voor het eerst RCS gebruikt, is er voor u geen configuratie beschikbaar. U moet een configuratie importeren uit de Algemene opslagplaats. Meer informatie is te vinden in [ER-configuraties downloaden uit de Algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Meld u aan** bij RCS en selecteer het werkgebied **Elektronische rapportage**.
2. Controleer of u een actieve configuratieprovider hebt voor uw organisatie die is ingesteld op actief (zie vereisten). 
3. Selecteer **Rapportageconfiguraties**.
4. Selecteer de configuratie waarvan u een nieuwe versie wilt afleiden. U kunt het filterveld boven de structuur gebruiken om de zoekopdracht te verfijnen.
5. Selecteer **Configuratie make** \> **Afleiden van naam**.
6. Voer een naam en omschrijving in en selecteer vervolgens **Configuratie maken** om een nieuwe afgeleide versie met de status Concept te maken.
7. Selecteer de zojuist afgeleide configuratie en breng indien nodig extra wijzigingen in de configuratie. 
8. Nadat uw wijzigingen zijn voltooid, moet u **Status wijzigen** voor de configuratie op **Voltooid** instellen om deze naar de opslagplaats te kunnen publiceren. Selecteer **OK**.

![Nieuwe configuratieversie in RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Wanneer de configuratiestatus wordt gewijzigd, kan er een validatiefoutbericht worden weergegeven met betrekking tot de verbonden toepassingen. Als u de validatie wilt uitschakelen, selecteert u in het actievenster op het tablad **Configuraties** de optie **Gebruikersparameters** en stelt u vervolgens de optie **Validatie overslaan bij statuswijziging en rebase van configuratie** in op **Ja** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Een configuratie uploaden naar de algemene opslagplaats

Als u een nieuwe of afgeleide configuratie wilt delen met uw organisatie, kunt u deze als volgt uploaden naar de algemene opslagplaats:

1. Selecteer de voltooide versie van de configuratie en selecteer vervolgens **Uploaden naar opslagplaats**.
2. Selecteer de optie **Algemeen (Microsoft)** en selecteer vervolgens **Uploaden**.

    ![Opties voor uploaden naar opslagplaats.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Selecteer **Ja** in het venster met het bevestigingsbericht. 
4. Werk de beschrijving van de versie zo nodig bij en selecteer vervolgens **OK**. U kunt de versie optioneel ook uploaden naar een verbonden toepassing of naar een GIT-opslagplaats.  

De status van de configuratie wordt bijgewerkt naar **Gedeeld** en de configuratie wordt geüpload naar de algemene opslagplaats. Er wordt ook een conceptversie van de geüploade configuratie gemaakt en deze kan worden gebruikt als u de volgende wijzigingen wilt aanbrengen.

Nadat de configuratie naar de Algemene opslagplaats is geüpload, kunt u er op de volgende manieren mee werken:

- Importeren in uw Dynamics 365-exemplaar. Zie [(ER) Configuraties importeren vanuit RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) voor meer informatie.
- Delen met een derde of een externe organisatie. Zie [RCS-configuraties voor elektronisch rapportage (ER) delen met externe organisaties](rcs-global-repo-share-configuration.md)

    ![Afgeleide Intrastat-configuratieversie voor Contoso in de algemene opslagplaats.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Een configuratie verwijderen uit de algemene opslagplaats
Voer de volgende stappen uit om een configuratie te verwijderen die uw organisatie heeft gemaakt.

1. Controleer in het werkgebied **Elektronische rapportage** of uw configuratieprovider **Actief** is. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
2. Selecteer voor uw actieve configuratieprovider de optie **Opslagplaats**.
3. Selecteer het type opslagplaats **Algemeen** en selecteer **Openen**.
4. Zoek op het sneltabblad **Filter** de configuratie die u wilt verwijderen met behulp van de functionaliteit **Filter**.
5. Selecteer op het sneltabblad **Versie** de versie van de configuratie die u wilt verwijderen en selecteer **Verwijderen**:

    ![Configuratie verwijderen uit algemene opslagplaats.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Selecteer **Ja** in het venster met het bevestigingsbericht.

    ![Bevestigingsbericht van configuratieversie verwijderen.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
De configuratieversie wordt verwijderd en er wordt een bevestigingsbericht weergegeven. 

> [!NOTE]
> Configuraties kunnen alleen worden verwijderd door de configuratieprovider die deze heeft gemaakt. Als de configuratie is gedeeld met een andere organisatie, moet het delen van de configuratie ongedaan worden maken voordat u deze kunt verwijderen.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
