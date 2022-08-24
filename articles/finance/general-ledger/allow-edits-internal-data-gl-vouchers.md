---
title: Bewerkingen in interne gegevens op boekstukken in het grootboek toestaan
description: Dit artikel biedt informatie over het bewerken van interne gegevens in boekstukken in het grootboek.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220647"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Bewerkingen in interne gegevens op boekstukken in het grootboek toestaan

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Wanneer u boekhoudingsposten in het grootboek boekt, wordt het veld **Omschrijving** vaak gebruikt voor het opslaan van interne notities of documentatie. Als de informatie onjuist is, kan dit tot verwarring leiden en het afsluiten van perioden lastiger maken. Met deze functie kan de accounting manager of supervisor fouten oplossen door het veld **Omschrijving** op geboekte boekstukken in het grootboek te bewerken.

Wijzigingen in geboekte boekstukken in het grootboek zijn beperkt tot gegevens van interne aard. Met deze functie kunt u nooit gegevens zoals bedragen, boekingsdatums, grootboekrekeningen en de transactievaluta bewerken. Wijzigingen in die gegevens beïnvloeden de externe rapportage van financiële overzichten en moeten alleen worden uitgevoerd via nieuwe boekstukken in het grootboek.

> [!NOTE]
> Voor Dynamics 365 Finance 10.0.29 is deze functie beperkt tot bewerkingen in het veld **Omschrijving**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Interne gegevens op boekstukken in het grootboek bewerken

Voordat interne gegevens in boekstukken in het grootboek kunnen worden bewerkt, moet u de functie **Bewerkingen in interne gegevens op boekstukken in het grootboek toestaan** in het werkgebied **Functiebeheer** inschakelen.
Nadat de functie is ingeschakeld, moet de gebruiker die geboekte boekstukken bewerkt, worden toegewezen aan de rol van accounting manager of supervisor. U kunt ook machtigingen aan andere rollen toevoegen door de beveiligingsrollen aan te passen.

Het bewerkingsproces is alleen toegestaan via de pagina Boekstuktransacties.

1. Ga naar **Grootboek** > **Query's en rapporten** > **Boekstuktransacties**.
2. Voer in het dialoogvenster **SysQuery** zoekcriteria in om boekstukken te selecteren.
3. Selecteer de regels voor de boekstukken die u wilt bewerken en selecteer vervolgens **Boekstuk bewerken** > **Interne boekstukgegevens bewerken**.

    [![De pagina Boekstuktransacties.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Op de pagina **Interne boekstukgegevens bewerken** worden de volgende gegevens weergegeven voor elke regel die u hebt geselecteerd:
  
  - Grootboekrekening
  - Rekeningnaam
  - Boekstuk
  - Huidige beschrijving
  - Nieuwe beschrijving

    [![Journaalboekstuk.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Alleen het veld **Nieuwe omschrijving** kan worden bewerkt. De waarde komt standaard overeen met de waarde van het veld **Huidige omschrijving**, zodat u kleine fouten in de omschrijving snel kunt oplossen.

4. Wijzig het veld **Nieuwe omschrijving** voor elke rij aan of verwijder de omschrijving uit elke rij.

   U kunt ook de volgende stappen uitvoeren als meerdere rijen met dezelfde waarde moeten worden bijgewerkt:

      1. Selecteer de rijen die u wilt bewerken en selecteer vervolgens **Geselecteerde records in bulk bijwerken**.
      2. Selecteer het veld dat u wilt bewerken in het veld **Te bewerken veld**. Momenteel omvat de opzoekactie alleen het veld **Nieuwe omschrijving**.
      3. Voer een nieuwe omschrijving in het veld **Nieuwe waarde** in.
      4. Selecteer **Bijwerken**. Alle geselecteerde records worden bijgewerkt met de nieuwe waarde.

      [![Het dialoogvenster Geselecteerde records in bulk bijwerken](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Voer in het veld **Reden voor bewerken** een aantekening in om aan te geven waarom de bewerking is uitgevoerd. Deze aantekening wordt weergegeven op de pagina **Audittrail van boekstukbewerkingen**.

   U kunt meerdere bewerkingen voor hetzelfde boekstuk uitvoeren en elke bewerking wordt bijgehouden.

## <a name="audit-trail-of-voucher-edits"></a>Audittrail van boekstukbewerkingen

Een audittrail wordt specifiek bijgehouden om de wijzigingen bij te houden die door deze functie zijn aangebracht. U kunt op twee manieren toegang krijgen tot het audittrail van boekstukbewerkingen:

  - Ga naar **Grootboek** > **Query's en rapporten** > **Boekstuktransacties**. Selecteer op de pagina **Boekstukcontrole** de optie **Boekstuk bewerken** > **Audittrail van boekstukbewerkingen**. De audittrail wordt alleen voor de geselecteerde boekstukrecord weergegeven. 
   
    Door de aanvraag op deze manier te openen, kunt u zich richten op alle bewerkingen die in één boekstukrecord zijn aangebracht.
  
  - Ga naar **Grootboek** > **Periodieke taken** > **Audittrail van boekstukbewerkingen**. Voer in het dialoogvenster criteria in om de boekstukken op te geven waarvoor u het audittrail van bewerkingen wilt weergeven. Als u het audittrail voor alle boekstukken wilt weergeven, laat u de criteria leeg en selecteert u **OK**. 
    
    Door de aanvraag op deze manier te openen, kunt u filteren op bewerkingen die op een bepaalde datum of door een bepaalde gebruiker zijn uitgevoerd.

De pagina **Audittrail van bewerkingen** toont de volgende informatie:

- **Aanmaakdatum en -tijd** – De datum en tijd van de bewerking.
- **Reden voor bewerking** – De reden die de gebruiker heeft ingevoerd voor de bewerking.
- **Gemaakt door** – De gebruiker die de bewerking heeft uitgevoerd.

Als u de details van een audittrail wilt weergeven, kunt u inzoomen op de waarde voor **Aanmaakdatum en -tijd**. Op de pagina **Eigenschappen van bewerkt boekstuk weergeven** wordt dezelfde informatie weergegeven als op de oorspronkelijke bewerkingspagina, inclusief de vorige omschrijving en de bijgewerkte omschrijving.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
