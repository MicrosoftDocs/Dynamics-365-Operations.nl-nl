---
title: Microsoft Project-clientintegratie
description: Een projectplanning plannen en onderhouden kan complex zijn, dus hebben projectmanagers hulpmiddelen nodig waarmee ze deze taak kunnen beheren. Integratie met Microsoft Project-client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "317471"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project-clientintegratie

[!include [banner](../includes/banner.md)]

Een projectplanning plannen en onderhouden kan complex zijn, dus hebben projectmanagers hulpmiddelen nodig waarmee ze deze taak kunnen beheren. Integratie met Microsoft Project-client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie. De projectmanager kan wijzigingen terug publiceren naar de projectstructuur voor werkspecificatie van Finance and Operations.

> [!NOTE]
> Als u Microsoft Dynamics 365 for Finance and Operations, update van juli gebruikt, moet u KB 4054797 en 4055884 installeren.

## <a name="configure-the-microsoft-project-client-add-in"></a>De invoegtoepassing voor de Microsoft Project-client configureren
Om integratie met de Microsoft Project-client mogelijk te maken, is installatie van een Microsoft Dynamics 365-invoegtoepassing vereist in de Microsoft Project-clienttoepassing van de gebruiker. Dit wordt gedaan door de **werkruimte Projectbeheer** te openen.

•   Klik op **De invoegtoepassing voor de Microsoft Project-client configureren** vanuit het gedeelte **Koppelingen** > **Instelling** van de werkruimte.

•   Klik op **openen** en klik vervolgens op **Uitvoeren** wanneer dat wordt gevraagd.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Een bestaand concept van een structuur voor werkspecificatie openen en bewerken in de Microsoft project-client
Als een project in Finance and Operations al een structuur voor werkspecificatie heeft gemaakt, kan de structuur voor werkspecificatie worden geopend in de Microsoft Project-clienttoepassing als de structuur voor werkspecificatie de conceptstatus heeft. Om te openen vanuit de pagina **Project**, klikt u op de koppeling **Openen in Microsoft Project** vanaf het tabblad **Plan**. Deze pagina kan ook worden geopend vanuit de clienttoepassing van Microsoft Project door te klikken op **Openen** op het tabblad **Microsoft Dynamics 365**. Selecteer de **Rechtspersoon** en het **Project** in de lijst.

> [!NOTE]
> Als u Internet Explorer als browser gebruikt, moet u klikken op **Opslaan** om handmatig te openen vanuit de locatie waarnaar het bestand is gedownload. Of klik op **Opslaan en openen** om het bestand te openen in de Microsoft project-client. Wijzig de bestandsnaam niet bij het opslaan.

Voordat u wijzigingen in het bestand aanbrengt met Microsoft Project-client, moet u het uitchecken. Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**. Dit voorkomt dat andere gebruikers de structuur voor werkspecificatie tegelijkertijd bewerken vanuit Finance and Operations. Als u de structuur voor werkspecificatie wilt publiceren na het voltooien van bewerkingen, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.

Als een projectteam al is toegevoegd aan het project in Finance and Operations, wordt de resourcelijst gevuld met de teamleden. Als een projectteam nog niet is toegevoegd aan het project, kunt u resources selecteren en het team in de Microsoft Project-client maken door te klikken op de knop **Resources** op het tabblad **Microsoft Dynamics 365**. 

De volgende gegevens worden terug gesynchroniseerd naar Finance and Operations als onderdeel van het incheckproces:

•   Taaknaam

•   Begindatum

•   Einddatum

•   Voorgangers

•   Bronnamen

•   Categorie

•   Resourcecategorie

•   Werkuren

•   Notities

•   Prioriteit

> [!NOTE]
> Als u meer kolommen aan het bestand Microsoft Project-clientbestand toevoegt, worden ze niet naar het bestand opgeslagen en worden ze niet weergegeven als het bestand opnieuw wordt geopend.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>De structuur voor werkspecificatie voor een bestaand project maken met behulp van de Microsoft Project-client
Als u een nieuwe structuur voor werkspecificatie wilt maken met Microsoft Project-client, volgt u deze stappen:


1.  Open de Microsoft Project-client.

2.  Klik op het tabblad **Microsoft Dynamics 365** op **Openen**.

3.  Selecteer de **rechtspersoon** voor het project.

4.  Selecteer het **Project**.

5.  Klik op **Uitchecken** op het tabblad **Microsoft Dynamics365**.

6.  Als u klaar bent om te publiceren naar Finance and Operations, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>De bestaande structuur voor werkspecificatie voor een bestaand project vervangen met de Microsoft Project-client
Als u een nieuwe structuur voor werkspecificatie wilt maken met behulp van de Microsoft Project-client en een bestaande structuur voor werkspecificatie voor een bestaand project wilt vervangen, gaat u als volgt te werk:

1.  Open de Microsoft Project-client.

2.  Maak de planning in de Microsoft Project-client.

3.  Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Bestaand project vervangen**.

4.  Selecteer de **rechtspersoon** voor het project.

5.  Selecteer het **Project**.

6.  Klik tot slot op **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Een nieuw project maken vanuit de Microsoft project-client


1.  Open de Microsoft Project-client.

2.  Maak de planning in de Microsoft Project-client.

3.  Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Opslaan in nieuw project**.

4.  Selecteer de **rechtspersoon** voor het project.

5.  Voer indien nodig de **project-id** in.

6.  Voer de **projectnaam** in.

7.  Selecteer het **projecttype**, de **projectgroep** en de **projectcontract-id**. U kunt ook een nieuw projectcontract maken door te klikken op **Nieuw**.

8.  Selecteer de **kalender** die voor resourcing moet worden gebruikt.

11. Klik tot slot op **OK**.
