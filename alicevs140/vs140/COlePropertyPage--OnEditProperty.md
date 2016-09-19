---
title: "COlePropertyPage::OnEditProperty"
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
ms.assetid: e3f1145b-272f-48e0-b910-7baa2348a5ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::OnEditProperty
The framework calls this function when a specific property is to be edited.  
  
## Syntax  
  
```  
  
      virtual BOOL OnEditProperty(  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `dispid`  
 Dispatch ID of the property being edited.  
  
## Return Value  
 The default implementation returns **FALSE**. Overrides of this function should return **TRUE**.  
  
## Remarks  
 You can override it to set the focus to the appropriate control on the page. The default implementation does nothing and returns **FALSE**.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)