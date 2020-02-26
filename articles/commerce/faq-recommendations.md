---
title: Veelgestelde vragen over productaanbevelingen
description: Dit onderwerp bevat informatie over processen en hulpprogramma's die u kunt gebruiken om problemen op te lossen die betrekking hebben op aanbevelingen van producten of hun resultaten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7951f92ef68a7a782f2874d7b73d7e45eba0afba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003022"
---
# <a name="product-recommendations-faq"></a>Veelgestelde vragen over productaanbevelingen


[!include [banner](includes/banner.md)]

Dit onderwerp bevat informatie over processen en hulpprogramma's die u kunt gebruiken om problemen op te lossen die betrekking hebben op [aanbevelingen van producten](product-recommendations.md) of hun resultaten.

## <a name="best-practices"></a>Aanbevolen procedures
Het is zeer belangrijk dat u het concept van productmodellen en varianten gebruikt. Met de juiste groepering van varianten onder een bovenliggend productmodel kunnen met de lijst van algoritmen en services betere modellen worden gemaakt. Daarnaast kan de service slechts één exemplaar van een product leveren in plaats van alle nauw verwante varianten in een lijst te plaatsen. Wanneer alle nauw verwante varianten in een lijst worden geplaatst, kunnen er onjuiste of dubbele resultaten optreden.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Waarom ontbreken er producten in de lijst met aanbevelingen?

Als er een artikel ontbreekt in een lijst met productaanbevelingen, is er mogelijk een probleem met de configuratie van een product. Er kan bijvoorbeeld een onjuiste startdatum of einddatum van het product zijn, een dimensie is mogelijk onjuist geconfigureerd of het product bevindt zich niet in het juiste kanaalassortiment, enzovoort.

Als een artikel ontbreekt in een aanbevelingslijst die is gebaseerd op kunstmatige intelligentie-machine learning (AI-ML), voldoet het artikel mogelijk niet aan de criteria van de lijst met aanbevelingen of zijn er onvoldoende inkooptransacties voor de aanbevelingslijst om het weer te geven.

Het is raadzaam om de volgende stappen te controleren:
1. **Controleer of de productaanbevelingen in HQ zijn ingeschakeld.** Zie [Productaanbevelingen inschakelen](enable-product-recommendations.md) voor meer informatie over het inschakelen van deze service.
1. **Controleer of de belangrijkste producteigenschappen zijn ingesteld.** Productassortimenten moeten bijvoorbeeld zijn ingesteld op **Opnemen**.
1. **Voor nieuwe geassorteerde producten kan het tot drie uur duren voordat het product in de nieuwe lijst wordt weergegeven.**
1. **Als een product nog steeds niet wordt weergegeven in Trending, Meest verkocht, Anderen vinden dit ook leuk of Vaak samen gekocht, heeft dat product mogelijk onvoldoende transacties.** In dat geval kunt u wachten op verdere transacties, de standaardparameters voor de aanbevelingslijst bijwerken of handmatige interventie gebruiken om de resultaten van de productlijst te wijzigen. Zie [Resultaten van aanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.
1. **Controleer of het product voldoet aan de aanbevelingscriteria voor de lijst.** Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Hoe voorkom ik dat er slechte aanbevelingen worden geretourneerd?

Voor aanbevelingslijsten is een groot volume aan transacties nodig om resultaten te produceren. Het is daarom belangrijk dat gebruikers volledige historische transactiegegevens kunnen opgeven.

Bovendien hebben producten zonder transacties of weinig transacties geen resultaten voor **Anderen vinden dit ook leuk** of **Vaak samen gekocht** en worden ze niet weergegeven in de lijst met aanbevelingen voor **Trending** of **Meest verkocht**. Deze situatie kan zich vaak voordoen voor zeer nieuwe producten of voor oude producten met een klein aantal aankopen. Dit probleem kan eenvoudig worden opgelost met populaire nieuwe items.

Het is raadzaam om de volgende stappen te volgen:
1. **Controleer of het product voldoet aan de aanbevelingscriteria voor die lijst.** Zie Resultaten van productaanbevelingen wijzigen op basis van AI-ML voor meer informatie over parameters voor aanbevelingen.
1. **Als het product nieuw is, kunt u overwegen een lijst met aanbevelingen te wijzigen totdat het product meer transacties heeft.** Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de resultaten voor de lijst met aanbevelingen.


- **Controleer of het product voldoet aan de aanbevelingscriteria voor die lijst.** Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over parameters voor aanbevelingen.
- **Als het product nieuw is, kunt u overwegen een lijst met aanbevelingen te wijzigen totdat het product meer transacties heeft**. Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de resultaten voor de lijst met aanbevelingen.

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Kan ik een product verwijderen, maar toch in de winkel zien?

U kunt lijsten aanpassen die algoritmisch gegenereerd worden als dat nodig is. Als een product echter wordt verwijderd uit een aanbevelingslijst, blijft het detecteerbaar in de winkel. Zie [Resultaten van productaanbevelingen beheren op basis van AI-ML](modify-product-recommendation-results.md) voor meer informatie over het wijzigen van de productaanbevelingen.

Als u wilt voorkomen dat een artikel wordt gevonden in de winkel, moet u de waarde van **Artikelassortimenten** wijzigen in **Uitsluiten**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Hoe voeg ik een lijst toe aan een e-commerce-pagina?

Zie [Aanbevelingslijsten voor producten toevoegen aan pagina's](add-reco-list-to-page.md) voor informatie over het toevoegen van pagina's met aanbevelingen aan uw e-commerce-website.

## <a name="how-do-i-enable-recommendations-on-pos"></a>Hoe schakel ik aanbevelingen in op POS?

Nadat u productaanbevelingen hebt ingeschakeld, moet u het deelvenster met aanbevelingen toevoegen aan het POS-scherm van het besturingselement. Zie [de documentatie bij deze functie](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) voor meer informatie over hoe u het deelvenster met aanbevelingen aan de POS-apparaatindeling kunt toevoegen.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht productaanbevelingen](product-recommendations.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Resultaten van productaanbevelingen op basis van AI-ML beheren](modify-product-recommendation-results.md)
