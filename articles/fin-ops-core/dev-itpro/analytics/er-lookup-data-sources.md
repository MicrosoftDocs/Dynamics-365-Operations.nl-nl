---
title: Gegevensbronnen voor opzoeken configureren om ER-toepassingsspecifieke parameters te gebruiken
description: In dit onderwerp wordt uitgelegd hoe u gegevensbronnen voor opzoeken in ER-indelingen (Elektronische rapportage) kunt configureren voor het gebruik van ER-applicatiespecifieke parameters.
author: NickSelin
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 542580c859759c25da84589ec82495eb72bbcbe5
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853516"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Gegevensbronnen voor opzoeken configureren om ER-toepassingsspecifieke parameters te gebruiken 

[!include[banner](../includes/banner.md)]

Met de functie voor toepassingsspecifieke [ER-parameters](general-electronic-reporting.md) kunt u gegevens filteren in een ER-indeling, zodat deze is gebaseerd op een set abstracte regels. Deze set regels kan worden geconfigureerd voor gebruik van de gegevensbronnen van het type **Opzoeken** die beschikbaar zijn in een ER-indeling. U kunt vervolgens echte regels opgeven die verder gaan dan het ontwerpen van ER-componenten door de gebruikersinterface (UI) te gebruiken die automatisch wordt gegenereerd op basis van de instellingen van de gegevensbron voor **Opzoeken** van de overeenkomstige ER-indeling en de huidige gegevens van de rechtspersoon. Uiteindelijk worden de opgegeven regels geopend door de gegevensbron **Opzoeken** van de ER-indeling wanneer deze ER-indeling wordt uitgevoerd.

> [!NOTE]
> Gebruik de geconfigureerde gegevensbronnen van de bewerkbare ER-indeling om op te geven welke toepassingsgegevens worden gebruikt om echte regels te configureren.

Gebruik de [ER Operations-ontwerper](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) om een gegevensbron van het type **Opzoeken** in uw ER-indeling op te nemen. De gegevensbron moet worden geconfigureerd om te beschrijven hoe uw abstracte regels eruitzien, waaronder het volgende:

   - De parameterset van een bepaald gegevenstype waarvan de waarde wordt opgegeven om één regel op te geven.
   - Het waardetype van bepaalde gegevenstypen dat door één regel wordt geretourneerd wanneer deze regel onder andere als het meest geschikt wordt beschouwd.

U kunt de volgende typen gegevensbronnen voor **Opzoeken** configureren, afhankelijk van het type waarde dat door elke geconfigureerde regel wordt geretourneerd:

   - Gebruik het type **Gegevensmodel\Opzoeken** wanneer een modelopsommingswaarde moet worden geretourneerd.
   - Gebruik het type **Dynamics 365 Operations\opzoeken** wanneer een opsommingswaarde voor een toepassing of een waarde voor een [uitgebreid gegevenstype van een toepassing](../extensibility/extensible-edts.md) moet worden geretourneerd.
   - Gebruik het type **Opmaakopsomming\Opzoeken** wanneer een opmaakopsommingswaarde moet worden geretourneerd.

In de volgende afbeelding ziet u hoe een opmaakopsomming kan worden geconfigureerd in de ER-voorbeeldindeling.

   ![Een opmaakopsomming weergeven als basis voor de geconfigureerde opzoekgegevensbron](./media/er-lookup-data-sources-img1.gif)

In de volgende afbeelding ziet u de opmaakonderdelen die zijn geconfigureerd om verschillende soorten belastingen te rapporteren in een andere sectie van een gegenereerd rapport.

   ![De opmaaksecties weergeven om verschillende soorten belastingen afzonderlijk te rapporteren](./media/er-lookup-data-sources-img2.png)

In de volgende afbeelding ziet u hoe de ER Operations-ontwerpfunctie de toevoeging van een gegevensbron van het type **Opmaakopsomming\Opzoeken** toestaat.  De toegevoegde gegevensbron wordt geconfigureerd als het retourneren van een waarde van de opmaakopsomming `List of taxation levels`.

   ![Een ER-gegevensbron toevoegen van het opmaakopsomming\opzoektype](./media/er-lookup-data-sources-img3.gif)

In de volgende afbeelding ziet u hoe de toegevoegde gegevensbron is geconfigureerd om het veld **Code** van de recordlijst **Model.Data.Tax** uit de gegevensbron **Model** te gebruiken als een parameter die voor elke geconfigureerde regel moet worden opgegeven.

![Parameters configureren van de toegevoegde gegevensbron van het type Opmaakopsomming\Opzoeken](./media/er-lookup-data-sources-img4.gif)

De toegevoegde `Model.Data.Tax`-gegevensbron is geconfigureerd om een belastingcode op te geven voor elke geconfigureerde regel door toegang te krijgen tot records van de  **TaxTable**-toepassingstabel.

   ![Beoordeling van de gegevensbron voor het opzoeken van één bedrijf van het type Opmaakopsomming\Opzoeken](./media/er-lookup-data-sources-img5.gif)

U kunt de opzoekregels voor de geselecteerde ER-indeling instellen met behulp van de gebruikersinterface die automatisch wordt uitgelijnd met de structuur van de geconfigureerde gegevensbron. Momenteel vereist deze gebruikersinterface dat u voor elke regel de geretourneerde waarde opgeeft als de waarde voor de `List of taxation levels`-opmaakopsomming en de belastingcode als parameter.

   ![De regels voor de geconfigureerde gegevensbron instellen](./media/er-lookup-data-sources-img6.gif)

In de volgende afbeelding ziet u hoe de gegevensbron `Model.Data.Summary.LevelByLookup` van het type **Berekend veld** kan worden geconfigureerd om de geconfigureerde **opzoekgegevensbron** met de vereiste parameters aan te roepen. Als u deze aanroep tijdens runtime wilt verwerken, doorloopt ER de lijst met geconfigureerde regels in de gedefinieerde reeks om de eerste regel te vinden die aan de opgegeven voorwaarden voldoet. In dit voorbeeld is het de regel die de belastingcode bevat die overeenkomt met de opgegeven code. Als gevolg hiervan wordt de meest geschikte regel gevonden en wordt door deze gegevensbron de opsommingswaarde geretourneerd die is geconfigureerd voor de gevonden regel.

> [!NOTE]
> Er wordt een uitzondering gegenereerd wanneer er geen toepasselijke regel wordt gevonden. Als u deze uitzonderingen wilt voorkomen, configureert u aanvullende regels aan het einde van de lijst met regels om aanvragen af te handelen wanneer een niet-geconfigureerde waarde of geen waarde wordt opgegeven. Gebruik dienovereenkomstig de opties **\*Niet leeg\*** en **\*Leeg\***.  
>
> ![Een gegevensbron toevoegen om de geconfigureerde opzoekgegevensbron aan te roepen](./media/er-lookup-data-sources-img7.png)

Wanneer u de optie **Meerdere bedrijven** instelt op **Ja** voor de bewerkbare opzoekgegevensbron, voegt u een nieuwe vereiste **bedrijfsparameter** toe aan de set parameters van deze gegevensbron. De waarde van de parameter **Bedrijf** moet tijdens runtime worden opgegeven wanneer de opzoekgegevensbron wordt aangeroepen. Wanneer de bedrijfscode tijdens runtime wordt opgegeven, worden de regels die voor dit bedrijf zijn geconfigureerd, gebruikt om de meest geschikte regel te vinden en wordt de bijbehorende waarde geretourneerd. In de volgende afbeelding ziet u hoe u dit kunt doen en hoe de set parameters van de bewerkbare gegevensbron wordt gewijzigd.

   ![Beoordeling van de gegevensbron voor het opzoeken van meerdere bedrijven van het type Opmaakopsomming\Opzoeken](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Selecteer elk bedrijf afzonderlijk om de set regels voor deze opzoekgegevensbron van de bewerkbare ER-indeling te configureren. Er wordt een uitzondering gegenereerd tijdens runtime wanneer de opzoekopdracht voor verschillende bedrijven wordt aangeroepen met de code van het bedrijf waarvoor de opzoekinstelling niet is voltooid.
>
> Zorg ervoor dat u machtigingen verleent voor een gebruiker die de ER-indeling uitvoert met de gegevensbron **Opzoeken** voor meerdere bedrijven om toegang te krijgen tot de gegevens van elk bedrijf binnen het bereik van deze gegevensbron. Anders moet een uitzondering worden gemaakt tijdens runtime.

Vanaf versie 10.0.19 zijn de uitgebreide mogelijkheden van de **opzoekgegevensbronnen** beschikbaar. Wanneer u de optie **Uitgebreid** instelt op **Ja** voor de bewerkbare opzoekgegevensbron, wordt de geconfigureerde opzoekgegevensbron getransformeerd naar de gestructureerde gegevensbron die de extra mogelijkheden biedt om de geconfigureerde set regels te analyseren. In de volgende afbeelding ziet u deze transformatie.

   ![Beoordeling van de gestructureerde opzoekgegevensbron van het type Opmaakopsomming\Opzoeken](./media/er-lookup-data-sources-img9.gif)

- Het subitem **Opzoeken** is ontworpen als een functie om de meest geschikte regel te vinden uit de set configureerbare regels op basis van de opgegeven set parameters.
- Het subitem **IsLookupResultSet** is ontworpen als een functie om de opgegeven waarde van de basisgegevensbron met opsomming te accepteren en de *booleaanse* waarde **true** te retourneren wanneer de set regels ten minste één regel bevat waarvoor de opgegeven opsommingswaarde is geconfigureerd als een geretourneerde waarde. Deze functie retourneert de *booleaanse* waarde **false** wanneer er geen regels zijn geconfigureerd om de opgegeven opsommingswaarde te retourneren.
- Het subitem **Instelling** is ontworpen als een functie die de set geconfigureerde regels retourneert als records van een recordlijst. De geretourneerde waarden en de set parameters van de geconfigureerde regels worden in elke geretourneerde record weergegeven als velden van de relevante gegevenstypen:

    - De geretourneerde waarde wordt weergegeven als het veld **Opzoekresultaat**.
    - De geconfigureerde parameters worden weergegeven als velden met namen van parameters (veld **Code** in dit voorbeeld).

Zie [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon zijn opgegeven](er-app-specific-parameters-configure-format.md) voor meer informatie over het configureren van de gegevensbron **Opzoeken**. Zie [De parameters van een ER-indeling per rechtspersoon instellen](er-app-specific-parameters-set-up.md) voor meer informatie over het instellen van de opzoekregels.

## <a name="additional-resources"></a>Aanvullende bronnen

[ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](er-app-specific-parameters-configure-format.md)

[De parameters van een ER-indeling per rechtspersoon instellen](er-app-specific-parameters-set-up.md)
