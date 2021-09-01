---
title: Kortingsbeheergroepen
description: In dit onderwerp wordt beschreven hoe u kortingsbeheergroepen instelt. Kortingsbeheergroepen kunnen worden gebruikt tijdens kortingsberekeningen en kunnen aan een hoofdrecord worden gekoppeld.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 10b5238f53f89dbd79e6a0fa4ef24ee92f0ae752f220c1f4d19ea629969a3049
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767383"
---
# <a name="rebate-management-groups"></a>Groepen voor kortingsbeheer

[!include [banner](../includes/banner.md)]

Kortingsbeheerberekeningen kunnen worden aangedreven door groepen. Kortingsbeheergroepen kunnen worden gemaakt voor klanten, leveranciers en artikelen. Ze kunnen aan een hoofdrecord worden gekoppeld.

## <a name="rebate-management-customer-groups"></a>Klantgroepen voor kortingsbeheer

De berekening voor een groep klanten wordt vaak uitgevoerd voor een keten van bedrijven, zoals een supermarktketen of een franchisebedrijf. Dit type berekening is meestal gerelateerd aan een korting.

Een inhouding wordt vaak berekend zonder na te gaan aan wie de in aanmerking komende order is verkocht. Er zijn echter uitzonderingen. Een licentienemer kan bijvoorbeeld een inhoudingsregeling opstellen waarbij klantgroep A 4 procent ontvangt, maar klantgroep B slechts 3 procent.

### <a name="set-up-customer-groups"></a>Klantengroepen instellen

Als u wilt werken met klantgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Klantgroepen**. U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen. Stel voor elke groep de volgende velden in:

- **Kortingsbeheergroep**: voer een unieke naam voor de groep in.
- **Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.

### <a name="manage-customer-group-assignments"></a>Toewijzingen van klantgroepen beheren

Elke klant kan tot een willekeurig aantal kortingsbeheergroepen behoren. Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de klantenlijst.

Volg deze stappen om klanten voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Klantgroepen**.
1. Selecteer de groep die u wilt beheren.
1. Selecteer in het actievenster de optie **Klanten**. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met klanten die al lid zijn van de geselecteerde groep.
1. Als u een nieuwe klant wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Klantrekening**: selecteer de klantrekening-id.

1. Als u een klant uit de groep wilt verwijderen, selecteert u de klant en selecteert u vervolgens **Verwijderen** in het actievenster.

Volg deze stappen om groepstoewijzingen voor een geselecteerde klant weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Klanten \> Klanten \> Alle klanten**.
1. Selecteer de klant waarmee u wilt werken.
1. Selecteer vervolgens in het actievenster op het tabblad **Klant** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe de geselecteerde klant al bestaat.
1. Als u de klant wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Kortingsbeheergroep**: selecteer de groep waaraan u de klant wilt toevoegen.

1. Als u een klant uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.

## <a name="rebate-management-vendor-groups"></a>Leveranciersgroepen voor kortingsbeheer

De berekening voor een groep leveranciers wordt vaak gemaakt voor een groep leveringspunten. Dit type berekening is meestal gerelateerd aan een korting.

### <a name="set-up-vendor-groups"></a>Leveranciersgroepen instellen

Als u wilt werken met leveranciersgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Leveranciersgroepen**. U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen. Stel voor elke groep de volgende velden in:

- **Kortingsbeheergroep**: voer een unieke naam voor de groep in.
- **Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.

### <a name="manage-vendor-group-assignments"></a>Toewijzingen van leveranciersgroepen beheren

Elke leverancier kan tot een willekeurig aantal kortingsbeheergroepen behoren. Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de leverancierslijst.

Volg deze stappen om leveranciers voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Leveranciersgroepen**.
1. Selecteer de groep die u wilt beheren.
1. Selecteer **Leveranciers** in het actievenster. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met leveranciers die al lid zijn van de geselecteerde groep.
1. Als u een nieuwe leverancier wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Leveranciersrekening**: selecteer de leveranciersrekening-id.

1. Als u een leverancier uit de groep wilt verwijderen, selecteert u de leverancier en selecteert u vervolgens **Verwijderen** in het actievenster.

Volg deze stappen om groepstoewijzingen voor een geselecteerde leverancier weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers**.
1. Selecteer de leverancier waarmee u wilt werken.
1. Selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe de geselecteerde leverancier al bestaat.
1. Als u de leverancier wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Kortingsbeheergroep**: selecteer de groep waaraan u de leverancier wilt toevoegen.

1. Als u een leverancier uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.

## <a name="item-rebate-groups"></a>Artikelkortingsgroepen

Door artikelen te groeperen, hebt u meer flexibiliteit bij het berekenen van kortingen en inhoudingen. Deze aanpak is vaak een efficiëntere manier om kortingen en inhoudingen in te stellen voor klanten en leveranciers.

### <a name="set-up-item-groups"></a>Artikelgroepen instellen

Als u wilt werken met artikelgroepen voor kortingsbeheer, gaat u naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**. U kunt de knoppen in het actiedeelvenster gebruiken om naar behoefte groepen toe te voegen en te verwijderen. Stel voor elke groep de volgende velden in:

- **Kortingsbeheergroep**: voer een unieke naam voor de groep in.
- **Beschrijving**: voer een beschrijving van de groep in om meer informatie te geven over hoe deze moet worden gebruikt.

### <a name="manage-item-group-assignments"></a>Toewijzingen van artikelgroepen beheren

Elk artikel kan tot een willekeurig aantal kortingsbeheergroepen behoren. Als u groepsleden wilt weergeven en toewijzen, kunt u beginnen vanuit de groepslijst of de artikellijst. U kunt ook artikelen toevoegen op basis van uw categoriehiërarchie.

Volg deze stappen om artikelen voor een geselecteerde groep weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**.
1. Selecteer de groep die u wilt beheren.
1. Selecteer **Artikelen** in het actievenster. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met artikelen die al lid zijn van de geselecteerde groep.
1. Als u een nieuw artikel wilt toevoegen aan de groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Artikelrekening**: selecteer de artikelrekening-id.

1. Als u een artikel uit de groep wilt verwijderen, selecteert u het artikel en selecteert u vervolgens **Verwijderen** in het actievenster.

Volg deze stappen om groepstoewijzingen voor een geselecteerd artikel weer te geven, toe te voegen of te verwijderen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer het artikel waarmee u wilt werken.
1. Selecteer vervolgens in het actievenster op het tabblad **Product** in de groep **Kortingsbeheer** de optie **Kortingsbeheergroepen**. De pagina **Kortingsbeheergroepen** wordt weergegeven en toont een lijst met groepen waartoe het geselecteerde artikel al bestaat.
1. Als u het artikel wilt toevoegen aan een nieuwe groep, selecteert u **Nieuw** in het actievenster om een rij toe te voegen aan het raster. Stel daarna het volgende veld in voor de nieuwe rij:

    - **Kortingsbeheergroep**: selecteer de groep waaraan u het artikel wilt toevoegen.

1. Als u een artikel uit een groep wilt verwijderen, selecteert u de groep en selecteert u vervolgens **Verwijderen** in het actievenster.

Volg deze stappen om artikel toe te voegen aan een groep op basis van uw categoriehiërarchie.

1. Ga naar **Kortingsbeheer \> Kortingsbeheergroepen instellen \> Artikelgroepen**.
1. Selecteer de groep die u wilt beheren.
1. Selecteer **Artikelen toevoegen** in het actievenster.
1. Selecteer in het dialoogvenster **Artikelen toevoegen** in het veld **Categoriehiërarchie** een categorie op het hoogste niveau.
1. De artikelhiërarchie wordt geopend in het linkerdeelvenster. Selecteer het hiërarchieniveau dat u zoekt. 
1. Artikelen uit de geselecteerde hiërarchie en van het geselecteerde hiërarchieniveau worden nu in het rechterdeelvenster weergegeven. Volg deze stappen om met het deelvenster te werken:

    - Schakel het selectievakje in voor elk artikel dat u wilt toevoegen.
    - Schakel het selectievakje in de rasterkop in om alle artikelen te selecteren die worden vermeld.
    - Selecteer de knop **Selectie weergeven** om het raster te filteren, zodat alleen de artikelen worden weergegeven die u tot nu toe hebt geselecteerd. Selecteer de knop nogmaals om terug te keren naar de volledige lijst.

1. Selecteer **OK** om uw artikelselectie toe te passen op de geselecteerde groep.
