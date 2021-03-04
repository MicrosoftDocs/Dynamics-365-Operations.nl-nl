---
title: ER-configuraties uitvoeren in RCS en deze uploaden naar de algemene opslagplaats
description: In dit onderwerp wordt uitgelegd hoe u een configuratie voor elektronische rapportage (ER) kunt maken in Microsoft Regulatory Configuration Services (RCS) en deze kunt uploaden naar de algemene opslagplaats.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442022"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER-configuraties uitvoeren in Regulatory Configuration Services (RCS) en deze uploaden naar de algemene opslagplaats

[!include [banner](../includes/banner.md)]

U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te ontwerpen en deze zo te publiceren dat ze in uw organisatie kunnen worden gebruikt.

In de volgende procedures wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een afgeleide versie van een ER-configuratie kan maken die is geconfigureerd in een RCS-exemplaar en vervolgens de afgeleide configuratie uploaden naar de algemene opslagplaats. 

Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:

- Open een RCS-exemplaar.
- Maak een actieve configuratieprovider. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.

U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw bedrijf.

1. Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie extern** en volgt u vervolgens de instructies om een RCS-omgeving in te richten.

Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Een afgeleide versie van een configuratie maken in RCS

1. Controleer in het werkgebied **Elektronische rapportage** of u een actieve configuratieprovider hebt voor uw organisatie. 
2. Selecteer **Rapportageconfiguraties**.
3. Selecteer de configuratie waarvan u een nieuwe versie wilt afleiden. U kunt het filterveld boven de structuur gebruiken om de zoekopdracht te verfijnen.
4. Selecteer **Configuratie make** \> **Afleiden van naam**.
5. Voer een naam en omschrijving in en selecteer vervolgens **Configuratie maken** om een nieuwe afgeleide versie te maken.
6. Selecteer de nieuw afgeleide configuratie, voeg een beschrijving van de versie toe en selecteer **OK**. De status van de configuratie wordt gewijzigd in **Voltooid**.

![Nieuwe configuratieversie in RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Wanneer de configuratiestatus wordt gewijzigd, kan er een validatiefoutbericht worden weergegeven met betrekking tot de verbonden toepassingen. Als u de validatie wilt uitschakelen, selecteert u in het actievenster op het tablad **Configuraties** de optie **Gebruikersparameters** en stelt u vervolgens de optie **Validatie overslaan bij statuswijziging en rebase van configuratie** in op **Ja** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Een configuratie uploaden naar de algemene opslagplaats

Als u een nieuwe of afgeleide configuratie wilt delen met uw organisatie, kunt u deze uploaden naar de algemene opslagplaats.

1. Selecteer de voltooide versie van de configuratie en selecteer vervolgens **Uploaden naar opslagplaats**.
2. Selecteer de optie **Algemeen (Microsoft)** en selecteer vervolgens **Uploaden**.

    ![Opties voor uploaden naar opslagplaats](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Selecteer **Ja** in het venster met het bevestigingsbericht. 
4. Werk de beschrijving van de versie zo nodig bij en selecteer vervolgens **OK**. 

De status van de configuratie wordt bijgewerkt naar **Delen** en de configuratie wordt geüpload naar de algemene opslagplaats. Vervolgens kunt u er het volgende mee doen:

- Importeren in uw Dynamics 365-exemplaar. Zie [(ER) Configuraties importeren vanuit RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) voor meer informatie.
- Delen met een derde of een externe organisatie. Zie [RCS-configuraties voor elektronisch rapportage (ER) delen met externe organisaties](rcs-global-repo-share-configuration.md)

    ![Afgeleide Intrastat-configuratieversie voor Contoso in de algemene opslagplaats](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Een configuratie verwijderen uit de algemene opslagplaats
Voer de volgende stappen uit om een configuratie te verwijderen die uw organisatie heeft gemaakt.

1. Controleer in het werkgebied **Elektronische rapportage** of uw configuratieprovider **Actief** is. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
2. Selecteer voor uw actieve configuratieprovider de optie **Opslagplaats**.
3. Selecteer het type opslagplaats **Algemeen** en selecteer **Openen**.
4. Zoek op het sneltabblad **Filter** de configuratie die u wilt verwijderen met behulp van de functionaliteit **Filter**.
5. Selecteer op het sneltabblad **Versie** de versie van de configuratie die u wilt verwijderen en selecteer **Verwijderen**:

    ![Configuratie verwijderen uit algemene opslagplaats](media/RCS_Delete_from_GlobalRepo.JPG)

6. Selecteer **Ja** in het venster met het bevestigingsbericht.

    ![Bevestigingsbericht van configuratieversie verwijderen](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
De configuratieversie wordt verwijderd en er wordt een bevestigingsbericht weergegeven. 

> [!NOTE]
> Configuraties kunnen alleen worden verwijderd door de configuratieprovider die deze heeft gemaakt. Als de configuratie is gedeeld met een andere organisatie, moet het delen van de configuratie ongedaan worden maken voordat u deze kunt verwijderen.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]