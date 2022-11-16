---
title: Workflows gebruiken om werknemersgegevens te beheren
description: In dit artikel wordt uitgelegd hoe u werkstromen kunt gebruiken om medewerkersgegevens te beheren.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750729"
---
# <a name="use-workflows-to-manage-employee-information"></a>Workflows gebruiken om werknemersgegevens te beheren

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt uitgelegd hoe u de workflowmogelijkheid voor Human resources kunt gebruiken om werknemersgegevens te beheren. U kunt bijvoorbeeld een workflow aan een positie koppelen en een goedkeuringsworkflow configureren die wordt gestart wanneer werknemers hun record wijzigen.

De workflowmogelijkheid voor Human resources biedt een groot aantal workflows voor het beheren van human resources-activiteiten. Bovendien zijn er vele opties beschikbaar zodat u specifieke workflows kunt wijzigen en deze aan een rapportagehiërarchie kunt koppelen. Werkstromen zijn beschikbaar om wijzigingen in verschillende typen medewerkersgegevens gemakkelijker te beheren. U kunt een workflow koppelen aan een positie. Vervolgens wordt er, als werknemers hun werknemersrecord wijzigen, een workflow gestart die moet worden goedgekeurd voordat de nieuwe informatie wordt opgeslagen. Werkstromen worden vooraf gedefinieerd voor de volgende typen informatie om wijzigingen efficiënt te beheren en uw medewerkersgegevens nauwkeurig te houden:

-   Identificatienummers
-   Cursussen
-   Onderwijs
-   Afbeelding
-   Geleende artikelen
-   Beroepservaring
-   Projectervaring
-   Vaardigheden
-   Vertrouwensposities
-   Acties van Human Resources
-   Cursusregistratie

Wanneer werknemers worden aangesteld of overgeplaatst of wanneer hun dienstverband wordt beëindigd, kan de workflow een controleproces bevatten. Op deze manier kan een document worden herzien of kunnen de voorwaarden van een actie als onderdeel van de werkstroom worden gedefinieerd. Wanneer het controleproces is voltooid, wordt het document of de actie voltooid en wordt de workflow verplaatst naar een laatste goedkeuringsstap.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Een workflow koppelen aan een positiehiërarchie

U kunt een workflow koppelen aan elke positiehiërarchie die u configureert. Er worden twee hiërarchietypen gebruikt voor workflowroutering: voor **leidinggevenden** en **configureerbaar**.

- Een **hiërarchie voor leidinggevenden** vertegenwoordigt de rapportagestructuur van het bedrijf of de organisatie. Zie [Verantwoording aan positie](hr-personnel-positions.md#reports-to-position) voor meer informatie over dit hiërarchietype .
- Een **configureerbare hiërarchie** vertegenwoordigt een matrix of aangepaste hiërarchie. Zie [Relaties](hr-personnel-positions.md#relationships) voor meer informatie over dit hiërarchietype .

### <a name="managerial-hierarchy-example"></a>Voorbeeld van hiërarchie voor leidinggevenden

U kunt een workflow zo configureren dat wanneer een werknemer een inkoopaanvraag indient voor een nieuwe computer, de aanvraag naar de manager van de werknemer wordt gerouteerd en managerniveaus worden overgeslagen. Wanneer u de workflowstap configureert, stelt u het veld **Toewijzingstype** in op **Hiërarchie**. Vervolgens wordt het tabblad **Hiërarchietype** beschikbaar. Selecteer voor dit voorbeeld de hiërarchie **Leidinggevenden**.

### <a name="configurable-hierarchy-example"></a>Voorbeeld van configureerbare hiërarchie

Als een positie is gekoppeld aan een matrixrapportagehiërarchie, kunt u een workflow configureren waarmee onkosten voor een bepaald project worden doorgestuurd naar de projectleider in plaats van de manager van de werknemer. In dit geval stelt u het veld **Toewijzingstype** in op **Hiërarchie**. Selecteer op het tabblad **Type hiërarchie** de optie **Configureerbare hiërarchie**. Nadat de workflow is ingesteld, selecteert u de hiërarchie **Koppelen** op de pagina **Workflows instellen** om de hiërarchie te selecteren die moet worden gebruikt voor de workflowroutering.

> [!IMPORTANT]
> Wanneer een document, transactie of hoofdrecord wordt ingediend voor workflowgoedkeuring, wordt de primaire positie van de indiener gebruikt om te bepalen naar wie het document moet worden gerouteerd.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hiërarchie-instelling in Workflowparameters

1. Ga op de pagina **Workflowparameters** naar **Hiërarchieroutering**.
2. De optie **Positiehiërarchie gebruiken** is standaard ingesteld op **Nee**. In dit geval gebruikt de workflow de primaire positie van de werknemer wanneer deze door de hiërarchie navigeert. Stel de optie in op **Ja** om ervoor te zorgen dat de workflow de bovenliggende functie gebruikt wanneer deze door de hiërarchie navigeert.

### <a name="additional-example"></a>Extra voorbeeld 

Werknemer Grace Sturman erkent twee functies: consultant en trainer. De primaire functie van Grace is die van trainer. Wanneer ze geen nieuwe werknemers traint, is ze beschikbaar voor advieswerk. Via haar primaire functie legt Grace verantwoording af aan Claire, directeur van de afdeling Human Resources. Claire legt verantwoording af aan Charlie. Voor haar functie als consultant heeft Grace meerdere indirecte relaties, afhankelijk van het project.

Het bedrijf van Grace maakt workflowrouteringsregels die zijn gebaseerd op een **configureerbare** hiërarchie (matrix-/projecthiërarchieën). Deze hiërarchie gebruikt de functie van consultant van Grace. Als de optie **Positiehiërarchie gebruiken** is ingesteld op **Nee**, wordt er, als een document ter goedkeuring naar Grace wordt gerouteerd, gekeken naar haar primaire functie (trainer) om te bepalen waarheen het document vervolgens moet worden gerouteerd. In dit geval wordt het eerst naar Claire en vervolgens naar Charlie gerouteerd. Als de optie is ingesteld op **Ja** en de workflow gebruikmaakt van een **configureerbare** hiërarchie, worden de consultantpositie van Grace en de hiërarchische relatie onderzocht om te bepalen waarnaar het document vervolgens moet worden gerouteerd.

### <a name="configure-a-human-resources-workflow"></a>Een workflow voor Human resources configureren
Voer de volgende stappen uit om een eenvoudige workflow te configureren die wordt gestart wanneer werknemers een wijziging van hun persoonlijke identificatienummer aanvragen.

1.  Op de pagina **Human resources-werkstromen** selecteert u **Nieuw**.
2.  Selecteer in de lijst met beschikbare workflows **Identificatienummers**.
3.  Selecteer **Uitvoeren** om de workflowontwerper te openen en voer vervolgens uw gebruikersnaam en wachtwoord in.
4.  Verplaats het element **Identificatienummer goedkeuren** vanuit de lijst met workflowelementen naar het ontwerperscanvas.
5.  Verbind het goedkeuringselement met **Starten** en **Voltooien**.
6.  Dubbeltik op (of dubbelklik) op **Element goedkeuren**, selecteer en houd dit vast (of klik met de rechtermuisknop) en selecteer **Eigenschappen**.
7.  Voer de volgende stappen uit om werkiteminstructies toe te voegen:

    1.  Selecteer **Toewijzing** en selecteer vervolgens **Hiërarchie** onder het toewijzingstype.
    2.  Selecteer onder de sectie **Hiërarchie** **Configureerbare hiërarchie**.
    3.  Voeg een stopvoorwaarde toe en sluit de pagina.

8.  Voltooi eventuele aanvullende instructies.
9.  Selecteer **Opslaan en sluiten**. Activeer de nieuwe workflow wanneer het dialoogvenster wordt geopend en selecteer **Actief maken**.
10. Ga naar **Human Resources** &gt; **Posities** &gt; **Positiehiërarchietypen**.
11. Selecteer **Matrix**.
12. Voeg de workflow **Identificatienummer van werknemer** aan de lijst toe.

## <a name="additional-resources"></a>Aanvullende bronnen

[Adreswijzigingen weergeven en beheren](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
