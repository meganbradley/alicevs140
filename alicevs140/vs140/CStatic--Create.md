---
title: "CStatic::Create"
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
ms.assetid: 2c50841a-fda3-4621-9c31-24729ea6aa52
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::Create
Creates the Windows static control and attaches it to the `CStatic` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpszText,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID = 0xffff   
);  
```  
  
#### Parameters  
 `lpszText`  
 Specifies the text to place in the control. If **NULL**, no text will be visible.  
  
 `dwStyle`  
 Specifies the static control's window style. Apply any combination of [static control styles](../vs140/Static-Styles.md) to the control.  
  
 `rect`  
 Specifies the position and size of the static control. It can be either a `RECT` structure or a `CRect` object.  
  
 `pParentWnd`  
 Specifies the `CStatic` parent window, usually a `CDialog` object. It must not be **NULL**.  
  
 `nID`  
 Specifies the static control's control ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Construct a `CStatic` object in two steps. First, call the constructor `CStatic`, and then call **Create**, which creates the Windows static control and attaches it to the `CStatic` object.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a static control:  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
 If you're going to display a bitmap, cursor, icon, or metafile in the static control, you'll need to apply one of the following [static styles](../vs140/Static-Styles.md):  
  
-   **SS_BITMAP** Use this style for bitmaps.  
  
-   **SS_ICON** Use this style for cursors and icons.  
  
-   **SS_ENHMETAFILE** Use this style for enhanced metafiles.  
  
 For cursors, bitmaps, or icons, you may also want to use the following style:  
  
-   **SS_CENTERIMAGE** Use to center the image in the static control.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#1)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::CStatic](../vs140/CStatic--CStatic.md)