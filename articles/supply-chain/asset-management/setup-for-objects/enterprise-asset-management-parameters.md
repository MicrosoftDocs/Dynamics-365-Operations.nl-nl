---
title: Parameters voor activabeheer
description: In Activabeheer moeten algemene parameters met betrekking tot activa, werkorders en de planning van werkorders worden ingesteld.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3336a3357578b25522e1ac457a48349f88b7318d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024563"
---
# <a name="asset-management-parameters"></a>Parameters voor activabeheer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer moeten algemene parameters met betrekking tot activa, werkorders en de planning van werkorders worden ingesteld. In dit onderwerp wordt uitgelegd hoe deze instelt. Selecteer **Activabeheer** > **Instellingen** > **Parameters voor activabeheer** om het formulier te openen.

De knop **Wizard Gegevens maken** kan worden gebruikt om automatisch instellingsgegevens te maken voor test- of demogegevens in een bedrijf in Dynamics 365 Supply Chain Management. Raadpleeg de whitepaper 'Testgegevens instellen in Activabeheer' voor informatie over het gebruik van de wizard.

Koppeling **Activa**

- **Standaard functionele locatie** is de standaard functionele locatie, die automatisch wordt geselecteerd voor activa wanneer u nieuwe activa maakt.  
- Selecteer in het veld **Standaardkalender** een kalender die moet worden gebruikt voor het berekenen van KPI's voor activa, in het geval er geen resource is geselecteerd voor een activum.  
- Selecteer in het veld **Weergave** de standaardweergave die wordt weergegeven wanneer u het formulier **Activaweergave** opent (**Activabeheer** > **Algemeen** > **Activa** > **Activaweergave**).
- **Standaard aanvraagtype** is het standaardtype onderhoudsaanvraag, dat automatisch wordt geselecteerd wanneer u een nieuwe aanvraag maakt.  
- Als u projecten wilt maken die betrekking hebben op activa, worden projectrelaties met betrekking tot de selectie van **Hoofdproject**, **Projecthiërarchie** en de optie **Automatisch projecten maken** ingesteld in **Parameters voor activabeheer**.  
- In het veld **Projectmasker voor werkorder** definieert u het aantal subprojecten dat is toegestaan voor werkorders en subactiva. Een werkordermasker wordt gebruikt om te definiëren hoeveel werkorders kunnen worden gemaakt voor een activum en gebruikt in het gerelateerde werkorderproject. Het werkordermasker wordt ingesteld in het veld **Verwant werkordermasker** in **Parameters voor activabeheer** (**Activabeheer** > **Instellingen** > **Parameters voor activabeheer** > **Werkorders**).  
>[!NOTE]
>De indeling voor een verwant werkordermasker is een aantal hash-tekens (#), afhankelijk van het maximumaantal werkorders dat u verwacht te maken voor een activum. Voorbeeld: met ## kunt u tot 99 subprojecten maken.  
- Prognoses voor taaktypen worden opgeslagen in het project dat is geselecteerd in het veld **Prognose project**. Voor elk taaktype wordt automatisch een nieuwe activiteit gemaakt voor het prognoseproject. Prognoses voor het taaktype worden vervolgens opgeslagen in het prognoseproject.  
- Selecteer in het veld **Model** het prognosemodel dat wordt gebruikt voor taaktype- en werkorderprognoses.  


Koppeling **Werkorders**

- **Standaard werkordertype** definieert standaardinstellingen bij het maken van een werkorder.  
- **Preventief werkordertype** definieert het type werkorder dat wordt gebruikt bij het maken van werkorders op basis van onderhoudsplannen. Als dit veld leeg blijft, wordt het werkordertype in het veld **Standaard werkordertype** gebruikt.  
- In het veld **Verwant werkordermasker** definieert u het maximumaantal werkorders dat aan een werkorder kan worden gekoppeld. Voorbeeld: met ## kunt u maximaal 99 verwante werkorders hebben. Als u een masker definieert zoals hier wordt beschreven, worden gerelateerde werkorders genummerd [werkorder-id van de werkorder waaraan een werkorder is gerelateerd]-01, -02, -03 enzovoort. Als u geen masker in dit veld definieert, krijgt een verwante werkorder de volgende sequentiële werkorder-id.  
- Selecteer 'Ja' op de wisselknop **Fouten kopiëren** als u automatisch fouten die zijn geregistreerd voor werkorders wilt kopiëren naar gerelateerde onderhoudsaanvragen.  
- In het veld **Niveau** definieert u het functionele locatieniveau dat automatisch in een werkorder wordt ingevoegd als alle gerelateerde werkordertaken naar dezelfde functionele locatie verwijzen. Als de werkordertaken niet allemaal betrekking hebben op dezelfde functionele locatie op het gedefinieerde niveau, wordt het veld **Functionele locatie** leeg gelaten in de werkorder. Voorbeeld: als u het cijfer '1' in dit veld invoegt, is dat het hoogste niveau in een functionele locatiestructuur. Als u het cijfer '0' in dit veld invoegt, hebt u geen specifiek functioneel locatieniveau gedefinieerd, maar alleen aangegeven dat de functionele locatie alleen aan de werkorder wordt toegevoegd als alle werkordertaken in een werkorder aan dezelfde functionele locatie zijn gerelateerd.  
- Journalen die worden gebruikt bij het boeken van verbruik in een werkorder kunnen worden geselecteerd op het sneltabblad **Algemeen** in de velden **Uur**, **Artikel** en **Onkosten**.  
- Selecteer in het veld **Producttaalbron** welke taal moet worden gebruikt voor productnamen in rapporten van Activabeheer. U kunt de taal selecteren die is ingesteld op de bedrijfsrekening of de taal die is ingesteld voor de gebruiker die momenteel is aangemeld.  
- Selecteer 'Ja' op de wisselknop **Real-time update** als u automatisch wijzigingen in de standaardwaarden voor taaktype, onderhoudsplannen en onderhoudsronden wilt bijwerken.
> - Als u 'Nee' selecteert, worden wijzigingen in de standaardwaarden voor taaktypen, onderhoudsplannen en onderhoudsronden niet automatisch bijgewerkt in Activabeheer  
> - Selecteer 'Nee' op de wisselknop als u grote hoeveelheden gegevens hebt die worden gesynchroniseerd, bijvoorbeeld veel activa of functionele locaties die zijn ingesteld op onderhoudsplannen of onderhoudsronden, of een groot aantal onderhoudsplannen of ronden.  
> - Als u wijzigingen aanbrengt in de standaardwaarden voor taaktypen of onderhoudsplannen of onderhoudsronden en hebt 'Nee' hebt geselecteerd voor een real-time update, wordt mogelijk geen waarschuwing weergegeven als de wijzigingen van invloed zijn op:
>   - functionele locaties die zijn ingesteld voor onderhoudsplannen of -ronden  
>   - objecten die zijn ingesteld voor onderhoudsplannen of -ronden  
>   - instellingen voor onderhoudsplannen  
>   - instellingen voor onderhoudsronden  
- Op het sneltabblad **Categorie** kunnen standaardcategorieën met betrekking tot verbruik op werkorders worden gedefinieerd.  


Koppeling **Planning van werkorders**

- **Time fence plannen** definieert een periode in dagen, berekend vanaf de verwachte begindatum van de werkorder, waarin werkordertaken worden gepland.  
- Het **hoofdplan** heeft betrekking op resources in de module **Organisatiebeheer**. Als u in dit veld een hoofdplan selecteert, kunt u capaciteitsreserveringen die betrekking hebben werkorders bekijken in **Capaciteitsreserveringen** (**Organisatiebeheer** > **Resources** > **Resources** > selecteer resource > tabblad **Resource** > knop **Capaciteitsreserveringen**). Als u dit veld leeg laat, kunt u capaciteitsbelasting die betrekking heeft werkorders bekijken in **Capaciteitsbelasting** (**Organisatiebeheer** \> **Resources** \> **Resources** \> selecteer resource \> tabblad **Resource** \> knop **Capaciteitsbelasting**).  

>[!NOTE]
>De selectie met betrekking tot het al dan niet gebruiken van een hoofdplan in de module **Activabeheer** en het gerelateerde formulier dat wordt gebruikt om een overzicht te krijgen van capaciteitsreserveringen of capaciteitsbelasting wordt standaard ingesteld in de standaardinstellingen. Afhankelijk van uw instellingen in het veld **Hoofdplan** krijgt u toegang tot capaciteitsgegevens in **Capaciteitsreserveringen** of **Capaciteitsbelasting** in de module **Organisatiebeheer**. Het is niet mogelijk om een instelling te maken waarin capaciteitsreserveringen in beide weergaven worden getoond.  

De velden die worden beschreven in de onderstaande lijst met opsommingstekens hebben betrekking op berekende beoordelingsscores, die worden gebruikt om de prioriteit van werkorders te berekenen tijdens de planning van werkorders.

- **Prioriteit** - een beoordelingsscore die samen met de beoordelingsscore wordt berekend in de velden **Kritieke eigenschap** en **Begindatum**. Het getal in dit veld wordt gedeeld door het getal in het veld **Prioriteit** in een werkorder. Voorbeeld: als de waarde '5,00' wordt ingevoegd in dit veld en een werkorder de prioriteit '20' heeft, bedraagt de beoordelingsscore voor prioriteit 0,25.  
- **Kritieke eigenschap** - een beoordelingsscore die samen met de beoordelingsscore wordt berekend in de velden **Prioriteit** en **Begindatum**. Het getal in dit veld wordt vermenigvuldigd met het getal in het veld **Kritieke eigenschap** in een werkorder. Voorbeeld: als de waarde '10,00' wordt ingevoegd in dit veld en een werkorder de kritieke eigenschap '5' heeft, bedraagt de beoordelingsscore voor kritieke eigenschap 50.  
- **Begindatum** - een beoordelingsscore die samen met de beoordelingsscore wordt berekend in de velden **Prioriteit** en **Kritieke eigenschap**. Dit veld geeft de dagelijkse score aan als een negatieve waarde en wordt vergeleken met het veld **Verwachte begindatum** in een werkorder. Voorbeeld: als de waarde '10,00' wordt ingevoegd in dit veld en de verwachte begindatum van een werkorder drie dagen van nu is, bedraagt het beoordelingsresultaat min 30,00. Als de resultaten van 0,25 en 50 uit de voorbeelden in de hierboven beschreven velden **Prioriteit** en **Kritieke eigenschap** worden opgeteld, komt u uit op een totaal van plus 20,25. Dat cijfer wordt vergeleken met alle andere beoordelingsscores voor werkorders tijdens de planning van werkorders en de hoogste beoordelingsscores worden vervolgens als eerste gepland.  
- **Verantwoordelijke medewerker** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerkersgroep**, **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum**. Als de waarde '50,00' wordt ingevoegd in dit veld en een verantwoordelijke medewerker is geselecteerd in een werkorder, krijgt de medewerker 50 punten in de algehele berekening voor medewerkers tijdens de planning van werkorders.  
- **Verantwoordelijke medewerkersgroep** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerker**, **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum**. Als de waarde '50,00' wordt ingevoegd in dit veld en een verantwoordelijke medewerker is geselecteerd in een werkorder, krijgt de medewerker 50 punten in de algehele berekening voor medewerkers tijdens de planning van werkorders.  
- De wisselknop Ja/Nee voor **Beperken tot verantwoordelijk** beperkt het aantal medewerkers dat beschikbaar is voor de planning van werkorders. Selecteer 'Nee' als u een score voor alle medewerkers wilt berekenen, ongeacht of deze zijn ingesteld als verantwoordelijke medewerkers of als onderdeel van een verantwoordelijke medewerkersgroep. Selecteer 'Ja' als u een score wilt berekenen voor medewerkers die zijn ingesteld als verantwoordelijke medewerker in de werkorder en/of zijn opgenomen in een verantwoordelijke medewerkersgroep die in de werkorder is geselecteerd.  
- **Voorkeursmedewerker** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerker**, **Voorkeursmedewerker**, **Voorkeursmedewerkergroep**, **Activalocatie** en **Begindatum**. De vier beoordelingsscores worden berekend en bij elkaar opgeteld om een score te geven die wordt gebruikt om te selecteren welke medewerker aan welke werkorder moet worden toegewezen tijdens de planning van werkorders. Als de waarde '10,00' in dit veld wordt ingevoegd en een medewerker is geselecteerd als voorkeursmedewerker in een werkorder, krijgt die medewerker 10 punten in de algehele berekening voor medewerkers tijdens de planning van werkorders.  
- **Voorkeursmedewerkergroep** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerker**, **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum**. Als de waarde '10,00' in dit veld wordt ingevoegd en een medewerker is toegewezen aan een voorkeursmedewerkersgroep die is geselecteerd in een werkorder, krijgt die medewerker 10 punten in de algehele berekening voor medewerkers tijdens de planning van werkorders.  
- De wisselknop Ja/Nee voor **Beperken tot voorkeur** beperkt het aantal medewerkers dat beschikbaar is voor de planning van werkorders. Selecteer 'Nee' als u een score voor alle medewerkers wilt berekenen, ongeacht of deze zijn ingesteld als voorkeursmedewerkers of als onderdeel van een verantwoordelijke medewerkersgroep. Selecteer 'Ja' als u alleen een score wilt berekenen voor medewerkers die zijn ingesteld als voorkeursmedewerkers en/of zijn opgenomen in een voorkeursmedewerkersgroep.  
- **Locatie** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerker**, **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum**. Als de waarde '3.000,00' wordt ingevoegd in dit veld, krijgt een medewerker 3000 punten bij de berekening als de medewerker zich in dezelfde fabriek of faciliteit bevindt als het activum waarvoor een taak moet worden gepland.  

  - Als uw bedrijf gebruikmaakt van functionele locaties, krijgen medewerkers een volledige score als ze zich op de functionele locatie bevinden die betrekking heeft op het activum. Als de functionele locatie van het activum een bovenliggend activum heeft, krijgen medewerkers op die functionele locatie 1/2 score. Als die locatie ook een bovenliggend item heeft, krijgen medewerkers op die locatie 1/3 score. Als die locatie ook een bovenliggend item heeft, krijgen medewerkers op die locatie 1/4 score enzovoort.  
  - Als uw bedrijf activalocatie gebruikt, wat we niet aanbevelen, worden locatie, gebied en zone gebruikt om locatiescores te berekenen. Werknemers krijgen een volledige score als ze zich op de locatie en in het gebied en de zone bevinden die verband houdt met het activum. Als de locatie van de medewerker alleen overeenkomt met locatie en gebied, is de beoordelingsscore voor de medewerker 2/3 van de volledige score. Als de locatie van de medewerker alleen overeenkomt met locatie, bedraagt de beoordelingsscore voor de medewerker 1/3 van de volledige score.  

- De wisselknop Ja/Nee voor **Beperken tot locatie** beperkt het aantal medewerkers dat beschikbaar is voor de planning van werkorders. Selecteer 'Nee' als u een score wilt berekenen voor alle medewerkers op alle functionele locaties. Selecteer 'Ja' als u alleen een score wilt berekenen voor medewerkers die zijn gekoppeld aan de functionele locatie van de werkorder.

>[!NOTE]
>De drie wisselknoppen 'Beperken tot...' worden geïntroduceerd om de snelheid van de planning van werkorders te verhogen door het aantal scores dat voor medewerkers wordt berekend te beperken.

**Begindatum van medewerker** - een beoordelingsscore die wordt berekend samen met de waarden voor de beoordelingsscores voor **Verantwoordelijke medewerker**, **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum**. Dit veld geeft de dagelijkse score aan als een negatieve waarde en wordt vergeleken met het veld **Verwachte begindatum** in een werkorder. Als de waarde '10,00' wordt ingevoegd in dit veld en de verwachte begindatum van een werkorder morgen is, bedraagt het beoordelingsresultaat min 10,00.

  - Ervan uitgaande dat er geen verantwoordelijke medewerker en verantwoordelijke medewerkersgroep zijn geselecteerd in een te plannen werkorder, komt u door de waarden van de beoordelingsscore in de bovenstaande velden **Voorkeursmedewerker**, **Voorkeursmedewerkersgroep**, **Activalocatie** en **Begindatum** op te tellen en af te trekken uit op een totaal van 3010,00. Dit betekent een hoge score voor de medewerker die al is geselecteerd als voorkeursmedewerker en die is opgenomen in de voorkeursmedewerkersgroep in de werkorder, terwijl de medewerker zich ook nog eens in dezelfde faciliteit bevindt als het activum waarvoor een taak moet worden gepland. Al met al betekent dit dat er een goede kans is dat de medewerker in kwestie wordt geselecteerd om de taak uit te voeren tijdens de planning van werkorders.  
  - Als de waarde '0,00' in een van de acht bovenstaande velden wordt ingevoegd, wordt die beoordelingsscore niet gebruikt tijdens de planning van werkorders.  


Koppeling **Documenttypen**

Selecteer de documenttypen die beschikbaar moeten zijn voor het afdrukken van bijlagen met betrekking tot een werkorderrapport. Dit wordt gedaan door op een documenttype te klikken in de sectie **Beschikbaar** en op de knop ![pijl naar voren](media/15-setup-for-objects.png) te klikken. Als u een geselecteerd documenttype wilt verwijderen, selecteert u het documenttype in de sectie **Geselecteerd** en klikt u op de knop ![pijl terug](media/16-setup-for-objects.png).



Koppeling **Nummerreeksen**

Selecteer de vereiste nummerreeksen in deze sectie. Er zijn twee nummerreeksen voor activa: één voor handmatig gemaakte activa en één voor activa die zijn gemaakt via in behandeling zijnde activa.
