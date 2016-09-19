---
title: "CRichEditView::GetContextMenu"
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
ms.assetid: 267f96a3-e7a4-459d-b139-10cbd36326c8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetContextMenu
The framework calls this function as part of the processing of [IRichEditOleCallback::GetContextMenu](http://msdn.microsoft.com/library/windows/desktop/bb774317).  
  
## Syntax  
  
```  
  
      virtual HMENU GetContextMenu(  
   WORD seltyp,  
   LPOLEOBJECT lpoleobj,  
   CHARRANGE* lpchrg   
);  
```  
  
#### Parameters  
 *seltyp*  
 The selection type. The selection type values are described in the Remarks section.  
  
 `lpoleobj`  
 Pointer to a **OLEOBJECT** structure specifying the first selected OLE object if the selection contains one or more OLE items. If the selection contains no items, `lpoleobj` is **NULL**. The **OLEOBJECT** structure holds a pointer to an OLE object v-table.  
  
 `lpchrg`  
 Pointer to a [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure containing the current selection.  
  
## Return Value  
 Handle to the context menu.  
  
## Remarks  
 This function is a typical part of right mouse-button down processing.  
  
 The selection type can be any combination of the following flags:  
  
-   `SEL_EMPTY` Indicates that there is no current selection.  
  
-   `SEL_TEXT` Indicates that the current selection contains text.  
  
-   `SEL_OBJECT` Indicates that the current selection contains at least one OLE item.  
  
-   `SEL_MULTICHAR` Indicates that the current selection contains more than one character of text.  
  
-   `SEL_MULTIOBJECT` Indicates that the current selection contains more than one OLE object.  
  
 The default implementation returns **NULL**. This is an advanced overridable.  
  
 For more information, see [IRichEditOleCallback::GetContextMenu](http://msdn.microsoft.com/library/windows/desktop/bb774317) and [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information on the **OLEOBJECT** type, see the OLE Data Structures and Structure Allocation article in the *OLE Knowledge Base*.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetSelectionType](../vs140/CRichEditCtrl--GetSelectionType.md)