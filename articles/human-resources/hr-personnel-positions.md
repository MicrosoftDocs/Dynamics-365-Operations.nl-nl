---
title: Posities
description: In dit onderwerp worden de conceptuele elementen beschreven die een positie kan bevatten. Het biedt ook voorbeelden die laten zien hoe u die elementen in uw organisatie kunt gebruiken.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 95abd7548d23ef1b4f5fc31ebaa818e06e179d60
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068814"
---
# <a name="positions"></a>Posities


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp worden de conceptuele elementen beschreven die een positie kan bevatten. Het biedt ook voorbeelden die laten zien hoe u die elementen in uw organisatie kunt gebruiken.

Voordat u een positie kunt maken, moet u eerst een taak instellen. Sommige positiedetails, zoals de compensatieregio, werknemertoewijzing, duur van de positie en rapporteringsrelatie, zijn van kracht.

## <a name="general-information"></a>Algemene informatie

Wanneer u een positie maakt, moet u een taak selecteren. Voor de geselecteerde taak worden automatisch de volgende gegevens ingevuld:

- Beschrijving
- Titel
- Voltijdse equivalent
- Taakgroep

De positietitel wordt gebruikt om naar de titel van een werknemer te verwijzen. (De titel die is vermeld op het niet-gebruikte aantal werknemers.) Daarom moeten positietitels zo veel mogelijk worden gestandaardiseerd.

> [!NOTE]
> Een medewerker kan niet aan een positie worden toegewezen op een datum die vóór de datum van beschikbaarheid voor toewijzing ligt.
>
> Met een parameter op het tabblad **Posities** van de pagina **Gedeelde Human Resources-parameters** wordt het gedrag van medewerkertoewijzingen bepaald. Selecteer een van de volgende waarden:
>
> - **Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.
> - **Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Als u deze optie selecteert, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar komt. Voer vervolgens op het tabblad **Algemeen** de datum voor **Beschikbaar voor toewijzing** in om medewerkertoewijzing in te schakelen. Als u deze optie selecteert, wordt de datum voor medewerkertoewijzing standaard ingesteld op **Nooit** wanneer u de medewerker probeert toe te wijzen.

## <a name="position-duration"></a>Positieduur

Elke positie is van kracht gedurende een bepaalde tijd die de duur wordt genoemd. Zomerposities kunnen bijvoorbeeld een duur hebben van 1 mei 2021 tot en met 31 augustus 2021. De activeringsdatum is de datum waarop de positie actief is in het systeem. De intrekkingsdatum is de datum waarop de positie niet langer actief is in het systeem.

Let erop dat noch de datum van beschikbaarheid voor toewijzing, noch de datum voor medewerkertoewijzing vóór de activeringsdatum kan liggen. Een positie die pas als actief is beschouwd als de activeringsdatum is bereikt. Bovendien kan een medewerkertoewijzing niet tot na de intrekkingsdatum van de positie duren.

## <a name="reports-to-position"></a>Verantwoording aan positie

Posities zijn belangrijke elementen op het lagere niveau van een organisatiehiërarchie. Op de pagina **Positie** kunt u de positie opgeven waaraan een positie rapporteert. Wanneer u een werknemer toewijst aan een positie die aan een andere positie rapporteert, maakt u een rapporteringsrelatie tussen de werknemers die zijn toegewezen aan die twee posities. Positie 000220 rapporteert bijvoorbeeld aan positie 000300. Kim Akers is toegewezen aan positie 000220 en Sanjay Patel is toegewezen aan positie 000300. Daarom rapporteert Kim Akers aan Sanjay Patel.

> [!TIP]
> De optie Verantwoording aan positie wordt in het gehele systeem gebruikt om te bepalen wie de manager van een werknemer is. Als de managerrol in het voorgaande voorbeeld is toegewezen aan Sanjay Hierel in het systeem, ziet hij Kim Akers als directe ondergeschikte in Selfservice manager. De rapporteringsrelatie kan ook worden gebruikt wanneer u regels voor het doorsturen van werkstromen en controlelijsttaken maakt.

## <a name="relationships"></a>Relaties

Als uw organisatie een matrixhiërarchie of een andere aangepaste hiërarchie gebruikt, kunt u positiehiërarchietypen instellen. U kunt vervolgens rapporteringsrelaties toevoegen aan posities voor elk hiërarchietype dat u hebt ingesteld. Lori Penor is bijvoorbeeld een algemeen manager bij Adventure Works en is toegewezen aan de positie **Algemeen manager**. Lori beheert de ontwikkeling van een product dat wordt gebruikt voor het reinigen van widgets. Ze heeft een boekhouder nodig om haar te helpen met de financiën. Daarom heeft ze Kim Akers als haar boekhouder aangeworven. Kim rapporteert rechtstreeks aan Sanjay Patel, maar werkt ook met Lori Penor aan activiteiten met betrekking tot de financiën voor de ontwikkeling van de widgetreiniger.

In het voorafgaande voorbeeld moet u de volgende taken voltooien voor het instellen van de werkrelatie tussen Kim Akers en Lori Penor:

1. Maak een aangepast positiehiërarchietype genaamd **Widget** om een hiërarchie te maken die posities bevat die verantwoordelijk zijn voor het werken aan de widgetreiniger.
2. Geef de positie van **Algemeen manager** op als de positie waaraan de positie van Kim rapporteert in de hiërarchie **Widget**.
3. Gebruik de positiehiërarchie de rapporteringsstructuur van posities weer te geven. Als u meerdere positiehiërarchieën hebt, kunt u de hiërarchie voor elk hiërarchietype weergeven in de positiehiërarchie. U kunt ook een positie zoeken via positie-id of de naam van de werknemer die aan de positie is toegewezen. De positiehiërarchie is een organisatiehiërarchie.

## <a name="labor-union"></a>Vakbond

U kunt registreren of een vakbondsovereenkomst is vereist voor de positie en welke vakbond wordt gebruikt. U kunt de overeenkomst ook aan een rechtspersoon koppelen.

## <a name="financial-dimensions"></a>Financiële dimensies

Wanneer u de financiële dimensie voor een positie maakt, moet u een rechtspersoon opgeven. U kunt de standaarddimenssie voor elke dimensie afzonderlijk selecteren. U kunt ook een verdelingsjabloon selecteren om automatisch standaarddimensies in te vullen. Een verdelingssjabloon biedt ook de mogelijkheid om bedragen toe te wijzen over meerdere dimensiewaarden.
