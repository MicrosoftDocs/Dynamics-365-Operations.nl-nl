---
title: Vergoedingenoverzicht
description: In het rapport Vergoedingenoverzicht wordt aangegeven voor welke vergoedingen een werknemer momenteel is ingeschreven.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 65bf91faba049b3fed4d80e020d77b82e48cceb6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068990"
---
# <a name="benefit-statement"></a>Vergoedingenoverzicht


[!INCLUDE [PEAP](../includes/peap-2.md)]

Het rapport **Vergoedingenoverzicht** biedt een overzicht van de vergoedingen waarvoor een werknemer momenteel is ingeschreven. Het rapport is rechtstreeks toegankelijk voor een werknemer of voor de beheerder van de vergoeding. Het **Vergoedingenoverzicht** biedt een lijst met de vergoedingen waarvoor de werknemers is ingeschreven, opties voor dekking, kosten en alle geregistreerde afhankelijken of begunstigden. Het overzicht kan worden afgedrukt voor één of meerdere werknemers.

> [!NOTE]
De functie **Vergoedingenbeheer** moet in de werkruimte **Functiebeheer** zijn ingeschakeld. Als u dit wilt doen, moet de functie **Vergoedingenbeheer** zijn ingeschakeld in Functiebeheer. 


## <a name="importing-the-benefit-statement"></a>Het vergoedingsoverzicht importeren 

U moet het **Vergoedingsoverzicht** met behulp van de rapportconfiguratie importeren voordat het **Vergoedingsoverzicht** beschikbaar is. Hiervoor moet u de volgende stappen uitvoeren:

1.  Ga naar de werkruimte **Systeembeheer**.

2.  Selecteer de tegel **Elektronische rapportage**.

3.  Ga naar **Configuratieproviders** en selecteer **Opslagplaatsen**.

  ![Selecteer Opslagplaatsen.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Selecteer **HR-resources** in de lijst en selecteer vervolgens **Openen**.

    ![Opslagplaatsen van configuraties.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Selecteer het **Model voor vergoedingsoverzicht** in het linkerdeelvenster en vouw het uit zodat **Indeling voor vergoedingsoverzicht** wordt weergegeven.

6.  Selecteer **Indeling voor vergoedingsoverzicht** in het linkerdeelvenster.

7.  Aan de rechterkant van het scherm wordt het sneltabblad **Versies** weergegeven. Selecteer **Importeren**.

    ![Sneltabblad Versies.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Het vergoedingsoverzicht genereren als PDF-bestand

Het **Vergoedingsoverzicht** wordt standaard als Microsoft Word-document afgedrukt. Als u het overzicht wilt afdrukken in de PDF-indeling, moet u de PDF-optie configureren in **Bestemming elektronische rapportage**. 

1. U kunt dit doen door naar de werkruimte **Systeembeheer** > **Elektronische rapportage** > **Gerelateerde koppelingen** > **Bestemming elektronische rapportage** te gaan.

1.  Selecteer **Nieuw**.

2.  Selecteer in het veld **Verwijzing** de indeling **Indeling vergoedingsoverzicht**.

3.  Selecteer **Nieuw** op het sneltabblad **Bestandsbestemming**.

4.  Voer in het veld **Naam** de waarde **PDF vergoedingenoverzicht** in.

5.  Selecteer in het veld **Naam bestandsonderdeel** de optie **Vergoedingenoverzicht**.

6.  Selecteer het selectievakje **Converteren naar PDF**.

7.  Selecteer **Instellingen** in de menu. 

    ![Bestandsbestemming.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Selecteer het sneltabblad **Bestand** en selecteer vervolgens **Ingeschakeld**.

9.  Selecteer **OK**.
   
> [!NOTE]
> De functie Vergoedingsbeheer heeft de previewstatus. Er is een bekend probleem bij het gebruik van de instelling voor de e-mailbestemming in het rapport **Bestemming elektronische rapportage**. Er wordt mogelijk een foutbericht weergegeven en het verzenden van het e-mailbericht mislukt.

Het **Vergoedingenoverzicht** kan vanaf de volgende pagina's worden gegenereerd:

-   Werkruimte **Vergoedingenbeheer** > **Koppelingen** > **Rapporten** > **Vergoedingenoverzicht**

-   **Werknemers (verouderd formulier)** > **Tabblad Persoonlijke gegevens** > **Vergoedingenoverzicht**

-   **Gestroomlijnde werknemersinvoer** > **Vergoedingenrapporten** > **Vergoedingenoverzicht**

-   **Werknemerszelfservice** > **Vergoedingen** > **Vergoedingenoverzicht weergeven**

> [!NOTE]
>  De toegang tot het **Vergoedingenoverzicht** in **Werknemerselfservice** wordt geregeld door de bevoegdheid **Vergoedingenoverzicht weergeven**. Dit valt onder de functie **Vergoedingen werknemerselfservice**. Deze bevoegdheid wordt standaard verleend aan werknemers.

## <a name="report-contents"></a>Inhoud van rapport

In **Vergoedingenoverzicht** worden de bevestigde planselecties van de werknemer afgedrukt, inclusief eventuele kwijtgescholden plannen. In de volgende afbeelding ziet u een voorbeeld van dit rapport. 

![Rapport vergoedingenoverzicht.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

In het rapport worden het **Plan**, de **Dekkingsoptie**, de **Werknemerskosten** en de **Werkgeverkosten** weergegeven. In het rapport worden ook eventuele afhankelijken vermeld. Als aan het plan begunstigden zijn gekoppeld, worden de begunstigden en hun distributiesprioriteit en -percentage weergegeven.

Het rapport **Vergoedingenoverzicht** kan voor meerdere werknemers tegelijk worden afgedrukt met de records via het sneltabblad **Op te nemen records** op de pagina **Vergoedingenoverzicht**.
