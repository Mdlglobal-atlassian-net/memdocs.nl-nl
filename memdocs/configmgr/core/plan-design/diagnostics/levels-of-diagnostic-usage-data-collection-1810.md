---
title: Diagnostische en gebruiks gegevens voor 1810
titleSuffix: Configuration Manager
description: Meer informatie over de specifieke gegevens die door Configuration Manager worden verzameld op elk niveau in versie 1810.
ms.date: 05/13/2019
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
ms.assetid: bce9e299-7b3a-4f51-8863-a322877daa2c
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: 2c1c5231ab67e11ee01b968a2e7238ea13c02fca
ms.sourcegitcommit: bbf820c35414bf2cba356f30fe047c1a34c5384d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "81714274"
---
# <a name="diagnostic-and-usage-data-for-version-1810"></a>Diagnostische en gebruiks gegevens voor versie 1810

*Van toepassing op: Configuration Manager (huidige vertakking)*

In de volgende secties vindt u meer informatie over de gegevens die op elk niveau worden verzameld. Zie [niveaus van diagnostische gebruiks gegevens](levels-overview.md)voor meer informatie over de niveaus en hoe u deze kunt wijzigen.

Wijzigingen ten opzichte van vorige versies worden aangegeven met ***[New]***, ***[updated]***, ***[dismoved]*** of ***[dismoved]***.

> [!IMPORTANT]
> Configuration Manager verzamelt geen site codes, namen van sites, IP-adressen, gebruikers namen, computer namen, fysieke adressen of e-mail adressen op het niveau basis of uitgebreid. Een verzameling van deze informatie op het niveau volledig is niet doel gericht. Het is mogelijk opgenomen in geavanceerde diagnostische gegevens, zoals logboek bestanden of moment opnamen van het geheugen. Micro soft gebruikt deze informatie niet om u te identificeren, contact met u op te nemen of reclame te ontwikkelen.

## <a name="level-1---basic"></a><a name="bkmk_level1"></a> Niveau 1 - Basis

Voor Configuration Manager versie 1810 bevat dit niveau de volgende gegevens:

- Statistieken over Configuration Manager-console verbindingen: besturingssysteem versie, taal, SKU en architectuur, systeem geheugen, aantal logische processors, verbinding maken met site-ID, geïnstalleerde .NET-versies en console taal pakketten

- Het aantal basis toepassingen en implementatie typen: totaal aantal apps, totaal aantal apps met meerdere implementatie typen, totaal aantal apps met afhankelijkheden, totaal aantal vervangen apps en het aantal implementatie technologieën dat in gebruik is

- Basis Configuration Manager site hiërarchie gegevens: site lijst, type, versie, status, aantal clients en tijd zone

- ***[Bijgewerkt]*** Basis configuratie van de Data Base: processors, geheugen grootte, geheugen instellingen, Configuration Manager database configuratie, Configuration Manager database grootte, cluster configuratie, configuratie van gedistribueerde weer gaven en versie van het bijhouden van wijzigingen  

- Basis detectie statistieken: aantal detecties, minimale/maximale/gemiddelde groeps grootten en wanneer de site volledig wordt uitgevoerd met Azure Active Directory Services

- Basis Endpoint Protection informatie over client versies voor antimalware

- Basis aantallen installatie kopieën van het besturings systeem

- Basis informatie over de site systeem server: gebruikte site systeem rollen, Internet-en SSL-status, besturings systeem, processors, fysieke of virtuele machine en gebruik van hoge Beschik baarheid van site server

- Configuration Manager-database schema (hash van alle object definities)

- Geconfigureerd niveau voor diagnostische en gebruiks gegevens, online-of offline modus en configuratie van snelle updates

- Aantal client talen en land instellingen

- Aantal Configuration Manager client versies, versies van besturings systemen en Office-versies

- Aantal besturings systemen voor beheerde apparaten en beleids regels die zijn ingesteld door de Exchange connector

- ***[Bijgewerkt]*** Aantal Windows 10-apparaten per vertakking, build en uniek Active Directory forest  

- Aantal Windows 10-clients die gebruikmaken van Windows Update voor bedrijven  

- Metrische database prestaties: informatie over replicatie verwerking, belangrijkste SQL Server opgeslagen procedures per processor en schijf gebruik

- Distributie punt-en beheer punt typen en basis configuratie-informatie: beveiligd, voor bereid, PXE, multi cast, SSL-status, pull/peer-distributie punten, MDM-ingeschakeld en SSL-ingeschakeld

- Gehashte lijst met extensies voor de eigenschappen pagina's en wizards van de beheer console

- Setup-informatie:  

    - Bouwen, type installatie, taal pakketten, functies die u hebt ingeschakeld   

    - Gebruik vóór de release, type installatie media, vertakkings type  

    - Verval datum Software Assurance  

    - Implementatie status en fouten van update pakket, download voortgang en vereiste fouten 

    - Gebruik van snelle ring van updates  

    - Versie van script na de upgrade  

- SQL-versie, service pack level, Edition, collatie-ID en tekenset  

- Statistieken voor diagnostische en gebruiks gegevens: bij uitvoering, runtime, fouten  

- Of netwerk detectie is ingeschakeld of uitgeschakeld  

- Aantal clients dat is gekoppeld aan Azure Active Directory  

- Aantal gefaseerde implementaties dat is gemaakt op basis van het type  

- Aantal uitgebreide samenwerkings clients  

- Gehashte lijst met de hardware-inventarisatie-eigenschappen die langer zijn dan 255 tekens  

- Aantal clients op basis van de inschrijvings methode voor co-beheer  

- Fout statistieken voor inschrijving van co-beheer  

- Aantal clients door de leeftijd van het Windows-besturings systeem, het dichtstbijzijnde interval van drie maanden  

- ***[Bijgewerkt]*** Top 10 van processor namen die worden gebruikt op clients en servers  

- Aantallen en verwerkings tarieven van Key Configuration Manager-objecten: gegevens detectie records (DDR), status berichten, status berichten, Hardware-inventarisatie, software-inventarisatie en totaal aantal bestanden in Postvak in  

- Informatie over de schijf-en processor prestaties van de site server  

- Informatie over de uptime en het geheugen gebruik voor Configuration Manager site server processen  

- Aantal crashes voor Configuration Manager site server processen en hand tekening-ID van Watson, indien beschikbaar  

- ***[Nieuw]*** Gehashte lijst met top SQL-query's op basis van het geheugen gebruik en het aantal vergren delingen  

- ***[Verplaatst, bijgewerkt]*** Samengevoegde gebruiks statistieken van co-beheer: het aantal clients dat ooit is inge schreven, het aantal geregistreerde clients, het aantal clients dat in behandeling is voor inschrijving, het ontvangen van beleid, de werk belasting, de status van de pilot/uitsluitings verzameling en inschrijvings fouten  



## <a name="level-2---enhanced"></a><a name="bkmk_level2"></a> Niveau 2 - Uitgebreid

Voor Configuration Manager versie 1810 bevat dit niveau de volgende gegevens:

### <a name="application-management"></a>Toepassingsbeheer  

- App-vereisten: aantal ingebouwde voor waarden waarnaar wordt verwezen door de implementatie technologie  

- Vervanging van app, maximum diepte van keten  

- Toepassings goedkeurings statistieken en gebruiks frequentie  

- Statistieken voor grootte van toepassings inhoud  

- Informatie over de implementatie van toepassingen: gebruik van installeren versus verwijderen, vereist goed keuring, gebruikers interactie ingeschakeld/uitgeschakeld, afhankelijkheid, vervanging en aantal gebruik van de functie voor installatie gedrag  

- Toepassings beleids grootte en complexiteits statistieken  

- Statistieken over beschikbare toepassingsaanvragen  

- Basis configuratie-informatie voor pakketten en Program ma's: implementatie opties en-programma vlaggen  

- Elementaire informatie over gebruik/targeting voor implementatie typen: gebruiker versus apparaat gericht, vereist versus beschikbaar en universele apps  

- Aantal App-V-omgevingen en implementatie-eigenschappen  

- Aantal toepassings toepasingen door besturings systeem  

- Aantal toepassingen waarnaar wordt verwezen in een taken reeks  

- Aantal afzonderlijke huis stijl voor toepassings catalogus  

- Aantal Office 365-toepassingen dat is gemaakt met dash board  

- Aantal pakketten per type  

- Aantal pakket/programma-implementaties  

- Aantal toepassingen met een Windows 10-licentie  

- Aantal Windows Installer implementatie typen door inhouds instellingen te verwijderen  

- Aantal Microsoft Store voor zakelijke apps en synchronisatie statistieken: samenvatte typen apps, status van een app en het aantal online en offline gelicentieerde apps  

- Type onderhoudsvenster en duur  

- Mini maal/Maxi maal/gemiddeld aantal toepassings implementaties per gebruiker/apparaat per tijds periode  

- Meest voorkomende fout codes voor toepassings installaties door implementatie technologie  

- MSI-configuratie opties en-tellingen  

- Statistieken over de interactie van de eind gebruiker met meldingen voor vereiste software-implementaties  

- Gebruik van Universal Data Access, hoe gemaakt  

- Statistische gegevens van affiniteit van gebruiker met apparaat  

- Max en gemiddelde primaire gebruikers per apparaat  

- Gebruik van globale voor waarde van toepassing per type  

- Configuratie van software Center-aanpassing  

- Gereedheid en aantal voor pakket conversie beheer  

- Aantal toepassings detectie methoden op type  

- Aantal toepassings afdwingings fouten  

- Eigenschappen van MSI-installatie programma  

- Statistieken van aanvragen voor gebruikers installatie  

- ***[Nieuw]*** Cumulatieve statistieken voor het gebruik van de functie voor e-mail goedkeuring  

- ***[Nieuw]*** Aantal bestanden, inhouds grootte, aantal services en aangepaste acties aantal MSIs in Application Catalog  


### <a name="client"></a>Client  

- De AMT-client versie (Active Management Technology)  

- BIOS-leeftijd in jaren  

- Aantal apparaten waarop beveiligd opstarten is ingeschakeld  

- Aantal apparaten op TPM-status  

- Automatische client upgrade: implementatie configuratie inclusief client Piloting en uitgesloten gebruik (uitgebreide interoperabiliteits client)  

- Configuratie van client cache grootte  

- Download fouten client implementatie  

- Client status statistieken en samen vatting van belangrijkste problemen per client versie  

- Status van bewerkings actie client melding: het aantal keren dat elke keer wordt uitgevoerd, het maximum aantal beoogde clients en het gemiddelde slagings percentage  

- Aantal clientinstallaties vanaf elk bronlocatietype  

- Aantal mislukte clientinstallaties  

- Aantal apparaten dat is gevirtualiseerd door Hyper-V of Azure  

- Aantal software Center-acties  

- Aantal met UEFI ingeschakelde apparaten  

- Implementatie methoden die worden gebruikt voor de client en het aantal clients per implementatie methode  

- Lijst met en aantal ingeschakelde clientagents  

- BESTURINGSSYSTEEM leeftijd in maanden  

- Aantal hardware-inventaris klassen, software-inventarisatie regels en regels voor bestands verzameling  

- Statistieken voor apparaatstatusverklaring: meest voorkomende fout codes, aantal on-premises servers en aantallen apparaten in verschillende Staten  

- Aantal apparaten standaard browser  

- Aantal door Configuration Manager gegenereerde certificaten voor Server verificatie  

- Aantal micro soft Surface-apparaten op model  


### <a name="cloud-services"></a>Cloud Services  

- Detectie statistieken Azure Active Directory  

- Configuratie-en gebruiks statistieken van cloudbeheergateway: aantallen regio's en omgevingen, en verificatie/autorisatie statistieken  

- Aantal Azure Active Directory toepassingen en services die zijn verbonden met Configuration Manager  

- Aantal verzamelingen dat is gesynchroniseerd met Azure Log Analytics  

- Aantal Upgrade Analytics-connectors  

- Of de Azure Log Analytics Cloud connector is ingeschakeld  

- Aantal pull-distributie punten met een Cloud distributiepunt als een bron locatie  


### <a name="cmpivot"></a>CMPivot

- Gebruiks statistieken voor CMPivot  

- ***[Nieuw]*** Aantal opgeslagen CMPivot-query's  

- ***[Nieuw]*** Aantal query's per entiteits type  


### <a name="co-management"></a>Co-beheer  

- Inschrijvings planning en historische statistieken  

- Telling van clients die in aanmerking komen voor co-beheer  

- Gekoppelde Microsoft Intune Tenant  


### <a name="collections"></a>Verzamelingen  

- Gebruik van verzamelings-ID (niet-uitgevoerde Id's)  

- Statistieken verzamelings evaluatie: query tijd, toegewezen versus niet-toegewezen aantallen, tellingen op type, ID-rollover en regel gebruik  

- Verzamelingen zonder een implementatie  


### <a name="compliance-settings"></a>Instellingen voor naleving  

- Basis informatie over de basislijn configuratie: aantal, aantal implementaties en aantal verwijzingen  

- Fout statistieken voor nalevings beleid  

- Aantal configuratie-items per type  

- Aantal implementaties die verwijzen naar ingebouwde instellingen, met inbegrip van de instelling herstellen  

- Aantal regels en implementaties die voor aangepaste instellingen zijn gemaakt, met inbegrip van herstel instelling  

- Aantal geïmplementeerde Simple Certificate Enrollment Protocol (SCEP), VPN, Wi-Fi, certificaat (. pfx) en nalevings beleids sjablonen  

- Aantal SCEP-certificaten, VPN-, Wi-Fi-, certificaat-en nalevings beleid-implementaties per platform  

- Windows hello voor bedrijven-beleid (gemaakt, geïmplementeerd)  

- Aantal geïmplementeerde micro soft Edge-browser beleid  


### <a name="content"></a>Inhoud  

- Statistieken grens groep: hoeveel snelle, hoeveel trage, aantallen per groep en terugval relaties  

- Informatie over grens groep: het aantal grenzen en site systemen dat is toegewezen aan elke grens groep  

- Relaties tussen grens groepen en terugval configuratie  

- Statistieken voor downloaden van client inhoud  

- Aantal grenzen per type  

- Aantal peer-cache-clients, gebruiks statistieken en gedeeltelijke download statistieken  

- Configuratie-informatie over Distribution Manager: threads, vertraging bij nieuwe pogingen, aantal nieuwe pogingen en pull-distributie punt instellingen  

- Configuratie-informatie voor distributie punt: het gebruik van Branch-cache en distributiepunt bewaking  

- Informatie over distributiepunten groepen: aantal pakketten en distributie punten die aan elke distributiepunten groep zijn toegewezen  

- Type inhouds bibliotheek, lokaal of extern  

- ***[Nieuw]*** Aantal grens groepen per configuratie  


### <a name="endpoint-protection"></a>Endpoint Protection  

- Micro soft Defender Advanced Threat Protection (ATP)-beleid (voorheen bekend als Windows Defender ATP): het aantal beleids regels en of er beleids regels worden geïmplementeerd. 

- Aantal waarschuwingen dat is geconfigureerd voor Endpoint Protection functie  

- Aantal verzamelingen dat is geselecteerd om te worden weer gegeven in Endpoint Protection dash board  

- Aantal Windows Defender exploit Guard-beleids regels, implementaties en gerichte clients  

- Endpoint Protection implementatie fouten, het aantal Endpoint Protection beleids implementatie fout codes  

- Endpoint Protection antimalware en Windows Firewall gebruik van beleid (aantal unieke beleids regels toegewezen aan groep). Deze gegevens bevatten geen informatie over de instellingen die zijn opgenomen in het beleid.  


### <a name="migration"></a>Migratie  

- Aantal gemigreerde objecten (gebruik van de wizard Migratie)  


### <a name="mobile-device-management-mdm"></a>Mobile Device Management (MDM)  

- Aantal uitgegeven acties voor mobiele apparaten: de opdrachten vergren delen, rest vastmaken, wissen, buiten gebruik stellen en nu synchroniseren  

- Aantal beleidsregels voor mobiele apparaten  

- Aantal mobiele apparaten Configuration Manager en Microsoft Intune beheerd, en hoe u deze hebt Inge schreven (bulksgewijs, op basis van gebruikers)  

- Aantal gebruikers met meerdere Inge schreven mobiele apparaten  

- Polling planning voor mobiele apparaten en statistieken voor de duur van het inchecken van mobiele apparaten  


### <a name="microsoft-intune-troubleshooting"></a>Microsoft Intune probleem oplossing  

- Aantal en grootte van Apparaatinstellingen (wissen, buiten gebruik stellen, vergren delen), gebruiks gegevens en gegevens berichten die worden gerepliceerd naar Microsoft Intune  

- Aantal en de grootte van de status, status, inventaris, RDR, DDR, UDX, Tenant status, POL, LOG, CERT, CRP, Resync, CFD, RDO, BEX, ISM en nalevings berichten die worden gedownload van Microsoft Intune  

- Volledige en Delta statistieken voor gebruikers synchronisatie voor Microsoft Intune  


### <a name="on-premises-mobile-device-management-mdm"></a>On-premises Mobile Device Management (MDM)  

- Aantal Windows 10-bulkregistratiepakketten en -profielen  

- Statistieken over geslaagde/mislukte lokale MDM-toepassingsimplementaties  


### <a name="os-deployment"></a>Besturingssysteemimplementatie  

- Aantal opstartinstallatiekopieën, stuurprogramma's, stuurprogrammapakketten, distributiepunten met ingeschakelde multicast, distributiepunten voor PXE-functionaliteit en takenreeksen  

- Aantal opstart installatie kopieën per Configuration Manager-client versie  

- Aantal opstart installatie kopieën per Windows PE-versie  

- Aantal editie-upgrade beleid  

- Aantal hardware-id's dat is uitgesloten van PXE  

- Aantal implementaties van het besturings systeem op besturingssysteem versie  

- Aantal upgrades van het besturings systeem gedurende een periode  

- Aantal implementaties van taken reeksen met de optie voor het vooraf downloaden van inhoud  

- Aantallen van het gebruik van taken reeks stappen  

- Versie van Windows ADK geïnstalleerd  

- Aantal bewerkings taken voor de installatie kopie  

- ***[Nieuw]*** Aantal geïmporteerde machines  


### <a name="site-updates"></a>Site-updates  

- Versies van geïnstalleerde Configuration Manager hotfixes  


### <a name="software-updates"></a>Software-updates  

- Beschik bare en deadline Deltas die worden gebruikt in regels voor automatische implementatie  

- Gemiddeld en maximumaantal toewijzingen per update  

- Evaluatie van client-updates en scanplanningen  

- Classificaties gesynchroniseerd door het software-update punt  

- Statistieken over clusterpatching  

- Configuratie van updates voor Windows 10 Express  

- Configuraties die worden gebruikt voor actieve Windows 10-onderhouds plannen  

- Aantal geïmplementeerde Office 365-updates  

- Aantal gesynchroniseerde Stuur Programma's van micro soft Surface  

- Aantal updategroepen en toewijzingen  

- Aantal update pakketten en het maximale/minimale/gemiddelde aantal distributie punten dat is gericht op pakketten  

- Aantal updates dat is gemaakt en geïmplementeerd met System Center update Publisher  

- Aantal Windows Update voor bedrijfs beleid dat is gemaakt en geïmplementeerd  

- Cumulatieve statistieken van Windows Update voor bedrijfs configuraties  

- Aantal regels voor automatische implementatie dat is gekoppeld aan synchronisatie  

- Aantal regels voor automatische implementatie waarmee nieuwe updates worden gemaakt of waarmee updates worden toegevoegd aan een bestaande groep  

- Aantal regels voor automatische implementatie met meerdere implementaties  

- Aantal updategroepen en minimaal/maximaal/gemiddeld aantal updates per groep  

- Aantal updates en het percentage updates dat is geïmplementeerd, verlopen, vervangen, gedownload en gebruiksrecht overeenkomst bevat  

- Statistieken voor taak verdeling van software-update punten  

- Synchronisatieplanning voor software-updatepunten  

- Totaal/gemiddeld aantal verzamelingen met software-update-implementaties en het maximum/gemiddeld aantal geïmplementeerde updates  

- Foutcodes voor updatescans en het aantal computers  

- Versies van Windows 10-dashboardinhoud  

- Aantal abonnementen en het gebruik van Software-Update catalogus van derden  

- Telling van software-updates die zijn geïmplementeerd met en zonder inhoud  

- ***[Nieuw]*** Cumulatieve statistieken voor het aantal UUP-updates dat vereist is, geïmplementeerd, verlopen, vervangen en gedownload  

- ***[Nieuw]*** Gebruik van UUP-product categorieën  

- ***[Nieuw]*** Aantal clients waarop ten minste één update van UUP of UUP onderdeel is geïmplementeerd  

- ***[Nieuw]*** Belangrijkste UUP-fout codes en-telling van betrokken apparaten  


### <a name="sqlperformance-data"></a>SQL/prestatie gegevens  

- Configuratie en duur van site samenvatting  

- Aantal van de grootste databasetabellen  

- Operationele statistieken voor detectie (aantal gevonden objecten)  

- Detectie typen, ingeschakeld en plannen (volledig, incrementeel)  

- Informatie over de SQL AlwaysOn-replica, het gebruik en de integriteits status  

- Prestatie problemen voor het bijhouden van SQL-wijzigingen, de Bewaar periode en de status van automatisch opschonen  

- Bewaar periode voor het bijhouden van SQL-wijzigingen  

- Prestatie statistieken status en status bericht, inclusief meest voorkomende en meest dure bericht typen  

- ***[Nieuw]*** Statistieken van het beheer punt verkeer (totale aantal verzonden en ontvangen bytes per eind punt)  

- ***[Nieuw]*** Metingen voor prestatie meter items beheer punt  


### <a name="miscellaneous"></a>Diversen  

- Configuratie van het Data Warehouse-service punt met inbegrip van de synchronisatie planning en de gemiddelde tijd  

- Aantal scripts en uitvoerings statistieken  

- Aantal sites met Wake On LAN (WOL)  

- Statistieken over gebruik en prestaties rapporteren  

- Gebruiks statistieken voor gefaseerde implementaties  

- Aantal en voortgang van management Insights-items  

- Aantal crashes voor unieke niet-Configuration Manager processen op de site server en de hand tekening-ID van de Watson, indien beschikbaar  



##  <a name="level-3---full"></a><a name="bkmk_level3"></a> Niveau 3 - Volledig

Voor Configuration Manager versie 1810 bevat dit niveau de volgende gegevens:

- Informatie over de evaluatieplanning voor regels voor automatische implementatie  

- ATP-status samenvatting  

- Evaluatie van verzamelingen en vernieuwingsstatistieken  

- Statistieken over nalevings beleid met betrekking tot naleving en fouten  

- Instellingen voor naleving: SCEP-, VPN-, Wi-Fi-en nalevings beleid sjabloon configuratie Details  

- DCM-configuratie pakket voor Configuration Manager gebruik  

- Gedetailleerde installatie fouten voor client implementatie  

- Endpoint Protection status overzicht: inclusief het aantal beveiligde, risico-, onbekende en niet-ondersteunde clients  

- Endpoint Protection-beleidsconfiguratie  

- Lijst met processen die zijn geconfigureerd met installatie gedrag voor toepassingen  

- Minimaal/maximaal/gemiddeld aantal uren sinds de vorige software-updatescan  

- Minimaal/maximaal/gemiddeld aantal inactieve clients in verzamelingen voor software-update-implementaties  

- Minimaal/maximaal/gemiddeld aantal software-updates per pakket  

- Statistieken voor de implementatie van MSI-product code  

- Algemene naleving van software-update-implementaties  

- Aantal groepen met verlopen software-updates  

- Aantal fouten en foutcodes voor software-update-implementaties  

- Informatie over de implementatie van software-updates: percentage implementaties die zijn gericht op client versus UTC-tijd, vereist versus optioneel versus stil en onderdrukking opnieuw opstarten  

- Software-update producten gesynchroniseerd door software-update punt  

- Percentage van geslaagde software-updatescans  

- Top 50 Cpu's in de omgeving  

- Type Exchange Active Sync (EAS) beleid voor voorwaardelijke toegang (blok of quarantaine) voor apparaten die Microsoft Intune beheert  

- Microsoft Store voor details van zakelijke toepassing: niet-geaggregeerde lijst met gesynchroniseerde toepassingen, waaronder AppID, online status of offline status en totaal aantal aangeschafte licenties  

- ***[Nieuw]*** Aantal clients dat is gepusht met de optie voor het niet toestaan van terugval naar NTLM  
