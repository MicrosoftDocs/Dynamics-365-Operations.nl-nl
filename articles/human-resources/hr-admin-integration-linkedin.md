---
title: Integreren met LinkedIn Talent Hub
description: In dit artikel wordt uitgelegd hoe u integratie instelt tussen Microsoft Dynamics 365 Human Resources en LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df4a0a4dec078392ba835318450f5983a6e95c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887742"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integreren met LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> De in dit artikel beschreven integratie tussen Dynamics 365 Human Resources en LinkedIn Talent Hub is op 31 december 2021 beëindigd. De integratieservice zal na deze datum niet meer beschikbaar zijn. Organisaties die de integratieservice nog niet gebruiken, kunnen de service niet implementeren voordat deze wordt beëindigd.

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is een ATS-platform (Applicant Tracking System). Hier zijn sourcing, beheer en aanstelling van werknemers op één plaats mogelijk. Door Microsoft Dynamics 365 Human Resources te integreren met LinkedIn Talent Hub kunt u eenvoudig werknemersrecords in Human Resources maken voor sollicitanten die voor een functie zijn aangesteld.

## <a name="setup"></a>Instelling

Een systeembeheerder moet installatietaken voltooien om integratie met LinkedIn Talent Hub mogelijk te maken. Eerst moet u in de Power Apps-omgeving een gebruiker en beveiligingsrol instellen om LinkedIn Talent Hub de juiste machtigingen te geven om gegevens naar Human Resources te schrijven.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Uw omgeving koppelen aan LinkedIn Talent Hub

1. Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Selecteer **Productinstellingen** in het vervolgkeuzemenu voor gebruikers.

3. Selecteer in het linkernavigatievenster in de sectie **Geavanceerd** de optie **Integraties**.

4. Selecteer **Autoriseren** voor de integratie met Microsoft Dynamics 365 Human Resources.

5. Selecteer op de pagina **Dynamics 365 Human Resources** de omgeving waaraan u LinkedIn Talent Hub wilt koppelen en selecteer vervolgens **Koppelen**.

    ![LinkedIn Talent Hub-onboarding.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > U kunt alleen koppelingen maken naar omgevingen waarin uw gebruikersaccount beheerderstoegang heeft tot zowel de Human Resources-omgeving als de bijbehorende Power Apps-omgeving. Als er geen omgevingen worden weergegeven op de koppelingspagina Human Resources, controleert u of u een gelicentieerde Human Resources-omgeving hebt op de tenant en of de gebruiker die u op de koppelingspagina hebt aangemeld, beheerdersrechten heeft voor zowel de Human Resources-omgeving als de Power Apps-omgeving.

### <a name="create-a-power-apps-security-role"></a>Een Power Apps-beveiligingsrol maken

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de omgeving die is gekoppeld aan de Human Resources-omgeving waaraan u uw exemplaar van LinkedIn Talent Hub wilt koppelen.

3. Selecteer **Instellingen**.

4. Vouw het knooppunt **Gebruikers en machtigingen** uit en selecteer **Beveiligingsrollen**.

5. Selecteer op de pagina **Beveiligingsrollen** op de werkbalk de optie **Nieuwe rol**.

6. Voer op het tabblad **Details** een naam in voor de rol, zoals **HRIS-integratie met LinkedIn Talent Hub.**

7. Selecteer op het tabblad **Aanpassing** de machtiging **Lezen** op organisatieniveau voor de volgende entiteiten:

    - Entiteit
    - Veld
    - Relatie

8. Sla de beveiligingsrol op en sluit deze.

### <a name="create-a-power-apps-application-user"></a>Een Power Apps-toepassingsgebruiker maken

Er moet een toepassingsgebruiker worden gemaakt voor de LinkedIn Talent Hub-adapter om machtigingen te verlenen aan de adapter om kandidaatrecords naar de Power Apps-omgeving te schrijven.

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com).

2. Selecteer in de lijst **Omgevingen** de omgeving die is gekoppeld aan de Human Resources-omgeving waaraan u uw exemplaar van LinkedIn Talent Hub wilt koppelen.

3. Selecteer **Instellingen**.

4. Vouw het knooppunt **Gebruikers en machtigingen** uit en selecteer **Gebruikers**.

5. Selecteer **Gebruikers beheren in Dynamics 365**.

6. Gebruik het vervolgkeuzemenu boven de lijst om de weergave te wijzigen van de standaardweergave **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.

    ![Weergave van toepassingsgebruikers.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Selecteer **Nieuw** op de werkbalk.

8. Voer op de pagina **Nieuwe gebruiker** de volgende stappen uit:

    1. Wijzig de waarde van het veld **Gebruikerstype** in **Toepassingsgebruiker**.
    2. Stel het veld **Gebruikersnaam** in op **HRIS-integratie met Dynamics365 HR LinkedIn**.
    3. Stel het veld **Toepassings-ID** in op **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Voer een waarde in de velden **Voornaam**, **Achternaam** en **Primaire e-mail** in.
    5. Selecteer **Opslaan \& sluiten** op de werkbalk.

### <a name="assign-a-security-role-to-the-new-user"></a>Een beveiligingsrol toewijzen aan de nieuwe gebruiker

Nadat u de nieuwe toepassingsgebruiker in de vorige sectie hebt opgeslagen en gesloten, komt u terug op de pagina **Gebruikerslijst**.

1. Wijzig op de pagina **Gebruikerslijst** de weergave in **Toepassingsgebruikers**.

2. Selecteer de toepassingsgebruiker die u hebt gemaakt in de vorige sectie.

3. Selecteer **Rollen beheren** op de werkbalk.

4. Selecteer de beveiligingsrol die u eerder hebt gemaakt voor de integratie.

5. Selecteer **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Een Azure Active Directory-app in Human Resources toevoegen

1. Open in Dynamics 365 Human Resources de pagina **Azure Active Directory-toepassingen**.
2. Voeg een nieuwe record toe aan de lijst en stel de volgende velden in:

    - **Client-ID**: voer **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** in.
    - **Naam**: voer de naam in van de Power Apps-beveiligingsrol die u eerder hebt gemaakt, zoals **HRIS-integratie met LinkedIn Talent Hub**.
    - **Gebruikers-ID**: selecteer een gebruiker met machtigingen voor het schrijven van gegevens in Personeelsbeheer.

### <a name="create-the-table-in-dataverse"></a>De tabel maken in Dataverse

> [!IMPORTANT]
> De integratie met de LinkedIn Talent Hub is afhankelijk van virtuele tabellen in Dataverse voor Human Resources. Als een voorwaarde voor deze stap in de instellingen moet u virtuele tabellen configureren. Zie [Virtuele tabellen in Dataverse configureren](./hr-admin-integration-common-data-service-virtual-entities.md) voor informatie over het configureren van virtuele tabellen.

1. Open in Human Resources de pagina **Integratie met Dataverse**.

2. Selecteer het tabblad **Virtuele tabellen**.

3. Filter de lijst met entiteiten op entiteitslabel om te zoeken naar **Geëxporteerde kandidaten voor LinkedIn**.

4. Selecteer de entiteit en selecteer vervolgens **Genereren/vernieuwen**.

## <a name="exporting-candidate-records"></a>Kandidaatrecords exporteren

Nadat de instellingen zijn voltooid, kunnen wervers en HR-professionals gebruikmaken van de functie **Exporteren naar HRIS** in LinkedIn Talent Hub om records van aangestelde kandidaten te exporteren vanuit LinkedIn Talent Hub naar Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Records exporteren vanuit LinkedIn Talent Hub

Nadat een kandidaat is verplaatst via het wervingsproces en is aangesteld, kunt u de kandidaatrecord exporteren vanuit LinkedIn Talent Hub naar Human Resources.

1. Open in LinkedIn Talent Hub het project waarvoor u de nieuwe werknemer hebt aangesteld.

2. Selecteer een kandidaatrecord.

3. Selecteer **Fase wijzigen** en selecteer vervolgens **Aangesteld**.

4. Selecteer in het menu met het weglatingsteken (**...**) voor de kandidaat de optie **Exporteren naar HRIS**.

5. Voer in het deelvenster **Exporteren naar HRIS** de gegevens in die moeten worden geëxporteerd:

    - Selecteer **Microsoft Dynamics 365 Human Resources** in het veld **HRIS-provider**.
    - Selecteer een waarde voor de nieuwe werknemer in het veld **Begindatum**.
    - Voer in het veld **Functie** een functie in voor de functie van de nieuwe werknemer.
    - Voer in het veld **Locatie** de locatie in waar de werknemer wordt geplaatst.
    - Voer het e-mailadres van de werknemer in of verifieer het.

![Deelvenster Exporteren naar HRIS in LinkedIn Talent Hub.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Onboarding in Human Resources voltooien

Kandidaatrecords die worden geëxporteerd vanuit LinkedIn Talent Hub naar Human Resources, worden weergegeven in de sectie **Aan te stellen kandidaten** op de pagina **Personeelsbeheer**.

1. Open in Human Resources de pagina **Personeelsbeheer**.

2. Selecteer in de sectie **Aan te stellen kandidaten** **Aanstellen** voor de geselecteerde kandidaat.

3. Bekijk de record in het dialoogvenster **Nieuwe werknemer aanstellen** en voeg alle vereiste gegevens toe. U kunt ook het positienummer selecteren waarvoor de kandidaat is aangesteld.

Nadat u de vereiste informatie hebt ingevoerd, kunt u doorgaan met uw standaardprocessen voor het maken van werknemersrecords en de onboarding van werknemers.

De volgende details worden geïmporteerd en opgenomen in de nieuwe werknemersrecord:

- Voornaam
- Achternaam
- Begindatum dienstverband
- E-mailadres
- Telefoonnummer

## <a name="see-also"></a>Zie ook

[Virtuele Dataverse-entiteiten configureren](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
