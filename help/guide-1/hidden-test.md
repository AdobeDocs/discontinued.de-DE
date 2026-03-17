---
title: Ausgeblendeter Test
description: Dies ist ein versteckter Test
hide: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: 0d0c957441babe95bad242da4b1249f8019615d1
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 8%

---

# Ausgeblendeter Test

&#x200B;17. März 2026 - `hold: true` ist aus.

Testen eines neuen Schlüssels

Dies ist ein versteckter Test. Ich füge dieses `[` hinzu, um sicherzustellen, dass es beim v2-Rendering funktioniert!

## In neuem Tab öffnen {#section_92882928}

`[See What's new](auditor.md){target="_blank"} `

[In derselben Registerkarte öffnen](auditor.md)

[Neue Registerkarte mit Leerzeichen in Anführungszeichen](auditor.md){target="_blank"} 

[Neue Registerkarte mit Anker](auditor.md){target=„_blank}

[Neue Registerkarte ohne Leerzeichen mit Anführungszeichen](auditor.md){target="_blank"}

[Neue Registerkarte mit Leerzeichen ohne Anführungszeichen](auditor.md){target=_blank} 

[Neue Registerkarte ohne Leerzeichen ohne Anführungszeichen](auditor.md){target=_blank}

[Neue Registerkarte mit Deep-Link](commerce-channels.md#channel-manager-extension){target="_blank"}

[Neue Registerkarte mit Deep-Link verankern](https://experienceleague.adobe.com/de/docs/analytics/analyze/home#key-analytics-resources){target="_blank"}

[Neue Registerkarte mit externem Link](https://www.adobe.com){target="_blank"}

[Root-Link für neue Registerkarte](/help/guide-1/auditor.md){target="_blank"}


<table>
  <tr>
    <th>Mit Anführungszeichen</a></th>
    <th>Ohne Anführungszeichen</th>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com" target="_blank">Neue Registerkarte in Adobe</a></td>
    <td><a href="https://www.adobe.com" target="_blank">Neue Registerkarte in Adobe</td>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com">Adobe - keine neue Registerkarte</a></td>
    <td><a href="https://www.adobe.com">Adobe - keine neue Registerkarte</td>
  </tr>
</table>

## Kommentartest

&#x200B;18. November 2025

<!-- 
## Comment with basic text

This is a new line.

Second new line. 
-->


Kommentar unten. Wenn dies das letzte ist, was Sie in diesem Artikel sehen, ist es aufgrund der Kommentarsyntax.

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

<!-- 
## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. 
-->

Diese Zeile ist nach dem Kommentar.

## Videotest

### Einfaches Video ohne Transkript - sollte Transkript anzeigen, da metadata.md nach unten durchsickert

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true)

### Mit auf „true“ festgelegtem Transkript

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=true}

### Wenn das Transkript auf „false“ gesetzt ist, sollte das Videotranskript nicht angezeigt werden.

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=false}

## Relative Links

* [Überblick](overview.md)
* [Suchen und Bewerben](search-promote.md)
* [Social](social.md)

## Expliziter Deep-Link

[Zusätzliche Übersicht (Stamm)](/help/guide-1/overview.md#additional-products)

[Zusätzliche Übersicht](overview.md#additional-products)

## Hover-Test {#this-is-a-heading-anchor}

Kein Hover-Text

```
![alt text](assets/maui-flip.jpg)
```

![Alternativtext](assets/maui-flip.jpg)


Ja Hover-Text

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![Alt-Text](assets/maui-flip.jpg "Hover-Text")

## Folie

Syntax:

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

Gerendert:

<!--
>[!SLIDE](analyze-project)
-->

Bob: Entfernen Sie den Folienkommentar, sobald Sie das Thema loc-Sache testen.
