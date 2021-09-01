---
title: Vergelijking van functies tussen cloud en on-premises
description: In dit onderwerp ziet u welke functies worden ondersteund in de cloud en on-premises.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 68082ad0ae264b76a852d8d12412af8c4ad917703441c41e67743d1b499a8d73
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736217"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Vergelijking van functies tussen cloud en on-premises

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een vergelijking van de beschikbare functies in cloud versus on-premises voor de volgende toepassingen:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Ook vindt u hier informatie over de [ontwikkelings- en beheerfuncties](cloud-prem-comparison.md#development-and-administration-features).

De volgende tabellen bevatten de toepassingsgebieden. Ondersteuning voor cloud en on-premises wordt voor de functie als geheel aangegeven. Als specifieke functies van het algehele gebied afwijken, worden de functies op een aparte regel in de kolom functie vermeld.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Gebied**             | **Functie**                | **Cloud** | **On-premises** |
|---------------------|-----------------------------|-----------|-----------------|
| Conformiteit en certificaten        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1-certificering van type 1                                                                | Ja       | Nee              |
| Gegevensbeheer en -integratie      |                                                                                           | Ja       | Ja             |
|                                      | Gegevens exporteren naar uw eigen datawarehouse                                                    | Ja       | Ja             |
|                                      | De export van incrementele updates naar een gegevensentiteit inschakelen                                 | Ja       | Ja             |
|                                      | Gegevensintegraties                                                                         | Ja       | Ja             |
| Documentbeheer                  |                                                                                           | Ja       | Ja             |
| Financieel beheer                 |                                                                                           | Ja       | Ja             |
| Help                                 |                                                                                           | Ja       | Nee              |
| Human Resources                      |                                                                                           | Ja       | Ja             |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronische rapportage (ER)                                                                 | Ja       | Ja             |
|                                      | ER: integratie met LCS                                                                  | Ja       | Nee              |
|                                      | ER: integratie met SharePoint                                                           | Ja       | Nee              |
|                                      | ER: integratie met Regulatory Configuration Services (RCS)                              | Ja       | Nee              |
|                                      | ER: gebruikt het lokale bestandssysteem als de opslag van ER-configuraties die toegankelijk zijn via ER-opslaglocaties | No        | Ja             |
|                                      | Integratie met PowerBI.com                                                              | Ja       | No              |
|                                      | Integratie met PowerBI Desktop                                                          | No        | Ja             |
|                                      | Analytische werkgebieden                                                                     | Ja       | No              |
|                                      | Intelligent bedrijfsproces: Aanbevelingen                                             | Ja       | Nee              |
|                                      | Power BI-rapporten met OData opstellen met Power BI Desktop- of Excel PowerQuery-hulpprogramma's    | Ja       | Nee              |
|                                      | SSRS (SQL Server Reporting Services) ondersteunt uitschalen                                 | Ja       | Ja             |
|                                      | Telemetrie wordt overgebracht naar de cloud                                                   | Ja       | No              |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Configureerbare bedrijfsprocessen                                                           | Ja       | Nee              |
| Lokalisaties                        |                                                                                           | Ja       | Ja             |
| Mobiele app, werkgebieden en platform |                                                                                           | Ja       | Ja             |
| Office-integratie                   |                                                                                           | Ja       | Ja             |
| Organisatiebeheer          |                                                                                           | Ja       | Ja             |
| Salaris                              |                                                                                           | Ja       | Ja             |
|                                      | Automatische overmaking                                                                            | Ja       | Nee              |
| Projectbeheer en boekhouding    |                                                                                           | Ja       | Ja             |
| Beveiliging                             |                                                                                           | Ja       | Ja             |
| Servicebeheer                   |                                                                                           | Ja       | Ja             |
| Webclient                           |                                                                                           | Ja       | Ja             |
|                                      | Taakregistratie: taakregistraties opslaan of laden uit de BPM-bibliotheek                         | Ja       | Nee              |
| Ondersteuning                              |                                                                                           | Ja       | Ja             |
|                                      | Toegang tot ondersteuning via het menu Help en ondersteuning                                             | Ja       | Nee              |
|                                      | Zakelijke gebeurtenissen                                                                           | Ja       | Ja (er is een internetverbinding vereist of er moeten aangepaste eindpunten worden geïmplementeerd voor het verzenden/ontvangen van zakelijke gebeurtenissen binnen het intranet)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Gebied**                | **Functie**             | **Cloud** | **On-premises** |
|-------------------------|-------------------|-----------|-----------------|
| Activabeheer                     |                                                                                           | Ja       | Ja             |
| Conformiteit en certificaten        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1-certificering van type 1                                                                | Ja       | Nee              |
| Kostprijsboekhouding                      |                                                                                           | Ja       | Ja             |
|                                      | Power BI-inhoudpakket - kostprijsboekhouding                                                 | Ja       | Nee              |
|                                      | Werkgebied Kostprijsboekhouding voor mobiele app                                                  | Ja       | Nee              |
| Kostenbeheer                      |                                                                                           | Ja       | Ja             |
|                                      | Inhoudpakket voor Power BI - kostenbeheer                                                 | Ja       | Nee              |
| Gegevensbeheer en -integratie      |                                                                                           | Ja       | Ja             |
|                                      | Uitbreiding op configuratiebasis                                                            | Ja       | Nee              |
|                                      | Gegevens exporteren naar uw eigen datawarehouse                                                    | Ja       | Ja             |
|                                      | De export van incrementele updates naar een gegevensentiteit inschakelen                                 | Ja       | Ja             |
|                                      | Gegevensintegraties                                                                         | Ja       | Ja             |
| Documentbeheer                  |                                                                                           | Ja       | Ja             |
| Help                                 |                                                                                           | Ja       | Nee              |
| Intelligence                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronische rapportage (ER)                                                                 | Ja       | Ja             |
|                                      | ER: integratie met LCS                                                                  | Ja       | Nee              |
|                                      | ER: integratie met SharePoint                                                           | Ja       | Nee              |
|                                      | ER: integratie met Regulatory Configuration Services (RCS)                              | Ja       | Nee              |
|                                      | ER: gebruikt het lokale bestandssysteem als de opslag van ER-configuraties die toegankelijk zijn via ER-opslaglocaties | No        | Ja             |
|                                      | Integratie met PowerBI.com                                                              | Ja       | No              |
|                                      | Integratie met PowerBI Desktop                                                          | No        | Ja             |
|                                      | Analytische werkgebieden                                                                     | Ja       | No              |
|                                      | Intelligent bedrijfsproces: Aanbevelingen                                             | Ja       | Nee              |
|                                      | Power BI-rapporten met OData opstellen met Power BI Desktop- of Excel PowerQuery-hulpprogramma's    | Ja       | Nee              |
|                                      | SSRS (SQL Server Reporting Services) ondersteunt uitschalen                                 | Ja       | Ja             |
|                                      | Telemetrie wordt overgebracht naar de cloud                                                   | Ja       | No              |
| Voorraadbeheer                 |                                                                                           | Ja       | Ja             |
| Lifecycle Services                   |                                                                                           | Ja       | Ja             |
|                                      | Configureerbare bedrijfsprocessen                                                           | Ja       | Nee              |
| Lokalisaties                        |                                                                                           | Ja       | Ja             |
| Productie                        |                                                                                           | Ja       | Ja             |
| Hoofdplanning en prognoses      |                                                                                           | Ja       | Ja             |
| Planningsoptimalisatie                |                                                                                           | Ja       | No              |
| Mobiele app, werkgebieden en platform |                                                                                           | Ja       | Ja             |
| Office-integratie                   |                                                                                           | Ja       | Ja             |
| Organisatiebeheer          |                                                                                           | Ja       | Ja             |
| Inkoopbeheer             |                                                                                           | Ja       | Ja             |
|                                      | Punch-out naar externe catalogus vanuit opdracht tot inkoop                                   | Ja       | Nee              |
|                                      | Power BI-rapporten - inkoop- en uitgavenanalyse                                                  | Ja       | Nee              |
| Productgegevensbeheer       |                                                                                           | Ja       | Ja             |
| Producthoofdgegevens                  |                                                                                           | Ja       | Ja             |
| Productie                           |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporten - productieprestaties                                                   | Ja       | Nee              |
| Projectbeheer en boekhouding    |                                                                                           | Ja       | Ja             |
| Verkoop                                |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporten - verkoop- en winstgevendheidsprestaties                                      | Ja       | Nee              |
| Beveiliging                             |                                                                                           | Ja       | Ja             |
| Servicebeheer                   |                                                                                           | Ja       | Ja             |
| Supply chain management              |                                                                                           | Ja       | Ja             |
| Transportbeheer            |                                                                                           | Ja       | Ja             |
| Leverancierssamenwerking                 |                                                                                           | Ja       | Nee              |
| Magazijnbeheer                 |                                                                                           | Ja       | Ja             |
|                                      | Mobiele magazijnapp                                                                      | Ja       | Ja             |
|                                      | Power BI-rapporten - magazijnbeheer                                                              | Ja       | Nee              |
| Webclient                           |                                                                                           | Ja       | Ja             |
|                                      | Taakregistratie: taakregistraties opslaan of laden uit de BPM-bibliotheek                         | Ja       | Nee              |
| Ondersteuning                              |                                                                                           | Ja       | Ja             |
|                                      | Toegang tot ondersteuning via het menu Help en ondersteuning                                             | Ja       | Nee              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Voor een lijst van mogelijkheden die in on-premises implementaties beschikbaar zijn, raadpleegt u [Functies in Commerce voor on-premises implementaties](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Gebied**         | **Functie**         | **Cloud** | **On-premises** |
|------------------|---------------------|-----------|-----------------|
| Alle Human Resources-gebieden | Alle Human Resources-functies | Ja       | Nee              |

## <a name="development-and-administration-features"></a>Ontwikkelings- en beheerfuncties

| **Gebied**                   | **Functie**                               | **Cloud** | **On-premises** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Maken en testen             |                                           | Ja       | Ja             |
| Uitbreidbaarheid              |                                           | Ja       | Ja             |
| Controle en telemetrie   |                                           | Ja       | Ja             |
| Platformcompatibiliteit     |                                           | Ja       | Ja             |
| Service                  |                                           | Ja       | Ja             |
|                            | Service-omgevingen                    | Ja       | No              |
| Traceparser               |                                           | Ja       | Ja             |
| PerfTimer                  |                                           | Ja       | Ja\*           |
| Bijwerken                    |                                           | Ja       | Ja             |
|                            | Bijwerken                                   | Ja       | No              |
|                            | Upgrade en ondersteuning voor eerdere versies | Ja       | No              |
| Visual Studio-ontwikkeling  |                                           | Ja       | Ja             |

\* In on-premises-omgevingen geeft PerfTimer alleen resultaten weer voor de client.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
