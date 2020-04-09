---
title: Schakelen tussen leverancierontwerpen
description: In dit onderwerp wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173034"
---
# <a name="switch-between-vendor-designs"></a>Schakelen tussen leverancierontwerpen

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Leveranciersgegevensstroom 

Als u ervoor kiest om de entiteit **Rekening** te gebruiken voor de opslag van leveranciers van het type **Organisatie** en de entiteit **Contactpersoon** om leveranciers van het type **Persoon** op te slaan, configureert u de volgende werkstromen. Anders is deze configuratie niet vereist.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Organisatie

Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen. U maakt een werkstroom voor elke sjabloon.

+ Leveranciers maken in entiteit Accounts
+ Leveranciers maken in entiteit Leveranciers
+ Leveranciers bijwerken in entiteit Accounts
+ Leveranciers bijwerken in entiteit Leveranciers

Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.

1. Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers maken in entiteit Accounts**. Selecteer vervolgens **OK**. Deze workflow verwerkt het scenario voor het maken van de entiteit **Account**.

    ![Het werkstroomproces Leveranciers maken in entiteit Accounts](media/create_process.png)

2. Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in entiteit Accounts**. Selecteer vervolgens **OK**. Deze workflow verwerkt het scenario voor het bijwerken van de entiteit **Account**.
3. Maak een nieuw werkstroomproces voor de entiteit **Account** en selecteer de werkstroomprocessjabloon **Leveranciers maken in entiteit Leveranciers**.
4. Maak een nieuw werkstroomproces voor de entiteit **Account** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in entiteit Leveranciers**.
5. U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten. Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.

    ![De knop Converteren naar een workflow op de achtergrond](media/background_workflow.png)

6. Activeer de werkstromen die u hebt gemaakt voor de entiteiten **Account** en **Leverancier** om de entiteit **Account** te gebruiken voor het opslaan van leveranciersgegevens van het type **Organisatie**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Persoon

Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen. U maakt een werkstroom voor elke sjabloon.

+ Leveranciers van het type Persoon maken in entiteit Leveranciers
+ Leveranciers van het type Persoon maken in entiteit Contactpersonen
+ Leveranciers van het type Persoon bijwerken in entiteit Contactpersonen
+ Leveranciers van het type Persoon bijwerken in entiteit Leveranciers

Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.

1. Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon maken in entiteit Contactpersonen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het maken van de entiteit **Contactpersoon**.
2. Maak een nieuw werkstroomproces voor de entiteit **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon bijwerken in entiteit Contactpersonen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het bijwerken van de entiteit **Contactpersoon**.
3. Maak een nieuw werkstroomproces voor de entiteit **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon maken in entiteit Leveranciers**.
4. Maak een nieuw werkstroomproces voor de entiteit **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon bijwerken in entiteit Leveranciers**.
5. U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten. Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.
6. Activeer de werkstromen die u hebt gemaakt voor de entiteiten **Contactpersoon** en **Leverancier** om de entiteit **Contactpersoon** te gebruiken voor het opslaan van leveranciersgegevens van het type **Persoon**.
