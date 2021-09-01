---
title: Migratie Valuta-gegevenstype voor Twee keer wegschrijven
description: In dit onderwerp wordt beschreven hoe u het aantal decimalen wijzigt dat door Twee keer wegschrijven wordt ondersteund voor valuta.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 1bfb719b20694db9af8a2a013786b8309c23c9d963c8746346930bbde96e9bbb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725131"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migratie Valuta-gegevenstype voor Twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U kunt het aantal decimalen dat voor valutawaarden wordt ondersteund, verhogen tot maximaal 10. De standaard limiet is vier decimalen. Door het aantal decimalen te verhogen voorkomt u gegevensverlies wanneer u met gegevens synchroniseert met Twee keer wegschrijven. De verhoging van het aantal decimalen is een optionele wijziging. Om dit te implementeren moet u ondersteuning vragen aan Microsoft.

Het proces waarbij het aantal decimalen wordt gewijzigd, heeft twee stappen:

1. De migratie aanvragen bij Microsoft.
2. Het aantal decimalen wijzigen in Dataverse.

De Finance and Operations-app en Dataverse moet hetzelfde aantal decimale posities in valutawaarden ondersteunen. Anders kunnen gegevens verloren gaan wanneer de gegevens tussen apps worden gesynchroniseerd. Het migratieproces configureert de manier waarop valuta- en wisselkoerswaarden worden opgeslagen, maar wijzigt geen gegevens. Nadat de migratie is voltooid, kan het aantal decimalen voor valutacodes en prijzen worden verhoogd. De gegevens die gebruikers invoeren en weergeven, kunnen de decimalen nauwkeuriger aangeven.

Migratie is optioneel. Als u meer decimalen wilt gebruiken, is het raadzaam om de migratie te overwegen. Organisaties die geen waarden nodig hebben met meer dan vier decimalen, hoeven niet te worden gemigreerd.

## <a name="requesting-migration-from-microsoft"></a>De migratie aanvragen bij Microsoft

Opslag voor bestaande valutakolommen in Dataverse kan niet meer dan vier decimalen ondersteunen. Daarom worden valutawaarden tijdens het migratieproces naar nieuwe interne kolommen in de database gekopieerd. Dit proces vindt voortdurend plaats totdat alle gegevens zijn gemigreerd. Intern worden de oude opslagtypen aan het eind van de migratie vervangen door de nieuwe opslagtypen, maar de gegevenswaarden blijven ongewijzigd. De valutakolommen kunnen vervolgens maximaal 10 decimale posities ondersteunen. Tijdens het migratieproces kunt u Dataverse zonder onderbreking blijven gebruiken.

Tegelijkertijd worden wisselkoersen gewijzigd, zodat ze maximaal 12 decimalen ondersteunen in plaats van de huidige limiet van 10. Deze wijziging is vereist om ervoor te zorgen dat het aantal decimalen in de Finance and Operations-app hetzelfde is als in Dataverse.

Bij de migratie worden de gegevens niet gewijzigd. Nadat de kolommen met valuta en wisselkoers zijn geconverteerd, kunnen beheerders het systeem zo configureren dat er maximaal tien decimalen worden gebruikt voor valutakolommen door het aantal decimalen voor elke transactievaluta en voor prijzen op te geven.

### <a name="request-a-migration"></a>Een migratie aanvragen

Om deze functie beschikbaar te maken stuurt u een e-mail naar **CDSExpandDecimal@microsoft.com** en voegt u de volgende informatie toe:

+ **Onderwerp:** aanvraag om ondersteuning voor uitgebreide decimalen in te schakelen voor \<organizationID\>
+ **Tekst:** Ik wil ondersteuning voor uitgebreide decimalen inschakelen voor mijn organisatie \<organizationID\>.

Voor de vervolgstappen neemt een Microsoft-vertegenwoordiger binnen twee tot drie werkdagen contact met u op.

Wanneer u een migratie aanvraagt, moet u op de hoogte zijn van de volgende details en kunt u deze dienovereenkomstig plannen:

+ De benodigde tijd voor het migreren van de gegevens is afhankelijk van de hoeveelheid gegevens in het systeem. De migratie van grote databases kan enkele dagen duren.
+ De grootte van de database neemt tijdelijk toe terwijl de migratie wordt uitgevoerd, omdat er extra ruimte nodig is voor indexen. De meeste extra ruimte wordt vrijgemaakt wanneer de migratie is voltooid.
+ Als er tijdens het migratieproces fouten optreden waardoor de migratie niet kan worden voltooid, stuurt het systeem waarschuwingen aan Microsoft Ondersteuning, zodat ondersteuningsmedewerkers kunnen ingrijpen. Zelfs als er tijdens de migratie fouten optreden, blijft Dataverse echter volledig beschikbaar voor normaal gebruik.
+ Het migratieproces kan niet ongedaan worden gemaakt.

## <a name="changing-the-number-of-decimal-places"></a>Het aantal decimalen wijzigen.

Wanneer de migratie is voltooid, kunt u in Dataverse getallen met meer decimalen opslaan. Beheerders kunnen kiezen hoeveel decimalen er worden gebruikt voor specifieke valutacodes en voor prijzen. Gebruikers van Microsoft Power Apps, Power BI en Power Automate kunnen getallen met meer decimalen weergeven en gebruiken.

Als u deze wijziging wilt aanbrengen, moet u de volgende instellingen bijwerken in Power Apps:

+ **Systeeminstellingen: valutanauwkeurigheid voor prijzen**: de kolom **Valutanauwkeurigheid instellen die in het systeem voor prijzen wordt gebruikt** bepaalt de manier waarop de valuta wordt berekend in de organisatie wanneer **Prijsprecisie** wordt geselecteerd.
+ **Bedrijfsbeheer: Valuta's**: in de kolom **Valutaprecisie** kunt u een aangepast aantal decimalen voor een bepaalde valuta opgeven. Er is een terugval voor de instelling voor de gehele organisatie.

Er zijn enkele beperkingen:

+ U kunt de valutakolom niet configureren voor een tabel.
+ U kunt meer dan vier decimalen opgeven op de niveaus **Prijzen** en **Transactievaluta**.

### <a name="system-settings-currency-precision-for-pricing"></a>Systeeminstellingen: Valutanauwkeurigheid voor prijzen

Beheerders kunnen de valutanauwkeurigheid instellen nadat de migratie is voltooid. Ga naar **Instellingen \> Beheer** en selecteer **Systeeminstellingen**. Wijzig vervolgens op het tabblad **Algemeen** de waarde van de kolom **Valutanauwkeurigheid instellen die in het systeem voor prijzen wordt gebruikt**, zoals in de volgende afbeelding wordt weergegeven.

![Systeeminstellingen voor valuta.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Bedrijfsbeheer: Valuta's

Als u wilt dat de valutanauwkeurigheid voor een bepaalde valuta afwijkt van de valutanauwkeurigheid die voor prijzen wordt gebruikt, kunt u deze wijzigen. Ga naar **Instellingen \> Bedrijfsbeheer**, selecteer **Valuta's** en selecteer de valuta die u wilt wijzigen. Vervolgens stelt u de kolom **Valutanauwkeurigheid** in op het gewenste aantal decimalen, zoals wordt weergegeven in de volgende afbeelding.

![Valuta-instellingen voor een bepaalde landinstelling.](media/specific-currency.png)

### <a name="tables-currency-column"></a>tabellen: kolom Valuta

Het aantal decimalen achter de komma dat kan worden geconfigureerd voor specifieke valutakolommen is beperkt tot vier.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]