---
title: Boekstukken importeren met behulp van de entiteit Algemeen journaal
description: Dit artikel bevat tips voor het importeren van gegevens in het algemeen journaal met behulp van de entiteit Algemeen journaal.
author: rcarlson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5917a047d3098875f3ab95087e761e6428c18b
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135714"
---
# <a name="importing-vouchers-by-using-the-general-journal-entity"></a>Boekstukken importeren met behulp van de entiteit Algemeen journaal

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Dit artikel bevat tips voor het importeren van gegevens in het algemeen journaal met behulp van de entiteit Algemeen journaal.

U kunt de entiteit Algemeen journaal gebruiken om boekstukken te importeren met het rekening- of tegenrekeningtype **Grootboek**, **Klant**, **Leverancier** of **Bank**. U kunt het boekstuk invoeren als één regel, door middel van de velden **Rekening** en **Tegenrekening**, of als een meerregelig boekstuk, waarbij u alleen het veld **Rekening** gebruikt en het veld **Tegenrekening** op elke regel leeg laat. De entiteit Algemeen journaal ondersteunt niet elk rekeningtype. In plaats daarvan bestaan andere entiteiten voor scenario's waarin verschillende combinaties van de rekeningtypen vereist zijn. Als u bijvoorbeeld een projecttransactie wilt importeren, gebruikt u de entiteit Projectonkostenjournaal. Elke entiteit is ontworpen om specifieke scenario's te ondersteunen. Dit betekent dat extra velden mogelijk beschikbaar zijn in entiteiten voor deze scenario's. Het is echter mogelijk dat extra velden niet beschikbaar zijn in entiteiten voor verschillende scenario's.

## <a name="setup"></a>Instelling
Controleer de volgende instellingen voordat u importeert met behulp van de entiteit Algemeen journaal:

- **Instelling nummerreeks voor het journaalbatchnummer** – Standaard gebruikt het journaalbatchnummer de nummerreeks die is gedefinieerd in de parameters van het grootboek als u importeert met behulp van de entiteit Algemeen journaal. Als u de nummerreeks voor het journaalbatchnummer instelt op **Handmatig**, wordt geen standaardnummer toegepast. Deze instelling wordt niet ondersteund.
- **Configuratie van financiële dimensies** – Elke organisatie moet de volgorde van de financiële dimensies definiëren als entiteiten worden gebruikt voor het importeren van transacties. De volgorde is gedefinieerd voor de indeling **Integratie van grootboekdimensies**, bij **Grootboek** &gt; **Rekeningschema** &gt; **Dimensies** &gt; **Configuratie van financiële dimensies voor integrerende toepassingen** &gt; **Gegevensentiteiten selecteren**. De segmenten van de grootboekrekening die is geïmporteerd, moeten dezelfde volgorde hebben. Anders treedt een fout op tijdens het importeren.

## <a name="general-journal-entity-setup"></a>Entiteit Algemeen journaal instellen
Twee instellingen in Gegevensbeheer zijn van invloed op hoe het standaard journaalbatchnummer of boekstuknummer wordt toegepast:

- **Op sets gebaseerde verwerking** (in de gegevensentiteit)
- **Automatisch gegenereerd** (in de veldtoewijzing).

In de volgende secties wordt het effect van deze instellingen beschreven. Tevens wordt uitgelegd hoe batchnummers voor journalen en boekstuknummers worden gegenereerd.

### <a name="journal-batch-number"></a>Batchnummer journaal

- De instelling **Op sets gebaseerde verwerking** in de entiteit Algemeen journaal heeft geen invloed op de manier waarop journaalbatchnummers worden gegenereerd.
- Als het veld **Journaalbatchnummer** is ingesteld op **Automatisch gegenereerd**, wordt een nieuw journaalbatchnummer gemaakt voor elke regel die wordt geïmporteerd. Dit gedrag wordt niet aanbevolen. De instelling **Automatisch gegenereerd** is te vinden in het importproject, onder **Kaart weergeven** op het tabblad **Gegevens toewijzen**.
- Als het veld **Journaalbatchnummer** niet is ingesteld op **Automatisch gegenereerd**, wordt het journaalbatchnummer als volgt gemaakt:

    - Als het journaalbatchnummer dat is gedefinieerd in het geïmporteerde bestand overeenkomt met een bestaand, niet-geboekt dagelijks journaal, worden alle regels met een overeenkomende journaalbatchnummer geïmporteerd in het bestaande journaal. Regels worden nooit in een geboekt journaalbatchnummer geïmporteerd. In plaats daarvan wordt er een nieuw nummer gemaakt.
    - Als het journaalbatchnummer dat is gedefinieerd in het geïmporteerde bestand niet overeenkomt met een bestaand, niet-geboekt dagelijks journaal, worden alle regels met hetzelfde journaalbatchnummer gegroepeerd onder een nieuw journaal. Zo worden bijvoorbeeld alle regels met een journaalbatchnummer van 1 geïmporteerd in een nieuw journaal en worden alle regels met een journaalbatchnummer van 2 geïmporteerd in een tweede nieuw journaal. Het journaalbatchnummer wordt gemaakt met behulp van de nummerreeks die is gedefinieerd in de grootboekparameters.

### <a name="voucher-number"></a>Boekstuknummer

- Als u de instelling **Op sets gebaseerde verwerking** gebruikt in de entiteit Algemeen journaal, moet het boekstuknummer worden opgegeven in het geïmporteerde bestand. Aan elke transactie in het algemeen journaal wordt het boekstuknummer toegewezen dat is verstrekt in het geïmporteerde bestand, zelfs als het boekstuk niet in evenwicht is. Houd rekening met het volgende als u de op sets gebaseerde verwerking wilt gebruiken, maar ook gebruik wilt maken van de nummerreeks die is gedefinieerd voor boekstuknummers.

    - U kunt deze functionaliteit inschakelen door in de journaalnaam die wordt gebruikt voor imports, **Nummertoewijzing tijdens boeking** in te stellen op **Ja**.
    - Er moet nog steeds een boekstuknummer worden gedefinieerd in het geïmporteerde bestand. Dit nummer is echter tijdelijk en wordt overschreven door het boekstuknummer als het journaal wordt geboekt. Zorg dat de regels van het journaal juist zijn gegroepeerd op tijdelijk boekstuknummer. Stel bijvoorbeeld dat tijdens het boeken drie regels worden gevonden die een tijdelijke boekstuknummer 1 hebben. Het tijdelijke boekstuknummer van alle drie de regels worden overschreven door het volgende nummer uit de nummerreeks. Als deze drie regels geen evenwichtige vermelding zijn, wordt het boekstuk niet geboekt. Vervolgens geldt dat, als er regels worden gevonden die een tijdelijk boekstuknummer van 2 hebben, dit nummer wordt overschreven door het volgende boekstuknummer in de reeks enzovoort.

- Als u de instelling **Op sets gebaseerde verwerking** niet gebruikt, hoeft u geen boekstuknummer op te geven in het geïmporteerde bestand. De boekstuknummers worden gemaakt tijdens het importeren, op basis van de instellingen van de journaalnaam (**Maximaal één boekstuknummer**, **In samenhang met saldo** enzovoort). Als bijvoorbeeld de journaalnaam is gedefinieerd als **In samenhang met saldo**, ontvangt de eerste regel een nieuw standaard boekstuknummer. Het systeem evalueert vervolgens de lijn om te bepalen of de debetbedragen gelijk zijn aan de creditbedragen. Als een tegenrekening voor de regel bestaat, ontvangt de volgende regel die wordt geïmporteerd in een nieuw boekstuknummer. Als er geen tegenrekening bestaat, evalueert het systeem of de debetbedragen gelijk zijn aan de creditbedragen bij het importeren van elke nieuwe regel.
- Als het veld **Boekstuknummer** is ingesteld op **Automatisch gegenereerd**, mislukt het importeren. De instelling **Automatisch gegenereerd** voor het veld **Boekstuknummer** wordt niet ondersteund.

Standaard gebruikt de entiteit Algemeen journaal verwerking op basis van sets. Nadat u de zakelijke vereisten voor uw organisatie hebt beoordeeld, kunt u de instelling **Op sets gebaseerde verwerking** wijzigen door te klikken op **Gegevensentiteiten** in de werkruimte **Gegevensbeheer**. Op sets gebaseerde verwerking wordt gebruikt om het importproces te versnellen. Als u geen gebruikmaakt van op sets gebaseerde verwerking, verloopt het importeren van de entiteit Algemeen journaal langzamer.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
