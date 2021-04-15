---
title: Projectinstellingen werkorder
description: In dit onderwerp wordt uitgelegd hoe u werkorderprojecten instelt in Activabeheer.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 071c73f9295ad7911037cbd10a48b46b044eebda
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808227"
---
# <a name="work-order-project-setup"></a>Projectinstellingen werkorder

[!include [banner](../../includes/banner.md)]

 

In de module **Activabeheer** is een projectrelatie vereist voor elke werkordertaak. Met het project dat is gekoppeld aan een werkordertaak, kunt u kosten bijhouden voor verschillende projecten die zijn gerelateerd aan Activabeheer, zoals interne onderhoudsprojecten, servicebeheerprojecten en investeringsprojecten. 

## <a name="project-setup-for-a-work-order-job"></a>Projectinstellingen voor een werkordertaak

Wanneer u een werkordertaak maakt voor een werkorder, bepalen de projectinstellingen in de module **Projectmanagement en boekhouding** en de projectinstellingen voor werkorders in de module **Activabeheer** hoe projecten voor kostenbeheer kunnen worden gebruikt voor het activum dat is geselecteerd op die werkordertaak. In deze sectie worden de volgende onderdelen van de projectinstellingen beschreven die worden gebruikt voor een werkorder: het hoofdproject (project-ID), projecttype, projectactiviteiten en financiële dimensies:

- Wanneer u een werkordertaak voor een werkorder maakt, worden er automatisch een unieke project-ID en bijbehorende projectactiviteit voor gemaakt. Als verschillende werkordertaken op een werkorder echter hetzelfde activum bevatten, wordt voor deze taken dezelfde project-ID gebruikt. Met andere woorden, er wordt één project-ID gemaakt voor elk activum in een werkorder.

    - Het bovenliggende project (project-ID) voor een werkordertaak is te vinden in de bovenliggende projectinstellingen. (Zie het volgende gedeelte voor meer informatie over de bovenliggende projectinstelling.) Als u bijvoorbeeld een klant of een functionele locatie koppelt aan een specifiek hoofdproject, wordt het hoofdproject gebruikt telkens wanneer u werkorders voor die klant of die functionele locatie maakt. Als u een specifiek project-ID niet relateert aan, bijvoorbeeld, een functionele locatie, wordt het volgende bovenliggende project in de projectinstellingen voor de werkorder gebruikt.
    - Een projecttype is vereist voor elke project-id. Het projecttype wordt gevonden in de instellingen van de instelling van de projectgroep. (Zie het volgende gedeelte voor meer informatie over de instelling van de projectgroep.) Als er geen overeenkomst wordt gevonden in de instelling van de projectgroep, wordt de instelling van de projectgroep voor het hoofdproject gebruikt.
    - De instellingen voor het vereisen van projectactiviteiten voor prognoses en journalen worden gekopieerd van het bovenliggende project naar het werkorderproject. Als de opties **Uur**, **Onkosten** en **Artikel** zijn ingesteld op **Ja** voor het project dat als hoofdproject wordt gebruikt, is een projectactiviteit verplicht voor prognoses en journalen. (Om toegang te krijgen tot deze opties selecteert u **Projectmanagement en boekhouding** \> **Projecten** \> **Alle projecten** en selecteert u vervolgens het project dat als een hoofdproject wordt gebruikt. De opties staan in de sectie **Activiteit vereisen op journalen** op het Sneltabblad **Instellingen**.)

- Financiële dimensies worden gekopieerd vanuit het activum en samengevoegd met het hoofdproject.

In het volgende gedeelte wordt uitgelegd hoe u bovenliggende projecten en projectgroepen instelt. Het bovenliggende project en de bovenliggende groepen worden gebruikt om de werkorders te beheren. Ze worden ook gebruikt voor het rapporteren over werkorders.

## <a name="set-up-work-order-projects"></a>Werkorderprojecten instellen

Voordat u werkorders gaat maken, moet u werkorderprojecten instellen. De pagina **Instellingen werkorderproject** (**Activabeheer** \> **Instellingen** \> **Werkorders** \> **Projectinstellingen**) bevat twee tabbladen: **Bovenliggend project** en **Projectgroep**.

Op het tabblad **Bovenliggend project** kunt u projectrelaties instellen die kunnen worden gebruikt als er geen project is ingesteld voor het activum dat is geselecteerd in de werkordertaak. Een bovenliggende projectinstelling is niet vereist als uw bedrijf gebruikmaakt van activaprojecten. Dit is alleen relevant als u werkorderprojecten wilt gebruiken in plaats van activaprojecten. In dat geval moet u minimaal één hoofdproject instellen.

Op het tabblad **Projectgroep** kunt u projectgroepen instellen die kunnen worden gekoppeld aan werkordertypen, activatypen en activa.

Projectgroepen kunnen worden gebruikt om specifieke categorieën (groepen) te maken die worden gebruikt voor kostenbeheer. Als u bijvoorbeeld projectgroepen maakt voor specifieke activatypen of werkordertypen, kunt u gedetailleerde onderhoudskosten op type volgen.

Projectgroepen zijn niet verplicht. Als u geen projectgroepen instelt, wordt het hoofdproject gebruikt om de projectgroep te bepalen en wordt een onderliggend project gemaakt op basis van de projectgroep van het bovenliggende project.

Met de instellingen kunt u volledige integratie met de module **Projectmanagement en boekhouding** uitvoeren. Daarom kunt u de kosten bijhouden die zijn gerelateerd aan werkorders in de gerelateerde projecten. De volgende procedure beschrijft de instellingen voor werkorderprojecten.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Projectinstellingen**.
2. Selecteer op het tabblad **Bovenliggend project** de optie **Toevoegen**.
3. Selecteer in de velden **Werkordertypen**, **Functionele locatie**, **Activumtype** en **Activum** de waardes die u nodig heeft. Voor elke regel die u toevoegt, kunt u slechts één veld of meerdere velden instellen. Het aantal velden dat u instelt, bepaalt welke combinatie wordt gebruikt wanneer een project-ID wordt geselecteerd in Activabeheer. 

    Als u een functionele locatie selecteert, worden de bijbehorende onderliggende locaties automatisch opgenomen. Als u een activum selecteert, kunt u meer instellingsregels voor werkorderprojecten maken voor hetzelfde activum, maar u kunt verschillende projecten voor dat activum selecteren.

4. Selecteer in het veld **Project-id** het project dat moet worden gerelateerd aan de instellingen die u in stap 3 hebt gemaakt.
5. Als de projectinstelling slechts een beperkte periode geldig moet zijn, selecteert u een einddatum in het veld **Einddatum**. Selecteer anders **Geen**.

    De begindatum is standaard de datum waarop u het werkorderproject aan de pagina toevoegt. Het wordt gecontroleerd door het veld **Geldig vanaf**, dat standaard verborgen is. Als u het veld **Geldig vanaf** wilt weergeven, selecteert u **Weergeven** \> **Alle**. U kunt vervolgens het veld **Geldig vanaf** in combinatie met het veld **Einddatum** gebruiken om een beperkte geldigheidsperiode in te stellen voor het werkorderproject.

    ![Pagina Projectinstellingen werkorders](media/17-setup-for-work-orders.png)

6. Selecteer op het tabblad **Projectgroep** de optie **Toevoegen**.
7. Selecteer een type werkorder in het veld **Werkordertype**.
8. Als u de koppeling van de projectgroep specifieker wilt opgeven, selecteert u een activumtype in het veld **Activumtype** of een activum in het veld **Activum**.
9. Selecteer in veld **Projectgroep** de projectgroep die moet worden gerelateerd aan het type werkorder. Een type werkorder met de naam **Preventief onderhoud** kan bijvoorbeeld worden gekoppeld aan een projectgroep met de naam **Prev Ond** of **Intern**. Een **Investering**-werkordertype dat wordt gebruikt voor werkorders die zijn gerelateerd aan investeringen en vaste activa, kan ook worden gekoppeld aan een projectgroep met de naam **Investeren** of **Investering.**
10. Selecteer **Opslaan**.

![Pagina Projectinstellingen werkorders, Werkorder toevoegen](media/18-setup-for-work-orders.png)

> [!NOTE]
> Elke keer dat er een werkorderregel wordt gemaakt, zoekt Activabeheer naar een projectgroep die gerelateerd moet zijn aan het taakproject van de werkorder. De zoekopdracht is gebaseerd op de instellingen die in dit onderwerp worden beschreven. Elke projectgroep heeft een gerelateerd projecttype. Project groepen die het projecttype **Tijd en materiaal** of **Vaste prijs** hebben, zijn alleen geldig voor activa die betrekking hebben op een klantenrekening.
>
> Voor bovenliggende projecten en projectgroepen geldt dat wanneer het systeem het beschikbare werk orderproject of projectgroep selecteert, de selectie is gebaseerd op de records die u met behulp van de voorgaande procedure hebt gemaakt. Met Activabeheer gaat u via records die zijn gerelateerd aan het werkplaatsproject om een mogelijke overeenkomst te controleren. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Dat wil zeggen dat voor het bovenliggend project van de werkorder, Activabeheer eerst controleert op een mogelijke overeenkomst voor het veld **Activa**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Activatype**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Functionele locatie** enzovoort. Zoals u kunt zien in de indeling van de pagina **Instellingen voor werkorderprojecten**, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden. Als er geen overeenkomst wordt gevonden, wordt het standaardrecord gebruikt waarin alleen een project-id wordt geselecteerd. Het proces voor het zoeken van de gerelateerde projectgroep is vergelijkbaar. Activabeheer controleert eerst of er mogelijke overeenkomsten zijn voor het veld **Activum**, vervolgens het veld **Activumtype** en dan het veld **Type werkorder**. Als er geen overeenkomst wordt gevonden, wordt het standaardrecord gebruikt waarin alleen een projectgroep wordt geselecteerd.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]