---
title: Persoonlijke productaanbevelingen inschakelen
description: In dit artikel wordt beschreven hoe u persoonlijke productaanbevelingen ter beschikking kunt stellen aan klanten in Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283609"
---
# <a name="enable-personalized-recommendations"></a>Persoonlijke aanbevelingen inschakelen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u persoonlijke productaanbevelingen ter beschikking kunt stellen aan klanten in Microsoft Dynamics 365 Commerce.

In Dynamics 365 Commerce kunnen detailhandelaren persoonlijke productaanbevelingen maken (ook wel personalisatie genoemd). Op deze manier kunnen persoonlijke aanbevelingen online en op het verkooppunt (POS) in de klantervaring worden opgenomen. Wanneer de functionaliteit voor persoonlijke instellingen is ingeschakeld, kan het systeem de inkoop- en productgegevens van een gebruiker koppelen om individuele productaanbevelingen te genereren.

## <a name="personalization-prerequisites"></a>Vereisten voor persoonlijke instellingen

Houd er, voordat u persoonlijke productaanbevelingen voor klanten beschikbaar stelt, rekening mee dat productaanbevelingen alleen worden ondersteund voor Commerce-gebruikers die hun opslag naar Azure Data Lake Store hebben gemigreerd. Voordat klanten persoonlijke productaanbevelingen kunnen ontvangen, moeten detailhandelen [productaanbevelingen inschakelen](enable-product-recommendations.md).

> [!NOTE]
> Door productaanbevelingen in te schakelen schakelt u ook persoonlijke instellingen in. Als u persoonlijke instellingen echter uitschakelt, schakelt u de andere typen productaanbevelingen niet uit.

Zie [Overzicht van productaanbevelingen](product-recommendations.md) voor meer informatie over productaanbevelingen.

## <a name="turn-on-personalization"></a>Persoonlijke instellingen inschakelen

Voer de volgende stappen uit om persoonlijke instellingen in te schakelen.

1. Zoek in Commerce-hoofdkantoren naar **Functiebeheer**.
1. Selecteer **Alles** om een lijst met beschikbare functies weer te geven. 
1. Typ **Aanbevelingen** in het zoekvak.
1. Selecteer de functie **Gepersonaliseerde productaanbevelingen**.
1. Selecteer in het eigenschappenvenster **Gepersonaliseerde productaanbevelingen** de optie **Nu inschakelen**.

![Persoonlijke instellingen inschakelen.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Wanneer u persoonlijke instellingen inschakelt, wordt het proces voor het genereren van persoonlijke productaanbevelingslijsten gestart. Mogelijk is maximaal één dag vereist voordat deze lijsten online en op het POS beschikbaar en zichtbaar zijn.

## <a name="personalized-lists"></a>Persoonlijke lijsten

Naast het toestaan van persoonlijke instellingen voor bestaande lijsten die door machines zijn gegenereerd, kunt u met de aanbevelingsservice zowel online als op het POS persoonlijke instellingen voor productdetectie opgeven.

Nadat persoonlijke instellingen is ingeschakeld, kunnen detailhandelaren persoonlijke lijsten met speciale selecties of aanbevelingen voor klanten weergeven op POS-terminals. Daarnaast kunnen detailhandelaren bestaande productaanbevelingslijsten aanpassen en AVG-opties (Algemene verordening gegevensbescherming) bieden voor geverifieerde gebruikers. Als u persoonlijke instellingen uitschakelt, schakelt u deze functies ook uit.

### <a name="online-picks-for-you-lists"></a>Online lijst 'Selectie voor u'

Een lijst 'Selectie voor u' is een via kunstmatige intelligentie en machine learning (AI-ML) gegenereerde lijst waarin een geverifieerde gebruiker een persoonlijke lijst met voorgestelde producten ziet. Deze lijst is gebaseerd op de omnichannel-inkoophistorie van de gebruiker. Persoonlijke aanbevelingen worden dynamisch bijgewerkt wanneer de gebruiker meer inkopen doet. Dit type lijst biedt ook ondersteuning voor het filteren van categorieën, zodat detailhandelaren speciale aanbiedingen kunnen weergeven op basis van navigatiehiërarchieën.

Voordat de lijst 'Selectie voor u' kan worden weergegeven op elke e-Commerce-pagina, moet aan de volgende vereisten voor de gebruiker worden voldaan:

- Gebruikers moeten zijn aangemeld. Anonieme gebruikers krijgen geen persoonlijke aanbevelingen te zien.
- Gebruikers moeten ten minste één inkoop hebben op hun rekening.
- Gebruikers moeten zich aanmelden om persoonlijke aanbevelingen te kunnen ontvangen.

In de volgende afbeelding ziet u een voorbeeld van een lijst 'Selectie voor u' op de pagina van een online winkel.

![Online lijst Selectie voor u.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Lijsten 'Aanbevolen voor klant' op het POS

Om hun clienteling te verbeteren kunnen detailhandelaren bestaande klantdetailpagina's aanpassen door een contextuele lijst 'Aanbevolen voor klant' toe te voegen.

In de volgende afbeelding ziet u een voorbeeld van een lijst 'Aanbevolen voor klant' op een POS-terminal.

![Lijst Aanbevolen voor klant op het POS.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Persoonlijke aanbevelingen toevoegen aan bestaande aanbevelingslijsten

Detailhandelaren kunnen persoonlijke aanbevelingen toevoegen aan bestaande aanbevelingslijsten, zoals 'Nieuw', 'Trending', 'Meest verkocht', 'Wat mensen ook leuk vinden' en 'Vaak samen gekocht'. Wanneer persoonlijke aanbevelingen worden toegevoegd aan bestaande lijsten, worden de artikelen die een aangemelde gebruiker eerder heeft gekocht, uit deze lijsten verwijderd. Voor zowel anonieme gebruikers als gebruikers die zich hebben aangemeld om persoonlijke aanbevelingen te ontvangen, worden standaardversies van de bestaande lijsten weergegeven. Daarom hoeven detailhandelaren niet handmatig afzonderlijke paginaversies te onderhouden.

Een aangemelde gebruiker heeft bijvoorbeeld het zwarte horloge en de bruine werkschoenen al gekocht die worden weergegeven in de lijst 'Trending - standaard' in de volgende afbeelding. De gebruiker ziet daarom nieuwe producten in plaats van deze producten, zoals wordt weergegeven in de lijst 'Trending - persoonlijk'.

![Persoonlijke instellingen toepassen.](./media/applypersonalization.png)

Als u persoonlijke instellingen wilt toepassen op een bestaande aanbevelingslijst in de Commerce Site Builder, voert u de volgende stappen uit.

1. Open een bestaande pagina voor Site Builder die een productverzamelingsmodule bevat.
1. Selecteer de productverzamelingsmodule in het navigatievenster aan de linkerkant.
1. Selecteer in het navigatievenster rechts de lijst onder **Producten**.
1. Selecteer het lijsttype in het dialoogvenster **Productlijstconfiguratie selecteren** onder **Type**.
1. Schakel het selectievakje **Persoonlijke instellingen toepassen** in en selecteer vervolgens **OK**.

    ![Persoonlijke instellingen toepassen op een trendlijst.](./media/ApplyPersonalizationToTrending.PNG)

1. Sla de pagina op, voltooi de bewerking ervan en publiceer de pagina vervolgens. Nadat de pagina is gepubliceerd, zien aangemelde gebruikers aangepaste trendlijsten.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht productaanbevelingen](product-recommendations.md)

[Azure Data Lake Storage inschakelen in een Dynamics 365 Commerce-omgeving](enable-adls-environment.md)

[Productaanbevelingen inschakelen](enable-product-recommendations.md)

[Aanbevelingen voor vergelijkbare artikelen inschakelen](shop-similar-looks.md)

[Afmelden voor gepersonaliseerde aanbevelingen](personalization-gdpr.md)

[Productaanbevelingen toevoegen op POS](product.md)

[Aanbevelingen toevoegen aan het transactiescherm](add-recommendations-control-pos-screen.md)

[Resultaten van AI-ML-aanbevelingen aanpassen](modify-product-recommendation-results.md)

[Handmatig gecureerde aanbevelingen maken](create-editorial-recommendation-lists.md)

[Aanbevelingen maken met voorbeeldgegevens](product-recommendations-demo-data.md)

[Veelgestelde vragen over productaanbevelingen](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
