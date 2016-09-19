---
title: "CTreeCtrl::Create"
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
ms.assetid: 57868e7a-fef8-48d0-a3cf-cf19a556dfbe
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::Create
If you specify the tree control in a dialog box template, or if you are using [CTreeView](../vs140/CTreeView-Class.md), your tree control is created automatically when the dialog box or view is created.  
  
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
 Specifies the tree view control's style. Apply window styles, described in [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679), and any combination of [tree view control styles](http://msdn.microsoft.com/library/windows/desktop/bb760013) as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `rect`  
 Specifies the tree view control's size and position. It can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
 `pParentWnd`  
 Specifies the tree view control's parent window, usually a `CDialog`. It must not be **NULL**.  
  
 `nID`  
 Specifies the tree view control's ID.  
  
## Return Value  
 Nonzero if initialization was successful; otherwise 0.  
  
## Remarks  
 If you want to create the tree control as a child window of some other window, use the **Create** member function. If you create the tree control using **Create**, you must pass it **WS_VISIBLE**, in addition to other tree view styles.  
  
 You construct a `CTreeCtrl` in two steps. First call the constructor, then call **Create**, which creates the tree view control and attaches it to the `CTreeCtrl` object.  
  
 To create a tree control with extended window styles, call [CreateEx](../vs140/CTreeCtrl--CreateEx.md) instead of **Create**.  
  
## Example  
 [!CODE [NVC_MFC_CTreeCtrl#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTreeCtrl#1)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::CTreeCtrl](../vs140/CTreeCtrl--CTreeCtrl.md)