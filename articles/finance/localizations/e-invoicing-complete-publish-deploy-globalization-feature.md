---
title: Een globaliseringsfunctie voltooien, publiceren en implementeren
description: Dit onderwerp bevat informatie over de levenscyclus van globaliseringsfuncties.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21e03660387c7e715bc0f4cb1dbcd3ec9ec6cee2
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554556"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Een globaliseringsfunctie voltooien, publiceren en implementeren

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Versies van een functie voor elektronische facturering

De functies voor elektronische facturering hebben bepaalde versies. Wanneer een nieuwe versie wordt gemaakt, wordt het versienummer automatisch verhoogd.

Versies van elektronische factureringsfuncties volgen een levenscyclus met maximaal drie statussen:

- **Concept**: als een functieversie deze status heeft, kunt u de configuratiekenmerken en onderdelen hiervan bewerken (bijvoorbeeld bestandsindelingsconfiguraties).
- **Volledig**: deze status geeft aan dat u de functieversie hebt bewerkt en dat u deze niet meer wilt wijzigen. Wanneer een functieversie deze status heeft, kunt u de functie en de onderdelen ervan niet meer bewerken.
- **Gepubliceerd**: deze status geeft aan dat de functieversie is gepubliceerd in de algemene opslagplaats die aan uw organisatie is gekoppeld. Wanneer een functieversie deze status heeft, kunt u de functie en de onderdelen ervan niet meer bewerken.

U kunt een **ingangsdatum** opgeven voor een nieuwe versie van een elektronische factureringsfunctie. Op deze manier kunt u een standaardversie definiëren die kan worden gebruikt of die kan worden overschreven wanneer de functie in de serviceomgeving wordt geïmplementeerd.

Als u de status van een versie van een elektronische factureringsfunctie wilt wijzigen, volgt u deze stappen.

1. Meld u aan bij uw RCS-account (Regulatory Configuration Service).
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
3. Selecteer links op de pagina **Functies voor elektronische facturering** de functie voor elektronische facturering.
4. Selecteer de versie op het tabblad **Versies** aan de rechterkant van de pagina.
5. Selecteer **Status wijzigen** en selecteer **Voltooid** (als de huidige status **Concept** is) of **Gepubliceerd** (als de huidige status **Voltooid** is).
6. Selecteer **Ja** in het berichtvenster om het verzoek te bevestigen.

De handmatige wijziging van de status **Voltooid** in **Gepubliceerd** is optioneel. Versies van elektronische factureringsfunctie worden automatisch bijgewerkt naar de status **Gepubliceerd** wanneer ze in de serviceomgeving worden geïmplementeerd.

U kunt de status in de kolom **Status van functieversie** bijhouden op het tabblad **Versies**.

## <a name="deploy-feature-versions"></a>Functieversies implementeren

In RCS gebruikt u de opdracht **Implementeren** om een versie van een elektronische factureringsfunctie naar de doelserviceomgeving of gekoppelde toepassing te publiceren.

1. Selecteer links op de pagina **Functies voor elektronische facturering** de functie voor elektronische facturering.
2. Selecteer de versie van de elektronische factureringsfunctie die u in de serviceomgeving of gekoppelde toepassing wilt implementeren op het tabblad **Versies** aan de rechterkant van de pagina. De geselecteerde versie moet de status **Voltooid** of **Gepubliceerd** hebben.
3. Selecteer **Implementeren** en selecteer vervolgens een of meer van de volgende opties om het doel van de implementatie te definiëren:

    - **Verbonden toepassing**: de configuratie die wordt geleverd door de toepassingsinstellingen, is geschreven in het exemplaar van Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management waaraan deze eerder was gekoppeld.
    - **Serviceomgeving**: de versie van de elektronische factureringsfunctie wordt in de serviceomgeving geïmplementeerd. Elektronische facturering is dan klaar om elektronische documenten te ontvangen en te verwerken die door Finance of Supply Chain Management worden verzonden.

> [!NOTE]
> Meestal wijzigt u de parameters van de functie Elektronische rapportage (ER) die in de serviceomgeving moet worden geïmplementeerd. Wijzigingen in de verbonden toepassing worden zelden aangebracht. U moet nieuwe versies alleen implementeren in de verbonden toepassing wanneer u de bijbehorende parameters van de toepassing wijzigt.

Controleer de informatie op het tabblad **Omgevingen** om te bepalen of een specifieke versie van een elektronische factureringsfunctie in een specifieke omgeving wordt geïmplementeerd.

## <a name="remove-feature-versions"></a>Functieversies verwijderen

In RCS gebruikt u **Annuleren** om een specifieke versie van een elektronische factureringsfunctie te verwijderen uit een serviceomgeving als deze daar is geïmplementeerd.

> [!IMPORTANT]
> De knop **Annuleren** werkt alleen voor serviceomgevingen. Deze functie verwijdert niets uit de verbonden toepassing voor de huidige elektronische factureringsfunctie.

## <a name="rebase-electronic-invoicing-features"></a>Functies voor elektronische facturering rebasen

Wanneer een elektronische factureringsfunctie van een andere is afgeleid, selecteert u **Rebase** om de afgeleide functie bij te werken met de wijzigingen die in de oorspronkelijke (bovenliggende) functie zijn aangebracht.

Volg deze stappen om een afgeleide versie van een door u gemaakte functie te rebasen.

1. Haal de laatste versie van de functie op door deze te importeren uit de Algemene opslagplaats. Zie [Functie importeren uit Algemene opslagplaats](e-invoicing-import-feature-global-repository.md) voor meer informatie.
2. Selecteer in de lijst met functies de functie die u wilt rebasen.
3. Selecteer op het tabblad **Versies** de optie **Nieuw** om een conceptversie te maken.
4. Selecteer **Rebase**.
5. Selecteer in het dialoogvenster **Rebase** de versie van de functie waarnaar u wilt rebasen.
6. Selecteer **OK**.
7. Controleer de functieonderdelen en breng eventueel vereiste wijzigingen aan.
8. Selecteer **Status wijzigen** om de functie te voltooien waarvoor een rebase is uitgevoerd. Wanneer de rebase is voltooid, kunt u extra acties uitvoeren.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Een specifieke versie van elektronische factureringsfuncties ophalen

Wanneer u een nieuwe versie van een elektronische factureringsfunctie maakt, wordt een kopie van de laatste functieversie gemaakt. Als u een eerdere versie van de functie wilt gebruiken als basis voor een nieuwe versie, selecteert u de versie en vervolgens **Deze versie ophalen**. Er wordt een nieuwe conceptversie van de functie gemaakt die een kopie is van de geselecteerde versie.
