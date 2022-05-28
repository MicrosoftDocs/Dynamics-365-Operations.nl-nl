---
title: Belastingconfiguraties aanpassen voor het opzoeken van hoofdgegevens
description: In dit onderwerp wordt uitgelegd hoe u belastingconfiguraties kunt aanpassen om de zoekfunctionaliteit van hoofdgegevens uit te breiden.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689123"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Belastingconfiguraties aanpassen voor het opzoeken van hoofdgegevens

[!include [banner](../includes/banner.md)]

Neem de stappen in dit onderwerp om belastingconfiguraties aan te passen om de zoekfunctionaliteit van hoofdgegevens uit te breiden.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Een belastingconfiguratie importeren die door Microsoft is geleverd

1. Selecteer in Regulatory Configuration Service (RCS) in de werkruimte **Elektronische rapportage** de configuratieprovider **Microsoft**.
2. Selecteer **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer vervolgens **Openen**.
4. Selecteer een belastingconfiguratie, zoals **Belastingberekeningsconfiguratie** en selecteer vervolgens een versie op het tabblad **Versies**.
5. Selecteer **Importeren**.

> [!NOTE]
> Standaard wordt de Dataverse-modeltoewijzing geïmporteerd. Als u waarschuwingsberichten ontvangt tijdens het importeren van configuraties, moet u de virtuele entiteiten in Dataverse inschakelen. Zie [Virtuele Dataverse-entiteiten inschakelen](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md) voor meer informatie.

## <a name="create-a-customized-data-model-configuration"></a>Een aangepaste configuratie voor een gegevensmodel maken

1. Selecteer in de werkruimte **Elektronische rapportage** de optie **Belastingconfiguraties** en selecteer vervolgens de configuratie van het gegevensmodel die u wilt uitbreiden. Selecteer bijvoorbeeld **Gegevensmodel voor belastingberekening**.
2. Selecteer **Configuratie maken**.
3. Selecteer **Belastbaar documentmodel afgeleid van naam: gegevensmodel voor belastingberekening, Microsoft**.
4. Voer in het veld **Naam** **Gegevensmodel voor aanpassing** in.
5. Selecteer **Configuratie maken**.

## <a name="create-customized-reference-models"></a>Aangepaste referentiemodellen maken

1. Selecteer op de pagina **Belastingconfiguraties** de optie **Gegevensmodel voor aanpassing** en selecteer vervolgens **Ontwerper**.
2. Selecteer de knop met het weglatingsteken (**...**) en selecteer vervolgens de weergave **Referentiemodel**.

    [![Referentiemodel.](./media/pic2.png)](./media/pic2.png)

3. Het aangepaste referentiemodel maken. Het aangepaste model is een hoofdmodel. De aangepaste entiteit is een recordlijst. Het aangepaste veld is een tekenreeksveld dat u wilt gebruiken in de zoekopdracht. U kunt zo nodig meer velden toevoegen.
4. Selecteer de knop met het weglatingsteken (**...**) en selecteer vervolgens de weergave **Belastbaar document**.
5. Selecteer het kenmerk dat u aan het aangepaste referentiemodel wilt koppelen. Selecteer bijvoorbeeld **Aangepast kenmerk** en ga dan als volgt te werk:

    1. Selecteer **Referentiemodel selecteren**.
    2. Selecteer **Aangepast model** en selecteer **OK**. De naam van het referentiemodel wordt bijgewerkt naar de waarde van het veld **Natuurlijke sleutel**.

        [![Het dialoogvenster Referentiemodel selecteren.](./media/pic5.png)](./media/pic5.png)

    3. Selecteer **Opslaan** en vervolgens **Voltooien**.

## <a name="create-a-customized-model-mapping-configuration"></a>Een aangepaste configuratie voor modeltoewijzing maken

1. Selecteer in de werkruimte **Elektronische rapportage** de optie **Belastingconfiguraties** en selecteer vervolgens de configuratie **Dataverse-modeltoewijzing**.
2. Selecteer in het veld **Standaard voor modeltoewijzing** de waarde **Nee**.
3. Selecteer **Configuratie maken**.
4. Selecteer **Belastbare documentmodeltoewijzing afgeleid van naam: Dataverse-modeltoewijzing, Microsoft**.
5. Voer in het veld **Naam** **Modeltoewijzing voor aanpassing** in.
6. Selecteer in het veld **Doelmodel** het gegevensmodel **Gegevensmodel voor aanpassen**.
7. Selecteer **Configuratie maken**.

    [![Het vervolgkeuzemenu Configuratie maken.](./media/pic6.png)](./media/pic6.png)

8. Selecteer **Modeltoewijzing voor aanpassing** en stel het veld **Gekoppelde toepassing** in op de verbinding die is gemaakt in stap 8 in [Een omgeving instellen voor het opschonen van hoofdgegevens](tax-service-set-up-environment-master-data-lookup.md)hoofdgegevens.
9. Stel het veld **Standaard voor modeltoewijzing** in op **Ja**.

## <a name="create-customized-model-mappings"></a>Aangepaste modeltoewijzingen maken

1. Selecteer op de pagina **Belastingconfiguraties** de optie **Modeltoewijzing voor aanpassing**.
2. Selecteer **Ontwerper** en selecteer vervolgens **Aanpassingsmodel**.

    [![Aanpassingsmodel.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Een modeltoewijzing aan een Dataverse-entiteit toewijzen

1. Selecteer op de pagina **Ontwerper modeltoewijzing** de optie **Aanpassingsmodel** en selecteer vervolgens **Ontwerper**.
2. Selecteer in de boomstructuur **Typen gegevensbronnen** de optie **Dataverse-tabel**.
3. Selecteer op het tabblad **Gegevensbronnen** de optie **Basis toevoegen**.
4. Voer in het veld **Naam** de optie **Aangepast Dataverse** in.
5. Selecteer een entiteit in het tweede veld **Naam**.
6. Selecteer **OK**.

    [![Dialoogvenster Eigenschappen van tabelgegevensbron](./media/pic9.png)](./media/pic9.png)

7. Selecteer **Aangepaste Dataverse** en **Aangepaste entiteit** en selecteer vervolgens **Binden**.

    [![Aangepaste Dataverse en Aangepaste entiteitsbinding.](./media/pic10.png)](./media/pic10.png)

8. Selecteer onder **Aangepaste Dataverse** en **Aangepast veld** een veld en selecteer vervolgens **Binden**.

    [![Aangepaste Dataverse en Aangepaste veldbinding.](./media/pic11.png)](./media/pic11.png)

9. Selecteer **Opslaan** en vervolgens **Voltooien**.

## <a name="create-a-customized-tax-configuration"></a>Een aangepaste belastingconfiguratie maken

1. Selecteer in de werkruimte **Elektronische rapportage** de optie **Belastingconfiguraties** en selecteer vervolgens **Belastingberekeningsconfiguratie**.
2. Selecteer **Configuratie maken**.
3. Selecteer **Belastingserviceconfiguratie afgeleid van naam: belastingberekeningsconfiguratie, Microsoft**.
4. Voer in het veld **Naam** **Aanpassingsconfiguratie** in.
5. Selecteer **Configuratie maken**.
6. Selecteer **Aanpassingsconfiguratie** en selecteer vervolgens **Ontwerper**.
7. Selecteer in het veld **Gegevensmodel** de optie **Gegevensmodel voor aanpassing**.
8. Selecteer in het veld **Gegevensmodelversie** de corresponderende gegevensmodelversie.

    [![Eigenschappensectie](./media/pic13.png)](./media/pic13.png)

9. Selecteer **Voltooien**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
