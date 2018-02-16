---
title: Microsoft Dynamics 365 for Talent inrichten
description: In dit onderwerp wordt u door het proces van het inrichten van een nieuwe omgeving voor Microsoft Dynamics 365 for Talent geleid.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: nl-nl
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent inrichten
In dit onderwerp wordt u door het proces van het inrichten van een nieuwe omgeving voor Microsoft Dynamics 365 for Talent geleid. In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Talent-serviceabonnement al is opgenomen en u de stappen in dit onderwerp niet kunt voltooien, neemt u contact op met de ondersteuning.

Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) en een nieuw Talent-project maken. Tenzij u vanwege een licentieprobleem Talent niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.

## <a name="create-an-lcs-project"></a>Een LCS-project maken
Als u LCS wilt gebruiken om Talent-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Talent.
2. Selecteer het plusteken (**+**) om een project te maken.
3. Selecteer **Microsoft Dynamics 365 for Talent** als de productnaam en -versie.
4. Selecteer de methodologie **Dynamics 365 for Talent**.
5. Selecteer **Maken**.

Zie de methodologie **Talent** die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Talent. Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Talent-omgeving in te richten.

## <a name="provision-a-talent-project"></a>Een Talent-project inrichten
Nadat u een LCS-project hebt gemaakt, kunt u Talent inrichten in een omgeving.

1. Selecteer in uw LCS-project de tegel **Beheer Talent-app**.
2. Talent wordt altijd ingericht in een Microsoft PowerApps-omgeving om de PowerApps-integratie en -uitbreidbaarheid mogelijk te maken. Als u nog geen PowerApps-omgeving hebt, volgt u de stappen in de sectie Een nieuwe PowerApps-omgeving maken (indien vereist) van dit onderwerp voordat u doorgaat.

    > [!NOTE]
    > Om bestaande omgevingen weer te geven of nieuwe omgevingen te maken, moet de tenantbeheerder die Talent inricht, worden toegewezen aan de PowerApps P2-licentie. Als uw organisatie geen PowerApps P2-licentie heeft, kunt u er een krijgen van uw provider van cloudoplossingen of downloaden via de [pagina met PowerApps-prijzen](https://powerapps.microsoft.com/en-us/pricing/).

3. Selecteer **Toevoegen** en selecteer de omgeving waarin Talent moet worden ingericht.
4. Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.

    Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant. U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**. Dit proces duurt meestal een paar minuten. Als de inrichting mislukt, moet u contact opnemen met de ondersteuning.

6. Selecteer **Aanmelden bij Talent** om uw nieuwe omgeving te gebruiken.

> [!NOTE]
> Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Talent in het project implementeren. Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft. Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.

## <a name="create-a-new-powerapps-environment-if-required"></a>Een nieuwe PowerApps-omgeving maken (indien vereist)

De visie achter de integratie van Talent met PowerApps-omgevingen is het inschakelen van gegevensintegratie en uitbreidingensstromen door het gebruik van PowerApps naast Talent-gegevens. Hierdoor is het belangrijk dat u het doel begrijpt van PowerApps-omgevingen bij het kiezen van de omgeving die moet worden gebruikt voor Talent. Zie voor meer informatie over PowerApps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van PowerApps-omgevingen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).  Elke tenant wordt automatisch in een standaard PowerApps-omgeving ingericht, maar dit is mogelijk niet de beste omgeving voor uw implementatie van Talent. Gegevensintegratie en teststrategieën moeten worden beschouwd tijdens deze stap, dus het is raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien het later niet eenvoudig te wijzigen is.

1. Selecteer **Omgevingen beheren** in LCS. Het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/environments) wordt geopend. Hier kunt u bestaande omgevingen weergeven en nieuwe omgevingen maken.
2. Selecteer de knop (**+**) **Nieuwe omgeving**.
3. Geef een unieke naam voor de omgeving op en selecteer de implementatielocatie.

    > [!NOTE]
    > Talent is niet beschikbaar in alle regio's. Daarom moet u controleren of Talent voor u beschikbaar is voordat u de locatie voor uw omgeving selecteert.

4. Wanneer u wordt gevraagd of u een database wilt maken, selecteert u **Database maken** om de CDS-database (Common Data Service) te maken die als host voor een deel van uw Talent-gegevens moet fungeren. Als u een database maakt, kunt u ook PowerApps-toepassingen integreren met Talent.
5. U wordt gevraagd welk toegangsniveau u wilt gebruiken voor de database. Wij raden u aan **Toegang beperken** te selecteren om te voorkomen dat gebruikers van Talent rechtstreeks toegang tot gevoelige gegevens kunnen krijgen via een PowerApps-toepassing.
6. De CDS-database die wordt gemaakt, bevat voorbeeldgegevens. Deze voorbeeldgegevens zijn nuttig omdat u deze kunt gebruiken voor tests of om taakopnamen of taakbegeleidingen te maken. Met de demonstratiegegevens worden echter ook onder andere inactieve werknemers en fictieve adressen toegevoegd aan uw productieomgeving. Als u deze voorbeeldgegevens wilt verwijderen, gaat u als volgt te werk als u klaar bent met het maken van de CDS-database:

    > [!IMPORTANT]
    > Als u eerder een CDS-database hebt gemaakt en hierin productiegegevens van uw bedrijf hebt opgegeven, worden met de volgende stappen **alle** gegevens in de geselecteerde database verwijderd, ook de productiegegevens van uw bedrijf.

    1. Meld u aan bij [PowerApps](https://preview.web.powerapps.com/home) en selecteer de omgeving die u hebt gemaakt in stap 2, in de vervolgkeuzelijst aan de rechterkant van de pagina.
    2. Vouw de **Common Data Service** uit in het linkernavigatievenster en kies **Entiteiten**.
    3. Selecteer rechts op de pagina de ellips (**...**) en selecteer vervolgens **Alle gegevens wissen**.
    4. Selecteer **Gegevens verwijderen** om te bevestigen dat u de gegevens wilt verwijderen. Met deze actie verwijdert u de demonstratiegegevens die standaard in de CDS zijn opgenomen. Daarnaast worden de gegevens verwijderd die zijn ingevoerd in de geselecteerde database.
    
U kunt uw nieuwe omgeving gebruiken.

## <a name="granting-access-to-the-environment"></a>Toegang verlenen tot de omgeving
De globale beheerder die de omgeving heeft gemaakt, heeft standaard toegang, maar aan aanvullende gebruikers van toepassingen moet uitdrukkelijk toegang worden verleend. Dit is mogelijk door [toevoegen van gebruikers](../dev-itpro/sysadmin/tasks/create-new-users.md) en [ze de juiste rollen toe te wijzen](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) binnen de Core HR-omgeving. Verder is het ook noodzakelijk deze gebruikers toe te voegen aan de PowerApps-omgeving, zodat zij toegang hebben tot de Attract- en Onboard-toepassingen.  Het logbericht [Inleiding in het PowerApps-beheercentrum](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) kan u helpen bij het voltooien van deze stappen die hier worden beschreven:

> 1.    De globale beheerder die de Talent-omgeving heeft geïmplementeerd, moet navigeren naar het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/environments).   
> 2.    Selecteer de desbetreffende omgevingen.
> 3.    Voeg onder het tabblad Beveiliging de benodigde gebruikers aan de rol 'Maker omgeving' toe.

Deze laatste stap voor het toevoegen van gebruikers aan de PowerApps-omgeving is tijdelijk. We zullen uiteindelijk functionaliteit toevoegen waarmee dit automatisch wordt ingeschakeld wanneer de gebruiker wordt toegevoegd aan Core HR.


