---
title: Containers voor verzending verpakken
description: Dit artikel beschrijft het verpakkingsproces waarmee u voorraadartikelen kunt valideren en ze in containers kunt verpakken.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708778"
---
# <a name="pack-containers-for-shipment"></a>Containers voor verzending verpakken

[!include [banner](../../includes/banner.md)]

Met het verpakkingsproces kunnen voorraadartikelen worden gevalideerd en in containers verpakt. Tijdens dit proces verzamelen magazijnmedewerkers meestal voorraadartikelen uit bulkopslaggebieden en verplaatsen ze deze naar een verpakkingsgebied. Daar controleren meerdere magazijnmedewerkers de hoeveelheden en typen artikelen en worden deze toegewezen aan containers van de juiste grootte. Wanneer een container volledig is ingepakt, wordt deze gesloten en verplaatst naar de het gebied met outbound docks, waar de container gereed wordt gemaakt voor verzending.

Containers staan voor fysieke structuren waarin artikelen zijn verpakt en u kunt containergegevens in het systeem bijhouden. Deze informatie kan nuttig zijn bij het plannen van transport, met name als u verzendkosten berekent op basis van containers. Voordat u gaat verzenden, kunt u het aantal containers dat voor een zending wordt gebruikt, de typen containers die worden gebruikt en de fysieke dimensies van elke container (zoals het totale volume en het totale gewicht) bekijken.

Voor containers kunnen verschillende gerelateerde mogelijkheden voor uitgaand magazijn worden gebruikt. Zie de volgende artikelen voor meer informatie:

- [Wave containervorming](wave-containerization.md)
- [Uitgaand sorteren](outbound-sorting.md)
- [Kleine pakketten verzenden](small-parcel-shipping.md)
- [Bevestigen en overboeken](confirm-and-transfer.md)
- [Verschillende dimensies voor verpakking en opslag instellen](packing-vs-storage-dimensions.md)
- [Verpakkingswerk voor het verpakken van uitgaande containers en het verwerken van zendingen](packing-work.md)
- [Containers inpakken met de mobiele app Warehouse Management](warehouse-app-packing-containers.md)
- [Voorbeeldscenario: containers inpakken met de mobiele app Warehouse Management](warehouse-app-pack-containers-scenario.md)
- [Containerlabels afdrukken](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Het magazijn instellen voor handmatige verpakkingsbewerkingen

U kunt uitgaande bewerkingen op twee basismanieren organiseren:

- **Waves aanmaken en verwerken**: werknemers verzamelen artikelen op basis van uitgaand magazijnwerk. Vervolgens plaatsen ze de artikelen direct op een uitgaande verzendlocatie waar ze klaar zijn voor directe verzending. Raadpleeg [Waves aanmaken en verwerken](wave-processing.md) voor meer informatie over het instellen en het gebruik van dit proces.
- **Handmatig verpakken bij inpakstations:** dit proces heeft een extra bewerking tussen de bewerkingen verzamelen en verzenden. In plaats van de voorraad op een *laaddeur voor de uiteindelijke verzendlocatie* te plaatsen, zetten werknemers deze op een *verpakkingslocatie*. Zij beheren vervolgens het verpakkingsproces op het inpakstation met behulp van de pagina **Verpakken** in de webclient. Om dit proces in te schaleken, moet het systeem echter eerst worden geconfigureerd zoals in dit gedeelte wordt beschreven.

### <a name="set-up-warehouse-locations-for-packing"></a>Magazijnlocaties voor verpakken instellen

U moet ten minste één inpaklocatie hebben waar werknemers voorraadartikelen plaatsen zodat ze in containers kunnen worden verpakt. Raadpleeg [Locaties configureren in een magazijn met WMS-ondersteuning](tasks\configure-locations-wms-enabled-warehouse.md) voor meer informatie over het aanmaken van magazijnlocaties. In de volgende subgedeelten wordt beschreven hoe verpakkingslocaties worden aangemaakt en ingesteld.

#### <a name="set-up-location-types-for-packing"></a>Locatietypen voor verpakken instellen

U moet een *locatietype* definiëren voor de verpakkingslocaties. Locatietypen kunnen worden gebruikt als filteropties om de andere magazijnbeheerprocessen te controleren. De naam van elk locatietype beschrijft meestal iets over hoe dat locatietype moet worden gebruikt. Het locatietype dat u hier instelt, moet worden gekoppeld aan elke locatie die wordt gebruikt voor verpakkingsbewerkingen.

Ga als volgt te werk om een locatietype in te stellen:

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locatietypen**.
1. Selecteer in het deelvenster Actie de optie **Nieuw** om een locatietype toe te voegen aan het raster.
1. Stel de volgende velden in voor het nieuwe locatietype:

    - **Locatietype**: voer een naam in voor het locatietype. Elke naam moet uniek zijn en moet iets beschrijven over de manier waarop het locatietype hoort te worden gebruikt.
    - **Beschrijving**: voer een korte beschrijving in van het locatietype.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Geef het systeem informatie over het type verpakkingslocatie

Nadat u een locatietype hebt aangemaakt, moet u het systeem zo instellen dat dit wordt herkend als het locatietype dat bij verpakkingsbewerkingen moet worden gebruikt.

Volg deze stappen om het locatietype in te stellen dat wordt gebruikt voor verpakkingsbewerkingen.

1. Ga naar **Magazijnbeheer \> Instellen \> Parameters voor magazijnbeheer**
2. Stel op het tabblad **Algemeen** op het sneltabblad **Locatietypen** het veld **Type verpakkingslocatie** in op het locatietype dat u gaat gebruiken om inpaktstations te identificeren.

> [!NOTE]
> Als u een upgrade uitvoert van een versie van Microsoft Dynamics AX, is de status *Wordt verpakt* verwijderd uit zendingen en ladingen, omdat deze niet consistent werkte en overbodige gegevens veroorzaakte. Daarom zijn de paklijstpagina's **In zendingen** en **Ladingen** afgeschaft. Containers die moeten worden verpakt, worden op locatieniveau bijgehouden.
>
> In eerdere versies hebt u de verpakkingslocatie gedefinieerd met behulp van het veld **profiel-ID voor verpakkingslocatie** op het tabblad **Verpakken** van de pagina **Parameters voor magazijnbeheer** om een *locatieprofiel* op te geven. In de huidige versie gebruikt u het veld **Type verpakkingslocatie** op het tabblad **Algemeen** van de **Parameters voor magazijnbeheer** om een *locatietype* op te geven, zoals wordt beschreven in dit artikel. Het nieuwe veld is beter afgestemd op het proces voor het identificeren van faseringslocaties en definitieve verzendlocaties.
>
> Hoewel u de oude **profiel-ID voor verpakkingslocatie** kunt blijven gebruiken, wordt het aanbevolen in plaats daarvan het nieuwe veld **Type verpakkingslocatie** te gaan gebruiken, omdat het oude veld uiteindelijk zal worden afgeschaft.
>
> Als u de instelling van het oude veld **profiel-ID voor verpakkingslocatie** leeg maakt en de pagina daarna opslaat, wordt het veld permanent uitgeschakeld. Voor installaties waarbij het veld **profiel-ID voor verpakkingslocatie** nooit is gebruikt, wordt het altijd uitgeschakeld. Nadat u de instelling van het veld **profiel-ID voor verpakkingslocatie** hebt uitgeschakeld, gebruikt u de instellingen die in dit artikel staan beschreven om uw verpakkingslocatie in te stellen en te identificeren.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Locatieprofielen voor verpakkingslocaties instellen

Elk *locatieprofiel* legt informatie en regels vast die van toepassing zijn op de gekoppelde locaties. Aangezien u ten minste één locatie nodig hebt die wordt gebruikt voor verpakkingsbewerkingen, moet u naast een locatietype ook een locatieprofiel voor de locatie aanmaken. Elk profiel kan door een willekeurig aantal locaties worden gebruikt. Locaties die worden gebruikt voor verpakken, moeten worden ingesteld om nummerplaten bij te houden.

Volg deze stappen om een locatieprofiel in te stellen voor een verpakkingslocatie.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatieprofielen**.
1. Selecteer een bestaand profiel in het deelvenster met lijsten of selecteer **Nieuw** in het deelvenster met acties om een nieuw profiel aan te maken.
1. Stel in de koptekst van het nieuwe of geselecteerde profiel de volgende velden in:

    - **ID locatieprofiel**: voer een unieke ID in voor het profiel.
    - **Naam**: voer een beschrijvende naam in voor het profiel.

1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - locatie **Locatie-indeling** : selecteer de locatie-indeling die voor de huidige locatie moet worden gebruikt. Locatie-indelingen zijn een benamingensysteem dat wordt gebruikt om unieke en consistente namen aan te maken voor verschillende locatiebakposities die binnen een magazijn worden gebruikt. Als u de benodigde indeling nog niet hebt, kunt u deze aanmaken door naar **Magazijnbeheer \> Instellen \> Magazijn \> Locatie-indelingen** te gaan. Zie [Locaties configureren in een magazijn met WMS-ondersteuning](tasks/configure-locations-wms-enabled-warehouse.md) voor meer informatie.
    - **Locatietype**: selecteer het locatietype dat is ingesteld als het type verpakkingslocatie op de pagina **Parameters voor magazijnbeheer**, zoals eerder in dit artikel beschreven.
    - **Nummerplaat traceren gebruiken**: stel deze optie voor verpakkingslocaties in op *Ja*. Het systeem moet nummerplaat-ID's op verpakkingslocaties kunnen bijhouden, zodat het verpakkingsproces kan worden gecontroleerd.
    - **Negatieve voorraad toestaan**: stel deze optie voor verpakkingslocaties in op *Nee*.
    - **Gemengde artikelen toestaan**: stel deze optie voor verpakkingslocaties in op *Ja*. Deze instelling is vereist omdat meestal een groot aantal verschillende artikelnummers tegelijkertijd naar de verpakkingslocaties wordt gebracht.
    - **Gemengde voorraadstatussen toestaan**: stel deze optie voor verpakkingslocaties in op *Ja*. Deze instelling is vereist omdat artikelen met verschillende voorraadstatussen meestal tegelijkertijd naar de verpakkingslocaties wordt gebracht.
    - **Gemengde voorraadbatches toestaan**: stel deze optie voor verpakkingslocaties in op *Ja*. Deze optie wordt automatisch ingesteld op *Ja* wanneer de optie **Gemengde artikelen toestsaan** is ingesteld op *Ja*.

#### <a name="set-up-packing-locations"></a>Verpakkingslocaties instellen

U moet ten minste één *locatie* hebben waar werknemers voorraadartikelen plaatsen die in containers moeten worden verpakt.

Ga als volgt te werk om een verpakkingslocatie in te stellen:

1. Ga naar **Magazijnbeheer \> Instellingen \> Magazijn \> Locaties**.
1. Selecteer in het deelvenster Actie **Nieuw** om een locatie toe te voegen.
1. Stel de volgende velden in voor de nieuwe locatie:

    - **Magazijn**: geef het magazijn op waar de verpakkingslocatie zich moet bevinden.
    - **Locatie**: voer een naam in voor de nieuwe locatie.
    - **Locatieprofiel-ID**: geef de ID op die u in het vorige gedeelte hebt aangemaakt.

## <a name="set-up-the-packing-process"></a>Het verpakkingsproces instellen

In dit gedeelte wordt beschreven hoe u instellingen configureert die het verpakkingsproces inschakelen en werknemers de voorraad in containers laten verpakken.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Inpakbeleid voor container instellen

Elk *inpakbeleid voor containers* definieert hoe een container moet worden verwerkt. Telkens wanneer u een nieuwe container aanmaakt, selecteert u ook een inpakbeleid voor containers dat daarop moet worden toegepast.

Voer de volgende stappen uit om een inpakbeleid voor containers in te stellen.

1. Ga naar **Magazijnbeheer \> Instellen \> Containers \> Inpakbeleid voor container**.
1. Selecteer een bestaand beleid in het deelvenster met lijsten of selecteer **Nieuw** in het deelvenster met acties om een nieuw beleid aan te maken.
1. Stel in de koptekst van het nieuwe of geselecteerde beleid de volgende velden in:

    - **Inpakbeleid voor containers**: voer een unieke naam voor het beleid in.
    - **Beschrijving**: voer hier een naam voor het beleid in.

1. Stel op het tabblad **Overzicht** de volgende velden in. Met deze velden kunt u opgeven welke acties moeten worden ondernomen wanneer de container wordt gesloten, of er moet worden gewerkt met of zonder het aanmaken van werk, en wanneer de container moet worden vrijgegeven vanuit het inpakstation.

    - **Magazijn**: selecteer het magazijn waarop het beleid van toepassing is.
    - **Standaardlocatie voor uiteindelijke verzending**: geef de voorkeurslocatie voor de container op nadat deze is gesloten. Dit veld is alleen beschikbaar wanneer het veld **Containervrijgavebeleid** is ingesteld op *Beschikbaar maken op uiteindelijke verzendlocatie*.
    - **Standaardlocatie voor sorteren:** dit veld wordt gebruikt met de mogelijkheid voor [uitgaande sortering](outbound-sorting.md).
    - **Gewichtseenheid**: selecteer de standaardmaateenheid die moet worden gebruikt wanneer een container wordt gesloten en wordt gemanifesteerd. Gewoonlijk is deze maateenheid de maateenheid die wordt gebruikt door een weegschaal bij het inpakstation. Dit veld is van toepassing op beleid met of zonder het aanmaken van werk.
    - **Containerafsluitingsbeleid**: selecteer een van de volgende opties om te definiëren wat er moet gebeuren wanneer de container wordt gesloten:

        - *Automatische vrijgave*: de container wordt beschouwd als vrijgegeven vanuit het inpakstation en de actie die is opgegeven in het veld **Containervrijgavebeleid** wordt geactiveerd.
        - *Uitgestelde vrijgave*: de container wordt niet direct vanuit het inpakstation vrijgegeven. Een magazijnmedewerker moet deze later handmatig vrijgeven.
        - *Optioneel*: terwijl een werknemer de container sluit, kan deze zelf bepalen of de container moet worden vrijgegeven.

        Als het inpakstation voornamelijk enkele containers verwerkt die direct naar klanten worden verzonden, is het de meest natuurlijke aanpak om de containers onmiddellijk vrij te geven. Als het inpakstation zendingen verwerkt die uit meerdere containers of zelfs pallets bestaan, is het waarschijnlijk beter de vrijgave uit te stellen totdat de hele zending of pallet is verpakt en klaar is om te worden opgehaald.

    - **Containervrijgavebeleid**: selecteer een van de volgende opties om te definiëren wat er moet gebeuren wanneer de container wordt vrijgegeven uit het inpakstation:

        - *Beschikbaar maken op de uiteindelijke verzendlocatie*: werk de container bij naar de uiteindelijke verzendlocatie. Als u deze optie selecteert, gebruik dan het veld **Standaardlocatie voor uiteindelijke verzending** om een voorkeurslocatie op te geven voor de container op nadat deze is gesloten.
        - *Werk aanmaken om een container van het inpakstation te verplaatsen*: werk aanmaken om de container van het inpakstation naar het faseringsgebied of rechtstreeks naar de laaddeur te verplaatsen. Gebruik het veld **Werksjabloon** om de werksjabloon op te geven die moet worden toegepast wanneer het werk voor de container wordt aangemaakt.
        - *Container toewijzen aan uitgaande sorteerpositie*: deze optie wordt gebruikt met de mogelijkheid voor [uitgaand sorteren](outbound-sorting.md).

        In de meeste gevallen is het raadzaam om werk aan te maken om containers te verplaatsen, omdat deze aanpak beter de werkelijke handmatige processen in het magazijn weergeeft. Bij eenvoudige scenario's, of situaties waarin het inpakstation zich direct in het gebied van de laaddeur bevindt, geniet het echter de voorkeur dat de container direct op de uiteindelijke verzendlocatie beschikbaar is.

    - **Werksjabloon**: selecteer de werksjabloon die moet worden toegepast wanneer werk voor de container wordt aangemaakt. Dit veld is alleen beschikbaar wanneer het veld **Containervrijgavebeleid** is ingesteld op *Werk aanmaken om container te verplaatsen van inpakstation* en is gerelateerd aan een werkordertype met de naam *Orderverzameling voor ingepakte container*. Raadpleeg [Werksjablonen en locatie-instructies](control-warehouse-location-directives.md) voor meer informatie.

    In de resterende stappen configureert u instellingen die betrekking hebben op *manifesteren*. Manifesteren is het proces waarbij het gewicht van een container, containergroep of zending wordt opgegeven, samen met de tracking-ID die wordt ontvangen van een transportprovider. Dynamics 365 Supply Chain Management integreert niet met systemen van externe transportproviders. In plaats daarvan moeten magazijnmedewerkers etiketten afdrukken die zijn ontvangen van de transportprovider en vervolgens een tracking-nummer scannen wanneer ze de manifesteringsprocedure uitvoeren.

    Aangezien de vereisten voor manifests van klant tot klant en zelfs van zending tot zending verschillen, zorgt verpakkingsbeleid voor aanzienlijke flexibiliteit in de workflow. U kunt manifests in elke combinatie instellen voor containers, containergroepen en zendingen.

    Als u een manifestprocedure met meerdere niveau's gebruikt, moeten werknemers alle containers manifesteren voordat ze de gerelateerde containergroep manifesteren; ook moeten alle containergroepen worden gemanifesteerd voordat de gerelateerde zending wordt gemanifesteerd

1. Stel op het sneltabblad **Containermanifest** de volgende velden in:

    - **Automatisch manifest bij containersluiting**: stel deze optie in op *Ja* om de manifestinformatie toe te passen als onderdeel van van het containersluitingsproces. Als u transportintegratie niet gebruikt, moet de informatie handmatig worden vastgelegd.
    - **Manifestvereisten voor container**: selecteer een van de volgende opties:

        - *Geen*: er wordt geen manifestproces gebruikt.
        - *Handmatig*: er is een manifest vereist voor de inpakworkflow. Een container kan pas worden gesloten of vrijgegeven wanneer het manifesteren is voltooid.
        - *Transportbeheer*: het manifest wordt uitgevoerd via tarief-engines van transportbeheer (TMS). Omdat voor deze optie aangepaste ontwikkeling vereist is om een specifieke engine te implementeren voor de transportprovider, werkt deze niet vanzelf in de huidige versie.

    - **Inhoud container afdrukken**: stel deze optie in op *Ja* om het rapport met de inhoud van de container automatisch af te drukken wanneer een container wordt geregistreerd als afgesloten. Het rapport kan ook op aanvraag worden afgedrukt.

1. Selecteer op het sneltabblad **Manifest voor containergroep** voor het veld **Vereisten manifest voor containergroep** een van de volgende opties:

    - *Geen*: het manifest van de containergroep wordt niet opgenomen als een vereiste in de inpakworkflow.
    - *Handmatig*: het manifest van de containergroep zal worden opgenomen als een vereiste in de inpakworkflow. Alle containers die in de groep zijn opgenomen, moeten worden afgesloten voordat voor de containergroep een manifest kan worden gemaakt. Selecteer deze optie als u verplicht bent om een manifest in te vullen voor elke containergroep die op het inpakstation is ingepakt. U selecteert deze optie doorgaans als containers op een pallet worden geplaatst en een manifest wordt gemaakt voor de gehele pallet.

    > [!NOTE]
    > De huidige versie biedt geen ondersteuning voor manifestrapporten voor containergroepen en er is geen ondersteuning voor een TMS-engine voor containergroepen.

1. Stel op het sneltabblad **Manifest zending** de volgende velden in:

    - **Manifestvereisten voor zending**: selecteer een van de volgende opties:

        - *Geen*: het manifest van de zending wordt niet opgenomen als een vereiste in de inpakworkflow.
        - *Handmatig*: het manifest van de zending zal worden opgenomen als een vereiste in de inpakworkflow. Er kunnen geen containers voor een zending worden vrijgegeven totdat het maken van het manifest is voltooid.
        - *Transportbeheer*: het maken van het manifest wordt uitgevoerd via tarief-engines van transportbeheer (TMS). Omdat voor deze optie aangepaste ontwikkeling vereist is om een specifieke engine te implementeren voor de transportprovider, werkt deze niet vanzelf in de huidige versie.

        Manifest voor zendingen moet zijn ingeschakeld als u een manifest moet maken voor de volledige zending die op het inpakstation wordt verpakt. Deze optie wordt meestal gebruikt wanneer één geconsolideerd manifest vereist is, zelfs als de zending uit meerdere containers of containergroepen bestaat.

    - **Pakbon afdrukken**: stel deze optie in op *Ja* als u de pakbon automatisch wilt afdrukken als onderdeel van het manifest van de zending. De pakbon kan ook op aanvraag worden afgedrukt.

### <a name="set-up-container-types"></a>Containertypen instellen

Tijdens het handmatige inpakproces moeten containers worden aangemaakt voordat artikelen in de containers kunnen worden ingepakt. Elke container moet zijn gebaseerd op een *containertype*, waarmee de maximale fysieke volume- en gewichtcapaciteit van een container worden bepaald.

Ga als volgt te werk om een containertype aan te maken.

1. Ga naar **Magazijnbeheer \> Instellingen \> Containers \> Containertypen**.
1. Selecteer in het deelvenster Actie de optie **Nieuw** om een containertype toe te voegen.
1. Stel de volgende velden in voor het nieuwe containertype:

    - **Code containertype**: geef een unieke ID voor het containertype op.
    - **Beschrijving**: voer een beschrijving van het nieuwe containertype in.
    - **Tarragewicht**: voer het werkelijke of geschatte gewicht van de container in.
    - **Maximum nettogewicht**: voer het maximale gewicht dat de container kan bevatten.

1. Voer in het gedeelte **Containerdimensies** de velden **Lengte**, **Breedte**, **Hoogte** en **Volume** de fysieke dimensies van de container zelf in.
1. Voer in het gedeelte **Maxima** in de velden **Lengte**, **Breedte**, **Hoogte** en **Volume** de maximale fysieke dimensies in die de container aankan.
1. U kunt extra kenmerken definiëren voor containertypen die zijn gekoppeld aan andere bewerkingen die containers gebruiken. Raadpleeg [Containerisatie](wave-containerization.md) voor meer informatie.

> [!NOTE]
> Voor het handmatige inpakproces gebruikt het systeem uitsluitend de waarde van de velden **Maximum nettogewicht** en **Volume** in het gedeelte **Maxima**.

### <a name="set-up-packing-profiles"></a>Verpakkingsprofielen instellen

*Verpakkingsprofielen* zijn vereist voor het verpakkingsproces. Deze kunnen standaard worden geselecteerd of ingesteld wanneer u een verpakkingsbewerking start op de pagina **Verpakken**.

Voer de volgende stappen uit om een verpakkingsprofiel in te stellen.

1. Ga naar **Magazijnbeheer \> Instellingen \> Verpakking \> Verpakkingsprofielen**.
1. Selecteer een bestaand profiel in het deelvenster met lijsten of selecteer **Nieuw** in het deelvenster met acties om een nieuw profiel aan te maken.
1. Stel in de koptekst van het nieuwe of geselecteerde profiel de volgende velden in:

    - **ID verpakkingsprofiel**: voer een kort ID in voor het profiel.
    - **Beschrijving**: voer een beschrijving van het verpakkingsprofiel in.
    - **Containerverpakkingsbeleid** : selecteer het verpakkingsbeleid dat van toepassing is op het profiel. Raadpleeg het gedeelte [Containerverpakkingsbeleid instellen](#packing-policy) eerder in dit artikel voor meer informatie.
    - **Modus container-ID**: selecteer of er automatisch een container-ID moet worden gegenereerd wanneer een container wordt aangemaakt of dit handmatig moet gebeuren.
    - **Containertype**: selecteer het containertype dat standaard moet worden gebruikt wanneer een nieuwe container wordt aangemaakt.
    - **Automatisch container aanmaken bij afsluiten container**: schakel dit selectievakje in om automatisch een nieuwe container aan te maken als de vorige container is afgesloten en er een of meer regels resteren voor de huidige zending.

### <a name="set-up-warehouse-workers"></a>Magazijnmedewerkers instellen

Elke gebruiker of werknemer die containers verpakt met behulp van de pagina **Verpakkingen** van de webclient of de activiteitencode *Verpakken* in de mobiele app Magazijnbeheer, moet een gebruikersaccount hebben dat is gekoppeld aan een *werknemers-/persoons-* record waaraan de vereiste toegangsrechten zijn toegewezen. (Raadpleeg [Nieuwe gebruikers aanmaken](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md) voor meer informatie over het instellen van gebruikers.)

Volg deze stappen om een *werknemers-/persoons* record in te stellen voor het verpakkingsproces.

1. Ga naar **Warehouse Management \> Instellen \> Medewerker**.
1. Selecteer in het deelvenster Actie **Nieuw** om een werkgebruiker toe te voegen.
1. Stel het veld **Medewerker** in op het bestaande werknemersrecord dat is gedefinieerd in de module **Human Resources** voor de gebruiker die het verpakkingsproces zal voltooien.
1. Stel op het sneltabblad **Profiel** de volgende velden in:

    - **Containerverpakkingsbeleid**: selecteer een containerverpakkingsbeleid dat bepaalt hoe containers op het inpakstation moeten worden verwerkt. Het containerverpakkingsbeleid dat u selecteert, wordt vooraf geselecteerd voor de medewerker wanneer deze het inpakstation opent. Raadpleeg de volgende blogpost voor meer informatie: [Verbeterde inpakfunctionaliteit](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611) voor meer informatie.
    - **ID verpakkingsprofiel**: selecteer een ID verpakkingsprofiel waarmee het verpakkingsbeleid en de containerinstellingen worden gedefinieerd die moeten worden gebruikt. Als de geselecteerde ID verpakkingsprofiel is gekoppeld aan een containerverpakkingsbeleid, kunt u de instelling van het veld **Containerverpakkingsbeleid** op deze pagina niet wijzigen.

1. Selecteer op het sneltabblad **Standaard inpakstation** de standaardsite, -magazijn en -locatie die op de werknemer van toepassing zijn.
1. Als de werknemer de mobiele app Magazijnbeheer zal gebruiken om het containerverpakkingswerk te beheren en te registreren, stel dan op het sneltabblad **Gebruikers** een of meer accounts in die de werknemer kan gebruiken om zich aan te melden bij de app. Raadpleeg [Gebruikersaccounts voor mobiele apparaten](mobile-device-work-users.md) voor meer informatie.

## <a name="example-scenario"></a><a name="scenario"></a>Voorbeeldscenario

In dit gedeelte staat een voorbeeldscenario dat laat zien hoe u een order aanmaakt en de artikelen inpakt.

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt dit scenario ook gebruiken als instructie voor het gebruiken van de functie in een productiesysteem. In dat geval moet u echter uw eigen waarden opgeven voor elke instelling die hier wordt beschreven.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Meld u aan als een gebruiker die verpakkingswerk kan doen

Meld u aan bij Supply Chain Management door een gebruikersaccount te gebruiken dat over de machtigingen beschikt die vereist zijn om containers in te pakken. De gebruiker *Julia Funderburk* is opgenomen als onderdeel van de demonstratiegegevens en beschikt over de vereiste machtigingen. Deze gebruiker heeft de gebruikers-ID *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Maak een verkooporder aan en voltooi het werk

Volg deze stappen om een verkooporder aan te maken en voltooi het werk van het verplaatsen van de bestelde artikelen naar het inpakstation.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde *US-005*.
1. Selecteer **OK** om het dialoogvenster te sluiten.
1. De nieuwe verkooporder wordt geopend en bevat één lege regel op het sneltabblad **Verkooporderregels**. Stel voor de nieuwe orderregel de volgende waarden in:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *2*
    - **Locatie:** *6*
    - **Magazijn:** *62*

1. Selecteer, met de orderregel nog geselecteerd, in de werkbalk van het sneltabblad **Verkooporderregels** **Voorraad \> Reservering**.
1. Selecteer op de pagina **Reservering** in het actievenster de optie **Partij reserveren** om de volledige hoeveelheid van de geselecteerde regel te reserveren in het magazijn.
1. Sluit de pagina **Reservering** om terug te keren naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

    Er wordt een bericht getoond met daarin zendings- en wave-ID's voor de order.

1. Selecteer, met de orderregel nog geselecteerd, in de werkbalk van het sneltabblad **Verkooporderregels** **Magazijn** \> **Werkgegevens**. Als u batchverwerking gebruikt om uw waves uit te voeren, moet u misschien even wachten tot het werk is aangemaakt.
1. Selecteer in het deelvenster Actie van de pagina **Werk** op het tabblad **Werk** de optie **Werk voltooien**.
1. Stel op de pagina **Werkvoltooiing** het veld **Gebruikers-ID** in op *62*.
1. Selecteer in het deelvenster Actie **Werk valideren**.
1. Wanneer u een bericht ontvangt waarin wordt aangegeven dat uw werk geldig is, selecteer dan **Werk voltooien** om het proces van verzamelen van de voorraadartikelen en het plaatsen ervan in de locatie voor *Verpakken* te voltooien.
1. Noteer de waarde voor **Zending-ID** die voor het werk wordt getoond in het bovenste raster.

### <a name="pack-the-ordered-items-into-a-container"></a>Pak de bestelde artikelen in een container in

De voorraadartikelen zijn nu naar het verpakkingsgebied gebracht en kunnen worden verpakt in containers. Voer de volgende stappen uit om een nieuwe container in het systeem aan te maken en deze in te pakken.

1. Ga naar **Magazijnbeheer \> Verpakking en containervorming \> Verpakken**.
1. Stel in het dialoogvenster **Inpakstation selecteren** de volgende waarden in:

    - **Locatie:** *6*
    - **Magazijn:** *62*
    - **Locatie:** *Verpakken*
    - **ID verpakkingsprofiel:** *WH62*

1. Selecteer **OK**.
1. Voer op de pagina **Verpakken** in het veld **Nummerplaat of zending** de zending-ID in die eerder is genoteerd. Op het sneltabblad **Open regels** moeten nu de resterende nog niet ingegepakte artikelen zichtbaar zijn.
1. Selecteer in het deelvenster Actie de optie **Nieuwe container** om een container aan te maken in het systeem.
1. Stel in het dialoogvenster **ID van de nieuwe container** het veld **Containertype** in op *SmallBox*.
1. Selecteer **OK** om de container aan te maken.
1. Selecteer **OK** om terug te gaan naar de pagina **Verpakken**. Op het sneltabblad **Open containers** wordt nu de waarde getoond van de **Container-ID** van de container die is aangemaakt.
1. In dit scenario verpakt u op dit moment slechts een van de bestelde artikelen. Stel daarvoor op het sneltabblad **Artikel verpakken** de volgende waarden in:

    - **Hoeveelheid:** *1.00*
    - **ID:** *A0001*

    Onmiddellijk nadat u de waarde voor **ID** is geselecteerd, werkt de pagina de sneltabbladen **Open regels** en **Alle regels** bij om aan te geven dat één artikel is ingepakt. U moet nu een van de twee stuks van artikel *A0001* hebben ingepakt.

1. Selecteer **Container sluiten** in het actievenster.
1. Selecteer in het dialoogvenster **Container sluiten** de optie **Systeemgewicht ophalen** om de standaardwaarde voor **Brutogewicht** in te vullen.
1. Selecteer **OK** om de container te sluiten.

> [!TIP]
> Containers kunnen op basis van de context op verschillende manieren worden bekeken. Wanneer u bijvoorbeeld een zending verpakt, is het vaak handig om ofwel containers weer te geven die deel uitmaken van de zending ofwel alle containers die fysiek op een inpakstation aanwezig zijn. De pagina **Inpakstation** bevat knoppen waarmee alle geopende en afgesloten containers op een inpakstation kunnen worden weergeven. Deze weergaven zijn niet beperkt tot een specifieke zending. Ze kunnen nuttig zijn wanneer bijvoorbeeld één werknemer een container aan het inpakken is en een andere werknemer bezig is met het manifest en de vrijgave van de container.
>
> Ook is een geconsolideerde weergave van alle containers beschikbaar. Deze weergave is het meest handig voor gebruikers die buiten de context van één inpakstation werken. Ga naar **Magazijnbeheer \> Verpakking en containerisatie \> Containers** om deze weergave te zien.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
