---
title: Redencodes voor voorraadtelling
description: Dit onderwerp beschrijft hoe u redencodes instelt en toepast voor teltaken.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 66e1fb9f32aa31221f85180339b8b6ee55836be1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996143"
---
# <a name="reason-codes-for-inventory-counting"></a>Redencodes voor voorraadtelling

[!include [banner](../includes/banner.md)]

Met redencodes kunt u de resultaten analyseren van een tellingsproces en eventuele verschillen die tijdens dat proces optreden. U kunt de reden voor het uitvoeren van de telling opgeven, zoals een gebroken pallet of een voorraadcorrectie die is gebaseerd op voorraadmonsters.

## <a name="recommendation"></a>Aanbeveling

Voordat u het systeem instelt, wordt aangeraden om een strategie voor het werken met redencodes te definiëren. Probeer bijvoorbeeld de volgende vragen te beantwoorden:

- Moeten redencodes verplicht zijn in magazijnen?
- Moeten redencodes verplicht of optioneel zijn voor bepaalde artikelen?
- Hoeveel redencodes hebt u nodig?
- Hoe moeten gebruikers van streepjescodescanners redencodes gebruiken? Moeten de redencodes vooraf worden geselecteerd, verplicht zijjn en niet kunnen worden bewerkt?
- Hebben magazijnmedewerkers andere redencodegedrag nodig voor mobiele scanners? Als het antwoord Ja is, kunt u meer menu-items maken en deze toewijzen aan verschillende personen.

## <a name="where-reason-codes-apply"></a>Waar redencodes toepassen

U kunt meerdere redencodebeleidsregels maken en elk redencodebeleid kan twee redencodebeleidsregels voor tellingen hebben. Het redencodebeleid voor tellingen kan worden gebruikt op magazijn- of artikelniveau.

## <a name="set-up-reason-code-policies"></a>Redencodebeleid instellen

1. Selecteer **Voorraadbeheer** \> **Instellen** \> **Voorraad** \> **Beleid van redencode voor telling** en maak een nieuw beleid voor de redencode.
2. Selecteer in het veld **Type redencode voor telling** de optie **Verplicht** of **Optioneel** om op te geven of de selectie van een redencode een optionele of verplichte actie moet zijn in een van de volgende tellijsten:

    - Cyclustelling (mobiel apparaat)
    - Plaatscyclustelling (mobiel apparaat)
    - Drempeltelling (mobiel apparaat)
    - Correctie-invoer (mobiel apparaat)
    - Correctie-uitvoer (mobiel apparaat)
    - Tellijst (rich client)

U kunt ook redencodes instellen voor afzonderlijke magazijnen en producten. De instelling van redencodes voor producten kunt de instelling voor magazijnen negeren.

## <a name="mandatory-reason-codes"></a>Verplichte redencodes

Als de parameter **Verplicht** is ingesteld in de configuratie van redencodes voor magazijnen of artikelen, kan de tellijst niet worden voltooid en afgesloten tot een redencode is opgegeven.

### <a name="set-up-reason-codes-for-warehouses"></a>Redencodes instellen voor magazijnen

1. Slecteer **Voorraadbeheer** \> **Instellingen** \> **Opsplitsing van voorraad** \> **Magazijnen**
2. Op het tabblad **Magazijn** in het veld **Beleid van redencode voor telling** selecteert u een van de volgende opties:

    - **Leeg**: de parameter die is ingesteld voor het artikel wordt gebruikt om te bepalen of de tellijsten verplicht zijn voor het product.
    - **Verplicht**: een redencode is altijd vereist voor tellijsten voor het magazijn.
    - **Optioneel**: een redencode is niet vereist voor tellijsten voor het magazijn.

### <a name="set-up-reason-codes-for-products"></a>Redencodes instellen voor producten

1. Selecteer **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
2. Op het tabblad **Product** selecteert u **Beleid van redencode voor telling** en vervolgens een van de volgende opties:

    - **Leeg**: de parameter die is ingesteld voor het magazijn wordt gebruikt om te bepalen of de tellijsten verplicht zijn voor het product.
    - **Verplicht**: een redencode is altijd vereist voor tellijsten voor het product. Deze instelling overschrijft de instelling van redencodes op magazijnniveau.
    - **Optioneel**: een redencode is niet vereist voor tellijsten voor het product. Deze instelling overschrijft de instelling van redencodes op magazijnniveau.

### <a name="use-reason-codes-in-counting-journals"></a>Redencodes gebruiken in tellijsten

In een tellijst kunt u redencodes van de volgende typen toevoegen:

- Cyclustelling
- Spotcyclustelling
- Drempeltelling
- Correctie-invoer
- Correctie-uitvoer

Redencodes worden toegevoegd aan de regels in tellijsten van het type **tellijst**.

1. Selecteer **Voorraadbeheer** \> **Journaalposten** \> **Artikeltelling** \> **Telling**.
2. In de regeldetails van de tellijst selecteert u een optie in het veld **Redencode voor telling**.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>De telhistorie weergeven, zoals is vastgelegd door redencodes

- Selecteer **Voorraadbeheer** \> **Query's en rapporten** \> **Telhistorie**, en geef in het veld **Redencode voor telling** de telhistorie weer die is geregistreerd via een redencode.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Een redencode gebruiken voor hoeveelheidcorrectie

1. Selecteer op de pagina **Voorhanden voorraad** **Hoeveelheid aanpassen**. U kunt de pagina **Voorhanden voorraad** op verschillende manieren openen. Selecteer bijvoorbeeld **Voorraadbeheer** \> **Query's en rapporten** \> **Voorhanden voorraad**.
2. Selecteer **Hoeveelheid aanpassen** en selecteer in het veld **Redencode voor telling** een redencode.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Redencodes voor menuopties op mobiele apparaten configureren

U kunt redencodes configureren voor elk type telling in een menuoptie op een mobiel apparaat. De configuratie van de menuoptie voor het mobiele apparaat bevat de volgende informatie:

- Of de redencode tijdens de telling wordt weergegeven aan de werknemer met het mobiele apparaat.
- De standaardredencode die wordt weergegeven in een menuoptie op het mobiele apparaat.
- Of de gebruiker de redencode kan bewerken.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Redencodes op een mobiel apparaat instellen

1. Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.
2. Selecteer op het tabblad **Cyclus tellen** de optie **Cyclustelling**.
3. Stel in het veld **Standaard redencode voor telling** de standaardredencode in die moet worden vastgelegd wanneer het tellen wordt uitgevoerd met behulp van de menuoptie op het mobiele apparaat.
4. Selecteer in het veld **Redencode voor telling weergeven** de optie **Regel** om de redencode weer te geven nadat elke afwijking is vastgelegd. U kunt ook **Verbergen** selecteren als de redencode niet moet worden weergegeven.
5. Stel de optie **Redencode voor telling bewerken** in op **Ja** of **Nee**. Als u deze optie instelt op **Ja**, kan de werknemer de redencode bewerken wanneer deze wordt weergegeven op het mobiele apparaat tijdens de telling.

> [!NOTE]
> De knop **Cyclustelling** kan worden ingeschakeld voor elke menuoptie op het mobiele apparaat waarmee de telling kan worden uitgevoerd. Dit kunnen menuopties zijn voor spotcyclustellingen, door de gebruiker uitgevoerd werk of door het systeem uitgevoerd werk.

## <a name="cycle-count-approvals"></a>Cyclustelling goedkeuren

Voordat een telling wordt goedgekeurd, kan de gebruiker de redencode wijzigen die is gekoppeld aan de telling. Als de telling is goedgekeurd, wordt de redencode ingevoerd in de regels van de tellijst.

### <a name="modify-cycle-count-approvals"></a>Goedkeuring van cyclustelling wijzigen

1. Selecteer **Magazijnbeheer** \> **Cyclustelling** \> **Cyclustellingswerk in afwachting van controle**.
2. Selecteer **Cyclustelling** en selecteer in het veld **Redencode** een nieuwe redencode.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>De menuoptie op het mobiele apparaat wijzigen voor Correctie-invoer en Correctie-uitvoer

1. Selecteer **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat** en selecteer vervolgens **Correctie invoer en uitvoer**.
2. Stel de optie **Bestaand werk gebruiken** in op **Nee**.
3. Selecteer in het veld **Proces van werkaanmaak** de optie **Correctie-invoer**.

De volgende velden worden toegevoegd aan de menuoptie op het mobiele apparaat wanneer **Correctie-invoer** of **Correctie-uitvoer** wordt geselecteerd tijdens het maken van werk:

- Standaard redencode voor telling
- Redencode voor telling weergeven
- Redencode voor telling bewerken
