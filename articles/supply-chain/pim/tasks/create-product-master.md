--- 
title: Een productmodel maken
description: Maak een productmodel voor de vooraf gedefinieerde varianten.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f944258e7efdd5c9eba7daf9a80c67058a6cc055
ms.openlocfilehash: 6e5cf92f7736523faf25ac97278a8a273e14ff88
ms.contentlocale: nl-nl
ms.lasthandoff: 10/25/2017

---
# <a name="create-a-product-master"></a>Een productmodel maken

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Maak een productmodel voor de vooraf gedefinieerde varianten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de productontwerper.


## <a name="create-a-new-product-master"></a>Een nieuw productmodel maken
1. Ga naar Productgegevensbeheer > Producten > Productmodellen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Productnummer.
    * Het nummer moet uniek zijn. Er kan een nummerreeks worden ingesteld voor het veld Productnummer. In dit geval hoeft de gebruiker geen waarde in te voeren.  
4. Typ een waarde in het veld Productnaam.
    * Voer een omschrijvende naam van het product in. Voor de waarde wordt standaard de zoeknaam gebruikt, maar deze kan door de gebruiker worden gewijzigd.  
5. Klik in het veld Productdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De productdimensiegroep bepaalt van de 4 productdimensies kunnen worden gebruikt voor het maken van productvarianten. In dit voorbeeld wordt een groep met kleur en maat gebruikt.  
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
    * De standaard configuratietechnologie is Vooraf gedefinieerde variant. Deze wordt gebruikt voor dit voorbeeld.  
8. Klik op OK.

## <a name="select-product-dimension-groups"></a>Productdimensiegroepen selecteren
1. Klik in het veld Kleurgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
2. Zoek en selecteer het gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het veld Formaatgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
6. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="add-dimension-groups"></a>Dimensiegroepen toevoegen
1. Klik in het actievenster op Product.
2. Klik op Dimensiegroepen om het dialoogvenster te openen.
3. Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De opslagdimensies helpen u bij het beheer over de opslag en het verwijderen van artikelen in de voorraad. Zo kan bijvoorbeeld een opslagdimensie Locatie en Magazijn bevatten.  
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De traceringsdimensiegroep bepaalt welke traceringsdimensies u kunt toevoegen aan een product. Het batchnummer en serienummer worden bijvoorbeeld gebruikt om voorraadartikelen te traceren.  
7. Zoek en selecteer de gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op OK.
10. Klik op Opslaan.
11. Sluit de pagina.


