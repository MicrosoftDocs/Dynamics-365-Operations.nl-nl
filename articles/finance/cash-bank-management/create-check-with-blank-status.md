---
title: Cheques met een status Blanco maken
description: In dit onderwerp wordt uitgelegd hoe u op de pagina Cheques een blanco cheque maakt voor een bankrekening.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1b01daa86055156092d035d61aad78a13349f869
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815951"
---
# <a name="create-checks-that-have-blank-status"></a>Cheques met een status Blanco maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u blanco cheques maakt. U kunt bijvoorbeeld een blanco cheque maken om een cheque te registreren die beschadigd is en die niet kan worden gebruikt om een betaling mee te verrichten.

Op de pagina **Cheques** voert u onderhoudstaken uit voor cheques. U kunt bijvoorbeeld nieuwe chequenummers maken en cheques verwijderen. U kunt ook cheques maken met de status **Blanco**. Blanco cheques die zijn gemaakt, kunnen niet meer worden verwijderd of opnieuw worden gebruikt in het systeem.

> [!NOTE]
> Deze functie is alleen beschikbaar op de pagina **Cheques** als u de functie **Cheques met een blanco status maken op de pagina Cheques** inschakelt op de pagina **Functiebeheer**. Als die functie niet is ingeschakeld, kunnen cheques met een status **Blanco** alleen worden gemaakt via het dialoogvenster **Betaling per cheque** tijdens het genereren van de betaling in Leveranciers.

Als u de pagina **Cheques** wilt openen, gaat u naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen** en selecteert u in het actievenster op het tabblad **Betalingen beheren** in de groep **Verwante informatie** de optie **Cheques**. U kunt ook naar **Contanten en bankbeheer \> Query's en rapporten \> Cheques** gaan.

Als u cheques met de status **Blanco** wilt maken, selecteert u in het actievenster de optie **Blanco cheques maken**. Terwijl er door het systeem blanco cheques worden gemaakt, wordt de bijbehorende bankrekening tijdelijk uitgeschakeld. Hierdoor wordt het risico kleiner dat betalingen worden gegenereerd op het moment dat blanco cheques worden gemaakt. Als de verwerking is voltooid, wordt de bijbehorende bankrekening opnieuw geactiveerd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]