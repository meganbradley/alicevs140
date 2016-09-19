---
title: "CMFCToolBarButton::GetClipboardFormat"
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
ms.assetid: 56b63893-f204-412a-b810-e6f938a5cdfe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::GetClipboardFormat
Retrieves the global clipboard format for the application.  
  
## Syntax  
  
```  
static CLIPFORMAT __stdcall GetClipboardFormat();  
```  
  
## Return Value  
 The global `CLIPFORMAT` value for the application.  
  
## Remarks  
 The framework calls this method to retrieve the clipboard format for OLE data transfer operations. For example, the [CMFCToolBarButton::CreateFromOleData](../vs140/CMFCToolBarButton--CreateFromOleData.md) method uses this method to copy data from a source OLE data object.  
  
 This method sets the global `CLIPFORMAT` value the first time this method is called. All subsequent calls to this method return this value.  
  
 To allow drag-and-drop operations to occur between applications, call the [CMFCToolBarButton::SetClipboardFormatName](../vs140/CMFCToolBarButton--SetClipboardFormatName.md) method.  
  
 For more information about clipboards in MFC, see [Clipboard](../vs140/Clipboard.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::CreateFromOleData](../vs140/CMFCToolBarButton--CreateFromOleData.md)   
 [CMFCToolBarButton::SetClipboardFormatName](../vs140/CMFCToolBarButton--SetClipboardFormatName.md)   
 [Clipboard](../vs140/Clipboard.md)