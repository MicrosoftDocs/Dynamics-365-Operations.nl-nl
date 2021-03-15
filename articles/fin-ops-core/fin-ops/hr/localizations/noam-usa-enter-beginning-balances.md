---
title: Beginsaldi voor salarisadministratie invoeren
description: In dit onderwerp worden de stappen beschreven voor het invoeren van de beginsaldi voor inkomstencodes, inhoudingen, vergoedingen en belastingen. Deze informatie is nuttig wanneer partners gegevens voor een nieuwe salarisadministratie-implementatie willen migreren of overbrengen vanuit een ander systeem.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8443bc5c63a90d80757ab4b7507502497c2aaa69
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797779"
---
# <a name="enter-payroll-beginning-balances"></a>Beginsaldi voor salarisadministratie invoeren

[!include [banner](../../includes/banner.md)]

In dit onderwerp worden de stappen beschreven voor het invoeren van de beginsaldi voor inkomstencodes, inhoudingen, vergoedingen en belastingen. Deze informatie is nuttig voor partners die gegevens voor een nieuwe salarisadministratie-implementatie willen migreren of overbrengen vanuit een ander systeem. Als voorbereiding voor het invoeren van beginsaldi controleren we de volgende informatie:

- Werknemersrecords zijn ingevoerd en beschikbaar in het systeem
- De volgende gegevens zijn ingesteld en toegewezen aan werknemers:

    - Betalingscycli en salarisperioden
    - Inkomstencodes
    - Belastingen
    - Vergoedingen en aftrekposten

- Het bedrijf moet een datum hebben gekozen waarop de beginsaldi kunnen worden ingesteld.
- Gegevens zijn verzameld voor alle inkomsten, vergoedingen/inhoudingen, vergoedingsbijdragen, werknemersbelastingen en werkgeverbelastingen en de betreffende JTH-bedragen in het oude systeem.

Bedenk bij het plannen van de invoer van beginsaldi hoe gedetailleerd de gegevens moeten zijn. De meeste bedrijven voeren een enkel, geconsolideerd bedrag voor JTH in. Als u meer gedetailleerde informatie nodig hebt, kunt u echter saldi invoeren in kwartaalstappen. Door te bepalen welk detailniveau nodig is, bepaalt u hoeveel handmatige salarisoverzichten u moet aanmaken voor elke werknemer. Voor een enkel JTH-bedrag is slechts één handmatig overzicht nodig voor elke werknemer. Hiervoor neemt u de JTH-bedragen van de laatste salarisoverzichten uit het oude systeem en voert u deze in als beginbedrag in de nieuwe salarisadministratie.

In het volgende voorbeeld ziet hoe u beginsaldi voor de werknemersalarissen kunt invoeren, inclusief inkomstencodes, vergoedingen/inhoudingen en belastingen. In de praktijk zou u een regelitem hebben voor elke inkomstencode, vergoedingsinhouding, vergoedingsbijdrage, werknemersbelasting en werkgeverbelasting, waarbij telkens het JTH-bedrag voor elk item wordt ingevoerd. Met deze lijst van codes en bedragen volgt u de stappen voor het maken van een handmatig inkomsten- en salarisoverzicht, met boekhouding uitgeschakeld, om de beginsaldi voor de salarisadministratie over te brengen. U schakelt hierbij de boekhouding uit, omdat u niet deze salarisbeginsaldi in uw grootboek wilt boeken. Dat is gedaan in het oude systeem en dit wordt naar het nieuwe systeem overgezet wanneer u de beginsaldi in het grootboek instelt.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Inkomstencodes instellen die worden gebruikt in de salarisbeginsaldi

Wanneer u salarisbeginsaldi invoert, let er dan op dat voor de gebruikte inkomstencodes de optie 'Bewerken van inkomstenoverzichttarieven toestaan' is ingeschakeld. Hierdoor kunt u handmatig het bedrag van het oude systeem intoetsen. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Inkomstenoverzichten maken met een beginsaldo voor een werknemer

In deze stap maakt u handmatig een inkomstenoverzicht aan voor elke werknemer voor de laatste periode van het oude systeem, waarmee u de inkomstenoverzichtsregels in de nieuwe salarisadministratie aanmaakt. Voeg één regel in per inkomstencode en het JTH-bedrag en -uren. De stappen met de demodata gaan als volgt:

1. Open de pagina **Alle inkomstenoverzichten** en klik op **Nieuw**.

    Voer de volgende gegevens in: 

    | Veld      | Waarde                 |
    |------------|-----------------------|
    | Medewerker     | Michael Redmond       |
    | Betalingscyclus  | SM                    |
    | Salarisperiode | 16-6-2017 - 30-6-2017 |

2. Voer op het tabblad **Inkomstenoverzichtregel** de volgende waarden in:

    Regel 1: tabblad **Inkomstenoverzichtregel**

    | Veld            | Waarde       |
    |------------------|-------------|
    | Inkomstencode    | Normaal salaris |
    | Hoeveelheid         | 1.00        |
    | Tarief             | 30,000      |
    | Tabblad Regeldetails |             |
    | Handmatig           | (gemarkeerd)    |

    Regel 2: tabblad **Inkomstenoverzichtregel**

    | Veld            | Waarde    |
    |------------------|----------|
    | Inkomstencode    | Bonus    |
    | Hoeveelheid         | 1.0000   |
    | Tarief             | 4250.00  |
    | Tabblad Regeldetails |          |
    | Handmatig           | (gemarkeerd) |

    Regel 3: tabblad **Inkomstenoverzichtregel**

    | Veld           | Waarde      |
    |-----------------|------------|
    | Inkomstencode   | Provisie |
    | Hoeveelheid        | 1.0000     |
    | Tarief            | 1.299,00   |
    | Tarief            | 1,299.00   |
    | Tabblad Regeldetails |            |
    | Handmatig          | (gemarkeerd)   |

    > [!NOTE]
    > Stel de schuifregelaar **Handmatig** op **Ja** in voor elke inkomstenoverzichtregel op het tabblad **Regeldetails** om salarisbeginsaldi te kunnen instellen voor elke medewerker.

3. Klik in het **actie** venster op **Inkomstenoverzicht vrijgeven** USA-FED-ER-FICA.
4. Klik in het **actie** venster op **Salarisoverzicht** om de pagina **Salarisoverzichten genereren** te openen en stel het volgende in:

    | Veld              | Waarde     |
    |--------------------|-----------|
    | Betalingsdatum       | 6/30/2017 |
    | Type betalingsronde   | Handmatig    |
    | Boekhouding uitschakelen |   Ja     |

    > [!NOTE] 
    > Dit is alleen beschikbaar wanneer het type van de betalingsronde handmatig is en als de gebruiker de boekhouding op de betalingsronde wil uitschakelen.

    Klik op **OK** en sluit het **Infologboek**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Waarom moet het selectievakje Boekhouding uitschakelen zijn ingesteld op Ja bij het genereren van salarisoverzichten?

Als u de schuifregelaar op **Ja** instelt, voorkomt u dat regels in het salarisoverzicht wordt gedistribueerd naar het grootboek. Grootboekbedragen worden eerder bijgewerkt wanneer de rekeningsaldi van het oude systeem zijn ingevoerd. Als u beginsaldi invoert voor salarissen, kunt u rapporten genereren die informatie uit eerdere jaren bevatten, alsmede limieten aangeven voor vergoedings- en belastingdoeleinden.

### <a name="c-create-pay-statements-for-employees"></a>C. Salarisoverzichten voor werknemers genereren

Na het genereren van salarisoverzichten met beginsaldi moet u controleren dat de salarisoverzichten de salarisgegevens correct weergeven. U moet ook handmatig de gegevens voor vergoedingen en belastingen bijwerken, zodat deze overeenkomen met de gegevens in de oude salarisadministratie. Nadat u hebt gecontroleerd of de bedragen uit de vorige salarisadministratie overeenkomen met de bedragen in de huidige salarisoverzichten, moet u de salarisoverzichten voltooien.

1. Open de pagina **Alle salarisoverzichten**.
2. Selecteer het laatst gegenereerde salarisoverzicht voor Michael Redmond.
3. Klik op **Bewerken** om de pagina **Salarisoverzicht** te openen.
4. Ga naar het tabblad **Vergoedingsinhoudingen** en voer de volgende waarden in:

    | Veld             | Waarde            |
    |-------------------|------------------|
    | Vergoeding           | Inhoudingsbedrag |
    | 401K              | Deelnemen      |
    | Tandartsverzekering            | SubSp            |
    | Uitgaven zorg afh. | Deelnemen      |
    | Zicht            | SupSp            |

5. Voer op het tabblad **Vergoedingsbijdragen** de volgende waarden in:

    | Veld   | Waarde               |
    |---------|---------------------|
    | Vergoeding | Bijdragebedrag |
    | 401K    | Deelnemen         |
    | Tandartsverzekering  | SubSp               |
    | Zicht  | SubSp               |

6. Voer op het tabblad **Belastinginhoudingen** de volgende waarden in:

    | Veld           | Waarde            |
    |-----------------|------------------|
    | Btw-code        | Inhoudingsbedrag |
    | USA-FED-ER-FICA | 1600.00          |
    | USA-FED-ER-MEDI | 825.75           |

7. Voer op het tabblad **Belastingbijdragen** de volgende waarden in:
8. Klik op **Berekenen**.

    > [!IMPORTANT] 
    > Valideer of de totaalbedragen van het salarisoverzicht overeenkomen met JTH-bedragen van het oude systeem voor de werknemer. U kunt het definitief maken in de volgende stap uitstellen en een validatie uitvoeren voor het totaal van alle salarisoverzichten. Na de validatie werkt u alle salarisoverzichten door en maakt u deze definitief.

Indien nodig kunt u hetzelfde proces uitvoeren per kwartaal voor alle voorgaande kwartalen in elk jaar. Dit is alleen nodig als de klant de gegevens per kwartaal moet zien, zonder terug te hoeven gaan naar het oude systeem.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Als u een fout maakt bij het invoeren van beginsaldi voor een werknemer

U kunt transacties ongedaan maken en opnieuw invoeren. Als u een transactie ongedaan wilt maken, hoeft u alleen maar de volgende stappen uit te voeren op de pagina **Alle salarisoverzichten**.

1. Klik op **Omkeren**.
2. Klik op **Ja** als het bericht "Als u dit salarisoverzicht omkeert, wordt een omgekeerd salarisoverzicht gemaakt als tegenboeking voor dit salarisoverzicht. Geen van beide salarisoverzichten kan worden bewerkt. Wilt u dit salarisoverzicht omkeren? wordt getoond. 

Na het omkeren van het salarisoverzicht kunt u een nieuw salarisoverzicht genereren voor de werknemer uit het inkomstenoverzicht dat u eerder hebt gemaakt. Zorg ervoor dat u onjuiste regels uit het inkomstenoverzicht corrigeert voordat u het nieuwe salarisoverzicht genereert en genereer vervolgens nieuwe salarisoverzichten met de juiste bedragen. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]