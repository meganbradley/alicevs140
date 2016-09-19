---
title: "CToolBar::SetButtonInfo"
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
ms.assetid: 5bbaa92b-62f7-4bbd-9fbf-c6d5c513ca8a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::SetButtonInfo
Call this member function to set the button's command ID, style, and image number.  
  
## Syntax  
  
```  
  
      void SetButtonInfo(  
   int nIndex,  
   UINT nID,  
   UINT nStyle,  
   int iImage   
);  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of the button or separator for which information is to be set.  
  
 `nID`  
 The value to which the button's command ID is set.  
  
 `nStyle`  
 The new button style. The following button styles are supported:  
  
-   **TBBS_BUTTON** Standard pushbutton (default)  
  
-   **TBBS_SEPARATOR** Separator  
  
-   **TBBS_CHECKBOX** Auto check-box button  
  
-   **TBBS_GROUP** Marks the start of a group of buttons  
  
-   **TBBS_CHECKGROUP** Marks the start of a group of check-box buttons  
  
-   **TBBS_DROPDOWN** Creates a drop-down list button.  
  
-   **TBBS_AUTOSIZE** The button's width will be calculated based on the text of the button, not on the size of the image.  
  
-   **TBBS_NOPREFIX** The button text will not have an accelerator prefix associated with it.  
  
 `iImage`  
 New index for the button's image within the bitmap.  
  
## Remarks  
 For separators, which have the style **TBBS_SEPARATOR**, this function sets the separator's width in pixels to the value stored in `iImage`.  
  
> [!NOTE]
>  You can also set button states using the `nStyle` parameter; however, because button states are controlled by the [ON_UPDATE_COMMAND_UI](../vs140/ON_UPDATE_COMMAND_UI.md) handler, any state you set using `SetButtonInfo` will be lost during the next idle processing. See [How to Update User-Interface Objects](../vs140/How-to--Update-User-Interface-Objects.md) and [TN031: Control Bars](../vs140/TN031--Control-Bars.md) for more information.  
  
 For information on bitmap images and buttons, see the [CToolBar](../vs140/CToolBar-Class.md) Overview and [CToolBar::LoadBitmap](../vs140/CToolBar--LoadBitmap.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::GetButtonInfo](../vs140/CToolBar--GetButtonInfo.md)