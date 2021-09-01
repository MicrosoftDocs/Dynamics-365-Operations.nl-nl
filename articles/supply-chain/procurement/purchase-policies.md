---
title: Overzicht van Aanschafbeleid
description: Dit artikel biedt informatie over aanschafbeleid. Een inkoopbeleid is een verzameling regels die het opdrachtproces regelen. Een aanschafbeleid helpt beheerders hun aanschaffingsstrategie implementeren door een beleidsstructuur te maken die is afgestemd op de strategische aanschaffingsbehoeften van de organisatie.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11614"
- intro-internal
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fd090f6e8b91c6a75eced17fadd76f686c5441f1526736534ad1a947d80cea0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761777"
---
# <a name="purchasing-policies-overview"></a>Overzicht van Aanschafbeleid

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over aanschafbeleid. Een inkoopbeleid is een verzameling regels die het opdrachtproces regelen. Een aanschafbeleid helpt beheerders hun aanschaffingsstrategie implementeren door een beleidsstructuur te maken die is afgestemd op de strategische aanschaffingsbehoeften van de organisatie.

Een inkoopbeleid bestaat uit een reeks beleidsregels. Wanneer u een beleidsregel definieert, selecteert u een regeltype. Vervolgens maakt u een regel voor het regeltype door de instellingen, de startdatum en de einddatum voor de regel te definiëren.  

Een beheerder maakt bijvoorbeeld een beleid, selecteert het regeltype **Catalogusbeleid** en voegt vervolgens een catalogusbeleidsregel aan het beleid toe. De catalogusbeleidsregel vermeldt dat de avontuurcatalogus moet worden gebruikt voor interne inkoop. Nadat het aanschaffingsbeleid aan een specifieke organisatie is gekoppeld, zien werknemers van die organisatie de avontuurcatalogus wanneer ze aanvragen maken.

## <a name="assigning-policies-to-organizations"></a>Beleid toewijzen aan organisaties
Voordat een beleid van kracht kan worden, moet het met een organisatie worden gekoppeld. Het aanschaffingsbeleid is gekoppeld met het hiërarchiedoel **Interne aanschaffingscontrole**. Daarom is het aanschaffingsbeleid alleen van toepassing op organisaties in hiërarchieën met het hiërarchiedoel **Interne aanschaffingscontrole**. U kunt ook organisaties selecteren in de platte lijst met rechtspersonen in de CompanyInfo-tabel. Deze rechtspersonen zijn aangeduid als “Bedrijven” in het beleidsraamwerk.

## <a name="determining-which-rule-to-apply"></a>Bepalen welke regel moet worden toegepast
Afhankelijk van hoe u uw inkoopbeleid configureert, kunnen meerdere regels de gebruikers in een organisatie beïnvloeden. De volgende voorbeelden illustreren de verschillende manieren waarop u het inkoopbeleid kunt configureren en kunt opgeven hoe het beleid wordt toegepast wanneer een transactie wordt uitgevoerd.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Voorbeeld 1: Eenvoudige configuratie van aanschafbeleid

Organisaties die klein en minder complex zijn, kunnen het inkoopbeleid per rechtspersoon instellen en kunnen alleen de organisatiehiërarchie Bedrijven gebruiken.  

Voor Fabrikam, een klein bedrijf, wijken de inkoopbehoeften weinig af in de hele organisatie. De inkoopregels variëren alleen tussen de rechtspersonen van de organisatie. Werknemers van Fabrikam Canada en werknemers van Fabrikam U.S. kopen bijvoorbeeld goederen en diensten in verschillende catalogi en bij verschillende leveranciers. Daarom stelt Fabrikam haar inkoopbeleid in op het niveau van de rechtspersoon.  

Fabrikam maakt twee inkoopbeleiden. Beleid A is van toepassing op de Amerikaanse rechtspersoon 1111. Beleid B is van toepassing op de Canadese rechtspersoon 2222. Wanneer een werknemer van rechtspersoon 1111 een opdracht tot inkoop maakt, worden de beleidsregels afgeleid van beleid A. De productcatalogus die de werknemer ziet wordt bijvoorbeeld opgegeven in de catalogusbeleidsregel voor beleid A.  

Wanneer een werknemer van rechtspersoon 2222 een opdracht tot inkoop maakt, worden de beleidsregels afgeleid van beleid B.  

**Opmerking:** Als een werknemer van rechtspersoon 1111 een artikel koopt namens een werknemer van rechtspersoon 2222, dan worden de beleidsregels die zijn opgegeven voor rechtspersoon 2222 (dat wil zeggen de beleidsregels uit beleid B), toegepast.

### <a name="example-2-complex-purchasing-policy-configuration"></a>Voorbeeld 2: Complexe configuratie van aanschafbeleid

In het vorige voorbeeld waren alle inkoopregel gedefinieerd in één organisatiehiërarchie, in dit geval de organisatiehiërarchie Bedrijven. Een complexe organisatie kan echter een beleid definiëren voor meerdere organisatiehiërarchieën.  


Contoso is een groot bedrijf dat complexe inkoopregels nodig heeft om het proces voor opdracht tot inkoop te beheren. Contoso heeft regels gedefinieerd voor twee verschillende organisatiehiërarchieën: Afdeling en Algemene inkoopcontrole.  

Beleid 123 is gedefinieerd voor de organisatiehiërarchie 'Afdeling' voor de Sales UK – Verkoopafdeling. In beleid 123 vermeldt de beheerregel voor opdrachten tot inkoop dat beperkingen op minimumorderhoeveelheden moeten worden afgedwongen. In deze regel is de optie **Beperkingen op minimumorderhoeveelheid afdwingen** geselecteerd.  

Beleid 456 is gedefinieerd voor de organisatiehiërarchie “Algemene inkoopcontrole” voor de afdeling Verkoop en marketing. In beleid 456 vermeldt de beheerregel voor de opdracht tot inkoop niet dat beperkingen op minimumorderhoeveelheden moeten worden afgedwongen. In deze regel is de selectie van de optie **Beperkingen op minimumorderhoeveelheid afdwingen** opgeheven.  

Sam werkt op de verkoopafdeling van Sales UK in het kantoor van Contoso in het Verenigd Koninkrijk. Het beleid voor zowel de organisatiehiërarchie 'Afdeling' als 'Algemene inkoopcontrole' is van toepassing op deze afdeling. Wanneer Sam een opdracht tot inkoop maakt, moet het systeem bepalen welk beleid moet worden toegepast. De systeembeheerder heeft de parameters van het inkoopbeleid ingesteld zodat het inkoopbeleid moet worden toegepast in de volgende prioriteitsvolgorde:

1.  Algemene inkoopcontrole
2.  Afdeling
3.  Bedrijven

Daarom wordt beleid 456 toegepast op de opdracht tot inkoop die Sam maakt, en is er geen minimumorderhoeveelheid vereist voor de opdracht tot inkoop.

## <a name="policy-rules"></a>Beleidsregels
### <a name="catalog-policy-rule"></a>Beleidsregel voor catalogus

De catalogusbeleidsregel bepaalt welke aanschaffingscatalogus gebruikers zien wanneer ze opdrachten tot inkoop maken. Als een gebruiker toestemming heeft gekregen om producten voor een andere gebruiker te bestellen, gebruikt de bestelopdracht de catalogusbeleidsregel die is gedefinieerd voor de rechtspersoon en operationele eenheid van de aanvrager, om te bepalen welke catalogus er moet worden weergegeven. Voordat u een catalogusbeleidsregel kunt definiëren, moet u een aanschaffingscatalogus maken en publiceren.

### <a name="category-access-policy-rule"></a>Toegangsbeleidsregel voor categorie

De beleidsregel voor categorietoegang bepaalt welke categorieën gebruikers kunnen openen wanneer ze opdrachten tot inkoop maken. Als geen regel is opgegeven, kunnen alle aanschaffingscategorieën aan de opdracht tot inkoop worden toegevoegd.

1.  Selecteer de optie **Bovenliggende regel opnemen** om de beleidsregel voor categorietoegang van de bovenliggende organisatie toe te passen op de categorie.
2.  Selecteer in het deelvenster **Beschikbare categorieën** de categorieën waarop de regel van toepassing is. Wanneer u een categorie selecteert, worden alle categorieën hoger in de hiërarchie ook toegevoegd aan de lijst **Geselecteerde categorieën**.
3.  Selecteer de optie **Subcategorieën opnemen** om de regel toe te passen op alle subcategorieën van de geselecteerde categorie.

### <a name="category-policy-rule"></a>Categoriebeleidsregel

De categoriebeleidsregel bepaalt hoe gebruikers voor elke categorie leveranciers kunnen selecteren. Deze definieert ook de vereisten voor de processen voor ontvangen en factureren.

### <a name="re-approval-rule-for-purchase-orders"></a>Regel voor het opnieuw goedkeuren van inkooporders

De regel voor het opnieuw goedkeuren is een optionele regel die de criteria bepaalt voor het vereisen van nieuwe goedkeuring wanneer een inkooporder is gewijzigd. De geselecteerde velden worden geëvalueerd in de workflow voor inkooporders wanneer de voorwaarde 'Opnieuw goedkeuren inkooporder vereist' is ingesteld in de workflow.

> [!NOTE]
> Boekhoudingsverdeling wordt altijd opnieuw ingesteld wanneer een goedgekeurde inkooporder wordt gewijzigd met wijzigingsbeheer ingeschakeld. Dus u moet er rekening mee houden dat als u hernieuwde goedkeuring van een inkooporder wilt voorkomen wanneer bepaalde velden veranderen, het veld Boekhoudingsverdeling NIET moet worden opgenomen als een geselecteerd veld voor hernieuwde goedkeuring. 

### <a name="purchase-requisition-rfq-rule"></a>Offerteaanvraagregel voor opdracht tot inkoop

De offerteaanvraagregel voor opdracht tot inkoop definieert criteria voor het aanvragen van een offerteaanvraag voor een regel in een opdracht tot inkoop. Als een regel aan de voorwaarden voldoet, verschijnt de stempel 'informele offerteaanvraag' of 'formele offerteaanvraag' op de aanvraagregel.

### <a name="purchase-requisition-control-rule"></a>Regel voor beheer van opdracht tot inkoop

De regel voor beheer van de opdracht tot inkoop voor opdrachten van het type **Verbruik** is een optionele regel. Wanneer u regels van dit type maakt, kunt u opties op verschillende tabbladen instellen:

-   Op het tabblad **Indienen bij workflow** kunt u de velden configureren die moeten worden ingevoerd op de opdrachtregel zodat de opdracht ter goedkeuring kan worden ingediend.
-   Op het tabblad **Orderhoeveelheden** kunt u de velden configureren die onder bepaalde voorwaarden op de opdracht tot inkoop zijn vereist. U kunt ook orderhoeveelheden afdwingen.
-   Op het tabblad **Datums** kunt u instellen of de boekingsdatum dezelfde als de aanvraagdatum is
-   Op het tabblad **Adres** kunt u bepalen of de gebruiker nieuwe adressen in het systeem mag maken om op de opdracht tot inkoop toe te passen.

### <a name="requisition-purpose-rule"></a>Regel voor bestelopdrachtdoelen

De regel voor bestelopdrachtdoelen is een optionele regel die bepaalt welk type doel voor het opdrachtdoel is toegestaan voor een specifieke rechtspersoon. Tenzij in deze regel een ander doel is aangegeven, hebben opdrachten automatisch het doel **Verbruik** wanneer ze worden gemaakt.

### <a name="replenishment-category-access-policy-rule"></a>Toegangsbeleidsregel voor aanvullingscategorie

De toegangsbeleidsregel voor aanvullingscategorie is een optionele regel bepaalt welke producten beschikbaar zijn voor het verwerken van de vraag naar een specifieke rechtspersoon wanneer het bestelopdrachtdoel **Aanvulling** is.

### <a name="replenishment-control-rule"></a>Regel aanvullingsbeheer

De regel voor aanvullingsbeheer is een optionele regel die de velden op de opdrachtregel definieert die moet worden ingevoerd voor de opdracht om deze ter goedkeuring in te dienen wanneer het doel van de opdracht **Aanvulling** is.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Regel voor maken van inkooporders en vraagconsolidatie

De regels voor het maken van inkooporders en consolidatie van de vraag bepaalt de beleidsregels die u moet gebruiken wanneer een inkooporder wordt gegenereerd vanuit een goedgekeurde opdracht tot inkoop. Wanneer u regels van dit type maakt, kunt u opties op verschillende tabbladen instellen:

-   Op het tabblad **Inkooporder splitsen** kunt u criteria definiëren voor het splitsen van regels in een opdracht tot inkoop in afzonderlijke inkooporders.
-   Op het tabblad **Overboeking prijs/korting** kunt u definiëren wanneer u de prijsafspraak opnieuw wilt berekenen wanneer een inkooporder is gemaakt:
    -   **Alleen bij geen handelsovereenkomst**- Prijzen en kortingen worden alleen overdragen van de opdracht tot inkoop als er geen geldende handelsovereenkomst of basisprijs is. Als er een handelsovereenkomst of basisprijs is voor het artikel of de leveranciers, worden de prijzen en kortingen herberekend op basis van de handelsovereenkomst of de basisprijs en worden deze toegepast op de inkooporder. Tenzij anders opgegeven, is dit het standaardgedrag.
    -   **Altijd** – Prijzen en kortingen worden altijd overgenomen van de opdracht tot inkoop.

    U kunt ook toestaan dat de aanvrager de overdrachtmethode voor prijs en korting wijzigt voor afzonderlijke regels van opdrachten tot inkoop, ongeacht de overdrachtregel die is bepaald voor prijs/korting. Selecteer de optie **Handmatig overschrijven toestaan per opdracht tot inkoopregel** indien u deze functie wilt inschakelen.
-   Op het tabblad **Overboeking artikelbeschrijving** kunt u de artikelomschrijving van de opdracht overboeken wanneer deze uit een offerteaanvraag afkomstig is.
-   Op het tabblad **Prijstolerantie** kunt u regels definiëren om goedgekeurde opdrachten tot inkoop opnieuw door het revisieproces te routeren wanneer de prijs van een artikel in de aanschaffingscatalogus is gestegen. Stel het maximumbedrag in waarmee het nettobedrag op een regel van een opdracht tot inkoop kan stijgen tussen het tijdstip waarop de opdracht tot inkoop is goedgekeurd en het tijdstip waarop de inkooporder is gemaakt. Het nettobedrag wordt berekend met de volgende formule: (\[Hoeveelheid× (Eenheidsprijs - Korting) ÷ Prijseenheid\] + Diverse toeslagen voor de bestelling) x (100 - Kortingspercentage) ÷ 100. Regels van de inkoopopdracht die de prijstolerantie overschrijden, worden vastgehouden voor handmatige verwerking. De regels die u configureert op het tabblad **Foutverwerking** bepalen hoe de regels van de opdracht tot inkoop worden verwerkt.
-   Op het tabblad **Foutverwerking** kunt u de verwerkingsregel configureren die wordt toegepast op een opdracht tot inkoop waarvan de validatie is mislukt bij het maken van de inkooporder vanwege een leveranciersfout of prijstolerantiefout. Een van de volgende opties selecteren:
    -   **Geen actie** - De regels van de opdracht tot inkoop blijven op de pagina **Goedgekeurde opdrachten tot inkoop vrijgeven**. De status van de regels van de opdracht tot inkoop blijft **Goedgekeurd**. De fouten moeten echter worden gecorrigeerd voordat er een inkooporder voor de regels van de opdracht tot inkoop kan worden gegenereerd.
    -   **De opdracht tot inkoopregel annuleren** De regels van de opdracht tot inkoop worden geannuleerd. Aanvragers kunnen een nieuwe opdracht tot inkoop voor de geannuleerde regels maken als zij de regelartikelen nog steeds willen aanvragen.
    -   **Een nieuwe opdracht tot inkoopregel maken** - De regels van de opdracht tot inkoop worden geannuleerd. Vervolgens worden er nieuwe opdrachten tot inkoop gegenereerd die alleen de regels van de opdracht tot inkoop bevatten waarvan de validatie is mislukt. De nieuwe opdrachten tot inkoop die worden gegenereerd, hebben de status **Concept**. Deze opdrachten tot inkoop kunnen opnieuw ter controle worden ingediend nadat de validatiefouten zijn gecorrigeerd. De voorbereider van de regels van de opdracht tot inkoop ontvangt een melding dat de regels zijn geannuleerd en dat er nieuwe opdrachten tot inkoop zijn gegenereerd voor de regels van de opdracht tot inkoop waarvan de validatie is mislukt.
-   Op het tabblad **Handmatig inkooporders maken** kunt u de parameters definiëren die bepalen of een opdracht tot inkoop handmatig moet worden verwerkt of automatisch naar een inkooporder kan worden geconverteerd. De parameters kunnen van toepassing zijn op interne-catalogusartikelen, externe-catalogusartikelen of niet-catalogusartikelen. Een van de volgende opties selecteren:
    -   **Handmatig inkooporders maken** - Maak handmatig inkooporders voor alle opdrachten tot inkoop.
    -   **Automatisch inkooporders maken** - Maak automatisch inkoopordersvoor alle goedgekeurde opdrachten tot inkoop. Er worden geen opdrachten tot inkoop vastgehouden voor het handmatig maken van inkooporders.
    -   **Inkooporders automatisch maken behalve in deze omstandigheden** - Handmatig inkooporders maken voor opdrachten tot inkoop die voldoen aan de criteria die u opgeeft. Alle andere goedgekeurde opdrachten tot inkoop worden automatisch geconverteerd naar inkooporders. Als u **Inkooporders automatisch maken behalve in deze omstandigheden** selecteert, kunt u aanschaffingscategorieën en leveranciers toevoegen om op te geven welke goedgekeurde regels van opdrachten tot inkoop worden vastgehouden voor handmatige verwerking. Deze optie kan van toepassing zijn op interne-catalogusartikelen, externe-catalogusartikelen en niet-catalogusartikelen. Wanneer u een aanschaffingscategorie selecteert, worden alle subcategorieën voor deze categorie eveneens geselecteerd. Selecteer de optie **Alle** voor een bepaald type regel van een opdracht tot inkoop om alle regels van dit regeltype vast te houden voor handmatige verwerking.

    Als u automatisch inkooporders van goedgekeurde opdrachten tot inkoop wilt genereren wanneer de batchtaak voor het genereren van inkooporders wordt uitgevoerd, selecteert u de optie **Het automatisch maken van inkooporders als batchtaak uitvoeren**. Deze optie is alleen van toepassing op opdrachten tot inkoop die geen handmatige verwerking vereisen. Als u een batchtaak voor het automatisch genereren van inkooporders uitvoert, kunt u deze activiteit plannen op een tijdstip waarop resources minder zwaar worden belast. Als de optie **Vooruitbetaling vereist** is geselecteerd op de regels van de opdracht tot inkoop, selecteert u de optie **Wanneer de aanvraag is ingesteld op vooruitbetaling** om goedgekeurde opdrachten tot inkoop vast te houden voor handmatige verwerking. Opdrachten tot inkoop die worden vastgehouden voor handmatige verwerking, kunnen worden gefilterd om alleen die regels van de opdracht tot inkoop weer te geven waarvoor vooruitbetaling is vereist.
-   Op het tabblad **Vraagconsolidatie** kunt u de parameters definiëren die bepalen of opdrachten tot inkoop die handmatig zijn verwerkt, in aanmerking kunnen worden genomen voor consolidatie van opdrachten tot inkoop. De parameters kunnen van toepassing zijn op interne-catalogusartikelen, externe-catalogusartikelen of niet-catalogusartikelen. Een van de volgende opties selecteren:
    -   **Vraagconsolidatie niet toestaan** - Geen goedgekeurde regels in opdrachten tot inkoop komen in aanmerking voor consolidatie van de vraag. Deze optie wordt standaard geselecteerd en is alleen van toepassing op regels van een opdracht tot inkoop waarvoor handmatige verwerking is vereist bij het maken van inkooporders.
    -   **Vraagconsolidatie altijd toestaan** - Alle goedgekeurde regels in opdrachten tot inkoop komen in aanmerking voor consolidatie van de vraag. **Opmerking:** Als u de optie **Vraagconsolidatie altijd toestaan** op het tabblad **Vraagconsolidatie** selecteert, maar ook de optie **Automatisch inkooporders maken** op het tabblad **Handmatig inkooporders maken**, worden alle opdrachten tot inkoop vastgehouden voor handmatige verwerking.
    -   **Vraagconsolidatie toestaan in deze omstandigheden** - Definieer de criteria die bepalen of goedgekeurde regels op opdrachten tot inkoop in aanmerking komen voor consolidatie van de vraag. U kunt de criteria per aanschaffingscategorie en leverancier instellen voor elke type regel van een opdracht tot inkoop. Als u **Vraagconsolidatie toestaan in deze omstandigheden** selecteert, kunt u de criteria per aanschaffingscategorie en leverancier instellen voor elke type regel van een opdracht tot inkoop. Wanneer u een aanschaffingscategorie selecteert, worden alle subcategorieën voor deze categorie eveneens geselecteerd. Als u de optie **Alle** selecteert voor een bepaald regeltype, komen alle regels van de opdracht tot inkoop met dit regeltype in aanmerking voor vraagconsolidatie.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]