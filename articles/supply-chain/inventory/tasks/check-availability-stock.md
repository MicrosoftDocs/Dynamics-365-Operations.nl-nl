---
title: De beschikbaarheid van voorraad controleren
description: Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren.
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 894c153761dc29e3d5d9fc22900d96a50ae33b6d5db92623118e229a9aedafe4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758635"
---
# <a name="check-the-availability-of-stock"></a>De beschikbaarheid van voorraad controleren

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren. Het geeft ook weer hoe u aanbodinformatie voor een artikel krijgt. De fysieke voorhanden voorraad is de voorhanden voorraad die beschikbaar is, dat wil zeggen dat de voorraad is ingekocht, ontvangen en geregistreerd. De voorhanden voorraad bevat de beschikbare voorraad, maar ook de voorraad die is besteld en wordt verwacht, maar nog niet is ontvangen of geregistreerd. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven. Deze taken worden meestal uitgevoerd door een magazijnmedewerker.


## <a name="check-on-hand-inventory-for-an-item"></a>Voorhanden voorraad voor een artikel controleren
1. Ga naar **Navigatievenster > Modules > Voorraadbeheer > Query's en rapporten > Voorhanden voorraad**.
2. Selecteer de rij **Artikelnummer**. Om de voorhanden voorraad op artikelnummer op te vragen, selecteert u de rij waar de tabel op **Voorhanden voorraad** is ingesteld en het veld op **Artikelnummer** is ingesteld.
3. Selecteer in het veld **Criteria** het artikel waarvoor u een query wilt uitvoeren. Als u het USMF-demobedrijf gebruikt, kunt u 'M9201' selecteren.  
4. Klik op **OK**.
5. Klik in het **actievenster** op **Dimensies**. Met het tabblad **Dimensies** selecteert u hoeveel details u wilt zien over de voorhanden voorraad. Als u gegevens met betrekking tot reserveringen nodig hebt, moet u alle voorraaddimensies voor de artikelen weergeven die geavanceerde magazijnbeheerprocessen gebruiken.
6. Klik op **OK**.
7. Klik in het **actievenster** op **Gerelateerde informatie**. Als deze optie niet wordt weergegeven, kunt u op de knop met weglatingstekens (...) klikken om extra actievensteropties te bekijken.
8. Klik op **Aanbodoverzicht**. Het tabblad **Aanbodoverzicht** biedt aanbodinformatie voor een bepaald artikel, zoals de voorhanden hoeveelheid, doorlooptijd, en leveranciersgegevens.  
9. Vouw de sectie **Voorhanden** uit.
10. Vouw de sectie **Leveranciers** uit.
11. Sluit de pagina.
12. Sluit de pagina.

## <a name="check-physical-on-hand-inventory"></a>Fysieke voorhanden voorraad controleren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Query's en rapporten > Fysieke voorhanden voorraad**.
2. Typ een waarde in het veld **Artikelnummer**. U kunt Locatie en Magazijn gebruiken om de lijst met artikelen te filteren. 
3. Vernieuw de pagina.
4. Klik in het **actievenster** op **Dimensies weergeven**. Met het tabblad Dimensies weergeven selecteert u hoeveel details u wilt zien over de voorhanden voorraad.
5. Klik op **OK**.
6. Sluit de pagina.

## <a name="check-on-hand-inventory-by-location"></a>De voorhanden voorraad per locatie controleren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Query's en rapporten > Voorhanden voorraad per locatie**.
2. Typ een waarde in het veld **Magazijn**. Als u het USMF-bedrijf van de demogegevens gebruikt, kunt u 51 gebruiken.  
3. Vernieuw de pagina.
4. Klik op **Dimensies weergeven**.
5. Klik op **OK**.
6. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]