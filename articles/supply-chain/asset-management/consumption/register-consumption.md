---
title: Verbruik registreren
description: In dit onderwerp wordt uitgelegd hoe u verbruik registreert in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c59664346c07f5e74825de41870f6635ced24ebd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216302"
---
# <a name="register-consumption"></a>Verbruik registreren

[!include [banner](../../includes/banner.md)]

 

Wanneer een onderhoudstaak voor een werkorder is voltooid, is de volgende stap het maken van verbruiksregistraties en het boeken van de journalen. U kunt registraties maken voor de volgende verbruikstypen: uren, artikelen en onkosten. De verschillende verbruikstypen worden geregistreerd en geboekt op de pagina **Werkorderjournalen**. De journaalinstellingen in **Activabeheer** worden gebruikt voor het maken en boeken van afzonderlijke journalen voor uren, artikelen en onkosten in de module **Projectbeheer en boekhouding**.

In sommige gevallen kunt u prognoseregels toevoegen aan of verwijderen uit een werkorder. De instelling van een levenscyclusstatus, het gerelateerde project type en de faseregels die betrekking hebben op het projecttype bepalen of u journaalregels kunt toevoegen of bewerken. Zie [Prognoses, werkorders en projecten](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md) voor meer informatie over levenscyclusstatussen van werkorders en gerelateerde projectfasen.

>[!NOTE]
>U kunt het automatisch boeken van journalen instellen in de levenscyclusstatus van werkorders. Zie [Levenscyclusstatussen van werkorder](../setup-for-work-orders/work-order-lifecycle-states.md) voor meer informatie.

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en klik op **Journalen**.

3. Klik op **Kopiëren van prognose** om prognoseregels over te boeken die mogelijk met de werkorder zijn verbonden. U kunt selecteren welke verbruikstypen u wilt overbrengen.

4. U kunt zo nodig meer verbruiksregels toevoegen op het relevante sneltabblad door op **Regel toevoegen** te klikken en gegevens op de regel in te vullen.

5. Klik op **Journalen valideren** om de journaalregels te valideren voordat deze worden geboekt.

6. Klik op **Journalen boeken** om de journaalregels te boeken.

7. Nadat u de verbruiksjournalen hebt geboekt, kunt u de levenscyclusstatus van de werkorder bijwerken. Als u bijvoorbeeld wilt aangeven dat de werkorder is voltooid, kunt u de levenscyclusstatus wijzigen in 'Beëindigd'.

    - Selecteer in het veld **Weergeven** bovenaan de pagina **Werkorderjournalen** de journaalregels die u wilt zien: **Alle**, **Niet geboekt** of **Geboekt**. Voor geboekte journalen is het selectievakje **Geboekt** ingeschakeld.  
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

- *Uur- en onkostenregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing. Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd. Tot slot worden financiële dimensies van de resource (medewerker) toegevoegd.

- *Uurregistraties:* eerst worden financiële dimensies uit de journaalkoptekst toegevoegd, indien van toepassing. Vervolgens worden financiële dimensies uit het gerelateerde werkorderproject toegevoegd. Vervolgens worden financiële dimensies van de site toegevoegd. Tot slot worden financiële dimensies van het artikel toegevoegd.

>[!NOTE]
>Voor alle drie de registratietypen wordt de combinatie van financiële dimensies gevalideerd en ongeldige combinaties worden blanco gemaakt. Dit is standaardinstelling bij andere Finance and Operations-apps.

