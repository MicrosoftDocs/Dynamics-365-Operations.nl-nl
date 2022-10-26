---
title: Geavanceerde instellingen voor de oplossing Invoice Capture
description: Dit artikel biedt informatie over geavanceerde instellingen in de oplossing Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691155"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Geavanceerde instellingen voor de oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dit artikel biedt informatie over geavanceerde instellingen in de oplossing Invoice Capture.

## <a name="create-additional-connections-for-channels"></a>Extra verbindingen voor kanalen maken

U moet verbindingen met e-mail of bestandsopslag maken om de controle van binnenkomende facturen vanuit verschillende kanalen mogelijk te maken. U moet in het begin verbindingen registreren om toegang te verlenen voor geautomatiseerde stromen die in de oplossing worden gebruikt.

De volgende verbindingstypen worden gebruikt om facturen te importeren:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Voor het kanaal voor het importeren van facturen worden de verbindingen in verdere configuratiestappen gebruikt. Voordat gebruikers een kanaal van een specifieke verbinding kunnen maken, moet aan hen de beveiligingsrol **Beheerder** worden toegewezen en moeten ze verbindingen maken.

Volg deze stappen om een verbinding met Microsoft Dataverse te maken.

1. Ga naar **Beheersysteem \> Standaardoplossing**.
2. Selecteer **Nieuw** en vervolgens **Verbindingsverwijzing**.
3. Geef in het veld **Weergavenaam** een naam op.
4. Selecteer **Microsoft Dataverse** als de connector.
5. Als u de verbinding voor het eerst instelt, selecteert u **Nieuwe verbinding**.
6. Maak in het dialoogvenster dat verschijnt een Dataverse-verbinding en selecteer vervolgens **Maken**.
7. Voer de Dataverse-account en het wachtwoord in.
8. Nadat de validatie is geslaagd, gaat u naar de verbindingspagina, selecteert u **Vernieuwen**, selecteert u de account en selecteert u **Maken**.

Voer de volgende stappen uit om verbinding met e-mail of een bestandsopslag te maken.

1. Selecteer op de pagina **Verbinding maken** in het veld **Verbindingstype** de waarde **Office 365 Outlook**.
2. Voor een e-mailverbinding kunt u **Outlook.com** of **Office 365 Outlook** als de connector selecteren. Voor een bestandsopslagverbinding kunt u **OneDrive** of **SharePoint** selecteren.

Als u bestaande verbindingen wilt controleren, gaat u naar **Standaardoplossing \> Objecten \> Verbindingsverwijzingen**. De gebruiker die kanalen maakt, moet minimaal één Dataverse-verbinding hebben naast specifieke e-mail- of bestandsopslagverbindingen. De maker van het nieuwe kanaal moet de eigenaar van de verbinding zijn.
