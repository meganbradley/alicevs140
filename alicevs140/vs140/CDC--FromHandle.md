---
title: "CDC::FromHandle"
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
ms.assetid: ced3d088-bf98-4f33-880e-00abfeb5d6e9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::FromHandle
Returns a pointer to a `CDC` object when given a handle to a device context.  
  
## Syntax  
  
```  
  
      static CDC* PASCAL FromHandle(  
   HDC hDC   
);  
```  
  
#### Parameters  
 `hDC`  
 Contains a handle to a Windows device context.  
  
## Return Value  
 The pointer may be temporary and should not be stored beyond immediate use.  
  
## Remarks  
 If a `CDC` object is not attached to the handle, a temporary `CDC` object is created and attached.  
  
## Example  
 See the example for [CPrintDialog::GetPrinterDC](../vs140/CPrintDialog--GetPrinterDC.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::DeleteTempMap](../vs140/CDC--DeleteTempMap.md)