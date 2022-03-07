---
title: Een activum maken
description: In dit onderwerp wordt beschreven hoe u een activum maakt in Activabeheer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e9c2b81e97a7b08dfdb596fbf6822ac94c7358dccd0b92c0677467dbc0c2e26
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721506"
---
# <a name="create-an-asset"></a>Een activum maken

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt beschreven hoe u een activum maakt in Activabeheer.

1. Klik op **Activabeheer** > **Algemeen** > **activa** > **Alle activa** of **Actieve activa**.
2. Klik op de knop **Nieuw**.
3. Voeg in het dialoogvenster **Activa maken** gegevens in met betrekking tot **Activum** (de activa-id) en de naam van het activum. Selecteer datum en tijd voor het activum in het veld **Geldig vanaf**. Vanaf die datum kunt u het activum op een functionele locatie installeren en het activum verplaatsen en vervangen in een activastructuur.
4. Selecteer in het veld **Type activa** het activumtype voor het activum (verplicht veld). Selecteer indien nodig **Activafabrikant** en **Activamodel** voor het activum. Als er slechts één product is ingesteld, wordt dat product automatisch geselecteerd in het veld **Activafabrikant**. De selecties die beschikbaar zijn in de velden **Activafabrikant** en **Activamodel** zijn afhankelijk van de instellingen in [Activafabrikanten en -modellen](../setup-for-objects/product-and-model.md).
5. In de groep **Bovenliggend activum** is het veld **Activum** standaard leeg. Indien nodig kunt u een bovenliggend activum selecteren en vervolgens worden alle velden in de groep **Bovenliggend activum** automatisch ingevuld.
    >[!NOTE]  
    >Wanneer u een bovenliggend activum selecteert, zijn er twee of drie tabbladen beschikbaar: het tabblad **Mijn activa** bevat activa die zijn gerelateerd aan de functionele locaties waaraan u (de onderhoudsmedewerker die is aangemeld bij het systeem) kan worden toegewezen. Als er geen functionele locaties zijn ingesteld voor een onderhoudsmedewerker in het formulier [Onderhoudsmedewerkers en groepen werknemers](../setup-for-objects/workers-and-worker-groups.md), is het tabblad **Mijn activa** niet zichtbaar. Het tabblad **Actieve activa** bevat een lijst met alle activa met de levenscyclusstatus 'Actief' voor activa. Op het tabblad **Activaweergave** wordt een structuurweergave getoond van functionele locaties en elementen die op die locaties zijn geïnstalleerd.

6. De standaard functionele locatie die u hebt ingesteld, wordt voorgesteld voor het activum in het veld **Activagroep** > **Functionele locatie** . Selecteer indien nodig een andere functionele locatie.

    >[!NOTE]
    >Nadat u een activum hebt gemaakt, kunt u dit op een andere functionele locatie installeren, indien nodig. Alleen activa van het hoogste niveau (activa zonder huidig bovenliggend activum) kunnen op een functionele locatie worden geïnstalleerd. Dit betekent dat u zowel het hoogste niveau als alle onderliggende activa op de geselecteerde functionele locatie installeert. Lees meer over het installeren van activa op functionele locaties in [Inleiding tot functionele locaties](../functional-locations/introduction-to-functional-locations.md).

7. Klik op **OK**.
8. Selecteer het activum in de lijst **Alle activa** en klik op de knop **Bewerken** als u nadere informatie aan het activum wilt toevoegen.

## <a name="general-information"></a>Algemene informatie

De functionele locatie waaraan het activum is gerelateerd, wordt weergegeven in het veld **Functionele locatie**. Als het activum een bovenliggend activum is, wordt het aantal onderliggende activa dat gerelateerd aan het activum weergegeven in het veld **Onderliggende**. Als het activum een subactivum van een bestaand activum is, wordt de id van het bovenliggende activum weergegeven in het veld **Bovenliggend**.

U kunt gegevens in **Activafabrikant** en **Activamodel** voor het activum bewerken. Deze worden gebruikt voor het beheren van reserveonderdelen, alternatieve reserveonderdelen en standaardwaarden voor taaktypen. Raadpleeg [Activafabrikanten en -modellen](../setup-for-objects/product-and-model.md) voor meer informatie. U kunt desgewenst ook informatie over **modeljaar** en **serienummer** toevoegen.

**Huidige levenscyclusstatus** wordt gebruikt om te definiëren of het activum actief of inactief is. Bij het maken van een activum wordt de fase altijd ingesteld op de eerste fase in de activafasegroep. Wanneer u klaar bent om een activum te activeren, klikt u op **Activastatus bijwerken** en selecteert u de levenscyclusstatus die u hebt gedefinieerd als 'activum actief'. Vervolgens klikt u op **OK**.

**Opmerking:** wanneer een activum is ingesteld op 'inactief', is het niet meer mogelijk om werkorders voor het activum te maken. U kunt ook geen preventieve onderhoudstaken plannen voor een inactief activum.

De velden **Serviceniveau** en **Kritieke eigenschap** hebben betrekking op werkorders die voor het activum zijn gemaakt. In de velden worden de waarden voor **Serviceniveau** en **Kritieke eigenschap** weergegeven die zijn berekend voor de huidige instellingen voor het activum. Raadpleeg [Serviceniveaus voor activa](../setup-for-objects/object-priorities.md) en [Typen kritieke eigenschappen van activa](../setup-for-objects/object-criticalities.md) met betrekking tot de instelling van deze waarden.

## <a name="asset"></a>Activum

U kunt een **resource** voor het activum selecteren. De resourceselectie bepaalt welke kalender wordt gebruikt voor de planning van de werkorder. Resourceselectie wordt vaak gebruikt voor vaste activa. Resources en resourcegroepen worden ingesteld in **Organisatiebeheer** > **Resources** > **Resourcegroepen** of **Resources**.

In het veld **Nummer van vaste activa** kunt u een vast activum selecteren dat aan het activum moet worden gekoppeld. Dit is relevant als uw activum is gerelateerd aan een investeringsproject.

- Als het activum is gerelateerd aan een vast activum, kunt u een werkordertype maken dat moet worden gebruikt voor werkorders die betrekking hebben op een investeringsproject. 
- Informatie over vaste activa voor een activum is gerelateerd aan de module **Vaste activa** in Dynamics 365 Supply Chain Management. Dit betekent dat u in **Vaste activa** > **Vaste activa** > **Vasta activa** een overzicht kunt krijgen van de projecten voor Activabeheer die kunnen worden gerelateerd aan een vast activum door het activum in de lijst te selecteren en de inhoud weer te geven in het deelvenster **Verwante informatie** > sectie **Gekoppelde projecten**.


## <a name="details"></a>Details

In het veld **Actief vanaf** wordt de datum weergegeven waarop u de levenscyclusstatus van activa hebt bijgewerkt naar een actieve status (raadpleeg [Levenscyclusstatussen van activa](../setup-for-objects/object-stages.md) met betrekking tot de instellingen van levenscyclusstatussen van activa). Als het activum niet meer actief is en u de levenscyclusstatus van activa hebt bijgewerkt naar een inactieve levenscyclusstatus, wordt de datum waarop het activum inactief is, weergegeven in het veld **Actief tot en met**. U kunt deze datums indien nodig handmatig wijzigen.

Indien nodig kunt u een verwachte datum invoegen voor vervanging van het activum in het veld **Vervangingsdatum**. Een geschatte waarde voor het vervangen van het activum kan worden ingevoegd in het veld **Vervangingswaarde**. Voorbeeld: u kunt vervangingsinformatie gebruiken om deze te vergelijken met de kosten van het onderhouden van een activum en vervolgens een beslissing nemen voor de aanschaf van een nieuw activum als de onderhoudskosten voor het bestaande activum snel toenemen.

## <a name="notes"></a>Opmerkingen

U kunt notities met betrekking tot het activum toevoegen op het sneltabblad **Notities**. Klik op de knop **Tijdstempel toevoegen** voordat u de notitie schrijft als u gebruikersgegevens en een datum/tijdstempel aan de notitie wilt toevoegen.

## <a name="attributes"></a>Kenmerken

Op dit sneltabblad kunt u waarden instellen voor kenmerken van activa. Deze kenmerken kunnen worden gebruikt om eigenschappen of kenmerken te beschrijven die relevant zijn voor het activum, bijvoorbeeld grootte, gewicht of machineconfiguratie.

Klik op **Regel toevoegen** en selecteer het kenmerktype. Voeg vervolgens de **waarde** in voor het kenmerktype in en sla de record op.

>[!NOTE] 
>U kunt een overzicht van kenmerktypen voor activa en hun relatie tot de activa krijgen in **Activakenmerk** en **Overzicht van activakenmerken**. Raadpleeg [Overzicht van activakenmerken](../objects/object-specification-overview.md) voor meer informatie.

## <a name="vendor"></a>Leverancier

Selecteer op het sneltabblad **Leverancier** een leverancierrekening voor het activum. Als er een leveranciersgarantie is verleend, kunt u hier ook garantiegegevens invoegen.

## <a name="address"></a>Adres

Op het sneltabblad **Adres** kunt u het adres van de apparatuur invoegen. Als er geen adres is ingevoegd voor het activum, gebruikt het activum het adres van een bovenliggend activum als het bovenliggende activum een adres heeft. Als er geen adres is gerelateerd aan het activum of aan een van de bovenliggende activa in de activahiërarchie, kan het adres van de functionele locatie waarop het activum is geïnstalleerd, worden gebruikt. Als aan die functionele locatie geen adres is gekoppeld, wordt het adres van de bovenliggende functionele locatie gebruikt voor het activum.

## <a name="asset-management-plans"></a>Plannen voor activabeheer

Onderhoudsplannen worden gebruikt voor het plannen van preventieve onderhoudstaken die met regelmatige tussenpozen worden uitgevoerd op het activum. Op dit sneltabblad kunt u onderhoudsplanregels instellen voor het geselecteerde activum. Er kunnen onderhoudsronden worden ingesteld voor verschillende activa waarop u met regelmatige tussenpozen een soortgelijke taak moet uitvoeren. Op het tabblad **Onderhoudsplannen voor functionele locatie** ziet u de onderhoudsplannen met betrekking tot de functionele locatie waarop het activum is geïnstalleerd.

>[!NOTE]
>Als u een onderhoudsplanregel of een onderhoudsronde met betrekking tot een activum in **Alle activa** verwijdert, verwijdert u ook automatisch alle onderhoudsschema's met de status 'Gemaakt' die zijn gemaakt op basis van dat onderhoudsplan of die onderhoudsronde.

## <a name="functional-location-maintenance-plans"></a>Onderhoudsplannen voor functionele locatie

Op dit sneltabblad krijgt u een overzicht van de onderhoudsplannen die betrekking hebben op de functionele locatie waarop het activum is geïnstalleerd.

## <a name="maintenance-rounds"></a>Onderhoudsronden

Op dit sneltabblad kunt u onderhoudsronden toevoegen of verwijderen die zijn gerelateerd aan het activum.

## <a name="financial-dimensions"></a>Financiële dimensies

U kunt financiële dimensies selecteren voor het activum.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]