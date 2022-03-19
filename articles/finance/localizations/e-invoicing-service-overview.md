---
title: Overzicht van Elektronische facturering
description: Dit onderwerp bevat een overzicht van Elektronische facturering in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23a98706bc2ab0abc2c72e9f20d8e8fbff56b2b9
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371449"
---
# <a name="electronic-invoicing-overview"></a>Overzicht van Elektronische facturering

[!include [banner](../includes/banner.md)]

Elektronische facturering voor Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management is een hyperschaalbare service voor meerdere tenants waarmee configureerbare verwerking van elektronische facturen en configureerbare elektronische documentuitwisseling mogelijk is. De regels voor verwerking en integratie zijn volledig configureerbaar en de logica wordt uitgevoerd buiten Finance en Supply Chain Management. De service is met name gericht op de verwerking van elektronische factuurdocumenten in scenario's van bedrijf tot overheid. Het kan echter aangepaste configuratie zijn voor andere doeleinden, zoals business-to-business scenario's voor verschillende typen documenten.

Elektronische facturering kan u helpen om de volgende doelstellingen te verwezenlijken:

- Snelle en eenvoudige toepassing van vereisten die specifiek per land/regio gelden
- Gestandaardiseerde implementaties van een oplossing voor elektronische facturering
- Verbeterde traceerbaarheid van documentgeschiedenis
- Kortere implementatiecyclus
- Lagere totale kosten
- Eenvoudig aanpasbare configuraties waarvoor geen codewijzigingen nodig zijn
- Vereenvoudigde configuratieverpakking
- Ingebouwde export, import en integratie en eenvoudige uitbreidbaarheid bij de verwerking van documenten van elektronische facturen
- Eenvoudig hergebruik van dezelfde export-, import- en integratieconfiguraties in verschillende bedrijven

## <a name="service-availability"></a>Beschikbaarheid van service

Momenteel is de elektronische factureringsfunctionaliteit beschikbaar voor klanten van Finance en Supply Chain Management. Bekijk de licentievoorwaarden voor de toepassing voor meer informatie.

Omdat de functionaliteit waarmee de per land/regio geldende vereisten worden toegepast, tot verschillende fasen van de release kan zijn beperkt, moet u altijd de meest actuele documentatie raadplegen waarin de dekking en het bereik van ondersteunde oplossingen per land/regio worden aangegeven.

Elektronische facturering wordt geïmplementeerd in de volgende Azure-regio´s:

- Verenigde Staten
- Europa
- Azië

> [!NOTE]
> Elektronische facturering biedt geen ondersteuning voor on-premises implementaties.

## <a name="feature-highlights"></a>Belangrijkste functies

- Standaardintegratie met Finance en Supply Chain Management
- Een consistente gebruikerservaring voor de configuratie en controle van het elektronische factureringsproces voor alle landen en regio's
- Snellere, eenvoudiger en goedkopere toepassing van oplossingen voor elektronische facturering in nieuwe landen of regio's
- Configuratie van de service via de instellingen van de RCS-service (Regulatory Configuration Service) en de globalisatiefuncties
- Transformatie van bedrijfsgegevens naar meerdere indelingen voor elektronische facturen, zoals XML, JavaScript Object Notation \[JSON\], TXT en \[CSV\] (door komma´s gescheiden waarden) met configuraties die zijn gedefinieerd in RCS:

    - Indelingen voor elektronische rapportage (ER) die beschikbaar zijn voor landen of regio's waar de configureerbaarheid van de transformatie van elektronische facturen niet beschikbaar is

- Configureerbare verzending van elektronische facturen naar externe webservices, waaronder certificeringsverwerking via digitale handtekeningen:

    - Ingebouwde, eenvoudig uitbreidbare en configureerbare integratie met extra inhoud voor verschillende landen en regio's

- Verwerking van reacties van webservices, waaronder configureerbare afhandeling van uitzonderingsberichten
- Ondersteuning voor elektronische handtekeningen (bijvoorbeeld handtekeningen met XMLDSig-algoritme)
- De mogelijkheid om documenten naar e-mails te verzenden en deze op te slaan in SharePoint
- Batchverwerking van berichten voor elektronische facturen
- Configureerbare transformatie van inkomende documenten en de verwerking van die documenten in Finance en Supply Chain Management
- De mogelijkheid om inkomende documenten te ontvangen van kanalen zoals e-mail en SharePoint

## <a name="privacy-notice"></a>Privacyverklaring

Als u elektronische facturering wilt inschakelen, moeten mogelijk beperkte gegevens worden verzonden. Deze gegevens omvatten de belastingregistratie-id van de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd om elektronische facturen te verzenden in de vooraf gedefinieerde indelingen die nodig zijn voor de integratie met de webservices van deze overheid. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service, is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de sectie 'Privacyverklaring' in de documentatie over land-/regiospecifieke functies voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
