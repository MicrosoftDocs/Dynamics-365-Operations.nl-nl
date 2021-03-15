---
title: Activatypen
description: In dit onderwerp wordt uitgelegd hoe u activatypen maakt in Activabeheer. Ook worden de elementen beschreven die gerelateerd zijn aan activatypen.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 295840c12f89bc6c6a4d53023985259ac761d6b2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017412"
---
# <a name="asset-types"></a>Activatypen

[!include [banner](../../includes/banner.md)]



In dit onderwerp wordt uitgelegd hoe u activatypen maakt. Ook worden de elementen beschreven die gerelateerd zijn aan activatypen. Activatypen worden gebruikt als algemene categorieën voor activa. Voorbeelden hiervan zijn CNC-machines, meetapparatuur en vrachtwagenmotoren. Activatypen worden gebruikt voor het beheren van de onderhoudstaaktypen (onderhoudstaken), levenscyclusstatussen van activa, tellers, kenmerken van activa, sjablonen voor beoordeling van voorwaarden en activamodellen die voor een activum kunnen worden geselecteerd. Wanneer u een activum maakt, moet u het activatype opgeven.

Voor elk activatype kunnen variaties van de instellingen van het activatype worden gemaakt. Als u bijvoorbeeld een activatype met de naam **Trucks** hebt, kunt u variaties van dat activatype maken voor verschillende activafabrikanten en activamodellen. Voor elke instelling van het activatype kunt u de benodigde reserveonderdelen en onderhoudsplannen toevoegen.

Eerst stelt u de vereiste activatypen in. Vervolgens maakt u de activamodellen die moeten worden gerelateerd aan de activatypen. Tot slot maakt u op de pagina **Standaardwaarden van activatype** alle variaties van activatypen die zijn vereist voor uw apparatuur.

## <a name="create-an-asset-type"></a>Een activatype maken

1. Selecteer **Activabeheer** > **Instellingen** > **Activatypen** > **Activatypen**.
2. Selecteer **Nieuw** om een activatype te maken.
3. Voer in het veld **Activatype** een id voor het activatype in.
4. Voer in het veld **Naam** een naam in.
5. Selecteer in het veld **Levenscyclusmodel van activa** een model voor de levenscyclus van activa. Zie [Levenscyclusstatussen van activa](object-stages.md) voor meer informatie over de levenscyclusstatussen van activa en levenscyclusmodellen van activa.
6. Stel de optie **Totaal** in op **Ja** als samengevatte KPI-waarden (Key Performance indicator) moeten worden berekend voor activa met dit activatype.
7. Selecteer **Opslaan**.
8. Selecteer op het sneltabblad **Typen onderhoudstaken** de onderhoudstaaktypen die moeten worden gerelateerd aan het activumtype:

    - Als u een onderhoudstaaktype wilt selecteren, selecteert u dit in het veld **Resterende onderhoudstaaktypen** en selecteert u vervolgens de knop pijl naar rechts ![knop Pijl naar rechts](media/29-setup-for-objects.png) om het te verplaatsen naar de sectie **Geselecteerde onderhoudstaaktypen**.
    - Als u alle beschikbare onderhoudstaaktypen wilt selecteren, selecteert u de knop ![Pijl allemaal doorsturen](media/30-setup-for-objects.png). Alle onderhoudstaaktypen worden overgebracht van het veld **Resterende onderhoudstaaktypen** naar het veld **Geselecteerde onderhoudstaaktypen**.
    - Als u de selectie van een onderhoudstaaktype wilt annuleren, selecteert u dit in het veld **Geselecteerde onderhoudstaaktypen** en selecteert u vervolgens de knop pijl naar links ![knop Pijl naar links](media/31-setup-for-objects.png) om het te verplaatsen naar het veld **Resterende onderhoudstaaktypen**.

9. U kunt ook de tellers selecteren die moeten worden gerelateerd aan het activatype. Maak op het sneltabblad **Tellers** uw selecties met behulp van de methoden die worden beschreven voor onderhoudstaaktypen in stap 8. Zie [Tellers](counters.md) voor meer informatie over het instellen van tellers.
10. U kunt ook de kenmerktypen selecteren die moeten worden gerelateerd aan het activatype. Maak op het sneltabblad **Kenmerktypen** uw selecties met behulp van de methoden die worden beschreven voor onderhoudstaaktypen in stap 8. Vervolgens kunt u de voorkeursvolgorde van kenmerktypen instellen door een kenmerktype te selecteren in het veld **Geselecteerde kenmerktypen** en de knoppen pijl-omhoog en pijl-omlaag te gebruiken om deze te verplaatsen. De volgorde van kenmerktypen wordt weergegeven voor activa die gebruikmaken van dit activatype. Zie [Kenmerktypen voor onderhoud](../setup-for-functional-locations/specification-types.md) voor meer informatie over kenmerken van activa.

    > [!NOTE]
    > Wanneer u nieuwe kenmerktypen toevoegt op het sneltabblad **Kenmerktypen**, worden bestaande activa automatisch bijgewerkt met die informatie.

11. U kunt ook de sjablonen voor beoordeling van voorwaarden selecteren die moeten worden gerelateerd aan het activatype. Maak op het sneltabblad **Toestandsbeoordelingen** uw selecties met behulp van de methoden die worden beschreven voor onderhoudstaaktypen in stap 8. Zie [Toestandsbeoordeling](../setup-for-objects/condition-assessment.md) voor meer informatie over sjablonen voor beoordeling van voorwaarden en registraties.
12. Op het sneltabblad **Activamodel** worden alle combinaties van activafabrikanten en -modellen weergegeven die zijn ingesteld voor het geselecteerde activatype. Als u de combinaties wilt zien opgesplitst naar fabrikant, selecteert u **Activamodel** om de pagina **Activamodel** te openen.

    Op de pagina **Activamodel** kunt u relaties tussen activamodel en activatype toevoegen. Bovendien kunt u op de pagina **Activatypen** relaties tussen activafabrikant en activamodel rechtstreeks toevoegen aan een activatype. Tot slot kunt u op de pagina **Activamodel** (**Activabeheer** \> **Instellingen** \> **Activa** \> **Activamodel**) nieuwe relaties tussen activafabrikant, activamodel en activatype. Daarom zijn er drie manieren om de relaties van activafabrikant, activamodel en activatype in te stellen en te bewerken. Alle beschikbare combinaties worden vanuit verschillende perspectieven weergegeven en u kunt het gewenste punt van binnenkomst selecteren wanneer u met de instellingen werkt.

> [!NOTE]
> - Als u tellers selecteert voor een activumtype, worden de selecties automatisch bijgewerkt op de pagina **Tellers** (**Activabeheer** > **Instellingen** > **Activa** > **Activatypen** > **Tellers**).
> - De velden in de sectie **Details** op het sneltabblad **Algemeen** tonen het aantal onderhoudstaaktypen, tellers, kenmerken enzovoort, die zijn ingesteld voor het geselecteerde activatype.

Gewoonlijk zijn werkorders die handmatig worden gemaakt gerelateerd aan correctief onderhoud, terwijl werkorders die automatisch worden gemaakt, zijn gerelateerd aan preventief onderhoud. Wanneer u handmatig werkorders maakt, kunnen alleen de onderhoudstaaktypen die zijn geselecteerd op het sneltabblad **Onderhoudstaaktypen** van de pagina **Activatypen** worden gebruikt. Automatisch gemaakte werkorders kunnen echter gebruikmaken van alle onderhoudstaaktypen die u maakt op de pagina **Onderhoudstaaktypen** (**Activabeheer** \> **Instellingen** \> **Taken** \> **Onderhoudstaaktypen**).

## <a name="create-asset-type-setup-lines"></a>Instellingsregels voor activatypen maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Activatypen** \> **Instellingen van activatype**. Of selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Activatypen** \> **Activatypen**, selecteer een activatype en selecter vervolgens **Instellingen van activatype**.
2. Wanneer u de pagina **Instellingen van activatype** voor het eerst gebruikt, kan de knop **Combinaties maken** handig zijn. U kunt deze knop gebruiken om snel alle combinaties van een activamodel voor een activatype te maken. Selecteer **Combinaties maken**, selecteer het activatype waarvoor u combinaties wilt maken en selecteer vervolgens **OK**.

    > [!NOTE]
    > Als u niet alle combinaties van instellingen voor activatypen gebruikt die automatisch zijn gemaakt, kunt u een instelling verwijderen door deze te selecteren en vervolgens **Verwijderen** te selecteren.

3. Selecteer **Nieuw** om handmatig een instelling voor een activatype te maken.
4. Afhankelijk van hoe specifiek de instellingen van het activatype moeten zijn, voert u selecties uit in de velden **Activatype**, **Fabrikant** en **Model**.
5. Als een garantieovereenkomst betrekking heeft op het activatype, selecteert u de overeenkomst in de velden **Leveranciersgarantie** en **Klantgarantie**. 
6. Selecteer op het sneltabblad **Reserveonderdelen** de optie **Toevoegen** om reserveonderdelen toe te voegen aan de geselecteerde instelling voor het activatype.
7. Als u een reserveonderdeel wilt goedkeuren, selecteert u de reserveonderdeelregel en selecteert u vervolgens **Goedkeuren**. U kunt meerdere regels selecteren voor goedkeuring.
8. Als u wilt zien of een reserveonderdeel ergens anders in activabeheer wordt gebruikt (bijvoorbeeld in relatie tot activa en werkorders), selecteert u de regel van het reserveonderdeel en selecteert u vervolgens **Artikel waar gebruikt** om de pagina **Artikel waar gebruikt** te openen. Als u alle actieve reserveonderdelen in de lijst wilt weergeven, schakelt u het selectievakje **Actief** in. Als u alleen goedgekeurde reserveonderdelen wilt zien, schakelt u het selectievakje **Goedgekeurd** in.
9. Selecteer op het sneltabblad **Onderhoudsplannen** de optie **Toevoegen** om onderhoudsplannen toe te voegen aan de geselecteerde instelling voor het activatype.
10. Als u een instelling van een activatype naar een andere instelling wilt kopiëren, gebruikt u de functie Kopiëren. Selecteer de instelling van het activatype waar u een instelling naartoe wilt kopiëren, selecteer **Instellingen kopiëren** en selecteer vervolgens de instelling van het activumtype waaruit u de instelling wilt kopiëren. De instellingen van de verschillende opties bepalen hoeveel informatie wordt opgenomen. Wanneer u klaar bent, selecteert u **OK** om de instelling te kopiëren.

> [!NOTE]
> Als u veel reserveonderdeelregels en onderhoudsplanregels hebt die u opnieuw wilt gebruiken, kunt u met de functie Kopiëren snel en eenvoudig gegevens instellen voor veel combinaties van instellingen van een activatype.

## <a name="spare-parts-on-the-asset-type-setup"></a>Reserveonderdelen in de instelling van het activatype

Zoals beschreven in de sectie 'Instellingsregels voor activatypen maken', worden reserveonderdelen ingesteld voor activamodellen op de pagina **Instellingen van activatype**. Wanneer u de pagina **Instellingen van activatype** opent, ziet u daarom alleen de reserveonderdelen die zijn gerelateerd aan de geselecteerde combinatie van een activatype, activafabrikant en activamodel. Als u een lijst met alle reserveonderdeelrecords wilt bekijken, opent u de pagina **Reserveonderdelen** (**Activabeheer** \> **Query's** \> **Reserveonderdelen**).

Op de pagian **Reserveonderdelen** kunt u ook nieuwe reserveonderdelen maken voor bestaande combinaties van een activatype, activafabrikant en activamodel. U kunt bepalen of u reserveonderdeelrecords wilt maken op de pagina **Instellingen van activatype** of op de pagina **Reserveonderdelen**. De pagina **Instellingen van activatype** biedt een overzicht van gegevens over de geselecteerde combinatie van een activatype, een activafabrikant en een activamodel, terwijl de pagina **Reserveonderdelen** een volledig overzicht biedt van alle instellingsregels voor het activatype. Als de pagina **Reserveonderdelen** veel records bevat, kan de pagina **Instellingen van activatype** u mogelijk een beter overzicht geven.

Als u wilt zien of het reserveonderdeel op de geselecteerde regel ergens anders in activabeheer wordt gebruikt (bijvoorbeeld in relatie tot activa en werkorders), selecteert u **Artikel waar gebruikt** om de pagina **Artikel waar gebruikt** te openen. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]