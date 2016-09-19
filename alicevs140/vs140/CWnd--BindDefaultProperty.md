---
title: "CWnd::BindDefaultProperty"
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
ms.assetid: 88e0c87c-837a-4b30-8153-738e0842f27a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::BindDefaultProperty
Binds the calling object's default simple bound property (such as an edit control), as marked in the type library, to the underlying cursor that is defined by the DataSource, UserName, Password, and SQL properties of the data-source control.  
  
## Syntax  
  
```  
  
      void BindDefaultProperty(  
   DISPID dwDispID,  
   VARTYPE vtProp,  
   LPCTSTR szFieldName,  
   CWnd * pDSCWnd   
);  
```  
  
#### Parameters  
 `dwDispID`  
 Specifies the DISPID of a property on a data-bound control that is to be bound to a data-source control.  
  
 `vtProp`  
 Specifies the type of the property to be bound — for example, `VT_BSTR`, **VT_VARIANT**, and so on.  
  
 `szFieldName`  
 Specifies the name of the column, in the cursor provided by the data-source control, to which the property will be bound.  
  
 `pDSCWnd`  
 Points to the window that hosts the data-source control to which the property will be bound. Call `GetDlgItem` with the resource ID of the DCS's host window to retrieve this pointer.  
  
## Remarks  
 The `CWnd` object on which you call this function must be a data-bound control.  
  
## Example  
 `BindDefaultProperty` might be used in the following context:  
  
 [!CODE [NVC_MFC_AxDataBinding#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#1)]  
[!CODE [NVC_MFC_AxDataBinding#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#2)]  
[!CODE [NVC_MFC_AxDataBinding#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_AxDataBinding#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDSCCursor](../vs140/CWnd--GetDSCCursor.md)   
 [CWnd::BindProperty](../vs140/CWnd--BindProperty.md)