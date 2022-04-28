---
title: Opslag van ouderdomsgegevens van klanten
description: In dit onderwerp wordt het proces beschreven waarbij externe opslag wordt gebruikt voor ouderdomsgegevens van klanten. U kunt het opslagproces voor ouderdomsgegevens van klanten uitvoeren om de uitvoer beschikbaar te maken voor export naar een extern systeem.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 497d49da84f4df90877908bef3031e079bc36066
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557873"
---
# <a name="customer-aging-data-storage"></a>Opslag van ouderdomsgegevens van klanten

[!include [banner](../includes/banner.md)]


In dit onderwerp wordt het proces beschreven waarbij externe opslag wordt gebruikt voor ouderdomsgegevens van klanten. In Microsoft Dynamics 365 Finance kunt u het opslagproces voor ouderdomsgegevens van klanten uitvoeren om de uitvoer beschikbaar te maken voor export naar een extern systeem. Wanneer u het proces uitgevoerd, zijn de opties voor naar ouderdom gerangschikte rapporten die beschikbaar zijn in het systeem gelijk aan de opties die beschikbaar zijn voor externe systemen. De details worden altijd opgenomen in de geëxporteerde gegevens.

Het kan helpen ouderdomsgegevens van klanten beschikbaar te maken voor opslag in gevallen waarin de uitvoer veel klanten en/of transacties bevat. Als er een time-out optreedt voor het bestaande rapport **Naar ouderdom gerangschikt rapport voor klanten** omdat er te veel gegevens zijn om af te drukken, biedt deze functie een alternatieve manier om dezelfde gegevens op te halen.

## <a name="enable-the-customer-aging-data-storage-feature"></a>De functie voor gegevensopslag van naar ouderdom gerangschikte gegevens van klanten inschakelen

Voordat u deze functie kunt gebruiken, moet u deze inschakelen in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor functiebeheer om de status van de functie te controleren en desgewenst in te schakelen. Schakel in de werkruimte **Functiebeheer** de functie als volgt in:

- **Module:** crediteringen en aanmaningen
- **Functienaam:** gegevensopslag van naar ouderdom gerangschikte gegevens van klanten

## <a name="run-the-customer-aging-data-storage-process"></a>Het proces voor gegevensopslag van naar ouderdom gerangschikte gegevens van klanten uitvoeren

1. Ga naar **Crediteringen en aanmaningen \> Query's en rapporten \> Klant \> Opslag van ouderdomsgegevens van klanten**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Naam** een naam in voor het proces.
4. Stel naar behoefte de resterende parameters in.

    > [!NOTE]
    > Transactiedetails worden altijd opgenomen en de verwerking wordt altijd uitgevoerd in een batchtaak.

5. Selecteer **OK**.
6. Vernieuw de pagina **Opslag van ouderdomsgegevens van klanten** zodat de waarden **Batchnaam** en **Batchverwerkingstijd** worden weergegeven, samen met de waarde voor **Verwerkingsstatus**. Wanneer de batchtaak is voltooid, wordt het veld **Verwerkingsstatus** ingesteld op **Beëindigd** en wordt het veld **Aantal ouderdomsregels** ingesteld. Als de batchtaak terugkerend is, wordt het veld **Verwerkingsstatus** ingesteld op **Wachten**.
7. Selecteer de knop **Filteren** naast het veld **Aantal ouderdomsregels** om de filters te controleren die zijn toegevoegd voor de batchtaak.

De pagina **Opslag van ouderdomsgegevens van klanten** bevat geen resultaten. Met de gegevensentiteit **Opslag van ouderdomsgegevens van klanten** kunt u echter de uitvoer exporteren naar elke indeling die door Gegevensbeheer wordt ondersteund.

> [!NOTE]
> Voordat u een export uitvoert, voegt u een filter toe om de geëxporteerde resultaten te beperken tot de meest recente ouderdom. Voeg bijvoorbeeld de volgende criteria toe om de meest recente batchrun te retourneren:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> U kunt ook de volgende criteria toevoegen om de meest recente batchrun voor de huidige gebruiker te retourneren:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
