---
title: Veelgestelde vragen over go-live
description: Dit onderwerp bevat veelgestelde vragen over hoe u live kunt gaan werken met een Dynamics 365 Human Resources-implementatieproject.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf00f7428c9b1852a5bf54fd7e30a3bddc1a31e
ms.sourcegitcommit: 0e60df840688932795b9c8f8fd45d98f5ab6ba8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2020
ms.locfileid: "4668940"
---
# <a name="go-live-faq"></a>Veelgestelde vragen over go-live 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat veelgestelde vragen over hoe u live kunt gaan werken met een Dynamics 365 Human Resources-implementatieproject. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Wanneer kan ik mijn productieomgeving configureren en aanvragen? 

Een productieomgeving wordt meestal geïmplementeerd als aan de volgende criteria is voldaan:

- Voor alle aanpassingen is de code voltooid.
- Acceptatietesten door gebruiker (UAT) zijn voltooid.
- De klant heeft zich afgemeld bij de oplossing.
- Er zijn geen problemen die het live gaan in de weg staan. 

Wanneer gekwalificeerde klanten zich in deze fase bevinden, werkt het Microsoft FastTrack-team samen met het projectteam om een go-live-beoordeling uit te voeren. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Wat zijn de vereisten voor de implementatie van een productieomgeving? 

Zie  [Voorbereiden op go-live](hr-admin-go-live-prepare.md) voor een lijst met de vereisten. 

## <a name="what-is-a-go-live-assessment"></a>Wat is een go-live-beoordeling?  

De go-live-beoordeling maakt deel uit van het  [Microsoft FastTrack-programma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Tijdens deze evaluatie beoordeelt een oplossingsarchitect of een implementatieproject gereed is voor een geslaagde cutover en go-live. Deze evaluatie is verplicht voor elk implementatieproject voordat u in een productieomgeving kunt verzoeken om live te gaan. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Onze Sandbox-omgevingen zijn geïmplementeerd in het Central US-datacenter. We willen dat onze productieomgevingen in het West US-datacenter worden geïmplementeerd. Kan ik West US als het datacenter selecteren in mijn productieconfiguratie? 

LCS weerhoudt u er niet van een ander datacenter te selecteren wanneer u een HRM-omgeving implementeert, maar het wordt nadrukkelijk afgeraden om een ander datacenter te selecteren.  

Als u het West US-datacenter voor uw productieomgeving wilt, moet u eerst uw Sandbox-omgevingen opnieuw implementeren voor het West US-datacenter, deze testen en afmelden. 

Zie [Netwerkvereisten](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements) voor informatie over het selecteren van het juiste datacenter. 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Welk toegangsniveau heb ik nodig voor de Azure-resources voor mijn Human Resources-omgevingen?  

De toegang tot de Human Resources-omgevingen is beperkt. U hebt geen toegang tot de virtuele machine (VM) of Microsoft internet Information Services (IIS). U kunt ook geen toegang krijgen tot de database via Microsoft SQL Server Management Studio. 

Hoewel u niet direct toegang kunt krijgen tot de Azure-resources of Dynamics 365 Human Resources-omgeving, zijn er aanvullende functies die u kunt gebruiken om toegang te krijgen tot uw gegevens:

- U kunt een Azure SQL-database implementeren in uw eigen Azure-tenant en de BYOD-functie (Bring Your Own Database) gebruiken om gegevens te synchroniseren. Meer informatie over BYOD vindt u in [Uw eigen database gebruiken (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- U kunt Common Data Service-integratie gebruiken om geselecteerde entiteiten te synchroniseren met de Common Data Service-database. Zie [Common Data Service-entiteiten](hr-developer-entities.md) voor meer informatie. 

## <a name="how-often-is-my-production-database-backed-up"></a>Hoe vaak wordt er een back-up van mijn productiedatabase gemaakt? 

Databases worden met de volgende frequenties beschermd door middel van automatische back-ups:

| Type back-up | Frequentie |
| --- | --- |
| Volledige databaseback-up | Wekelijks |
| Differentiële databaseback-up | Elke 12-24 uur |
| Back-up van transactielogboek | Elke 5 tot 10 minuten |

Microsoft bewaart voldoende back-ups zodat PITR (Point in Time Restore) binnen de afgelopen 14 dagen mogelijk is. 

Zie  [Meer informatie over automatische back-ups van SQL-database](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database) voor meer informatie. 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Kan ik een kopie van de back-up van mijn productiedatabase aanvragen? 

Nr. U kunt echter een serviceaanvraag voor het vernieuwen van de database indienen om uw productieomgeving naar uw Sandbox-omgeving te kopiëren. U kunt een Azure SQL-database implementeren in uw eigen Azure-tenant en de BYOD-functie gebruiken om gegevens te synchroniseren vanuit uw productieomgeving. Meer informatie over BYOD vindt u in [Uw eigen database gebruiken (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Hoe verplaats ik mijn Sandbox-omgeving naar productie voor een go-live? 

Omdat er geen kopieerfunctie beschikbaar is om uw omgeving te verplaatsen vanuit een Sandbox- naar een productieomgeving, moet u gegevenspakketten gebruiken om gegevens naar uw productieomgeving te verplaatsen.  

Het is raadzaam een duidelijke lijst met entiteiten die in uw Sandbox zijn geconfigureerd in het hele project bij te houden. Test vervolgens het proces van wijziging en migratie van alle gegevenspakketten die nodig zijn voor uw go-live. U moet gegevenspakketten handmatig naar de productieomgeving verplaatsen als u klaar bent om live te gaan. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Wat moet ik doen als er een storing in mijn productieomgeving is? 

Als u een storing in de productie wilt rapporteren, volgt u het proces dat wordt beschreven in  [Een storing in de productie rapporteren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Zie ook

 [Voorbereiden voor go-live](hr-admin-go-live-prepare.md)
