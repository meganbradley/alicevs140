---
title: "CMDIFrameWnd::CreateClient"
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
ms.assetid: 960f1946-5dd2-426f-82e6-e741a4601769
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::CreateClient
Creates the MDI client window that manages the `CMDIChildWnd` objects.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateClient(  
   LPCREATESTRUCT lpCreateStruct,  
   CMenu* pWindowMenu   
);  
```  
  
#### Parameters  
 `lpCreateStruct`  
 A long pointer to a [CREATESTRUCT](../vs140/CREATESTRUCT-Structure.md) structure.  
  
 `pWindowMenu`  
 A pointer to the Window pop-up menu.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function should be called if you override the `OnCreate` member function directly.  
  
## Example  
 [!CODE [NVC_MFCWindowing#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#14)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::CMDIFrameWnd](../vs140/CMDIFrameWnd--CMDIFrameWnd.md)