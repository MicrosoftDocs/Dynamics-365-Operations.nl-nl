---
title: Talent uitbreiden met Power Apps en Power Automate
description: In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Human Resources die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859512"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Uitbreiden met Power Apps en Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden enkele voorbeelden beschreven van uitbreidbaarheidsscenario's voor Microsoft Dynamics 365 Human Resources die gebruikmaken van Microsoft Power Apps en Microsoft Power Automate. U kunt het oplossingspakket importeren dat is gekoppeld aan elk voorbeeld in uw Power Apps-omgeving. Vervolgens kunt u de pakketten als richtlijn of als beginpunt gebruiken voor het implementeren van scenario's die van toepassing op uw organisatie.

> [!IMPORTANT]
> Als u de sjablonen en apps die worden beschreven in dit artikel, 'as is' wilt gebruiken, moet u ze testen om er zeker van te zijn dat ze betrekking hebben op alle scenario's die specifiek voor uw implementatie zijn.

## <a name="prerequisites"></a>Vereisten

- Als u wilt pakketten wilt importeren, moeten gebruikers beschikken over de machtiging **Maker omgeving** beschikken.
- Als u apps wilt exporteren of importeren, moeten gebruikers een Power Apps Plan 2-licentie of een proeflicentie van Power Apps Plan 2 hebben.

## <a name="integration-with-microsoft-365-power-automate"></a>Integratie met Microsoft 365, Power Automate

De app **Integratie met Microsoft 365** kan worden gebruikt voor het ophalen van teamgegevens voor aangemelde gebruikers vanuit Microsoft 365. Het verwijst naar werknemers in Human resources om identificatietypen voor werknemers te extraheren. Managers kunnen vervaldatums van typen werknemer-id's controleren. Ze kunnen ook een herinnering per e-mail verzenden als het type werknemer-id verloopt. Power Automate integreert met Power Apps om deze herinnering te verzenden. Er wordt een bevestiging teruggestuurd naar Power Apps vanuit Power Automate wanneer de herinnering is verzonden. Identificatietypen zijn onder andere rijbewijs, paspoort en andere aanvaardbare vormen van identificatie.

U kunt deze app uitbreiden voor andere scenario's. U kunt deze bijvoorbeeld gebruiken om teamvakantiegegevens, agenda-items en teamspecifieke gebeurtenissen weer te geven.

Voor het downloaden van de app voor **integratie met Microsoft 365, Power Automate** gaat u naar [Integratie met Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) in het Microsoft Downloadcentrum.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren

Met de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** wordt verbinding gemaakt met Microsoft SQL Server en kunnen SQL-query's worden uitgevoerd.

Hoewel met deze sjabloon SQL-tabellen worden gelezen en bijgewerkt, kunt u deze uitbreiden en gebruiken voor andere scenario's. Zo kunt u de sjabloon bijvoorbeeld gebruiken voor het vullen van een faseringstabel in Dataverse met records van SQL Server en voor het periodiek synchroniseren van de faseringstabel met behulp van een incrementele push van SQL Server.

Geavanceerde query is geïntegreerd met Flow om gegevenstransformatie en incrementele push mogelijk te maken.

Voor het downloaden van de sjabloon **Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren** gaat u naar [Power Automate: verbinding maken met SQL en SQL-query´s uitvoeren](https://go.microsoft.com/fwlink/?linkid=2081789) in het Microsoft Downloadcentrum.

## <a name="additional-resources"></a>Aanvullende bronnen

[Het Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
