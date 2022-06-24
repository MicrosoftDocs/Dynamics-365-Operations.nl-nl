---
title: ER-configuraties in RCS/de algemene opslagplaats delen met externe organisaties
description: In dit artikel wordt uitgelegd hoe u ER-configuraties (elektronische rapportage) in Microsoft Regulatory Configuration Services (RCS)/de algemene opslagplaats rechtstreeks met externe organisaties kunt delen.
author: JaneA07
ms.date: 05/04/2020
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
ms.openlocfilehash: 976a86aee75581d1afa764bea049b6c0eaecf9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888918"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>ER-configuraties (elektronische rapportage) in Microsoft Regulatory Configuration Services (RCS) algemene opslagplaats met externe organisaties delen

[!include [banner](../includes/banner.md)]

U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om configuraties voor elektronische rapportage (ER) te delen en deze vervolgens te publiceren naar externe organisaties.

In de volgende procedures wordt uitgelegd hoe een RCS-gebruiker een versie van een ER-configuratie die is geconfigureerd in een RCS-exemplaar kan delen met een externe organisatie. Voordat u deze procedures kunt uitvoeren, moet u eerst aan de volgende vereisten voldoen:

- Open een RCS-exemplaar.
- Maak een actieve configuratieprovider. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
- Maak en upload een nieuwe versie van een ER-configuratie. Zie [Een nieuwe versie van een ER-configuratie (elektronische rapportage) maken en uploaden](rcs-global-repo-upload.md) voor meer informatie.

U moet er ook voor zorgen dat een RCS-omgeving wordt ingericht voor uw bedrijf.

1. Ga in een Finance and Operations-app naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie extern** en volgt u vervolgens de instructies om een RCS-omgeving in te richten.

Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.

## <a name="verify-the-configuration-that-you-want-to-share"></a>De configuratie controleren die u wilt delen

Voer de volgende stappen uit om te controleren of de configuratie die u wilt delen al is geüpload naar de algemene opslagplaats.

1. Selecteer in het werkgebied **Elektronische rapportage** de optie **Opslagplaatsen** voor uw configuratieprovider.

    ![Configuratieproviders.](media/1_RCS_Repo_for_config_provider.JPG)

2. Selecteer **Algemene opslagplaats** \> **Openen**.
3. Zoek naar de configuratie die u wilt delen. U kunt het filterveld gebruiken om de zoekopdracht te verfijnen. Als u de configuratie niet kunt vinden in de algemene opslagplaats, volgt u de stappen in [Een nieuwe versie van een ER-configuratie (elektronische rapportage) maken en uploaden](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>ER-configuraties delen met externe organisaties

Nadat u een configuratie hebt gemaakt onder uw configuratieprovider, kunt u deze rechtstreeks delen met externe organisaties via het sneltabblad **Gedeeld met** op de pagina **Algemene opslagplaats voor configuratie**.

1. Selecteer in het werkgebied **Elektronische rapportage** de optie **Opslagplaatsen** voor uw configuratieprovider.
2. Selecteer **Algemene opslagplaats** \> **Openen**. 
3. Selecteer de configuratie die u wilt delen.
4. Selecteer op het sneltabblad **Gedeeld met** de optie **Organisatie**.

    ![Sneltabblad Gedeeld met.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. Voer in het dialoogvenster de domeinnaam in voor de externe organisatie en selecteer vervolgens **OK**.

    ![Dialoogvenster Configuratieversie delen met externe organisatie.](media/1_RCS_Repo_for_Share_with_form.JPG)

De configuratie wordt gedeeld met de externe organisatie en is beschikbaar voor die organisatie in de algemene opslagplaats. Hier kan het worden geïmporteerd in het exemplaar van RCS of in de exemplaren van apps voor financiën en bedrijfsactiviteiten van de organisatie.

6. Als u het delen van een configuratie die eerder met een externe organisatie is gedeeld ongedaan wilt maken, selecteert u de configuratie en klikt u op **Delen ongedaan maken**. Selecteer vervolgens **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]