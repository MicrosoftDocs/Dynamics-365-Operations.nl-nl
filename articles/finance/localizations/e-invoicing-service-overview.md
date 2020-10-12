---
title: Overzicht van de invoegtoepassing voor elektronische facturering
description: Dit onderwerp bevat informatie over de invoegtoepassing voor elektronische facturering in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b3445157efce6349b3febafb6c860260052f7d6c
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835930"
---
# <a name="electronic-invoicing-add-on-overview"></a>Overzicht van de invoegtoepassing voor elektronische facturering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

De invoegtoepassing voor elektronische facturering voor Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management is een hyperschaalbare service voor meerdere tenants waarmee configureerbare verwerking van elektronische factuurdocumenten en configureerbare documentuitwisseling mogelijk is. De regels voor verwerking en integratie zijn volledig configureerbaar en de logica wordt uitgevoerd buiten Finance en Supply Chain Management. De service is voornamelijk gericht op de verwerking van elektronische facturen tussen bedrijven en de overheid, maar dit kunt u aanpassen voor andere doeleinden.

De invoegtoepassing voor elektronische facturering kan u helpen om de volgende doelstellingen te verwezenlijken:

- Snelle en eenvoudige toepassing van vereisten die specifiek per land/regio gelden
- Gestandaardiseerde implementaties van een invoegtoepassingsoplossing voor elektronische facturering
- Verbeterde traceerbaarheid van documentgeschiedenis
- Kortere implementatiecyclus
- Lagere totale kosten
- Eenvoudig aanpasbare configuraties waarvoor geen codewijzigingen nodig zijn
- Vereenvoudigde configuratieverpakking
- Ingebouwde export, import en integratie en eenvoudige uitbreidbaarheid bij de verwerking van documenten van elektronische facturen
- Eenvoudig hergebruik van dezelfde export-, import- en integratieconfiguraties in verschillende bedrijven

Als u de invoegtoepassing voor elektronische facturering wilt gebruiken, moet u deze installeren vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS). Volg vervolgens de configuratieprocedure om de integratie met Finance of Supply Chain Management in te schakelen. Zie [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md) voor meer informatie.

## <a name="availability"></a>Beschikbaarheid

In eerste instantie is de invoegtoepassing voor elektronische facturering beschikbaar voor geselecteerde klanten via een voorbeeldprogramma. Later wordt het voorbeeld voor een groter aantal klanten geopend. Tot slot wordt de service in het algemeen beschikbaar. Omdat de functionaliteit waarmee de per land/regio geldende vereisten worden toegepast, tot verschillende fasen van de release kan zijn beperkt, moet u altijd de meest actuele documentatie raadplegen waarin de dekking en het bereik van ondersteunde oplossingen per land/regio worden aangegeven.

De invoegtoepassing voor elektronische facturering wordt geïmplementeerd in de volgende Azure-regio´s:

- Verenigde Staten
- Europa

> [!NOTE]
> Met de invoegtoepassing voor elektronische facturering worden geen on-premises implementaties ondersteund.

## <a name="extended-configurability"></a>Uitgebreide configureerbaarheid

De invoegtoepassing voor elektronische facturering kan worden gebruikt in scenario's waarin u een elektronisch document moet maken en naar de toegewezen partijen moet verzenden. Het is speciaal ontworpen voor het uitvoeren van een configureerbare stroom van verwerkingsacties op basis van ontvangen gegevens. De configureerbaarheidsopties die beschikbaar zijn in Finance en Supply Chain Management, zijn beperkt tot documenttransformatie. Met de service worden deze opties uitgebreid door de configureerbare integraties toe te voegen die in de service beschikbaar zijn. Bovendien worden voor alle functionaliteiten voor elektronische facturen die eerder beschikbaar waren, zoals de Braziliaanse Nota Fiscal eletrônica (NF-e), de Mexicaanse Comprobante Fiscal Digital por Internet (CFDI) of andere West-Europese UBL- (Universal Business Language) en Pan-Europese PEPPOL-functies (Public Procurement OnLine), configuraties gebruikt voor export en import en voor het inschakelen van integraties met externe webservices.

## <a name="feature-highlights"></a>Belangrijkste functies

- Standaardintegratie met Finance en Supply Chain Management
- Consistente gebruikerservaring voor de configuratie en controle van het elektronische factureringsproces voor alle landen of regio's
- Snellere, eenvoudiger en goedkopere toepassing van invoegtoepassingsoplossingen voor elektronische facturering in nieuwe landen of regio's
- Configuratie van de service via de instellingen van de RCS-service (Regulatory Configuration Service) en de globalisatiefunctie
- Transformatie van bedrijfsgegevens naar meerdere indelingen voor elektronische facturen, zoals XML, JavaScript Object Notation \[JSON\], TXT en \[CSV\] (door komma´s gescheiden waarden) met configuraties die zijn gedefinieerd in RCS:

    - Indelingen voor elektronische rapportage die beschikbaar zijn voor landen of regio's waar de configureerbaarheid van de transformatie van elektronische facturen niet beschikbaar is

- Configureerbare verzending van elektronische facturen naar externe webservices, waaronder certificeringsverwerking via digitale handtekeningen:

    - Ingebouwde, eenvoudig uitbreidbare en configureerbare integratie met extra inhoud voor verschillende landen

    > [!NOTE]
    > Momenteel wordt een beperkt aantal directe verzendingen ondersteund. Zie de sectie [Beschikbaarheid](#availability), eerder in dit onderwerp, voor meer informatie. De ondersteuning wordt in de toekomst uitgebreid.

- Verwerking van reacties van webservices, waaronder configureerbare afhandeling van uitzonderingsberichten
- Ondersteuning voor elektronische handtekeningen (bijvoorbeeld met behulp van het XMLDSig-algoritme voor handtekeningen)
- Batchverwerking van berichten voor elektronische facturen

## <a name="architecture-and-data-flow"></a>Architectuur en gegevensstroom

Wanneer de invoegtoepassing voor elektronische facturering wordt geïnstalleerd vanuit LCS en de vereiste instellingen in alle vereiste toepassingen zijn voltooid, wordt een beveiligde verbinding tot stand gebracht. De service bevindt zich momenteel in datacenters in de Verenigde Staten en Europa. De locatie van de service kan dus verschillen van de locatie van de gerelateerde Finance- of Supply Chain Management-instantie. Nadat u de instellingen van de invoegtoepassing voor elektronische facturering hebt voltooid en de integratie hebt ingeschakeld, worden elke keer wanneer een elektronische factuur wordt verzonden hoofdgegevens en transactiegegevens die zijn gerelateerd aan een bepaald document, verzonden naar de invoegtoepassing voor elektronische facturering.

> [!NOTE]
> Als uw elektronische factuur of een ander document persoonlijke gegevens bevat, controleert u of u deze functie gebruikt in overeenstemming met de AVG (algemene verordening gegevensbescherming) en andere voorschriften die zijn gerelateerd aan de overdracht van persoonsgegevens.

### <a name="high-level-description-of-the-data-flow"></a>Beschrijving op hoog niveau van de gegevensstroom

1. De client verzendt een canoniek bedrijfsdocument naar de service.
2. Op basis van de contextinformatie die wordt ontvangen van de client, wordt de desbetreffende verwerkingsstroom geselecteerd.
3. Met de service worden de verwerkingsacties uitgevoerd. Deze acties kunnen het transformeren van het bedrijfsdocument naar een elektronische factuur, het toepassen van een elektronische handtekening en het indienen van het document bij een externe webservice betreffen.
4. Alle ontvangen en verwerkte documenten worden opgeslagen in de Azure Blob Storage van de klant.
5. Alle tenantgeheimen en -certificaten die voor verwerking zijn gebruikt, worden opgeslagen in de Azure-sleutelkluis van de klant.
6. De service biedt de client informatie op aanvraag over de verwerkingsstatus van het verzonden bedrijfsdocument.
7. De client ontvangt informatie over de voltooide verwerkingsuitvoering en maakt alle logboekgegevens beschikbaar. Ook wordt het document beschikbaar gemaakt dat is gemaakt of ontvangen tijdens de verwerking van de stroom.

In de volgende afbeelding wordt weergegeven hoe de gegevensstroom van en naar de invoegtoepassing voor elektronische facturering verloopt.

![Gegevensstroom voor de invoegtoepassing voor elektronische facturering](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Privacyverklaring
Voor het inschakelen en gebruiken van elektronische facturering moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-ID voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd om elektronische facturen te verzenden in de vooraf gedefinieerde indelingen die nodig zijn voor de integratie met de webservices van deze overheid. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië](e-invoicing-bra-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Mexico](e-invoicing-mex-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië](e-invoicing-ita-get-started.md)
- [De invoegtoepassing voor elektronische facturering instellen](e-invoicing-setup.md)
