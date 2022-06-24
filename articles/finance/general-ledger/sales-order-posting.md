---
title: Verkooporders boeken
description: Dit artikel biedt informatie over het tabblad Verkooporder van de voorraadboekingsprofielpagina.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886308"
---
# <a name="sales-order-posting"></a>Verkooporders boeken

Het tabblad **Verkooporder** op de pagina **Voorraadboekingsprofielen** wordt gebruikt om te bepalen hoe verkooporders naar het grootboek worden geboekt. Twee hoofdactiviteiten worden voor een verkooporder naar het grootboek geboekt: 

- Pakbon
- Factuur

Als u een fysieke transactie (pakbon) wilt boeken in het grootboek voor een verkooporder, moet er aan de volgende voorwaarden zijn voldaan:

- Op de pagina **Parameters van voorraad- en magazijnbeheer** moet het selectievakje **Pakbon in grootboek boeken** worden geselecteerd.
- Op de pagina **Artikelmodelgroep** voor het artikel dat is geselecteerd op de verkooporderregel, moet het selectievakje **Fysieke voorraad in het grootboek boeken** zijn ingeschakeld.
- Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
  - Kosten van eenheden, geleverd
  - Kosten van verkochte goederen, geleverd

Als u een financiële transactie (factuur) wilt boeken in het grootboek voor een verkooporder, moet er aan de volgende voorwaarden zijn voldaan:

- Op de pagina **Artikelmodelgroep** voor het artikel dat is geselecteerd op de verkooporderregel, moet het selectievakje **Financiële voorraad in het grootboek boeken** zijn ingeschakeld.
- Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
  - Kosten van eenheden, gefactureerd
  - Kosten van verkochte goederen, gefactureerd
  - Omzet
  - Korting\*

> [!NOTE]
> De kortingsrekening is optioneel. Veel boekhoudregels, zoals GAAP en IFRS, vereisen dat kortingen de verkoopopbrengsten verlagen en daarom worden deze rekeningen niet in veel scenario's gebruikt. Als de lokale regelgeving dat toestaat, gebruikt u een afzonderlijke hoofdrekening om het deel van de verkoopprijs te boeken waarop korting van toepassing is.

Als u de uitgestelde (geschatte) opbrengstwaarde naar het grootboek wilt boeken wanneer u een pakbon voor een verkooporder genereert, moet er aan de volgende voorwaarden worden voldaan:

- Op de pagina **Artikelmodelgroep** voor het artikel dat is geselecteerd op de verkooporderregel, moet het selectievakje **Fysieke voorraad in het grootboek boeken** zijn ingeschakeld.
- Op de pagina **Artikelmodelgroep** moet het selectievakje **Boeken op rekening voor uitgestelde opbrengst bij levering** zijn ingeschakeld.
- Op de pagina **Parameters van voorraad- en magazijnbeheer** moet het selectievakje **Pakbon in grootboek boeken** worden geselecteerd.
- Op de pagina **Parameters van voorraad- en magazijnbeheer** moet het selectievakje **Fysieke btw boeken** worden geselecteerd.
- Op de pagina **Parameters van module Klanten** moet het selectievakje **Pakbon in grootboek boeken** worden geselecteerd.
- Op de pagina **Voorraadboekingsprofiel** moeten de hoofdrekeningen worden opgegeven voor de volgende boekingstypen:
  - Uitgestelde opbrengst bij levering
  - Tegenrekening uitgestelde opbrengst bij levering
  - Uitgestelde btw bij levering

> [!NOTE]
> We raden u in het algemeen aan om de opties **Fysieke voorraad boeken** en **Pakbon in grootboek boeken** te selecteren. Als u deze opties inschakelt, kunt u de procedures voor het afsluiten van een maand versnellen, omdat er geen vertragingen meer nodig zijn om handmatig te worden berekend en geboekt. Bovendien worden in financiële overzichten de uitgestelde bedragen automatisch weergegeven zonder handmatige tussenkomst.

> [!IMPORTANT]
> De optie **Boeken op rekening voor uitgestelde opbrengst bij levering** wordt niet gebruikt met opbrengsttoerekening. Ga naar [Overzicht van opbrengsttoerekening](/accounts-receivable/revenue-recognition-overview.md) voor meer informatie over opbrengsttoerekening.

## <a name="sample-posting-profile-configuration"></a>Voorbeeldconfiguratie van boekingsprofiel 

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen:
 
- De kolom **Vereffeningsrekening** geeft aan of het boekingstype een vereffeningsrekening is. Het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt. 
- In de kolom **P/F** verwijst **P** naar fysieke boeking en **F** naar financiële boeking. 
- De kolom **Volgen** geeft aan of de hoofdrekening voor een bepaald boekingstype gewoonlijk hetzelfde is als een ander boekingstype. De waarde in de kolom geeft het type boeking aan dat normaal gesproken wordt gebruikt.

> [!NOTE]
> Deze hoofdrekeningen en hoofdrekeningnamen zijn alleen suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.


| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Kosten van eenheden, geleverd | 140100</br>140101 | Materiaalvoorraad</br>Materiaal verzonden niet gefactureerd | Activum | Credit | Ja | W | Kosten van eenheden, gefactureerd | Wordt gebruikt wanneer een pakbon van een verkooporder wordt geboekt. De verschuiving op de rekening betreft de kosten van de verkochte goederen, geleverd. Het bedrag dat op deze rekening wordt geboekt, wordt teruggeboekt wanneer een factuur voor een verkooporder wordt geboekt. U wilt misschien een rekening Materiaal verzonden niet gefactureerd gebruiken om de fysieke voorraad weer te geven en de rekening Materiaalvoorraad reserveren voor de financiële update. |
| Kosten van verkochte goederen, geleverd | 500150 | Uitgestelde COGS | Onkosten | Debet | Ja | W  | Wordt gebruikt wanneer een pakbon van een verkooporder wordt geboekt. De verschuiving op de rekening betreft de kosten van de eenheden, geleverd. Het bedrag dat op deze rekening wordt geboekt, wordt teruggeboekt wanneer een factuur voor een verkooporder wordt geboekt. |
| Kosten van eenheden, gefactureerd | 140100 | Materiaalvoorraad | Activum | Credit | Nr. | Vr | Kosten van eenheden, geleverd | Wordt gebruikt wanneer een factuur van een verkooporder wordt geboekt. De verschuiving op deze rekening betreft de kosten van de verkochte goederen, gefactureerd. Deze rekening vertegenwoordigt de voorraad op uw balans. |
| Kosten van verkochte goederen, gefactureerd | 500100 | COGS materialen | Onkosten | Debet | Nr. | Vr  | Wordt gebruikt wanneer een factuur van een verkooporder wordt geboekt. De verschuiving op deze rekening betreft de kosten van eenheden, gefactureerd. Deze rekening vertegenwoordigt de COGS op uw winst-en-verliesoverzicht. |
| Opbrengst (verkooporderopbrengst*) | 400100 | Opbrengst materialen | Omzet | Credit | Nr. | Vr   | Wordt gebruikt wanneer een factuur van een verkooporder wordt geboekt. De tegenrekening voor deze rekening is de overzichtsrekening (Klantsaldo*) op het **Klantboekingsprofiel**. |
| Commissie (verkoop, commissie*) | 602150 | Commissie-uitgaven | Onkosten | Debet | Nr. | Vr  | Deze wordt gebruikt wanneer commissie wordt ingeschakeld en berekend voor een verkoop en wordt geboekt tijdens het verkooporderfactuurproces. De verschuiving op deze rekening is de verschuldigde provisie. |
| Commissieverschil (verkoop, commissieverschil*) | 201110 | Te betalen provisie | Aansprakelijkheid | Credit | Ja | Vr | Deze wordt gebruikt wanneer commissie wordt ingeschakeld en berekend voor een verkoop en wordt geboekt tijdens het verkooporderfactuurproces. De verschuiving op deze rekening zijn de provisiekosten. |
| Uitgestelde opbrengst bij levering (Verkoop – pakbonopbrengst*) | 401400 | Transitorische verkoop | Omzet | Credit | Ja | W  | Wordt gebruikt wanneer uitgestelde opbrengst voor levering is ingeschakeld en wordt geboekt wanneer u een pakbon van een verkooporder verwerkt. De verschuiving op deze rekening is het uitgestelde opbrengstverschil. De bedragen op deze rekening worden automatisch omgekeerd wanneer u de verkooporderfactuur maakt. |
| Uitgesteld opbrengstverschil bij levering (Verkoop – pakbonopbrengstverschil)* | 130400 | Klanten – niet gefactureerd | Activum | Debet | Ja | W  | Wordt gebruikt wanneer uitgestelde opbrengst voor levering is ingeschakeld en wordt geboekt wanneer u een pakbon van een verkooporder verwerkt. De verschuiving op deze rekening is de uitgestelde opbrengst bij levering. De bedragen op deze rekening worden automatisch omgekeerd wanneer u de verkooporderfactuur maakt. |
| Uitgestelde btw bij levering (Verkoop, pakbon-btw*) | 250500 | Uitgestelde btw | Aansprakelijkheid | Credit | Ja | W  | Dit wordt gebruikt wanneer Uitgestelde opbrengst bij levering en Fysieke btw boeken zijn ingeschakeld. Het btw-bedrag wordt geboekt wanneer u een pakbon van een verkooporder verwerkt. |

\*Waarden die tussen haakjes in deze tabel worden weergegeven, staan voor de waarde die wordt gebruikt in het veld **Boekingstype** op de pagina **Boekstuktransacties**. U kunt het **boekingstype** bekijken op de pagina **Boekstuktransacties** op het tabblad **Algemeen**.

## <a name="sales-category-posting"></a>Verkoopcategorie boeken

In plaats van het instellen van de voorraadboeking voor alle artikelen, een groep artikelen of een enkel artikel, kunt u categorieën instellen en de boeking in het grootboek beheren per verkoopcategorie. Als u meer informatie wilt over het instellen van een categoriehiërarchie en het toewijzen van categorieën aan producten, gaat u naar [Een hiërarchie van productclassificatie maken](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) en [Een product classificeren met categoriehiërarchieën](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Nadat u een categoriehiërarchie hebt gemaakt, moet u de hiërarchie aan een of meer typen toewijzen. Als u een categoriehiërarchie op verkooporders wilt gebruiken, moet u de categorie toewijzen aan het type Verkoopcategoriehiërarchie. Zie voor meer informatie [Over categoriehiërarchieën](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Opbrengstboekingen maken op verkoopcategorie

Als u grootboekboekingen wilt toewijzen voor een verkooporder op basis van een verkoopcategorie, gaat u als volgt te werk:

1. Ga naar **Voorraadbeheer** > **Instellen** > **Boeken** > **Boeken**.
2. Selecteer het tabblad **Verkoop**.
3. Selecteer het keuzerondje voor het boekingstype dat u wilt configureren (bijvoorbeeld **Opbrengst**).
4. Selecteer **Nieuw**.
5. Selecteer **Categorie** in het veld **Artikelcode**.
6. Gebruik het veld **Categorierelatie** om de categorie voor het boekingsprofiel te selecteren.
7. Selecteer in het veld **Rekeningcode** een optie voor **Tabel**, **Groep** of **Alle**. Als u bijvoorbeeld het boekingsprofiel wilt toepassen op alle klanten, selecteert u **Alle**.
   - Als u **Tabel** hebt geselecteerd bij stap 6, selecteert u het specifieke **leveranciernummer** voor het boekingsprofiel in het veld **Rekeningrelatie**.
   - Als u **Groep** hebt geselecteerd bij stap 6, selecteert u de **leveranciergroep** voor het boekingsprofiel in het veld **Rekeningrelatie**.
   - Als u **Alle** hebt geselecteerd bij stap 6, blijft het veld **Rekeningrelatie** leeg.

8. Als u een bepaalde btw-groep met het geselecteerde boekingstype wilt koppelen, selecteert u een **btw-groep**. Als u dit veld leeg laat, is het boekingstype van toepassing op alle bestaande btw-groepen. Boekingen die zijn opgegeven voor belastinggroepen, zijn alleen van toepassing op verkoop- en inkooptransacties.

9. Geef in het veld **Hoofdrekening** het rekeningnummer op waarnaar u het rekeningtype wilt boeken. Selecteer een van de bestaande rekeningnummers in het rekeningschema.
