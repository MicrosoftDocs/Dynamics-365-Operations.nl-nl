---
title: Gegevensvelden toevoegen in belastingconfiguraties
description: In dit onderwerp wordt uitgelegd hoe u belastingconfiguraties aanpast door gegevensvelden toe te voegen.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022782"
---
# <a name="add-data-fields-in-tax-configurations"></a>Gegevensvelden toevoegen in belastingconfiguraties

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u belastingconfiguraties aanpast met behulp van [gegevensvelden die worden toegevoegd in de belastingintegratie](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Het belastinggegevensmodel aanpassen

1. Ga in Microsoft Dynamics 365 Finance naar **Elektronische rapportage** \> **Belastingconfiguraties**.
2. Selecteer **Belastinggegevensmodel - Europa** in de configuratiestructuur. Selecteer vervolgens **Configuratie maken** in het actievenster.
3. Selecteer in het dialoogvenster met vervolgkeuzemenu de optie **Belastingdocumentmodel afgeleid van Naam: Belastinggegevensmodel - Europa, Microsoft**, voer een naam in voor het nieuwe belastinggegevensmodel en selecteer **Configuratie maken**.
4. Selecteer het belastinggegevensmodel dat u zojuist hebt gemaakt en selecteer vervolgens **Ontwerper** in het actievenster.
5. Vouw de gegevensmodelstructuur uit, selecteer **Regels** en selecteer **Nieuw**.
6. Voer in het dialoogvenster **Knooppunt maken** een naam in, geef het itemtype op en selecteer **Toevoegen**.
7. Voeg de vereiste kolommen toe.
8. Selecteer in het actievenster **Opslaan** en vervolgens **Voltooien**.
9. Sluit de pagina en bekijk de voltooide versie van uw belastinggegevensmodel.

## <a name="customize-the-tax-configuration"></a>De belastingconfiguratie aanpassen

1. Ga in Finance naar **Elektronische rapportage** \> **Belastingconfiguraties**.
2. Selecteer **Belastingconfiguratie -- Europa** in de configuratiestructuur. Selecteer vervolgens **Configuratie maken** in het actievenster.
3. Selecteer in het dialoogvenster met vervolgkeuzemenu de optie **Belastingserviceconfiguratie afgeleid van Naam: Belastingconfiguratie - Europa, Microsoft**, voer een naam in voor de nieuwe belastingconfiguratie en selecteer **Configuratie maken**.
4. Selecteer de belastingconfiguratie die u zojuist hebt gemaakt en selecteer vervolgens **Ontwerper** in het actievenster.
5. Selecteer in de sectie **Eigenschappen** in het veld **Gegevensmodel** het aangepaste belastinggegevensmodel dat u eerder hebt gemaakt.
6. Selecteer in het veld **Gegevensmodelversie** de voltooide versie van het belastinggegevensmodel.
7. Selecteer **Toevoegen** en voeg de vereiste belastingmaatregelen toe.
8. Selecteer in het actievenster **Opslaan** en vervolgens **Voltooien**.
9. Sluit de pagina en bekijk de voltooide versie van uw belastingconfiguratie.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Belastingfuncties implementeren in de aangepaste belastingconfiguratie

1. Ga in Regulatory Configuration Services (RCS) naar **Globalisatiefuncties** \> **Belasting**.
2. Selecteer **Toevoegen**, voer informatie over de nieuwe functie in en selecteer vervolgens **Functie maken**.
3. Selecteer de de functie op het tabblad **Versies** en selecteer vervolgens **Bewerken**.
4. Selecteer op het tabblad **Algemeen** in het veld **Configuratieversie** de aangepaste belastingconfiguratie en -versie.
5. Selecteer in het dialoogvenster **Kolommen beheren** de kop- en regelkolommen die u wilt opnemen in uw aangepaste belastingmaatregel en selecteer vervolgens de juiste pijl-knop om ze toe te voegen aan de lijst **Geselecteerde kolommen**.
