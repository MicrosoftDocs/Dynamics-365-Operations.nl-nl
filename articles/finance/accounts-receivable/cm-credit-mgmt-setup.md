---
title: Parameters voor kredietbeheer instellen
description: In dit artikel worden de opties beschreven die u kunt gebruiken om kredietbeheer te configureren om tegemoet te komen aan de vereisten van uw bedrijf.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8955518e7b5c0200d3827c1c22b7d150a09be244
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799540"
---
# <a name="credit-management-parameters-setup"></a>Parameters voor kredietbeheer instellen

[!include [banner](../includes/banner.md)]

In dit artikel worden de opties beschreven die u kunt gebruiken om kredietbeheer te configureren om tegemoet te komen aan de vereisten van uw bedrijf. Als u de functies voor kredietbeheer wilt gaan gebruiken, stelt u de parameters in op de pagina **Parameters voor crediteringen en aanmaningen** (**Crediteringen en aanmaningen \> Instellen \> Parameters voor crediteringen en aanmaningen**).

## <a name="credit-parameters"></a>Kredietparameters

Er zijn vier sneltabbladen in de sectie **Krediet** waar u de parameters voor kredietbeheer kunt wijzigen: **Krediet geblokkeerd**, **Controlepunt voor kredietbeheer**, **Kredietbeheerstatistieken** en **Kredietlimieten**. In de volgende secties worden de instellingen beschreven die beschikbaar zijn op elk sneltabblad.

### <a name="credit-holds"></a>Kredietblokkeringen

- Stel de optie **Toestaan dat verkooporderwaarde wordt bewerkt nadat orderwachtstand is vrijgegeven** in op **Nee** om te vereisen dat de boekingsregels opnieuw worden gecontroleerd als de verkooporderwaarde (de berekende prijs) is verhoogd nadat de verkooporder is vrijgegeven vanuit de wachtstandenlijst.
- Selecteer in het veld **Redenen voor geannuleerde orders** de reden van de vrijgave die standaard wordt gebruikt wanneer een verkooporder wordt geannuleerd die in de wachtstand voor kredietbeheer stond.
- Stel de optie **Kredietlimiet van kredietgroepen van klant controleren** in op **Ja** als u de kredietlimiet van een kredietgroep van klant wilt controleren wanneer de klant voor een verkooporder tot een kredietgroep van klant behoort. De kredietlimiet voor de groep wordt gecontroleerd en als deze voldoende is, wordt de kredietlimiet voor de klant gecontroleerd.
- Stel de optie **Kredietlimiet controleren wanneer betalingsvoorwaarden veranderen** in op **Ja** als u wilt dat de classificatie van de betalingsvoorwaarden wordt gecontroleerd om na te gaan of de betalingsvoorwaarden op de verkooporder verschillen van de standaardbetalingsvoorwaarden voor de klant. Als de nieuwe betalingsvoorwaarden een hogere classificatie hebben dan de oorspronkelijke betalingsvoorwaarden, wordt de order in de wachtstand voor kredietbeheer geplaatst.
- Stel de optie **Kredietlimiet controleren wanneer een betalingskorting verandert** in op **Ja** als u wilt dat de classificatie van de betalingskorting wordt gecontroleerd om na te gaan of de contantkorting op de verkooporder verschilt van de standaardcontantkorting voor de klant. Als de nieuwe betalingskorting een hogere classificatie heeft dan de oorspronkelijke betalingskorting, wordt de order in de wachtstand voor kredietbeheer geplaatst.
- Selecteer in het veld **Reden voor het vrijgeven van gewijzigde orders** de reden voor vrijgave die standaard wordt gebruikt wanneer gewijzigde orders automatisch worden vrijgegeven uit de wachtstand voor kredietbeheer.
- Stel de optie **Blokkeerregel Kredietlimiet verlopen negeren wanneer vervaldatum leeg is** in op **Ja** als u het gedrag van de regel **Kredietlimiet verlopen** wilt beheren. Stel de optie in op **Nee** als u een order wilt blokkeren wanneer de vervaldatum leeg is.
- In Magazijnbeheer kunnen ladingen worden gemaakt op het moment dat de verkooporder wordt ingevoerd. Stel de optie **Geblokkeerde ladingsregels verwijderen** in op **Nee** als u verkooporderregels op de lading wilt laten staan wanneer een verkooporder in de kredietwachtstand staat. De lading kan niet worden verwerkt terwijl de verkooporder in de wachtstand staat. Stel de optie in op **Ja** als u verkooporderregels uit de lading wilt verwijderen wanneer een verkooporder in de kredietwachtstand staat. De lading kan dan worden verwerkt.
- Verkooporders kunnen automatisch worden vrijgegeven uit kredietbeheerbeoordeling. Selecteer in het veld **Reden om automatisch vrij te geven** de reden van vrijgave die standaard wordt gebruikt wanneer verkooporders automatisch worden vrijgegeven.
- Verkooporders kunnen automatisch worden vrijgegeven uit kredietbeheerbeoordeling. Selecteer in het veld **Automatisch vrijgeven** de optie **Zonder boeking** om de blokkering van een order vrij te geven. U moet het proces dat de order in de wachtstand heeft geplaatst handmatig uitvoeren. Selecteer **Met boeking** als u de order wilt boeken met hetzelfde boekingsproces dat is uitgevoerd toen de verkooporder in de wachtstand werd gezet.

### <a name="credit-management-checkpoint"></a>Controlepunt voor kredietbeheer

U kunt de timing instellen die wordt gebruikt om verkooporders te controleren op kredietproblemen. Het sneltabblad **Controlepunt voor kredietbeheer** identificeert de documentboekingsprocessen die de verwerking van regels voor kredietbeheer omvatten. U kunt ook de krediet regels controleren terwijl u een pro-forma boeking of een volledige boeking van de verkooporder doet. Schakel de selectievakjes in om de boekingsprocessen te definiëren die een order in de wachtstand moeten zetten als er een probleem wordt gevonden nadat de blokkeerregels van kredietbeheer zijn verwerkt.

U kunt ook het aantal respijtdagen definiëren voordat de kredietregels opnieuw worden gecontroleerd. Hoewel u kunt opgeven dat de regels voor kredietbeheer bij het boeken moeten worden gecontroleerd, worden de regels niet gecontroleerd gedurende het opgegeven aantal respijtdagen. Stel, u bevestigt een verkooporder op dag één en u geeft twee respijtdagen op voor de bevestigingsstap. In dit geval worden de kredietregels niet gecontroleerd bij de volgende boekingsstap (bijvoorbeeld het maken van een pakbon of de facturering van de order) tot dag vier. Op of na dag vier worden de regels opnieuw gecontroleerd als er een boeking plaatsvindt en verandert het aantal respijtdagen in de waarde die is opgegeven voor het volgende boekingscontrolepunt.

Als u het aantal respijtdagen niet opgeeft, worden de kredietregels gecontroleerd bij elke boekingsstap die is ingesteld voor het uitvoeren van regels voor kredietbeheer. Als u de verkooporder vrijgeeft zonder boeking en vervolgens weer dezelfde orderverwerkingsstap uitvoert, worden de kredietregels opnieuw gecontroleerd. Stel, een order wordt na een bevestiging in de wachtstand gezet, en u geeft deze vervolgens vrij met of zonder boeking. In dat geval wordt de order opnieuw in de wachtstand gezet als u deze opnieuw bevestigt. Gebruik respijtdagen als de order naar de volgende verwerkingsstap moet worden verplaatst zonder dat deze opnieuw in de wacht wordt gezet.

> [!Note]
> Als voor één boekingsperiode een respijtdag is ingevoerd, moeten alle boekingsdagen die zijn gemarkeerd voor boeking respijtdagen hebben.

- Schakel het selectievakje **Boeking** in als u de regels voor kredietbeheer wilt uitvoeren wanneer het boekingscontrolepunt wordt uitgevoerd dat op de regel wordt weergegeven. Als u het selectievakje niet inschakelt, worden de regels slechts eenmaal tijdens het gehele boekingsproces gecontroleerd.
- Als u het selectievakje **Boeking** inschakelt, geeft u het aantal respijtdagen op dat moet verstrijken voordat de blokkeerregels opnieuw worden gecontroleerd. U kunt geen respijtdagen toevoegen als het selectievakje **Boeking** is uitgeschakeld.
- Schakel het selectievakje **Pro forma** in als u de regels voor kredietbeheer wilt uitvoeren wanneer het pro-forma boekingscontrolepunt wordt uitgevoerd dat op de regel wordt weergegeven. In de meeste gevallen wordt het veld **Boeking** ingesteld op **Nee** in het dialoogvenster dat wordt weergegeven wanneer een verkooporder wordt geboekt.
- Als u het selectievakje **Boeking** inschakelt, geeft u het aantal respijtdagen op dat moet verstrijken voordat de blokkeerregels opnieuw worden gecontroleerd. U kunt geen respijtdagen toevoegen als het selectievakje **Boeking** is uitgeschakeld.

### <a name="credit-management-statistics"></a>Kredietbeheerstatistieken

Diverse statistieken voor kredietbeheer zijn opgenomen in het feitenvak **Statistieken voor klantkredietbeheer** op de pagina **Klant**. U moet verschillende waarden opgeven die nodig zijn om deze statistieken te berekenen. Voer in het feitenvak **Statistieken voor klantkredietbeheer** het aantal maanden in dat wordt gebruikt voor het berekenen van de volgende waarden:

1. Dagen uitstaande verkoop 1
2. Dagen uitstaande verkoop 2
3. Gemiddeld saldo 1
4. Gemiddeld saldo 2
5. Gemiddeld kredietlimietpercentage
6. Gemiddeld risicopercentage

### <a name="credit-limits"></a>Kredietlimieten

- In kredietbeheer wordt de kredietlimiet van de klant weergegeven in de valuta van de klant. U moet het wisselkoerstype voor de kredietlimiet opgeven in de valuta van de klant. Selecteer in het veld **Wisselkoerstype voor kredietlimiet** het type wisselkoers dat moet worden gebruikt om de primaire kredietlimiet om te zetten in de kredietlimiet van de klant.
- Stel de optie **Handmatig bewerken van kredietlimieten toestaan** in op **Nee** als u wilt voorkomen dat gebruikers kredietlimieten op de pagina **Klant** kunnen bewerken. Als deze optie is ingesteld op **Nee**, kunnen wijzigingen in de kredietlimiet van een klant alleen worden gedaan door het boeken van kredietlimietcorrecties voor klant.
- Stel de optie **Voorraadreserveringen overslaan** in op **Ja** om voorraadreserveringen te negeren wanneer de blokkeringsregels van creditbeheer worden gecontroleerd. In dit geval worden de hoeveelheden gecontroleerd en worden respijtperioden voor controlepunten ingeschakeld, ongeacht de voorraadreserveringshoeveelheid.
- Wanneer Creditbeheer is ingeschakeld, wordt de instelling van het veld **Bericht bij overschrijding van kredietlimiet** gebruikt om alleen vrije-tekstfacturen te verwerken. Berichten worden nog steeds aan verkooporders toegevoegd wanneer de klant de kredietlimiet heeft overschreden, maar de aanwezigheid van die berichten zorgt er niet voor dat de bevestiging wordt geblokkeerd en dat het afdrukken van orderverzamellijsten en pakbonnen of het boeken van facturen wordt voorkomen.

    Creditbeheer is standaard ingeschakeld, maar u kunt het uitschakelen. Als deze functie is ingeschakeld, gebruikt u de blokkeringsregels en controlepunten voor kredietbeheer om aan te geven wanneer klanten hun kredietlimiet hebben overschreden. Als deze is uitgeschakeld, kunt u door de berichten die aan verkooporders worden toegevoegd op basis van de instelling van het veld **Bericht bij overschrijding van kredietlimiet** aangeven wanneer klanten de kredietlimiet hebben overschreden.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Nummerreeksen en parameters voor gedeelde nummerreeksen

Een journaal-id is vereist om kredietlimietcorrecties te verwerken. U moet het nummer van de kredietlimietcorrectie toevoegen die moet worden gebruikt om de journaal-id te genereren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
