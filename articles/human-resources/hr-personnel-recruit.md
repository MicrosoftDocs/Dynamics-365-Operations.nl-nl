---
title: Kandidaten werven
description: In dit onderwerp wordt beschreven hoe u kandidaten werft in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6437e6a90574ccbb1d166c4dc75328bb93a3ff4d072faacc5bd69f42870991b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750215"
---
# <a name="recruit-job-candidates"></a>Kandidaten werven

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Met Dynamics 365 Human Resources kunt u wervingsaanvragen te beheren. Ook kunt u met dit programma sollicitanten naadloos omzetten in werknemers. Als uw organisatie gebruikmaakt van een afzonderlijke wervingsapplicatie, kan uw wervingsproces de volgende stappen bevatten:

- Uw wervingsaanvraag invoeren in Human Resources.
- Kandidaat-verwijzingen ontvangen in Human Resources vanuit de wervingsapplicatie.
- Het goedkeuringsproces voor kandidaten in voltooien in Human Resources.

Als u geen afzonderlijke wervingsapplicatie gebruikt, kunt u de kandidaten ook handmatig beheren in Human Resources.

>[!NOTE]
>Zie [Dataverse-integratie configureren](hr-admin-integration-common-data-service.md) en [Virtuele Dataverse-tabellen configureren](hr-admin-integration-common-data-service-virtual-entities.md) als u een beheerder of ontwikkelaar bent en u Human Resources wilt integreren met een wervingsapplicatie van derden.
>
> U kunt ook apps voor wervingsintegratie vinden op [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Zie [Integratie met LinkedIn Talent Hub](hr-admin-integration-linkedin.md) voor informatie over het gebruik van de preview-functie voor integratie met LinkedIn Talent Hub.

## <a name="enable-recruiting-requests"></a>Wervingsaanvragen inschakelen

Als u wervingsaanvragen in Human Resources wilt verzenden, moet u eerst de functionaliteit **Gedeelde Human Resources-parameters** inschakelen.

1. In de werkruimte **Personeelsbeheer** selecteert u **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Gedeelde Human Resources-parameters**.

3. Op het tabblad **Werving** onder **WERVING**, stelt u **Wervingsaanvragen inschakelen** in op **Ja**.

## <a name="add-a-recruiting-request-location"></a>De locatie van een wervingsaanvraag toevoegen

Als uw organisatie meerdere locaties heeft, kunt u deze toevoegen zodat aanvragers een locatie kunnen selecteren waar de nieuwe werving actief is. De locatie wordt opgenomen in de vacaturebeschrijving.

1. Voer in de zoekbalk **Locatie voor wervingsaanvraag** in.

2. Selecteer **Nieuw**.

3. Voer in het veld **Locatie voor wervingsaanvraag** de locatienaam in.

   ![De locatie van een wervingsaanvraag toevoegen.](./media/hr-recruit-0a-add-location.png)

4. Voer in het veld **Omschrijving** een omschrijving voor de locatie in.

5. Selecteer **Locatie** onder **Producten**. Als het venster **Nieuw adres** verschijnt, voert u het adres voor de locatie in.

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

6. Selecteer onder **Algemeen** een werver uit de keuzelijst **Werver** en selecteer een locatie in de **Locatie voor wervingsaanvraag**.

7. Wijzig onder **Vacature** de benodigde informatie en selecteer **Details uit vacature aanmaken**.

   ![Details van taak maken.](./media/hr-recruit-3-create-details-from-job.png)

   De rest van het wervingsverzoek wordt gevuld met de standaardinformatie over de vacature die u hebt ingevoerd.

8. Voer onder **Externe omschrijving** een externe vacatureomschrijving in.

9. Selecteer onder **Functies** de optie **Toevoegen** en selecteer vervolgens een functie voor deze wervingsaanvraag.

   ![Een functie toevoegen.](./media/hr-recruit-4-select-position.png)

10. Selecteer onder **Vaardigheden** **Toevoegen** en selecteer vervolgens een vaardigheid.

11. Selecteer onder **Opleidingseisen** **Toevoegen** en vervolgens waarden uit de vervolgkeuzelijsten **Opleiding** en **Opleidingsniveau**.

   ![Opleidingseisen toevoegen.](./media/hr-recruit-5-select-educational-requirements.png)

12. Voeg onder **Opmerkingen** opmerkingen toe indien nodig.

13. Selecteer onder **Compensatie** een niveau in de vervolgkeuzelijst **Niveau** en wijzig vervolgens de **Lage drempelwaarde**, het **Controlepunt** en **Hoge drempelwaarde** indien nodig.

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

6. Selecteer onder **Wervingsaanvraag** een wervingsaanvraag om de kandidaat aan te koppelen. Vul vervolgens de **Geschatte begindatum**, **Aanstellend manager**, **Functie**  en **Omschrijving** in.

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

1. Selecteer op het kandidaatformulier de optie **Aannemen**.

   ![Een kandidaat aannemen.](./media/hr-recruit-11-hire.png)

2. Vul in het formulier **Nieuwe werknemers aannemen** onder **Gegevens** alle velden in.

   ![Gegevens nieuwe werknemer invoeren.](./media/hr-recruit-12-hire-new-worker.png)

3. Controleer en wijzig onder **Functiegegevens** zo nodig de gegevens.

4. Selecteer onder **Controlelijsten voor onboarding** de relevante controlelijsten voor deze werknemer.

5. Selecteer **Doorgaan** om het werknemersdossier te maken.

   >[!NOTE]
   >Afhankelijk van de workflows van uw organisatie kan het kandidaatdossier aanvullende goedkeuringsstappen nodig hebben voordat deze wordt omgezet in een werknemersdossier.

## <a name="decide-not-to-hire-a-candidate"></a>Besluiten om een kandidaat niet aan te nemen

Als u besluit een kandidaat niet aan te nemen, volgt u deze procedure om ze te verwijderen uit het wervingsproces. 

1. Selecteer op het kandidaatformulier de optie **Niet aannemen**.

   ![Een kandidaat niet aannemen.](./media/hr-recruit-13-do-not-hire.png)

2. Selecteer een **Redencode** en voeg eventuele opmerkingen toe.

3. Selecteer **OK**.

## <a name="dismiss-a-candidate"></a>Een kandidaat ontslaan

U kunt een kandidaat zo nodig ontslaan nadat u deze hebt aangenomen. Een kandidaat kan bijvoorbeeld uw aanbod afwijzen of op de eerste dag niet komen opdagen.

- Selecteer op het kandidaatformulier de optie **Kandidaat ontslaan**.

  ![Kandidaat negeren.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Zie ook

[Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Uw personeel organiseren](hr-personnel-departments-jobs-positions.md)<br>
[De onderdelen van een taak instellen](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
