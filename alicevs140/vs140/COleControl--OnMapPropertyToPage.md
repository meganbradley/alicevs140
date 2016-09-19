---
title: "COleControl::OnMapPropertyToPage"
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
ms.assetid: 1a42df07-37c6-4c6c-b2c4-86a288c001f4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnMapPropertyToPage
Called by the framework to obtain the class ID of a property page that implements editing of the specified property.  
  
## Syntax  
  
```  
  
      virtual BOOL OnMapPropertyToPage(  
   DISPID dispid,  
   LPCLSID lpclsid,  
   BOOL* pbPageOptional   
);  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of a property of the control.  
  
 `lpclsid`  
 Pointer to a **CLSID** structure through which a class ID will be returned.  
  
 *pbPageOptional*  
 Returns an indicator of whether use of the specified property page is optional.  
  
## Return Value  
 Nonzero if a class ID has been returned in `lpclsid`; otherwise 0.  
  
## Remarks  
 Override this function to provide a way to invoke your control's property pages from the container's property browser.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnGetDisplayString](../vs140/COleControl--OnGetDisplayString.md)