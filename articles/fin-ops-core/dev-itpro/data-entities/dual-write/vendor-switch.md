---
title: Schakelen tussen leverancierontwerpen
description: In dit onderwerp wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen Finance and Operations-apps en Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 70904ee716aabd019210e92895a894810bde27fb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346515"
---
# <a name="switch-between-vendor-designs"></a>Schakelen tussen leverancierontwerpen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Leveranciersgegevensstroom 

Als u ervoor kiest om de tabel **Rekening** te gebruiken voor de opslag van leveranciers van het type **Organisatie** en de tabel **Contactpersoon** om leveranciers van het type **Persoon** op te slaan, configureert u de volgende werkstromen. Anders is deze configuratie niet vereist.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Organisatie

Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen. U maakt een werkstroom voor elke sjabloon.

+ Leveranciers maken in tabel Accounts
+ Leveranciers maken in tabel Leveranciers
+ Leveranciers bijwerken in tabel Accounts
+ Leveranciers bijwerken in tabel Leveranciers

Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.

1. Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers maken in tabel Rekeningen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het maken van de tabel **Rekening**.

    ![Het werkstroomproces Leveranciers maken in tabel Accounts.](media/create_process.png)

2. Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in tabel Rekeningen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het bijwerken van de tabel **Rekening**.
3. Maak een werkstroomproces voor de tabel **Rekening** en selecteer de werkstroomprocessjabloon **Leveranciers maken in tabel Leveranciers**.
4. Maak een werkstroomproces voor de tabel **Rekening** en selecteer de werkstroomprocessjabloon **Leveranciers bijwerken in tabel Leveranciers**.
5. U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten. Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.

    ![De knop Converteren naar een workflow op de achtergrond.](media/background_workflow.png)

6. Activeer de werkstromen die u hebt gemaakt voor de tabellen **Rekening** en **Leverancier** om de tabel **Rekening** te gebruiken voor het opslaan van leveranciersgegevens van het type **Organisatie**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Het uitgebreide leveranciersontwerp gebruiken voor leveranciers van het type Persoon

Het oplossingspakket **Dynamics365FinanceExtended** bevat de volgende sjablonen voor werkstroomprocessen. U maakt een werkstroom voor elke sjabloon.

+ Leveranciers van het type Persoon maken in tabel Leveranciers
+ Leveranciers van het type Persoon maken in tabel Contactpersonen
+ Leveranciers van het type Persoon bijwerken in tabel Contactpersonen
+ Leveranciers van het type Persoon bijwerken in tabel Leveranciers

Ga als volgt te werk om nieuwe werkstroomprocessen te maken op basis van de werkstroomprocessjablonen.

1. Maak een werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon maken in tabel Contactpersonen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het maken van de tabel **Contactpersoon**.
2. Maak een nieuw werkstroomproces voor de tabel **Leverancier** en selecteer de werkstroomprocessjabloon **Leveranciers van het type Persoon bijwerken in tabel Contactpersonen**. Selecteer vervolgens **OK**. Deze werkstroom verwerkt het scenario voor het bijwerken van de tabel **Contactpersoon**.
3. Maak een werkstroomproces voor de tabel **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon maken in tabel Leveranciers**.
4. Maak een werkstroomproces voor de tabel **Contactpersoon** en selecteer de sjabloon **Leveranciers van het type Persoon bijwerken in tabel Leveranciers**.
5. U kunt de werkstromen configureren als realtime werkstromen of werkstromen op de achtergrond, afhankelijk van uw vereisten. Als u een werkstroom als een achtergrondwerkstroom wilt configureren, selecteert u **Converteren naar een workflow op de achtergrond**.
6. Activeer de werkstromen die u hebt gemaakt voor de tabellen **Contactpersoon** en **Leverancier** om de tabel **Contactpersoon** te gebruiken voor het opslaan van leveranciersgegevens van het type **Persoon**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]