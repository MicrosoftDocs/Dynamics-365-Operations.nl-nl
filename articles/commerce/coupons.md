---
title: Coupons
description: In dit artikel vindt u een overzicht van de mogelijkheden voor coupons in Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709754"
---
# <a name="coupons"></a>Coupons

[!include [banner](../includes/banner.md)]

In dit artikel vindt u een overzicht van de mogelijkheden voor coupons in Microsoft Dynamics 365 Commerce.

Coupons zijn codes en streepjescodes die worden gebruikt om kortingen aan transacties toe te voegen. Detailhandelaren verdelen coupons onder potentiële of bestaande klanten om de naamsherkenning te verbeteren, de conversie te stimuleren, hun klantenbasis te behouden, de verkoop te versterken en uiteindelijk de opbrengst te verhogen. Coupons zijn een van de populairste marketingprogramma's geworden en zijn een nieuwe norm in e-commerceverkoop.

In Dynamics 365 Commerce worden coupons gekoppeld aan kortingen en worden ze beschouwd als extra validatie boven op kortingen. Elke coupon is gerelateerd aan één korting, en de gekoppelde korting definieert de set producten waar de coupon geldig voor is.

Prijsgroepen die aan een korting zijn gekoppeld, definiëren de voorwaarden waaronder een coupon kan worden gebruikt. Deze voorwaarden omvatten klantengroepen en verkoopkanalen. Coupons geven ook de **gebruikslimiet** en **de vereiste klanteigenschappen** aan die kunnen worden gebruikt om optionele gebruiksbeperkingen te configureren.

Elke coupon kan meerdere couponcodes en couponstreepjescode bevatten en elke code kan een eigen geldigheidsperiode en status hebben. Als de status van een code is ingesteld op **Inactief**, kan de code in geen enkel kanaal worden gebruikt.

## <a name="set-up-a-coupon"></a>Een coupon instellen

Voordat u een coupon kunt instellen, moet u de streepjescode en twee nummerreeksen voor de coupon instellen.

Volg deze stappen als u een coupon in Commerce headquarters wilt instellen.

1. Ga naar **Detailhandel en commerce \> Voorraadbeheer \> Streepjescodes en etiketten \> Maskertekens**.
1. Selecteer **Toevoegen** om een maskerteken van het type **Couponcode** te maken. In het veld **Teken** kunt u elk ongebruikt teken selecteren.
1. Ga naar **Detailhandel en commerce \> Voorraadbeheer \> Streepjescodes en etiketten \> Instellingen streepjescodemasker**.
1. Selecteer **Nieuw** om een streepjescodemasker van het type **Coupon** te maken.
1. Ga naar **Detailhandel en commerce \> Voorraadbeheer \> Streepjescodes en etiketten \> Instellingen streepjescode**.
1. Selecteer **Nieuw** om een streepjescode te maken met het streepjescodemasker dat u zojuist hebt gemaakt.
1. Ga naar **Organisatiebeheer \> Nummerreeksen**.
1. Maak twee nummerreeksen:

    1. Eén reeks voor de referentie **Couponnummer**. Deze reeks bepaalt de unieke id van coupon.
    1. Eén reeks voor de referentie **Couponcode-id**. De reeks bepaald de unieke id voor elke couponcode voor een coupon.

    U moet voor beide nummerreeksen het veld **Bereik** instellen op **Bedrijf**. In de meeste gevallen moeten beide volgnummers automatisch worden gegenereerd.

1. Ga naar **Commerce-parameters \> Prijzen en kortingen \> Coupons**.
1. Stel het veld **Streepjescodemasker voor coupon** in op de streepjescode die u eerder hebt gemaakt.
1. Ga naar **Commerce-parameters \> Nummerreeksen**.
1. Selecteer de nummerreeksen die u eerder hebt gemaakt voor de referenties **Couponnummer** en **Couponcode-id**.

Als u een coupon wilt instellen, moet u de korting en de coupon afzonderlijk maken en deze vervolgens koppelen door de korting te selecteren in het veld **Korting** van de couponconfiguratie. Nadat een coupon aan een korting is gekoppeld, worden de velden **Status**, **Ingangsdatum** en **Vervaldatum** van de gekoppelde korting alleen-lezen omdat de waarden worden bepaald door de status en geldigheidsperiode van de coupon. Wanneer de status van een coupon is ingesteld op **Actief**, wordt de status van de gekoppelde korting automatisch ingesteld op **Ingeschakeld**. Wanneer de status van een coupon is ingesteld op **Inactief**, wordt de status van de gekoppelde korting ook automatisch ingesteld op **Uitgeschakeld**.

## <a name="use-a-coupon"></a>Een coupon gebruiken

Als u een coupon wilt toevoegen aan een verkooptransactie in Commerce POS, kunt u een couponcode of streepjescode van coupon gebruiken. Als u een couponcode wilt gebruiken, selecteert u de bewerking **Coupon toevoegen** en voert u de code in. Als u streepjescode van een coupon wilt gebruiken, scant u de streepjescode met een scanapparaat of voert u de streepjescode in met het numerieke toetsenbord in het scherm **Transactie**.

Detailhandelaren willen soms dat kassiers een vast kortingsbedrag aan klanten kunnen geven vanwege klanten tevreden te stellen of vanwege productafwijkingen, maar ze willen geen couponcodes afdrukken en ze aan de kassiers distribueren. In dit geval kunt u de optie **Toepassen zonder couponcode** voor de coupon instellen op **Ja**. POS-kassiers kunnen vervolgens de functie **Coupon toepassen** in de bewerking **Beschikbare kortingen weergeven** gebruiken om een coupon aan een transactie toe te voegen zonder de code handmatig in te voeren. Als er meerdere couponcodes voor een coupon zijn, selecteert het systeem automatisch de eerste actieve code en past deze toe voor de transactie.

Voor het toevoegen van een coupon aan een verkooporder voor een callcenter, moet een callcentergebruiker **Coupons** selecteren op het tabblad **Beheren** van het actievenster op de verkooporderpagina.

Voor het toevoegen van een coupon aan een e-commerceorder, kan de klant de couponcode invoeren in het **promotiecodeveld** in de winkelwagen.

Nadat een coupon is toegevoegd aan een verkooporder, wordt door de prijsengine onmiddellijk een herberekening voor de gehele order ingeschakeld, ongeacht of vertraagde berekening is ingeschakeld.

> [!NOTE]
> In Commerce versie 10.0.30 en eerder moeten callcentergebruikers nadat ze een coupon hebben toegevoegd aan een verkooporder van een callcenter, **Opnieuw berekenen** selecteren in de groep **Berekenen** op het tabblad **Verkopen** van het actievenster om de korting toe te passen die aan die coupon is gekoppeld.

## <a name="coupon-usage-limit"></a>Limiet coupongebruik

Coupons kunnen worden geconfigureerd voor beperkt gebruik. Deze beperkingen kunnen worden gedefinieerd per klant, per kanaal of als een algehele beperking. De gebruikslimiet wordt afgedwongen per couponcode op een coupon. Een coupon voor eenmalig gebruik met twee couponcodes kan bijvoorbeeld twee maal worden gebruikt: voor elke couponcode één keer.

Coupons kunnen worden gebruikt voor alle verkoopkanalen. Voor callcenters kunnen coupons voor beperkt gebruik echter alleen worden toegepast wanneer de instelling **Ordervoltooiing inschakelen** voor het callcenterkanaal is ingeschakeld. Als de instelling **Ordervoltooiing inschakelen** is uitgeschakeld, kunnen alleen niet-beperkte coupons worden toegepast.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
