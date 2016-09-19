---
title: "CGdiObject::DeleteTempMap"
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
ms.assetid: e420b381-1efc-43f4-8c22-18e4d1a6265e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::DeleteTempMap
Called automatically by the `CWinApp` idle-time handler, `DeleteTempMap` deletes any temporary `CGdiObject` objects created by `FromHandle`.  
  
## Syntax  
  
```  
  
static void PASCAL DeleteTempMap( );  
```  
  
## Remarks  
 `DeleteTempMap` detaches the Windows GDI object attached to a temporary `CGdiObject` object before deleting the `CGdiObject` object.  
  
## Example  
 [!CODE [NVC_MFCDocView#175](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#175)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::Detach](../vs140/CGdiObject--Detach.md)   
 [CGdiObject::FromHandle](../vs140/CGdiObject--FromHandle.md)