---
title: "CMenu::Detach"
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
ms.assetid: cc83c02c-4782-42f2-b957-53d1bb62f026
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::Detach
Detaches a Windows menu from a `CMenu` object and returns the handle.  
  
## Syntax  
  
```  
  
HMENU Detach( );  
```  
  
## Return Value  
 The handle, of type `HMENU`, to a Windows menu, if successful; otherwise **NULL**.  
  
## Remarks  
 The `m_hMenu` data member is set to **NULL**.  
  
## Example  
 [!CODE [NVC_MFCWindowing#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#21)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::Attach](../vs140/CMenu--Attach.md)