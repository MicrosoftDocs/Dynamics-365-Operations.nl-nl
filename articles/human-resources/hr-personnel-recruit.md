---
title: Kandidaten werven
description: In dit artikel wordt beschreven hoe u kandidaten werft in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879245"
---
# <a name="recruit-job-candidates"></a>Kandidaten werven


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Met Dynamics 365 Human Resources kunt u wervingsaanvragen te beheren. Ook kunt u met dit programma sollicitanten naadloos omzetten in werknemers. Als uw organisatie gebruikmaakt van een afzonderlijke wervingsapplicatie, kan uw wervingsproces de volgende stappen bevatten:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Uw wervingsaanvraag invoeren in Human Resources.
- Kandidaat-verwijzingen ontvangen in Human Resources vanuit de wervingsapplicatie.
- Het goedkeuringsproces voor kandidaten in voltooien in Human Resources.

Als u geen afzonderlijke wervingsapplicatie gebruikt, kunt u de kandidaten ook handmatig beheren in Human Resources.

> [!NOTE]
> Ga naar [Dataverse-integratie configureren](hr-admin-integration-common-data-service.md) en [Virtuele Dataverse-tabellen configureren](hr-admin-integration-common-data-service-virtual-entities.md) als u een beheerder of ontwikkelaar bent en u Human Resources wilt integreren met een wervingsapplicatie van derden.
>
> U kunt ook apps voor wervingsintegratie vinden op [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Wervingsaanvragen voor de samengevoegde infrastructuur inschakelen

Als u wervingsaanvragen wilt indienen in HR-werving, moet u eerst de functies **HR-gebruikerservaring** en **Wervingsproces beheren** inschakelen.

Zodra de functies zijn ingeschakeld, selecteert u de functionaliteit met de volgende stappen: 
1. Ga naar **Human resources** > **Instellingen** > **Human resources-parameters**.
2. Stel op het tabblad  **Werving**  het veld **Werving ingeschakeld** in op **Ja**.
3. Selecteer **HR-werving** in de vervolgkeuzelijst **Wervingservaring**.  
4. Klik op **Opslaan**. 

> [!Note] 
> Als **HR-werving** is geselecteerd, is **Wervingsprojecten** (verouderd) niet beschikbaar. 


## <a name="add-a-recruiting-request-location"></a>De locatie van een wervingsaanvraag toevoegen

Als uw organisatie meerdere locaties heeft, kunt u deze toevoegen zodat aanvragers een locatie kunnen selecteren waar de nieuwe werving actief is. De locatie wordt opgenomen in de vacaturebeschrijving.

1. Voer in de zoekbalk **Locatie voor wervingsaanvraag** in.
2. Selecteer **Nieuw**.
3. Voer in het veld **Locatie voor wervingsaanvraag** de locatienaam in.

    ![De locatie van een wervingsaanvraag toevoegen.](./media/hr-recruit-0a-add-location.png)

4. Voer bij **Omschrijving** een omschrijving voor de locatie in.
5. Selecteer **Locatie** onder **Producten**. Als het dialoogvenster **Nieuw adres** verschijnt, voert u het adres voor de locatie in.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Adres invoeren.](./media/hr-recruit-0b-address.png)

6. Voer onder **Contactgegevens** de gegevens in voor de contactpersoon van de locatie.
7. Selecteer **Opslaan**.

## <a name="add-a-recruiting-request"></a>Een wervingsaanvraag toevoegen

Managers kunnen wervingsverzoeken indienen in Human Resources. Als u een afzonderlijke wervingsapplicatie gebruikt, zal het uitvoeren van deze stappen een wervingsaanvraag verzenden en het wervingsproces starten in die applicatie. Voer anders deze procedure uit om de workflow te starten voor uw eigen interne wervingsproces.

1. Selecteer **Werknemerselfservice**.
2. Selecteer het tabblad **Mijn team**.
3. Selecteer **Wervingsaanvraag**.

    ![Een wervingsaanvraag starten.](./media/hr-recruit-1-request-to-recruit.png)

4. Vul de velden **Omschrijving**, **Vacature** en **Geschatte begindatum** in.

    ![De wervingsaanvraag voltooien.](./media/hr-recruit-2-request-to-recruit.png)

5. Selecteer **Continue**. De wervingsaanvraag voor uw functie wordt weergegeven.
6. Selecteer onder **Algemeen** een werver in de vervolgkeuzelijst **Werver** en selecteer een locatie in de vervolgkeuzelijst **Locatie voor wervingsaanvraag**.
7. Wijzig onder **Vacature** de benodigde informatie en selecteer **Details uit vacature aanmaken**.

    ![Details van taak maken.](./media/hr-recruit-3-create-details-from-job.png)

    De rest van het wervingsverzoek wordt gevuld met de standaardinformatie over de vacature die u hebt ingevoerd.

8. Voer onder **Externe omschrijving** een externe vacatureomschrijving in.
9. Selecteer onder **Functies** de optie **Toevoegen** en selecteer vervolgens een functie voor deze wervingsaanvraag.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Een functie toevoegen.](./media/hr-recruit-4-select-position.png)

10. Selecteer onder **Vaardigheden** **Toevoegen** en selecteer vervolgens een vaardigheid.
11. Selecteer onder **Opleidingseisen** **Toevoegen** en vervolgens waarden uit de vervolgkeuzelijsten **Opleiding** en **Opleidingsniveau**.

    ![Opleidingseisen toevoegen.](./media/hr-recruit-5-select-educational-requirements.png)

12. Voeg onder **Opmerkingen** opmerkingen toe indien nodig.
13. Selecteer onder **Compensatie** een niveau in de vervolgkeuzelijst **Niveau** en wijzig vervolgens **Lage drempelwaarde**, **Controlepunt** en **Hoge drempelwaarde** indien nodig.
14. Wanneer uw wervingsaanvraag is voltooid en u klaar bent om het wervingsproces te starten, selecteert u **Activeren** in de menubalk.

    ![Wervingsaanvraag activeren.](./media/hr-recruit-6-activate-recruit-request.png)

15. Selecteer **Opslaan**.

## <a name="view-and-edit-your-recruiting-requests"></a>Uw wervingsaanvragen weergeven en bewerken

Als u manager bent en u uw eigen aanvragen wilt bekijken, gaat u als volgt te werk:

1. Selecteer **Werknemerselfservice**.
2. Selecteer het tabblad **Mijn team**.
3. Selecteer onder **Mijn teamgegevens** het tabblad **Wervingsaanvragen**.

    ![Selecteer het tabblad Wervingsaanvragen.](./media/hr-recruit-7-recruiting-requests.png)

4. Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.

Als u een HR-professional bent en alle wervingsaanvragen wilt bekijken, gaat u als volgt te werk:

1. Selecteer **Personeelsbeheer**.
2. Selecteer **Wervingsaanvragen**.

    ![Wervingsaanvragen weergeven in Personeelsbeheer.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Als u een wervingsaanvraag wilt weergeven of bewerken, selecteert u deze in het raster.

## <a name="add-or-edit-a-candidate-profile"></a>Een kandidaatprofiel toevoegen of bewerken

Als uw organisatie is geïntegreerd met een andere toepassing om wervingsaanvragen te beheren, worden deze doorgestuurd naar die toepassing. De wervingstoepassing stuurt vervolgens informatie over kandidaten terug naar Human Resources. Anders kunt u uw eigen interne wervingsprocessen volgen en handmatig kandidaatgegevens invoeren.

1. Selecteer **Personeelsbeheer**.
2. Selecteer **Koppelingen**.
3. Selecteer onder **Werving** **Kandidaten**.

    ![Bekijk de kandidaten.](./media/hr-recruit-9-candidates.png)

4. Selecteer **Nieuw** om een kandidaat toe te voegen. Om een bestaande kandidaat te bewerken, selecteert u de kandidaat uit de lijst en vervolgens **Bewerken**. Het kandidaatprofiel wordt weergegeven.
5. Voer onder **Kandidaatoverzicht** de kandidaatgegevens van de kandidaat in of bewerk deze indien nodig.
6. Selecteer onder **Wervingsaanvraag** een wervingsaanvraag om de kandidaat aan te koppelen. Vul vervolgens de velden **Geschatte begindatum**, **Aanstellend manager**, **Functie**  en **Omschrijving** in.

    ![Een wervingsaanvraag koppelen.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Vul alle gegevens in de volgende gebieden in die u wilt opnemen in het dossier van de kandidaat:

    - **Opmerkingen**
    - **Beroepservaring**
    - **Gegevens contactpersoon**
    - **Onderwijs**
    - **Vaardigheden**
    - **Getuigschriften**
    - **Screenings**

8. Selecteer **Opslaan**.

## <a name="hire-a-candidate"></a>Een kandidaat aannemen

Wanneer u klaar bent om een kandidaat aan te nemen, volgt u deze procedure om de kandidaat om te zetten in een werknemer.

1. Selecteer op de pagina **Kandidaat** de optie **Aannemen**.

    ![Een kandidaat aannemen.](./media/hr-recruit-11-hire.png)

2. Vul op de pagina **Nieuwe werknemer aannemen** onder **Gegevens** alle velden in.

    ![Gegevens nieuwe werknemer invoeren.](./media/hr-recruit-12-hire-new-worker.png)

3. Controleer en wijzig onder **Functiegegevens** zo nodig de gegevens.
4. Selecteer onder **Controlelijsten voor onboarding** de relevante controlelijsten voor deze werknemer.
5. Selecteer **Doorgaan** om het werknemersdossier te maken.

    > [!NOTE]
    > Afhankelijk van de workflows van uw organisatie kan het kandidaatdossier aanvullende goedkeuringsstappen nodig hebben voordat deze wordt omgezet in een werknemersdossier.

## <a name="decide-not-to-hire-a-candidate"></a>Besluiten om een kandidaat niet aan te nemen

Als u besluit een kandidaat niet aan te nemen, volgt u deze procedure om ze te verwijderen uit het wervingsproces. 

1. Selecteer op de pagina **Kandidaat** de optie **Niet aannemen**.

    ![Een kandidaat niet aannemen.](./media/hr-recruit-13-do-not-hire.png)

2. Selecteer een **Redencode** en voeg eventuele opmerkingen toe.
3. Selecteer **OK**.

## <a name="dismiss-a-candidate"></a>Een kandidaat ontslaan

U kunt een kandidaat zo nodig ontslaan nadat u deze hebt aangenomen. Een kandidaat kan bijvoorbeeld uw aanbod afwijzen of op de eerste dag niet komen opdagen.

- Selecteer op de pagina **Kandidaat** de optie **Kandidaat negeren**.

    ![Kandidaat negeren.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Zie ook

[Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Uw personeel organiseren](hr-personnel-departments-jobs-positions.md)<br>
[De onderdelen van een taak instellen](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
