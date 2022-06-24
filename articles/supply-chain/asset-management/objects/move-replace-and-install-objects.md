---
title: Activa verplaatsen, vervangen en installeren
description: In dit artikel wordt uitgelegd hoe u activa verplaatst, vervangt en installeert in Activabeheer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1454f41bb0b43e22c5278463f63aa4178696eef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872119"
---
# <a name="move-replace-and-install-assets"></a>Activa verplaatsen, vervangen en installeren

[!include [banner](../../includes/banner.md)]

 

In dit artikel wordt uitgelegd hoe u activa verplaatst, vervangt en installeert in Activabeheer. U kunt afzonderlijke activa maken die geen relaties hebben met andere activa, of u kunt een activastructuur maken die een bovenliggend activum (op het hoogste niveau) en gerelateerde onderliggende activa (subactiva) bevat. In Activabeheer zijn er drie benaderingen voor het verplaatsen en wijzigen van de locatie van een activum:

- **Verplaatsen**: een activum verplaatsen naar een andere activastructuur of naar een andere locatie in dezelfde activastructuur.
- **Vervangen**: tijdelijk een activum verwijderen uit een activastructuur zodat het kan worden gerepareerd of gereviseerd, en vervolgens het gereviseerde activum weer aan de activastructuur toevoegen. U kunt ook een gebruikt activum permanent vervangen door een nieuw activum.
- **Installeren**: een bovenliggend activum en alle gerelateerde onderliggende activa op een functionele locatie installeren.

> [!NOTE]
> Het activum dat u verplaatst, vervangt of installeert, is mogelijk gerelateerd aan een andere functionele locatie. In dat geval kan het activum financiële dimensies van de functionele locatie gebruiken. Op de pagina **Functionele locatietypen** stelt u de verwerking van financiële dimensies in op functionele locaties.

## <a name="move-asset"></a>Activum verplaatsen

Gebruik de functie **Activum verplaatsen** om een activum te verplaatsen naar een andere activastructuur of naar een andere locatie in dezelfde activastructuur. U kunt een activum ook uit een activastructuur verplaatsen, zodat het een zelfstandig activum wordt dat geen structuurrelaties heeft.

> [!NOTE]
> Gebruik deze functie niet als activa worden gerepareerd of tijdelijk worden vervangen. Gebruik in plaats daarvan de functie **Activum vervangen** die verderop in dit artikel wordt beschreven.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.
2. Selecteer in de lijst het activum dat u wilt verplaatsen. Als het activum onderliggende activa heeft, verplaatst u deze activa ook.
3. Selecteer **Activum verplaatsen**.
4. Als u het activum wilt verplaatsen zodat het onderdeel wordt van een activastructuur, selecteert u het nieuwe bovenliggende activum in het veld **Bovenliggend activum**. Als u een onderliggend element verplaatst en u daarvan een zelfstandig activum wilt maken dat geen structuurrelaties heeft, laat u het veld **Bovenliggend activum** leeg.
5. Standaard is het veld **Geldig vanaf** ingesteld op de huidige datum en tijd. U kunt echter een andere datum en tijd selecteren waarop de activaverplaatsing geldig wordt.
6. Selecteer **OK**.

## <a name="replace-asset"></a>Activum vervangen

Gebruik de functie **Activum vervangen** in verband met reparaties, revisie of permanente vervanging van een versleten activum door een nieuw activum. Deze functie wordt gebruikt om onderliggende activa in een activastructuur te vervangen. Voor bovenliggende activa (dat zijn activa die momenteel geen bovenliggend activum hebben), wordt deze vervanging uitgevoerd op een functionele locatie. Zie [Activa installeren op functionele locaties](../functional-locations/install-objects-on-functional-locations.md) voor meer informatie over het vervangen van bovenliggende activa op een functionele locatie.

> [!NOTE]
> Als een reparatiewerkplaats is gerelateerd aan uw productieafdeling, kunt u functionele locaties zoals **reparatie**, **uitval** en **opslag** maken om de reparatie en vervanging van activa te verwerken.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.
2. Selecteer in de lijst het onderliggende activum dat wordt vervangen. Als het activum onderliggende activa heeft, vervangt u deze activa ook.
3. Selecteer **Activum vervangen**.

    Het veld **Structuurwijziging** bevat de laatste datum en tijd waarop het geselecteerde activum en de bijbehorende onderliggende activa zijn verplaatst in de activastructuur.

4. Selecteer in de sectie **Geselecteerd activum** in het veld **Doel functionele locatie** de functionele locatie waarnaar u het activum wilt verplaatsen. Selecteer bijvoorbeeld de locatie van de **reparatie** of **uitval**.

    In de sectie **Bovenliggend activum** bevat het veld **Geldig vanaf** de laatste datum en tijd waarop het bovenliggende activum en de bijbehorende onderliggende activa zijn geïnstalleerd of verplaatst op de huidige functionele locatie.

5. Selecteer in de sectie **Nieuw activum** in het veld **Activum** het activum dat u wilt invoegen als tijdelijke of permanente vervanging voor het geselecteerde activum. Dit activum kan zich momenteel bevinden op een andere functionele locatie, zoals **opslag**.
7. In de sectie **Geldig vanaf** is het veld **Geldig vanaf** standaard ingesteld op de huidige datum en tijd. U kunt echter een andere datum en tijd selecteren waarop de activavervanging geldig wordt.
8. Selecteer **OK**.

## <a name="install-asset"></a>Activum installeren

Gebruik de functie **Activum installeren** om een activastructuur op een functionele locatie te installeren.

> [!NOTE]
> Selecteer altijd een bovenliggend activum. Het bovenliggende activum en de bijbehorende onderliggende activa worden verplaatst naar de geselecteerde functionele locatie.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.
2. Selecteer in de lijst het bovenliggende activum dat u wilt installeren op een andere functionele locatie.
3. Selecteer **Activum installeren**.

    De sectie **Kenmerken** geeft de activumkenmerken weer die zijn ingesteld voor het bovenliggende activum.

4. Selecteer de nieuwe locatie in het veld **Functionele locatie**.
5. Standaard is het veld **Geldig vanaf** ingesteld op de huidige datum en tijd. U kunt echter een andere datum en tijd selecteren waarop de installatie in de activastructuur geldig wordt.
6. Selecteer **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]