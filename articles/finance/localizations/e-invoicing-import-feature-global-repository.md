---
title: Functies importeren vanuit de algemene opslagplaats
description: Dit artikel licht toe hoe u globalisatiefuncties importeert vanuit de Algemene opslagplaats.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278306"
---
# <a name="import-features-from-the-global-repository"></a>Functies importeren vanuit de algemene opslagplaats

[!include [banner](../includes/banner.md)]

De Algemene opslagplaats bevat elektronische factureringsfuncties die met uw configuratieprovider worden gedeeld. Alle functies voor elektronische facturering die door Microsoft worden geleverd, worden gedeeld met alle bedrijven. U hebt automatisch toegang tot alle elektronische factureringsfuncties die Microsoft vrijgeeft en publiceert naar de Algemene opslagplaats.

Als u wilt gaan werken met elektronische factureringsfuncties die worden gedeeld met uw configuratieprovider, importeert u deze in uw exemplaar van Regulatory Configuration Service (RCS) vanuit de algemene opslagplaats. Bekijk vervolgens de details van de functie, zoals de ER-configuraties (Electronic Reporting) en de verwerking van pijplijnen.

## <a name="import-a-feature-from-the-global-repository"></a>Een functie importeren vanuit de algemene opslagplaats

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Selecteer **Importeren** om de zoekopdracht **Functie importeren uit algemene opslagplaats** te openen.
4. Als u wilt bladeren door de Elektronische factureringsfuncties die beschikbaar zijn in de algemene opslagplaats voor een specifieke configuratieprovider, synchroniseert u het RCS-exemplaar van uw organisatie door **Synchroniseren** te kiezen. Nadat de synchronisatie is voltooid, wordt de lijst met beschikbare Elektronische factureringsfuncties bijgewerkt uit de Algemene opslagplaats. Deze update kan mogelijk enkele minuten in beslag nemen.
5. Selecteer de functie die u wilt importeren en selecteer **Importeren**.

Als u de geïmporteerde elektronische factureringsfunctie wilt weergeven, moet u de juiste configuratieprovider selecteren. Functies die door de actieve configuratieprovider zijn gemaakt, worden standaard automatisch weggefilterd. U kunt het filter aanpassen om functies weer te geven die door andere providers zijn gemaakt, zoals de Microsoft-configuratieprovider.

U kunt nu werken met de geïmporteerde functie. U kunt de details bekijken en een nieuwe functie maken door de geïmporteerde functie als een sjabloon te gebruiken.

> [!NOTE]
> U kunt een functie alleen wijzigen als deze is gemaakt door de configuratieprovider die momenteel actief is. U kunt een nieuwe functie maken door de oorspronkelijke functie als basis te gebruiken. Vervolgens kunt u de vereiste wijzigingen aanbrengen of de parameters instellen.

Wanneer Microsoft of een ander bedrijf dat globalisatiefuncties deelt met uw bedrijf, functies wijzigt die u hebt geïmporteerd, kunt u controleren op bijgewerkte versies met **Controleren op functie-updates** in de sectie **Verwante instellingen** van de werkruimte **Globalisatiefuncties**.

Als u ziet dat er updates zijn voor een functie die u als sjabloon gebruikt, kunt u een nieuwe versie importeren nadat u de lijst met gepubliceerde functies in de Algemene opslagplaats hebt gesynchroniseerd.
