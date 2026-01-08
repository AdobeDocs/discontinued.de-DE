---
keywords: Device-graph;Ende der Lebensdauer
title: Gerätediagramm
description: Erfahren Sie mehr über die End-of-Life-Pläne für das Gerätediagramm.
source-git-commit: c7264d94e52fb3efad7d59edd1b73f805a9a00f6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Ende der Lebensdauer für Gerätediagramm

>[!WARNING]
>
>Das Gerätediagramm in der geräteübergreifenden Analyse ist ab dem 31. **2025 nicht mehr**. Wechseln Sie alle aktuellen für Gerätediagramme aktivierten Virtual Report Suites in die [feldbasierte Methode](https://experienceleague.adobe.com/de/docs/analytics/components/cda/field-based-stitching).
>

Die geräteübergreifende Analyse verwendete das private Diagramm nicht, um Daten zusammenzufügen. Das private Diagramm ist ein Repository mit gehashten Geräte-IDs, das speziell für Ihre Organisation gilt. Die geräteübergreifende Analyse kommuniziert regelmäßig mit dem Gerätediagramm, um Geräte miteinander zu verknüpfen.

## Für das Gerätediagramm spezifische Voraussetzungen

Wenn Sie die geräteübergreifende Analyse mit der Methode „Device Graph“ implementieren wollten, waren die folgenden Schritte erforderlich.

>[!WARNING]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, kann die geräteübergreifende Analyse nicht aktiviert werden oder es können beim Zusammenfügen von Daten schlechte Ergebnisse erzielt werden.
>

* Ihr Unternehmen muss das private Diagramm [Adobe Experience Platform Identity Service verwenden](https://business.adobe.com/de/products/experience-platform/identity-service.html). Siehe auch [Startseite](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de) im Identity Service-Benutzerhandbuch.
* Ihre Implementierung muss die neueste Version des Experience Cloud ID-Service (ECID) verwenden. Siehe die [Startseite](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) im Benutzerhandbuch für den ID-Service. Bei den meisten Implementierungen mit [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de) in Adobe Experience Platform ist der ID-Service wahrscheinlich bereits bereitgestellt.
* Ihre Implementierung muss die `setCustomerIDs` (oder das SDK-Äquivalent) aufrufen, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, falls sie verwendet werden. Siehe [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html?lang=de) im ID-Service-Benutzerhandbuch.

## Für das Gerätediagramm spezifische Einschränkungen

* Legacy-Analytics-IDs werden nicht unterstützt. Nur Besucherinnen und Besucher mit Experience Cloud IDs werden zugeordnet.
* Wenn Ihr Unternehmen ein privates Diagramm verwendet, dauert es bis zu 24 Stunden, bis neue Geräte zugeordnet werden.
* Gerätediagramme von Drittanbietern werden nicht unterstützt.
