---
title: "CWnd::DeleteTempMap"
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
ms.assetid: 01023c00-c6ad-4133-b584-2f38e043cfbc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::DeleteTempMap
Called automatically by the idle time handler of the `CWinApp` object.  
  
## Syntax  
  
```  
  
static void PASCAL DeleteTempMap( );  
```  
  
## Remarks  
 Deletes any temporary `CWnd` objects created by the `FromHandle` member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#86](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#86)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::FromHandle](../vs140/CWnd--FromHandle.md)