---
title: Beveiligingsconfiguratieconcepten voor integraties op basis van virtuele tabel
description: In dit artikel wordt een architectuur beschreven voor het bouwen van een integratie tussen Microsoft Dynamics 365 Human Resources en andere systemen.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759650"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Beveiligingsconfiguratieconcepten voor integraties op basis van virtuele tabel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Het artikel beschrijft een architectuur voor het gebruiken van [Microsoft Dataverse-virtuele tabellen (entiteiten)](/dev-itpro/power-platform/virtual-entities-overview) om een integratie op te bouwen tussen Dynamics 365 Human Resources en een systeem van derden. De focus van het artikel ligt op de beveiligingsconfiguratie en op de verificatie- en autorisatieaspecten die tussen de systeemgrenzen zijn vereist om een functioneel, beveiligd systeem te bouwen.

## <a name="prerequisite-reference-articles"></a>Referentieartikelen over vereisten

De volgende artikelen bevatten meer informatie over de concepten in dit artikel:

- [Overzicht van virtuele entiteiten](/dev-itpro/power-platform/virtual-entities-overview)
- [Aan de slag met virtuele tabellen (entiteiten)](/developer/data-platform/virtual-entities/get-started-ve)
- [Server-naar-serververificatie gebruiken voor meerdere tenants (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [OAuth-verificatie gebruiken met Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [Referentiestroom van OAuth 2.0-clients op het Microsoft-identiteitsplatform](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Verificatie en autorisatie](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Architectuur 

In het volgende architectuurdiagram worden de belangrijkste concepten weergegeven die zijn betrokken bij een integratie waarin virtuele tabellen (entiteiten) worden gebruikt.

![Integratie op basis van virtuele tabel.](./media/Hosts.jpg)

Hier vindt u een uitleg van een aantal elementen in het voorgaande diagram:

- **Microsoft**: Microsoft beheert en gebruikt de verschillende Dynamics 365-producten namens klanten.

    - **Azure Active Directory (Azure AD) tenant C**: een Azure AD-tenant die eigendom is van Microsoft. In deze tenant zijn de Dynamics 365-toepassingen geregistreerd.

- **Partner integreren**

    - **Integratiesysteem**: het systeem dat wordt geïntegreerd met Dynamics 365. Dit kan een salarissysteem zijn of een systeem dat is gebaseerd op gegevens die zijn opgeslagen in Dynamics 365.
    - **Adapter**: de software of service die verantwoordelijk is voor de interactie met Dynamics 365 en het integratiesysteem.

        > [!NOTE]
        > Als een adapter door meerdere Dynamics 365-klanten moet worden gebruikt, is het de bedoeling dat deze als een multitenanttoepassing wordt geregistreerd in Azure AD.

    - **Azure AD-tenant A**: een Azure AD-tenant die het eigendom is van de integratiepartner. In deze tenant is de toepassings-id van de adapter geregistreerd.

- **Wederzijdse klant**: een klant die de oplossing van Dynamics 365 Human Resources en de integratiepartner implementeert.

    - **Dynamics 365 Finance of Human Resources**: het klantspecifieke exemplaar van Dynamics 365 Finance of Human Resources dat de klantgegevens bevat die door het integratiesysteem worden vereist.
    - **Dataverse**: de klantspecifieke Dataverse-omgeving die is gekoppeld aan Finance of Human Resources. Dataverse biedt een web-API voor interactie met Dynamics 365-gegevens.
    - **Azure AD-tenant B**: de Azure AD-tenant van de klant. Deze fungeert als identiteitsprovider (autorisatieserver) en geeft tokens uit waarmee aanroepers worden geautoriseerd om het Dataverse-exemplaar van de klant aan te roepen.

## <a name="basic-request-flow"></a>Basisaanvraagstroom

In deze sectie wordt de basisstroom beschreven van een standaardaanvraag die betrokken is bij een integratie. Deze verwijst naar het architectuurdiagram eerder in dit artikel.

Bij een standaardaanvraag moet de adapter een query op Dynamics 365 uitvoeren voor gegevens en deze gegevens vervolgens opslaan en synchroniseren met het integratiesysteem.

1. De adapter roept de web-API van Dataverse aan om query's uit te voeren voor relevante gegevens.

    > [!NOTE]
    > Verificatie is een vereiste en het verwerven van tokens is een hoofdonderdeel van het proces. Verificatie wordt beschreven in de sectie [Verificatie en autorisatie bij systeemgrenzen](#authentication-and-authorization-at-system-boundaries).

    Deze aanroep wordt gedaan op basis van de web-API van Dataverse om een query uit te voeren op toepassingsgegevens die beschikbaar worden gemaakt via een virtuele tabel. (Zie "2. Initiële synchronisatie" en "3. Deltasynchronisatie" in het diagram.)

2. Dataverse verwerkt de aanvraag door een query uit te voeren op de virtuele tabel via de invoegtoepassing Virtuele entiteit ("Virtuele tabelproxy" in het diagram). De Dataverse-aanvraag wordt doorgestuurd naar de virtuele entiteitsservice Finance of Human Resources om een query uit te voeren op de gegevens die fysiek zijn opgeslagen in de database van Finance of Human Resources.
3. De virtuele entiteitsservice Finance of Human Resources zet de aanvraag op basis van de virtuele entiteit om in een query voor de Finance of Human Resources-entiteit waarmee de virtuele Dataverse-entiteit wordt ondersteund. De gegevens worden opgehaald uit de database, omgezet naar de Dataverse-entiteitsweergave en teruggestuurd naar de aanroeper.
4. De adapter voltooit de vereiste toewijzing en gegevensvertaling en start een aanroep naar het integratiesysteem om de gegevens in de database van het integratiesysteem te gebruiken. (Zie "4. Gegevens opslaan" in het diagram.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Verificatie en autorisatie bij systeemgrenzen

Met *verificatie* wordt gevalideerd dat de identiteit van een gebruiker of toepassing is bevestigd en dat de gebruiker of de toepassing correct zijn. *Autorisatie* verleent de gebruiker of toepassing het recht om toegang te krijgen tot specifieke machtigingen op toepassingsniveau. Zie [Verificatie versus autorisatie](/azure/active-directory/develop/authentication-vs-authorization) voor meer informatie.

Bij de meeste oproepen tussen systemen in het eerder in dit artikel beschreven architectuurdiagram is de adapter betrokken. De adapter moet worden geverifieerd om de volgende aanroepen te doen:

- Aanroep naar Dataverse
- Aanroep naar het integratiesysteem

Bekijk de systeemgrenzen in het diagram. Elke webaanvraag tussen systemen moet worden geverifieerd en autorisatiecontroles op toepassingsniveau moeten worden doorgegeven voordat de gegevens aan de aanroeper worden geretourneerd. Voor een aanvraag tegen een virtuele tabel van Dynamics 365 die is gebaseerd op Finance of Human Resources, worden verificatie- en autorisatiecontroles afgedwongen bij de volgende systeemgrenzen:

- De aanroep tussen de adapter en het eindpunt van de Dataverse-web-API (OData)
- De aanroep tussen de Dataverse-invoegtoepassing voor virtuele entiteit en de virtuele entiteitsservice Finance of Human Resources

In beide gevallen worden verificatiecontroles eerst uitgevoerd. Vervolgens worden er autorisatiecontroles op toepassingsniveau uitgevoerd om ervoor te zorgen dat de geverifieerde gebruiker of toepassing de juiste bevoegdheden op toepassingsniveau heeft om de aangevraagde gegevens op te halen.

De verificatie voor het aanroepen van Dataverse wordt verwerkt via een bearer-token dat als een HTTP-kop in de webaanvraag aan Dataverse moet worden opgenomen. De adapter moet een token krijgen van het tenant B-exemplaar van Azure AD. (Zie "1. Token ophalen" in het diagram.) Azure AD fungeert als identiteitsprovider in de verificatiestroom.

De adapter verifieert door de toepassings-id (niet-geheim, zoals geregistreerd in Azure AD-tenant A) en een toepassingsgeheim of certificaat in te dienen dat alleen de adaptertoepassing heeft.

Nadat de gebruiker of toepassing is geverifieerd om aanroepen te doen naar Dataverse, worden op Dataverse-niveau autorisatiecontroles uitgevoerd voor elke aanvraag. Met deze controles controleert u of de aanroeper (de identiteit van de adaptertoepassing, die in het diagram is aangeduid als \<guid A\>) over de juiste machtigingen beschikt. Autorisatie op toepassingsniveau wordt beheerd in Dataverse via een toepassingsgebruiker die de toepassings-id van de adapter vertegenwoordigt. Machtigingen op toepassingsniveau worden beheerd door toegang te verlenen tot specifieke in Dataverse gedefinieerde toepassingsrollen. Deze rollen geven gedetailleerde bevoegdheden voor de toepassing.

Zie voor meerdere instructies [Server-naar-serververificatie gebruiken voor meerdere tenants](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Als de machtigingscontroles op Dataverse-niveau zijn geslaagd, doet de invoegtoepassing voor de virtuele entiteit een aanroep naar het eindpunt van de virtuele entiteitsservice in de omgeving van Finance of Human Resources. Server-naar-serververificatie (S2S) wordt gebruikt voor deze aanroep. Het gebruikt de identiteit en het geheim die zijn geconfigureerd in de configuratierecord van de virtuele gegevensbron van Finance and Operations.

![Configuratierecord van de virtuele gegevensbron van Finance and Operations in de sandbox-omgeving.](./media/sandbox.jpg)

Zie [Virtuele Dataverse-entiteiten configureren](/dev-itpro/power-platform/admin-reference) voor meer informatie.

De aanroep van de Dataverse-invoegtoepassing voor de virtuele entiteit naar Finance of Human Resources omvat de adapteridentiteit van de oorspronkelijke aanroep naar Dataverse vanuit de adapter (de identiteit die in het architectuurdiagram is aangeduid als \<guid A\>). Als de gegevensbron van de virtuele entiteit juist is geconfigureerd en de S2S-verificatiecontroles zijn geslaagd, wordt de query uitgevoerd door de virtuele entiteitsservice van Finance of Human Resources in de context van de oorspronkelijke aanroeper (de adapter, \<guid A\>). Op het niveau van Finance of Human Resources worden de machtigingen voor de toepassing gecontroleerd (autorisatie) om ervoor te zorgen dat de adapter de bevoegdheden heeft die zijn vereist voor het openen van de gegevensentiteiten die via de query worden aangevraagd.

De beveiliging van Finance en Human Resources wordt op de volgende manieren beheerd:

1. Door de adapteridentiteit (\<guid A\>) toe te wijzen aan een specifieke Finance- of Human Resources-gebruiker. Deze toewijzing wordt uitgevoerd op de pagina **Azure Active Directory-toepassingen**. Zie [Uw externe toepassing registreren](/dev-itpro/data-entities/services-home-page.md#register-your-external-application) voor meer informatie.
2. Door de Finance- of Human Resources-gebruiker de juiste rollen, functies en bevoegdheden op toepassingsniveau te verlenen. Zie voor meer informatie [Op rollen gebaseerde beveiliging](/dev-itpro/sysadmin/role-based-security).

Als aan de adaptertoepassing (\<guid A\>) de bevoegdheden worden toegekend die zijn vereist om toegang te krijgen tot de gevraagde gegevens, vinden de volgende gebeurtenissen plaats:

1. De query wordt uitgevoerd.
2. De gegevens worden terugvertaald naar de Dataverse-entiteitspagina.
3. De gegevens worden teruggestuurd naar de adapter.

> [!IMPORTANT]
> Tijdens de ontwikkeling kan de adapter worden uitgevoerd door een Finance- of Human Resources-gebruiker met de rol Beheerder. In een productieomgeving moet de adapter echter nooit worden uitgevoerd met beheerdersbevoegdheden.

## <a name="key-takeaways"></a>Hoofdpunten

Hieronder staan enkele belangrijke implicaties van de virtuele tabel- of entiteitsarchitectuur:

- De beveiligingsconfiguratie voor virtuele tabellen die worden ondersteund door Human Resources wordt beheerd in Human Resources.
- De klant ("Wederzijdse klant" in het architectuurdiagram eerder in dit artikel) heeft volledige controle over welke bevoegdheden aan de integratieadapter-id worden toegekend (aangeduid als "\<guid A\>" in het diagram).
- De klant is verantwoordelijk voor de juiste beveiligingsconfiguratie van de Human Resources-omgeving. De integratiepartner die de adapter maakt, moet richtlijnen aanleveren voor de bevoegdheden die de adapter nodig heeft.
