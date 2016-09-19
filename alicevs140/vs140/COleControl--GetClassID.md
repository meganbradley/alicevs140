---
title: "COleControl::GetClassID"
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
ms.assetid: e86ab91f-88e8-4942-bb68-b25db31ac771
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetClassID
Called by the framework to retrieve the OLE class ID of the control.  
  
## Syntax  
  
```  
  
      virtual HRESULT GetClassID(  
   LPCLSID pclsid   
) = 0;  
```  
  
#### Parameters  
 *pclsid*  
 Pointer to the location of the class ID.  
  
## Return Value  
 Nonzero if the call was not successful; otherwise 0.  
  
## Remarks  
 Usually implemented by the [IMPLEMENT_OLECREATE_EX](../vs140/IMPLEMENT_OLECREATE_EX.md) macro.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)