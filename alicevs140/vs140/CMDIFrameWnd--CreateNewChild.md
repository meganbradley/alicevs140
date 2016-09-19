---
title: "CMDIFrameWnd::CreateNewChild"
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
ms.assetid: 71e4096a-ac0b-4685-9724-2741652c2afd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::CreateNewChild
Creates a new child window.  
  
## Syntax  
  
```  
  
      CMDIChildWnd* CreateNewChild(  
   CRuntimeClass* pClass,  
   UINT nResource,  
   HMENU hMenu = NULL,  
   HACCEL hAccel = NULL  
);  
```  
  
#### Parameters  
 `pClass`  
 The run-time class of the child window to be created.  
  
 *nResource*  
 The ID of shared resources associated with the child window.  
  
 `hMenu`  
 The child window's menu.  
  
 `hAccel`  
 The child window's accelerator.  
  
## Remarks  
 Use this function to create child windows of an MDI frame window.  
  
## Example  
 [!CODE [NVC_MFCWindowing#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#15)]  
  
 This example is an excerpt from Knowledge Base article Q201045, "HOWTO: Add Multiple Window Types to a Non-Document/View MDI App." Knowledge Base articles are available in the MSDN Library Visual Studio documentation or at [http://support.microsoft.com](http://support.microsoft.com/).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)