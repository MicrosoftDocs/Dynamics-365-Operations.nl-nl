---
title: Boekhoudprincipe voor boeken op toeslagrekening
description: Dit onderwerp biedt een overzicht van het boekhoudprincipe voor boeken op toeslagrekening.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45dc1775c0db83faa89a7a1fa799bdd070d1b09a
ms.sourcegitcommit: 283e237d7bd2a76dd3a8ff64685b0a5f146edd25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721393"
---
# <a name="post-to-charge-account-accounting-principle"></a>Boekhoudprincipe voor boeken op toeslagrekening

Met het boekhoudprincipe voor *boeken op toeslagrekening* kunt u eenvoudiger verschillen in de eenheidsprijs afstemmen tussen een fysieke boeking en een financiële boeking, indirecte kosten voor ingekochte artikelen of toeslagen op een inkooporder. 

Twee configuraties voor toeslagencodes voor Leveranciers op de pagina **Toeslagcode** (**Leveranciers \> Instelling van toeslagen \> Toeslagcode**) kunnen ertoe leiden dat een inkooporder van invloed is op de waardering van voorraadactiva:

- Voor toeslagcodes waarbij het veld **Debettype** is ingesteld op *Artikel* en het veld **Credittype** op *Grootboekrekening*, werkt de grootboekrekening die is geselecteerd als absorptierekening als een voorraadvariatierekening.
- Voor toeslagcodes waarbij het veld **Debettype** is ingesteld op *Artikel* en het veld **Credittype** op *Klant/leverancier*, wordt de toeslag als materiaalkosten verantwoord en wordt de voorraadvariatierekening van het artikel gebruikt.

## <a name="european-special-accounting-rule"></a>Speciale Europese boekhoudingsregel

In Europa wordt het boekhoudprincipe voor *boeking naar toeslagrekening* vaak gebruikt om een speciale regel voor de boekhouding op te nemen. Een van de volgende methoden wordt bijvoorbeeld meestal gebruikt om voorraadwijzigingen te verantwoorden:

- **Kosten van verkoop-methode**: deze methode wordt ondersteund door de configuratie van het standaardprofiel voor voorraadboeking. Het boekhoudprincipe *boeking naar toeslagrekening* is niet vereist.
- **Aard van onkosten-methode**: kleinere organisaties gebruiken deze methode vaak. Meestal gaat het om de volgende stappen:

    1. Kosten van goederen of services worden volledig opgevoerd op het moment van ontvangst.
    2. Aan het einde van de periode wordt een cyclustelling uitgevoerd.
    3. Een handmatige aanpassing voor de hoeveelheid en de waarde wordt geboekt in de voorraad. (De tegenrekening is een voorraadvariatierekening die de onkosten compenseert die in stap 1 zijn geboekt. Daarom ziet u het verschil in de voorraadwaarde alleen voor deze rekening.)

Met het principe voor *boeken naar toeslagrekening* kunt u de twee boekingen volledig automatiseren. Op deze manier kunt u een handmatige afsluitingscorrectie aan het einde van de periode verwijderen.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Boekhoudprincipe voor boeken op toeslagrekening inschakelen

Volg deze stappen om het boekhoudprincipe voor *boeken naar toeslagrekening* in te stellen.

1. Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.
2. Stel op het tabblad **Factuur** op het sneltabblad **Factuur** de optie **Boeken op toeslagrekening in grootboek** in op *Ja*.
3. Sluit de pagina.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Vereisten en aanbevolen parameters voor het boekhoudprincipe voor boeken op toeslagrekening

Als u van plan bent om inkoopkosten en voorraadverschillen te verantwoorden, moet aan de volgende vereisten voldoen:

- Op het tabblad **Factuur** van de pagina **Parameters van module Leveranciers** (**Leveranciers \> Instellen \> Parameters van module Leveranciers**), moet de optie **Boeken op toeslagrekening in grootboek** zijn ingesteld op *Ja*.
- Op de pagina **Artikelmodelgroepen** (**Kostenbeheer \> Instelling voor boekhoudingbeleid voorraad \> Artikelmodelgroepen**) moeten alle volgende opties worden ingesteld op *Ja* voor elke relevante modelgroep die artikelen bevat die in een inkooporder zijn opgenomen:

    - Fysieke voorraad boeken
    - Financiële voorraad boeken
    - Toerekening van aansprakelijkheid bij productontvangstbon

- Op het tabblad **Levering** van de pagina **Parameters voor inkoopbeheer** (**Inkoop en sourcing \> Instellen \> Parameters voor inkoopbeheer**) moet de optie **Toeslagen genereren op productontvangstbon** op *Ja* zijn ingesteld.
- Op het tabblad **Voorraadboekhouding** van de pagina **Parameters voor voorraad- en magazijnbeheer** (**Voorraadbeheer \> Instellen \> Parameters voor voorraad- en magazijnbeheer**) moet de optie **Pakbon in grootboek boeken** worden ingesteld op *Ja*.
- Op het tabblad **Inkooporder** van de pagina **Boeking** (**Voorraadbeheer \> Instellen \> Boeking \> Boeking**) moeten voor elk van de volgende boekingstypen hoofdrekeningen worden opgegeven die van toepassing zijn op elk relevant artikel:

    - Inkoopuitgave, niet-gefactureerd
    - Inkoopuitgave voor product
    - Voorraadwijziging

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Voorbeeldscenario 1: Kostprijs per eenheid wijzigen

Voor dit voorbeeldscenario gelden de volgende vereisten:

- FIFO-kostprijsmodel (First In, First Out)

In de volgende procedure vindt u een voorbeeld van wat er gebeurt wanneer u de kostprijs per eenheid op een inkooporder wijzigt.

1. Maak een inkooporder voor een hoeveelheid van 1 voor een artikel met een eenheidsprijs van 100,00.
2. Bevestig de inkooporder.
3. Boek de productontvangstbon voor de inkooporder.
4. Valideer het boekstuk op de productontvangstbon. In de volgende tabel ziet u een voorbeeldboekstuk.

    | Boekingstype | Hoofdrekening | Naam hoofdrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Fysiek/financieel? | Bedrag |
    |---|---|---|---|---|---|---|---|
    | Inkoop, voorraadwijziging | 600170 | Materialen voorraadwijziging | Onkosten | Credit | Nr. | Fysiek | -100,00 |
    | Kosten van ingekocht ontvangen materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Ja | Fysiek | 100.00 |
    | Inkoopuitgave, niet-gefactureerd | 600180 | Materiaalontvangstbonnen | Onkosten | Debet | Ja | Fysiek | 100.00 |
    | Inkoop, toerekening | 200140 | Transitorische aankopen | Aansprakelijkheid | Credit | Ja | Fysiek | -100,00 |

5. De factuur voor de inkooporder met een bijgewerkte eenheidsprijs van 110,00.
6. Valideer het boekstuk op de factuur. In de volgende tabel ziet u een voorbeeldboekstuk.

    | Boekingstype | Hoofdrekening | Naam hoofdrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Fysiek/financieel? | Bedrag |
    |---|---|---|---|---|---|---|---|
    | Inkoop, voorraadwijziging | 600170 | Materialen voorraadwijziging | Onkosten | Credit | Nr. | Financieel | -10.00 |
    | Kosten van ingekocht ontvangen materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Ja | Financieel | -100,00 |
    | Inkoopuitgave, niet-gefactureerd | 600180 | Materiaalontvangstbonnen | Onkosten | Debet | Ja | Financieel | -100,00 |
    | Inkoop, toerekening | 200140 | Transitorische aankopen | Aansprakelijkheid | Credit | Ja | Financieel | 100.00 |
    | Kosten van ingekocht gefactureerd materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Nr. | Financieel | 110.00 |
    | Inkoopuitgave voor product | 600180 | Materiaalontvangstbon | Onkosten | Credit | Nr. | Financieel | 110.00 |
    | Leveranciersaldo | 211000 | Handelsrekening voor Leveranciers | Aansprakelijkheid | Credit | Nr. | Financieel | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Voorbeeld 2: toeslagen en indirecte kosten op de inkooporder

Voor dit voorbeeldscenario gelden de volgende vereisten:

- FIFO-kostprijsmodel
- **Toeslagencode 1:** Debet artikel en credit grootboekrekening voor 10%
- **Toeslagencode 2:** Debet artikel en credit klant/leverancier met proportioneel 10,00
- **Indirecte kosten:** 2,00% opgeteld bij de inkoopprijs

In de volgende procedure vindt u een voorbeeld van wat er gebeurt wanneer u toeslagen en indirecte kosten op een inkooporder opneemt.

1. Maak een inkooporder voor een hoeveelheid van 1 voor een artikel met een eenheidsprijs van 100,00.
2. Voeg één toeslagencode toe voor 10 procent waardoor het artikel wordt gedebiteerd en het grootboek wordt gecrediteerd.
3. Voeg één toeslagencode toe voor 10,00 waardoor het artikel wordt gedebiteerd en de klant/leverancier wordt gecrediteerd.
4. Wijs de toeslagen toe aan inkooporderregels.
5. Bevestig de inkooporder.
6. Boek de productontvangstbon voor de inkooporder.
7. Valideer het boekstuk op de productontvangstbon. In de volgende tabel ziet u een voorbeeldboekstuk.

    | Boekingstype | Hoofdrekening | Naam hoofdrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Fysiek of financieel | Bedrag |
    |---|---|---|---|---|---|---|---|
    | Inkoop, voorraadwijziging | 600170 | Materialen voorraadwijziging | Onkosten | Credit | Nr. | Fysiek | -110,00 |
    | Geraamde indirect geabsorbeerde kosten | 600520 | Geabsorbeerde indirecte kosten | Onkosten | Credit | Ja | Fysiek | -2,40 |
    | Inkoopvracht | 600120 | Vracht-/transportkosten | Onkosten | Credit | Nr. | Fysiek | -10.00 |
    | Kosten van ingekocht ontvangen materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Ja | Fysiek | 122.40 |
    | Inkoopuitgave, niet-gefactureerd | 600180 | Materiaalontvangstbonnen | Onkosten | Debet | Ja | Fysiek | 110.00 |
    | Inkoop, toerekening | 200140 | Transitorische aankopen | Aansprakelijkheid | Credit | Ja | Fysiek | -110,00 |

8. Boek de factuur voor de inkooporder.
9. Valideer het boekstuk op de factuur. In de volgende tabel ziet u een voorbeeldboekstuk.

    | Boekingstype | Hoofdrekening | Naam hoofdrekening | Rekeningtype | Debet/Credit? | Vereffeningsrekening | Fysiek/financieel? | Bedrag |
    |---|---|---|---|---|---|---|---|
    | Inkoop, voorraadwijziging | 600170 | Materialen voorraadwijziging | Onkosten | Credit | Nr. | Financieel | 0,00 |
    | Geraamde indirect geabsorbeerde kosten | 600520 | Geabsorbeerde indirecte kosten | Onkosten | Debet | Ja | Financieel | 2.40 |
    | Indirect geabsorbeerde kosten | 600520 | Geabsorbeerde indirecte kosten | Onkosten | Debet | Nr. | Financieel | -2,40 |
    | Kosten van ingekocht ontvangen materiaal | 140100 | Materiaalvoorraad | Activum | Credit | Ja | Financieel | -110,00 |
    | Inkoopuitgave, niet-gefactureerd | 600180 | Materiaalontvangstbonnen | Onkosten | Credit | Ja | Financieel | -110,00 |
    | Inkoop, toerekening | 200140 | Transitorische aankopen | Aansprakelijkheid | Debet | Ja | Financieel | 110.00 |
    | Kosten van ingekocht gefactureerd materiaal | 140100 | Materiaalvoorraad | Activum | Debet | Nr. | Financieel | 110.00 |
    | Inkoopuitgave voor product | 600180 | Materiaalontvangstbon | Onkosten | Credit | Nr. | Financieel | 110.00 |
    | Leveranciersaldo | 211000 | Handelsrekening voor Leveranciers | Aansprakelijkheid | Credit | Nr. | Financieel | -110,00 |
