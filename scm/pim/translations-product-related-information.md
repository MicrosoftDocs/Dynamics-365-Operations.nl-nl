---
title: Productgebonden vertalingen Veelgestelde vragen
description: Dit onderwerp beschrijft hoe u vertalingen voor producten, productdimensiewaarden en productkenmerken kunt beheren.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Productgebonden vertalingen Veelgestelde vragen

Dit onderwerp beschrijft hoe u vertalingen voor producten, productdimensiewaarden en productkenmerken kunt beheren. 

<a name="what-product-related-data-can-be-translated"></a>Welke productgerelateerde gegevens kunnen worden vertaald?
--------------------------------------------

U kunt vertalingen voor de volgende productgerelateerde informatie maken:
-   Namen en omschrijvingen van producten.
-   Omschrijvingen, beschrijvende namen en help-tekst van productkenmerkwaarden.
-   Namen en omschrijvingen van de productdimensiewaardes.

U kunt de productgerelateerde informatie in elke taal vertalen die in het formulier **Tekstvertaling** beschikbaar is. Raadpleeg voor meer informatie de volgende sectie **Hoe kan ik vertalingen voor productgerelateerde informatie maken**.

## <a name="where-can-i-view-the-translated-information"></a>Waar kan ik de vertaalde informatie weergeven?
U kunt vertalingen van productgerelateerde informatie in een extern brondocument, zoals een factuur weergeven, die een taal gebruikt waarvan de vertalingen beschikbaar zijn.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Hoe maak ik vertalingen voor productrelated informatie
Om een vertaling te maken voor een project, volgt u deze stappen:
1.  Klik op **productgegevensbeheer**&gt;**veelgebruikte**&gt;**vrijgegeven producten**.
2.  Selecteer een product en in het actievenster in de **talen** groep, klikt u op **vertalingen**.
3.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Voor het toevoegen van meer talen, vouw de **taal**, en klik vervolgens op **OK**.
4.  Voer in de groep **Vertaalde tekst** vertalingen in in de velden **Omschrijving** en **Productienaam**.

Om vertalingen te maken voor productkenmerken, volgt u deze stappen:
1.  Klik op **productgegevensbeheer**&gt;**veelgebruikte**&gt;**vrijgegeven producten**.
2.  Klik onder **Instellen** op **Kenmerken** en vervolgens op **Kenmerken**.
3.  Klik op de pagina **Kenmerken** op **Vertalen**.
4.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Voor het toevoegen van meer talen, vouw de **taal**, en klik vervolgens op **OK**.
5.  Voer in de groep **Vertaalde tekst** vertalingen in in de velden **Omschrijving** en **Beschrijvende naam** en **Help-tekst**.

Om een vertaling te maken voor een productdimensiewaarden volgt u deze stappen:
1.  Klik op **productgegevensbeheer**&gt;**veelgebruikte**&gt;**vrijgegeven producten**.
2.  Selecteer een product en klik op **Productdimensies**.
3.  Selecteer een van de koppelingen voor de productdimensies: **Configuraties**, **Afmetingen** **Kleuren** of **Opmaakmodel**.
4.  Selecteer een dimensiewaarde en klik dan op **Vertalen**.
5.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Voor het toevoegen van meer talen, vouw de **taal**, en klik vervolgens op **OK**.
6.  In de **vertaalde tekst** groep, voer vertalingen in de **naam** en **omschrijving** velden.

## <a name="can-the-names-of-product-variants-be-translated"></a>Kunnen de namen van productvarianten worden vertaald?
Productvarianten zijn gebaseerd op de dimensies van een vrijgegeven product. De namen van productvarianten zijn gebaseerd op een combinatie van dimensiewaarden. Als de dimensiewaarden worden vertaald die aan een productvariant zijn gekoppeld, verschijnt de naam van de productvariant in de vertaalde versie.  

**Voorbeeld**  

Uw product is een T-shirt die in verschillende grootte en kleuren beschikbaar is en de verschillende namen zijn gebaseerd op de volgende gegevens:
-   Productnummer: \#3
-   Dimensies: Grootte en kleur
-   Groottedimensiewaarden: Small, Medium, Large
-   Kleurdimensiewaarden: Groen, Zwart, rood

De naam van een productvariant die is gebaseerd op de dimensie kleine waarden en rood is **\#3:Small:Red**.  

Een klant wil enkele rode T-shirts small kopen en de naam van het T-shirt moet in het Frans op de factuur worden weergegeven. U de dimensiewaarden klein en rood, vertalen in de Franse en de naam van de productvariant is **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Om de voorkeurstaal van een klant in te stellen, volgt u deze stappen:
<ol>  
<li>Klik op <strong>verkoop en marketing</strong>&gt;<strong>veelgebruikte</strong>&gt;<strong>klanten</strong>&gt;<strong>alle</strong> <strong>klanten</strong>.</li>
<li>Dubbelklik op een klant om de pagina <strong>Klanten</strong> te openen. Selecteer op het tabblad <strong>Algemeen</strong> in het veld <strong>Taal</strong> de <strong>taal</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Wat moet gebeuren als een klant een voorkeurstaal heeft waarvoor geen vertalingen beschikbaar zijn?
Als de vertalingen niet beschikbaar zijn in de voorkeurstaal van de klant, worden de namen en omschrijvingen weergegeven in de globale taal van uw eigen bedrijf.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kan ik vertalingen beheren voor een reeks dimensiewaarden tegelijk?
Dimensiewaarden zijn productspecifiek en u kunt de vertalingen voor de dimensiewaarden voor elk product beheren. Als u echter een dimensiewaardegroep maakt en vertalingen maakt voor de waarden in de waardegroep maakt, is het eenvoudiger om de vertalingen te beheren.   

**Example**  

Uw bedrijf maakt T-shirts in verschillende stijlen en elke stijl is beschikbaar in de maten Small, Medium en Large. De groottes worden in één dimensiewaardegroep verzameld. Wanneer een nieuwe t-shirtstijl wordt toegevoegd, kunt u deze aan de dimensiewaardegroep koppelen die wordt gebruikt voor groottes, zodat alle groottes beschikbaar zijn voor het product. U kunt ook op elk moment vertalingen toevoegen of wijzigen voor de groottes in de dimensiewaardegroep.  

Een dimensiewaarde die aan een product is gekoppeld door een dimensievariantgroep moet worden beheerd vanaf de productvariantgroep.   
Volg deze stappen om een dimensiewaardegroep te maken:
1.  Klik op **productgegevensbeheer**&gt;**Setup**&gt;**variantgroepen**.
2.  Selecteer **Groottegroepen******, **Kleurgroepen** of **Stijlgroepen**.
3.  Klik op **New**, en voer vervolgens een naam voor de groep in de **grootte****groep**, **kleurgroep**, of **stijlgroep** veld. Klik op **Afmetingen**, **Kleuren** of **Stijlen** om regels voor de groepen te maken.
4.  In de **grootte****groep** regels, **kleur****groep****regels**, of **stijl groepstructuur** pagina, klikt u op **New**, en maak vervolgens de maten, kleuren en stijlen voor de groepen.

Om vertalingen voor waarden in een dimensiewaardegroep te beheren, volgt u deze stappen:
1.  Volg de stappen in de vorige procedure om een dimensiewaardegroep te maken om de pagina **Groottegroepregels**, **Kleurgroepregels** of **Stijlgroepregels** te openen.
2.  Klik op **Tekstvertaling**. In de **tekstvertaling** pagina in de **vertaalde tekst** groep, voer vertalingen in de **naam** en **omschrijving** velden.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Wanneer de vertaling van productrelated informatie kunnen worden beheerd?
Vertalingen van productgerelateerde informatie kunnen op elk moment worden beheerd. Wanneer vertalingen worden bijgewerkt voor een dimensiewaarde die aan een product is gekoppeld, wordt de productinformatie bijgewerkt, ongeacht of het product transacties heeft.




