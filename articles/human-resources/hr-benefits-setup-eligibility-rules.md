---
title: Geschiktheidsregels en -opties configureren
description: Stel de geschiktheidsregels en -opties in voor vergoedingen in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25593bc4d136e403c7ba87e044c95f4fae1e7db9
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558364"
---
# <a name="configure-eligibility-rules-and-options"></a>Regels en opties voor geschiktheid configureren 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Nadat u de vereiste parameters voor vergoedingenbeheer hebt geconfigureerd, kunt u de geschiktheidsregels, bundels, perioden en programma's maken die u aan uw vergoedingsplannen gaat koppelen.

Geschiktheidsregels worden gebruikt om te bepalen of werknemers in aanmerking komen voor een regeling. Werknemers moeten aan de voorwaarde van ten minste één regel voldoen om in aanmerking te komen voor de vergoeding. U hebt bijvoorbeeld twee regels in een plan. De eerste regel (regel 1) geeft aan dat werknemer van het type **Werknemer** moet zijn. De tweede regel (regel 2) geeft aan dat de werknemer een fulltime medewerker moet zijn. Daarom komen werknemers die aan regel 1 voldoen ook in aanmerking als ze alleen parttime werken.

U kunt echter één regel met meerdere voorwaarden instellen. In dat geval moeten werknemers aan alle voorwaarden van de regel voldoen om in aanmerking te komen voor de vergoeding. U hebt bijvoorbeeld een regel die **Fulltime werknemer** wordt genoemd. Deze regel geeft aan dat het werknemerstype **Werknemer** moet zijn *en* dat de werknemer fulltime moet werken. Daarom moeten werknemers aan beide voorwaarden van de regel voldoen om in aanmerking te komen.

> [!IMPORTANT]
> Aan elk vergoedingsplan moet ten minste één geschiktheidsregel worden gekoppeld. U kunt meerdere regels aan een vergoeding koppelen.

## <a name="create-an-eligibility-rule"></a>Een geschiktheidsregel maken

Met geschiktheidsregels wordt gedefinieerd welke werknemers zich kunnen inschrijven bij elk vergoedingsplan. Nadat u geschiktheidsregels hebt gedefinieerd, wijst u deze toe aan vergoedingsplannen. Vervolgens kunt u de geschiktheid voor inschrijving verwerken om te zien welke werknemers in aanmerking komen voor elk plan. 

Tijdens open inschrijving kunnen werknemers vergoedingsplannen selecteren. Als ze niet in aanmerking komen voor een vergoedingsplan dat is gebaseerd op geschiktheidsregels nadat ze al zijn ingeschreven, worden ze niet automatisch weer uitgeschreven. Gewoonlijk wordt, wanneer zich een levensgebeurtenis voordoet die van invloed is op de geschiktheid voor een plan, een inschrijvingsperiode geïnitieerd voor de werknemer om plannen te selecteren waarvoor hij of zij in aanmerking komt. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsregels en -opties**.

2. Selecteer op het tabblad **Geschiktheidsregels** de optie **Nieuw** om een geschiktheidsregel te maken. Selecteer **Gekoppelde plannen** om plannen weer te geven die aan een geschiktheidsregel zijn gekoppeld.

3. Geef de waarden op voor de volgende velden.

   | Veld | Beschrijving |
   | --- | --- |
   | **Geschiktheidsregel** | Een unieke id voor de geschiktheidsregel. |
   | **Beschrijving** | Een beschrijving van de geschiktheidsregel. |
   | **Geldig vanaf datum en tijd** | De begindatum van de geschiktheidsregel. | 
   | **Geldig tot datum en tijd** | De einddatum van de geschiktheidsregel. |
   | **Gebruikerstype werknemer** | Geeft aan of het werknemerstype van de werknemer moet worden gebruikt in de geschiktheidsregel. |
   | **Medewerkertype** | Het werknemertype, als de schakeloptie **Werknemertype gebruiken** is ingesteld op **Ja**. |
   | **Werknemerstatus gebruiken** | Geeft aan of het werknemertype van de werknemer moet worden gebruikt in de geschiktheidsregel. |
   | **Status** | De werknemerstatus, als de schakeloptie **Werknemerstatus gebruiken** is ingesteld op **Ja**. Als de schakeloptie **Werknemerstatus gebruiken** is ingesteld op **Nee**, wordt het veld niet gebruikt. |
   | **Aanstellingscategorie gebruiken** | Geeft aan of het waarde voor **Aanstellingscategorie** van de werknemer moet worden gebruikt als onderdeel van de geschiktheidsregel voor vergoedingen. | 
   | **Aanstellingscategorie** | De aanstellingscategorie van de werknemer als de schakeloptie **Aanstellingscategorie gebruiken** is ingesteld op **Ja**. |
   | **Nieuwe aanstellingsregel gebruiken** | Geeft aan of de waarde voor een nieuwe aanstellingsperiode van een nieuw aangenomen werknemer wordt gebruikt als onderdeel van de geschiktheidsregel voor vergoedingen. |
   | **Inschrijvingsperiode** | De tijdsperiode waarin inschrijving van nieuw aangenomen werknemers is toegestaan. Als u dit ook instelt in parameters, heeft de parameterinstelling voorrang op deze waarde. |
   | **Voormalige aanstellingsstatus gebruiken** | Geeft aan of het gebruik van een eerdere aanstellingsstatus van een werknemer moet worden gebruikt als onderdeel van de geschiktheidsregel voor vergoedingen. U kunt bijvoorbeeld een geschiktheidsregel opgeven die de wachttijd voor de dekking kwijtscheldt voor alle werknemers die zijn overgegaan van een status **Ontslagen** naar een status **Aangesteld** binnen 90 dagen na hun vorige aanstelling. |

4. Selecteer onder **Aanvullende criteria** de volgende opties en voeg zo nodig informatie toe.

   | Optie | Beschrijving |
   | --- | --- |
   | **Geschikte leeftijd** | Geeft het leeftijdsbereik of de leeftijdsbereiken aan die zijn vereist om aan de geschiktheidsregel te voldoen. |
   | **Geschikte afdeling** | Geeft de afdeling of afdelingen aan waartoe een werknemer moet behoren om aan de geschiktheidsregel te voldoen. |
   | **Geschikt aanstellingstype** | Geeft het type of de typen aanstelling aan waaronder een werknemer moet zijn gecategoriseerd om aan de geschiktheidsregel te voldoen. Bijvoorbeeld voltijd of deeltijd. |
   | **Geschikte taak** | Geeft de functie of functies aan die aan de geschiktheidsregel voldoen. Functies zijn gekoppeld aan posities en posities worden bekleed door werknemers. |
   | **Geschikte taakfunctie** | Geeft de functiepositie of -posities aan die aan een geschiktheidsregel voldoen. Bijvoorbeeld verkoopmedewerkers of technici. |
   | **Geschikt taaktype** | Geeft het functietype of de functietypen aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld administratief of leidinggevend. |
   | **In aanmerking komende rechtspersoon** | Geeft de rechtspersoon of rechtspersonen aan die geldig zijn voor de geschiktheidsregel. Bijvoorbeeld Contoso Entertainment System USA. |
   | **Geschikte compensatieregio** | Geeft de werknemerslocatie aan die aan de geschiktheidsregel voldoet. Bijvoorbeeld VS - midden. |
   | **Geschikte positie** | Geeft de positie of posities aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld HR-assistent of HR-manager. |
   | **Geschikt positietype** | Geeft het positietype of de positietypen aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld voltijd. |
   | **Geschikte status** | Geeft de staten of provincies aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld North Dakota VS of British Columbia, Canada. |
   | **Geschikte arbeidsvoorwaarden** | Geeft de arbeidsvoorwaarden aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld individueel of groepscontract. |
   | **In aanmerking komende vereniging** | Geeft de lidmaatschappen van vakverenigingen aan die aan de geschiktheidsregel voldoen. Voorbeeld: Forklift Drivers of America.</br></br>Wanneer u een op vakbondslidmaatschap gebaseerde geschiktheidsregel gebruikt, moet in de vakbondsrecord van de werknemer de einddatum zijn ingevuld. U kunt dit veld niet leeg laten. |
   | **Geschikte postcode** | Geeft de postcodes aan die aan de geschiktheidsregel voldoen. Bijvoorbeeld 58104. |

5. Onder **Aanvullende details** kunt u de volgende aanvullende gegevens weergeven.

   | Veld | Beschrijving |
   | --- | --- |
   | **Veld met geschikte gebruiker** | Geeft aanvullende geschiktheidsregels aan die zijn gebaseerd op door de klant gedefinieerde velden. |
   | **Geschiktheidstype** | Geeft de criteriacategorie aan die u onder **Aanvullende criteria** hebt geselecteerd. |
   | **Geschiktheidsverwijzing** | Geeft de waarden aan die u onder **Aanvullende criteria** hebt geselecteerd. |
   | **Beschrijving** | De beschrijving die u onder **Aanvullende criteria** hebt geselecteerd. |

6. Selecteer **Opslaan**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Aangepaste velden in geschiktheidsregels gebruiken

U kunt [aangepaste velden](hr-developer-custom-fields.md) in Human Resources maken om extra informatie bij te houden. Deze velden kunnen rechtstreeks aan de gebruikersinterface worden toegevoegd en een kolom wordt dynamisch toegevoegd aan de onderliggende tabel.  

Aangepaste velden kunnen worden gebruikt in het geschiktheidsproces. Geschiktheidsregels kunnen een of meer aangepaste velden gebruiken om de geschiktheid van een werknemer vast te stellen.  Als u een aangepast veld wilt toevoegen aan een bestaande regel of een nieuwe regel wilt maken, gaat u naar **Vergoedingenbeheer > Koppelingen > Instellingen > Geschiktheidsregels > Geschiktheid aangepast veld**. Op deze pagina kunt u een regel maken met één of meerdere aangepaste velden en u kunt meerdere waarden definiëren voor elk aangepast veld om de geschiktheid te bepalen.

In de volgende tabellen worden aangepaste velden ondersteund die kunnen worden gebruikt bij het verwerken van geschiktheid:

- Werknemer (HcmWorker)  
- Functie (HcmJob)  
- Positie (HcmPosition)  
- Positiedetails (HcmPositionDetail)  
- Medewerkertoewijzing voor positie  
- Dienstverband (HcmEmployment)  
- Details dienstverband (HcmEmploymentDetails)  
- Functiedetails (HcmJobDetails)  

De volgende typen aangepaste velden worden ondersteund bij het verwerken van geschiktheid:

- Tekst  
- Selectielijst  
- Nummer  
- Decimaal  
- Selectievakje  

In de volgende tabel ziet u informatie over het formulierveld Geschiktheid aangepast veld.

| Veld  | Beschrijving |
|--------|-------------|
| Naam | Naam van de criteria die worden gemaakt. |
| Tabelnaam | De tabelnaam die het aangepaste veld bevat dat wordt gebruikt voor de geschiktheidsregel. |
| Veldnaam | Het veld dat wordt gebruikt voor de geschiktheidsregel. |
| Operatortype | Geeft de operator weer die wordt gebruikt in de configuratie van aangepaste velden voor geschiktheid. |
| Waarde | Geeft de waarde weer die wordt gebruikt in de configuratie van aangepaste velden voor geschiktheid. |

## <a name="eligibility-logic"></a>Geschiktheidslogica

In de volgende secties wordt beschreven hoe geschiktheid voor vergoedingen wordt verwerkt.

### <a name="rules-assigned-to-a-plan"></a>Regels die aan een plan zijn toegewezen 
Wanneer meerdere geschiktheidsregels aan een vergoedingsplan zijn toegewezen, moet een werknemer aan ten minste één regel voldoen om in aanmerking te komen voor inschrijving bij het vergoedingsplan.  In het volgende voorbeeld moet de werknemer voldoen aan de vereisten van de regel **Functietype** of de regel **Actieve werknemers**.

![De werknemer moet voldoen aan de vereisten van de regel Functietype of de regel Actieve werknemers.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Criteria binnen een geschiktheidsregel 
Binnen een regel definieert u de criteria waaruit de regel bestaat. In het bovenstaande voorbeeld is het criterium voor de regel **Functietype** waar Functietype = Directeuren. Daarom moet de werknemer een directeur zijn om in aanmerking te komen. Dit is een regel met slechts één criterium binnen de regel.

U kunt regels met meerdere criteria definiëren. Wanneer u meerdere criteria binnen een geschiktheidsregel definieert, moet een werknemer voldoen aan alle criteria binnen de regel om in aanmerking te komen voor het vergoedingsplan. 

De bovenstaande regel **Actieve werknemers** bestaat bijvoorbeeld uit de volgende criteria. Een werknemer kan alleen in aanmerking komen op basis van de regel **Actieve werknemers** als de werknemer in dienst is bij rechtspersoon USMF *en* een positie van het type fulltime heeft.  

![Criteria binnen een geschiktheidsregel.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Meerdere voorwaarden binnen criteria

Regels kunnen verder worden uitgebreid om meerdere voorwaarden te gebruiken binnen één criterium. De werknemer moet aan ten minste één voorwaarde voldoen om in aanmerking te komen. Als u verder wilt gaan op het bovenstaande voorbeeld kan de regel **Actieve werknemers** verder worden uitgebreid met werknemers die ook parttime werknemers zijn. Als resultaat hiervan moet de werknemer nu een werknemer in USMF zijn *en* een fulltime of parttime werknemer zijn.  

![Meerdere voorwaarden binnen criteria.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Geschiktheidsvoorwaarden binnen een criterium van een aangepast veld 
Op dezelfde manier als hierboven is het mogelijk om aangepaste velden te gebruiken bij het maken van geschiktheidsregels. Deze werken op dezelfde manier. U kunt bijvoorbeeld terugbetaling van internetkosten aanbieden aan werknemers in Utrecht en Amsterdam die thuis werken, omdat de internetkosten op die locaties hoger zijn. Hiervoor maakt u twee aangepaste velden: **Kantoorlocatie** (selectielijst) en **Thuiswerken** (selectievakje). Maak vervolgens een regel met de naam **Thuiswerkende werknemers**. Als criterium voor de regel wordt **Kantoorlocatie = Utrecht** of **Amsterdam** gebruikt *en* **Thuiswerkend = Ja**.

Aangepaste geschiktheidsregels moeten worden ingesteld, zoals in de volgende afbeelding wordt aangegeven. 

![Geschiktheidsvoorwaarden binnen het criterium van een aangepast veld.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Bundels configureren

Bundels zijn een reeks gerelateerde vergoedingsplannen. U kunt vergoedingsbundels gebruiken om vergoedingsplannen te groeperen die een werknemer moet kiezen om zich in te schrijven bij bepaalde vergoedingsplannen die afhankelijk kunnen zijn van andere inschrijvingen voor vergoedingsplannen. Voorbeelden van wanneer u een bundel kunt gebruiken, zijn:

- Een bundel met een ziektekostenverzekering die een hoge aftrekbare ziektekostenverzekering omvat met een bijbehorende spaarrekening voor gezondheidszorg (HSA).

- Een levensverzekeringsplan met een verplichte levensverzekering voor een werknemer, gebundeld met een levensverzekering voor gezinsleden. Dit zou ervoor zorgen dat een werknemer geen levensverzekering voor gezinsleden kan selecteren zonder zich aan te melden voor verzekering van de werknemer.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsregels en -opties**.

2. Selecteer op het tabblad **Bundels** de optie **Nieuw** om een bundel te maken. Selecteer **Gekoppelde plannen** om plannen weer te geven die aan een bundel zijn gekoppeld.

3. Geef de waarden op voor de volgende velden.

   | Veld | Beschrijving |
   | --- | --- |
   | **Bundel** | Een unieke id voor de bundel. |
   | **Beschrijving** | Een beschrijving van de bundel. |
   | **Hoofdvrachtbrief** | Geeft aan of een van de plannen in de bundel moet worden gemarkeerd als het hoofdplan. Het hoofdplan moet worden geselecteerd tijdens een open inschrijving als onderdeel van de bundel voordat de vergoedingsbeheerder de keuzen voor vergoedingen van de werknemer kan bevestigen. |
   | **Geldig vanaf datum en tijd** | De datum en tijd waarop de bundel actief wordt. |
   | **Geldig tot** | De datum waarop de bundel verloopt. De standaardwaarde is 12/31/2154, wat voor nooit staat. |

4. Selecteer **Opslaan**.

## <a name="configure-periods"></a>Perioden configureren

Perioden bepalen wanneer vergoedingen van kracht zijn en wanneer werknemers zich mogen inschrijven. U kunt zoveel perioden maken als u wilt om open inschrijving voor vergoedingen en perioden voor vergoedingen te behouden. Vergoedingsplanjaren kunnen al dan niet een kalenderjaar volgen. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsregels en -opties**.

2. Selecteer op het tabblad **Perioden** de optie **Nieuw** om een periode te maken. Selecteer **Plannen koppelen** om een proces uit te voeren waarbij alle geldige actieve vergoedingsplannen aan de vergoedingsperiode worden gekoppeld. Selecteer **Gekoppelde plannen** om plannen weer te geven die aan een bundel zijn gekoppeld. 

3. Geef de waarden op voor de volgende velden.

   | Veld | Beschrijving |
   | --- | --- |
   | **Periode** | Een unieke id voor de periode. |
   | **Geldig vanaf datum en tijd** | De begindatum en -tijd waarop de vergoedingsperiode actief is. |
   | **Geldig tot datum en tijd** | De datum en tijd waarop de vergoedingsperiode inactief wordt. |
   | **Begin inschrijving** | De begindatum voor open inschrijving. Open inschrijving is wanneer een werknemer vergoedingskeuze kan maken via selfservice. |
   | **Einde inschrijving** | De einddatum voor open inschrijving. |
   | **Open** | Geeft aan of de periode open is op basis van de systeemdatum en de begindatum en -tijd en de einddatum en -tijd van de geldigheidsperiode. | 
   | **Vorige periode** | Geeft de vergoedingsperiode aan die voorafgaat aan de geselecteerde vergoedingsperiode. Deze informatie wordt gebruikt tijdens de inschrijving van de geschiktheid voor een vergoeding om plannen, dekkingsopties en aangewezen personen uit een voorafgaand jaar toe te wijzen. |
 
4. Selecteer **Opslaan**.

## <a name="use-a-flex-credit-program"></a>Een flex-kredietprogramma gebruiken

U kunt flex-kredietprogramma's gebruiken om werknemers in te schrijven voor vergoedingen op basis van een vooraf bepaald aantal flex-kredieten. Werknemers kunnen kiezen hoe zij hun flex-kredieten willen toewijzen. Als een werknemer bijvoorbeeld onder het ziektekostenverzekeringsplan van zijn of haar echtgenoot of echtgenote valt, kan deze werknemer de kredieten die hij of zij anders zou hebben gebruikt voor gezondheidszorg, nu gebruiken voor andere vergoedingen.

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsregels en -opties**.

2. Selecteer op het tabblad **Perioden** de optie **Flex-kredietprogramma's**.

3. Selecteer een flex-kredietprogramma dat moet worden toegepast. De velden bevatten de volgende informatie.

   | Veld | Beschrijving |
   | --- | --- |
   | Vergoedingskrediet-id | De unieke id van het flex-kredietprogramma. |
   | Beschrijving | Een omschrijving van het flex-kredietprogramma. | 
   | Begindatum | De datum waarop het flex-kredietprogramma actief wordt. |
   | Einddatum | De einddatum van het flex-kredietprogramma. U kunt de standaardwaarde (12/31/2154) laten staan om aan te geven dat het Flex-kredietprogramma geen geplande vervaldatum heeft. |
   | Totale kredietwaarde | Het aantal kredieten dat iedere werknemer dient te gebruiken voor zijn of haar vergoedingen. |
   | Omslagregel | De regel die moet worden gebruikt voor het evenredig verdelen van flex-kredieten wanneer een werknemer in dienst wordt genomen midden in een flex-kredietperiode. </br></br><ul><li>**Geen** – de werknemer ontvangt geen flex-kredieten als deze is aangesteld nadat de periode van het flex-kredietprogramma is gestart.</li><li>**Volledig krediet** – de werknemer ontvangt het volledige aantal flex-kredieten, ongeacht het moment waarop deze is aangesteld.</li><li>**Evenredig** – de werknemer ontvangt een evenredig aantal flex-kredieten op basis van de begindatum.</li></ul> |
   | Formule voor het berekenen van een evenredig aantal flex-kredieten | De regel die moet worden gebruikt voor het evenredig verdelen van het aantal flex-kredieten voor werknemers die in dienst wordt genomen midden in een vergoedingsperiode voor het flex-kredietprogramma. Het evenredige aantal flex-kredieten wordt berekend op basis van de begindatum van de aanstelling. Dit veld wordt alleen gebruikt als u **Evenredig** selecteert in het veld **Evenredigheidsregel**. </br></br><ul><li>**Dagelijks** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op dagniveau. Het totale aantal flex-kredieten wordt gedeeld door het aantal dagen in de periode. Als uw vergoedingsperiode bijvoorbeeld 400 dagen is, wordt het totale aantal flex-kredieten door 400 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per dag ontvangen.</li><li>**Huidige maand** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op maandniveau, afgerond op de huidige maand. Het totale aantal flex-kredieten wordt gedeeld door het aantal maanden in de periode. Als uw vergoedingsperiode bijvoorbeeld 15 maanden is, wordt het totale aantal flex-kredieten door 15 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per maand ontvangen.</li><li>**Volgende maand** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op maandniveau, afgerond op de volgende maand. Het totale aantal flex-kredieten wordt gedeeld door het aantal maanden in de periode. Als uw vergoedingsperiode bijvoorbeeld 15 maanden is, wordt het totale aantal flex-kredieten door 15 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per maand ontvangen.</li></ul> |
   
   Zorg ervoor dat elk vergoedingsplan is ingeschreven voor slechts één flex-kredietprogramma per vergoedingsperiode. Anders weet het systeem niet welk flex-kredietprogramma wordt gebruikt om flex-kredieten toe te kennen en treden er problemen op. 

## <a name="configure-programs"></a>Programma's configureren

Programma's zijn een reeks vergoedingsplannen die een gemeenschappelijke set geschiktheidsregels hebben. U kunt geschiktheidsregels definiëren voor het gehele programma in plaats van voor afzonderlijke plannen. Bijvoorbeeld een FTE-programma voor Contoso Canada of een Executive-programma voor Contoso Europe. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsregels en -opties**.

2. Selecteer op het tabblad **Programma's** de optie **Nieuw** om een programma te maken. Als u uitzonderingen wilt maken voor werknemers die niet voldoen aan de vereisten voor de geschiktheidsregel, selecteert u **Geschiktheidsregel negeren**. Selecteer **Gekoppelde plannen** om plannen weer te geven die aan een programma zijn gekoppeld.

3. Geef de waarden op voor de volgende velden.

   | Veld | Beschrijving |
   | --- | --- |
   | **Programma** | Een unieke id voor het programma. |
   | **Beschrijving** | Een beschrijving van het programma. | 
   | **Geldig vanaf datum en tijd** | De datum en tijd waarop het programma actief wordt. |
   | **Geldig tot datum en tijd** | De datum en tijd waarop het programma afloopt. De standaardwaarde is 12/31/2154, wat voor nooit staat. |
   | **Wachtperiode voor dekking** | De periode die een werknemer moet wachten voordat de dekking start voor het vergoedingsprogramma. |
   | **Wachtperiode voor inhouding** | De periode die een werknemer wacht voordat inhoudingen beginnen voor het vergoedingsprogramma. |
   | **Geschiktheidsregels** | Selecteer de geschiktheidsregels die u wilt toepassen op het vergoedingsprogramma. U definieert de geschiktheidsregels op het tabblad **Geschiktheidsregels** op deze pagina. |
   
4. Selecteer **Opslaan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
