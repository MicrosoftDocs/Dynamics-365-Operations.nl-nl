---
title: Schakelen tussen leverancierontwerpen
description: In dit artikel wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen apps voor financiën en bedrijfsactiviteiten en Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 88be9a4c6e2a860e8ac496e9a135ecabd8474c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901559"
---
# <a name="switch-between-vendor-designs"></a>Schakelen tussen leverancierontwerpen

[!include [banner](../../includes/banner.md)]





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