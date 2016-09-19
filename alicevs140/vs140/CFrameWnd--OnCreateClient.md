---
title: "CFrameWnd::OnCreateClient"
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
ms.assetid: 1a03d8ab-d869-4e5a-ae43-011fd617ad12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::OnCreateClient
Called by the framework during the execution of `OnCreate`.  
  
## Syntax  
  
```  
  
      virtual BOOL OnCreateClient(  
   LPCREATESTRUCT lpcs,  
   CCreateContext* pContext   
);  
```  
  
#### Parameters  
 `lpcs`  
 A pointer to a Windows [CREATESTRUCT](../vs140/CREATESTRUCT-Structure.md) structure*.*  
  
 `pContext`  
 A pointer to a [CCreateContext](../vs140/CCreateContext-Structure.md) structure*.*  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Never call this function.  
  
 The default implementation of this function creates a `CView` object from the information provided in `pContext`, if possible.  
  
 Override this function to override values passed in the `CCreateContext` object or to change the way controls in the main client area of the frame window are created. The `CCreateContext` members you can override are described in the [CCreateContext](../vs140/CCreateContext-Structure.md) class.  
  
> [!NOTE]
>  Do not replace values passed in the `CREATESTRUCT` structure. They are for informational use only. If you want to override the initial window rectangle, for example, override the `CWnd` member function [PreCreateWindow](../vs140/CWnd--PreCreateWindow.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)