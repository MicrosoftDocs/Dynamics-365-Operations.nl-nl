---
title: BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving
description: In dit onderwerp wordt uitgelegd hoe u online kopen, ophalen in winkel (BOPIS) kunt configureren, in een Microsoft Dynamics 365 Commerce-evaluatieomgeving nadat deze is ingericht.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ec1c556a70ed92a40d3cb2bf45fb6156b7dbf7fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993470"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="1e7f1-103">BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving</span><span class="sxs-lookup"><span data-stu-id="1e7f1-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e7f1-104">In dit onderwerp wordt uitgelegd hoe u online kopen, ophalen in winkel (BOPIS) kunt configureren, in een Microsoft Dynamics 365 Commerce-evaluatieomgeving nadat deze is ingericht.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="1e7f1-105">Vereiste</span><span class="sxs-lookup"><span data-stu-id="1e7f1-105">Prerequisite</span></span>

<span data-ttu-id="1e7f1-106">Voltooi de procedures in dit onderwerp pas nadat uw evaluatieomgeving van Commerce is ingericht en geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="1e7f1-107">Zie [Een omgevingomgeving van Dynamics 365 Commerce inrichten](provisioning-guide.md) en [Een evaluatieomgeving van Dynamics 365 Commerce configureren](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning) voor meer informatie over het inrichten en configureren van uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="1e7f1-108">Nadat uw Commerce-omgeving is ingericht en volledig is geconfigureerd, kunt u dit onderwerp gebruiken om BOPIS-scenario's in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="1e7f1-109">Het POS configureren</span><span class="sxs-lookup"><span data-stu-id="1e7f1-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="1e7f1-110">Modern POS configureren</span><span class="sxs-lookup"><span data-stu-id="1e7f1-110">Configure Modern POS</span></span>

<span data-ttu-id="1e7f1-111">BOPIS-scenario's waarbij een creditcardbetaling nodig is, vereisen een hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="1e7f1-112">Het hardwarestation is ingebouwd in de Modern POS-programma's voor Windows en Android-clients.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="1e7f1-113">Als u met Cloud POS of Modern POS voor iOS werkt, moet de POS-client zijn gekoppeld aan een gedeeld hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="1e7f1-114">In dit onderwerp wordt uitgelegd hoe u BOPIS configureert voor Windows en Android-clients.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="1e7f1-115">Zie voor meer informatie over het instellen van een gedeeld hardwarestation het onderwerp [Retail Hardware Station configureren en installeren](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="1e7f1-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="1e7f1-116">Ga naar **Detailhandel en Commerce \> Kanaalinstellingen \> POS-instellingen \> Kassa's**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="1e7f1-117">Selecteer **SANFRAN-5** registreren en vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="1e7f1-118">Wijzig de waarde van het veld **Hardwareprofiel** van **HW002** in **HW001** en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="1e7f1-119">Als u de wijzigingen wilt synchroniseren, gaat u naar **Detailhandel en commerce \> IT detailhandel en Commerce \> Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="1e7f1-120">Selecteer de distributieplanning **1090** en selecteer vervolgens **Nu uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="1e7f1-121">Selecteer **Ja** en klik vervolgens op **OK** om de gegevenssynchronisatie te starten.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="1e7f1-122">Modern POS installeren</span><span class="sxs-lookup"><span data-stu-id="1e7f1-122">Install Modern POS</span></span>

1. <span data-ttu-id="1e7f1-123">Ga naar **Detailhandel en Commerce \> Kanaalinstellingen \> POS-instellingen \> Apparaten**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="1e7f1-124">Selecteer apparaat **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="1e7f1-125">Selecteer in het actievenster de optie **Download** en selecteer vervolgens **Configuratiebestand**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="1e7f1-126">Selecteer **Download** en vervolgens **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="1e7f1-127">Selecteer **Bestand openen** wanneer het bestand **ModernPOSSetup.exe** is gedownload.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Bestand openen](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="1e7f1-129">Klik op **Volgende** om door te gaan met het installatieproces.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="1e7f1-130">Selecteer **Sluiten** wanneer de installatie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="1e7f1-131">Modern POS activeren</span><span class="sxs-lookup"><span data-stu-id="1e7f1-131">Activate Modern POS</span></span>

1. <span data-ttu-id="1e7f1-132">Klik op het bureaublad van Windows op de knop **Start** en typ **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="1e7f1-133">Selecteer de **Retail Modern POS**-toepassing om activering te starten.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="1e7f1-134">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-134">Select **Next**.</span></span> <span data-ttu-id="1e7f1-135">De velden **Server-URL**, **Apparaat-id** en **Registernummer** moeten vooraf worden ingesteld met informatie uit het configuratiebestand dat u in de vorige procedure hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="1e7f1-136">Selecteer **Activeren**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-136">Select **Activate**.</span></span>
5. <span data-ttu-id="1e7f1-137">Het verificatiedialoogvenster wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-137">An authentication dialog box appears.</span></span> <span data-ttu-id="1e7f1-138">Selecteer de rekening die gebruikmaakt van het e-mailadres dat eerder is gekoppeld aan werknemer **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e7f1-139">Als u nog geen werknemer hebt gekoppeld aan uw identiteit, wordt de activering niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="1e7f1-140">Volg in dat geval de stappen onder de sectie "Een medewerker aan uw identiteit koppelen" in het onderwerp [Een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="1e7f1-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="1e7f1-141">Selecteer **Alleen deze app** bij de vraag en laat uw organisatie het apparaat beheren.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="1e7f1-142">Wanneer de activering is voltooid, selecteert u **Aan de slag**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="1e7f1-143">BOPIS inschakelen in Modern POS</span><span class="sxs-lookup"><span data-stu-id="1e7f1-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="1e7f1-144">Meld u aan bij Modern POS door **000713** te gebruiken als operator-id en **123** als wachtwoord.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="1e7f1-145">Terwijl de introductievideo wordt afgespeeld, schakelt u de twee selectievakjes in de linkerbenedenhoek van het dialoogvenster in en sluit u het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="1e7f1-146">Als u niet wordt gevraagd de ploeg af te sluiten, schuift u naar rechts op de pagina **Welkom**, selecteert u **Ploeg sluiten** en meldt u zich vervolgens weer aan bij het POS.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="1e7f1-147">Wanneer u bent aangemeld, selecteert u **Een niet-ladebewerking uitvoeren** wanneer u daarom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="1e7f1-148">Schuif op de pagina **Welkom** naar rechts en selecteer de optie **Hardwarestation selecteren**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="1e7f1-149">Selecteer **Beheren**, stel de optie **Hardwarestation gebruiken** in op **Aan** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="1e7f1-150">Meld u af bij het POS en vervolgens opnieuw aan.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="1e7f1-151">Nadat u bent aangemeld, selecteert u **Een nieuwe ploeg openen** en vervolgens **Lade**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="1e7f1-152">Een BOPIS-scenario voltooien</span><span class="sxs-lookup"><span data-stu-id="1e7f1-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="1e7f1-153">Een winkelorder maken voor afhalen in de winkel</span><span class="sxs-lookup"><span data-stu-id="1e7f1-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="1e7f1-154">Ga naar de URL die u hebt opgegeven in de stap [e-Commerce initialiseren](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) tijdens omgevingsconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="1e7f1-155">Selecteer een artikel en selecteer **Toevoegen aan winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="1e7f1-156">Selecteer op de pagina met de boodschappentas de optie **Dit ophalen** voor de orderregel die u zojuist hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="1e7f1-157">Voer in het dialoogvenster **Een winkel selecteren** **San Francisco** in en selecteer vervolgens de knop **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="1e7f1-158">Zoek in de lijst met resultaten naar de winkel in San Francisco en selecteer **Hier ophalen**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="1e7f1-159">Selecteer op de pagina met de boodschappentas de optie **Uitchecken als gast**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1e7f1-160">Als u wilt doorgaan met uitchecken, moet u de cookiemelding accepteren.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="1e7f1-161">Deze melding wordt weergegeven als een banner boven aan de uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="1e7f1-162">Voer voor de betalingsmethode met creditcard de volgende gegevens in:</span><span class="sxs-lookup"><span data-stu-id="1e7f1-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="1e7f1-163">**Naam kaarthouder:** voer een willekeurige naam in.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="1e7f1-164">**Kaartnummer:** voer **4111-1111-1111-1111** in.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="1e7f1-165">**Vervaldatum:** voer **10/20** in.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="1e7f1-166">**Kaartverificatiewaarde (CVV):** voer **737** in.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1e7f1-167">Gebruik in geen geval echte creditcardgegevens op de testsite.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="1e7f1-168">Ga verder met de afhandeling door de details van het factuuradres in te voeren en selecteer **Opslaan en doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="1e7f1-169">Wanneer de order gereed is om te worden geplaatst, selecteert u **Uitchecken**.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="1e7f1-170">Online orders synchroniseren naar de backoffice</span><span class="sxs-lookup"><span data-stu-id="1e7f1-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="1e7f1-171">Zie [Online verkopen en betalingen boeken](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments) voor informatie over het synchroniseren van online orders.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="1e7f1-172">Een order ophalen in winkel</span><span class="sxs-lookup"><span data-stu-id="1e7f1-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="1e7f1-173">Meld u aan bij het POS.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="1e7f1-174">Selecteer in het scherm **Welkom** de opdracht **Orderafhandeling**</span><span class="sxs-lookup"><span data-stu-id="1e7f1-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="1e7f1-175">Selecteer in de lijst met op te halen artikelen de regel van de order die online is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="1e7f1-176">Selecteer de optie **Ophalen** als de orderregel is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="1e7f1-177">Het regelartikel wordt toegevoegd aan het transactiescherm en **$ 0,00** wordt weergegeven als het verschuldigde saldo.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="1e7f1-178">Selecteer het openstaande saldo van **$ 0,00** of selecteer een betalingsmethode om de transactie te sluiten.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e7f1-179">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="1e7f1-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="1e7f1-180">Online orders die worden opgehaald in POS, hebben een openstaand saldo dat niet gelijk is aan nul</span><span class="sxs-lookup"><span data-stu-id="1e7f1-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="1e7f1-181">Wanneer een order in de winkel wordt opgehaald, moet u ervoor zorgen dat Modern POS wordt gebruikt en dat het hardwarestation actief is, als het te betalen saldo niet 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="1e7f1-182">Als Cloud POS of Modern POS voor iOS wordt gebruikt, controleert u of het gedeelde hardwarestation actief is.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="1e7f1-183">Een bepaalde vorm van actief hardwarestation vereist om betalingen op te halen die online zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="1e7f1-184">Algemene problemen met het vastleggen van betalingen</span><span class="sxs-lookup"><span data-stu-id="1e7f1-184">General issues with payment capture</span></span>

<span data-ttu-id="1e7f1-185">Voor alle algemene problemen moet u de gebeurtenislogboeken voor Modern POS of Internet Information Services-hardwarestation (IIS) altijd als eerste stap raadplegen.</span><span class="sxs-lookup"><span data-stu-id="1e7f1-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="1e7f1-186">U vindt deze logboeken onder de volgende knooppunten in het Windows-gebeurtenislogboek:</span><span class="sxs-lookup"><span data-stu-id="1e7f1-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="1e7f1-187">Logboeken voor toepassingen en services \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="1e7f1-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="1e7f1-188">Logboeken voor toepassingen en services \> Microsoft \> Dynamics \> Commerce-Hardwarestation</span><span class="sxs-lookup"><span data-stu-id="1e7f1-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e7f1-189">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1e7f1-189">Additional resources</span></span>

[<span data-ttu-id="1e7f1-190">Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1e7f1-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="1e7f1-191">Een evaluatieomgeving voor Dynamics 365 Commerce inrichten</span><span class="sxs-lookup"><span data-stu-id="1e7f1-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="1e7f1-192">Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren</span><span class="sxs-lookup"><span data-stu-id="1e7f1-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="1e7f1-193">Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1e7f1-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="1e7f1-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="1e7f1-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="1e7f1-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="1e7f1-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="1e7f1-196">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="1e7f1-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="1e7f1-197">Dynamics 365 Commerce-website</span><span class="sxs-lookup"><span data-stu-id="1e7f1-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="1e7f1-198">De Adyen-betalingsconnector</span><span class="sxs-lookup"><span data-stu-id="1e7f1-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="1e7f1-199">Online betaalmiddelen opslaan met de Adyen-connector</span><span class="sxs-lookup"><span data-stu-id="1e7f1-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="1e7f1-200">Overzicht van betalingen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="1e7f1-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
