---
title: "COleControlContainer::AttachControlSite"
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
ms.assetid: 90a4f70b-0cab-496c-8198-f0aef1ff64f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::AttachControlSite
Called by the framework to create and attach a control site.  
  
## Syntax  
  
```  
  
      virtual void AttachControlSite(  
   CWnd* pWnd,  
   UINT nIDC = 0   
);  
void AttachControlSite(  
   CWnd* pWnd,  
   UINT nIDC = 0   
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to a `CWnd` object.  
  
 `nIDC`  
 The ID of the control to be attached.  
  
## Remarks  
 Override this function if you want to customize this process.  
  
> [!NOTE]
>  Use the first form of this function if you are statically linking to the MFC library. Use the second form if you are dynamically linking to the MFC library.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)