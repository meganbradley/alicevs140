---
title: "CMFCRibbonEdit::CreateEdit"
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
ms.assetid: 8f02ae87-ae60-43e3-b553-ba500730d361
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::CreateEdit
Creates a new text box for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Syntax  
  
```  
virtual CMFCRibbonRichEditCtrl* CreateEdit(  
    CWnd* pWndParent,  
    DWORD dwEditStyle   
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 A pointer to the parent window of the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
 [in] `dwEditStyle`  
 Specifies the style of the text box. You can combine the window styles listed in the Remarks section with the [edit control styles](http://msdn.microsoft.com/library/windows/desktop/bb775464) that are described in the Windows SDK.  
  
## Return Value  
 A pointer to the new text box if the method was successful; otherwise, `NULL`.  
  
## Remarks  
 Override this method in a derived class to create a custom text box.  
  
 You can apply the following [Window Styles](../vs140/Window-Styles.md) to a text box:  
  
-   **WS_CHILD**  
  
-   **WS_VISIBLE**  
  
-   **WS_DISABLED**  
  
-   **WS_GROUP**  
  
-   **WS_TABSTOP**  
  
## Requirements  
 **Header:** afxRibbonEdit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)