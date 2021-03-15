---
title: De ontvangst van retourartikelen registreren
description: U kunt de ontvangst van geretourneerde artikelen registreren met het formulier Ontvangstoverzicht of Registratie.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b46801ee150d1cf25d8f4c6ea9aaa8011e1cbd38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006611"
---
# <a name="register-the-receipt-of-returned-items"></a>De ontvangst van retourartikelen registreren 

[!include [banner](../includes/banner.md)]


Er zijn twee methoden beschikbaar voor het registreren van de ontvangst van geretourneerde artikelen. De eerste methode is een ontvangstproces in het magazijn dat gebruikmaakt van het formulier **Aankomstoverzicht**. De tweede gebruikt het formulier **Registratie**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>De ontvangst van geretourneerde artikelen registreren met het formulier Overzicht aankomst

U kunt het formulier **Aankomstoverzicht** gebruiken om een retourzending te identificeren volgens het bijbehorende RMA-nummer (Return Material Authorization). Als een journaalnaam is gedefinieerd op het tabblad **Instellen** en de journaalregels die overeenkomen met de regels die zijn geselecteerd op het formulier **Aankomstoverzicht** bestaan, wordt een nieuwe journaalkop gemaakt wanneer u klikt op **Begin aankomst**.

1.  Klik op **Voorraadbeheer** \> **Periodiek** \> **Overzicht aankomst**.

2.  Selecteer in het veld **Naam instelling** **Retourorder** en klik vervolgens op **Update**.
    

    > [!TIP]
    > <P>U kunt de <STRONG>Bereik</STRONG>-velden gebruiken om de zoekresultaten te beperken. U kunt het RMA-nummer typen of selecteren in het veld <STRONG>RMA-nummer</STRONG> voor een exact resultaat. Als u een reeks filters wilt definiëren en opslaan waarmee wordt beperkt welke inkomende ontvangsten worden weergegeven, klikt u op het tabblad <STRONG>Instellen</STRONG>. De beschikbare filters zijn typen, magazijnen en docks.</P>

    

    > [!WARNING]
    > <P>Retourorders kunnen niet worden gecombineerd met andere aankomsttypen in het formulier <STRONG>Aankomstoverzicht</STRONG>. Daarom de verkooporder altijd de referentie zijn, maar wordt er geen verkooporder-ID opgegeven op de journaalkop.</P>



3.  Zoek in het raster **Ontvangsten** naar de regel die overeenkomt met het artikel dat wordt geretourneerd en schakel het selectievakje in de kolom **Selecteren voor aankomst** in.

4.  Als u bepaalde regels, zoals artikelen uit de oorspronkelijke order die niet zijn opgenomen in de retourzending, wilt uitsluiten van de retourontvangst, schakelt u de bijbehorende selectievakjes **Selecteren voor aankomst** in de tabel **Regels** in het onderste gedeelte van het formulier uit.

5.  Klik op de knop **Begin aankomst** om een aankomstjournaal te maken.
    

    > [!NOTE]
    > <P>U kunt meerdere retourorders selecteren en deze opnemen in één aankomstproces. Elke retourorderregel wordt gekopieerd naar een overeenkomstige aankomstjournaalregel.</P>

    

    > [!NOTE]
    > <P>U kunt ook handmatig een aankomstjournaal maken met het formulier <STRONG>Artikelontvangst</STRONG>. 



6.  Ga naar **Voorraadbeheer** \> **Journaalposten** \> **Artikelontvangst** \> **Artikelontvangst**.

7.  Selecteer het aankomstjournaal dat u zojuist hebt gemaakt en klik vervolgens op **Regels** om het formulier **Journaalregels, locaties** te openen.

8.  Pas op het tabblad **Algemeen** het nummer aan in het veld **Hoeveelheid** indien dit nodig is en wijs vervolgens een beschikkingscode toe in het veld **Beschikkingscode**.
    
    U kunt ook het selectievakje **Quarantainebeheer** inschakelen om de geretourneerde artikelen een inspectieproces te laten ondergaan in het kader van een quarantaineorder.
    

    > [!NOTE]
    > <P>Als u de geretourneerde artikelen in quarantaine plaatst, kunt u geen beschikkingscode opgeven.</P>



9.  Klik op de knop **Valideren**.

10. Klik op **Boeken** als het validatieproces geen fouten bevat.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>De ontvangst van geretourneerde artikelen registreren met het registratieformulier.

Als alternatief voor het formulier **Aankomstoverzicht** kunt u het formulier **Registratie** gebruiken om de aankomst van geretourneerde artikelen te registreren.

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**. Een nieuwe retourorder maken of de retourorder openen in de lijst. Selecteer de retourorderregel op het sneltabblad **Regels**. Klik op **Regel bijwerken** en klik vervolgens op **Registratie**.

2.  Wijs een beschikkingscode toe in het veld **Beschikkingscode** en klik op **OK**.
    

    > [!NOTE]
    > <P>Het is niet mogelijk het artikel te verzenden voor inspectie als een quarantaineorder met het formulier <STRONG>Registratie</STRONG>.</P>



3.  Selecteer in het raster **Transacties** de transactie die moet worden geregistreerd.

4.  Klik in het raster **Nu registreren** op **Toevoegen**. Herhaal de vorige twee stappen totdat alle geretourneerde artikelen worden weergegeven in het raster **Nu registreren**.

5.  Klik op **Alles boeken**.

## <a name="see-also"></a>Zie ook

[Overzicht aankomst (formulier)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]