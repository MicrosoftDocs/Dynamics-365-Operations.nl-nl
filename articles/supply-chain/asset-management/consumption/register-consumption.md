---
title: Verbruik registreren
description: In dit onderwerp wordt uitgelegd hoe u verbruik registreert in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024655"
---
# <a name="register-consumption"></a>Verbruik registreren

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Wanneer een onderhoudstaak voor een werkorder is voltooid, is de volgende stap het maken van verbruiksregistraties en het boeken van de journalen. U kunt registraties maken voor de volgende verbruikstypen: uren, artikelen en onkosten. De verschillende verbruikstypen worden geregistreerd en geboekt op de pagina **Werkorderjournalen**. De journaalinstellingen in **Activabeheer** worden gebruikt voor het maken en boeken van afzonderlijke journalen voor uren, artikelen en onkosten in de module **Projectbeheer en boekhouding**.

U kunt mogelijk prognoseregels toevoegen aan of verwijderen uit een werkorder. De instelling van een levenscyclusstatus, het gerelateerde project type en de faseregels die betrekking hebben op het projecttype bepalen of u journaalregels kunt toevoegen of bewerken. Lees meer over de levenscyclusstatussen van werkorders en gerelateerde projectfasen in [Integratie met Projectbeheer en boekhouding](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>U kunt het automatisch boeken van journalen instellen in de levenscyclusstatus van werkorders. Zie [Levenscyclusstatussen van werkorder](../setup-for-work-orders/work-order-lifecycle-states.md) voor meer informatie.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en klik op **Journalen**.

3. Klik op **Kopiëren van prognose** om prognoseregels over te boeken die mogelijk met de werkorder zijn verbonden. U kunt selecteren welke verbruikstypen u wilt overbrengen.

4. U kunt zo nodig meer verbruiksregels toevoegen op het relevante sneltabblad door op **Regel toevoegen** te klikken en gegevens op de regel in te vullen.

5. Klik op **Journalen valideren** om de journaalregels te valideren voordat deze worden geboekt.

6. Klik op **Journalen boeken** om de journaalregels te boeken.

7. Nadat u de verbruiksjournalen hebt geboekt, kunt u de levenscyclusstatus van de werkorder bijwerken, bijvoorbeeld naar Beëindigd, om aan te geven dat de werkorder is voltooid.

- Selecteer in het veld **Weergeven** boven aan de pagina **Werkorderjournalen** de journaalregels die u wilt zien: Alle, Niet geboekt of Geboekt. Voor geboekte journalen is het selectievakje **Geboekt** ingeschakeld.  
- Wanneer er artikelregels worden gemaakt in het werkorderjournaal, worden productdimensies en traceringsdimensies die betrekking hebben op het artikel automatisch overgenomen op de journaalregel.  

In de volgende schermafbeelding ziet u een voorbeeld van uren- en artikelregistraties in een werkorder in **Werkorderjournalen**.

![Figuur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Uren splitsen in werkorders met meerdere werkordertaken

Als een werkorder verschillende werkordertaken bevat, kunt u openingstijden registreren met de functie **Uren splitsen**, wat betekent dat één uurregistratieregel gelijkmatig kan worden verdeeld over alle werkordertaken.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en klik op **Journalen**.

3. Selecteer de uurregistratieregel die u wilt splitsen en klik op **Uren splitsen**.

4. In het dialoog venster **Gesplitste uren voor onderhoudstaken voor werkorders** wordt de naam van de medewerker die is aangemeld automatisch weergegeven in het veld **Medewerker**. Selecteer desgewenst een andere medewerker.

5. Selecteer een categorie voor de uurregistratie in het veld **Categorie**.

6. Voeg in het veld **Uren** het aantal werkuren in dat moet worden gesplitst.

![Figuur 2](media/02-consumption.png)

7. Klik op **OK**.

*Voorbeeld*: in de onderstaande schermafbeelding worden journaalregels voor een werkorder met drie werkordertaken weergegeven. De eerste regel, met drie werkuren, is gesplitst en één uur wordt geregistreerd voor elke werkordertaak. Nadat de drie uurregistratieregels zijn gemaakt, beslist u wat u met de oorspronkelijke uurregistratieregel wilt doen (de eerste regel in het voorbeeld). U kunt deze houden of verwijderen. 

![Figuur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Financiële dimensies voor verbruiksregistraties

Wanneer u verbruiksregistraties uitvoert, worden financiële dimensies met betrekking tot de verschillende registratietypen in een specifieke volgorde aan de registraties toegevoegd. 

*Uur- en onkostenregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing. Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd. Tot slot worden financiële dimensies van de resource (medewerker) toegevoegd.

*Uurregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing. Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd. Vervolgens worden financiële dimensies van de site toegevoegd. Tot slot worden financiële dimensies van het artikel toegevoegd.

>[!NOTE]
>Voor alle drie de registratietypen wordt de combinatie van financiële dimensies gevalideerd en ongeldige combinaties worden blanco gemaakt. Dit zijn standaardinstellingen in Finance and Operations.

