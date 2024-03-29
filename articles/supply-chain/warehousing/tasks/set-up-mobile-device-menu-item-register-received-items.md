---
title: Een menuopdracht voor een mobiel apparaat instellen om de ontvangen artikelen te registreren
description: Dit artikel is gericht op de instelling van een menuopdracht voor een mobiel apparaat.
author: Mirzaab
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b59a78ef98215bec7610fe17ed56e6fc287004c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882310"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Een menuopdracht voor een mobiel apparaat instellen om de ontvangen artikelen te registreren

[!include [banner](../../includes/banner.md)]

Dit artikel is gericht op de instelling van een menuopdracht voor een mobiel apparaat. Deze menuopdracht wordt gebruikt voor de registratie van de ontvangst van artikelen die via inkooporders werden besteld. 

U kunt deze guide gebruiken in het demobedrijf USMF. Deze procedure is bedoeld voor de magazijnbeheerder.


## <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menuopties voor mobiel apparaat**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Menuoptie**. Dit is de unieke id voor deze menuopdracht van mobiel apparaat. Zo kunt u `My PO registration` typen.  
4. Typ een waarde in het veld **Titel**. Dit is de titel, die wordt weergegeven aan de gebruiker op het mobiele apparaat. Zo kunt u `PO registration` typen.  
5. Selecteer **Werk** in het veld **Modus**. De registratie van voorhanden hoeveelheden ontvangen voor een inkooporderregel creëert werk: het verplaatsen van de artikelen van het ontvangende gebied naar de voorraad. Werk wordt niet gemaakt voordat de artikelen zijn geregistreerd. Laat de optie **Bestaand werk gebruiken** daarom ingesteld op **Nee**.
6. Selecteer **Ontvangen van inkooporderartikel** in het veld **Proces van werkaanmaak** van e sectie **Algemeen**.
    - Een inkooporderregel moet uniek worden geïdentificeerd voordat voorhanden voorraad kan worden geregistreerd in het magazijn. In dit scenario zal het mobiele apparaat het inkoopordernummer en artikelnummer registreren, waardoor het systeem de IO-regel zal kunnen identificeren. Weggezet werk zal worden gemaakt en zal door een andere medewerker kunnen worden verzameld. De methode voor werkaanmaak die u selecteert, bepaalt welke velden beschikbaar worden op het sneltabblad **Algemeen**.  
    - Als u de optie **Standaardgegevens gebruiken** selecteert, wordt de knop **Standaardgegevens** ingeschakeld. Hier kunt u velden selecteren voor het weergeven van gegevens die een medewerker meestal in het dagelijks werk nodig heeft, zodat deze waarden op het mobiele apparaat worden weergegeven.  
    - De parameter **Nummerplaatgroepering** werkt in combinatie met de volgordegroep voor de eenheid die is toegewezen aan het artikel dat is ontvangen. U kunt opgeven of ontvangstbewijzen van minder dan of meer dan een pallet moeten worden gegroepeerd in een nummerplaat, of opgedeeld in een aparte nummerplaat voor elke eenheid.  
    - Als u de optie **Nummerplaat maken** selecteert, wordt een uniek nummerplaatnummer gegenereerd op basis van de nummerreeksselectie.  
    - U kunt de sjabloon selecteren die wordt gebruikt wanneer werk wordt gemaakt. Als u bijvoorbeeld een artikel voor een inkooporder registreert, wordt het weggezette werk gegenereerd op basis van het werksjabloon. Als u hier geen werksjabloon selecteert, wijst het systeem een sjabloon toe op basis van de zoekcriteria die aan de sjablonen zijn gekoppeld.  
    - Als er op het mobiele apparaat beschikkingscodes worden weergegeven, kunnen de medewerkers de status of kwaliteit van de artikelen beoordelen en de gewenste code selecteren. De regels voor de beschikkingscode definiëren of de artikelen voor andere magazijnprocessen beschikbaar zijn. De regels bepalen ook welke locatie-instructie wordt gebruikt voor het werk dat wordt gemaakt.   
    - Als u de optie **Batchbeschikkingscodes** selecteert, kunnen medewerkers de status of kwaliteit van een batch beoordelen en de gewenste beschikkingscode selecteren. De regels die zijn ingesteld voor de batchbeschikkingscode definiëren of de batch voor andere magazijnprocessen beschikbaar is.  
    - Als u de optie **Etiketten afdrukken** selecteert, wordt een nummerplaatlabel automatisch afgedrukt wanneer de artikelen zijn ontvangen.  
7. Selecteer **Opslaan**.
8. Sluit de pagina.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>De menuopdracht toevoegen aan het menu van een mobiel apparaat
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellingen > Mobiel apparaat > Menu voor mobiel apparaat**.
2. Gebruik het **snelfilter** om op het veld **Naam** te filteren met de waarde `inbound`.
3. Selecteer **Bewerken**.
4. Selecteer in de structuur Beschikbare menu's en menuopdrachten de menuopdracht die u eerder hebt gemaakt.
5. Selecteer de pijl naar rechts.
6. Selecteer **Opslaan**.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]