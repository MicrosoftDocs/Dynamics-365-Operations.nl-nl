---
title: Een projectteam maken
description: Dit onderwerp biedt informatie over het maken en beheren van projectteams.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760514"
---
# <a name="create-a-project-team"></a>Een projectteam maken

[!include [banner](../includes/banner.md)]

Om de rollen te gebruiken die eerder in een project zijn geconfigureerd, moet een projectmanager de rollen aan het project koppelen. Voor een project kunnen meerdere rollen worden toegewezen. Om verwarring te voorkomen, worden deze rollen automatisch gelabeld tijdens de reservering. Als de projectmanager drie software-engineers nodig heeft, worden bijvoorbeeld automatisch drie software-engineerrollen gegenereerd met de labels **Software-engineer 1**, **Software-engineer 2** en **Software-engineer 3**. Als voor de rol eerder rolkenmerken zijn ingesteld, worden deze toegepast als filter in zoekopdrachten naar een resource. Aanvullende kenmerken kunnen indien nodig worden toegevoegd om het zoeken te verfijnen.

Weergave-instellingen kunnen ook worden aangepast voor een betere weergave van de beschikbaarheid van resources. Er zijn opties voor weergave van beschikbaarheid per uur, dag, week, maand, kwartaal en jaar. Er is ook een optie om beschikbaar en resterende capaciteit van resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u beschikbare tijd voor activiteiten of resourcebeschikbaarheid raamt.

De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereisten voldoet, daarvoor een resource reserveren die de rol vervult. De resources hoeven niet op dit moment in de planningsfase te worden gereserveerd. Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project. Als rollen worden vervangen door bemande rollen in de WBS, werkt de resourceconfiguratie automatisch de projectteamlijst en de planning bij.

[![Projectteamlijst die zowel rollen als werkelijke resources bevat](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende opties om een resource op een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Percentage van capaciteit** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen wijzigen. Twee typen boeking worden ondersteund:

- **Vast boeken**: De resourcereservering is goedgekeurd en is bevestigd om aan de taak te werken voor de opgegeven periode.
- **Variabel boeken**: De resourcereservering is voorlopig ingesteld om aan de taak te werken voor de opgegeven periode.

De onderstaande procedure licht toe hoe u een projectteam maakt.

## <a name="create-a-project-team"></a>Een projectteam maken

1. Selecteer een project op de lijstpagina **Alle projecten** en selecteer **Bewerken**.
2. Voer op het tabblad **Projectteam en planning** in het veld **Planning einddatum** de begindatum van het schema plus één maand in. Als bijvoorbeeld de planningbegindatum 24 juni 2017 is (24-06-2017), voert u **24-07-2017** in.
3. Selecteer **Toevoegen**.
4. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Senior projectmanager**.
5. Selecteer **Vereiste competenties**.
6. Op de pagina **Kenmerken kiezen** zijn de kenmerken die u eerder hebt ingesteld voor de rol Senior projectmanager automatisch geselecteerd. Selecteer **OK**.
7. Voer op de pagina **Rollen toevoegen aan project** in het veld **Aantal resources** de waarde **1** in.
8. In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en **Maken**.
9. Selecteer op de pagina **Project** de optie **Toevoegen**.
10. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Selecteer **Maken**.
12. Selecteer op de pagina **Projecten** de optie **Voorzien in resource**.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1. Selecteer op de pagina **Alle projecten** de koppeling **Project-ID** voor het project **XYZ-upgrade Fase 2**.
2. Controleer op het sneltabblad **Projectteam en planning** of de daar vermelde projectresources correct zijn.
