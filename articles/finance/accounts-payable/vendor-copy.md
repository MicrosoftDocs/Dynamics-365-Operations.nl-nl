---
title: Leveranciers kopiëren met behulp van gedeelde nummerreeksen
description: In dit onderwerp wordt uitgelegd hoe u gedeelde nummerreeksen kunt gebruiken om een leverancier te kopiëren naar een andere rechtspersoon, maar met behoud van dezelfde leverancier-id.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4cea8269082b39e2374ffb3c3dc82def8ce35679
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358460"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Leveranciers kopiëren met behulp van gedeelde nummerreeksen

[!include [banner](../includes/banner.md)]

U kunt gedeelde nummerreeksen gebruiken om leverancier-id's toe te wijzen. Met gedeelde nummerreeksen kunt u ook leveranciers kopiëren van de ene rechtspersoon naar een andere, maar dezelfde leverancier-id's gebruiken voor beide rechtspersonen.

## <a name="setup"></a>Instellen

De functie wordt geactiveerd wanneer u een gedeelde nummerreeks gebruikt om leverancier-id's toe te wijzen. In elke rechtspersoon waarnaar u een leverancier wilt kopiëren, moet u dezelfde nummerreeks gebruiken. U wijzigt de nummerreeks voor de leverancier op de pagina **Parameters van module Leveranciers** voor elke rechtspersoon. Selecteer **Leveranciers** \> **Instellen** \> **Parameters van module Leveranciers** en selecteer vervolgens het tabblad **Nummerreeksen**.

U kunt ook nummerreeksen voor elke leveranciersgroep instellen. Deze nummerreeksen moeten ook worden gedeeld. Eerst wordt de nummerreeks voor een leveranciersgroep gebruikt. Als er geen nummerreeks is opgegeven voor een leveranciersgroep, wordt de nummerreeks gebruikt die is opgegeven op de pagina **Parameters van module Leveranciers**.

U kunt ook leveranciers kopiëren tussen rechtspersonen als u handmatige leverancier-id's gebruikt. Als u echter een leverancier probeert te kopiëren naar een rechtspersoon waar de leverancier-id al bestaat, wordt het kopieerproces niet gestart.

## <a name="copy-a-vendor"></a>Een leverancier kopiëren

Als u een leverancier wilt kopiëren, selecteert u **Nieuw** op de lijstpagina **Alle leveranciers** om de pagina **Alle leveranciers, nieuwe record** te openen. De nieuwe leverancier-id wordt niet onmiddellijk toegewezen. Dit gedrag wijkt af van het gedrag in eerdere versies. Omdat u de leveranciersgroep nog niet hebt geselecteerd, kan niet de juiste nummerreeks worden bepaald die moet worden gebruikt. Het kan bovendien niet bepalen of u een nieuwe leverancier wilt maken of een leverancier kopieert. Daarom wordt de leverancier-id pas toegewezen als u **Opslaan** selecteert onderaan op de pagina.

Als u een nieuwe leverancier maakt, kunt u zoals gebruikelijk verdergaan met het invullen van de velden. Wanneer u klaar bent en **Opslaan** selecteert, wordt de leverancier-id automatisch toegewezen. Bij handmatige nummerreeksen ziet u dat de handmatige leverancier-id is gebruikt.

Als u een leverancier wilt kopiëren, voert u in het veld **Naam** een of meer tekens in die de leverancier aangeven die u zoekt. In het dialoogvenster Zoeken ziet u een overzicht van de partijen die mogelijk de gezochte leverancier aangeven. Wanneer u een van de partijen selecteert, wordt aanvullende informatie aan de rechterkant van het dialoogvenster weergegeven:

- Op het tabblad **Algemeen** ziet u het telefoonnummer en het adres van de partij.
- Op het tabblad **Rollen** ziet u de rollen die de geselecteerde partij kan hebben en de rechtspersoon waarin de partij een rol heeft.
- Het tabblad **Belastingregistratie-id** geeft de belastingregistratie-id's weer die zijn toegewezen aan de partij.

U kunt een partij alleen kopiëren als deze een leverancierrol heeft in een rechtspersoon die niet de huidige rechtspersoon is. Volg deze stappen als u een partij vindt die aan deze criteria voldoet.

1. De optie **Leverancier kopiëren** wordt weergegeven. Standaard is deze optie ingesteld op **Nee**. Als u de leverancier naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**. 
2. Het veld **Rechtspersoon** wordt weergegeven. Selecteer de rechtspersoon waarvan u de leverancier wilt kopiëren. Als de leverancier alleen in één rechtspersoon bestaat, wordt het veld standaard ingesteld op die rechtspersoon.
3. Selecteer **Selecteren**. De leverancier wordt gemaakt.

## <a name="validation"></a>Validatie

Wanneer u een leverancier kopieert, wordt geprobeerd de gegevens van de nieuwe leverancier op te slaan. Er worden validaties uitgevoerd om te controleren of de gekopieerde gegevens correct zijn. U ontvangt een foutbericht voor elke mislukte validatie. In het foutbericht wordt uitgelegd welke gegevens moeten worden bijgewerkt. De kopie van de leverancier kan pas worden opgeslagen als u alle validatiefouten hebt opgelost.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Een leverancier kopiëren met de functie Btw-nummer zoeken

U kunt leveranciers ook kopiëren met de functie **Btw-nummer zoeken** die u vindt in de groep **Registratie** op het tabblad **Leverancier** in het actievenster van de pagina **Alle leveranciers**. In het dialoogvenster **Btw-nummer zoeken** dat wordt weergegeven, ziet u btw-nummers, de leverancier-id, de naam van de leverancier en de rechtspersoon waarin de btw-id wordt gebruikt. U kunt een leverancier alleen kopiëren als deze bij een rechtspersoon hoort die niet de huidige rechtspersoon is. Nadat u een leverancier hebt geselecteerd die aan dit criterium voldoet, volgt u deze stappen.

1. De optie **Leverancier kopiëren** wordt weergegeven. Standaard is deze optie ingesteld op **Nee**. Als u de leverancier naar de huidige rechtspersoon wilt kopiëren, zet u de optie op **Ja**.
2. Selecteer **Selecteren**. De leverancier wordt gemaakt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
