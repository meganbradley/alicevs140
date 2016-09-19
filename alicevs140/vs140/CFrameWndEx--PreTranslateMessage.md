---
title: "CFrameWndEx::PreTranslateMessage"
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
ms.assetid: 1c71caf9-81e4-42a3-8bd0-4b20d1e2455a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::PreTranslateMessage
Handles specific window messages before they are dispatched.  
  
## Syntax  
  
```  
virtual BOOL PreTranslateMessage(  
   MSG* pMsg  
);  
```  
  
#### Parameters  
 [in] `pMsg`  
 A pointer to a [MSG](../vs140/MSG-Structure.md) structure that contains the message to process.  
  
## Return Value  
 Non-zero if the message was handled and should not be dispatched; 0 if the message was not handled and should be dispatched.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)