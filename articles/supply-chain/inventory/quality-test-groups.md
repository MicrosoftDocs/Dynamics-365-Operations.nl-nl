---
title: Testgroepen voor kwaliteitsbeheer
description: In dit artikel wordt beschreven hoe u testgroepen maakt, zodat er meerdere tests kunnen worden gebruikt met kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7722bc92d8c2bf52d6a798a93f07af44037d4e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857688"
---
# <a name="quality-management-test-groups"></a>Testgroepen voor kwaliteitsbeheer

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u testgroepen maakt, zodat er meerdere tests kunnen worden gebruikt met kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.

U kunt de pagina **Testgroepen** gebruiken voor het instellen, bewerken en weergeven van testgroepen en van de afzonderlijke tests die aan deze testgroepen zijn toegewezen. In het bovenste gedeelte van de pagina worden de testgroepen weergegeven en in het onderste gedeelte worden de tests weergegeven die aan een geselecteerde testgroep zijn toegewezen.

U wijst verschillende beleidsregels toe aan een testgroep, zoals een bemonsteringsplan en een acceptabel kwaliteitsniveau en u geeft op of het uitvoeren van een destructieve test vereist is. Wanneer u vervolgens een afzonderlijke test aan een testgroep toewijst, definieert u extra informatie, zoals de volgorde, datums en geldigheidsdatums. Voor een kwantitatieve test omvatten de gedefinieerde gegevens ook de acceptabele meetwaarden. Voor een kwalitatieve test omvatten de gegevens de testvariabele en standaarduitkomst.

De testgroep die aan een kwaliteitsorder is toegewezen, bepaalt de standaardverzameling aan tests die moeten worden uitgevoerd op het opgegeven artikel. U kunt echter ook tests toevoegen aan, verwijderen uit of wijzigen in de kwaliteitsorder. De testresultaten worden vastgelegd voor elke test in een kwaliteitsorder.

Wanneer u een testgroep definieert, kunt u desgewenst een artikelbemonstering opgeven. Artikelbemonsteringen worden gebruikt om de hoeveelheid van het product te bepalen die moet worden getest. Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie. U kunt ook aangeven of de testen in een testgroep destructief zijn. In een destructieve test wordt de artikelbemonstering vernietigd en wordt de hoeveelheid uit de voorhanden voorraad verwijderd.

## <a name="example-of-a-test-group"></a>Voorbeeld van een testgroep

Een productiebedrijf stelt een testgroep in voor elke wijziging van in de kwaliteitsrichtlijnen van het bedrijf. De verschillende testgroepen vertegenwoordigen de verschillen in de bemonsteringsplannen, de verzameling tests die moet worden uitgevoerd, de AQL en andere factoren. Voor kwantitatieve tests zijn er ook verschillen in de acceptabele meetwaarden. Om zijn kwaliteitsrichtlijnen af te dwingen, wijst het bedrijf een testgroep toe aan elke regel die wordt gebruikt om automatisch kwaliteitsorders te genereren op de pagina **Kwaliteitskoppelingen**. Het bedrijf wijst ook een testgroep toe aan kwaliteitsorders die handmatig zijn gemaakt.

## <a name="create-a-test-group"></a>Een testgroep maken

Volg deze stappen om een testgroep te maken.

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Testgroepen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster in het bovenste deel van de pagina. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Testgroep**: voer een unieke id of naam op voor de testgroep in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de testgroep in.
    - **Acceptabel kwaliteitsniveau**: geef hier op hoeveel procent van de testresultaten van een groep van tests in totaal goed moet zijn om de tests als geslaagd te beschouwen.
    - **Artikelbemonstering**: selecteer een artikelbemonstering. Zie [Artikelbemonstering voor kwaliteitsbeheer](quality-item-sampling.md) voor meer informatie.
    - **Destructief**: schakel dit selectievakje in om aan te geven dat de testgroep de artikelen die worden getest, zal vernietigd.

1. Selecteer, terwijl de nieuwe rij nog steeds is geselecteerd, het tabblad **Algemeen** in het bovenste gedeelte van de pagina. Enkele instellingen voor de testgroep die is geselecteerd op het tabblad **Overzicht**, worden hier herhaald. Daarnaast kunt u de volgende velden instellen voor de groep:

    - **Voorraadbatchkenmerk bijwerken**: wanneer u deze optie hier instelt op *Ja*, wordt deze optie automatisch ingesteld op *Ja* voor elke nieuwe test die wordt toegevoegd aan de testgroep in het onderste gedeelte van de pagina.
    - **Batchbeschikking bijwerken**: wanneer u deze optie instelt op *Ja* en als het artikel dat wordt getest, een batchartikel is, wordt de batchbeschikking automatisch bijgewerkt met de waarde die is geselecteerd in het veld **Mislukte batchbeschikking voor kwaliteitsorder** of **Batchbeschikking voor kwaliteitsorder geslaagd**.
    - **Mislukte batchbeschikking voor kwaliteitsorder**: selecteer de batchbeschikkingscode die moet worden toegewezen wanneer een kwaliteitsorder die deze testgroep bevat, mislukt omdat deze het acceptabele kwaliteitsniveau niet heeft gehaald.
    - **Batchbeschikking voor kwaliteitsorder geslaagd**: selecteer de batchbeschikkingscode die moet worden toegewezen wanneer een kwaliteitsorder die deze testgroep bevat, slaagt omdat deze het acceptabele kwaliteitsniveau heeft gehaald.
    - **Voorraadstatus bijwerken**: als u deze optie instelt op *Ja* als **Voorraadstatus** is ingeschakeld in de opslagdimensiegroep voor het artikel dat wordt getest, wordt de status automatisch bijgewerkt met de status die is geselecteerd in het veld **Kwaliteitsorderstatus Mislukt** of **Kwaliteitsorderstatus Geslaagd**.
    - **Kwaliteitsorderstatus Mislukt**: selecteer de voorraadstatus die moet worden toegewezen aan het artikel wanneer een kwaliteitsorder die deze testgroep bevat, mislukt omdat deze het acceptabele kwaliteitsniveau niet heeft gehaald.
    - **Kwaliteitsorderstatus Geslaagd**: selecteer de voorraadstatus die moet worden toegewezen aan het artikel wanneer een kwaliteitsorder die deze testgroep bevat, slaagt omdat deze het acceptabele kwaliteitsniveau heeft gehaald.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Een kwalitatieve test toevoegen aan een testgroep

Volg deze stappen om een kwalitatieve test aan een testgroep toe te voegen.

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Testgroepen**.
1. Selecteer op het tabblad **Overzicht** in het bovenste gedeelte van de pagina de testgroep waar u een test aan wilt toevoegen.
1. Selecteer in het onderste gedeelte van de pagina op het tabblad **Overzicht** de optie **Toevoegen** op de werkbalk om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Volgnummer**: voer een geheel getal in om de volgorde op te geven waarin de tests moeten worden uitgevoerd. Testen met kleinere volgnummers worden uitgevoerd vóór tests met grotere volgnummers.

        > [!NOTE]
        > U wordt aangeraden steeds ruimte vrij te laten tussen de volgnummers. Stel bijvoorbeeld het veld **Volgnummer** in op *10* voor uw eerste test en verhoog de waarde vervolgens met 10 voor elke extra test. Op deze manier kunt u later nieuwe tests toevoegen zonder dat u regels hoeft te verwijderen en opnieuw te maken om de tests in de gewenste volgorde te plaatsen.

    - **Test**: selecteer de test die u wilt uitvoeren. Als u een kwalitatieve test wilt uitvoeren, selecteert u een test waarvan het veld **Type** ingesteld op *Optie*.
    - **Ingangsdatum**: selecteer de eerste datum waarop de test geldig is. Als u dit veld leeg laat, is er geen limiet.
    - **Vervaldatum**: selecteer de laatste datum waarop de test geldig is. Als u dit veld leeg laat of dit instelt op *Nooit*, is er geen limiet.
    - **Testwaarde bepalen**: geef op hoe een acceptabel kwaliteitsniveau moet worden bepaald wanneer er meerdere resultaten worden geregistreerd voor dezelfde test. Voor een kwalitatieve test kan alleen *Handmatig* worden geselecteerd. Als u een van de andere waarden selecteert (*Gemiddelde*, *Minimum* of *Maximum*), wordt er een foutbericht weergegeven wanneer u de testgroep opslaat.
    - **Kenmerk**: als u testresultaten wilt registreren in een batchkenmerk, selecteert u hier het kenmerk en schakelt u het selectievakje **Voorraadbatchkenmerk bijwerken** in.
    - **Voorraadbatchkenmerk bijwerken**: schakel dit selectievakje in om testresultaten te registreren voor het batchkenmerk dat is geselecteerd in het veld **Kenmerk**.

1. Selecteer in het onderste gedeelte van de pagina het tabblad **Algemeen**. Sommige instellingen voor de test die is geselecteerd op het tabblad **Overzicht**, worden hier herhaald. Daarnaast kunt u de volgende velden instellen voor de test:

    - **Analysecertificaatrapport**: stel deze optie in op *Ja* om aan te geven dat de testresultaten moeten worden afgedrukt op het analysecertificaat (CoA). Dit rapport kan worden gegenereerd op basis van de kwaliteitsorder.
    - **Actie bij fout**: selecteer *Accepteren* of *Afgekeurd* om aan te geven of de test moet slagen of mislukken als het acceptabele kwaliteitsniveau ervoor niet is gehaald.
    - **Acceptabel kwaliteitsniveau**: geef hier op hoeveel procent van de resultaten van een test in totaal goed moet zijn om de test te beschouwen als geslaagd.

1. Stel in het onderste deel van de pagina op het tabblad **Test** de volgende velden in:

    - **Variabele**: selecteer de testvariabele waarvoor de testresultaten voor de kwalitatieve test worden vastgelegd.
    - **Standaarduitkomst**: selecteer de standaarduitkomst die voor de testresultaten moet worden vastgelegd.
    - **Testinstrument**: selecteer het apparaat dat moet worden gebruikt voor de test. Als er een testinstrument is gedefinieerd, wordt dit automatisch ingevoerd voor de test in de testgroep.

1. Sluit de pagina.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Een kwantitatieve test toevoegen aan een testgroep

Volg deze stappen om een kwantitatieve test aan een testgroep toe te voegen.

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitsbeheer \> Testgroepen**.
1. Selecteer op het tabblad **Overzicht** in het bovenste gedeelte van de pagina de testgroep waar u een test aan wilt toevoegen.
1. Selecteer in het onderste gedeelte van de pagina op het tabblad **Overzicht** de optie **Toevoegen** op de werkbalk om een rij aan het raster toe te voegen. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Volgnummer**: voer een geheel getal in om de volgorde op te geven waarin de tests moeten worden uitgevoerd. Testen met kleinere volgnummers worden uitgevoerd vóór tests met grotere volgnummers.

        > [!NOTE]
        > U wordt aangeraden steeds ruimte vrij te laten tussen de volgnummers. Stel bijvoorbeeld het veld **Volgnummer** in op *10* voor uw eerste test en verhoog de waarde vervolgens met 10 voor elke extra test. Op deze manier kunt u later nieuwe tests toevoegen zonder dat u regels hoeft te verwijderen en opnieuw te maken om de tests in de gewenste volgorde te plaatsen.

    - **Test**: selecteer de test die u wilt uitvoeren. Als u een kwantitatieve test wilt uitvoeren, selecteert u een test waarvan het veld **Type** is ingesteld op *Breuk* of *Geheel getal*.
    - **Ingangsdatum**: selecteer de eerste datum waarop de test geldig is. Als u dit veld leeg laat, is er geen limiet.
    - **Vervaldatum**: selecteer de laatste datum waarop de test geldig is. Als u dit veld leeg laat of dit instelt op *Nooit*, is er geen limiet.
    - **Testwaarde bepalen**: geef op hoe een acceptabel kwaliteitsniveau moet worden bepaald wanneer er meerdere resultaten worden geregistreerd voor dezelfde test. De beschikbare opties zijn *Gemiddelde*, *Minimum*, *Maximum* en *Handmatig*.
    - **Kenmerk**: als u testresultaten wilt registreren in een batchkenmerk, selecteert u hier het kenmerk en schakelt u het selectievakje **Voorraadbatchkenmerk bijwerken** in.
    - **Voorraadbatchkenmerk bijwerken**: schakel dit selectievakje in om testresultaten te registreren voor het batchkenmerk dat is geselecteerd in het veld **Kenmerk**.

1. Selecteer in het onderste gedeelte van de pagina het tabblad **Algemeen**. Sommige instellingen voor de test die is geselecteerd op het tabblad **Overzicht**, worden hier herhaald. Daarnaast kunt u de volgende velden instellen voor de test:

    - **Analysecertificaatrapport**: stel deze optie in op *Ja* om aan te geven dat de testresultaten moeten worden afgedrukt op het analysecertificaat (CoA). Dit rapport kan worden gegenereerd op basis van de kwaliteitsorder.
    - **Actie bij fout**: selecteer *Accepteren* of *Afgekeurd* om aan te geven of de test moet slagen of mislukken als het acceptabele kwaliteitsniveau ervoor niet is gehaald.
    - **Acceptabel kwaliteitsniveau**: geef hier op hoeveel procent van de resultaten van een test in totaal goed moet zijn om de test te beschouwen als geslaagd.

1. Stel in het onderste deel van de pagina op het tabblad **Test** de volgende velden in:

    - **Standaard**: voer de hoeveelheid (geheel getal of breuk) in die wordt verwacht voor de testresultaten. De waarde die u invoert, wordt standaard ingevoerd in de testresultaten. Bovendien wordt deze waarde automatisch ingevoerd als een standaardwaarde in de velden **Min** en **Max**.
    - **Min**: voer de toegestane minimumwaarde voor de testresultaten in. De waarde die u invoert, moet lager zijn dan de hoeveelheid die in het veld **Standaard** is ingesteld. Wanneer u het veld **Min** bijwerkt, wordt het veld **Min. tolerantie (%)** automatisch bijgewerkt. En ook andersom wanneer u het veld **Min. tolerantie (%)** bijwerkt, wordt het veld **Min** automatisch bijgewerkt.
    - **Max**: voer de toegestane maximumwaarde voor de testresultaten in. De waarde die u invoert, moet hoger zijn dan de hoeveelheid die in het veld **Standaard** is ingesteld. Wanneer u het veld **Max** bijwerkt, wordt het veld **Max. tolerantie (%)** automatisch bijgewerkt. En ook andersom wanneer u het veld **Max. tolerantie (%)** bijwerkt, wordt het veld **Max** automatisch bijgewerkt.
    - **Testinstrument**: selecteer het apparaat dat moet worden gebruikt voor de test. Als er een testinstrument is gedefinieerd, wordt dit automatisch ingevoerd voor de test in de testgroep.

1. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Testinstrumenten voor kwaliteitsbeheer](quality-management-processes.md)
- [Kwaliteitsbeheertests](quality-management-processes.md)
- [Testvariabelen voor kwaliteitsbeheer](quality-management-processes.md)
- [Kwaliteitskoppelingen](quality-management-processes.md)
- [Batchkenmerken](../production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
