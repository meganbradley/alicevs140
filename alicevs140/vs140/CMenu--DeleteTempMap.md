---
title: "CMenu::DeleteTempMap"
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
ms.assetid: cb9f6a96-fd3d-4695-aba5-b63e18bfb5ad
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::DeleteTempMap
Called automatically by the `CWinApp` idle-time handler, deletes any temporary `CMenu` objects created by the [FromHandle](../vs140/CMenu--FromHandle.md) member function.  
  
## Syntax  
  
```  
  
static void PASCAL DeleteTempMap( );  
```  
  
## Remarks  
 `DeleteTempMap` detaches the Windows menu object attached to a temporary `CMenu` object before deleting the `CMenu` object.  
  
## Example  
 [!CODE [NVC_MFCWindowing#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#23)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)