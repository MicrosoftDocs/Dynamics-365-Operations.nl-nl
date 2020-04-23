---
title: Upgrade van magazijnbeheer van Microsoft Dynamics AX 2012 naar Supply Chain Management
description: Dit onderwerp biedt een overzicht van opties voor het migreren van product- en magazijnbeheer.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 123be2430f910dfbea438cb6a51be7203eb39fc8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216661"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Upgrade van magazijnbeheer van Microsoft Dynamics AX 2012 naar Supply Chain Management 


[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van het proces voor het upgraden van Microsoft Dynamics AX 2012 R3, waarvoor de module WMSII wordt uitgevoerd, naar Supply Chain Management .

Supply Chain Management ondersteunt de verouderde module **WMSII** van Microsoft Dynamics AX 2012 niet meer. In plaats daarvan kunt u de module **Magazijnbeheer** gebruiken. In de WMSII-module konden de voorraaddimensies Locatie en Pallet-ID worden geselecteerd voor financiële voorraad, maar de voorraaddimensie Pallet-ID kan niet worden gebruikt voor financiële voorraad in Supply Chain Management.

Tijdens een upgrade worden alle producten die zijn gekoppeld aan een opslagdimensiegroep waarbij de voorraaddimensie Pallet-ID wordt geïdentificeerd, gemarkeerd als geblokkeerd en niet verwerkt voor een upgrade.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Bijwerken naar Supply Chain Management wanneer AX 2012 R3 WMSII wordt gebruikt
Na de upgrade kunt u een reeks opties in het formulier **Opslagdimensiegroep voor artikelen wijzigen** gebruiken om producten te deblokkeren die tijdens de upgrade zijn geblokkeerd. Vervolgens kunt u transacties voor deze producten verwerken.

### <a name="enabling-items-in-supply-chain-management"></a>Artikelen inschakelen in Supply Chain Management 
Deze wijziging is vereist omdat in Supply Chain Management traceren van artikelen deel uitmaakt van de magazijnbeheerprocessen. Voor deze processen moeten alle magazijnen en hun locaties worden gekoppeld aan een locatieprofiel. Als u magazijnbeheerprocessen wilt gebruiken, moet het volgende worden geconfigureerd:
-   Bestaande magazijnen moet worden ingeschakeld voor gebruik van magazijnbeheerprocessen 
-   Bestaande vrijgegeven producten moeten worden gekoppeld aan een opslagdimensiegroep die magazijnbeheerprocessen gebruikt 

Als de bronopslagdimensiegroepen de voorraaddimensie Pallet-ID gebruiken, moeten de locaties van bestaande voorhanden voorraad die de voorraaddimensie Pallet-ID gebruikt, zijn gekoppeld aan een locatieprofiel waarin de parameter **Bijhouden nummerplaat gebruiken** is geselecteerd. Als u de bestaande magazijnen niet wilt inschakelen voor gebruik van magazijnbeheerprocessen, kunt u de opslagdimensiegroepen van de bestaande voorhanden voorraad wijzigen naar groepen die alleen de voorraaddimensies Vestiging, Magazijn en Locatie gebruiken. 

> [!NOTE] 
>  U kunt de opslagdimensiegroep wijzigen voor artikelen als er openstaande voorraadtransacties bestaan.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Producten zoeken die zijn geblokkeerd vanwege pallet-ID
Om de lijst weer te geven van vrijgegeven producten die tijdens de upgrade zijn geblokkeerd en niet kunnen worden verwerkt, klikt u op **Voorraadbeheer** &gt; **Instellingen** &gt; **Voorraad** &gt; **Artikelen die zijn geblokkeerd voor voorraadupdates**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Opslagdimensiegroep voor geblokkeerde producten wijzigen 
 
Om te kunnen worden gebruikt als onderdeel van een magazijnbeheerproces moet een artikel worden gekoppeld aan een opslagdimensiegroep waarin de voorraaddimensie Locatie actief is en de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd. Als deze instelling is ingeschakeld, worden de voorraaddimensies Vestiging, Magazijn, Voorraadstatus, Locatie en Nummerplaat actief.

Als u producten wilt deblokkeren die tijdens de upgrade zijn geblokkeerd, moet u een nieuwe opslagdimensiegroep voor deze producten selecteren. Merk op dat u de opslagdimensiegroep zelfs kunt wijzigen als er openstaande voorraadtransacties bestaan. Om artikelen te gebruiken die tijdens de upgrade zijn geblokkeerd, hebt u twee mogelijkheden:

-   Wijzig de opslagdimensiegroep voor het artikel naar een opslagdimensiegroep die alleen de voorraaddimensies Vestiging, Magazijn en Locatie gebruikt. Als gevolg hiervan wordt de voorraaddimensie Pallet-ID niet meer gebruikt.
-   Wijzig de opslagdimensiegroep voor het artikel naar een opslagdimensiegroep die de magazijnbeheerprocessen gebruikt. Als gevolg hiervan wordt nu de voorraaddimensie Nummerplaat gebruikt.

## <a name="configure-warehouse-management-processes"></a>Magazijnbeheerprocessen configureren
Voordat u vrijgegeven producten in de module **Magazijnbeheer** kunt gebruiken, moeten de producten een opslagdimensiegroep gebruiken waarvoor de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Magazijnen inschakelen voor gebruik van magazijnbeheerprocessen

1.  Maak tenminste één nieuw locatieprofiel.
2.  Klik op **Magazijnbeheer** &gt; **Instellingen** &gt; **Magazijnbeheerprocessen inschakelen** &gt; **Magazijninstellingen inschakelen**.
3.  Op de pagina **Magazijninstellingen inschakelen** voegt u de magazijnen toe die u wilt inschakelen. U kunt deze stap rechtstreeks op de pagina uitvoeren of door middel van de integratie met Microsoft Office.
4.  Wijs een locatieprofiel toe aan alle locaties. U kunt deze stap eenvoudig uitvoeren door middel van de integratie met Microsoft Office rechtstreeks vanaf de pagina. U kunt de gegevens exporteren en importeren, of de entiteit voor gegevensverwerking in [Gegevensbeheer](../../dev-itpro/data-entities/data-entities.md) gebruiken.
5.  Valideer de wijzigingen. Als onderdeel van het validatieproces worden verschillende validaties van gegevensintegriteit uitgevoerd. Als onderdeel van een groter upgradeproces moeten mogelijk problemen die optreden worden gecorrigeerd in de bron-implementatie. In dit geval is een aanvullende gegevensupgrade vereist.
6.  Verwerk de wijzigingen.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Wijzig de opslagdimensiegroep voor het artikel, zodat het gebruik maakt van magazijnbeheerprocessen

1.  Maak een nieuwe waarde aan voor **Voorraadstatus** en wijs deze toe als de **Standaardvoorraadstatus-id** in de instellingen **Parameters voor magazijnbeheer**.
2.  Maak een nieuwe opslagdimensiegroep aan waarin de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd.
3.  Definieer op de pagina **Reserveringshiërarchie** een nieuwe reserveringshiërarchie op basis van de opslag- en traceringsdimensiegroepen van het artikel.
4.  Maak een of meer eenheidvolgordegroepen die ten minste dezelfde eenheden bevatten die worden gebruikt voor de voorraadeenheden van het artikel.
5.  Klik op **Magazijnbeheer** &gt; **Instellingen** &gt; **Magazijnbeheerprocessen inschakelen** &gt; **Opslagdimensiegroep voor artikelen wijzigen**.
6.  Voeg op de pagina **Opslagdimensiegroep voor artikelen wijzigen** de artikelnummers, opslagdimensiegroepen en eenheidvolgordegroepen toe. U kunt deze stap rechtstreeks op de pagina uitvoeren met behulp van de Microsoft Office-integratie of door middel van het gegevensentiteitsproces in [Gegevensbeheer](../../dev-itpro/data-entities/data-entities.md).
7.  Valideer de wijzigingen. Als onderdeel van het validatieproces worden verschillende validaties van gegevensintegriteit uitgevoerd. Als onderdeel van een groter upgradeproces moeten mogelijk problemen die optreden worden gecorrigeerd in de bron-implementatie. In dit geval is een aanvullende gegevensupgrade vereist.
8.  Verwerk de wijzigingen. Het bijwerken van alle voorraaddimensies kan even duren. U kunt de voortgang controleren met behulp van de taken voor batchtaken.
