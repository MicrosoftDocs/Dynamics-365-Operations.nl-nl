---
title: De oplossing Invoice Capture configureren
description: In dit artikel wordt uitgelegd hoe u de oplossing Invoice Capture configureert.
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
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691147"
---
# <a name="configure-the-invoice-capture-solution"></a>De oplossing Invoice Capture configureren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nadat de oplossing Invoice Capture is geïnstalleerd, moet u de omgeving configureren. Het proces omvat de volgende basisstappen:

1. **Vereist:** de rechtspersonen synchroniseren vanuit Microsoft Dynamics 365 Finance. Deze stap wordt gebruikt om de organisatiestructuur in te stellen in Microsoft Power Platform.
2. **Vereist:** de kanalen voor het importeren van factuurafbeeldingen configureren. Het oplossing ondersteunt de volgende kanalen:

    - Office 365 Outlook (standaard)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Optioneel:** extra configuratiegroepen definiëren voor de OCR-service (Optical Character Recognition).
4. **Optioneel:** toewijzingsregels definiëren voor de rechtspersoon, leverancierrekening, artikel en inkooptype.

Dit artikel is gericht op de twee vereiste stappen van het proces. Zie [Configuratiegroepen voor de oplossing Invoice Capture](invoice-capture-config-group.md) voor meer informatie over configuratiegroepen. Zie [Toewijzingsregels voor de oplossing Invoice Capture](invoice-capture-mapping-rules.md) voor meer informatie over toewijzingsregels .

## <a name="manage-legal-entities"></a>Rechtspersonen beheren

In Finance worden rechtspersonen gedefinieerd als een organisaties die worden geïdentificeerd via registratie bij wettelijke instanties. Bedrijfsactiviteiten worden in afzonderlijke rechtspersonen uitgevoerd en vastgelegd. In Microsoft Power Platform zijn bedrijfseenheden, beveiligingsrollen en gebruikers aan elkaar gekoppeld op een manier die in overeenstemming is met het op rollen gebaseerde beveiligingsmodel.

Bedrijfseenheden worden samen met beveiligingsrollen gebruikt om de toegang tot gegevens te beheren. Gebruikers zien alleen de informatie die zij nodig hebben om hun werk te doen. De oplossing Invoice Capture biedt een configuratieruimte waar u basisinformatie van bestaande rechtspersonen in Finance kunt laden en die entiteiten kunt beheren die handmatig zijn gemaakt. De rechtspersonen worden gebruikt voor leveranciersfacturen en in beveiligingsbeheer.

Wanneer een rechtspersoon wordt gemaakt en weergegeven in de lijstweergave, wordt automatisch een standaardbedrijfseenheid met dezelfde naam gemaakt. Het team krijgt de beveiligingsrol van **Klantenadministrateur**. Wanneer rechtspersonen worden geïmporteerd, worden basismodelgegevens uit Finance geïmporteerd. De niet-bestaande artikelen worden geïdentificeerd door de rechtspersoon en toegevoegd aan de oplossing Invoice Capture. De standaardconfiguratiegroep wordt aan nieuwe rechtspersonen toegewezen.

### <a name="sync-legal-entities"></a>Rechtspersonen synchroniseren

U kunt rechtspersonen niet rechtstreeks maken. U kunt wel rechtspersonen synchroniseren vanuit Finance. Volg deze stappen om rechtspersonen te synchroniseren.

1. Ga naar **Instellingen \> Systeeminstellingen \> Rechtspersonen beheren**.
2. Selecteer **Rechtspersonen synchroniseren** en selecteer **OK** in het bevestigingsvenster.

Als de synchronisatie is voltooid, wordt het aantal nieuwe rechtspersonen weergegeven. De nieuwe rechtspersonen worden in de lijstweergave weergegeven. De standaardconfiguratiegroep wordt aan de nieuwe rechtspersonen toegewezen.

## <a name="configure-invoice-import-channels"></a>Kanalen voor het importeren van facturen configureren

Leveranciers verzenden facturen via verschillende kanalen (e-mail, bestandswerkgebied of factuurportal) en indelingen (papier of afbeelding). De oplossing Invoice Capture kan verschillende kanalen en indelingen verwerken. De volgende typen worden ondersteund:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Wanneer een kanaal wordt gemaakt voor een specifieke rekening, wordt een geautomatiseerde stroom met een vooraf gedefinieerde sjabloon gemaakt om de binnenkomende e-mails of bestanden in het Postvak IN of de ruimte te controleren. Alle bestanden met een geldige factuur kunnen worden herkend en verzonden naar het factuurgebied in afwachting van verwerking door de klantenadministrateur. De bijlage moet een PDF- of afbeeldingsindeling hebben. Facturen kunnen op basis van de kanaalconfiguratie in de oplossing Invoice Capture worden geladen.

### <a name="create-a-channel"></a>Een kanaal maken

Als u het extra oplossingspakket (Dynamics 365 Invoice Capture – Installation Tools) hebt geïmporteerd, is de standaardverbinding voor Office 365 Outlook gereed voor gebruik. Zie [Extra verbindingen voor kanalen maken](invoice-capture-advanced-settings.md#create-additional-connections-for-channels) als u meer verbindingen wilt maken voor verschillende e-mailaccounts of andere typen kanalen.

Volg deze stappen om een kanaal te maken.

1. Ga naar **Instellingen \> Systeeminstellingen \> Configuratiekanalen**.
2. Selecteer **Nieuw**.
3. Stel de volgende velden in:

    - Naam van kanaal
    - Description
    - Type
    - Verbinding

Alleen e-mails of bestanden die aan de volgende criteria voldoen, kunnen in de oplossing worden geïmporteerd.

| Type               | Configuratie  | Meer informatie |
|--------------------|----------------|------------------|
| Office 365 Outlook | Map         | De e-mailmap moet zich onder de hoofdmap bevinden. Standaard wordt de map Postvak IN gebruikt. Een submap wordt niet ondersteund. |
|                    | Onderwerpfilter | (Optioneel) Een subtekenreeks die in het onderwerp moet worden opgenomen. |
|                    | Vanaf           | (Optioneel) Het e-mailadres van de afzender(s). Als u meerdere adressen wilt opgeven, gebruikt u een puntkomma (;) als scheidingsteken. |
| SharePoint         | Siteadres   | De URL van het siteadres. |
|                    | Map         | De map op het siteadres. |

### <a name="activate-the-channel"></a>Het kanaal activeren

Wanneer een stroom wordt opgeslagen, worden in velden de status van het kanaal en het tijdstip waarop dit is gemaakt weergegeven. Het veld **Status** is in eerste instantie ingesteld op **Inactief**. Het veld **Reden van status** geeft aan dat het kanaal is geïnitialiseerd en gereed is om te worden geactiveerd.

Selecteer **Activeren** om het kanaal te activeren. De velden **Status** en **Reden van status** worden bijgewerkt.

Als een kanaal niet vereist is, kunt u het deactiveren. Selecteer **Deactiveren** om het kanaal te deactiveren. De velden **Status** en **Reden van status** worden bijgewerkt.

### <a name="manage-flows-in-flow-management"></a>Stromen in stroombeheer beheren

U kunt een kanaal weergeven op de pagina **Configuratiekanalen** of in stroombeheer.

Ga voor meer details naar **Beheersysteem \> Standaardoplossing \>Cloudstromen** en selecteer de doelstroom. De weergegeven details zijn onder andere gekoppelde verbindingen, eigenaren en uitvoeringsgeschiedenissen.

Als u de status wilt synchroniseren, selecteert u **Controleren** om te controleren of de status van het kanaal overeenkomt met de status van de stroom.

Sommige gevallen van uitzonderingsverwerking worden weergegeven in het veld **Reden van status**:

- **Ontbrekende Dataverse-verbinding**: de huidige gebruiker heeft niet minimaal één **Microsoft Dataverse**-verbindingsverwijzing gemaakt.
- **Niet gevonden**: de stroom die aan het kanaal is gekoppeld, is verwijderd in stroombeheer. Het kanaal moet opnieuw worden opgeslagen om een nieuw kanaal te maken.
- **Gedeactiveerd in stroombeheer**: de stroom is gedeactiveerd in stroombeheer en de status van het kanaal verschilt van de status van de stroom.
- **Geactiveerd in stroombeheer**: de stroom is geactiveerd in stroombeheer en de status van het kanaal verschilt van de status van de stroom.
- **Er is een onverwachte fout opgetreden**: de gebruiker moet bevestigen dat de site een communicatiesite is en dat de map Documentbibliotheek is.
