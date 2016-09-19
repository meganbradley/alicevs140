---
title: "COleControl::OnEdit"
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
ms.assetid: e4631397-b23d-4dd4-b0a4-643eb2e4552b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnEdit
Causes the control to be UI activated.  
  
## Syntax  
  
```  
  
      virtual BOOL OnEdit(  
   LPMSG lpMsg,  
   HWND hWndParent,  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpMsg`  
 A pointer to the Windows message that invoked the verb.  
  
 `hWndParent`  
 A handle to the parent window of the control.  
  
 `lpRect`  
 A pointer to the rectangle used by the control in the container.  
  
## Return Value  
 Nonzero if the call is successful; otherwise 0.  
  
## Remarks  
 This has the same effect as invoking the control's `OLEIVERB_UIACTIVATE` verb.  
  
 This function is typically used as the handler function for an `ON_OLEVERB` message map entry. This makes an "Edit" verb available on the control's "Object" menu. For example:  
  
 [!CODE [NVC_MFCAxCtl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#5)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)