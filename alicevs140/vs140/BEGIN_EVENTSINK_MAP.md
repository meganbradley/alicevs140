---
title: "BEGIN_EVENTSINK_MAP"
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
ms.assetid: ccc7be4d-ed34-459b-adbc-14254f5916d9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_EVENTSINK_MAP
Begins the definition of your event sink map.  
  
## Syntax  
  
```  
  
BEGIN_EVENTSINK_MAP(  
theClass  
,   
baseClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the control class whose event sink map this is.  
  
 `baseClass`  
 Specifies the name of the base class of `theClass`.  
  
## Remarks  
 In the implementation (.cpp) file that defines the member functions for your class, start the event sink map with the `BEGIN_EVENTSINK_MAP` macro, then add macro entries for each event to be notified of, and complete the event sink map with the `END_EVENTSINK_MAP` macro.  
  
 For more information on event sink maps and OLE control containers, see the article [ActiveX Control Containers](../vs140/ActiveX-Control-Containers.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_EVENTSINK_MAP](../vs140/DECLARE_EVENTSINK_MAP.md)   
 [END_EVENTSINK_MAP](../vs140/END_EVENTSINK_MAP.md)