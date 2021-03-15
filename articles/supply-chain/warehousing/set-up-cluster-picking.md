---
title: Clusterverzameling instellen
description: In dit onderwerp wordt beschreven hoe u clusterverzameling instelt en hoe u van artikelbevestiging toepast met clusterverzameling.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da11a474e1bb031fac26e04c91cbdbab5f62eb0b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977348"
---
# <a name="set-up-cluster-picking"></a>Clusterverzameling instellen

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u werknemers in staat kunt stellen hun mobiel apparaat te gebruiken om verzamelwerk te groeperen in clusters zodat ze artikelen van één locatie kunnen verzamelen voor meerdere werkorders tegelijkertijd. Dit wordt *clusterverzameling* genoemd.

## <a name="about-cluster-picking"></a>Over clusterverzameling

Nadat werkorders worden vrijgegeven aan het magazijn, kan de werknemer een mobiel apparaat gebruiken om de orders toe te wijzen aan een cluster. De cluster zal het verzamelwerk organiseren voor de werknemer. Wanneer een werkorder wordt toegewezen aan een cluster, moet de werknemer clusterverzameling gebruiken om het verzamelwerk voor de order uit te voeren. De werknemer kan geen andere verzamelmethodes gebruiken. Als een werkorder per ongeluk wordt toegewezen aan een cluster, moet de werknemer de cluster opbreken en opnieuw maken.

Indien nodig kan een werknemer een cluster doorgeven aan een andere werknemer. Dit verandert de clusterstatus naar Doorgegeven. Wanneer de medewerker een mobiel apparaat gebruikt om aan te geven dat het picken en opslaan is voltooid, moet de zending of lading worden bevestigd in de client.

## <a name="enable-cluster-picking"></a>Clusterverzameling inschakelen

U moet het volgende instellen om clusterverzameling in te schakelen:

- **Clusterprofielen**: geef aan of cluster-id's automatisch moeten worden gegenereerd, hoeveel posities moeten worden gebruikt, wanneer clusters moeten worden opgebroken, wat de volgorde is van het verzamelwerk en hoe dit wordt gecontroleerd.

- **Werksjablonen**: definieer hoe het verzamelwerk voor clusterverzameling moet worden gemaakt.

- **Locatie-instructies**: geef op waaruit artikelen moeten worden verzameld en waar deze moeten worden geplaatst.

- **Menuopties voor mobiel apparaat**: configureer een menu voor een mobiel apparaat om bestaand werk te gebruiken dat wordt geleid door clusterverzameling. U moet vervolgens het menuartikel toevoegen aan een menu voor een mobiel apparaat zodat het wordt weergegeven op mobiele apparaten.

- **Parameters voor magazijnbeheer**: geef de te gebruiken nummervolgorde op als u id's voor clusters wilt genereren.

## <a name="set-up-a-cluster-profile"></a>Een clusterprofiel instellen

Ga als volgt te werk om een clusterprofiel in te stellen:

1. Klik op **Magazijnbeheer** \> **Instellen** \> **Mobiel apparaat** \> **Clusterprofielen**.

1. Klik op **Nieuw** om een nieuwe profiel te maken.

1. Klik op **Cluster maken** en klik onder **Cluster sorteren** op **Nieuw** om de sorteercriteria voor het cluster in te stellen. De rangschikkingscriteria bepalen de volgorde waarin de werknemer het verzamelwerk zal uitvoeren. U kunt zoveel criteria toevoegen als nodig zijn.

1. Voer in het veld **Volgnummer** een cijfer in om te bepalen in welke volgorde de sorteercriteria worden verwerkt.

1. Selecteer in het veld **Veldnaam** het veld dat de rangschikking zal bepalen. Als u bijvoorbeeld het veld **WMSLocationId** selecteert, zal het werk worden gerangschikt volgens locatie.

1. Selecteer een van de volgende opties in het veld **Sorteren**.

| **Optie**     | **Beschrijving**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Oplopend**  | Verzamelwerk wordt in oplopende volgorde geplaatst op basis van de rangschikkingscriteria Als u bijvoorbeeld het veld **WMSLocationId** gebruikt als rangschikkingscriteria en uw locatie-id's zijn 1, 2, 3 en 4, zult u eerst verzamelen vanaf locatie 4. |
| **Aflopend** | Verzamelwerk wordt in een aflopende volgorde geplaatst op basis van de rangschikkingscriteria. Als u bijvoorbeeld het veld **WMSLocationId** gebruikt als rangschikkingscriteria en uw locatie-id's zijn 1, 2, 3 en 4, zult u eerst verzamelen vanaf locatie 1. |

## <a name="item-confirmation"></a>Artikelbevestiging

Wanneer clusterverzameling wordt toegepast, is artikelbevestiging van groot belang om de artikelen te controleren die aan clusters worden toegevoegd. U kunt artikelen in clusterverzameling controleren tijdens het clusterverzamelingsproces. De instelling is gebaseerd op de instelling voor productstreepjescodes.

### <a name="set-up-item-verification-with-cluster-picking"></a>Artikelverificatie met clusterverzameling instellen

1. Open op een menu-item voor mobiele apparaten het instellingsformulier voor werkbevestiging: **Magazijnbeheer** \> **Magazijnbeheer** \> **Instellingen** \> **Mobiel apparaat** \> **Menuopties voor mobiel apparaat**.

1. Open in de menuoptie voor het mobiele apparaat **Werkbevestigingsinstellingen**. Met de optie **Productbevestiging** kunt u elk stuk van de voorraad tijdens het scannen vanaf het mobiele apparaat controleren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]