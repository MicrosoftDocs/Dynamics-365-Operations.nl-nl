---
title: Intercompany-parameters
description: In dit artikel komen de intercompany-parameters aan de orde
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7a9b921c7db47fe99981438932e5587f9a18f018
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850520"
---
# <a name="intercompany-parameters"></a>Intercompany-parameters

[!include [banner](../../includes/banner.md)]

In een intercompany-organisatie kunt u parameters instellen die bepalen hoe tussen verschillende bedrijven moet worden gehandeld. Deze parameters worden bepaald door de velden die u selecteert. U kunt verschillende combinaties selecteren om de verschillende handelsscenario's aan te geven.

In de volgende twee voorbeelden worden scenario's beschreven voor intercompany-organisaties, één met twee niveaus en één met drie niveaus.

## <a name="example-1-two-level-intercompany-chain"></a>Voorbeeld 1: intercompany-keten met twee niveaus

De intercompany-organisatie heeft de volgende rechtspersonen:

- Rechtspersoon A – Verkoopt aan externe klanten maar heeft geen voorraad. Deze rechtspersoon koopt van rechtspersoon B.
- Rechtspersoon B – Verkoopt alleen aan rechtspersoon A.

Beide rechtspersonen kunnen aan elkaar verkopen en van elkaar kopen.

In dit voorbeeld is de prijs van de originele verkooporder (voor de externe klant) altijd gebaseerd op de verkoopprijs. De prijzen van de intercompany-verkooporder en de intercompany-inkooporder worden bepaald door de interne verkoop- of overboekingsprijzen van de intercompany-verkooporder in rechtspersoon B.

De gegevens van de orderkoptekst worden bepaald door de originele verkooporder naar de externe klant. Elke wijziging in de intercompany-verkooporder wordt niet gesynchroniseerd in de originele verkooporder.

Selecteer in rechtspersoon A op de pagina **Intercompany** voor leveranciers de optie **Inkooporderbeleid**. Selecteer in de veldgroep **Oorspronkelijke verkooporder (rechtstreekse levering)** de volgende velden:

- **Pakbon automatisch afdrukken**
- **Factuur automatisch boeken**
- **Factuur automatisch afdrukken**

Selecteer in de veldgroep **Intercompany-inkooporder (rechtstreekse levering)** het volgende veld:

- **Factuur automatisch boeken**

Selecteer in de veldgroep **Oorspronkelijke verkooporder <-> Intercompany-inkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**

Selecteer in de veldgroep **Intercompany-inkooporder <-> Intercompany-verkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Selecteer in rechtspersoon B op de pagina **Intercompany** voor leveranciers de optie **Verkooporderbeleid**. Selecteer in de veldgroep **Intercompany-verkooporder maken** de volgende velden:

- **Verkoopordernummering**: **Bedrijf + origineel nummer**
- **Overzichtsupdate van documenten voor oorspronkelijke klant toestaan**

Selecteer in de veldgroep **Intercompany-verkooporderprijzen** de volgende velden:

- **Prijs en korting zoeken**
- **Bewerking van prijs toestaan**
- **Bewerking van korting toestaan**

Selecteer in de veldgroep **Intercompany-verkooporder \> Intercompany-inkooporder** de volgende velden:

- **Batchnummer**
- **Serienummer**

## <a name="example-2-three-level-intercompany-chain"></a>Voorbeeld 2: intercompany-keten met drie niveaus

De intercompany-organisatie heeft de volgende rechtspersonen:

- Rechtspersoon A – Een verkopend rechtspersoon die verkoopt aan externe klanten en koopt van rechtspersoon B.
- Rechtspersoon B – Een producerend of distribuerend rechtspersoon die geen producten kan leveren en koopt van rechtspersoon C.
- Rechtspersoon C – Een producerend of distribuerend rechtspersoon die producten levert aan rechtspersoon B.

Interne overboekingsprijzen tussen rechtspersonen B en C komen voor rekening van de verkopende rechtspersoon aan het begin van de keten. Ze zijn ook voor rekening van rechtspersoon A, die aan externe klanten verkoopt. De prijzen van de originele verkooporder voor de externe klant zijn echter altijd gebaseerd op de verkoopprijs.

De prijzen van de intercompany-verkooporder en de intercompany-inkooporder worden bepaald door de intercompany-verkooporder. Dit wordt aan het begin van de keten geregeld. Dat wil zeggen dat rechtspersoon C, die aan rechtspersoon B verkoopt, de prijs bepaalt. De prijzen van de intercompany-verkooporder zijn gebaseerd op de interne verkoop- of overboekingsprijs die in rechtspersoon C is ingesteld.

De gegevens van de orderkoptekst worden bepaald door de originele verkooporder naar de externe klant. Elke wijziging in de intercompany-ordera worden niet gesynchroniseerd in de originele verkooporder.

De volgende parameters moeten zijn geselecteerd:

Selecteer in rechtspersoon A op de pagina **Intercompany** voor leveranciers de optie **Inkooporderbeleid**. Selecteer in de veldgroep **Oorspronkelijke verkooporder (rechtstreekse levering)** de volgende velden:

- **Pakbon automatisch afdrukken**
- **Factuur automatisch boeken**
- **Factuur automatisch afdrukken**

Selecteer in de veldgroep **Intercompany-inkooporder (rechtstreekse levering)** het volgende veld:

- **Factuur automatisch boeken**

Selecteer in de veldgroep **Oorspronkelijke verkooporder <-> Intercompany-inkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**

Selecteer in de veldgroep **Intercompany-inkooporder <-> Intercompany-verkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Selecteer in rechtspersoon B op de pagina **Intercompany** voor leveranciers de optie **Verkooporderbeleid**. Selecteer in de veldgroep **Intercompany-verkooporder maken** de volgende velden:

- **Verkoopordernummering**: **Bedrijf + origineel nummer**
- **Overzichtsupdate van documenten voor oorspronkelijke klant toestaan**

Selecteer in de veldgroep **Intercompany-verkooporder \> Intercompany-inkooporder** de volgende velden:

- **Batchnummer**
- **Serienummer**

Selecteer in de veldgroep **Intercompany-klantfactuurboeking** de volgende velden:

- **Eenheidsprijs gelijk aan kostprijs**
- **Boeken van de oorspronkelijke klantfactuur starten**

Selecteer in rechtspersoon B op de pagina **Intercompany** voor leveranciers de optie **Inkooporderbeleid**. Selecteer in de veldgroep **Oorspronkelijke verkooporder (rechtstreekse levering)** de volgende velden:

- **Pakbon automatisch afdrukken**
- **Factuur automatisch boeken**
- **Factuur automatisch afdrukken**

Selecteer in de veldgroep **Intercompany-inkooporder (rechtstreekse levering)** het volgende veld:

- **Factuur automatisch boeken**

Selecteer in de veldgroep **Oorspronkelijke verkooporder <-> Intercompany-inkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**
- **Prijs en korting**

Selecteer in de veldgroep **Intercompany-inkooporder <-> Intercompany-verkooporder** de volgende velden:

- **Klantgegevens**
- **RMA-nummer**
- **Batchnummer**
- **Serienummer**

Selecteer in rechtspersoon C op de pagina **Intercompany** voor klanten de optie **Verkooporderbeleid**. Selecteer in de veldgroep **Intercompany-verkooporder maken** de volgende velden:

- **Verkoopordernummering**: **Nummerreekscode**
- **Overzichtsupdate van documenten voor oorspronkelijke klant toestaan**

Selecteer in de veldgroep **Intercompany-verkooporderprijzen** het volgende veld:

- **Prijs en korting zoeken**

Selecteer in de veldgroep **Intercompany-klantfactuurboeking** de volgende velden:

- **Eenheidsprijs gelijk aan kostprijs**
- **Boeken van de oorspronkelijke klantfactuur starten**

Selecteer in de veldgroep **Intercompany-verkooporder <-> Intercompany-inkooporder** de volgende velden:

- **Batchnummer**
- **Serienummer**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
