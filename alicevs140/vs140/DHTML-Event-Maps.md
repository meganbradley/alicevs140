---
title: "DHTML Event Maps"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a2c8ae7-7216-4a5e-bc60-6b98695be0c6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTML Event Maps
The following macros can be used to handle DHTML events.  
  
## DHTML Event Map Macros  
 The following macros can be used to handle DHTML events in [CDHtmlDialog](../vs140/CDHtmlDialog-Class.md)-derived classes.  
  
|||  
|-|-|  
|[BEGIN_DHTML_EVENT_MAP](../vs140/BEGIN_DHTML_EVENT_MAP.md)|Marks the start of the DHTML event map.|  
|[BEGIN_DHTML_EVENT_MAP_INLINE](../vs140/BEGIN_DHTML_EVENT_MAP_INLINE.md)|Marks the start of the DHTML event map.|  
|[DECLARE_DHTML_EVENT_MAP](../vs140/DECLARE_DHTML_EVENT_MAP.md)|Declares the DHTML event map.|  
|[DHTML_EVENT](../vs140/DHTML_EVENT.md)|Used to handle an event at the document level for a single HTML element.|  
|[DHTML_EVENT_AXCONTROL](../vs140/DHTML_EVENT_AXCONTROL.md)|Used to handle an event fired by an ActiveX control.|  
|[DHTML_EVENT_CLASS](../vs140/DHTML_EVENT_CLASS.md)|Used to handle an event at the document level for all HTML elements with a particular CSS class.|  
|[DHTML_EVENT_ELEMENT](../vs140/DHTML_EVENT_ELEMENT.md)|Used to handle an event at the element level.|  
|[DHTML_EVENT_ONAFTERUPDATE](../vs140/DHTML_EVENT_ONAFTERUPDATE.md)|Used to handle the **onafterupdate** event from an HTML element.|  
|[DHTML_EVENT_ONBEFOREUPDATE](../vs140/DHTML_EVENT_ONBEFOREUPDATE.md)|Used to handle the **onbeforeupdate** event from an HTML element.|  
|[DHTML_EVENT_ONBLUR](../vs140/DHTML_EVENT_ONBLUR.md)|Used to handle the **onblur** event from an HTML element.|  
|[DHTML_EVENT_ONCHANGE](../vs140/DHTML_EVENT_ONCHANGE.md)|Used to handle the `onchange` event from an HTML element.|  
|[DHTML_EVENT_ONCLICK](../vs140/DHTML_EVENT_ONCLICK.md)|Used to handle the **onclick** event from an HTML element.|  
|[DHTML_EVENT_ONDATAAVAILABLE](../vs140/DHTML_EVENT_ONDATAAVAILABLE.md)|Used to handle the **ondataavailable** event from an HTML element.|  
|[DHTML_EVENT_ONDATASETCHANGED](../vs140/DHTML_EVENT_ONDATASETCHANGED.md)|Used to handle the **ondatasetchanged** event from an HTML element.|  
|[DHTML_EVENT_ONDATASETCOMPLETE](../vs140/DHTML_EVENT_ONDATASETCOMPLETE.md)|Used to handle the **ondatasetcomplete** event from an HTML element.|  
|[DHTML_EVENT_ONDBLCLICK](../vs140/DHTML_EVENT_ONDBLCLICK.md)|Used to handle the **ondblclick** event from an HTML element.|  
|[DHTML_EVENT_ONDRAGSTART](../vs140/DHTML_EVENT_ONDRAGSTART.md)|Used to handle the **ondragstart** event from an HTML element.|  
|[DHTML_EVENT_ONERRORUPDATE](../vs140/DHTML_EVENT_ONERRORUPDATE.md)|Used to handle the **onerrorupdate** event from an HTML element.|  
|[DHTML_EVENT_ONFILTERCHANGE](../vs140/DHTML_EVENT_ONFILTERCHANGE.md)|Used to handle the **onfilterchange** event from an HTML element.|  
|[DHTML_EVENT_ONFOCUS](../vs140/DHTML_EVENT_ONFOCUS.md)|Used to handle the **onfocus** event from an HTML element.|  
|[DHTML_EVENT_ONHELP](../vs140/DHTML_EVENT_ONHELP.md)|Used to handle the `onhelp` event from an HTML element.|  
|[DHTML_EVENT_ONKEYDOWN](../vs140/DHTML_EVENT_ONKEYDOWN.md)|Used to handle the **onkeydown** event from an HTML element.|  
|[DHTML_EVENT_ONKEYPRESS](../vs140/DHTML_EVENT_ONKEYPRESS.md)|Used to handle the **onkeypress** event from an HTML element.|  
|[DHTML_EVENT_ONKEYUP](../vs140/DHTML_EVENT_ONKEYUP.md)|Used to handle the **onkeyup** event from an HTML element.|  
|[DHTML_EVENT_ONMOUSEDOWN](../vs140/DHTML_EVENT_ONMOUSEDOWN.md)|Used to handle the **onmousedown** event from an HTML element.|  
|[DHTML_EVENT_ONMOUSEMOVE](../vs140/DHTML_EVENT_ONMOUSEMOVE.md)|Used to handle the `onmousemove` event from an HTML element.|  
|[DHTML_EVENT_ONMOUSEOUT](../vs140/DHTML_EVENT_ONMOUSEOUT.md)|Used to handle the **onmouseout** event from an HTML element.|  
|[DHTML_EVENT_ONMOUSEOVER](../vs140/DHTML_EVENT_ONMOUSEOVER.md)|Used to handle the **onmouseover** event from an HTML element.|  
|[DHTML_EVENT_ONMOUSEUP](../vs140/DHTML_EVENT_ONMOUSEUP.md)|Used to handle the **onmouseup** event from an HTML element.|  
|[DHTML_EVENT_ONRESIZE](../vs140/DHTML_EVENT_ONRESIZE.md)|Used to handle the **onresize** event from an HTML element.|  
|[DHTML_EVENT_ONROWENTER](../vs140/DHTML_EVENT_ONROWENTER.md)|Used to handle the **onrowenter** event from an HTML element.|  
|[DHTML_EVENT_ONROWEXIT](../vs140/DHTML_EVENT_ONROWEXIT.md)|Used to handle the **onrowexit** event from an HTML element.|  
|[DHTML_EVENT_ONSELECTSTART](../vs140/DHTML_EVENT_ONSELECTSTART.md)|Used to handle the **onselectstart** event from an HTML element.|  
|[DHTML_EVENT_TAG](../vs140/DHTML_EVENT_TAG.md)|Used to handle an event at the document level for all elements with a particular HTML tag.|  
|[END_DHTML_EVENT_MAP](../vs140/END_DHTML_EVENT_MAP.md)|Marks the end of the DHTML event map.|  
  
## URL Event Map Macros  
 The following macros can be used to handle DHTML events in [CMultiPageDHtmlDialog](../vs140/CMultiPageDHtmlDialog-Class.md)-derived classes.  
  
|||  
|-|-|  
|[BEGIN_DHTML_URL_EVENT_MAP](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md)|Marks the start of the multipage DHTML and URL event map.|  
|[BEGIN_EMBED_DHTML_EVENT_MAP](../vs140/BEGIN_EMBED_DHTML_EVENT_MAP.md)|Marks the start of an embedded DHTML event map.|  
|[BEGIN_URL_ENTRIES](../vs140/BEGIN_URL_ENTRIES.md)|Marks the start of a URL event entry map.|  
|[DECLARE_DHTML_URL_EVENT_MAP](../vs140/DECLARE_DHTML_URL_EVENT_MAP.md)|Declares the multipage DHTML and URL event map.|  
|[END_DHTML_URL_EVENT_MAP](../vs140/END_DHTML_URL_EVENT_MAP.md)|Marks the end of the multipage DHTML and URL event map.|  
|[END_EMBED_DHTML_EVENT_MAP](../vs140/END_EMBED_DHTML_EVENT_MAP.md)|Marks the end of an embedded DHTML event map.|  
|[END_URL_ENTRIES](../vs140/END_URL_ENTRIES.md)|Marks the end of a URL event entry map.|  
|[URL_EVENT_ENTRY](../vs140/URL_EVENT_ENTRY.md)|Maps a URL or HTML resource to a page in a multipage dialog.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)