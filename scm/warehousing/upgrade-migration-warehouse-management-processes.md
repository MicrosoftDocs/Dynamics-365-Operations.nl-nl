---
title: Migreren van AX 2012 naar Finance and Operations
description: In dit artikel vindt u een overzicht van de opties voor migratie van product- en magazijnbeheer in Dynamics 365 voor Finance and Operations.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cacf48bc10be5c06154816c2f9951ab4bbaee1c1
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="migrate-from-ax-2012-to-finance-and-operations"></a>Migreren van AX 2012 naar Finance and Operations

In dit onderwerp vindt u een overzicht van de opties voor migratie van product- en magazijnbeheer in Microsoft Dynamics 365 voor Finance and Operations, Enterprise Edition.

<a name="introduction"></a>Introductie
------------

Tijdens een upgrade naar Finance and Operations worden producten geblokkeerd, als ze zijn gekoppeld aan een opslagdimensiegroep met instellingen die niet overeenkomen met de vereisten voor opslagdimensiegroepinstellingen in Finance and Operations. Na de upgrade kunt u echter met een reeks migratieopties in het proces **Opslagdimensiegroep voor artikelen wijzigen** producten deblokkeren die tijdens de upgrade zijn geblokkeerd. Vervolgens kunt u transacties voor die producten verwerken. Sommige van deze artikelen zijn mogelijk al gekoppeld aan de opslagdimensiegroepen waarvoor de voorraaddimensies Vestiging, Magazijn en Locatie actief zijn en fysiek worden bijgehouden. In dit geval kunt u met het proces **Opslagdimensiegroep voor artikelen wijzigen** die artikelen inschakelen die u wilt gebruiken in magazijnbeheersprocessen. Deze functie is handig als u de functionaliteit voor magazijnbeheer wilt gebruiken voor bestaande artikelen.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Upgraden naar Finance and Operations wanneer AX 2012 R3 WMSII wordt gebruikt
Finance and Operations ondersteunt niet meer de verouderde module **WMSII** van Microsoft Dynamics AX 2012. In plaats daarvan kunt u de nieuwe module **Magazijnbeheer** gebruiken. In vorige versies konden de voorraaddimensies Locatie en Pallet-ID worden geselecteerd voor de financiële voorraad. Als onderdeel van het upgradeproces kan echter de voorraaddimensie Pallet-ID niet langer worden ingeschakeld voor de financiële voorraad. Alle producten die zijn gekoppeld aan een opslagdimensiegroep die gebruik maakt van de voorraaddimensie Pallet-ID, worden geblokkeerd en niet verwerkt.

### <a name="enabling-items-in-finance-and-operations"></a>Artikelen in inschakelen in Finance and Operations

In Finance and Operations moeten artikelen die worden gebruikt als onderdeel van magazijnbeheerprocessen worden gekoppeld aan een opslagdimensie waarvoor de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd. Als deze instelling is ingeschakeld, worden de voorraaddimensies Vestiging, Magazijn, Voorraadstatus, Locatie en Nummerplaat actief. U kunt alleen artikelen op dit type opslagdimensiegroep instellen die al zijn gekoppeld aan opslagdimensiegroepen waarvoor de voorraaddimensie Locatie actief is.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Artikelen die zijn geblokkeerd voor voorraadupdates

Om de lijst weer te geven van vrijgegeven producten die tijdens de upgrade zijn geblokkeerd en niet kunnen worden verwerkt, klikt u op **Voorraadbeheer** &gt; **Instellingen** &gt; **Voorraad** &gt; **Artikelen die zijn geblokkeerd voor voorraadupdates**.

### <a name="reapplying-blocked-products"></a>Geblokkeerde producten opnieuw toepassen

Als u producten wilt deblokkeren die tijdens de upgrade zijn geblokkeerd, moet u een nieuwe opslagdimensiegroep voor deze producten selecteren. Merk op dat u de opslagdimensiegroep zelfs kunt wijzigen als er openstaande voorraadtransacties bestaan. Om artikelen te gebruiken die tijdens de upgrade zijn geblokkeerd, hebt u twee mogelijkheden:

-   Wijzig de opslagdimensiegroep voor het artikel naar een opslagdimensiegroep die alleen de voorraaddimensies Vestiging, Magazijn en Locatie gebruikt. Als gevolg hiervan wordt de voorraaddimensie Pallet-ID niet meer gebruikt.
-   Wijzig de opslagdimensiegroep voor het artikel naar een opslagdimensiegroep die de magazijnbeheerprocessen gebruikt. Als gevolg hiervan wordt nu de voorraaddimensie Nummerplaat gebruikt.

### <a name="migration-processes"></a>Migratieprocessen

In Finance and Operations maakt traceren van artikelen deel uit van de magazijnbeheerprocessen. Voor deze processen moeten alle magazijnen en hun locaties worden gekoppeld aan een locatieprofiel. Conceptueel geldt dat als u magazijnbeheerprocessen wilt gebruiken, twee processen moeten worden verwerkt:

-   Bestaande magazijnen moet ingeschakeld zijn voor gebruik van magazijnbeheerprocessen.
-   Bestaande vrijgegeven producten moeten gekoppeld zijn aan een nieuwe opslagdimensiegroep die magazijnbeheerprocessen gebruikt.

Als de bronopslagdimensiegroepen de voorraaddimensie Pallet-ID gebruiken, moeten de locaties van bestaande voorhanden voorraad die de voorraaddimensie Pallet-ID gebruiken, zijn gekoppeld aan een locatieprofiel waarvoor de parameter **Bijhouden nummerplaat gebruiken** is geselecteerd. Als u de bestaande magazijnen niet wilt inschakelen voor gebruik van magazijnbeheerprocessen, kunt u de opslagdimensiegroepen van de bestaande voorhanden voorraad wijzigen naar groepen die alleen de voorraaddimensies Vestiging, Magazijn en Locatie gebruiken.

### <a name="using-the-warehouse-management-processes"></a>De magazijnbeheerprocessen gebruiken

Voordat u vrijgegeven producten in de module **Magazijnbeheer** kunt gebruiken, moeten de producten een opslagdimensiegroep gebruiken waarvoor de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Magazijnen inschakelen voor gebruik van magazijnbeheerprocessen

1.  Maak tenminste één nieuw locatieprofiel.
2.  Klik op **Magazijnbeheer** &gt; **Instellingen** &gt; **Magazijnbeheerprocessen inschakelen** &gt; **Magazijninstellingen inschakelen**.
3.  Op de pagina **Magazijninstellingen inschakelen** voegt u de magazijnen toe die u wilt inschakelen. U kunt deze stap rechtstreeks op de pagina uitvoeren of door middel van de integratie met Microsoft Office.
4.  Wijs een locatieprofiel toe aan alle locaties. U kunt deze stap eenvoudig uitvoeren door middel van de integratie met Microsoft Office rechtstreeks vanaf de pagina. U kunt de gegevens exporteren en importeren, of de entiteit voor gegevensverwerking in [Gegevensbeheer](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities) gebruiken.
5.  Valideer de wijzigingen. Als onderdeel van het validatieproces worden verschillende validaties van gegevensintegriteit uitgevoerd. Als onderdeel van een groter upgradeproces moeten mogelijk problemen die optreden worden gecorrigeerd in de bron-implementatie. In dit geval is een aanvullende gegevensupgrade vereist.
6.  Verwerk de wijzigingen.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Wijzig de opslagdimensiegroep voor het artikel, zodat het gebruik maakt van magazijnbeheerprocessen

1.  Maak een nieuwe waarde aan voor **Voorraadstatus** en wijs deze toe als de **Standaardvoorraadstatus-id** in de instellingen **Parameters voor magazijnbeheer**.
2.  Maak een nieuwe opslagdimensiegroep aan waarin de parameter **Magazijnbeheerprocessen gebruiken** is geselecteerd.
3.  Definieer op de pagina **Reserveringshiërarchie** een nieuwe reserveringshiërarchie op basis van de opslag- en traceringsdimensiegroepen van het artikel.
4.  Maak een of meer eenheidvolgordegroepen die ten minste dezelfde eenheden bevatten die worden gebruikt voor de voorraadeenheden van het artikel.
5.  Klik op **Magazijnbeheer** &gt; **Instellingen** &gt; **Magazijnbeheerprocessen inschakelen** &gt; **Opslagdimensiegroep voor artikelen wijzigen**.
6.  Voeg op de pagina **Opslagdimensiegroep voor artikelen wijzigen** de artikelnummers, opslagdimensiegroepen en eenheidvolgordegroepen toe. U kunt deze stap rechtstreeks op de pagina uitvoeren met behulp van de Microsoft Office-integratie of door middel van het gegevensentiteitsproces in [Gegevensbeheer](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities).
7.  Valideer de wijzigingen. Als onderdeel van het validatieproces worden verschillende validaties van gegevensintegriteit uitgevoerd. Als onderdeel van een groter upgradeproces moeten mogelijk problemen die optreden worden gecorrigeerd in de bron-implementatie. In dit geval is een aanvullende gegevensupgrade vereist.
8.  Verwerk de wijzigingen. Het bijwerken van alle voorraaddimensies kan even duren. U kunt de voortgang controleren met behulp van de taken voor batchtaken.



