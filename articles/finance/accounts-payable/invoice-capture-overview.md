---
title: Overzicht van de oplossing Invoice Capture
description: Dit artikel biedt informatie over de oplossing Invoice Capture.
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
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691164"
---
# <a name="invoice-capture-solution"></a>De oplossing Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dit artikel biedt informatie over de oplossing Invoice Capture die automatisch leveranciersfacturen van digitale factuurafbeeldingen maakt.

De afdeling Leveranciers beheert en verwerkt facturen voor ontvangen goederen en services. De leveranciersboekhouder controleert gegevens op leveranciersfacturen om de volgende redenen:

- Om extra werk voor aanpassingen of correcties tijdens het sluiten van perioden te voorkomen
- Om leveranciersfacturen op tijd te betalen en financiële verliezen als gevolg van fouten of fraude voorkomen

OCR (Optical Character Recognition) is de afgelopen jaren op grote schaal gebruikt door verschillende bedrijfstakken. Het is nu gebruikelijk dat afgedrukte teksten worden gedigitaliseerd, zodat ze elektronisch kunnen worden bewerkt, kunnen worden doorzocht, compacter kunnen worden opgeslagen en online kunnen worden weergegeven. De digitale tekst kan worden gebruikt in machineprocessen, zoals cognitieve gegevensverwerking, machinevertaling, de omzetting van tekst naar spraak, sleutelgegevens en tekst-mining.

Dankzij de ontwikkeling van AI-technologie kunnen moderne OCR-oplossingen verschillende factuurindelingen van verschillende leveranciers gebruiken zonder dat er veel menselijke tussenkomst nodig is. Meer bedrijven zien in dat ze geld kunnen besparen en de nauwkeurigheid kunnen verbeteren door facturen te verwerken via automatisering in plaats van handmatige verwerking.

## <a name="system-landscape"></a>Systeemlandschap

Hieronder ziet u een voorbeeld van de belangrijkste onderdelen en stappen in de oplossing Invoice Capture.

[![Onderdelen en stappen in de oplossing Invoice Capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Vereiste rollen

In de volgende tabel ziet u de rollen die nodig zijn om de oplossing Invoice Capture in te stellen en te gebruiken.

| Rol          | Acties | Systemen | Rolnamen |
|---------------|---------|---------|-----------|
| Beheerder | <ul><li>Omgevingen instellen in Microsoft Power Platform.</li><li>Oplossingen in Microsoft Power Platform implementeren.</li><li>Verbindingen instellen tussen Dynamics 365 en AI Builder.</li><li>Azure Data Lake Storage-locaties instellen.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365-beheerder</li><li>Power Platform-beheerder</li><li>Eigenaar van gegevens in opslagblob</li></ul> |
| AI-maker      | <ul><li>Stromen beheren.</li><li>Aangepaste AI-modellen maken.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Citizen makers</li></ul> |
| Klantenadministrateur      | <ul><li>Acties controleren en uitvoeren op het faseringsgebied van leveranciersfacturen.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Nieuwe rol van klantenadministrateur in Power Platform</li></ul> |
| Klantenadministrateur      | <ul><li>Dagelijkse bewerkingen uitvoeren als klantenadministrateur.</li><li>Navigeren naar het faseringsgebied voor leveranciersfacturen.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Leveranciersmedewerker</li></ul> |
  
Zie [Invoice Capture installeren](../accounts-payable/install-invoice-capture.md) voor meer informatie over het installeren van Invoice Capture.  
