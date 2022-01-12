---
title: Tips voor voorraadzichtbaarheid
description: Dit onderwerp biedt een aantal tips die u kunt overwegen bij het instellen en gebruiken van de invoegtoepassing Voorraadzichtbaarheid.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920798"
---
# <a name="inventory-visibility-tips"></a>Tips voor voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]

Hier volgt een aantal tips die u kunt overwegen bij het instellen en gebruiken van de invoegtoepassing Voorraadzichtbaarheid:

- Momenteel ondersteunt de invoegtoepassing Voorraadzichtbaarheid alleen Microsoft Dataverse-omgevingen die zijn gemaakt met Microsoft Dynamics Lifecycle Services (LCS). Als uw Dataverse-omgeving op een andere manier gemaakt is (bijvoorbeeld door het Power Apps-beheercentrum te gebruiken) en als deze aan uw Dynamics 365 Supply Chain Management-omgeving gekoppeld is, moet u eerst het productteam van Voorraadzichtbaarheid vragen om het toewijzingsprobleem te verhelpen. U kunt contact opnemen met het team op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Het team laat u weten wanneer uw omgeving gereed is voor installatie van Voorraadzichtbaarheid.
- Als u meerdere LCS-omgevingen hebt, maakt u een andere Azure Active Directory (Azure AD)-toepassing voor elke omgeving. Als u dezelfde toepassings-id en tenant-id gebruikt om de invoegtoepassing Voorraadzichtbaarheid voor verschillende omgevingen te installeren, treedt er een probleem met een token op voor oudere omgevingen. Alleen het laatste exemplaar van de invoegtoepassing Voorraadzichtbaarheid die is geïnstalleerd, is geldig.
- Voorraadzichtbaarheid wordt momenteel niet ondersteund voor in de cloud gehoste omgevingen. Het wordt alleen ondersteund voor Tier 2+-omgevingen.
- De API (Application Programming Interface) ondersteunt momenteel query's met maximaal 100 afzonderlijke artikelen per `ProductID`-waarde. Ook kunnen in elke query meerdere `SiteID`- en `LocationID`-waarden worden opgegeven. De maximumlimiet wordt gedefinieerd als `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- De `fno`-gegevensbron is gereserveerd voor Supply Chain Management. Als de invoegtoepassing Voorraadzichtbaarheid is geïntegreerd met een Supply Chain Management-omgeving, raden we u aan om geen configuraties te verwijderen die betrekking hebben op `fno`in de [gegevensbron](inventory-visibility-configuration.md#data-source-configuration).
- De [partitieconfiguratie](inventory-visibility-configuration.md#partition-configuration) bestaat momenteel uit twee basisdimensies (`SiteId` en `LocationId`) die aangeven hoe de gegevens worden gedistribueerd. Bewerkingen onder dezelfde partitie kunnen betere prestaties bieden tegen lagere kosten. De oplossing bevat standaard deze partitieconfiguratie. Daarom *hoeft u deze niet zelf te definiëren*. Pas de standaard partitieconfiguratie niet aan. Als u deze verwijdert of wijzigt, veroorzaakt u waarschijnlijk een onverwachte fout.
- Basisdimensies die in de partitieconfiguratie zijn gedefinieerd, mogen niet worden gedefinieerd in de [configuratie voor de productindexhiërarchie](inventory-visibility-configuration.md#index-configuration).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
