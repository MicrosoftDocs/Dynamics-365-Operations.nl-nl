---
title: Toegang voor werknemers per rechtspersoon beperken
description: In dit artikel wordt uitgelegd hoe u toegang voor werknemers kunt instellen per rechtspersoon.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780388"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Toegang voor werknemers per rechtspersoon beperken

In dit artikel wordt uitgelegd hoe u toegang voor werknemers kunt instellen per rechtspersoon.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Werknemers zijn in dienst bij rechtspersonen. Hieronder volgen een aantal voorbeelden:

- Aaron Con is werknemer van de rechtspersoon USSI.
- Ahmed Barnett is werknemer van de rechtspersoon USMF.
- Alicia Thornber is in dienst van de rechtspersonen GLSI en USMF.

Afhankelijk van de rol van een gebruiker in het bedrijf, kan het zijn dat de gebruiker toegang nodig heeft om alle werknemers in alle rechtspersonen weer te geven. Of een gebruiker moet worden beperkt, zodat alleen werknemers in de rechtspersoon zichtbaar zijn waarvoor ze toegang hebben. Als u wilt bepalen welke werknemers een gebruiker kan weergeven, selecteert u de parameter **Toegang tot werknemersgegevens beperken** op de pagina **Gedeelde Human Resources-parameters** .

Een gebruiker heeft bijvoorbeeld toegang tot de pagina **Werknemer** en heeft alleen toegang tot de rechtspersoon USMF. In dit geval kan de gebruiker de volgende informatie weergeven voor de werknemers in de voorgaande lijst:

- Als de functie voor het beperken van de toegang tot werknemersgegevens niet is ingeschakeld, kan de gebruiker informatie weergeven voor Aaron, Ahmed en Alicia.
- Als de functie is ingeschakeld, kan de gebruiker alleen informatie weergeven voor Ahmed en Alicia, omdat ze ook bij de rechtspersoon USMF in dienst zijn.

Welke informatie wordt weergegeven, is afhankelijk van de toepassing die u gebruikt.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources als zelfstandige toepassing

Als de functie voor het beperken van toegang tot werknemergegevens is ingeschakeld, ziet de beperkte gebruiker een lege waarde in sommige lijsten die de naam van de werknemer bevatten.

Een gebruiker die bijvoorbeeld alleen toegang heeft tot de rechtspersoon USMF, ziet het volgende gedrag:

- In de lijst **Actieve posities** is de kolom **Werknemer** leeg voor de positie van Aaron omdat de gebruiker geen toegang heeft tot werknemers in de rechtspersoon USSI.
- Als de gebruiker inzoomt op de naam van de werknemer, wordt er een lege pagina **Werknemer** weergegeven.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources met Finance-infrastructuur

Als de functie voor het beperken van toegang tot werknemergegevens is ingeschakeld, ziet de beperkte gebruiker de naam van de werknemer in sommige lijsten.

Een gebruiker die bijvoorbeeld alleen toegang heeft tot de rechtspersoon USMF, ziet het volgende gedrag:

- In de lijst **Actieve posities** wordt de naam Aaron in de kolom **Werknemer** weergegeven. Als de gebruiker met de muis over de naam van de werknemer beweegt, worden alleen de naam en de functie weergegeven.
- Als de gebruiker inzoomt op de naam van de werknemer, wordt er een lege pagina **Werknemer** weergegeven.

> [!TIP]
> Als u Dynamics 365 Human Resources met een Finance-infrastructuur gebruikt en wilt dat beperkte gebruikers lege waarden voor namen van werknemers zien, kunt u de beveiligingsbevoegdheid **Toegang tot werknemers beperken** toevoegen aan de gebruikersrollen op de pagina **Beveiligingsconfiguratie**.

Nadat u de functie hebt ingeschakeld, moet u extra stappen uitvoeren om machtigingen in te stellen voor elke gebruiker van wie de weergave moet worden beperkt.

1. Selecteer een gebruiker op de pagina **Gebruikers**.
2. Selecteer een rol voor de gebruiker. De optie **Organisaties toewijzen** komt beschikbaar.
3. Selecteer **Organisaties toewijzen**.
4. Selecteer op de nieuwe pagina **De toegang verlenen tot specifieke organisaties** en selecteer vervolgens de organisaties waartoe de gebruiker toegang moet hebben.
5. Herhaal stap 2 tot en met 4 voor elke andere rol die de gebruiker heeft, inclusief de rol van de systeemgebruiker.

> [!NOTE]
> De rechtspersonen waartoe een gebruiker toegang heeft, moeten overeenkomen met alle rollen van de gebruiker.
