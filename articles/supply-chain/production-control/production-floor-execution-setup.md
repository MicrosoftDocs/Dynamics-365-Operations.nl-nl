---
title: Een apparaat instellen om de uitvoeringsinterface voor de werkvloer uit te voeren
description: De uitvoeringsinterface van de werkvloer wordt ingesteld voor elk apparaat op de werkvloer. Bedrijven stellen meestal elk apparaat anders in, afhankelijk van het doel van het apparaat. Een bedrijf kan bijvoorbeeld één apparaat in de receptie hebben staan, waar werknemers in- en uitklokken en een ander apparaat op de werkvloer, waar werknemers hun taken beheren.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9a5911e81547134d3034d1a47ef94c553ccbb331
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353959"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Een apparaat instellen om de uitvoeringsinterface voor de werkvloer uit te voeren

[!include [banner](../includes/banner.md)]

De uitvoeringsinterface van de werkvloer wordt ingesteld voor elk apparaat op de werkvloer. Bedrijven stellen meestal elk apparaat anders in, afhankelijk van het doel van het apparaat. Een bedrijf kan bijvoorbeeld één apparaat in de receptie hebben staan, waar werknemers in- en uitklokken en een ander apparaat op de werkvloer, waar werknemers hun taken beheren.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>De configuratie en filters voor een specifiek apparaat instellen

Als u de configuratie en taakfilters voor een apparaat wilt instellen, meldt u zich aan bij de pagina **Uitvoering werkvloer** met een account die een beveiligingsrol heeft die over het recht *Tijdsupervisor beheren* beschikt. (Van de standaardbeveiligingsrollen heeft alleen *Werkvloersupervisor* dit recht.) Voer vervolgens de volgende stappen uit.

1. Ga naar het apparaat dat u wilt instellen en meld u aan bij Microsoft Dynamics 365 Supply Chain Management als werkvloersupervisor. (Gebruik een account die over het recht *Tijdsupervisor beheren* beschikt.)
1. Controleer of er een configuratie beschikbaar is voor het apparaat dat u instelt. Als er nog geen configuratie bestaat, wordt een standaardconfiguratie opgegeven. Zie [Uitvoeringsinterface van de werkvloer configureren](production-floor-execution-configure.md) voor meer informatie over het instellen van een configuratie.
1. Ga naar **Productiebeheer \> Productie-uitvoering \> Uitvoering werkvloer**.

    Als de uitvoeringsinterface van de werkvloer al minimaal één keer is geconfigureerd voor het huidige apparaat, wordt een aanmeldingspagina weergegeven. Anders verschijnt er een welkomstpagina.

1. Selecteer op de aanmeldingspagina of de welkomstpagina de optie **Configureren**.
1. Selecteer een configuratie in de lijst.
1. Selecteer **Volgende**.
1. Selecteer een of meer filters die u op het huidige apparaat wilt toepassen. Met deze filters wordt ervoor gezorgd dat alleen relevante taken op het apparaat worden weergegeven. Als u een filter wilt instellen, selecteert u het filtertype om een lijst met waarden te openen en selecteert u vervolgens de waarde waarop u wilt filteren. De volgende filters zijn beschikbaar:

    - **Productie-eenheid**: dit filter is het filter op het hoogste niveau. Het verwijst meestal naar een groot werkgebied met verschillende resourcegroepen die afzonderlijke resources bevatten.
    - **Resourcegroep**: dit filter is een filter op gemiddeld niveau. Het verwijst meestal naar een verzameling verwante resources in een beperkt gebied van de werkruimte. Als u eerst het filter **Productie-eenheid** selecteert, worden in de lijst met resourcegroepen alleen de groepen van die eenheid weergegeven. Anders worden alle beschikbare resourcegroepen weergegeven.
    - **Resource**: dit filter is het meest specifieke filter. Het verwijst meestal naar een specifieke machine of een andere afzonderlijke resource. Als u eerst het filter **Resourcegroep** en/of **Productie-eenheid** selecteert, worden in de lijst met resources alleen resources van die groep en/of eenheid weergegeven. Anders worden alle beschikbare resources weergegeven.

1. Selecteer **OK**.
1. De aanmeldingspagina wordt weergegeven en uw apparaat is gereed voor gebruik.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Een werknemer toestaan de standaardfilters te overschrijven

U kunt specifieke werknemers machtigen om de filterinstellingen te wijzigen op een apparaat dat ze gebruiken. Voor werknemers die over deze machtiging beschikken, biedt de uitvoeringsinterface van de werkvloer de knop **Filter** op de pagina's **Alle taken** en **Actieve taak**.

> [!NOTE]
> Als een werknemer een filter wijzigt, is het nieuwe filter vanaf dat punt van toepassing voor alle gebruikers die zich aanmelden bij het apparaat.

Voer de volgende stappen uit om een werknemer toe te staan de standaardtaakfilters te overschrijven die voor een apparaat zijn ingesteld.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Tijdregistratiewerknemers**.
1. Selecteer een werknemer in de lijst om de pagina **Tijdregistratiewerknemers** te openen.
1. Stel op het tabblad **Tijdregistratie** de optie **Filters instellen** in op *Ja*.

## <a name="run-the-interface-in-full-screen-mode"></a>De interface op volledig scherm uitvoeren

Vaak wordt de uitvoeringsinterface van de werkvloer uitgevoerd op een apparaat dat uitsluitend voor dat doel wordt gebruikt. Daarom kan het zinvol zijn om de interface op volledig scherm uit te voeren zonder dat er navigatie en/of de browser Chrome wordt weergegeven.

- Als u het navigatiedeelvenster wilt verbergen dat wordt weergegeven in Supply Chain Management, voegt u de volgende tekst toe aan het einde van de URL op de adresbalk van de browser: `\&limitednav=true`.
- Als u ook de adresbalk van de browser wilt verbergen, gebruikt u de native volledig-schermmodus van de browser. (Zie de documentatie van uw browser voor instructies.)

In het bovenste gedeelte van de volgende afbeelding ziet u hoe de interface er standaard uitziet. In het onderste gedeelte ziet u hoe de interface eruitziet in de modus Volledig scherm wanneer het navigatiedeelvenster is verborgen.

![Standaardinterface versus interface met volledig scherm.](media/pfei-full-screen.png "Standaardinterface versus interface met volledig scherm")

## <a name="extend-the-session-past-12-hours"></a>De sessie na 12 uur verlengen

Standaard wordt de uitvoeringsinterface van de werkvloer afgemeld als niemand deze gedurende 12 uur gebruikt. Een gebruiker van Supply Chain Management moet zich vervolgens opnieuw aanmelden. U kunt de time-outlimiet echter uitbreiden naar maximaal 90 dagen.

Als u de time-outlimiet wilt uitbreiden, meldt u zich aan bij Supply Chain Management en gaat u naar **Systeembeheer \> Gebruikers \> Sessieverlengingen**. Geef de gebruikersaccount voor Supply Chain Management op die wordt gebruikt om u aan te melden bij het apparaat en het aantal uren dat de sessie actief moet blijven.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]