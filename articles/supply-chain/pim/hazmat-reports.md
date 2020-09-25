---
title: Informatie en rapporten voor gevaarlijke stoffen
description: In dit onderwerp wordt uitgelegd hoe u kunt werken met de verschillende rapporten die betrekking hebben op gevaarlijke stoffen. Veel van deze rapporten zijn vereist, zodat u tijdens de verzending en opslag voldoet aan de diverse voorschriften voor gevaarlijke stoffen.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 188c339ddf5f5c2488133924e9a0288f218f495c
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803010"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Informatie en rapporten voor gevaarlijke stoffen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management biedt diverse rapporten die betrekking hebben op gevaarlijke stoffen. Veel van deze rapporten zijn vereist, zodat u tijdens de verzending en opslag voldoet aan de diverse voorschriften voor gevaarlijke stoffen.

Al deze rapporten, met uitzondering van het rapport **Multimodale gevaarlijke stoffen**, gebruiken de leveringsmethode die voor de zending is gedefinieerd, om de regelgeving te zoeken die moet worden gebruikt om de verzendtekst voor artikelen af te drukken. De leveringsmethode is gekoppeld aan de vervoerder en vervoerdersservice. Daarom moet u een vervoerder en vervoerdersservice instellen en deze koppelen aan een leveringsmethode. De leveringsmethode is gerelateerd aan de regelgeving voor gevaarlijke stoffen.

In de volgende afbeelding ziet u de volgorde van activiteiten die plaatsvinden wanneer het systeem rapporten voor gevaarlijke stoffen genereert.

![Volgorde van activiteiten voor rapporten over gevaarlijke stoffen](media/hazmat-report-sequence.png "Volgorde van activiteiten voor rapporten over gevaarlijke stoffen")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Rapportage over gevaarlijke stoffen instellen

Als u artikelen verzendt die gevaarlijke stoffen bevatten, moet u meestal specifieke rapporten genereren om de veiligheid te waarborgen en te voldoen aan regelgeving inzake gevaarlijke stoffen. Volg deze stappen om uw rapporten in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
2. Open het tabblad **Rapporten**. Stel op het sneltabblad **Rapportparameter voor gevaarlijke stoffen** de volgende velden in.

    | Sectie | Veld | Beschrijving |
    |---|---|---|
    | Multimodale gevaarlijke stoffen | Reguleringscode | Selecteer de regelgeving die moet worden gebruikt wanneer een rapport voor **Multimodale gevaarlijke goederen** wordt gegenereerd. |
    | Voorraadlimieten voor gevaarlijke stoffen | Reguleringscode | Selecteer de regelgeving die moet worden gebruikt wanneer voorraadlimieten worden beoordeeld. |
    | Vervoer van goederen over de weg | Product CMR-groep | CMR is de afkorting van "carcinogenic, mutagenic, and reprotoxic substances" oftewel kankerverwekkende, mutagene en reprotoxische stoffen. Stel deze optie in op **Ja** om het systeem zo te configureren dat er specifieke waarschuwingen en berichten worden afgedrukt die betrekking hebben op de behandeling van deze stoffen. |
    | Vervoer van goederen over de weg | Groepsomschrijving van gevaarlijk materiaal | Voer de tekst in van specifieke waarschuwingen die zijn gerelateerd aan CMR en vervoer van goederen over de weg. Deze tekst wordt in het rapport opgenomen. |
    | Shipper´s Declaration | Waarschuwing | Voer de tekst in van een waarschuwingsbericht dat moet worden afgedrukt op de Shipper´s Declaration (bijvoorbeeld "Waarschuwing: gevaarlijke goederen, brandbaar"). |
    | Shipper´s Declaration | Declaratie voettekst | Voer de tekst in van een bericht dat onderaan de Shipper´s Declaration moet worden afgedrukt. |
    | Rapporttaal voor gevaarlijke goederen | Rapporttaal voor gevaarlijke goederen binnenlands | Selecteer de standaardtaal voor rapporten voor gevaarlijke stoffen die is gekoppeld aan binnenlandse zendingen. |
    | Rapporttaal voor gevaarlijke goederen | Rapporttaal voor export gevaarlijke goederen | Selecteer de standaardtaal voor rapporten voor gevaarlijke stoffen die is gekoppeld aan internationale zendingen. |

## <a name="hazardous-materials-report"></a>Rapport over gevaarlijke stoffen

Het rapport **Gevaarlijke stoffen** bevat een lijst met alle artikelen die zijn ingesteld en gedefinieerd, zodat ze informatie over gevaarlijke goederen bevatten. U kunt dit rapport gebruiken om de informatie die u moet onderhouden, te controleren te herzien. De pagina voor het rapport bevat een beperkte selectie velden uit de instellingen voor gevaarlijke stoffen. U kunt deze echter aanpassen en extra velden toevoegen als dat nodig is.

Als u dit rapport wilt weergeven, gaat u naar **Productgegevensbeheer \> Informatie en rapporten \> Vervoersdocumentatie voor gevaarlijke stoffen \> Gevaarlijke stoffen**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Rapport Voorraadlimiet voor gevaarlijke stoffen

Met het rapport **Voorraadlimiet voor gevaarlijke stoffen** kunt u de voorraadniveaus van de gevaarlijke stoffen op uw magazijnlocaties controleren, om na te gaan of ze onder de vastgestelde veilige grenzen blijven. Deze limieten zijn afkomstig uit de limieten die voor elk vrijgegeven product zijn gedefinieerd.

Als u dit rapport wilt weergeven, gaat u naar **Productgegevensbeheer \> Informatie en rapporten \> Vervoersdocumentatie voor gevaarlijke stoffen \> Voorraadlimiet voor gevaarlijke stoffen**.

Zie [Voorraadlimieten voor gevaarlijke producten instellen](hazmat-items.md#stock-limits) voor meer informatie over het instellen van voorraadlimieten voor een vrijgegeven product.

De regelgeving die voor voorraadlimieten wordt gebruikt, wordt gedefinieerd op de pagina **Parameters voor magazijnbeheer**. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer** en geef op het tabblad **Rapporten** in **Voorraadlimiet voor gevaarlijke stoffen** een regelgevingscode op. Zie voor meer informatie de sectie [Rapportage voor gevaarlijke stoffen instellen](#set-up) eerder in dit onderwerp.

## <a name="verified-gross-mass-report"></a>Rapport Geverifieerde brutomassa

Met het rapport **Geverifieerde brutomassa** kunt u informatie afdrukken over het gewicht van een zending.

Als u dit rapport wilt genereren en afdrukken, gaat u naar **Magazijnbeheer \> Zendingen \> Alle zendingen** en opent u de relevante zending. Selecteer vervolgens in het actievenster op het tabblad **Zendingen** in de groep **Document voor gevaarlijke stoffen** de optie **Geverifieerde brutomassa**.

## <a name="multimodal-dangerous-goods-report"></a>Rapport Multimodale gevaarlijke stoffen

Het rapport **Multimodale gevaarlijke stoffen** wordt verstrekt voor zendingen die moeten worden verplaatst met behulp van een combinatie van transportmethoden. Het wordt meestal gebruikt wanneer een zending eerst over de weg en later over zee wordt getransporteerd.

Als u dit rapport wilt genereren en afdrukken, gaat u naar **Magazijnbeheer \> Zendingen \> Alle zendingen** en opent u de relevante zending. Selecteer vervolgens in het actievenster op het tabblad **Zendingen** in de groep **Document voor gevaarlijke stoffen** de optie **Multimodale gevaarlijke stoffen**.

Wanneer u dit rapport genereert, worden de gegevens opgeslagen zodat u deze kunt bewerken en/of het rapport zo nodig opnieuw kunt afdrukken. Als u een gegenereerd rapport wilt bewerken, gaat u naar **Magazijnbeheer \> Informatie en rapporten \> Vervoersdocumentatie gevaarlijke stoffen \> Multimodale gevaarlijke stoffen** en zoekt u het relevante rapport in de lijst. Nadat u de gewenste inhoud hebt bewerkt, selecteert u **Afdrukken** in het actievenster om het rapport af te drukken.

## <a name="shippers-declaration-report"></a>Rapport Shipper´s Declaration

Met het rapport **Shipper´s Declaration** kunt u gegevens afdrukken die betrekking hebben op een verklaring van de materialen die in de zending zijn opgenomen.

Als u dit rapport wilt genereren en afdrukken, gaat u naar **Magazijnbeheer \> Zendingen \> Alle zendingen** en opent u de relevante zending. Selecteer vervolgens in het actievenster op het tabblad **Zendingen** in de groep **Document voor gevaarlijke stoffen** de optie **Shipper´s Declaration**.

## <a name="carriage-of-merchandise-by-road-report"></a>Rapport Vervoer van goederen over de weg

Het rapport **Vervoer van goederen over de weg** lijkt op een vrachtbrief, maar wordt meestal gebruikt voor wegtransport in Europa in het kader van de ADR (overeenkomst inzake het internationale vervoer van gevaarlijke goederen over de weg). In dit rapport wordt de verzendtekst voor een artikel gebruikt, tenzij u het veld **Beschrijving voor groep gevaarlijke stoffen** op de pagina **Parameters voor magazijnbeheer** hebt ingesteld.

Als u dit rapport wilt genereren en afdrukken, gaat u naar **Magazijnbeheer \> Zendingen \> Alle zendingen** en opent u de relevante zending. Selecteer vervolgens in het actievenster op het tabblad **Zendingen** in de groep **Document voor gevaarlijke stoffen** de optie **Vervoer van goederen over de weg**.

Wanneer u dit rapport genereert, worden de gegevens opgeslagen zodat u deze kunt bewerken en/of het rapport zo nodig opnieuw kunt afdrukken. Als u een gegenereerd rapport wilt bewerken, gaat u naar **Magazijnbeheer \> Informatie en rapporten \> Vervoersdocumentatie gevaarlijke stoffen \> Vervoer van goederen over de weg** en zoekt u het relevante rapport in de lijst. Nadat u de gewenste inhoud hebt bewerkt, selecteert u **Afdrukken** in het actievenster om het rapport af te drukken.

## <a name="shipment-summary-report"></a>Rapport zendingsoverzicht

Het rapport **Zendingsoverzicht** bevat informatie die wordt samengevat voor de transportcategorie die is gekoppeld aan de vrijgegeven artikelen.

Als u dit rapport wilt genereren en afdrukken, gaat u naar **Magazijnbeheer \> Zendingen \> Alle zendingen** en opent u de relevante zending. Selecteer vervolgens in het actievenster op het tabblad **Zendingen** in de groep **Document voor gevaarlijke stoffen** de optie **Zendingsoverzicht**.

## <a name="bill-of-lading-report"></a>Rapport Vrachtbrief

Wanneer de functie voor gevaarlijke stoffen is ingeschakeld in uw systeem, bevat het rapport **Vrachtbrief** een kolom **Gevaarlijke stoffen** waarin wordt aangegeven of een lading gevaarlijke stoffen bevat. Dit rapport is zoals gewoonlijk te vinden op de pagina **Alle ladingen**.

## <a name="packing-list-report"></a>Rapport Verpakkingslijst

Wanneer de functie voor gevaarlijke stoffen is ingeschakeld in uw systeem, bevatten verpakkingslijsten aanvullende informatie over de verzendtekst voor een artikel. Dit rapport is zoals gewoonlijk te vinden op de pagina **Alle ladingen**.
