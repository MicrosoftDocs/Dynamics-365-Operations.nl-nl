---
title: Klanten kopiëren met behulp van gedeelde nummerreeksen
description: In dit onderwerp wordt uitgelegd hoe u gedeelde nummerreeksen kunt gebruiken om een klant te kopiëren naar een andere rechtspersoon, maar met behoud van dezelfde klant-id.
author: abruer
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0a93f0519b292c12ea31a8faf3bff051fc111216
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753484"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Klanten kopiëren met behulp van gedeelde nummerreeksen

[!include [banner](../includes/banner.md)]

U kunt gedeelde nummerreeksen gebruiken om klant-id's toe te wijzen. Met gedeelde nummerreeksen kunt u ook klanten kopiëren van de ene rechtspersoon naar een andere, maar dezelfde klant-id's gebruiken voor beide rechtspersonen.

## <a name="setup"></a>Instellen

De functie wordt geactiveerd wanneer u een gedeelde nummerreeks gebruikt om klant-id's toe te wijzen. In elke rechtspersoon waarnaar u een klant wilt kopiëren, moet u dezelfde nummerreeks gebruiken. U wijzigt de nummerreeks voor de klant op de pagina **Parameters van module Klanten** voor elke rechtspersoon. Selecteer **Klanten** \> **Parameters** en selecteer vervolgens het tabblad **Nummerreeksen**.

U kunt ook nummerreeksen voor elke klantengroep instellen. Deze nummerreeksen moeten ook worden gedeeld. Eerst wordt de nummerreeks voor een klantengroep gebruikt. Als er geen nummerreeks is opgegeven voor een klantengroep, wordt de nummerreeks gebruikt die is opgegeven op de pagina **Parameters van module Klanten**.

U kunt ook klanten kopiëren tussen rechtspersonen als u handmatige klant-id's gebruikt. Als u echter een klant probeert te kopiëren naar een rechtspersoon waar de klant-ID al bestaat, wordt het kopieerproces niet gestart.

## <a name="copy-a-customer"></a>Een klant kopiëren

Als u een klant wilt kopiëren, selecteert u **Nieuw** op de lijstpagina **Alle klanten** om het dialoogvenster **Klant maken** te openen. U ziet dat de nieuwe klant-id niet onmiddellijk wordt toegewezen. Dit gedrag wijkt af van het gedrag in eerdere versies. Omdat u de klantengroep nog niet hebt geselecteerd, kan het systeem niet de juiste nummerreeks bepalen die moet worden gebruikt. Het kan bovendien niet bepalen of u een nieuwe klant wilt maken of een klant kopieert. Daarom wordt de klant-id pas toegewezen als u **Opslaan** selecteert onderaan in het dialoogvenster.

Als u een nieuwe klant maakt, kunt u zoals gebruikelijk verdergaan met het invullen van alle velden. Wanneer u klaar bent en **Opslaan** selecteert, ziet u dat de klant-ID automatisch is toegewezen. Bij handmatige nummerreeksen ziet u dat de handmatige klant-id is gebruikt.

Als u een klant wilt kopiëren, voert u in het veld **Naam** een of meer tekens in die de klant aangeven die u zoekt. In het dialoogvenster Zoeken ziet u een overzicht van de partijen die mogelijk de gezochte klant aangeven. Wanneer u een van de partijen selecteert, wordt aanvullende informatie aan de rechterkant van het dialoogvenster weergegeven:

- Op het tabblad **Algemeen** ziet u het telefoonnummer en het adres van de partij.
- Op het tabblad **Rollen** ziet u de rollen die de geselecteerde partij kan hebben en de rechtspersoon waarin de partij een rol heeft.
- Het tabblad **Belastingregistratie-id** geeft de belastingregistratie-id's weer die zijn toegewezen aan de partij.

U kunt een partij alleen kopiëren als deze een klantrol heeft in een rechtspersoon die niet de huidige rechtspersoon is. Volg deze stappen als u een partij vindt die aan deze criteria voldoet.

1. De optie **Klant kopiëren** wordt weergegeven. Standaard is deze optie ingesteld op **Nee**. Als u de klant naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**. 
2. Het veld **Rechtspersoon** wordt weergegeven. Selecteer de rechtspersoon waarvan u de klant wilt kopiëren. Als de klant alleen in één rechtspersoon bestaat, wordt het veld standaard ingesteld op die rechtspersoon.
3. Selecteer **Selecteren**. De klant wordt gemaakt.

## <a name="validation"></a>Validatie

Wanneer u een klant kopieert, probeert het systeem de gegevens van de nieuwe klant op te slaan. Er worden validaties uitgevoerd om te controleren of de gekopieerde gegevens correct zijn. U ontvangt een foutbericht voor elke mislukte validatie. In het foutbericht wordt uitgelegd welke gegevens moeten worden bijgewerkt. De kopie van de klant kan pas worden opgeslagen als u alle validatiefouten hebt opgelost.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Een klant kopiëren met de functie Btw-nummer zoeken

U kunt klanten ook kopiëren met de functie Btw-nummer zoeken die u vindt in de groep **Registratie** op het tabblad **Klant** in het actievenster van de pagina **Alle klanten**. In het dialoogvenster **Btw-nummer zoeken** dat wordt weergegeven, ziet u btw-nummers, de klant-id, de naam van de klant en de rechtspersoon waarin de btw-id wordt gebruikt. U kunt een klant alleen kopiëren als deze bij een rechtspersoon hoort die niet de huidige rechtspersoon is. Nadat u een klant hebt geselecteerd die aan dit criterium voldoet, volgt u deze stappen.

1. De optie **Klant kopiëren** wordt weergegeven. Standaard is deze optie ingesteld op **Nee**. Als u de klant naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**. 
2. Selecteer **Selecteren**. De klant wordt gemaakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
