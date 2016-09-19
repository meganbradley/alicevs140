---
title: "CWnd::BindProperty"
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
ms.assetid: bbcdbf16-2158-415a-b121-ee52f1d43366
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::BindProperty
Binds a cursor-bound property on a data-bound control (such as a grid control) to a data-source control and registers that relationship with the MFC binding manager.  
  
## Syntax  
  
```  
  
      void BindProperty(  
   DISPID dwDispId,  
   CWnd * pWndDSC  
);  
```  
  
#### Parameters  
 *dwDispId*  
 Specifies the DISPID of a property on a data-bound control that is to be bound to a data-source control.  
  
 `pWndDSC`  
 Points to the window that hosts the data-source control to which the property will be bound. Call `GetDlgItem` with the resource ID of the DCS's host window to retrieve this pointer.  
  
## Remarks  
 The `CWnd` object on which you call this function must be a data-bound control.  
  
## Example  
 `BindProperty` might be used in the following context:  
  
 [!CODE [NVC_MFC_AxDataBinding#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#1)]  
[!CODE [NVC_MFC_AxDataBinding#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#4)]  
[!CODE [NVC_MFC_AxDataBinding#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDSCCursor](../vs140/CWnd--GetDSCCursor.md)   
 [CWnd::BindDefaultProperty](../vs140/CWnd--BindDefaultProperty.md)