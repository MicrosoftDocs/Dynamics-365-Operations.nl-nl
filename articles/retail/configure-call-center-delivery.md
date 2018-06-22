---
title: Leveringsmethoden en toeslagen van callcenters configureren
description: In dit onderwerp wordt beschreven hoe u leveringsmethoden en toeslagen instelt voor een callcenterorder in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: ebc8ee52da7d10ca18147684a0190e52a495ad5a
ms.contentlocale: nl-nl
ms.lasthandoff: 05/15/2018

---

# <a name="configure-call-center-delivery-modes-and-charges"></a>Leveringsmethoden en toeslagen van callcenters configureren

[!INCLUDE [banner](includes/banner.md)]

Wanneer een verkooporder wordt geplaatst in Microsoft Dynamics 365 for Retail, als de persoon die de verkooporder heeft ingevoerd is gekoppeld aan een callcenterkanaal, worden logica en regels gebruikt voor het valideren van de leveringsmethode en het berekenen van toeslagen voor de order.

Wanneer u een verkooporder maakt, kunt u een leveringsmethode selecteren in de verkooporderkop en op de verkooporderregels. De leveringsmethode die u in de koptekst selecteert, wordt standaard gebruikt voor alle verkooporderregels. U kunt echter de standaardleveringsmethode op afzonderlijke verkoopregels overschrijven als u wilt. U kunt ook een leveringsmethode definiëren op een klantrecord. Wanneer dan orders voor de klant worden gemaakt, wordt die leveringsmethode standaard gebruikt in de verkooporderkop.

Retail heeft mogelijkheden waarmee gebruikers de leveringsmethoden die kunnen worden gebruikt door een kanaal, de leveringsmethoden die kunnen worden gebruikt voor een product en de leveringsmethoden die geldig zijn voor specifieke verzendingbestemmingen, kunnen beperken. Toeslagen kunnen ook worden gedefinieerd, zodat aanvullende kosten worden toegevoegd aan een order van een klant, op basis van de leveringsmethoden die zijn geselecteerd voor de verkooporder en de totale waarde.

## <a name="define-delivery-modes"></a>Leveringsmethoden definiëren
Voordat u opgeeft welke leveringsmethoden kunnen worden gebruikt voor callcenterorders en de bijbehorende regels en toeslagen definieert, moet u de leveringsmethoden definiëren. Ga naar **Verkoop en marketing \> Instellen \> Distributie \> Leveringsmethoden**. Selecteer **Nieuw** om een nieuwe leveringsmethode te maken. U kunt ook een bestaande leveringsmethode selecteren in de lijst en vervolgens **Bewerken** selecteren om wijzigingen aan te brengen.

In het veld **Leveringsmethode** kunt u elke combinatie van alfanumerieke tekens invoeren, op basis van uw zakelijke behoeften. U kunt vervolgens het veld **Omschrijving** gebruiken om extra context te bieden. De velden **Toeslagengroep** en **Spoed** zijn optioneel en worden verderop in dit onderwerp gedetailleerder beschreven.

Voeg op het sneltabblad **Detailhandelkanalen** een eventueel detailhandelkanaal in dat de leveringsmethode mag gebruiken wanneer verkooptransacties worden gemaakt in dat kanaal.

Op het sneltabblad **Producten** kunt u opgeven voor welke producten en/of productcategorieën de leveringsmethode wel en niet kan worden gebruikt. Als een product bijvoorbeeld niet met luchtpost kan worden verzonden vanwege de beperkingen van gevaarlijk materiaal (hazmat), zorg dat het product of de productcategorie is uitgesloten van alle leveringsmethoden die transport door de lucht betreffen.

Op het sneltabblad **Adressen** kunt u opgeven voor welke landen, regio's of staten de leveringsmethode wel en niet kan worden gebruikt. Orders die worden verzonden naar Hawaï of Alaska komen bijvoorbeeld niet in aanmerking voor de levering over land. Daarom moeten deze staten worden uitgesloten van leveringsmethoden die zijn gekoppeld aan levering over land, maar worden opgenomen in leveringsmethoden die zijn gekoppeld aan levering door de lucht.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Leveringsmethoden voor een callcenterorder valideren
Nadat de leveringsmethoden zijn gedefinieerd, moet u de batchverwerking **Leveringsmethoden verwerken** uitvoeren. Deze taak maakt de leveringsmethoden beschikbaar zodat ze kunnen worden gebruikt in verkooporderprocessen voor detailhandelkanalen. Als u de verwerking **Leveringsmethoden verwerken** wilt uitvoeren, gaat u naar **Retail \> IT detailhandel \> Leveringsmethoden verwerken**. Deze taak moet worden uitgevoerd wanneer nieuwe leveringsmethoden worden toegevoegd aan een detailhandelkanaal of wijzigingen worden aangebracht in bestaande relaties voor leveringsmodus/kanaal.

Nadat u de batchverwerking **Leveringsmethoden verwerken** hebt uitgevoerd, kunt u naar **Detailhandel \> Kanalen \> Callcenters \> Alle callcenters** gaan. Selecteer op de pagina **Alle callcenters** in het actievenster op het tabblad **Instellen** **Leveringsmethoden**. De pagina **Leveringsmethoden** bevat alle geldige leveringsmethoden voor het geselecteerde callcenterkanaal. Als u bestaande leveringsmethoden wilt bewerken of nieuwe leveringsmethoden wilt toevoegen, selecteert u **Leveringsmethoden beheren**. De batchverwerking **Leveringsmethoden verwerken** moet steeds worden uitgevoerd wanneer wijzigingen worden aangebracht.

## <a name="define-charges-for-delivery-services"></a>Toeslagen voor leveringsservices definiëren
Wanneer verkooporders worden gemaakt voor klanten, wil een bedrijf mogelijk toeslagen die automatisch worden berekend, toevoegen op basis van de leveringsmethoden die zijn geselecteerd voor de order. Deze toeslagen kunnen worden geconfigureerd zodat ze hetzelfde zijn voor alle klanten en leveringsmethoden. De toeslagen kunnen ook variëren, afhankelijk van de klant en/of de leveringsmethoden die zijn geselecteerd voor de verkooporder.

Als u toeslagen wilt definiëren, gaat u naar **Detailhandel \> Afzetkanaalinstellingen \> Toeslagen \> Automatische toeslagen**. Selecteer **Nieuw** om nieuwe toeslagen toe te voegen. U kunt ook een bestaand gegeven selecteren en vervolgens **Bewerken** selecteren.

Toeslagen kunnen worden gedefinieerd zodat deze op het niveau van de orderkoptekst of de orderregels worden berekend. Gebruik het veld **Niveau** om het gewenste niveau te selecteren.

Toeslagen kunnen worden gedefinieerd voor een specifieke klant, een groep klanten of alle klanten. Selecteer in het veld **Rekeningcode** **Tabel** om toeslagen te definiëren die alleen op een specifieke klant toegepast worden. Selecteer **Groep** om kosten te definiëren voor een bepaalde klantgroep. Selecteer **Alle** om de toeslagen toe te passen op elke klant die een verkooporder plaatst met de gerelateerde leveringsmethode. Als u **Tabel** of **Groep** hebt geselecteerd in het veld **Rekeningcode**, selecteert u de klant of klantengroep in het veld **Rekeningrelatie**.

Toeslagen kunnen worden geconfigureerd zodat ze worden toegepast voor een bepaalde leveringsmethode, een groep leveringsmethoden of alle leveringsmethoden. Als u **Tabel** selecteert in het veld **Code van leveringsmethode**, moet u een specifieke leveringsmethode selecteren in het veld **Relatie voor leveringsmethode**. Als u **Groep** selecteert, moet u een groep leveringsmethoden selecteren in het veld **Relatie voor leveringsmethode**. Leveringsmethodegroepen worden gedefinieerd op **Detailhandel \> Afzetkanaalinstellingen \> Toeslagen \> Toeslaggroepen voor levering**. Ze kunnen vervolgens worden gekoppeld aan een of meer leveringsmethoden op de pagina **Leveringsmethoden**. Als u een groep selecteert wanneer u toeslagen definieert, gebruikt elke leveringsmethode die is gekoppeld aan de geselecteerde leveringsgroep, deze toeslagen. Ten slotte, als u **Alle** selecteert in het veld **Code van leveringsmethode**, gebruiken alle leveringsmethoden de toeslagen. Daarom selecteert u geen waarde in het veld **Relatie voor leveringsmethode**.

In de **Regels** kunt u indien nodig een of meer toeslagen definiëren per valuta. Toeslagen moeten worden gekoppeld aan een toeslagencode die u de financiële boekingsregels voor de toeslag definieert. Het veld **Categorie** wordt gebruikt om te definiëren hoe toeslagen worden berekend. Bijvoorbeeld: als klanten een vast tarief in rekening moet worden gebracht van $9,95 om een order te verzenden met een specifieke leveringsmethode, gebruikt u de categorie **Vast**. Als het bedrijf beslist klanten een toeslag van een percentage van het ordertotaal in rekening te brengen voor de leveringskosten, gebruikt u de categorie **Percentage** categorie. De feitelijke kosten voor de klanten worden gedefinieerd in het veld **Waarde van toeslagen**.

Detailhandelbedrijven configureren vaak gelaagde toeslagen. In dit geval wordt het bedrag dat klanten voor de levering betalen gebaseerd op de orderwaarde. Als u gelaagde toeslagen wilt configureren, voert u waarden in de velden **Van-bedrag** en **Tot-bedrag** in, naast dat u de toeslag zelf definieert in het veld **Waarde van toeslagen**. Voor orders met een waarde die kleiner is dan € 50, brengt een detailhandelaar bijvoorbeeld € 5,95 in rekening voor verzending over land. Voor orders met een waarde die gelijk is aan of groter is dan € 50, maar minder dan € 100, brengt de detailhandelaar € 7,95 in rekening. Voor orders met een waarde die gelijk is aan of groter is dan € 100, biedt de detailhandelaar gratis verzending. In de volgende afbeelding ziet u de configuratie van deze kosten.

![Voorbeeld van vaste gelaagde toeslagen](media/fixedtieredcharges.png)

U kunt een combinatie van categorieën voor toeslagen gebruiken, afhankelijk van uw zakelijke behoeften. Voor alle orders met een waarde die kleiner is dan € 100, is er bijvoorbeeld een vaste toeslag van € 9,95 voor verzending. Voor orders met een waarde die gelijk is aan of groter is dan € 100, worden leveringstoeslagen berekend volgens een percentage van 5 procent van de orderwaarde. In de volgende afbeelding ziet u de configuratie van deze kosten.

![Voorbeeld van gecombineerde gelaagde toeslagen](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Leveringsmethoden toepassen tijdens het invoeren van orders in een callcenter
Wanneer een nieuwe verkooporder wordt gemaakt, moet een waarde worden opgegeven in het veld **Leveringsmethode** op het sneltabblad **Levering** van de verkooporderkoptekst. Dit veld kan automatisch worden ingevuld, op basis van standaardwaarden uit de klantrecord.

De leveringsmethode die is gedefinieerd in de orderkop, wordt automatisch gekopieerd naar de verkooporderregels zodra deze worden gemaakt. U kunt de instelling van de leveringsmethode voor een specifiek regelartikel echter wijzigen op het tabblad **Levering** in het gedeelte **Regeldetails** van de pagina voor verkooporderinvoer.

Als de geselecteerde leveringsmethode niet geldig is voor het product of het afleveradres dat is gedefinieerd voor de order of de orderregel, ontvangt u een foutbericht. U moet dan een leveringsmethode selecteren die is gedefinieerd voor de ondersteuning van die product- of adresconfiguratie.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Berekening van leveringskosten tijdens orderinvoer
Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld voor uw callcenterkanaal, worden verzendkosten automatisch berekend voor verkooporders wanneer gebruikers **Gereed** selecteren. Het volgende bericht verschijnt boven aan de pagina **Overzicht van verkooporder**: 'Gelaagde toeslagen worden berekend.'' De toeslagen die worden berekend, worden opgeteld bij de waarde van het veld **Verkooptotaal**. Op het sneltabblad **Bedrag** bevat het veld **Toeslagen** het totale bedrag van alle toeslagen die zijn berekend voor de order en de regels. Als u een gedetailleerd overzicht van de toeslagen wilt zien, selecteert u **Order** op de pagina **Overzicht van verkooporder** en selecteert u de optie **Toeslagen** om de toeslagen weer te geven, toe te voegen of te bewerken. Houd er rekening mee dat de berekening van leveringstoeslagen in de orderkop is gebaseerd op de leveringsmethode die is gekoppeld aan de koptekst. Leveringstoeslagen op regelniveau worden berekend op basis van de leveringsmethode die is geconfigureerd voor de verkoopregel. Als meerdere leveringsmethoden worden gebruikt op verschillende regels, kunnen meerdere toeslagen worden toegepast en bij elkaar opgeteld. Het totale bedrag wordt vervolgens weergegeven in het veld **Toeslagen** op de pagina **Overzicht van verkooporder**.

Als de instelling **Ordervoltooiing inschakelen** is uitgeschakeld, moeten gebruikers handmatig de berekening van toeslagen activeren. Selecteer op de pagina **Verkooporder** in het actievenster, op het tabblad **Verkopen** in de groep **Berekenen** de optie **Gelaagde toeslagen**. Het bericht 'Gelaagde toeslagen worden berekend' wordt weergegeven. Vervolgens kunt u de optie **Toeslagen** op het tabblad **Verkopen** selecteren om de berekende toeslagen te bekijken, bewerken of verwijderen.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Spoedleveringsmethoden gebruiken in callcenterorders
U kunt desgewenst een versnellingscode koppelen aan een leveringsmethode die u configureert. Deze code wordt gebruikt als hulpmiddel voor prioriteitssortering en rapportage. Op dit moment worden hierdoor geen extra kosten opgeteld bij de order. Als u spoedcodes wilt instellen, gaat u naar **Verkoop en marketing \> Instellen \> Distributie \> Versnellingscodes**.

Orders die de volgende dag met luchtpost worden verzonden, moeten bijvoorbeeld elke dag om 13:00 in het magazijn worden opgehaald. In dit geval kan een versnellingscode worden gemaakt en die code kan worden gekoppeld aan een leveringsmethode voor levering de volgende dag die in het systeem is geconfigureerd. Als het magazijn de orderverzamelingswave maakt, kan de juiste versnellingscode in het veld **Spoed** worden gebruikt als filter, zodat orderverzameling alleen wordt uitgevoerd voor orders met leveringsmethoden die zijn gekoppeld aan deze code.

Wanneer een callcenterorder wordt ingevoerd, kan een versnellingscode ook handmatig worden toegepast op de verkooporderkop of op een afzonderlijke verkooporderregel. De code kan weer worden gebruikt voor sorteren of rapportagedoeleinden. Soms moet een order zorgvuldig worden verwerkt vanwege een probleem van de klantenservice. In dit geval kan een specifieke versnellingscode worden toegepast op de orderkop of -regels om de order te helpen identificeren en prioriteren tijdens de afhandeling.

