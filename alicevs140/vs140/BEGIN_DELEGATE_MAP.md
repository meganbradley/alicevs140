---
title: "BEGIN_DELEGATE_MAP"
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
ms.assetid: cdf4341f-1c71-40bb-abc8-fc2c35b8247d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_DELEGATE_MAP
Begins a delegate map.  
  
## Syntax  
  
```  
BEGIN_DELEGATE_MAP(  
   CLASS  
);  
```  
  
#### Parameters  
 `CLASS`  
 The class in which the managed control is hosted.  
  
## Remarks  
 This macro marks the beginning of a list of delegate entries, which compose a delegate map. For an example of how this macro is used, see [EVENT_DELEGATE_ENTRY](../vs140/EVENT_DELEGATE_ENTRY.md).  
  
## Requirements  
 **Header:** msclr\event.h  
  
## See Also  
 [MAKE_DELEGATE](../vs140/MAKE_DELEGATE.md)   
 [EVENT_DELEGATE_ENTRY](../vs140/EVENT_DELEGATE_ENTRY.md)   
 [END_DELEGATE_MAP](../vs140/END_DELEGATE_MAP.md)   
 [How To: Sink Windows Forms Events from Native C++ Classes](../Topic/How%20to:%20Sink%20Windows%20Forms%20Events%20from%20Native%20C++%20Classes.md)