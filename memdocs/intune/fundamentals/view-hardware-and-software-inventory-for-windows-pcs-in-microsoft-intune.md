---
title: Hardware- en software-inventaris voor Windows-computers weergeven
titleSuffix: Microsoft Intune
description: Hoe u hardware- en software-informatie kunt weergeven over Windows-desktops die u beheert als pc's met de Intune-softwareclient.
keywords: ''
author: dougeby
ms.author: dougeby
manager: dougeby
ms.date: 06/26/2019
ms.topic: archived
ms.service: microsoft-intune
ms.subservice: fundamentals
ms.localizationpriority: medium
ms.technology: ''
ms.assetid: 3c10f4c9-520b-4864-92fc-a45a9f640ad4
ms.reviewer: owenyen
ms.suite: ems
search.appverid: MET150
ms.custom: intune-classic-keep
ms.collection: M365-identity-device-management
ms.openlocfilehash: 9e2d5e3f1e5839040c3ffd2229c34f3063a3ce87
ms.sourcegitcommit: 7f17d6eb9dd41b031a6af4148863d2ffc4f49551
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "79354695"
---
# <a name="view-hardware-and-software-inventory-for-windows-pcs"></a>Hardware- en software-inventaris voor Windows-computers weergeven

[!INCLUDE [classic-portal](../includes/classic-portal.md)]

> [!NOTE]
> De informatie in dit onderwerp geldt alleen voor Windows-desktops die u als pc's beheert met behulp van de Intune-softwareclient. Zie [Apparaatdetails weergeven in Intune](../remote-actions/device-inventory.md) als u de inventarisatie wilt weergeven voor Windows-pc's die zijn ingeschreven als mobiele apparaten.

Intune verzamelt gedetailleerde informatie over de hardware en software voor desktops die u als pc's beheert met behulp van de Intune-softwareclient. Gebruik de informatie in de volgende procedures om het volgende te leren maken:

- Een rapport met een overzicht van de informatie over de hardwaremogelijkheden van de pc's die u beheert.

- Een rapport met een overzicht van de software die op elke pc is geïnstalleerd.

- De inventarisatie van een pc vernieuwen om ervoor te zorgen dat de gegevens in het rapport actueel zijn.

## <a name="to-display-information-about-pcs-you-manage"></a>Informatie weergeven over de pc's die u beheert

1. Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com/) de optie **Rapporten** &gt; **Computerinventarisatierapporten**.

2. Op de pagina **Nieuw rapport maken** accepteert u de standaardwaarden of past u deze aan om de resultaten te filteren die door het rapport worden geretourneerd. U kunt bijvoorbeeld selecteren dat alleen pc's met Windows 8.1 worden weergegeven in het rapport.

3. Klik op **Rapport weergeven** om het **Computerinventarisatierapport** te openen in een nieuw venster.

    U kunt het rapport rangschikken op een kolom, zoals **Naam**, **Chassistype** of **Fabrikant**, door te klikken op de bijbehorende kolomkop.

## <a name="to-display-software-installed-on-pcs-you-manage"></a>Software weergeven die is geïnstalleerd op pc's die u beheert

1. Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com/) de optie **Rapporten** &gt; **Rapporten met gedetecteerde software**.

2. Op de pagina **Nieuw rapport maken** accepteert u de standaardwaarden of past u deze aan om de resultaten te filteren die door het rapport worden geretourneerd. U kunt bijvoorbeeld selecteren dat alleen de software die is uitgegeven door Microsoft, wordt weergegeven in het rapport.

3. Klik op **Rapport weergeven** om het **Rapport met gedetecteerde software** te openen in een nieuw venster.

    U kunt het rapport rangschikken op een kolom zoals **Naam**, **Uitgever** of **Categorie** door te klikken op de bijbehorende kolomkop. U kunt de updates in de lijst uitbreiden om meer details weer te geven (zoals de pc's waarop deze update is geïnstalleerd) door de richtingspijl naast het item te kiezen.

## <a name="to-refresh-computer-inventory-to-ensure-it-is-current"></a>Computerinventarisatie vernieuwen zodat deze actueel is

1. Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com/) de optie **Groepen** &gt; **Alle apparaten** (of een andere groep die de pc bevat waarvoor u de inventarisatie wilt vernieuwen).

2. Selecteer een pc of houd **Ctrl** ingedrukt om meerdere pc's te selecteren.

3. Kies op de taakbalk **Externe taken** &gt; **Inventarisatie vernieuwen**.

4. Als u de status van de taak wilt weergeven, klikt u op **Externe taken** in de rechterbenedenhoek van de pagina.

    Het dialoogvenster **Taakstatus** wordt weergegeven met huidige externe taken, taakstatus, apparaatnaam en gerapporteerde fouten, en het bevat een koppeling naar informatie voor probleemoplossing.

## <a name="see-also"></a>Zie ook

[Algemene beheertaken voor Windows-pc's met de Intune-softwareclient](common-windows-pc-management-tasks-with-the-microsoft-intune-computer-client.md)
