---
title: Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom
description: U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189839"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom

[!include [task guide banner](../../includes/task-guide-banner.md)]

U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden. Er kan bijvoorbeeld een e-mailbericht naar een gebruiker worden verzonden wanneer deze een document voor goedkeuring toegewezen krijgt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.

1. Ga naar **Navigatievenster > Modules > Systeembeheer > Gebruikers > Gebruikers**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in het **actievenster** op **Gebruikersopties**.
4. Klik op het tabblad **Workflow**. Controleer of de sectie **Meldingen** is uitgevouwen. Geef in de sectie **Meldingen** op hoe de gebruiker geïnformeerd moet worden over zaken die betrekking hebben op workflows.  
5. Selecteer een optie in het veld **Meldingtype workflow voor regelartikelen**.
    - Gegroepeerd: Regelartikelmeldingen worden gegroepeerd tot één e-mailbericht.
    - Individueel: Een e-mailbericht wordt verzonden voor elk regelartikel.  
    - Als u wilt dat de gebruiker meldingen ontvangt in de client, schakelt u het selectievakje **Meldingen verzenden in e-mail** in.  
6. Klik op **Opslaan**.
7. Sluit de pagina.

