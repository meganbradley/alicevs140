---
title: "CListCtrl::Create"
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
ms.assetid: 80878188-62b0-4ef1-bc2c-04c09ad25dbc
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::Create
Creates a list control and attaches it to a `CListCtrl` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the list control's style. Apply any combination of list control styles to the control. See [List view window styles](http://msdn.microsoft.com/library/windows/desktop/bb774739) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a complete list of these styles. Set extended styles specific to a control using [SetExtendedStyle](../vs140/CListCtrl--SetExtendedStyle.md).  
  
 `rect`  
 Specifies the list control's size and position. It can be either a `CRect` object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
 `pParentWnd`  
 Specifies the list control's parent window, usually a `CDialog`. It must not be **NULL**.  
  
 `nID`  
 Specifies the list control's ID.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 You construct a `CListCtrl` in two steps. First, call the constructor and then call **Create**, which creates the list view control and attaches it to the `CListCtrl` object.  
  
 To apply extended Windows styles to the list control object, call [CreateEx](../vs140/CListCtrl--CreateEx.md) instead of **Create**.  
  
## Example  
 [!CODE [NVC_MFC_CListCtrl#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListCtrl#1)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::CListCtrl](../vs140/CListCtrl--CListCtrl.md)   
 [CListCtrl::CreateEx](../vs140/CListCtrl--CreateEx.md)