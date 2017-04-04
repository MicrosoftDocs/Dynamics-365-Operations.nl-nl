---
title: De taalinstellingen van de POS-toepassing en gebruiker
description: In dit onderwerp wordt beschreven hoe taalinstellingen wijzigen in de detailhandel moderne POS (MPOS) en Cloud-POS.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>De taalinstellingen van de POS-toepassing en gebruiker

In dit onderwerp wordt beschreven hoe taalinstellingen wijzigen in de detailhandel moderne POS (MPOS) en Cloud-POS.

<a name="overview"></a>Overzicht
========

Retail moderne POS (MPOS) en Cloud-POS ondersteuning voor omgevingen waar taalinstellingen en vertalingen tussen de winkel- en instellingen variëren kunnen. De winkel kan bijvoorbeeld bevinden in een gebied waar Engels is gebruikelijk voor hun klanten, maar sommige werknemers liever de toepassing met Franse vertalingen gebruiken.

## <a name="data-language"></a>Gegevenstaal
Ongeacht de instellingen van de gebruiker, wordt MPOS en Cloud-POS gebruik altijd de taalinstellingen van de winkel om te bepalen van de vertalingen voor de gegevens gebruikt. Hierdoor zorgt u dat alle gebruikers en klanten een consistente ervaring hebben.  Voorbeelden van gegevens zijn:

-   Producten
-   Kenmerken en waarden
-   Categorienamen
-   Afgedrukte of ge-e-mailde transactieontvangstbewijzen
-   Namen betalingsmethodes
-   Regelweergaveberichten

De taal van de winkel worden ook gebruikt voor het hoofdscherm van POS-aanmelding omdat de gebruiker onbekend voordat u zich aanmeldt. Als een vertaling niet beschikbaar voor de taal van de winkel is, wordt het POS terug naar de taal van het bedrijf.

### <a name="configuring-the-stores-language-setting"></a>De taalinstelling van de winkel configureren

De taalinstelling van de winkel wordt ingesteld op **alle detailhandel** op de **winkel** pagina onder ** algemene &gt;landinstellingen &gt;taal. ** Aansluiting omlaag gebruiken om de taal voor elke winkel te kiezen.

## <a name="user-interface-language"></a>Taal gebruikersinterface
De taalinstelling van de POS-gebruiker bepaalt de vertalingen die in de gebruikersinterface van de toepassing gebruikt. Dit omvat alle labels, menu's en lijsten die gegevens niet worden beschouwd. Een uitzondering is de tekst die wordt weergegeven op de POS-knoppenrasters. De knoppenrasters ondersteunen geen vertalingen, zodat ze altijd de tekst weergegeven zoals gedefinieerd op de knop. Ter ondersteuning van vertaalde knoppen hebt u wilt kopiëren en afzonderlijke knoppenrasters beheren en deze toewijzen aan de gebruikers.

### <a name="configuring-the-users-language-setting"></a>De taalinstelling van de gebruiker configureren

De taalinstelling van de POS-gebruiker wordt ingesteld op **alle werknemers** op de **werknemer** pagina onder **detailhandel &gt;taal**.  Het is niet ingesteld op het tabblad met belangrijkste profiel.  Deze instelling wordt niet gebruikt door POS. Als de taal van de gebruiker niet is ingesteld of is ingesteld op een taal waarvoor geen vertalingen beschikbaar zijn, stapt het POS weer over op de taal van de winkel.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **De taal van gebruikersinterface** ** **      | **Gegevenstaal (producten, ontvangstindelingen, regelweergave, enzovoort.)** |
| **Bedrijf** | Standaard                    | Standaard                                                           |
| **Winkel**   | Overschrijft bedrijf          | Overschrijft bedrijf                                                 |
| **User**    | Overschrijft opslag of bedrijf | Nooit                                                             |




