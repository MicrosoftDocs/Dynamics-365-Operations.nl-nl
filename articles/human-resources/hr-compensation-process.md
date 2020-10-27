---
title: Compensatie verwerken
description: Met compensatieverwerking kunt u nieuwe basiscompensatiebedragen berekenen voor uw werknemers, op basis van salarisaanpassingen, loonsverhoging voor verdienste en prestaties.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 979a4f311d59cb51cdf0fc6ce85d5b3338ffa870
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958712"
---
# <a name="process-compensation"></a>Compensatie verwerken

Met compensatieverwerking kunt u nieuwe basiscompensatiebedragen berekenen voor uw werknemers, op basis van salarisaanpassingen, loonsverhoging voor verdienste en prestaties. In dit artikel wordt uitgelegd hoe de algemene stroom van compensatie wordt verwerkt voor vaste-compensatieplannen zonder rekening te houden met prestaties van de werknemer.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>De nieuwe compensatiebedragen en -budgetten plannen
Als u uw werknemers een loonsverhoging voor verdienste wilt geven, moet u een budget voor vaste verhoging instellen voor al uw afdelingen: Compensatiebeheer > Koppelingen > Verdiensteverhogingsdoelen. (U kunt dit formulier ook openen via de afdeling: Organisatie > Afdelingen.) Hier kunt u nader specificeren of werknemers in een bepaalde vakbond of locatie een verschillend verhogingspercentage moeten krijgen. De velden **Budget** en **Valuta** zijn ter informatie en kunnen worden gebruikt om een valutabedrag voor het budget te vermelden.

## <a name="set-up-the-compensation-process"></a>Het compensatieproces instellen
Met een procesgebeurtenis kunt u de parameters voor de compensatieverwerking opgeven. Dit omvat de periode die moet worden geëvalueerd voor het bepalen van de compensatiebedragen en de datum waarop de nieuwe compensatiebedragen van kracht worden.

U kunt desgewenst een aanstellingsdatum voor omgeslagen vast loon opnemen, als een van uw vaste-compensatieplannen een aanstellingsregel van het type Procent gebruikt. Voor deze plannen krijgt iedereen die in dienst is genomen na de cyclusbegindatum en vóór de aanstellingsdatum voor omgeslagen vast loon 100% van hun berekende verhoging voor verdienste of algemene verhoging. Iedereen die is aangesteld na de aanstellingsdatum voor omgeslagen vast loon en vóór de cycluseinddatum ontvangt een deel van de berekende verhoging, op basis van het aantal dagen in de cyclus waarin zij in dienst waren. Als onze cyclus bijvoorbeeld loopt van 1 januari tot en met 31 december en de aanstellingsdatum voor omgeslagen vast loon is bepaald op 1 april, krijgt een werknemer die in maart in dienst is genomen de volledige berekende verhoging. Een werknemer die in dienst is genomen op 1 juli ontvangt daarentegen ongeveer de helft van de berekende verhoging.

De procesgebeurtenisdatum **Punt-in-tijd** wordt alleen gebruikt voor het verwerken van bepaalde plannen voor variabele compensatie en worden hier niet behandeld. De **Controledeadline** is de uiterste termijn voor het doen van aanbevelingen, zodat de nieuwe compensatiebedragen in de record van de werknemer kunnen worden geladen. De controledatum is alleen ter informatie.

Nadat de parameters van de procesgebeurtenis zijn opgeslagen, klikt u op de knop **Instellen** om aan te geven welke plannen u in deze procesuitvoering wilt opnemen en welke vaste-compensatieacties voor elk plan moeten worden uitgevoerd.

Klik op de knop **Toevoegen** op het tabblad **Plannen** om een compensatieplan toe te voegen aan de procesgebeurtenis. De kolommen **Andere hefboomwerking gebruiken**, **Hefboomwerkingsfactor** en **Beschrijving van hefboomwerking** worden alleen gebruikt voor variabele-compensatieplannen en worden niet behandeld in dit artikel.

Sla de record op en klik vervolgens op de knop **Toevoegen** op het tabblad **Acties** om vaste-compensatieacties voor het geselecteerde plan toe te voegen. Gebruik de optie **Aanbevelingen inschakelen**, als u een bedrag wilt kunnen invoeren dat afwijkt van de berekende richtlijnverhoging voor de actie. Als u een actie wilt berekenen op basis van het resultaat van de vorige actie om zo meerdere compensatieacties aan elkaar te koppelen, schakel dan de optie **Vorig resultaat gebruiken** in. Vaste-compensatieacties zijn typen compensatielogica waaraan u een beschrijvende naam kunt geven. Bij Schaal- en Bandplannen kunt u alleen vaste-compensatieacties van de volgende typen toevoegen:

| Type vastecompensatieactie | Functionaliteit                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eigen vermogen                        | Salarisaanpassingsacties vergelijken de het salaristarief van de werknemer op de einddatum van de cyclus met het laagste referentiepunt voor het niveau dat is aangegeven voor de functie van de werknemer. Als het salaristarief van de werknemer lager is dan het minimum referentiepunt, wordt de verhoging berekend die nodig is om de werknemer naar het laagste punt in dat bereik te krijgen.                                                                                |
| Verdienste                         | Acties voor verdienste berekenen een verhoging op basis van het salaristarief van de werknemer vanaf de einddatum van de cyclus en het verhogingspercentage in de vaste-budgetverhoging voor de afdeling, de vakbond en de locatie van de werknemer.                                                                                                                                                                                         |
| Algemeen                       | Algemene acties berekenen een verhoging op basis van een percentage of geven de werknemers een vast bedrag. Dit wordt bepaald op basis van de instellingen voor **Vaste compensatie** op het tabblad **Algemeen**.                                                                                                                                                                                                                        |
| Promotie                     | Promotieacties bieden een benoemde locatie waar u een verhoging kunt toekennen. Let er daarom op dat u de optie **Aanbeveling inschakelen** activeert, zodat u een aanbeveling kunt invoeren voor de werknemers die promoties ontvangen.  Bij werknemers zonder een aanbevolen verhoging wordt niet de **Promotie**-actie toegevoegd aan hun vaste-compensatierecords.                                                                       |
| Andere niveauwijziging            | In het voorgaande voorbeeld is **Terugzetten in functie** de naam van de **Vaste-compensatieactie** met het type **Andere niveauwijziging**. Hiermee wordt een richtlijnverhoging van 0 (geen wijziging) gegenereerd, zodat u een aanbevolen bedrag kunt invoeren om het salaristarief van de werknemer aan te passen. (Let erop dat u de optie **Aanbeveling inschakelen** activeert.) Bij werknemers zonder een aanbeveling wordt deze actie niet toegevoegd aan de vaste-compensatierecords. |

U kunt alleen **Vaste-compensatieacties** van het type Stap toevoegen aan een Stappenplan.

| Type vastecompensatieactie | Functionaliteit                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stap                           | Geef op het tabblad Algemeen aan of deze Stap-actie de werknemers 0 stappen, één stap of twee stappen naar voren moet verplaatsen.                                                                                  |
|                                | **0 stappen**: De werknemer ontvangt het salaristarief voor de stap waarop hij/zij zich momenteel bevindt.                                                                                                                      |
|                                | **1 stap**: Het systeem controleert of de werknemer al bij het laatste referentiepunt voor diens niveau is.                                                                                             |
|                                | **2 stappen**: Het systeem verplaatst de werknemer twee stappen naar voren op het huidige niveau. Het systeem verplaatst de werknemer mogelijk slechts één stap (of zelfs nul stappen) als deze het laatste referentiepunt voor hun niveau bereikt. |

## <a name="run-the-compensation-process"></a>Het compensatieproces uitvoeren
Nadat de procesgebeurtenis is ingesteld met de nodige datumvelden, plannen en acties, kunt u klikken op **Proces uitvoeren** op de pagina **Procesgebeurtenis**. Hiermee opent u het dialoogvenster **Compensatieproces uitvoeren**. Klik in dit dialoogvenster de optie **Resultaten van verwerking weergeven** aan om te zien hoe de compensatiebedragen voor elke werknemer zijn berekend. Als u op **OK** klikt, wordt het compensatieproces uitgevoerd voor alle werknemers in de geselecteerde compensatieplannen vanaf de cycluseinddatum.

## <a name="view-the-process-results"></a>De verwerkingsresultaten weergeven
Om de verwerkingsresultaten te bekijken, opent u de pagina **Verwerkingsresultaten**. Telkens wanneer de procesgebeurtenis wordt uitgevoerd, wordt een compensatiegebeurtenis gemaakt. Op deze manier kunt u testruns uitvoeren, correcties aanbrengen en de compensatiegebeurtenis meerdere keren uitvoeren, om te zien hoe verschillende wijzigingen de werknemerscompensatie beïnvloeden.

De pagina **Verwerkingsresultaten** bevat informatie over de verwerkingsuitvoering, inclusief wanneer de uitvoering plaatsvond, de gebruiker die het proces uitvoerde en of er fouten optraden tijdens het uitvoeren van de verwerking. U kunt ook de optie **Vergrendeld** inschakelen om de knop de **Compensatie laden** uit te schakelen en te voorkomen dat iemand de compensatiegebeurtenissen in de werknemersrecords laadt. Als u klikt op de knop **Werknemersresultaten**, wordt de lijst met werknemers getoond die zijn opgenomen in de uitvoering.

De optie **Resultaten werknemer** geeft informatie over het proces zelf, alsmede eventuele compensatieacties die in het proces worden uitgevoerd. De sectie **Vaste compensatie** sectie bevat een record voor elke actie die is opgenomen in de procesgebeurtenis voor het compensatieplan. De kolommen **Huidige richtlijn** en **Aanbeveling** geven meer informatie voor de actie die is geselecteerd in de sectie **Vaste compensatie**. Als voor de actie de optie **Aanbevelingen inschakelen** was geactiveerd, zijn de velden Aanbevelingen bewerkbaar. U kunt dan handmatig de bedragen voor de werknemers aanpassen. Opmerking: Als u de optie **Vorig resultaat gebruiken** had ingeschakeld voor de actie op de procesgebeurtenis, moet u de bedragen voor eventuele afhankelijke acties handmatig bijwerken.

Wanneer de compensatiebedragen voor een werknemer zijn gecontroleerd en eventuele aanpassingen aan de aanbevolen waarden zijn doorgevoerd, kunt u de **Status** op de regel **Werknemersgebeurtenis** wijzigen om aan te geven of de gebeurtenis is goedgekeurd of moet worden genegeerd. Desgewenst kunt u eventuele wijzigingen in de aanbeveling van de werknemer wissen, door te klikken op de knop **Herberekenen**. Hierdoor krijgt de bestaande werknemersgebeurtenis de status Negeren en wordt een nieuwe werknemersgebeurtenis aangemaakt met de herberekende waarden.

## <a name="loading-approved-compensation-changes"></a>Goedgekeurde compensatiewijzigingen laden
Wanneer de status van een of meer werknemersgebeurtenissen is gewijzigd in Goedgekeurd, kunnen ze worden geladen in de vaste-compensatierecords van de werknemers. U kunt dit doen door elke werknemersgebeurtenis apart te selecteren en te klikken op de knop **Werknemerscompensatie laden** op de pagina **Resultaten werknemer**, of door te klikken op **Compensatie laden** op de pagina **Verwerkingsresultaten** om zo alle goedgekeurde werknemersgebeurtenissen tegelijk te laden.

Als u klikt op **OK** in het dialoogvenster **Compensatie laden**, voegt u de compensatieactieregels die een waarde hoger dan nul hebben in de pagina **Vaste compensatie voor werknemer**.
