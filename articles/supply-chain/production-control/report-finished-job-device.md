---
title: Gereedmelden via het apparaat voor taakkaarten
description: In dit onderwerp wordt beschreven hoe u het systeem zo configureert dat gebruikers van een apparaat voor taakkaarten producten van een productieorder naar de voorraad kunnen gereedmelden.
author: johanhoffmann
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6ba5d8bc0c22f97e6d2ce61c636090e04fae5abd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425375"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Gereedmelden via het apparaat voor taakkaarten

[!include [banner](../includes/banner.md)]

Werknemers gebruiken de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten om voltooide hoeveelheden voor een productietaak te rapporteren. In dit onderwerp wordt beschreven hoe u verschillende opties instelt die bepalen hoe werknemers op deze pagina kunnen gereedmelden en wat er vervolgens gebeurt. De volgende opties zijn beschikbaar:

- Bepalen of en hoe hoeveelheden die zijn gereedgemeld, moeten worden toegevoegd aan voorraad.
- Bepalen of en hoe batchnummers worden gegenereerd en toegepast wanneer wordt gereedgemeld.
- Bepalen of en hoe serienummers worden gegenereerd en toegepast wanneer wordt gereedgemeld.
- Bepalen of en hoe wordt gereedgemeld naar een nummerplaat.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Bepalen of hoeveelheden die zijn gereedgemeld, moeten worden toegevoegd aan voorraad

Volg deze stappen om te bepalen of en hoe de hoeveelheden die zijn gereedgemeld voor de laatste bewerking, moeten worden toegevoegd aan voorraad.

1. Ga naar **Productiebeheer \> Instellingen \> Productieregistratie \> Standaardwaarden van productieorder**.
1. Stel op het tabblad **Rapporteren als gereed** het veld **Gereedmelding online bijwerken** in op een van de volgende waarden:

    - **Nee**: er wordt geen hoeveelheid aan voorraad toegevoegd wanneer hoeveelheden worden gerapporteerd voor de laatste bewerking. De status van de productieorder wordt nooit gewijzigd.
    - **Status + hoeveelheid**: de status van de productieorder wordt gewijzigd in *Gereedgemeld* en de hoeveelheid wordt gereedgemeld voor de voorraad.
    - **Hoeveelheid**: de hoeveelheid wordt gereedgemeld voor de voorraad, maar de status van de productieorder wijzigt nooit.
    - **Status**: alleen de status van de productieorder wordt gewijzigd. Er worden geen hoeveelheden aan voorraad toegevoegd wanneer hoeveelheden worden gerapporteerd voor de laatste bewerking.

> [!NOTE]
> Hoeveelheden worden niet in de voorraad bijgehouden als de bewerkingen waarvoor ze zijn gereedgemeld, niet zijn gedefinieerd als de laatste bewerking. Deze hoeveelheden kunnen echter worden gebruikt om de voortgang weer te geven. Ze kunnen ook worden opgenomen in regels die bepalen of werknemers de volgende bewerking kunnen starten voordat een gedefinieerde drempelwaarde van de gerapporteerde hoeveelheden voor de vorige bewerking wordt bereikt. U kunt deze regels definiëren op het tabblad **Validatie hoeveelheid** op de pagina **Standaardwaarden van productieorder**.

Zie [Productieparameters in Productieregistratie](production-parameters-manufacturing-execution.md) voor meer informatie over het werken met de pagina **Standaardwaarden van productieorder**.

## <a name="report-batch-controlled-items-as-finished"></a>Batchartikelen gereedmelden

Het apparaat voor taakkaarten ondersteunt drie scenario's voor het rapporteren van batchartikelen. Deze scenario's zijn zowel van toepassing op artikelen die zijn ingeschakeld voor geavanceerde magazijnprocessen als voor artikelen die niet zijn ingeschakeld voor geavanceerde magazijnprocessen.

- **Handmatig toegewezen batchnummers:** werknemers voeren een aangepast batchnummer in. Dit batchnummer kan afkomstig zijn van een externe bron die niet bekend is bij het systeem.
- **Vooraf gedefinieerde batchnummers:** werknemers selecteren een batchnummer in een lijst met batchnummers die automatisch door het systeem worden gegenereerd voordat de productieorder wordt vrijgegeven naar het apparaat voor taakkaarten.
- **Vaste batchnummers:** werknemers typen of selecteren geen batchnummer. In plaats daarvan wijst het systeem automatisch een batchnummer toe aan de productieorder voordat deze wordt vrijgegeven.


### <a name="enable-the-feature-on-your-system"></a>De functie inschakelen op uw systeem

Om ervoor te zorgen dat uw apparaat voor taakkaarten een batchnummer kan accepteren tijdens de gereedmelding, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de volgende functies in te schakelen (in deze volgorde):

1. Verbeterde gebruikerservaring voor het rapportvoortgangsvenster op het apparaat voor taakkaart
1. Schakel deze optie in als u batch- en serienummers wilt invoeren bij het gereedmelden vanaf het apparaat van de taakkaart (preview)

### <a name="configure-products-that-require-batch-number-reporting"></a>Producten configureren waarvoor rapportage van batchnummers nodig is

Voer de volgende stappen uit om een product de beschikbare scenario's voor batchcontrole te laten ondersteunen:

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product om te configureren.
1. Selecteer op het sneltabblad **Voorraad beheren** in het veld **Batchnummergroep** de traceringsnummergroep die is ingesteld om uw scenario te ondersteunen.

> [!NOTE]
> Als er geen batchnummergroep is toegewezen aan een batchproduct, biedt het apparaat voor taakkaarten tijdens het rapporteren als gereed standaard handmatige invoer voor het batchnummer.

In de volgende secties wordt beschreven hoe u traceringsnummergroepen instelt ter ondersteuning van elk van de drie scenario's voor het rapporteren van batchartikelen.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Een traceringsnummergroep instellen waarmee werknemers handmatig een batchnummer kunnen toewijzen

Voer de volgende stappen uit om een traceringsnummergroep in te stellen en handmatig toegewezen batchnummers toe te staan.

1. Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Handmatig** in op **Ja**.

    ![Een traceringsnummergroep voor handmatige batchnummers](media/tracking-number-group-manual.png "Een traceringsnummergroep voor handmatige batchnummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, is het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een tekstvak waarin werknemers een willekeurige waarde kunnen invoeren.

![De pagina Voortgang rapporteren met een veld voor handmatige batchnummers](media/job-card-device-batch-manual.png "De pagina Voortgang rapporteren met een veld voor handmatige batchnummers")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Een traceringsnummergroep instellen die een lijst met vooraf gedefinieerde batchnummers bevat

Voer de volgende stappen uit om een traceringsnummergroep in te stellen en een lijst met vooraf gedefinieerde batchnummers te bieden.

1. Ga naar **Voorraadbeheer \> Instellingen > Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Ja**.
1. Gebruik het veld **Per hoev.** om batchnummers per hoeveelheid te splitsen op basis van de waarde die u invoert. Stel dat u een productieorder hebt voor tien stuks en dat het veld **Per hoev.** is ingesteld op *2*. In dit geval worden er vijf batchnummers toegewezen aan de productieorder wanneer deze wordt gemaakt.

    ![Een traceringsnummergroep voor vooraf gedefinieerde batchnummers](media/tracking-number-group-predefined.png "Een traceringsnummergroep voor vooraf gedefinieerde batchnummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, is het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een vervolgkeuzelijst is waarin werknemers een vooraf gedefinieerde waarde moeten selecteren.

![De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde batchnummers](media/job-card-device-batch-predefined.png "De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde batchnummers")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Een traceringsnummergroep instellen waarmee automatisch batchnummers worden toegewezen

Als batchnummers automatisch moeten worden toegewezen, zonder invoer van de werknemer, voert u deze stappen uit om een traceringsnummergroep in te stellen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Nee**.
1. Stel de optie **Handmatig** in op **Nee**.

    ![Een traceringsnummergroep voor vaste batchnummers](media/tracking-number-group-fixed.png "Een traceringsnummergroep voor vaste batchnummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als batchnummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, bevat het veld **Batchnummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een waarde, maar kunnen werknemers deze niet bewerken.

![De pagina Voortgang rapporteren met een vast batchnummer](media/job-card-device-batch-fixed.png "De pagina Voortgang rapporteren met een vast batchnummer")

## <a name="report-serial-controlled-items-as-finished"></a>Artikelen met serienummers gereedmelden

Het apparaat voor taakkaarten ondersteunt drie scenario's voor het rapporteren van artikelen met serienummers. Deze scenario's zijn zowel van toepassing op artikelen die zijn ingeschakeld voor geavanceerde magazijnprocessen als voor artikelen die niet zijn ingeschakeld voor geavanceerde magazijnprocessen.

- **Handmatig toegewezen serienummers:** werknemers voeren een aangepast serienummer in. Dit serienummer kan afkomstig zijn van een externe bron die niet bekend is bij het systeem.
- **Vooraf gedefinieerde serienummers:** werknemers selecteren een serienummer in een lijst met batchnummers die automatisch door het systeem worden gegenereerd voordat de productieorder wordt vrijgegeven naar het apparaat voor taakkaarten.
- **Vaste serienummers:** werknemers typen of selecteren geen serienummer. In plaats daarvan wijst het systeem automatisch een serienummer toe aan de productieorder voordat deze wordt vrijgegeven.

### <a name="enable-the-feature-on-your-system"></a>De functie inschakelen op uw systeem

Om ervoor te zorgen dat uw apparaat voor taakkaarten een serienummer kan accepteren tijdens de gereedmelding, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de volgende functies in te schakelen (in deze volgorde):

1. Verbeterde gebruikerservaring voor het rapportvoortgangsvenster op het apparaat voor taakkaart
1. Schakel deze optie in als u batch- en serienummers wilt invoeren bij het gereedmelden vanaf het apparaat van de taakkaart (preview)

### <a name="configure-products-that-require-serial-number-reporting"></a>Producten configureren waarvoor rapportage van serienummers nodig is

Voer de volgende stappen uit om een product de beschikbare scenario's voor seriecontrole te laten ondersteunen:

Voer de volgende stappen uit om een scenario in te schakelen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het product om te configureren.
1. Selecteer op het sneltabblad **Voorraad beheren** in het veld **Serienummergroep** de traceringsnummergroep die is ingesteld om uw scenario te ondersteunen.

> [!NOTE]
> Als er geen serienummergroep is toegewezen aan een serieproduct, biedt het apparaat voor taakkaarten tijdens het rapporteren als gereed standaard handmatige invoer voor het serienummer.

In de volgende secties wordt beschreven hoe u traceringsnummergroepen instelt ter ondersteuning van elk van de drie scenario's voor het rapporteren van artikelen met serienummers.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Een traceringsnummergroep instellen waarmee werknemers handmatig een serienummer kunnen toewijzen

Voer de volgende stappen uit om een traceringsnummergroep in te stellen en handmatig toegewezen serienummers toe te staan.

1. Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Handmatig** in op **Ja**.

    ![Pagina Groepen traceringsnummers, serienummers](media/tracking-number-group-manual-serial.png "Pagina Groepen traceringsnummers, serienummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als serienummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, is het veld **Serienummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een tekstvak waarin werknemers een willekeurige waarde kunnen invoeren voor het serienummer. Bij het invoeren van een waarde wordt deze toegevoegd aan de lijst met serienummers. In deze lijst kunnen werknemers het volgende doen:

- Als u een serienummer als buiten gebruik wilt markeren, selecteert u de knop **Uitval** voor de desbetreffende rij. De werknemer wordt gevraagd een **Foutoorzaak** op te geven.
- Als u een serienummer wilt verwijderen, selecteert u de knop **Verwijderen** voor de desbetreffende rij.

![De pagina Voortgang rapporteren met een veld voor handmatige serienummers](media/job-card-device-serial-manual.png "De pagina Voortgang rapporteren met een veld voor handmatige serienummers")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Een traceringsnummergroep instellen die een lijst met vooraf gedefinieerde serienummers bevat

Voer de volgende stappen uit om een traceringsnummergroep in te stellen en een lijst met vooraf gedefinieerde serienummers te bieden.

1. Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Ja**.
1. Gebruik het veld **Per hoev.** om serienummers te splitsen per hoeveelheid van één.

    ![Een traceringsnummergroep voor vooraf gedefinieerde serienummers](media/tracking-number-group-predefined-sn.png "Een traceringsnummergroep voor vooraf gedefinieerde serienummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als serienummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, is het veld **Serienummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een vervolgkeuzelijst waarin werknemers een vooraf gedefinieerde waarde moeten selecteren.

![De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde serienummers](media/job-card-device-serial-predefined.png "De pagina Voortgang rapporteren met een lijst met vooraf gedefinieerde serienummers")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Een traceringsnummergroep instellen waarmee automatisch serienummers worden toegewezen

Als een serienummer automatisch moet worden toegewezen, zonder invoer van de werknemer, voert u deze stappen uit om een traceringsnummergroep in te stellen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Dimensies \> Traceringsnummergroepen**.
1. Maak of selecteer de traceringsnummergroep die u wilt instellen.
1. Stel op het sneltabblad **Algemeen** de optie **Alleen voor voorraadtransacties** in op **Nee**.
1. Stel de optie **Handmatig** in op **Nee**.

    ![Een traceringsnummergroep voor vaste serienummers](media/tracking-number-group-fixed-sn.png "Een traceringsnummergroep voor vaste serienummers")

1. Stel andere waarden in zoals u nodig hebt en selecteer vervolgens deze traceringsnummergroep als serienummergroep voor vrijgegeven producten waarvoor u dit scenario wilt gebruiken.

Wanneer u dit scenario gebruikt, bevat het veld **Serienummer** op de pagina **Voortgang rapporteren** op het apparaat voor taakkaarten een waarde, maar kunnen werknemers deze niet bewerken. Dit scenario is alleen relevant wanneer een productieorder wordt gemaakt voor een hoeveelheid van één stuk van een artikel met een serienummer.

![De pagina Voortgang rapporteren met een vast serienummer](media/job-card-device-serial-fixed.png "De pagina Voortgang rapporteren met een vast serienummer")

## <a name="report-as-finished-to-a-license-plate"></a>Melden als voltooid aan een nummerplaat

Met geavanceerde magazijnprocessen kan de nummerplaatdimensie worden gebruikt om de voorraad bij te houden voor magazijnlocaties die voor dit doel zijn ingesteld. In dat geval is het nummerplaatnummer vereist wanneer een werknemer hoeveelheden meldt als voltooid.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Afdrukken van nummerplaatrapportgae en -label inschakelen

Als u de functies wilt gebruiken die in deze sectie worden beschreven, moet u [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de volgende functies in te schakelen (in deze volgorde):

1. Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten
1. Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten
1. Label afdrukken vanaf apparaat voor taakkaart

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Melden als voltooid aan een nummerplaat instellen

Voer de volgende stappen uit om te bepalen of werknemers een bestaande nummerplaat opnieuw moeten gebruiken of een nieuwe nummerplaat moeten genereren wanneer ze hoeveelheden gereedmelden.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Taakkaart configureren voor apparaten**.
2. Stel voor elk apparaat de volgende opties in:

    - **Nummerplaat maken**: stel deze optie in op **Ja** om voor elke gereedmelding een nieuwe nummerplaat te genereren. Stel de optie in op **Nee** als een bestaande nummerplaat moet worden gebruikt voor elke gereedmelding.
    - **Label afdrukken**: stel deze optie in op **Ja** als de werknemer een nummerplaatlabel voor elke gereedmelding moet afdrukken. Stel deze optie in op **Nee** als geen label vereist is. 

![De pagina Taakkaart configureren voor apparaten](media/config-job-card-raf.png "De pagina Taakkaart configureren voor apparaten")

> [!NOTE]
> Ga naar **Magazijnbeheer \> Instellen \> Documentroutering \> Documentroutering** om het label te configureren. Zie [Afdrukken van nummerplaatlabel inschakelen](../warehousing/tasks/license-plate-label-printing.md) voor meer informatie.
