---
title: Dataverse-synchronisatie opnieuw instellen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen met records die niet correct worden gesynchroniseerd tussen Microsoft Dynamics 365 Human Resources en de HCM Common-oplossing (Human Capital Management) in Microsoft Dataverse.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d6b20b6b2ae4fdbbfb27a765dfb7a1dc82fe7981
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071155"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse-synchronisatie opnieuw instellen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Probleem

Records worden niet gesynchroniseerd tussen Microsoft Dynamics 365 Human Resources en de entiteiten in de HCM Common-oplossing (Human Capital Management) in Microsoft Dataverse. Ga voor meer informatie over synchronisatie naar[Dataverse-integratie](hr-admin-integration-common-data-service.md) configureren. Een niet-correcte synchronisatie kan zich voordoen wanneer de batchtaken **Dataverse-integratie opnieuw uitvoeren** of **Dataverse-integratie mist aanvraag voor synchronisatie** vastlopen in een status **Uitvoeren**.

## <a name="resolution"></a>Oplossing

Wanneer de batchtaken **Dataverse-integratie opnieuw uitvoeren** of **Dataverse-integratie mist aanvraag voor synchronisatie** vastlopen in een status **Uitvoeren** of **Annuleren**, kunt u de status opnieuw instellen. U kunt dit doen door de batchtaak te annuleren door de stappen in [Vastgelopen batchtaken opnieuw instellen](hr-admin-troubleshooting-batch-execution.md) te volgen. Nadat u de batchtaak hebt geannuleerd, kunt u de batchtaak opnieuw instellen door de status van de taak in te stellen op **Wachten**. De batchtaak wordt vervolgens uitgevoerd tijdens de volgende geplande runtime.

1. Als u dit nog niet hebt gedaan, moet u de functie **Verbeterde batchafbreking** in **Functiebeheer** inschakelen.
   1. Ga naar de pagina **Functiebeheer** (**Systeembeheer** > **Overzicht** > **Functiebeheer**).
   2. Selecteer het tabblad **Alle**.
   3. Selecteer de kolom **Functienaam** en filter op **Verbeterde batchafbreking**.
   4. Selecteer de actie **Inschakelen** als deze nog niet is ingeschakeld.

2. Schakel de Dataverse-integratie uit.
   1. Ga naar de pagina **Microsoft Dataverse-integratie** (**Systeembeheer**, **Koppelingen** > **Integraties** > **Dataverse-configuratie**).
   2. Stel **Dataverse-integratie inschakelen** in op **Nee**.

3. Annuleer de batchtaak **Dataverse-integratie opnieuw uitvoeren**.
   1. Ga naar de pagina **Batchtaken** (**Systeembeheer**, **Koppelingen** > **Batchtaken** > **Batchtaken**).
   2. Filter de kolom **Taakomschrijving** op **Integratie**.
   3. Selecteer de batchtaak **Dataverse-integratie opnieuw uitvoeren**.
   4. Selecteer op het actielint de optie **Batchtaak**, **Annuleren afdwingen** en selecteer vervolgens **Ja** om uw keuze te bevestigen.

   > [!NOTE]
   > Afhankelijk van wanneer de integratie voor het eerst is ingeschakeld, heeft de batchtaak mogelijk de beschrijving **Common Data Service-integratie opnieuw uitvoeren**. Selecteer deze batchtaak als deze wordt weergegeven in plaats van de batchtaak **Dataverse-integratie opnieuw uitvoeren**.

4. Verwijder alle Dataverse-integratiebatchtaken.
   1. Selecteer op de pagina **Batchtaken** de batchtaken **Gemiste aanvragen Dataverse-integratie synchroniseren**, **Dataverse-integratie opnieuw uitvoeren** en **Initiële Dataverse-synchronisatietaken**.
   2. Selecteer op het actielint de actie **Status wijzigen**. 
   3. Selecteer **Inhouden** en selecteer **OK**.
   4. Selecteer de actie **Verwijderen** op het actielint en selecteer vervolgens **Ja** om de actie te bevestigen.

5. Schakel de Dataverse-integratiebatchtaken in.
   1. Ga naar de pagina **Microsoft Dataverse-integratie** (**Systeembeheer** > **Koppelingen** > **Integratie** > **Dataverse-configuratie**).
   2. Stel **Dataverse-integratie inschakelen** in op **Ja**.

6. Ga naar de pagina **Batchtaken** en bevestig dat de batchtaken **Dataverse-integratie opnieuw uitvoeren** en **Gemiste aanvragen Dataverse-integratie synchroniseren** zijn gemaakt.

Wanneer de batchtaken opnieuw zijn gemaakt, kunt u de batchtaak **Dataverse-integratie opnieuw uitvoeren** controleren om te zien hoelang de uitvoering van de taak duurt. U kunt vervolgens controleren of de records correct worden gesynchroniseerd met de HCM Common-oplossing in Microsoft Dataverse.

## <a name="see-also"></a>Zie ook

[Integratie met Dataverse configureren](hr-admin-integration-common-data-service.md)<br>
[Vastgelopen batchtaken opnieuw instellen](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
