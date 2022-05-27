---
title: Geschiktheid voor inschrijving verwerken
description: In dit onderwerp wordt uitgelegd hoe u het proces voor het bepalen van de geschiktheid voor inschrijving uitvoert.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78a7de6dbb8d8ed13392eb7eb9aa02b15db2e009
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693166"
---
# <a name="process-enrollment-eligibility"></a>Geschiktheid voor inschrijving verwerken


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt uitgelegd hoe u het proces voor het bepalen van de geschiktheid voor inschrijving uitvoert.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Geschiktheid voor inschrijving verwerken**.

2. Geef in het dialoogvenster **Geschiktheidsproces voor inschrijving op vergoedingen uitvoeren** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Inschrijvingsperiode** | De inschrijvingsperiode waarvoor de geschiktheid voor inschrijving moet worden verwerkt. |
   | **Rechtspersoon** | De rechtspersoon waarvoor de geschiktheid voor inschrijving moet worden verwerkt. |
   | **Medewerker** | De medewerker waarvoor de geschiktheid voor inschrijving moet worden verwerkt. Als u dit veld leeg laat, wordt de geschiktheid voor inschrijving voor alle medewerkers verwerkt. |
   | **Vergoedingsplan** | Het vergoedingsplan waarvoor de geschiktheid voor inschrijving moet worden verwerkt.

3. Als u het proces op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Voer gegevens in voor het proces.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het proces wordt uitgevoerd met de parameters die u instelt.

4. Selecteer **OK**.

## <a name="view-process-results"></a>Procesresultaten weergeven

In dit onderwerp wordt uitgelegd hoe u de resultaten van het geschiktheidsproces weergeeft.

1.  Selecteer in het werkgebied **Vergoedingenbeheer** onder **Verwerken** de optie **Procesresultaten**.

2.  Op de pagina **Procesresultaten** zijn de volgende velden opgegeven:

   | Veld | Beschrijving |
   | --- | --- |
   | **Proces-ID** | De unieke id voor de combinatie van werknemer, rechtspersoon en procesuitvoering. |
   | **Procestype** | Hiermee wordt het proces aangegeven dat is uitgevoerd. Bijvoorbeeld: registratie. |
   | **Tijdstempel** | De tijd waarop het geschiktheidsproces is uitgevoerd. |
   | **Rechtspersoon** | De rechtspersoon die tijdens het registratieproces is opgegeven. |
   | **Werknemer** | De werknemer die is verwerkt. |
   | **Plan | Het vergoedingsplan waarvoor de registratie is gedaan. |
   | **Geschiktheidsregel** | De geschiktheidsregel die is verwerkt. Als er een fout is opgetreden voordat de geschiktheid werd uitgevoerd, is dit leeg. Bijvoorbeeld: als er geen compensatie voor een werknemer is gedefinieerd, wordt het geschiktheidsproces niet uitgevoerd en blijft dit veld leeg. |
   | **Resulterende status** | Dit komt wel of niet in aanmerking. De status van het resultaat komt niet in aanmerking als de werknemer niet voldoet aan de criteria voor de geschiktheidsregel, als er vereiste informatie ontbreekt voor de werknemer, zoals een betalingsfrequentie of vaste compensatie, of als er gegevens ontbreken in het vergoedingsplan waardoor werknemers niet kunnen worden ingeschreven. |
   | **Resulterend bericht** | Geeft aan waarom een werknemer niet in aanmerking komt voor een vergoedingsplan of is geslaagd voor een geschiktheidsregel. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
