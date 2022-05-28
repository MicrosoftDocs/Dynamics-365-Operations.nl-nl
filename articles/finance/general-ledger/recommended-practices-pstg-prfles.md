---
title: Aanbevolen praktijken voor boekingsprofielen
description: In dit onderwerp worden de aanbevolen praktijken beschreven voor de configuratie van boekingsprofielen.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 211dc42b80089eb1f59a435f09d6e9d9f956736b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734270"
---
# <a name="recommended-practices-for-posting-profiles"></a>Aanbevolen praktijken voor boekingsprofielen

Er zijn verscheidene aanbevolen praktijken die u moet volgen wanneer u boekingsprofielen in het systeem configureert. In dit onderwerp worden de verschillende scenario's en de bijbehorende aanbevolen procedures beschreven.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>De vlag Handmatige invoer niet toestaan instellen

Op de pagina **Hoofdrekeningen** moet het selectievakje **Handmatige invoer niet toestaan** worden ingeschakeld voor de hoofdrekening die wordt gebruikt voor een boekingsprofiel. Met deze instelling wordt voorkomen dat gebruikers een journaalpost handmatig naar de hoofdrekening boeken. Hierdoor zorgt u dat de subadministratie in balans blijft met het grootboek en het afstemmingsproces eenvoudiger wordt.

Als correcties zijn vereist voor een rekening die wordt gecontroleerd door het systeem en automatisch wordt geboekt, kunt u een van de volgende methoden gebruiken:

- Maak een secundaire hoofdrekening waar de correcties kunnen worden geboekt. Gebruik vervolgens een totaalrekening of een speciale rij in uw financiële rapporten om de rekeningen te groepen en bij elkaar op te tellen.
- Keer de oorspronkelijke transacties in het desbetreffende boek om, maak eventuele vereiste correcties en boek de transactie vervolgens opnieuw via hetzelfde boek.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Boekingsprofielen wijzigen als er transacties bestaan

Als u een boekingsprofiel wijzigt als er transacties zijn, kan de afstemming mislukken en kunnen sub- en grootboek niet meer in balans komen. In het algemeen is het raadzaam om het boekingsprofiel **niet** te wijzigen als er transacties zijn.

Als wijzigingen vereist zijn, gebruikt u de volgende richtlijnen om de integriteit van het systeem te waarborgen:

- De wijzigingen aanbrengen tijdens de sluiting van een financiële periode.
- De wijzigingen aanbrengen wanneer er geen andere transacties voorkomen in het systeem.
- Het grootboek valideren en het afstemmen op de subadministratie voor en nadat u de wijzigingen hebt aangebracht.
- Geboekte transacties worden niet bijgewerkt als u het boekingsprofiel wijzigt. Overweeg zorgvuldig of er aanpassingsposten vereist zijn voor uw wijziging.
- Als u voorraadboekingsprofielen wijzigt, moet u overwegen wat de gevolgen van die wijzigingen zijn voor uw beschikbare voorraad- en grootboeksaldi. Voor sommige wijzigingen moet u de voorraad bijvoorbeeld terugbrengen naar 0 (nul), de voorraad sluiten en vervolgens de voorraad weer opnemen nadat de wijzigingen zijn aangebracht.
- Test altijd uw wijzigingen in een niet-productieomgeving voordat u ze in productie aanbrengt.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Databaselogboeken gebruiken om wijzigingen in boekingsprofielen te controleren

Overweeg om een databaselogboekregistratie in te stellen voor elk boekingsprofiel en voor de parametertabellen die de boeking regelen. Als vervolgens een parameter of profiel wordt gewijzigd, wordt er een volledige controlerecord uitgevoerd voor de waarde die is gewijzigd, wie deze heeft gewijzigd, wanneer deze is gewijzigd en wat de vorige waarde was. Deze informatie kan cruciaal zijn tijdens het afstemmingsproces, en uw auditor vereist wellicht de ondersteunende documentatie.

Zie [Databaselogboeken configureren](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md) voor meer informatie.

Gebruik de volgende tabel als verwijzing voor algemene tabelnamen die zijn gerelateerd aan boekingsprofielen en gerelateerde boekingsparameters.

| Paginanaam | Navigatiepad | Tabelnaam |
|-----------|-----------------|------------|
| Parameters van module Leveranciers | Leveranciers &gt; Instellingen &gt; Parameters van module Leveranciers | VendParm |
| Boekingsprofiel van leverancier | Leveranciers &gt; Instellen &gt; Boekingsprofiel van leverancier | VendPosting |
| Toeslagcode | Leveranciers &gt; Instelling van toeslagen &gt; Toeslagcode of Klanten &gt; Instelling van toeslagen &gt; Toeslagcode | MarkupTable |
| Betalingsmethoden | Leveranciers &gt; Betalingsinstelling &gt; Betalingsmethoden | VendPaymMode |
| Contantkortingen | Leveranciers &gt; Betalingsinstelling &gt; Contantkortingen of Klanten &gt; Betalingsinstelling &gt; Contantkortingen | CashDisc |
| Betalingskosten (leverancier) | Leveranciers &gt; Betalingsinstelling &gt; Betalingskosten | VendPaymFee |
| Parameters van module Klanten | Klanten &gt; Instellingen &gt; Parameters van module Klanten | CustParm |
| Boekingsprofielen van klant | Klanten &gt; Instellen &gt; Boekingsprofiel van klant | CustPosting |
| Betalingsmethoden | Klanten &gt; Betalingsinstelling &gt; Betalingsmethoden | CustPaymMode |
| Betalingskosten (Klant) | Klanten &gt; Betalingsinstelling &gt; Betalingsmethoden | CustPaymFee |
| Leaseparameters voor activa | Activa leasen &gt; Instellingen &gt; Parameters voor activa leasen | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankrekeningen | Contanten en bankbeheer &gt; Bankrekeningen &gt; Bankrekeningen | BankAccountsTable |
| Banktransactietypen | Kas- en bankbeheer &gt; Instellingen &gt; Banktransactietypen | BankTransType |
| Schrappingregels | Consolidaties &gt; Instellen &gt; Schrappingsregel | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Onkostencategorieën | Onkostenbeheer &gt; Instellingen &gt; Algemeen &gt; Onkostencategorieën | ProjCategories |
| Vaste-activaparameters | Vaste activa &gt; Instellen &gt; Parameters vaste activa | AssetParameters |
| Boekingsprofielen vaste activa | Vaste activa &gt; Instellingen &gt; Boekingsprofielen voor vaste activa | AssetLedgerAccounts<br>AssetDisposalParameters |
| Rekeningen voor valutaherwaardering | Grootboek &gt; Valuta's &gt; Rekeningen voor valutaherwaardering | CurrencyLedgerGainLossAccount |
| Rekeningen voor automatische transacties | Grootboek &gt; Boekingsinstellingen &gt; Rekeningen voor automatische transacties | LedgerSystemAccounts |
| Intercompany-boekhouding | Grootboek &gt; Boekingsinstellingen &gt; Intercompany-rekeningen | LedgerIntercompany |
| Boekdefinities voor transacties | Grootboek &gt; Boekingsinstellingen &gt; Transactieboekingsdefinities | JournalizingDefinitionTrans |
| Boekdefinities | Grootboek &gt; Boekingsinstellingen &gt; Boekingsdefinities | JournalizingDefintion |
| Boeking (Voorraad) | Voorraadbeheer &gt; Instellen &gt; Boeken &gt; Boeken | InventPosting |
| Codes voor kostentype | Francoprijzen &gt; Kosten instellen &gt; Kostentypecodes | ITMCostTypeTable |
| Bronnen | Productiebeheer &gt; Instellen &gt; Resources &gt; Resources | WrkCtrTable |
| Resourcegroepen | Productiebeheer &gt; Instellen &gt; Resources &gt; Resourcegroepen | WrkCtrResourceGroup |
| Productiegroepen | Productiebeheer &gt; Instellen &gt; Productie &gt; Productiegroep | ProdGroup |
| Kostencategorieën | Productiebeheer &gt; Instellen &gt; Routes &gt; Kostencategorieën | ProjCategory |
| Projectgroepen | Projectbeheer en boekhouding &gt; Instellen &gt; Boeken &gt; Projectgroepen | ProjGroup |
| Boeking in grootboek instellen (Projecten) | Projectbeheer en boekhouding &gt; Instellingen &gt; Boeken &gt; Boeking in grootboek instellen | ProjPosting |
| Standaardtegenrekening voor uitgaven | Projectbeheer en boekhouding &gt; Instellingen &gt; Boeken &gt; Standaardtegenrekeningen voor uitgaven | ProjDefaultOffsetSetup |
| Boekingsprofielen voor kortingsbeheer | Kortingsbeheer &gt; Boekingsinstellingen voor kortingsbeheer &gt; Boekingsprofielen voor kortingsbeheer | TAMRebatePosting |
| Groep boekingen in grootboek (belasting) | Belasting &gt; Instellingen &gt; Btw &gt; Grootboekboekingsgroep | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Groepen wijzigen als er transacties zijn

Wees voorzichtig bij het wijzigen van groepen in hoofdgegevens. Als u groepen gebruikt om uw boekingsprofielen te definiëren, kan elke wijziging in een groep in een hoofdrecord een negatieve invloed hebben op de mogelijkheid om het grootboek af te stemmen op de subadministratie. U kunt bijvoorbeeld het voorraadboekingsprofiel configureren voor verkooporderopbrengsten zodat er voor elke artikelgroep een andere opbrengstrekening wordt gebruikt. Als u de artikelgroep wijzigt die na transacties aan een artikel is toegewezen, wordt de opbrengst van de nieuwe transacties naar de bijgewerkte rekening geboekt. Alle opbrengsten die zijn geboekt vóór de wijziging, blijven echter behouden op de oorspronkelijke rekening.

## <a name="testing-posting-profiles"></a>Boekingsprofielen testen

Voordat u live gaat en nadat u eventuele wijzigingen of toevoegingen aan uw boekingsprofielen of gerelateerde parameters hebt aangebracht, moet u elk scenario testen. U moet elk boekingstype minimaal testen om te controleren of de boeking juist werkt. De aanbevolen methode is echter om elke boekingsprofieltransactie en -combinatie te testen.

U hebt bijvoorbeeld twee klantboekingsprofielen, met elk drie registraties die specifiek zijn voor klantengroepen. In dit geval moet u elk transactietype testen.

**Boekingsprofielen:**

- **GEN**: het algemene boekingsprofiel met een groep voor werknemers, klanten en intercompany. Elke groep verwijst naar een andere handelsrekening van klanten.
- **PRE**: het vooruitbetalingsboekingsprofiel met één record voor alle vooruitbetalingen die naar de vooruitbetalingsrekeningen van de klant wijst.

### <a name="testing-scenarios"></a>Scenario's testen

- Vrije-tekstfactuur voor een klant in de groep **Werknemer** die het **GEN-boekingsprofiel** gebruikt
- Vrije-tekstfactuur voor een klant in de groep **Werknemer** die het **PRE-boekingsprofiel** gebruikt
- Verkooporderfactuur voor een klant in de groep **Werknemer** die het **GEN-boekingsprofiel** gebruikt
- Verkooporderfactuur voor een klant in de groep **Werknemer** die het **PRE-boekingsprofiel** gebruikt
- Betalingsjournaal voor een klant in de groep **Werknemer** die het **GEN-boekingsprofiel** gebruikt
- Betalingsjournaal voor een klant in de groep **Werknemer** die het **PRE-boekingsprofiel** gebruikt

Herhaal in het voorgaande voorbeeld één testscenario voor elke klantengroep en herhaal elke groep testscenario's voor elk aanvullend transactietype (bijvoorbeeld projectfacturen en servicebeheer).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Grootboek afstemmen op subadministratie

Het grootboek moet elke periode worden afgestemd op de subadministratie. Veel modules bevatten standaardrapporten die kunnen worden gebruikt bij het afstemmen. Afhankelijk van uw lokale vereisten moet u mogelijk echter aangepaste rapporten ontwikkelen of de bestaande rapporten uitbreiden om aan uw rapportagevereisten te voldoen.

We raden u aan om als test een periode af te sluiten en elk van uw subadministraties af te stemmen op het grootboek voordat u ze ingebruikneemt. We raden u ook aan om een testoverstap uit te voeren voor alle openstaande saldi en openstaande transacties voordat u live gaat. Als onderdeel van dit proces moet u een volledige afstemming uitvoeren om te controleren of de migratie van saldi en openstaande transacties naar de verouderde systemen wordt voltooid, en dat alle grootboeken in balans zijn voordat nieuwe transacties worden gemaakt.
