---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458753"
---
Bij het kopiëren van een database tussen omgevingen moet u het inrichtingshulpprogramma voor de omgeving opnieuw uitvoeren voordat de gekopieerde database volledig functioneel is, om ervoor te zorgen dat alle Commerce-onderdelen bijgewerkt zijn.

> [!IMPORTANT]
> We raden u aan deze procedure uit te voeren, ongeacht of u Commerce-onderdelen gebruikt of niet, omdat Commerce-functionaliteit is opgenomen in alle omgevingen. 

Voordat u doorgaat, moet u controleren of aan de volgende vereisten wordt voldaan:
1. Als u een upgrade uitvoert naar release 7.2.11792.56024 van juli 2017 (ook bekend als 7.2), past u de volgende X++-toepassingshotfixes toe in de doelomgeving voordat u de gegevensupgrade in die omgeving uitvoert. Hiermee wordt voorkomen dat verschillende fouten optreden tijdens de gegevensupgrade:

    - KB 4036156 - kleine versie-upgrade voor Retail - 'Nummerreeks variant is niet ingesteld.' Dit hotfix-pakket bevat ook KB 4035399 en KB 4035751. Houd er rekening mee dat u minimaal Platform Update 9 moet hebben om dit pakket te kunnen gebruiken. Als u het niet zeker weet, installeert u de meest recente binaire bestanden.
    
2. Als u een upgrade uitvoert van Microsoft Dynamics AX 2012, installeert u de volgende X++-toepassingshotfixes in de doelomgeving voordat u de gegevensupgrade uitvoert:
    - KB 4033183 - Dynamics AX 2012 R2 of Dynamics AX 2012 R3 pre-CU8 upgrade (niet voor detailhandel) mislukt omdat object niet is gevonden voor dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 - Upgrade van Dynamics AX 2012 R3 naar Microsoft Dynamics 365 for Operations 7.2 mislukt door dubbele index RetailSalesLine op SalesLineIdx.
    - KB 4035490 - Prestatieprobleem met upgradescript voor veld MainAccount van GeneralJournalAccountEntry.


Voer de volgende stappen uit om het hulpprogramma voor het opnieuw inrichten van de omgeving uit te voeren.

1. Selecteer in de bibliotheek voor gedeelde activa de optie **Implementeerbaar softwarepakket**.
2. Download het hulpprogramma voor het opnieuw inrichten van de omgeving.
3. Selecteer in de bibliotheek met activa voor uw project de optie **Implementeerbaar softwarepakket**.
4. Selecteer **Nieuw** om een nieuw pakket te maken.
5. Voer een naam en beschrijving voor het pakket in. U kunt het **hulpprogramma voor het opnieuw inrichten van de omgeving** gebruiken als pakketnaam.
6. Upload het pakket dat u eerder hebt gedownload.
7. Selecteer op de pagina **Omgevingsdetails** voor uw doelomgeving de optie **Onderhouden** > **Updates toepassen**.
8. Selecteer het hulpprogramma voor het opnieuw inrichten van de omgeving dat u eerder hebt geüpload en selecteer vervolgens **Toepassen** om het pakket toe te passen.
9. Controleer de voortgang van de implementatie van het pakket. 

Zie voor meer informatie over het toepassen van een implementeerbaar pakket [Een implementeerbaar pakket toepassen](../deployment/create-apply-deployable-package.md). Zie voor meer informatie over het handmatig toepassen van een implementeerbaar pakket [Een implementeerbaar pakket installeren](../deployment/install-deployable-package.md).
