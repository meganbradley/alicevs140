---
title: "COleControlContainer::CheckRadioButton"
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
ms.assetid: f177da15-19d1-488b-9fef-1fe4478e010f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::CheckRadioButton
Selects a specified radio button in a group and clears the remaining buttons in the group.  
  
## Syntax  
  
```  
  
      virtual void CheckRadioButton(  
   int nIDFirstButton,  
   int nIDLastButton,  
   int nIDCheckButton   
);  
```  
  
#### Parameters  
 `nIDFirstButton`  
 Specifies the identifier of the first radio button in the group.  
  
 `nIDLastButton`  
 Specifies the identifier of the last radio button in the group.  
  
 `nIDCheckButton`  
 Specifies the identifier of the radio button to be checked.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)