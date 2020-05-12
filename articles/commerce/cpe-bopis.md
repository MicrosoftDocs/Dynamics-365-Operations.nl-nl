---
title: BOPIS configureren in een Dynamics 365 Commerce-omgeving
description: In dit onderwerp wordt uitgelegd hoe u online kopen, ophalen in winkel (BOPIS) kunt configureren, in een Microsoft Dynamics 365 Commerce-omgeving nadat deze is ingericht.
author: rubendel
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 956d66d09885d4d54655ce25b3aa7ba6a9c34cf4
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282791"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-environment"></a>BOPIS configureren in een Dynamics 365 Commerce-omgeving


[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u online kopen, ophalen in winkel (BOPIS) kunt configureren, in een Microsoft Dynamics 365 Commerce-omgeving nadat deze is ingericht.

## <a name="prerequisite"></a>Vereiste

Voltooi de procedures in dit onderwerp pas nadat uw preview-omgeving van Commerce is ingericht en geconfigureerd. Zie [Een preview-omgeving van Dynamics 365 Commerce inrichten](provisioning-guide.md) en [Een preview-omgeving van Dynamics 365 Commerce configureren](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning) voor meer informatie over het inrichten en configureren van uw omgeving.

Nadat uw Commerce-omgeving is ingericht en volledig is geconfigureerd, kunt u dit onderwerp gebruiken om BOPIS-scenario's in te schakelen.

## <a name="configure-the-pos"></a>Het POS configureren

### <a name="configure-modern-pos"></a>Modern POS configureren

BOPIS-scenario's waarbij een creditcardbetaling nodig is, vereisen een hardwarestation. Het hardwarestation is ingebouwd in de Modern POS-programma's voor Windows en Android-clients. Als u met Cloud POS of Modern POS voor iOS werkt, moet de POS-client zijn gekoppeld aan een gedeeld hardwarestation. In dit onderwerp wordt uitgelegd hoe u BOPIS configureert voor Windows en Android-clients. Zie voor meer informatie over het instellen van een gedeeld hardwarestation het onderwerp [Retail Hardware Station configureren en installeren](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Ga naar **Detailhandel en Commerce \> Kanaalinstellingen \> POS-instellingen \> Kassa's**.
2. Selecteer **SANFRAN-5** registreren en vervolgens **Bewerken**.
3. Wijzig de waarde van het veld **Hardwareprofiel** van **HW002** in **HW001** en selecteer **Opslaan**.
4. Als u de wijzigingen wilt synchroniseren, gaat u naar **Detailhandel en commerce \> IT detailhandel en Commerce \> Distributieplanning**.
5. Selecteer de distributieplanning **1090** en selecteer vervolgens **Nu uitvoeren** in het actievenster.
6. Selecteer **Ja** en klik vervolgens op **OK** om de gegevenssynchronisatie te starten. 

### <a name="install-modern-pos"></a>Modern POS installeren

1. Ga naar **Detailhandel en Commerce \> Kanaalinstellingen \> POS-instellingen \> Apparaten**.
2. Selecteer apparaat **SANFRANCIS-5**.
3. Selecteer in het actievenster de optie **Download** en selecteer vervolgens **Configuratiebestand**.
4. Selecteer **Download** en vervolgens **Retail Modern POS**. 
5. Selecteer **Bestand openen** wanneer het bestand **ModernPOSSetup.exe** is gedownload.

    ![Bestand openen](./dev-itpro/media/PAYMENTS/openfile.png)

6. Klik op **Volgende** om door te gaan met het installatieproces. Selecteer **Sluiten** wanneer de installatie is voltooid.

### <a name="activate-modern-pos"></a>Modern POS activeren

1. Klik op het bureaublad van Windows op de knop **Start** en typ **Retail Modern POS**.
2. Selecteer de **Retail Modern POS**-toepassing om activering te starten.
3. Selecteer **Volgende**. De velden **Server-URL**, **Apparaat-id** en **Registernummer** moeten vooraf worden ingesteld met informatie uit het configuratiebestand dat u in de vorige procedure hebt gedownload.
4. Selecteer **Activeren**.
5. Het verificatiedialoogvenster wordt weergegeven. Selecteer de rekening die gebruikmaakt van het e-mailadres dat eerder is gekoppeld aan werknemer **000713 - Andrew Collette**.

    > [!NOTE]
    > Als u nog geen werknemer hebt gekoppeld aan uw identiteit, wordt de activering niet voltooid. Volg in dat geval de stappen onder de sectie "Een medewerker aan uw identiteit koppelen" in het onderwerp [Een Dynamics 365 Commerce-voorbeeldomgeving configureren](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Selecteer **Alleen deze app** bij de vraag en laat uw organisatie het apparaat beheren.
7. Wanneer de activering is voltooid, selecteert u **Aan de slag**.

### <a name="enable-bopis-in-modern-pos"></a>BOPIS inschakelen in Modern POS

1. Meld u aan bij Modern POS door **000713** te gebruiken als operator-id en **123** als wachtwoord.
2. Terwijl de introductievideo wordt afgespeeld, schakelt u de twee selectievakjes in de linkerbenedenhoek van het dialoogvenster in en sluit u het dialoogvenster.
3. Als u niet wordt gevraagd de ploeg af te sluiten, schuift u naar rechts op de pagina **Welkom**, selecteert u **Ploeg sluiten** en meldt u zich vervolgens weer aan bij het POS.
4. Wanneer u bent aangemeld, selecteert u **Een niet-ladebewerking uitvoeren** wanneer u daarom wordt gevraagd.
5. Schuif op de pagina **Welkom** naar rechts en selecteer de optie **Hardwarestation selecteren**.
6. Selecteer **Beheren**, stel de optie **Hardwarestation gebruiken** in op **Aan** en selecteer vervolgens **OK**.
7. Meld u af bij het POS en vervolgens opnieuw aan.
8. Nadat u bent aangemeld, selecteert u **Een nieuwe ploeg openen** en vervolgens **Lade**.

## <a name="complete-a-bopis-scenario"></a>Een BOPIS-scenario voltooien

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Een winkelorder maken voor afhalen in de winkel

1. Ga naar de URL die u hebt opgegeven in de stap [e-Commerce initialiseren](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) tijdens omgevingsconfiguratie.
2. Selecteer een artikel en selecteer **Toevoegen aan winkelwagen**.
3. Selecteer op de pagina met de boodschappentas de optie **Dit ophalen** voor de orderregel die u zojuist hebt toegevoegd.
4. Voer in het dialoogvenster **Een winkel selecteren** **San Francisco** in en selecteer vervolgens de knop **Zoeken**.
5. Zoek in de lijst met resultaten naar de winkel in San Francisco en selecteer **Hier ophalen**.
6. Selecteer op de pagina met de boodschappentas de optie **Uitchecken als gast**. 

    > [!NOTE]
    > Als u wilt doorgaan met uitchecken, moet u de cookiemelding accepteren. Deze melding wordt weergegeven als een banner boven aan de uitcheckpagina.

7. Voer voor de betalingsmethode met creditcard de volgende gegevens in:

    - **Naam kaarthouder:** voer een willekeurige naam in.
    - **Kaartnummer:** voer **4111-1111-1111-1111** in.
    - **Vervaldatum:** voer **10/20** in.
    - **Kaartverificatiewaarde (CVV):** voer **737** in.

    > [!IMPORTANT]
    > Gebruik in geen geval echte creditcardgegevens op de testsite.

8. Ga verder met de afhandeling door de details van het factuuradres in te voeren en selecteer **Opslaan en doorgaan**.
9. Wanneer de order gereed is om te worden geplaatst, selecteert u **Uitchecken**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Online orders synchroniseren naar de backoffice

Zie [Online verkopen en betalingen boeken](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments) voor informatie over het synchroniseren van online orders.

### <a name="pick-up-an-order-in-the-store"></a>Een order ophalen in winkel

1. Meld u aan bij het POS.
2. Selecteer in het scherm **Welkom** de opdracht **Orderafhandeling**
3. Selecteer in de lijst met op te halen artikelen de regel van de order die online is geplaatst.
4. Selecteer de optie **Ophalen** als de orderregel is geselecteerd.

    Het regelartikel wordt toegevoegd aan het transactiescherm en **$ 0,00** wordt weergegeven als het verschuldigde saldo.

5. Selecteer het openstaande saldo van **$ 0,00** of selecteer een betalingsmethode om de transactie te sluiten.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Online orders die worden opgehaald in POS, hebben een openstaand saldo dat niet gelijk is aan nul

Wanneer een order in de winkel wordt opgehaald, moet u ervoor zorgen dat Modern POS wordt gebruikt en dat het hardwarestation actief is, als het te betalen saldo niet 0 (nul) is. Als Cloud POS of Modern POS voor iOS wordt gebruikt, controleert u of het gedeelde hardwarestation actief is. Een bepaalde vorm van actief hardwarestation vereist om betalingen op te halen die online zijn gemaakt.

### <a name="general-issues-with-payment-capture"></a>Algemene problemen met het vastleggen van betalingen

Voor alle algemene problemen moet u de gebeurtenislogboeken voor Modern POS of Internet Information Services-hardwarestation (IIS) altijd als eerste stap raadplegen. U vindt deze logboeken onder de volgende knooppunten in het Windows-gebeurtenislogboek:

- Logboeken voor toepassingen en services \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Logboeken voor toepassingen en services \> Microsoft \> Dynamics \> Commerce-Hardwarestation

## <a name="additional-resources"></a>Aanvullende bronnen

[Omgevingsoverzicht Dynamics 365 Commerce-preview](cpe-overview.md)

[Een previewomgeving voor Dynamics 365 Commerce inrichten](provisioning-guide.md)

[Optionele functies voor een Dynamics 365 Commerce-preview-omgeving configureren](cpe-optional-features.md)

[Veelgestelde vragen over Dynamics 365 Commerce-preview-omgeving](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

[De Adyen-betalingsconnector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Online betaalmiddelen opslaan met de Adyen-connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Overzicht van betalingen voor meerdere kanalen](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)