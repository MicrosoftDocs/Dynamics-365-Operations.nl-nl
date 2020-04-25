---
title: Een voorkeurstechnicus instellen
description: U kunt een willekeurige werknemer selecteren als voorkeurstechnicus voor een serviceovereenkomst of serviceorder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea0265eb27fb5cf32f5f921caa7ac2e44a0116
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217282"
---
# <a name="set-up-a-preferred-technician"></a>Een voorkeurstechnicus instellen 

[!include [banner](../includes/banner.md)]


U kunt een willekeurige werknemer selecteren als voorkeurstechnicus voor een serviceovereenkomst of serviceorder. Het is echter een goed idee om de werknemer toe te voegen aan het relevante verzendteam zodat de werknemer is opgenomen op het **Verzendgroep**.

## <a name="assign-employee-to-a-dispatch-team"></a>Een werknemer toewijzen aan een verzendteam

1.  Klik op **Human resources** \> **Algemeen** \> **Medewerkers** \> **Medewerkers**. Dubbelklik op een werknemer om de detailpagina van de werknemer te openen. Klik in het **Actievenster** op **Instellen** \> **Verzendteam** om het formulier **Verzendmedewerkers** te openen.

2.  Selecteer in het veld **Verzendteam** het team om toe te wijzen aan de werknemer.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Een voorkeurstechnicus toewijzen aan een serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**. Dubbelklik op een serviceovereenkomst om het detailformulier te openen.

2.  Selecteer op het tabblad **Algemeen** het veld **Voorkeurstechnicus** en selecteer vervolgens een lid van het relevante verzendteam als de voorkeurstechnicus voor de serviceovereenkomst.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Een voorkeurstechnicus toewijzen aan een serviceorder

1.  Klik op **Servicebeheer** \> **Periodiek** \> **Verzendbord**.
    

    > [!NOTE]
    > <P>Geef in het formulier <STRONG>Verzendbord</STRONG> een datumbereik op voor de verzendactiviteiten die u wilt weergeven. Geef ook op of afgesloten activiteiten moeten worden weergegeven en of de lijst met verzendactiviteiten moet worden beperkt tot teams waartoe u behoort of waarvoor u bevoegd bent om deze te controleren. Klik op <STRONG>OK</STRONG> om het formulier <STRONG>Verzendbord</STRONG> te openen.</P>



2.  Selecteer de regel van de te wijzigen serviceactiviteit.

3.  Gebruik op het tabblad **Verwant** de lijst **Werknemer** om een lid van het relevante verzendteam toe te wijzen als voorkeurstechnicus voor de servicebeurt.

## <a name="see-also"></a>Zie ook

[Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen](service-agreements.md)

[Handmatig serviceorders maken](create-service-orders-manually.md)

[Serviceovereenkomsten (formulier)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  


