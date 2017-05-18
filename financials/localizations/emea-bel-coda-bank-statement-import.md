---
title: CODA-bankafschrift
description: Dit onderwerp bevat informatie over CODA. Dit is een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, BankCodaAccountStatement, BankCodaAccountStatementLines, BankCodaParameters, BankCodaTrans, BankCodaTransCategory, BankCodaTransDefTable, BankCodaTransFamily
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262534
ms.assetid: 38a1f540-1488-4b63-b850-04e270622296
ms.search.region: Belgium
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c9fd101561ad2b699e813d47541a28a0978171a4
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="coda-bank-statement"></a>CODA-bankafschrift

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat informatie over CODA. Dit is een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt. 

Voor importen van Belgische bankoverzichten gebruikt u de CODA-bestandsindeling. Met deze functie kunt u begin- en eindsaldi van bedrijfsbankrekeningen controleren en kunt u geïmporteerde transacties op basis van afstemmingsregels afstemmen.

## <a name="import-transactions-from-a-bank-statement"></a>Transacties van een bankafschrift importeren
Voer de volgende stappen uit om een bankafschriftbestand voor een bankrekening te importeren. **Opmerking**: voordat u een bankafschriftbestand importeert, moet u het volgende al hebben uitgevoerd:

-   De CODA-configuraties vanuit Lifecycle Services (LCS) importeren Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Selecteer de geïmporteerde CODA-configuratie op de pagina **CODA-parameters**.

1.  Ga naar de pagina **Bankrekeningen**.
2.  Klik op **Afstemmen** &gt; **CODA**.
3.  Klik op **CODA** &gt; **Importeren uit bestand** en selecteer vervolgens het pad naar het bankafschriftbestand.

Nadat u transacties hebt geïmporteerd, kunt u het volgende doen op de pagina **Bankafschrift**.

-   De begin- en eindsaldi controleren.
-   De geïmporteerde transacties weergeven als een bankafschriftrapport dat u kunt afdrukken.
-   Geïmporteerde transacties weergeven met extra regels, zoals regels met het rekeningtype 'Geen'. Klik op **CODA &gt; Details**.

## <a name="process-imported-bank-statement-transactions"></a>Geïmporteerde bankafschrifttransacties verwerken
Voer de volgende stappen uit om de bankafschrifttransacties te verwerken.

1.  Verwerk detailregels (**CODA** &gt; **Detailregels verwerken**). Start automatisch afstemmen op basis van **CODA-definities**. Deze regels bepalen welk grootboek of welke klant of leverancier moet worden gebruikt voor deze transactie. De vergelijking wordt gebaseerd op welke transactiegroepscode, transactiecode en transactiecategoriecode zijn opgegeven in het CODA-bestand voor elke transactie.
2.  Transacties met een klant- en leveranciersrekeningtype kunnen worden vergeleken met de facturen. Indien nodig kunnen geïmporteerde transacties handmatig op elk gewenst moment na verwerking worden gewijzigd, alvorens ze worden overgeboekt naar het grootboek.
3.  Als er transacties met fouten zijn (in het algemeen als er geen regels zijn ingesteld), kunnen deze worden verwezen naar de speciale grootboekrekening die is opgegeven op de pagina **CODA-parameters**(**CODA** &gt; **Fouten wissen**).
4.  Nadat alle transacties in het bankafschrift zijn vereffend, kunnen ze worden overgeboekt naar het grootboekjournaal (**CODA** &gt; **Overboeken naar grootboek**). Voor de bankrekening moeten journaalinstellingen worden opgegeven. Journalen kunnen worden geopend op de pagina Bankrekeningen voor de geselecteerde record door te klikken op **Instellen** &gt; **CODA-journaal**.

Nadat bankafschrifttransacties zijn verwerkt, wordt een nieuw grootboekjournaal gemaakt en is deze gereed voor boeking.




