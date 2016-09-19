---
title: "CStatic::SetCursor"
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
ms.assetid: 43c20087-4e2c-4d40-aa8d-492dc96ddfff
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::SetCursor
Associates a new cursor image with the static control.  
  
## Syntax  
  
```  
  
      HCURSOR SetCursor(  
   HCURSOR hCursor   
);  
```  
  
#### Parameters  
 `hCursor`  
 Handle of the cursor to be drawn in the static control.  
  
## Return Value  
 The handle of the cursor previously associated with the static control, or **NULL** if no cursor was associated with the static control.  
  
## Remarks  
 The cursor will be automatically drawn in the static control. By default, it will be drawn in the upper-left corner and the static control will be resized to the size of the cursor.  
  
 You can use various window and static control styles, including the following:  
  
-   **SS_ICON** Use this style always for cursors and icons.  
  
-   **SS_CENTERIMAGE** Use to center in the static control. If the image is larger than the static control, it will be clipped. If it is smaller than the static control, the empty space around the image will be filled with the background color of the static control.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::GetCursor](../vs140/CStatic--GetCursor.md)   
 [STM_SETIMAGE](http://msdn.microsoft.com/library/windows/desktop/bb760782)   
 [Cursors](http://msdn.microsoft.com/library/windows/desktop/ms646970)