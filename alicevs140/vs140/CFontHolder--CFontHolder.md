---
title: "CFontHolder::CFontHolder"
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
ms.topic: reference
ms.assetid: 72cae07c-55bb-4666-8f9b-33fb82135746
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontHolder::CFontHolder
Constructs a `CFontHolder` object.  
  
## Syntax  
  
```  
  
      explicit CFontHolder(  
   LPPROPERTYNOTIFYSINK pNotify   
);  
```  
  
#### Parameters  
 *pNotify*  
 Pointer to the font's `IPropertyNotifySink` interface.  
  
## Remarks  
 You must call `InitializeFont` to initialize the resulting object before using it.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CFontHolder Class](../vs140/CFontHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontHolder::InitializeFont](../vs140/CFontHolder--InitializeFont.md)