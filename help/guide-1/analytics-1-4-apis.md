---
title: Einstellung der Adobe Analytics 1.4-API
description: Die Adobe Analytics 1.4-API- und WSSE-Authentifizierung haben am 31. August 2026 das Ende ihrer Lebensdauer erreicht. Erfahren Sie, was betroffen ist und wie Sie zu den Analytics 2.0-APIs migrieren.
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%
---
# Einstellung der Adobe Analytics 1.4-API

Zum **(31. August**) hat Adobe die Adobe Analytics 1.4-API- und WSSE-Authentifizierung eingestellt. Alle Endpunkte, die diese Version der API verwenden, sind nicht mehr zugänglich, und darauf aufbauende Integrationen funktionieren nicht mehr.

Die Adobe Analytics 1.4-APIs bieten eine breite Palette von Aktionen, z. B. Berichte, Klassifizierungen, Daten-Feeds, Segmente, berechnete Metriken, Datenquellen und Report Suite-Konfigurationen. Sie wurden durch die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0) ersetzt, mit denen Sie fast alle in der Adobe Analytics-Benutzeroberfläche verfügbaren Aktionen durchführen können, einschließlich der Berichterstellung und Verwaltung von Komponenten wie Segmenten und berechneten Metriken. Wenn Sie über eine Integration verfügen, die noch aktualisiert werden muss, befolgen Sie die Anleitung unter [Migrieren zu Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration).

## Was das Ende der Lebensdauer erreicht hat

Dieses Ende des Lebenszyklus wirkt sich direkt auf die folgenden 1.4-API-Funktionen aus. Migrieren Sie jeden betroffenen Workflow in die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0):

* Reporting (einschließlich Data Warehouse-, Echtzeit-, Pfad- und Zusammenfassungsberichten)
* Report Suite-Konfiguration und -Administration
* Klassifizierungen
* Segmente
* Berechnete Metriken
* Datenquellen
* Daten-Feeds
* Lesezeichen und Methoden des Unternehmens (Endpunkt)

Außerdem wird die **Adobe Analytics WSSE-Authentifizierung** eingestellt (siehe [WSSE-Authentifizierung](#wsse-authentication) unten).

>[!IMPORTANT]
>
>Dieses Ende der Nutzungsdauer wirkt sich *nicht* auf die Datenerfassung aus. Tagging-Lösungen wie Tags (früher Adobe Launch), die Web-SDK und AppMeasurement sind davon nicht betroffen. Die [Dateneinfüge-API](#data-insertion-api) wird ebenfalls *nicht* eingestellt. Wenn Sie jedoch die 1.4-Datenquellen- oder Klassifizierungs-APIs zur Verbesserung Ihrer Daten verwenden, müssen Sie diese Workflows zu den Adobe Analytics 2.0-APIs migrieren.

## WSSE-Authentifizierung

Die WSSE-Authentifizierung ist ein veraltetes Authentifizierungsprotokoll, das von den Analytics 1.4-APIs unterstützt wurde. Sie wurde durch die OAuth-basierten Authentifizierungsoptionen ersetzt, die in der [Adobe Developer Console bereitgestellt &#x200B;](https://developer.adobe.com/console/home). Projekte, die die WSSE-Authentifizierung verwenden, müssen ihre Anmeldeinformationen auf die in der Adobe Developer Console bereitgestellten aktualisieren.

Um zu migrieren, melden Sie sich bei der [Adobe Developer Console an &#x200B;](https://developer.adobe.com/console/home) erstellen Sie ein Projekt für Ihre Analytics 2.0-API-Integration. Wählen Sie entweder die Authentifizierungsmethode **OAuth-** oder **OAuth-Server-zu-Server** aus.

## Dateneinfüge-API

Die Dateneinfüge-**ist** Teil dieses End-of-Life. Die Dokumentation wurde auf die Site der [Adobe Analytics-Datenerfassungs](https://developer.adobe.com/analytics-collection-apis/)APIs verschoben, zusammen mit den anderen serverseitigen Erfassungsmethoden:

* [Dateneinfüge-](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/): Senden Sie Ereignisdaten einen Treffer nach dem anderen, als Abfragezeichenfolge (Bildanforderung) oder als XML-`POST`.
* [Bulk Data Insertion-](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/): Laden Sie Batches von Server-Aufrufdaten als Dateien hoch. Adobe empfiehlt die Verwendung der Bulk Data Insertion-API für neue Server-seitige Implementierungen.

## Häufig gestellte Fragen

+++Hat dies Auswirkungen auf meine bestehenden Adobe Developer-Projekte für die Analytics-APIs?

Alle vorhandenen Projekte, die die Analytics 1.4-APIs verwenden, sind betroffen. Diese Integrationen müssen in die [Adobe Analytics 2.0-APIs migriert &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/).

+++

+++Ich habe meine Adobe-Anmeldedaten für ein anderes Produkt oder eine andere Anwendung freigegeben, das bzw. die die Analytics-APIs verwendet. Sind sie betroffen?

Wenn dieses Produkt oder diese Anwendung Ihre WSSE-Anmeldeinformationen verwendet oder die Analytics 1.4-APIs aufruft, ist es betroffen und muss migriert werden. Wenden Sie sich an den Produkt- oder Anwendungsanbieter, um Details zu seinen Migrationsplänen und zum Zeitplan zu erhalten.

+++

+++Wie kann ich feststellen, welche API mein Projekt verwendet?

Die Basis-URL, die Ihr Projekt aufruft, bestimmt, welche API-Version es verwendet. Die Adobe Analytics 1.4-APIs verwendeten die folgenden Basis-URLs:

* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

Die [Adobe Analytics 2.0-APIs](https://developer.adobe.com/analytics-apis/docs/2.0/) verwenden die folgende Basis-URL:

* `https://analytics.adobe.io`

Wenn eines Ihrer API-Projekte `api*.omniture.com` aufruft, verwendet es die nicht mehr unterstützten Adobe Analytics 1.4-APIs und muss zu den 2.0-APIs migrieren.

+++

+++Hat dieses Ende der Nutzungsdauer Auswirkungen auf die Datenerfassung?

Nein. Das Ende der Nutzungsdauer wirkt sich **nicht** auf die direkte Datenerfassung aus, z. B. Tags, die Web-SDK, AppMeasurement oder die Data Insertion-API. Wenn Sie jedoch die 1.4-Datenquellen- oder Klassifizierungs-APIs zur Verbesserung Ihrer Daten verwenden, müssen Sie diese Workflows zu den Adobe Analytics 2.0-APIs migrieren.

+++

Wenn Sie weitere Fragen zu diesem End of Life haben, die auf dieser Seite nicht beantwortet werden, wenden Sie sich an Ihr Adobe Account Team.
