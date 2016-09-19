---
title: "CDC::DrawFrameControl"
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
ms.assetid: 3bc8d0f1-0652-4480-80a1-3716b234556d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DrawFrameControl
Call this member function to draw a frame control of the specified type and style.  
  
## Syntax  
  
```  
  
      BOOL DrawFrameControl(  
   LPRECT lpRect,  
   UINT nType,  
   UINT nState   
);  
```  
  
#### Parameters  
 `lpRect`  
 A pointer to a **RECT** structure that contains the logical coordinates of the rectangle.  
  
 `nType`  
 Specifies the type of frame control to draw. See the *uType* parameter in [DrawFrameControl](http://msdn.microsoft.com/library/windows/desktop/dd162480) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of this parameter's possible values.  
  
 `nState`  
 Specifies the initial state of the frame control. Can be one or more of the values described for the *uState* parameter in `DrawFrameControl` in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Use the `nState` value **DFCS_ADJUSTRECT** to adjust the bounding rectangle to exclude the surrounding edge of the push button.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 In several cases, `nState` depends on the `nType` parameter. The following list shows the relationship between the four `nType` values and `nState`:  
  
-   **DFC_BUTTON**  
  
    -   **DFCS_BUTTON3STATE** Three-state button  
  
    -   **DFCS_BUTTONCHECK** Check box  
  
    -   **DFCS_BUTTONPUSH** Push button  
  
    -   **DFCS_BUTTONRADIO** Radio button  
  
    -   **DFCS_BUTTONRADIOIMAGE** Image for radio button (nonsquare needs image)  
  
    -   **DFCS_BUTTONRADIOMASK** Mask for radio button (nonsquare needs mask)  
  
-   **DFC_CAPTION**  
  
    -   **DFCS_CAPTIONCLOSE** Close button  
  
    -   **DFCS_CAPTIONHELP** Help button  
  
    -   **DFCS_CAPTIONMAX** Maximize button  
  
    -   **DFCS_CAPTIONMIN** Minimize button  
  
    -   **DFCS_CAPTIONRESTORE** Restore button  
  
-   **DFC_MENU**  
  
    -   **DFCS_MENUARROW** Submenu arrow  
  
    -   **DFCS_MENUBULLET** Bullet  
  
    -   **DFCS_MENUCHECK** Check mark  
  
-   **DFC_SCROLL**  
  
    -   **DFCS_SCROLLCOMBOBOX** Combo box scroll bar  
  
    -   **DFCS_SCROLLDOWN** Down arrow of scroll bar  
  
    -   **DFCS_SCROLLLEFT** Left arrow of scroll bar  
  
    -   **DFCS_SCROLLRIGHT** Right arrow of scroll bar  
  
    -   **DFCS_SCROLLSIZEGRIP** Size grip in bottom-right corner of window  
  
    -   **DFCS_SCROLLUP** Up arrow of scroll bar  
  
## Example  
 This code draws the size gripper in the bottom-right corner of your window. It's appropriate for the `OnPaint` handler of a dialog box, which has no styles and normally doesn't contain other controls (like a status bar) that may give it a size gripper.  
  
 [!CODE [NVC_MFCDocView#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#34)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DrawFrameControl](http://msdn.microsoft.com/library/windows/desktop/dd162480)