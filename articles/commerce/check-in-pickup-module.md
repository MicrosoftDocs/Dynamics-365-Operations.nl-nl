---
title: Inchecken voor afhaalmodule
description: In dit artikel wordt de module Inchecken voor afhalen beschreven en wordt uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7002db893da1802063148a9b800ffa92f3e5f065
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885470"
---
# <a name="check-in-for-pickup-module"></a>Inchecken voor afhaalmodule

[!include [banner](includes/banner.md)]

In dit artikel wordt de module Inchecken voor afhalen beschreven en wordt uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.

De module Inchecken voor afhalen biedt een bevestigingspagina voor klanten die de mogelijkheden voor inchecken door klanten in Dynamics 365 Commerce gebruiken om een winkel te informeren dat zij er zijn. Met de module Inchecken voor afhalen kunt u ook een formulier configureren waarin extra informatie van klanten wordt verzameld om de orderlevering te vergemakkelijken. Deze informatie omvat het parkeerplaatsnummer van de klant en het merk en model van diens voertuig. 

## <a name="module-properties"></a>Module-eigenschappen

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Bevestigingstekst | Tekenreeks | Inhoud van de kop die wordt weergegeven op de pagina met bevestiging van het inchecken. |
| QR-code weergeven | **True** of **False** | Wanneer deze eigenschap is ingesteld op **Waar**, wordt op de bevestigingspagina voor het inchecken een QR-code getoond die de orderbevestigings-id bevat. |
| Koptekst met aanvullende informatie | Tekenreeks | Inhoud van de kop die wordt weergegeven wanneer extra informatievelden zijn geconfigureerd. |
| Sleutels voor aanvullende informatie | Paar met bron-id/bronwaarde | Met elke sleutel worden een formulierveld en een bijbehorend label gemaakt, waarmee extra informatie kan worden verzameld van klanten. |
| Sleutels voor aanvullende informatie \> Bron-id | Tekenreeks | Met elke informatiesleutel worden een formulierveld en een bijbehorend label gemaakt, waarmee extra informatie kan worden verzameld van klanten. Deze eigenschap identificeert de sleutel voor aanvullende informatie. In de taak die is gemaakt op het POS (Point of Sale) wordt de waarde van deze eigenschap weergegeven als het label in het veld met instructies. |
| Sleutels voor aanvullende informatie \> Bronwaarde | Tekenreeks | Het label voor het tekstveld in de taak in POS. |
| Sleutels voor aanvullende informatie \> Vereist | **True** of **False** | Met deze eigenschap wordt opgegeven of klanten het formulierveld moeten invullen voordat ze kunnen doorgaan. Wanneer deze eigenschap wordt ingesteld op **Waar**, wordt een sterretje naast het formulierlabel weergegeven en wordt er een null-controle uitgevoerd om te voorkomen dat klanten doorgaan als geen waarde is ingevoerd. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>De module Inchecken voor afhalen toevoegen aan een pagina

De module Inchecken voor afhalen moet worden toegevoegd aan de nieuwe pagina die u maakt voor de bevestiging van het inchecken. Deze pagina wordt gebruikt als de bevestigingservaring voor inchecken voor klanten die de koppeling of knop **Ik ben er** in de e-mail selecteren. 

## <a name="configure-the-additional-information-form"></a>Het formulier voor aanvullende gegevens configureren

Als geen sleutels voor extra informatie zijn geconfigureerd, wordt in de module voor de klanten standaard de pagina voor bevestigen van het inchecken getoond. Wanneer de bevestiging van het inchecken wordt weergegeven, wordt een taak gemaakt in POS voor de winkel waarin de order wordt opgehaald.

Wanneer een of meer sleutels voor aanvullende informatie worden geconfigureerd, wordt klanten eerst gevraagd informatie in te voeren. Wanneer ze **Verzenden** selecteren, wordt de bevestiging van het inchecken weergegeven en wordt een taak gemaakt in het POS. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Incheckmeldingen van klanten in Point of Sale (POS) inschakelen](enable-customer-check-in.md)
