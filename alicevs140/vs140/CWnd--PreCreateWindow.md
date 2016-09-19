---
title: "CWnd::PreCreateWindow"
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
ms.assetid: d0b5d783-15dd-4047-a1d2-1252e7c2a73e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::PreCreateWindow
Called by the framework before the creation of the Windows window attached to this `CWnd` object.  
  
## Syntax  
  
```  
  
      virtual BOOL PreCreateWindow(  
   CREATESTRUCT& cs   
);  
```  
  
#### Parameters  
 *cs*  
 A [CREATESTRUCT](../vs140/CREATESTRUCT-Structure.md) structure.  
  
## Return Value  
 Nonzero if the window creation should continue; 0 to indicate creation failure.  
  
## Remarks  
  
> [!WARNING]
>  `CWnd::PreCreateWindow` now assigns the hMenu member of `cs` to the `this` pointer if the menu is `NULL` and the style contains `WS_CHILD`. For proper functionality, ensure that your dialog control has an ID that is not `NULL`.  
>   
>  This change fixes a crash in managed/native interop scenarios. A `TRACE` statement in `CWnd::Create` alerts the developer of the problem.  
  
 Never call this function directly.  
  
 The default implementation of this function checks for a **NULL** window class name and substitutes an appropriate default. Override this member function to modify the `CREATESTRUCT` structure before the window is created.  
  
 Each class derived from `CWnd` adds its own functionality to its override of `PreCreateWindow`. By design, these derivations of `PreCreateWindow` are not documented. To determine the styles appropriate to each class and the interdependencies between the styles, you can examine the MFC source code for your application's base class. If you choose to override **PreCreateWindow,** you can determine whether the styles used in your application's base class provide the functionality you need by using information gathered from the MFC source code.  
  
 For more information on changing window styles, see the [Changing the Styles of a Window Created by MFC](../vs140/Changing-the-Styles-of-a-Window-Created-by-MFC.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#112](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#112)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)   
 [CREATESTRUCT Structure](../vs140/CREATESTRUCT-Structure.md)