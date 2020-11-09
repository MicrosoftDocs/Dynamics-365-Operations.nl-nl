---
title: Een leverancierrekening maken
description: Deze procedure laat zien hoe u een leveranciersrekening maakt en een adres en contactgegevens toevoegt.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017202"
---
# <a name="create-a-vendor-account"></a>Een leverancierrekening maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een leveranciersrekening maakt en een adres en contactgegevens toevoegt. De procedure toont niet hoe u alle velden vult voor inkoop- en financiële doelen. Voor meer informatie over deze velden leest u de veldbeschrijvingen. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. Leveranciersrekeningen worden gewoonlijk gemaakt door een inkoop- of debiteurenmedewerker.


## <a name="create-a-vendor-account"></a>Een leverancierrekening maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Leveranciersrekening**.
    - De waarde kan automatisch worden ingevuld. Zo ja, dan kunt u deze stap overslaan.  
    - U kunt leveranciersrekeningen voor een persoon of een organisatie maken. Dit zal beïnvloeden welke velden beschikbaar zijn. In dit voorbeeld wordt een leveranciersrekening voor een organisatie gemaakt.   
4. Typ of selecteer een waarde in het veld **Naam**. Als de leverancier reeds een geregistreerde partij in uw systeem is kunt u de vervolgkeuzelijst gebruiken en een item in dit veld selecteren. De nieuwe leveranciersrekening neemt dan het adres en de contactgegevens over die al zijn geregistreerd.
5. Typ of selecteer een waarde in het veld **Groep**. De leveranciersgroep wordt gebruikt om leveranciers te groeperen die een van de volgende parameters gemeenschappelijk hebben: betalingsvoorwaarden, vereffeningsperiode, grootboekrekeningen voor voorraadboeking (met inbegrip van de btw-groep), standaardgrootboekrekeningen, productfiltercodes of aanbodprognoseconfiguratie.
6. Voer in het veld **Aantal werknemers** een getal in.
7. Typ een waarde in het veld **Organisatienummer**.

## <a name="add-an-address"></a>Een adres toevoegen
1. Vouw de sectie **Adressen** uit.
2. Klik op **Toevoegen**.
3. Typ of selecteer een waarde in het veld **Doel**. U kunt een of meerdere doelen selecteren. Deze worden gebruikt om het juiste adres voor een bepaald doel te selecteren. Als bijvoorbeeld "Factuur" het doel is, wordt dat adres gebruikt wanneer u facturen verzendt.
4. Typ een waarde in het veld **Naam of omschrijving**.
5. Typ of selecteer een waarde in het **veld Land/regio**. Voer de adresgegevens in. Het land/regio dat u hebt geselecteerd bepaalt welke velden u ziet, corresponderend met de adresindeling voor het land/regio. 
6. Klik op **OK**.

## <a name="add-contact-information"></a>Contactgegevens toevoegen
1. Vouw de sectie **Contactgegevens** uit.
2. Klik op **Toevoegen**.
3. Typ een waarde in het veld **Beschrijving**.
4. Selecteer een optie in het veld **Type**.
5. Typ een waarde in het veld **Contactnummer/-adres**. U kunt het selectievakje Primair inschakelen als dit de primaire contactpersoon is.  
6. Klik op **Opslaan**.
7. Sluit de pagina.
8. Sluit de pagina.

