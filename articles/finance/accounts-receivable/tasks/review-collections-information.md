---
title: Incassogegevens controleren
description: In dit onderwerp wordt uitgelegd hoe u incassogegevens controleert en wat de verschillende instellingsopties en incassotransacties zijn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd606461b9d7198bda12e297598fae0cbf8b39a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188712"
---
# <a name="review-collections-information"></a>Incassogegevens controleren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u incassogegevens controleert en wat de verschillende instellingsopties en incassotransacties zijn. Bij deze procedure wordt het demobedrijf USMF gebruikt.

## <a name="create-customer-pools"></a>Klantverzamelingen maken
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Instellen > Klantverzamelingen**.
- Met deze pagina kunt u klantverzamelingen instellen. Dit zijn query's waarmee een groep klantrekeningen wordt gedefinieerd die kan worden weergegeven en beheerd voor aanmaningen of processen voor ouderdomsrangschikking. Met klantverzamelingen kunt u gegevens filteren op de lijstpagina **Aanmaningen** en gerelateerde lijstpagina's. U kunt klantverzamelingen ook gebruiken om de klantrekeningen te filteren, die worden opgenomen bij de aanmaak van ouderdomsmomentopnamen.  
- U kunt klantverzamelingen gebruiken om de klantrekeningen te filteren, die worden opgenomen bij de aanmaak van ouderdomsmomentopnamen.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Groeps-ID.**
4. Typ een waarde in het veld **Beschrijving van groep**.
5. Klik op **Verzamelingscriteria selecteren**.
6. Typ een waarde in het veld **Criteria**.
7. Selecteer **OK**.
8. Selecteer **Voorbeeld van klantverzameling**.

## <a name="create-collections-agents"></a>Incassomedewerkers maken
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Instellen > Incassomedewerkers**.  
- Gebruik deze pagina om medewerkers in te stellen als incassomedewerkers en hieraan desgewenst klantverzamelingen toe te wijzen. Een *incassomedewerker* is een persoon die met klanten samenwerkt om ervoor te zorgen dat de betalingen op tijd worden geïnd.  
- Incassomedewerkers die op deze pagina worden ingesteld, worden automatisch toegevoegd aan een team van incassomedewerkers. Als een team wordt geselecteerd in het veld **Team** op de pagina **Parameters van module Klanten**, worden incassomedewerkers aan dat team toegevoegd. Als er geen team wordt geselecteerd, wordt er automatisch een nieuw team met de naam Aanmaningen gemaakt en worden de incassomedewerkers aan dat team toegevoegd.  
2. Selecteer de gewenste medewerker en selecteer **Toevoegen** op de pagina.
3. Selecteer in het veld **Groeps-ID** de gewenste record in het vervolgkeuzemenu.
4. Schakel het selectievakje **Standaardgroep** in of uit.
- Selecteer deze optie om alle klantverzamelingen op te nemen in filterlijsten voor de geselecteerde incassomedewerker. Als deze optie niet is geselecteerd, zijn alleen de klantverzamelingen die aan de incassomedewerker zijn toegewezen, beschikbaar in filterlijsten.  

## <a name="create-aging-period-definition"></a>Ouderdomsperiodedefinitie maken
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Instellen > Ouderdomsperiodedefinities**.
- Met ouderdomsperiodedefinities kunt u de vervaldag van klant- en leverancierrekeningen analyseren op basis van een door u ingevoerde datum. Elke ouderdomsperiode die u instelt voor de ouderdomsperiodedefinitie, correspondeert met een kolom op de lijstpagina of in het formulier of rapport wanneer de analyse wordt uitgevoerd.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Ouderdomsperiodedefinitie**.
4. Typ een waarde in het veld **Beschrijving**.
- De periodenaam, -eenheid en -interval op voor elke ouderdomsperiode die u in de ouderdomsperiodedefinitie wilt opnemen. De regel met 0 (nul) in het veld Eenheid staat voor de datum waarop de analyse is uitgevoerd. Bij regels die hieraan voorafgaan, bevat het veld Eenheid standaard de waarde -1, bij regels die hierop volgen, is de standaardwaarde 1. U kunt deze waarden wijzigen. Selecteer **Omhoog** en **Omlaag** om de regels opnieuw te rangschikken. De regel met de waarde 0 (nul) kan niet worden verplaatst.  
- Plaats de aanwijzer op de positie waar u een nieuwe regel wilt invoegen en klik op **Toevoegen**.  
- Selecteer een indicator om de ouderdomsperiode weer de geven in het formulier en de lijstpagina **Aanmaningen**. U kunt bijvoorbeeld een groene indicator selecteren voor een huidige periode, een gele indicator voor een periode van 30 dagen geleden en een rode indicator voor een periode van 90 dagen geleden.  
- De afdrukrichting selecteren voor de ouderdomsperiodedefinitie. Deze selectie bepaalt in welke volgorde de kolommen worden weergegeven in het rapport Ouderdom klant of het rapport Ouderdom leveranciers.  
  - Vooruit: kolommen worden afgedrukt in dezelfde volgorde als waarin de kopteksten in de tabel worden weergegeven, te beginnen met de bovenste rij.  
  - Achteruit: kolommen worden afgedrukt in omgekeerde volgorde als waarin de kolomkoppen in de tabel worden weergegeven, te beginnen met de onderste rij.    

## <a name="setup-collections-parameters"></a>Parameters voor incasso´s instellen
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Instellen > Parameters van module Klanten**.
2. Selecteer het tabblad **Aanmaningen**.
3. Vouw de sectie **Standaardwaarden incasso** uit of samen.
- Selecteer een ouderdomsperiodedefinitie voor de standaardouderdomsmomentopname die wordt gebruikt op het formulier **Aanmaningen**.  
- Selecteer een team incassomedewerkers die worden toegewezen op het formulier **Incassomedewerker**. Alleen teams van het type Aanmaningen worden weergegeven in de lijst.  
4. Vouw de sectie **Afschrijven** uit of samen.
- Selecteer de journaalnaam die wordt ingesteld voor dagelijkse grootboekjournalen en moet worden gebruikt wanneer een transactie wordt afgeschreven met behulp van het formulier **Aanmaningen** of gerelateerde lijstpagina's.  
- Selecteer de standaardredencode die moet worden gebruikt wanneer afschrijvingstransacties worden gemaakt met behulp van het formulier **Aanmaningen** of gerelateerde lijstpagina's.  
- Selecteer deze optie als u een aparte journaalregel voor btw-bedragen wilt maken wanneer afschrijvingen worden gemaakt met behulp van de pagina **Aanmaningen** of gerelateerde lijstpagina's. Als u deze optie selecteert, kunt u eenvoudig de btw-bedragen volgen die een rol spelen bij afschrijvingstransacties. U kunt de btw-bedragen afzonderlijk volgen zodat u eenvoudiger uw btw-belastingschuld voor de betrokken periode kunt aanpassen.  
5. Vouw de sectie **E-mailsjabloon** uit of samen.
- Selecteer de e-mailsjabloon die moet worden gebruikt wanneer u een e-mail verzendt met behulp van de actie **E-mail > Transacties** naar contactpersoon op het formulier **Aanmaningen**.  
- Selecteer de e-mailsjabloon die moet worden gebruikt wanneer u een klantoverzicht als bijlage per e-mail verzendt met behulp van de actie **E-mail > Verklaring** naar contactpersoon op het formulier **Aanmaningen**.  
- Selecteer de e-mailsjabloon die moet worden gebruikt wanneer u een e-mail verzendt met behulp van de actie **E-mail > Transacties** naar verkoper op het formulier **Aanmaningen**.  

## <a name="age-customer-balance"></a>Ouderdom van klantsaldo berekenen
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Periodieke teaken > Ouderdom van klantsaldi berekenen**.
- Selecteer een ouderdomsperiodedefinitie. Tijdens het ouderdomsmomentopnameproces wordt de ouderdom van transacties berekend volgens de ouderdomsperioden die zijn gedefinieerd in de geselecteerde definitie van ouderdomsperioden.  
- Een klantverzameling selecteren. U kunt dit veld leeg laten als u een ouderdomsmomentopname wilt maken voor alle klanten. Als u een klantverzameling selecteert, wordt het ouderdomsmomentopnameproces alleen toegepast op klantrekeningen die deel uitmaken van die klantverzameling. De geselecteerde klantverzameling moet van het type Ouderdomsmomentopname zijn.  
- Het type datum selecteren waarop u de ouderdomsmomentopname moet worden gebaseerd.  
  - Transactiedatum: de ouderdom van elke transactie wordt berekend op basis van de transactiedatum.    
  - Vervaldatum: de ouderdom van elke transactie wordt berekend op basis van de vervaldatum.    
  - Documentdatum: de ouderdom van elke transactie te berekenen op basis van de documentdatum.  
- De datum selecteren die moet worden gebruikt als huidige datum voor de ouderdomsmomentopname. Ouderdomsperioden worden berekend op basis van deze datum.    
  - Datum van vandaag: gebruik de systeemdatum. Gebruik deze optie als het ouderdomsmomentopnameproces moet worden verwerkt in een terugkerende batchtaak. Als u deze optie gebruikt, kan de terugkerende batchtaak periodiek worden uitgevoerd en wordt de systeemdatum van dat moment gebruikt.    
  - Geselecteerde datum: gebruik een datum die u opgeeft. Als u deze optie selecteert, moet u een ouderdomsdatum invoeren.  
2. Selecteer **OK**.

## <a name="view-aged-customer-balances"></a>Vervallen klantsaldi weergeven
1. Ga in het navigatievenster naar **Modules > Crediteringen en aanmaningen > Aanmaningen > Vervallen saldi**.
- Gebruik deze lijstpagina om klantsaldi en op ouderdom gerangschikte bedragen op ouderdomsperiode weer te geven. Deze gegevens worden opgeslagen in een ouderdomsmomentopname. De ouderdomsperioden worden bepaald door de ouderdomsperiodedefinitie die wordt gebruikt. De ouderdomsperiodedefinitie is afkomstig van de klantverzameling, als er één is opgegeven voor de verzamelingquery. Als de klantverzameling geen ouderdomsperiodedefinitie heeft, wordt de standaardouderdomsperiodedefinitie gebruikt die wordt opgegeven in het formulier Parameters van module Klanten.  
2. Vouw het feitenvak **Contactpersoon** uit. Hier kunt u contactgegevens weergeven:
- Contactpersoon aanmaningen voor de klant.  
- Standaardverkoper voor de klant.  
3. Vouw het feitenvak **Kredietlimiet** uit.
- Gebruik het feitenvak **Kredietinformatie** om de kredietlimiet en het huidige saldo voor de klant te bekijken.  

## <a name="view-customer-collections-details"></a>Details van klantaanmaningen weergeven
1. Zorg ervoor dat de gewenste record is geselecteerd.
2. Vouw de feitenvakken **Adres**, **Contactpersoon**, **Ouderdom** en **Kredietlimiet** uit om de gegeven informatie weer te geven.
3. Selecteer **Incasso** in het actievenster.
- De ouderdomsmomentopname voor de klant bijwerken met de huidige datum als de ouderdomsdatum waarmee de transactiedatums worden vergeleken. Als de ouderdomsmomentopname informatie over meerdere rechtspersonen bevat, bevat de bijgewerkte ouderdomsmomentopname informatie voor dezelfde reeks rechtspersonen. Bedragen worden opgeslagen in de valuta voor de boekhouding van de rechtspersoon waarbij u bent aangemeld tijdens het bijwerken van de ouderdomsmomentopname.  
- Selecteer een ouderdomsperiodedefinitie. Standaard wordt de ouderdomsperiodedefinitie weergegeven die is gekoppeld aan de ouderdomsmomentopname voor de klant. De ouderdomsperiodedefinitie bepaalt de ouderdomsperioden en bedragen die worden weergegeven in de feitenvakken **Vervallen saldi** en **Kredietinformatie**.  
- Een menu met de volgende opties openen:    
  - Bedrijf – Bedragen weergeven in de feitenvakken Vervallen saldi en Kredietinformatie in de valuta voor boekhouding van de rechtspersoon.  
  - Klant - bedragen weergeven in de feitenvakken Verouderde saldi en Kredietinformatie in de valuta van de klant.  
- Een of meer rechtspersonen selecteren in de ouderdomsmomentopname van de klant waarvoor u informatie wilt weergeven. De rechtspersonen die in de lijst worden weergegeven, zijn geselecteerd tijdens het maken van de ouderdomsmomentopname.  
- Het rekeningoverzicht van de klant weergeven in Microsoft Excel-indeling. U kunt een begindatum voor het bereik van transacties selecteren die in het overzicht moeten worden opgenomen, en bepalen of u alleen openstaande transacties of openstaande en vereffende transacties wilt opnemen. Als de ouderdomsmomentopname informatie voor meerdere rechtspersonen bevat, worden de transacties voor alle rechtspersonen opgenomen.  
- Open het formulier **Documenten** waarin u documenten of notities kunt maken of bewerken.  
4. Selecteer **Communiceren** in het actievenster.  
- Outlook openen waarin u een e-mailbericht kunt verzenden naar de contactpersoon die is opgegeven in het veld Contact. Als er geen contactpersoon voor incasso´s is opgegeven, wordt het primaire adres voor de klant gebruikt. Als er geen primaire contactpersoon is opgegeven, worden e-mailberichten verzonden naar het eerste adres in het formulier **Contactpersonen**. De transacties die worden geselecteerd, worden opgenomen als bijlage. De bijlage is in de Excel-indeling en bevat drie werkbladen. Een e-mailsjabloon voor berichten aan klantcontactpersonen kan in het formulier **Parameters van module Klanten** worden opgegeven.  
- Deze knop is niet beschikbaar als de contactpersoon die in dit formulier is geselecteerd, geen e-mailadres heeft ingesteld.  
- Bereid een overzicht voor en open Outlook, waar u een e-mailbericht met een gekoppeld overzicht kunt verzenden naar het adres dat is opgegeven in het veld **Contactpersoon**. Als er geen contactpersoon voor incasso´s is opgegeven, wordt het primaire adres voor de klant gebruikt. Als er geen primaire contactpersoon is opgegeven, worden e-mailberichten verzonden naar het eerste adres in het formulier **Contactpersonen**.  
- Deze knop is niet beschikbaar als de contactpersoon die in dit formulier is geselecteerd, geen e-mailadres heeft ingesteld.  
- Outlook openen waarin u een e-mailbericht kunt verzenden naar de werknemer die is opgegeven als de vertegenwoordiger die aan de klant is toegewezen werknemer. Als er transacties zijn geselecteerd, worden deze opgenomen als bijlage. De bijlage is in de Excel-indeling en bevat twee werkbladen. Een e-mailsjabloon voor berichten naar verkopers kan in het formulier **Parameters van module Klanten** worden opgegeven.  
- Deze knop is niet beschikbaar als de verkoper die in dit formulier wordt weergegeven, geen e-mailadres heeft ingesteld.  
- Bekijk en voer acties uit op transacties voor de klant. Als u gecentraliseerde betalingen gebruikt, is de informatie voor alle rechtspersonen opgenomen die in de ouderdomsmomentopname van de klant is opgenomen. U kunt de informatie over de rechtspersoon beperken door **Bedrijf** in de groep **Selecteren** in het actievenster te selecteren.  
- De verzamelingenstatus voor de geselecteerde transacties wijzigen.    
  - Niet betwist: er zijn geen incassoacties voor de transactie uitgevoerd.    
  - Betwist: de klant heeft u geïnformeerd dat er een probleem is met de transactie.    
  - Beloofd te betalen: de klant is akkoord gegaan met betaling van het transactiebedrag.    
  - Opgelost: alle problemen met de transactie zijn opgelost en er zijn geen aanvullende incassoacties vereist.  
- Open een menu en selecteer een van de volgende opties om op te geven welke transacties in dit formulier moeten worden weergegeven:    
  - Openen – Alleen transacties weergeven die niet zijn vereffend.    
  - Geopend en afgesloten: alle transacties weergeven, zowel vereffend als niet vereffend.  
- De geselecteerde betaling verwerken als betaling met ontoereikend saldo (NSF).    
  - Deze knop is alleen beschikbaar als de geselecteerde transactie een betaling is (een creditsaldo zonder een factuur) die is ingevoerd in een betalingsjournaal, als er een bankrekening is toegewezen aan de transactie, en de betaling niet eerder is geannuleerd.  
- De geselecteerde transacties afschrijven.  
- De geselecteerde transacties markeren voor vereffening met elkaar.  
- Open het formulier **Oorspronkelijk document** waarin u het document voor de geselecteerde transactie kunt weergeven en afdrukken.  
- Open een **menu** met de volgende opties:    
  - Aanmaningen – Alleen activiteiten weergeven die zijn gemaakt in het formulier Aanmaningen.    
  - Alle: alle activiteiten voor de klant weergeven, ongeacht waar de activiteiten zijn gemaakt.  
- Open een **menu** met de volgende opties:    
  - Openen – Alleen activiteiten weergeven die niet afgesloten zijn.    
  - Geopend en afgesloten: alle activiteiten weergeven, ongeacht de status.  
- Een incassoaanvraag selecteren die is toegewezen aan de klant, of dit veld leeg laten. Als er een aanvraag is geselecteerd, worden alleen transacties en activiteiten die aan de aanvraag zijn gekoppeld, in dit formulier weergegeven.  
5. Selecteer **Lijst weergeven**.
- Een klantrekening selecteren of de standaardinvoer accepteren. Standaard is dit de geselecteerde klantrekening op de lijstpagina of in het formulier van waaruit u dit formulier hebt geopend. Als u het formulier vanuit een lijstpagina hebt geopend, zijn de klanten in de lijst de klanten die in de incassoverzameling zijn opgenomen die op de lijstpagina wordt gebruikt.  

