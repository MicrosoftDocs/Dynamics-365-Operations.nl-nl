---
title: Gegevensimport- en exporttaken
description: Gebruik het werkgebied Gegevensbeheer om taken voor het importeren en exporteren van gegevens te maken en te beheren.
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fc47f6cd9cfe4a850e0959bf89da086ca82f3b69
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="data-import-and-export-jobs"></a>Gegevensimport- en exporttaken

[!INCLUDE [banner](../includes/banner.md)]

Als u gegevensimport- en exporttaken wilt maken en beheren in Microsoft Dynamics 365 for Finance and Operations, gebruikt u het werkgebied **Gegevensbeheer**. Standaard wordt met het proces voor gegevensimport en -export een faseringstabel gemaakt voor elke entiteit in de doeldatabase. Met faseringstabellen kunt u gegevens verifiëren, opschonen of converteren voordat u deze verplaatst.

> [!NOTE]
> Dit onderwerp gaat ervanuit dat u vertrouwd bent met [gegevensentiteiten](data-entities.md).

## <a name="data-importexport-process"></a>Proces voor importeren/exporteren van gegevens
Hier vindt u de stappen die u moet uitvoeren om gegevens te importeren of te exporteren.

1. Maak een import- of exporttaak waarbij u de volgende taken uitvoert:

    - Definieer de projectcategorie.
    - Identificeer de entiteiten die u wilt importeren of exporteren.
    - Stel de gegevensindeling voor de taak in.
    - Bepaal de volgorde van de entiteiten, zodat ze in logische groepen en in een logische volgorde worden verwerkt.
    - Bepaal of u faseringstabellen wilt gebruiken.

2. Controleer of de bron- en doelgegevens juist zijn toegewezen.
3. Controleer de beveiliging voor uw import- of exporttaak.
4. Voer de import- of exporttaak uit.
5. Controleer aan de hand van de taakhistorie of de taak naar verwachting is uitgevoerd.
6. Schoon de faseringstabellen op.

In de overige secties van dit onderwerp vindt u meer informatie over elke stap van het proces.

> [!NOTE]
> Gebruik het pictogram voor het vernieuwen van formulieren om het formulier voor gegevensimport/-export te vernieuwen en de meest recente voortgang te bekijken. Vernieuwen op browserniveau wordt niet aanbevolen omdat hiermee import-/exporttaken worden onderbroken die niet in een batch worden uitgevoerd.

## <a name="create-an-import-or-export-job"></a>Een import- of exporttaak maken
Een taak voor het importeren of exporteren van gegevens kan één keer of meerdere keren worden uitgevoerd.

### <a name="define-the-project-category"></a>De projectcategorie definiëren
Het is raadzaam om de tijd te nemen om een juiste projectcategorie voor uw import- of exporttaak te selecteren. Met projectcategorieën kunt u gerelateerde taken beheren.

### <a name="identify-the-entities-to-import-or-export"></a>De entiteiten identificeren die u wilt importeren of exporteren
U kunt specifieke entiteiten toevoegen aan een import- of exporttaak of een sjabloon selecteren om toe te passen. Sjablonen vullen een taak met een lijst met entiteiten. De optie **Sjabloon toepassen** is beschikbaar als u de taak een naam geeft en opslaat.

### <a name="set-the-data-format-for-the-job"></a>De gegevensindeling voor de taak instellen
Wanneer u een entiteit selecteert, moet u de indeling selecteren van de gegevens die worden geëxporteerd of geïmporteerd. U definieert indelingen via de tegel **Instelling van gegevensbronnen**. Een brongegevensindeling is een combinatie van **Type**, **Vestandsindeling**, **Scheidingsteken rij** en **Scheidingsteken voor kolommen**. Er zijn ook andere kenmerken, maar dit zijn de belangrijkste. In de volgende tabel staan de geldige combinaties.

| **Bestandsindeling**        | **Scheidingsteken rij/kolom**                   | **XML-stijl**             |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-N.v.t.                     |
| XML                    | \-N.v.t.                                      | XML-element XML-kenmerk |
| Gescheiden, vaste breedte | Komma, puntkomma, tab, verticale streep, dubbele punt | \-N.v.t.                     |



### <a name="sequence-the-entities"></a>De volgorde van de entiteiten bepalen
Entiteiten kunnen worden geordend in een gegevenssjabloon of in import- en exporttaken. Wanneer u een taak met meer dan één gegevensentiteit uitvoert, moet u ervoor zorgen dat de gegevensentiteiten correct zijn geordend. U stelt voornamelijk een volgorde voor entiteiten in als er functionele afhankelijkheden tussen entiteiten bestaan. Als entiteiten geen functionele afhankelijkheden hebben, kunnen ze worden gepland voor parallel importeren of exporteren.

#### <a name="execution-units-levels-and-sequences"></a>Uitvoeringseenheden, -niveaus en -volgordes
De uitvoeringseenheid, het niveau in de uitvoeringseenheid en de volgorde van entiteiten bepalen in welke volgorde de gegevens worden geëxporteerd of geïmporteerd.

- Entiteiten in verschillende uitvoeringseenheden worden parallel verwerkt.
- In elke uitvoeringseenheid worden entiteiten parallel verwerkt als ze hetzelfde niveau hebben.
- In elk niveau worden entiteiten verwerkt op basis van hun volgnummer in dat niveau.
- Nadat één niveau is verwerkt, wordt het volgende niveau verwerkt.

#### <a name="resequencing"></a>Opnieuw sequentiëren
In de volgende situaties kan opnieuw sequentiëren nut hebben:

- Als er slechts één gegevenstaak wordt gebruikt voor al uw wijzigingen, kunt u opties voor opnieuw sequentiëren gebruiken om de uitvoeringstijd voor de volledige taak te optimaliseren. In deze gevallen kunt u de uitvoeringseenheid gebruiken voor de module, het niveau voor het functiegebied in de module en de volgorde voor de entiteit. Met deze benadering kunt u parallel werken in verschillende modules, maar u kunt ook op volgorde in een module werken. Om ervoor te zorgen dat parallelle bewerkingen lukken, moet u rekening houden met alle afhankelijkheden.
- Als er meerdere gegevenstaken worden gebruikt (bijvoorbeeld één taak voor elke module), kunt u de optie voor sequentiëren gebruiken om het niveau en de volgorde van entiteiten te wijzigen voor een optimale uitvoering.
- Als er helemaal geen afhankelijkheden zijn, kunt u entiteiten in verschillende uitvoeringseenheden sequentiëren voor maximale optimalisatie.

Het menu **Opnieuw sequentiëren** is beschikbaar wanneer er meerdere entiteiten zijn geselecteerd. U kunt opnieuw sequentiëren op basis van het uitvoeringsniveau, het niveau of sequentieopties. U kunt een verhoging instellen voor het opnieuw sequentiëren van de entiteiten die zijn geselecteerd. De eenheid, het niveau en/of het volgnummer dat is geselecteerd voor elke entiteit wordt bijgewerkt op basis van de opgegeven verhoging.

#### <a name="sorting"></a>Sorteren
Gebruik de optie **Sorteren op** om de entiteitslijst op volgorde weer te geven.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Controleren of de bron- en doelgegevens juist zijn toegewezen
Toewijzing is een functie die zowel op importtaken als op exporttaken wordt toegepast.

- In de context van een importtaak wordt met toewijzing beschreven welke kolommen in het bronbestand de kolommen in de faseringstabel worden. Op deze manier kan het systeem bepalen welke kolomgegevens in het bronbestand naar welke kolom van de faseringstabel moeten worden gekopieerd.
- In de context van een exporttaak wordt met toewijzing beschreven welke kolommen van de faseringstabel (de bron) de kolommen in het doelbestand worden.

Als de kolomnamen in de faseringstabel en het bestand overeenkomen, wordt de toewijzing automatisch uitgevoerd, op basis van de namen. Als de namen afwijken, worden kolommen echter niet automatisch toegewezen. In deze gevallen moet u de toewijzing voltooien door de optie **Kaart weergeven** te selecteren voor de entiteit in de gegevenstaak.

Er zijn twee toewijzingsweergaven: **Visualisering van toewijzing**, de standaardweergave, en **Gegevens toewijzen**. Met een rood sterretje (\*) worden de vereiste velden in de entiteit aangeduid. Deze velden moeten worden toegewezen voordat u met de entiteit kunt werken. U kunt de toewijzing van andere velden desgewenst ongedaan maken wanneer u met de entiteit werkt. Als u de toewijzing van een veld ongedaan wilt maken, selecteert u het veld in de kolom **Entiteit** of **Bron** en selecteert u vervolgens **Selectie verwijderen**. Selecteer **Opslaan** om uw wijzigingen op te slaan en sluit de pagina om terug te keren naar het project. U kunt hetzelfde proces gebruiken om de veldtoewijzingen van bron naar fasering te bewerken na het importeren.

U kunt een toewijzing op de pagina genereren door **Brontoewijzing maken** te selecteren. Een gegenereerde toewijzing gedraagt zich als een automatische toewijzing. Daarom moet u niet-toegewezen velden handmatig toewijzen.

![Toewijzing van gegevens](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>De beveiliging voor uw import- of exporttaak controleren
De toegang tot het werkgebied **Gegevensbeheer** kan worden beperkt zodat niet-beheerders alleen toegang tot bepaalde gegevenstaken krijgen. Toegang tot een gegevenstaak houdt volledige toegang tot de uitvoeringshistorie van die taak en de faseringstabellen in. Daarom moet u ervoor zorgen dat passende toegangsbeperkingen zijn ingesteld wanneer u een gegevenstaak maakt.

### <a name="secure-a-job-by-roles-and-users"></a>Een taak beveiligen op rollen en gebruikers
Gebruik het menu **Toepasselijke rollen** om de taak tot een of meer beveiligingsrollen te beperken. Alleen gebruikers in deze rollen hebben toegang tot de taak.

U kunt een taak ook beperken tot bepaalde gebruikers. Wanneer u een taak op basis van gebruikers beveiligt in plaats van op rollen, is er meer controle wanneer meerdere gebruikers aan een rol zijn toegewezen.

### <a name="secure-a-job-by-legal-entity"></a>Een taak beveiligen op rechtspersoon
Gegevenstaken zijn algemeen van aard. Daarom is een taak zichtbaar in andere rechtspersonen in het systeem als een taak in een rechtspersoon is gemaakt en gebruikt. Dit standaardgedrag kan in sommige toepassingsscenario's de voorkeur genieten. Een organisatie die facturen op basis van gegevensentiteiten importeert, kan bijvoorbeeld een centraal team voor de verwerking van facturen samenstellen dat verantwoordelijk is voor het beheren van factuurfouten voor alle divisies in de organisatie. In dit scenario is het nuttig voor het centrale team voor het verwerken van facturen om vanuit alle rechtspersonen toegang te hebben tot taken voor het importeren van facturen. Daarom voldoet het standaardgedrag aan de vereisten vanuit het perspectief van een rechtspersoon.

Een organisatie kan echter ook de voorkeur geven aan aparte factuurverwerkingsteams per rechtspersoon. In dit geval moet een team in een rechtspersoon alleen toegang hebben tot de taak voor het importeren van facturen binnen de eigen rechtspersoon. Om te voldoen aan deze vereiste, kunt u toegangsbeheer op basis van rechtspersoon voor de gegevenstaken configureren via het menu **Toepasselijke rechtspersonen** in de gegevenstaak. Na de configuratie krijgen gebruikers alleen taken te zien die beschikbaar zijn in de rechtspersoon waarbij ze momenteel zijn aangemeld. Als een gebruiker taken van een andere rechtspersoon wil weergeven, moet hij of zij overschakelen naar die rechtspersoon.

Een taak kan tegelijkertijd op basis van rollen, gebruikers en rechtspersoon worden beveiligd.

## <a name="run-the-import-or-export-job"></a>De import- of exporttaak uitvoeren
U kunt één taak tegelijk uitvoeren door de knop **Importeren** of **Exporteren** te selecteren nadat u de taak hebt gedefinieerd. Als u een terugkerende taak wilt instellen, selecteert u **Terugkerende gegevenstaak maken**.

## <a name="validate-that-the-job-ran-as-expected"></a>Controleren of de taak naar verwachting is uitgevoerd
De taakhistorie is beschikbaar voor het oplossen van problemen bij import- en exporttaken. Historische taakuitvoeringen worden ingedeeld op tijd.

![Taakhistoriebereiken](./media/dixf-job-history.md.png)

Voor elke taakuitvoering worden de volgende gegevens weergegeven:

- Uitvoeringsdetails
- Uitvoeringslogboek

In uitvoeringsgegevens wordt de status weergegeven van elke gegevensentiteit die door de taak is verwerkt. Op deze manier kunt u snel de volgende informatie vinden:

- Welke entiteiten zijn verwerkt
- Hoeveel records voor een entiteit zijn verwerkt en mislukt
- De faseringsrecords voor elke entiteit

U kunt de faseringsgegevens in een bestand voor exporttaken downloaden of u kunt de gegevens downloaden als een pakket voor import- en exporttaken.

Vanuit de uitvoeringsgegevens kunt u ook het uitvoeringslogboek openen.

## <a name="clean-up-the-staging-tables"></a>De faseringstabellen opschonen
U kunt faseringstabellen opschonen met de functie **Fasering opschonen** in het werkgebied **Gegevensbeheer**. U kunt de volgende opties gebruiken om op te geven welke records moeten worden verwijderd uit welke faseringstabel:

- **Entiteit** : als alleen een entiteit is opgegeven, worden alle records uit de faseringstabel van die entiteit verwijderd. Selecteer deze optie om alle gegevens voor de entiteit in alle gegevensprojecten en alle taken te verwijderen.
- **Taak-ID**: als alleen een taak-ID is opgegeven, worden alle records voor alle entiteiten in de geselecteerde taak verwijderd uit de betreffende faseringstabellen.
- **Gegevensprojecten**: als alleen een gegevensproject is geselecteerd, worden alle records voor alle entiteiten en in alle taken voor het geselecteerde gegevensproject verwijderd.

U kunt de opties ook combineren om verder te beperken welke recordset wordt verwijderd.

