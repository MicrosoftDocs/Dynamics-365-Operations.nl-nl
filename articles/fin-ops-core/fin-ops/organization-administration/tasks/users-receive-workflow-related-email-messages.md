---
title: Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom
description: U kunt het systeem configureren voor het verzenden van e-mailberichten aan werknemers als er werkstroom-gerelateerde zaken optreden.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3207727c8deba97eebfd7516e9600238e5e79b3d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747244"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Gebruikers toestaan om e-mailberichten te ontvangen die betrekking hebben op de werkstroom

[!include [banner](../../includes/banner.md)]

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

> [!NOTE]
> De e-mailsjablonen voor workflows zijn e-mailsjablonen van het systeem of de organisatie, afhankelijk van of de workflow van systeemniveau (bedrijfsspecifiek) of organisatieniveau (bedrijfsspecifieke) is.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]