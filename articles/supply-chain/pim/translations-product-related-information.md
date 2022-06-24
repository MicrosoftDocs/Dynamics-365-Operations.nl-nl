---
title: Veelgestelde vragen (FAQ) over productgerelateerde vertalingen
description: Dit artikel beschrijft hoe u vertalingen voor producten, productdimensiewaarden en productkenmerken kunt beheren.
author: t-benebo
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2798e25d1f6c293aa71a6c143ded5293f241060
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850549"
---
# <a name="product-related-translations-faq"></a>Veelgestelde vragen (FAQ) over productgerelateerde vertalingen

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft hoe u vertalingen voor producten, productdimensiewaarden en productkenmerken kunt beheren. 

## <a name="what-product-related-data-can-be-translated"></a>Welke productgerelateerde gegevens kunnen worden vertaald?

U kunt vertalingen voor de volgende productgerelateerde informatie maken:
-   Namen en omschrijvingen van producten.
-   Omschrijvingen, beschrijvende namen en help-tekst van productkenmerkwaarden.
-   Namen en omschrijvingen van de productdimensiewaardes.

U kunt de productgerelateerde informatie in elke taal vertalen die in het formulier **Tekstvertaling** beschikbaar is. Raadpleeg voor meer informatie de volgende sectie **Hoe kan ik vertalingen voor productgerelateerde informatie maken**.

## <a name="where-can-i-view-the-translated-information"></a>Waar kan ik de vertaalde informatie weergeven?
U kunt vertalingen van productgerelateerde informatie in een extern brondocument, zoals een factuur weergeven, die een taal gebruikt waarvan de vertalingen beschikbaar zijn.

## <a name="how-do-i-create-translations-for-product-related-information"></a>Hoe maak ik vertalingen voor productgerelateerde informatie?
Om een vertaling te maken voor een project, volgt u deze stappen:
1.  Klik op **Productgegevensbeheer** &gt; **Algemeen** &gt; **Vrijgegeven producten**.
2.  Selecteer een product en klik in het venster Actie, in de groep **Talen** op **Vertalingen**.
3.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Om meer talen te voegen, vouwt u het veld **Taal** uit en klikt u op **OK**.
4.  Voer in de groep **Vertaalde tekst** vertalingen in in de velden **Omschrijving** en **Productienaam**.

Om vertalingen te maken voor productkenmerken, volgt u deze stappen:
1.  Klik op **Productgegevensbeheer** &gt; **Algemeen** &gt; **Vrijgegeven producten**.
2.  Klik onder **Instellen** op **Kenmerken** en vervolgens op **Kenmerken**.
3.  Klik op de pagina **Kenmerken** op **Vertalen**.
4.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Om meer talen te voegen, vouwt u het veld **Taal** uit en klikt u op **OK**.
5.  Voer in de groep **Vertaalde tekst** vertalingen in in de velden **Omschrijving** en **Beschrijvende naam** en **Help-tekst**.

Om een vertaling te maken voor een productdimensiewaarden volgt u deze stappen:
1.  Klik op **Productgegevensbeheer** &gt; **Algemeen** &gt; **Vrijgegeven producten**.
2.  Selecteer een product en klik op **Productdimensies**.
3.  Selecteer een van de koppelingen voor de productdimensies: **Configuraties**, **Afmetingen** **Kleuren** of **Opmaakmodel**.
4.  Selecteer een dimensiewaarde en klik dan op **Vertalen**.
5.  Selecteer een taal op de pagina **Tekstvertaling** in het veld **Taal**. Om meer talen te voegen, vouwt u het veld **Taal** uit en klikt u op **OK**.
6.  Voer in de groep **Vertaalde tekst** vertalingen in in de velden **Naam** en **Omschrijving**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Kunnen de namen van productvarianten worden vertaald?
Productvarianten zijn gebaseerd op de dimensies van een vrijgegeven product. De namen van productvarianten zijn gebaseerd op een combinatie van dimensiewaarden. Als de dimensiewaarden worden vertaald die aan een productvariant zijn gekoppeld, verschijnt de naam van de productvariant in de vertaalde versie.  

**Voorbeeld**  

Uw product is een T-shirt die in verschillende grootte en kleuren beschikbaar is en de verschillende namen zijn gebaseerd op de volgende gegevens:
-   Productnummer: \#3
-   Dimensies: Grootte en kleur
-   Groottedimensiewaarden: Small, Medium, Large
-   Kleurdimensiewaarden: Groen, Zwart, rood

De naam van een productvariant die op is gebaseerd op de dimensiewaarden Small en Rood is **\#3:Small:Rood**.  

Een klant wil enkele rode T-shirts small kopen en de naam van het T-shirt moet in het Frans op de factuur worden weergegeven. U vertaalt de dimensiewaarden, Small en Rood, in het Frans, en de naam van de productvariant is **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Om de voorkeurstaal van een klant in te stellen, volgt u deze stappen:
<ol><br/><li>Klik op <strong>Verkoop en marketing</strong> &gt; <strong>Algemeen</strong> &gt; <strong>Klanten</strong> &gt; <strong>Alle</strong> <strong>klanten</strong>.</li>
<li>Dubbelklik op een klant om de pagina <strong>Klanten</strong> te openen. Selecteer op het tabblad <strong>Algemeen</strong> in het veld <strong>Taal</strong> de <strong>taal</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Wat moet gebeuren als een klant een voorkeurstaal heeft waarvoor geen vertalingen beschikbaar zijn?
Als de vertalingen niet beschikbaar zijn in de voorkeurstaal van de klant, worden de namen en omschrijvingen weergegeven in de globale taal van uw eigen bedrijf.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kan ik vertalingen beheren voor een reeks dimensiewaarden tegelijk?
Dimensiewaarden zijn productspecifiek en u kunt de vertalingen voor de dimensiewaarden voor elk product beheren. Als u echter een dimensiewaardegroep maakt en vertalingen maakt voor de waarden in de waardegroep maakt, is het eenvoudiger om de vertalingen te beheren.   

**Voorbeeld**  

Uw bedrijf maakt T-shirts in verschillende stijlen en elke stijl is beschikbaar in de maten Small, Medium en Large. De groottes worden in één dimensiewaardegroep verzameld. Wanneer een nieuwe t-shirtstijl wordt toegevoegd, kunt u deze aan de dimensiewaardegroep koppelen die wordt gebruikt voor groottes, zodat alle groottes beschikbaar zijn voor het product. U kunt ook op elk moment vertalingen toevoegen of wijzigen voor de groottes in de dimensiewaardegroep.  

Een dimensiewaarde die aan een product is gekoppeld door een dimensievariantgroep moet worden beheerd vanaf de productvariantgroep.   
Volg deze stappen om een dimensiewaardegroep te maken:
1.  Klik op **Productgegevensbeheer** &gt; **Instellen** &gt; **Variantgroepen**.
2.  Selecteer **Grootte** **groepen**, **Kleurgroepen** of **Stijlgroepen**.
3.  Klik op **Nieuw**, en typ vervolgens een naam voor de groep in het veld **Grootte** **groep**, **Kleurgroep** of **Stijlgroep**. Klik op **Afmetingen**, **Kleuren** of **Stijlen** om regels voor de groepen te maken.
4.  Klik op de pagina **Groottegroep** regels, **Kleurgroepregels** of **Stijlgroepregels** op **Nieuw** en maak vervolgens de grootten, de kleuren en de stijlen voor de groepen.

Om vertalingen voor waarden in een dimensiewaardegroep te beheren, volgt u deze stappen:
1.  Volg de stappen in de vorige procedure om een dimensiewaardegroep te maken om de pagina **Groottegroepregels**, **Kleurgroepregels** of **Stijlgroepregels** te openen.
2.  Klik op **Tekstvertaling**. Typ op de pagina **Tekstvertaling** in de groep **Vertaalde tekst** vertalingen in de velden **Naam** en **Omschrijving**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Wanneer kunnen vertalingen van productgerelateerde informatie worden beheerd?
Vertalingen van productgerelateerde informatie kunnen op elk moment worden beheerd. Wanneer vertalingen worden bijgewerkt voor een dimensiewaarde die aan een product is gekoppeld, wordt de productinformatie bijgewerkt, ongeacht of het product transacties heeft.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]