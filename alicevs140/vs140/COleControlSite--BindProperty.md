---
title: "COleControlSite::BindProperty"
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
ms.assetid: 2f29a3fa-6dfb-4f37-b9ac-df61d4703a7d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::BindProperty
Binds the calling object's simple bound property, as marked in the type library, to the underlying cursor that is defined by the DataSource, UserName, Password, and SQL properties of the data-source control.  
  
## Syntax  
  
```  
  
      virtual void BindProperty(  
   DISPID dwDispId,  
   CWnd* pWndDSC   
);  
```  
  
#### Parameters  
 *dwDispId*  
 Specifies the **DISPID** of a property on a data-bound control that is to be bound to a data-source control.  
  
 `pWndDSC`  
 A pointer to the `CWnd`-derived object that hosts the data-source control to which the property will be bound.  
  
## Remarks  
 The `CWnd` object on which you call this function must be a data-bound control.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::BindDefaultProperty](../vs140/COleControlSite--BindDefaultProperty.md)