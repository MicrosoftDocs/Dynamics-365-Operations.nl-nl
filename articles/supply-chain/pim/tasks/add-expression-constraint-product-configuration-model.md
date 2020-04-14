---
title: Een expressiebeperking toevoegen aan een productconfiguratiemodel
description: Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ac010b96892450c8d37bb08f967ecf4491b4b5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148004"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Een expressiebeperking toevoegen aan een productconfiguratiemodel

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een nieuwe expressie voor beperking toevoegt aan een productconfiguratiemodel. Deze geeft aan hoe u kunt verplicht dat de hoekbescherming moet worden toegepast op een luidspreker als de gebruiker een grill in metaal heeft geselecteerd. De procedure gebruikt het onderdeel Geavanceerde luidspreker in het demobedrijf USMF.


## <a name="create-an-expression-constraint"></a>Maak een expressiebeperking
1. Klik op Definitie van productvariantmodel.
2. Klik op Productconfiguratiemodellen.
3. Zoek en selecteer de gewenste record in de lijst.
    * In dit voorbeeld wordt het model Geavanceerde luidspreker gebruikt.  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Vouw de sectie Beperkingen uit.
6. Klik op Toevoegen.
7. Klik op Maken.
8. Typ een waarde in het veld Naam.

## <a name="enter-expression"></a>Expressie invoeren
1. Klik op Expressie bewerken.
    * Als u de gebruikersinterface in de taakregistratie in deze fase ontgrendelt, kunt u IntelliSense en de lijst van symbolen gebruiken om de expressie voor de beperking te maken.  
2. Typ 'Implies[FrontGrill=="Metal", CornerProtection] ' in het veld ConstraintBody.
    * Deze expressielogica meldt: Als de grill van metaal is, moet de optie voor hoekbescherming worden geselecteerd.  
3. Klik op Valideren.
    * De validatiefunctie wordt uitgevoerd op de expressie voor de beperking en controleert op syntaxisfouten.  
4. Klik op Sluiten.
5. Klik op OK.

