---
title: "DECLARE_EVENT_MAP"
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
ms.assetid: cd25283d-ea94-40f3-91df-89c84a328ed0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_EVENT_MAP
Each `COleControl`-derived class in your program can provide an event map to specify the events your control will fire.  
  
## Syntax  
  
```  
  
DECLARE_EVENT_MAP( )  
```  
  
## Remarks  
 Use the `DECLARE_EVENT_MAP` macro at the end of your class declaration. Then, in the .cpp file that defines the member functions for the class, use the `BEGIN_EVENT_MAP` macro, macro entries for each of the control's events, and the `END_EVENT_MAP` macro to declare the end of the event list.  
  
 For more information on event maps, see the article [ActiveX Controls: Events](../vs140/MFC-ActiveX-Controls--Events.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_EVENT_MAP](../vs140/BEGIN_EVENT_MAP.md)   
 [END_EVENT_MAP](../vs140/END_EVENT_MAP.md)   
 [EVENT_CUSTOM](../vs140/EVENT_CUSTOM.md)   
 [EVENT_CUSTOM_ID](../vs140/EVENT_CUSTOM_ID.md)