---
title: "WM_FORWARDMSG"
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
ms.assetid: 50ffb097-f451-426b-bece-135ee1ad39c8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WM_FORWARDMSG
This macro forwards a message received by a window to another window for processing.  
  
## Syntax  
  
```  
  
WM_FORWARDMSG  
  
```  
  
## Return Value  
 Nonzero if the message was processed, zero if not.  
  
## Remarks  
 Use `WM_FORWARDMSG` to forward a message received by a window to another window for processing. The LPARAM and WPARAM parameters are used as follows:  
  
|Parameter|Usage|  
|---------------|-----------|  
|WPARAM|Data defined by user|  
|LPARAM|A pointer to a `MSG` structure that contains information about a message|  
  
## Example  
 In the following example, `m_hWndOther` represents the other window that receives this message.  
  
 [!CODE [NVC_ATL_Windowing#137](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#137)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Windows Messages Macros](../vs140/Windows-Messages-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)