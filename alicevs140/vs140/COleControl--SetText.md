---
title: "COleControl::SetText"
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
ms.assetid: a1c7ecee-a274-435d-b967-ca4d5d2388c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetText
Sets the value of your control's stock Caption or Text property.  
  
## Syntax  
  
```  
  
      void SetText(  
   LPCTSTR pszText   
);  
```  
  
#### Parameters  
 `pszText`  
 A pointer to a character string.  
  
## Remarks  
 Note that the stock Caption and Text properties are both mapped to the same value. This means that any changes made to either property will automatically change both properties. In general, a control should support either the stock Caption or Text property, but not both.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetText](../vs140/COleControl--GetText.md)   
 [COleControl::InternalGetText](../vs140/COleControl--InternalGetText.md)   
 [COleControl::OnTextChanged](../vs140/COleControl--OnTextChanged.md)