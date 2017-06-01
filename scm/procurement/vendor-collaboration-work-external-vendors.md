---
title: Leverancierssamenwerking met externe leveranciers
description: In dit onderwerp wordt beschreven hoe aankoopbemiddelaars met externe leveranciers kunnen samenwerken om informatie over inkooporders en consignatievoorraad uit te wisselen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b141ed78306504949eae641377b5c5a2b0599572
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Leverancierssamenwerking met externe leveranciers

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt beschreven hoe aankoopbemiddelaars met externe leveranciers kunnen samenwerken om informatie over inkooporders en consignatievoorraad uit te wisselen.

De module **Leverancierssamenwerking** is bedoeld voor leveranciers die geen EDI-integratie (Electronic Data Interchange) met Microsoft Dynamics 365 for Operations hebben. Hiermee kunnen leveranciers werken met inkooporder-, factuur- en consignatievoorraadgegevens. In dit onderwerp wordt beschreven hoe u kunt samenwerken met externe leveranciers die de interface voor leverancierssamenwerking gebruiken om met inkooporders en consignatievoorraad te werken. Daarnaast wordt beschreven hoe u een specifieke leverancier in staat stelt om leverancierssamenwerking te gebruiken en hoe u de gegevens definieert die alle leveranciers te zien krijgen wanneer ze reageren op een inkooporder. Meer informatie over wat externe leveranciers kunnen doen in de interface voor leverancierssamenwerking vindt u in [Leverancierssamenwerking met klanten](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Meer informatie over hoe leveranciers leverancierssamenwerking kunnen gebruiken in factureringsprocessen vindt u in [Werkgebied voor samenwerkingsfacturering van leveranciers](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace) Meer informatie over hoe u nieuwe gebruikers van leverancierssamenwerking inricht, vindt u in [Leverancierssamenwerkingsgebruikers beheren](manage-vendor-collaboration-users.md)

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>De gegevens opgeven die voor leveranciers te zien zijn wanneer ze reageren op inkooporders
Als leveranciers reageren op een inkooporder die u verzendt, krijgen ze een dialoogvenster te zien waarin ze moeten bevestigen dat ze de inkooporder willen accepteren, afwijzen of accepteren met wijzigingen. Welke gegevens voor de leverancier op dat moment moeten worden weergegeven, is afhankelijk van uw bedrijf, dus u kunt de tekst opgeven die in elk van de drie bevestigingsberichten moet worden weergeven. Met de tekst kan de leverancier bijvoorbeeld worden geïnformeerd over de volgende stappen in het proces of over de voorwaarden.  

De tekst opgeven die moet worden weergegeven in de reactie op een inkooporder:

1.  Open de pagina **Informatie voor leveranciers die reageren op inkooporders**.
2.  Selecteer een van de typen reacties.
3.  Klik op **Bewerken**.
4.  Voer in het vak **Informatiebericht** de gegevens in die leveranciers te zien moeten krijgen.

Als u berichten in meerdere talen moet toevoegen, maakt u afzonderlijke berichten met de betreffende taalcodes. De leverancier krijgt het bericht te zien in de eigen taal.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>De opties voor leverancierssamenwerking voor een specifieke leverancier instellen
De algemene instellingen voor leverancierssamenwerking in Dynamics 365 for Operations worden geconfigureerd door een beheerder. Deze bepaalt bijvoorbeeld welke beveiligingsrollen beschikbaar zijn voor alle leveranciers waarmee u samenwerkt. Er zijn ook bepaalde instellingen die voor elke leverancierrekening kunnen afwijken, en u moet deze instellen:

-   Schakel leverancierssamenwerking in.
-   Bepaal of u wilt dat de leverancier prijsgegevens te zien krijgt.

### <a name="enable-vendor-collaboration"></a>Leverancierssamenwerking inschakelen

Voordat gebruikersrekeningen kunnen worden gemaakt voor een externe leverancier, moet u de leveranciersrekening zo configureren dat ze leverancierssamenwerking kunnen gebruiken. U doet dit door **Samenwerkingactivering** op actief in te stellen op het tabblad **Algemeen** op de pagina **Leveranciers**. Er zijn twee opties die u kunt kiezen:

-   **Actief (IO wordt automatisch bevestigd)**- Inkooporders worden automatisch bevestigd wanneer de leverancier deze zonder wijzigingen accepteert.
-   **Actief (IO wordt niet automatisch bevestigd)**- Inkooporders moeten handmatig door uw organisatie worden bevestigd nadat de leverancier ze heeft geaccepteerd.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Bepalen of de leverancier prijsgegevens te zien krijgt

Als u prijsgegevens, zoals de eenheidsprijs, kortingen en toeslagen, wilt delen via de samenwerkingsinterface, moet u de optie **Prijzen/bedrag van inkooporder** voor de leveranciersrekening instellen op **Ja**. Deze optie is beschikbaar op het tabblad **Details over inkooporders**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Werken met inkooporders bij het gebruik van leverancierssamenwerking
### <a name="sending-a-po-to-the-vendor"></a>Een inkooporder verzenden naar de leverancier

Inkooporders worden voorbereid in Dynamics 365 for Operations. Wanneer de inkooporder de status **Goedgekeurd** heeft, kunt u deze naar de leverancier verzenden met de actie **Verzenden voor bevestiging **op de pagina **Inkooporder**. De status van de inkooporder wordt gewijzigd in **Externe controle.** Nadat de inkooporder is ingediend, kan de leverancier deze bekijken op de pagina **Inkooporders ter beoordeling** in de interface voor leverancierssamenwerking en de order accepteren of afwijzen, of wijzigingen voorstellen. De leverancier kan ook opmerkingen toevoegen om informatie zoals wijzigingen in de inkooporder door te geven. Als u de aandacht van de leverancier naar de nieuwe inkooporder wilt trekken, kunt u de inkooporder ook via e-mail verzenden met behulp van het afdrukbeheersysteem.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Bevestiging en acceptatie van de inkooporder door de leverancier

Wanneer een leverancier een inkooporder heeft geaccepteerd, kan de inkooporder automatisch worden bevestigd of moet deze mogelijk handmatig worden bevestigd. Dit is afhankelijk van de instelling van het veld **Leveranciersactivering **: **Actief (IO wordt automatisch bevestigd)** of **Actief (IO wordt niet automatisch bevestigd)**.  

De onderstaande tabel geeft de typische uitwisseling van informatie weer, afhankelijk van hoe de leverancier antwoordt als u deze een inkooporder voor bevestiging toestuurt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Leveranciersantwoord</strong></td>
<td><strong>Resultaat</strong></td>
</tr>
<tr class="even">
<td>De leverancier <strong>accepteert</strong> de order. Dynamics 365 for Operations is geconfigureerd om IO's automatisch te bevestigen wanneer de leverancier accepteert.</td>
<td>De status van de order verandert in <strong>Bevestigd</strong>. Als bijwerking van de order door iets wordt voorkomen, wordt het antwoord van de leverancier wel geregistreerd als <strong>Geaccepteerd</strong>, maar blijft de inkooporder de status <strong>Externe controle</strong> behouden.</td>
</tr>
<tr class="odd">
<td>De leverancier <strong>accepteert</strong> de order. Dynamics 365 for Operations is niet geconfigureerd om IO's automatisch te bevestigen wanneer de leverancier accepteert.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Geaccepteerd</strong>, maar de inkooporder behoudt de status <strong>Externe controle</strong>.</td>
</tr>
<tr class="even">
<td>De leverancier <strong>wijst de order af</strong>.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Afgewezen</strong>, maar de inkooporder behoudt de status <strong>Externe controle</strong>. De afwijzing wordt ontvangen met de leveranciersnotitie.</td>
</tr>
<tr class="odd">
<td>De leverancier <strong>accepteert de order met wijzigingen</strong>. Wijzigingen worden voorgesteld op regelniveau. Het is mogelijk om afzonderlijke regels te accepteren of af te wijzen. Andere mogelijke wijzigingen zijn:
<ul>
<li>Gewijzigde datums of hoeveelheden.</li>
<li>Opsplitsingen van regels voor verschillende leveringsdatums of -hoeveelheden.</li>
<li>De vervanging van een item.</li>
</ul>
Prijsgegevens en toeslagen kunnen niet door de leverancier worden gewijzigd. Suggesties voor wijzigingen hierin kunnen met notities worden gedaan.</td>
<td>Het leveranciersantwoord wordt geregistreerd als <strong>Geaccepteerd met wijzigingen</strong>, <strong></strong> en de inkooporder behoudt de status <strong>Externe controle</strong>.</td>
</tr>
</tbody>
</table>

U kunt het werkgebied **Voorbereiding van** **inkooporder** gebruiken om te controleren op welke inkooporders de leverancier heeft gereageerd. Deze werkruimte bevat twee lijsten die inkooporders met de status **Externe controle** bevatten:

-   Bij externe herziening is actie vereist.
-   Bij externe herziening in afwachting van antwoord van leverancier.

### <a name="changing-a-po"></a>Een inkooporder wijzigen

Wanneer u een inkooporder wilt wijzigen waarop al is gereageerd, verzendt u een nieuwe versie van de inkooporder naar de leverancier. De nieuwe inkooporder heeft een versieachtervoegsel om aan te geven dat het om een gewijzigde versie van een inkooporder gaat die eerder is doorgegeven. Op de pagina **Historie van leveranciersbevestigingen van inkooporders** kunnen u en uw leveranciers de historie van elke order volgen. De eerder bevestigde versie van de inkooporder blijft in de lijst met bevestigde PO's tot de nieuwe inkooporder is bevestigd.

### <a name="cancelling-a-po"></a>Een inkooporder annuleren

Wanneer u een inkooporder annuleert, wordt de status gewijzigd in **Goedgekeurd**. U moet de inkooporder via de leveranciersportal terug naar de leverancier sturen zodat de leverancier de annulering kan bevestigen of afwijzen. Nadat de annulering is bevestigd, wordt de inkooporder in de lijst met bevestigde PO's van de leverancier weergegeven als **Geannuleerd**.

### <a name="adding-attachments-to-a-po"></a>Bijlagen toevoegen aan een inkooporder

U kunt bijlagen, zoals bestanden, afbeeldingen en notities, aan de inkooporder toevoegen via het documentbeheersysteem. De bijlagen die met de beperking van het type **Extern** worden toegevoegd, worden voor de leverancier weergegeven wanneer u deze de inkooporder toestuurt.

## <a name="purchase-order-statuses-and-versions"></a>Inkooporderstatussen en -versies
In dit onderdeel worden de statussen beschreven die een inkooporder kan hebben tot het moment dat deze wordt bevestigd. Daarnaast wordt aangegeven op welk moment nieuwe versies van de inkooporder aan de leverancier beschikbaar worden gemaakt. Dit kan verschillen, afhankelijk van of u wijzigingsbeheer voor inkooporders gebruikt. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versies en status als u geen wijzigingsbeheer gebruikt

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actie**                                                               | **Status en versie**                                                                                                                                       |
| De oorspronkelijke versie van de IO wordt gemaakt in Dynamics 365 for Operations. | De status is **Goedgekeurd**.                                                                                                                                  |
| De IO wordt verzonden naar de leverancier.                                            | Er wordt een versie geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**.                                          |
| De leverancier verzendt een antwoord **Geaccepteerd met wijzigingen**.                  | De status is nog steeds **Externe controle**.                                                                                                                  |
| U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd.                  | De status wordt gewijzigd in **Goedgekeurd**.                                                                                                                        |
| U verzendt de nieuwe versie van de IO naar de leverancier.                        | Er wordt een nieuwe versie geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**.                                      |
| De leverancier accepteert de nieuwe versie van de inkooporder.                            | De status is nog steeds **Externe controle**, tenzij de leveranciersrekening zo is geconfigureerd dat de IO bij acceptatie automatisch de status **Bevestigd** krijgt. |

Leveranciers hoeven de inkooporder niet te bevestigen via de interface voor leverancierssamenwerking. Ze kunnen ook een e-mailbericht verzenden of hun acceptatie van een inkooporder via andere kanalen laten weten. U kunt de order vervolgens handmatig in Dynamics 365 for Operations bevestigen. In dit geval ontvangt u een waarschuwing dat de order wordt bevestigd, zelfs als er geen antwoord van de leverancier is. De inkooporder wordt vervolgens in de bevestigingshistorie weergegeven als een openstaande bevestigde order die geen antwoorden heeft. De leverancier heeft niet meer de mogelijkheid om de inkooporder te bevestigen of af te wijzen.  

**Opmerking:** de versie van de inkooporder die beschikbaar is voor andere processen in Dynamics 365 for Operations, is altijd de laatste versie, ook als deze versie nog niet is geregistreerd in de interface voor leverancierssamenwerking.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versies en status als u wijzigingsbeheer gebruikt

Als wijzigingsbeheer is ingeschakeld voor inkooporders, doorloopt de inkooporder een goedkeuringsworkflow om de status **Goedgekeurd** te bereiken. Dit proces is niet zichtbaar voor de leverancier.  

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat als wijzigingsbeheer is ingeschakeld. De versie wordt geregistreerd wanneer de inkooporder wordt goedgekeurd, niet wanneer de inkooporder naar de leverancier wordt verzonden of wordt bevestigd.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actie**                                                                                                    | **Status en versie**                                                                                                                                                                                                                                                                                                                                                                      |
| De oorspronkelijke versie van de IO wordt gemaakt in Dynamics 365 for Operations.                                      | De status is **Concept**.                                                                                                                                                                                                                                                                                                                                                                    |
| De IO wordt verzonden naar het goedkeuringsproces. (Dit is een intern proces waarbij de leverancier niet is betrokken.) | De status wordt gewijzigd van **Concept** in **Wordt gecontroleerd** in **Goedkeuring** als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. De goedgekeurde inkooporder wordt geregistreerd als een versie.                                                                                                                                                                                                                     |
| De IO wordt verzonden naar de leverancier                                                                                  | De versie wordt geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**.                                                                                                                                                                                                                                                                       |
| U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd.                                                       | De status wordt weer gewijzigd in **Concept**.                                                                                                                                                                                                                                                                                                                                                    |
| De IO wordt weer naar het goedkeuringsproces verzonden.                                                            | De status wordt gewijzigd van **Concept** in **Wordt gecontroleerd** in **Goedkeuring** als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. Het systeem kan ook zo worden geconfigureerd dat voor bepaalde veldwijzigingen geen nieuwe goedkeuring vereist is. In dit geval wordt de status eerst gewijzigd in **Concept** en vervolgens automatisch bijgewerkt in **Goedgekeurd**. De goedgekeurde inkooporder wordt geregistreerd als een nieuwe versie. |
| U verzendt de nieuwe versie van de IO naar de leverancier.                                                             | De nieuwe versie wordt geregistreerd in de interface voor leverancierssamenwerking en de status wordt gewijzigd in **Externe controle**.                                                                                                                                                                                                                                                                   |
| De leverancier keurt de nieuwe versie van de inkooporder goed                                                                | De status wordt gewijzigd in **Bevestigd**. Dit gebeurt automatisch of wanneer u het antwoord van de leverancier ontvangt en vervolgens de inkooporder bevestigt.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Informatie over consignatievoorraad delen
Als u consignatievoorraad gebruikt, kunnen leveranciers de interface voor leverancierssamenwerking gebruiken om informatie op de volgende pagina's te bekijken:

-   **Inkooporders die consignatievoorraad verbruiken** - Inkooporders voor consignatievoorraad worden gegenereerd wanneer het eigendom van de voorraad van de leverancier naar uw bedrijf overgaat. Tegelijkertijd wordt een productontvangstbon geboekt. Deze consignatie-inkooporders worden alleen weergegeven op de pagina **Inkooporders die consignatievoorraad verbruiken**. Ze worden niet opgenomen op de pagina **Alle bevestigde inkooporders** in de module **Leverancierssamenwerking**.
-   **Producten ontvangen uit consignatievoorraad** - Deze pagina bevat een overzicht van alle transacties waarvan het eigendom van producten van de leverancier is overgedragen aan uw bedrijf. Leveranciers kunnen deze informatie gebruiken om de klant te factureren.
-   **Voorhanden consignatievoorraad** - Op deze pagina wordt de voorhanden consignatievoorraad weergegeven die het eigendom is van de leverancier en is ontvangen in uw magazijn.





