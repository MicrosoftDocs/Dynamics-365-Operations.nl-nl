---
title: Conventies
description: In dit onderwerp wordt beschreven hoe u conventies in kunt stellen om vast te stellen hoe kosten moeten worden opgenomen in Algemene voorraadboekhouding.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273138"
---
# <a name="conventions"></a>Conventies

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Een conventie is een container voor een set beleidsregels die van invloed zijn op het systeemgedrag. Op basis van de behoeften van uw bedrijf, moet u conventies definiëren met behulp van een combinatie van de verschillende beleidsregels die bepalen hoe kosten moeten worden verantwoord in Algemene voorraadboekhouding. U kunt elke conventie aan een of meer grootboeken koppelen om consistentie te garanderen in het boekhoudbeleid dat wordt toegepast in grootboeken.

Ga voor het instellen van uw conventies naar **Algemene voorraadboekhouding \> Instellingen \> Conventies**. Stel voor elke conventie de volgende velden in:

- **Naam**: voer de naam van de conventie in.
- **Beschrijving**: voer een beschrijving van de conventie in.
- **Kostenobjectbeleid**: selecteer een kostenobjectbeleid. Met dit beleid wordt het niveau van gedetailleerdheid bepaald dat het systeem gebruikt voor het berekenen en onderhouden van de voorraadwaarde. De volgende vooraf gedefinieerde opties zijn beschikbaar:

    - Artikel
    - Product – Locatie
    - Product – Locatie – Magazijn

    Als u bijvoorbeeld *Product – Locatie* selecteert voor elke voorraadverplaatsing (in- of uitstroom), berekent en onderhoudt het systeem de voorraadkosten van elk product op locatieniveau. Daarom heeft voorraadverloop op lagere niveaus, zoals het magazijnniveau, geen invloed op de voorraadwaarde. (Een voorbeeld van een overdracht op magazijnniveau is een artikeloverdracht tussen twee magazijnen op één locatie.) Zo is het ook mogelijk dat u de voorraadkosten niet op een lager niveau kunt weergeven, zoals het magazijnniveau.

- **Beleid voor invoermetingbasis**: selecteer een beleid voor de invoermetingbasis. Dit beleid bepaalt de kosten die in de voorraadrekening moeten stromen en de kosten die in rekening moeten worden gebracht. De volgende opties zijn relevant voor handelsbedrijven:

    - **Normaal historisch**: alle kostencomponenten stromen naar de voorraadrekening.
    - **Standaard**: de standaardkosten stromen naar de voorraadrekeningen en het verschil tussen de toegepaste kosten en de werkelijke kosten wordt in rekening gebracht in afwijkingsrekeningen. Als u voor invoermetingbasis een *Standaard*-beleid wilt maken, moet u eerst een prijslijst maken waarin de standaardkosten van het artikel door het beleid kunnen worden opgezocht.
    - **Prijslijsten**: Algemene voorraadboekhouding ondersteunt het ophalen van artikelprijzen van meerdere rechtspersonen. U kunt een prijslijst definiëren die wordt gebruikt in het beleid voor invoermetingsbasis. Op deze manier weet het systeem waar de artikelprijs moet worden opgezocht. Ga als volgt te werk om prijslijsten in te stellen:

        1. Voer in het veld **Naam** een naam in.
        1. Voer in het veld **Beschrijving** een beschrijving in.
        1. Selecteer een kostprijsberekeningstype (*Standaardkosten* of *Geplande kosten*) in het veld **Kostprijsberekeningstype**.
        1. Selecteer in het veld **Prijstype** een prijstype (*Kosten*, *Inkoop* of *Verkoopprijs*).
        1. Voeg een kostprijsberekeningsversie toe.
        1. Selecteer **Prijs** in het actievenster om de artikelprijzen in de prijslijst te valideren.

- **Beleid voor veronderstelling van kostenstroom**: selecteer een beleid voor de veronderstelling van de kostenstroom. Dit beleid bepaalt hoe kosten worden verwijderd uit de voorraad en worden gerapporteerd als de kosten van verkochte goederen. De volgende vooraf gedefinieerde opties zijn beschikbaar:

    - Gemiddeld
    - Specifiek– Batch

    > [!NOTE]
    > Algemene voorraadboekhouding is een voorraadsysteem. Het systeem houdt de voorraadwaarde daarom bij per transactie.

- **Kostenelementbeleid**: u kunt het beleid voor kostenelementen definiëren en deze aan dit veld koppelen. Een *kostenelement* betreft de kosten van een resource die door een gebeurtenis wordt verbruikt. U kunt kostenelementen gebruiken om kosten bij te houden en te categoriseren. Als u een beleid voor kostenelementen wilt maken, voert u de gegevens als volgt in:

    - Veld **Naam**
    - Veld **Omschrijving**
    - Lijst **Kostenelement**
    - Raster **Regels**

    Als u de voorraadwaarde niet verder wilt opsplitsen, moet u toch een kostenelementlijst met één kostenelement maken. U moet vervolgens een beleid voor kostenelementen maken om alle relevante metingtypen (kostencomponenten) toe te wijzen aan dat kostenelement.
