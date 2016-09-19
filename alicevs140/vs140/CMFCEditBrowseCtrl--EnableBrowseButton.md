---
title: "CMFCEditBrowseCtrl::EnableBrowseButton"
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
ms.assetid: c7397f46-6b4e-488f-8a3f-736136cb0e6b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCEditBrowseCtrl::EnableBrowseButton
Displays or does not display the browse button on the current edit browse control.  
  
## Syntax  
  
```  
void EnableBrowseButton(  
   BOOL bEnable=TRUE,  
   LPCTSTR szLabel=_T("...")  
);  
```  
  
#### Parameters  
 `bEnable`  
 `TRUE` to display the browse button; `FALSE` not to display the browse button. The default value is `TRUE`.  
  
 `szLabel`  
 The label that is displayed on the browse button. The default value is "**...**".  
  
## Remarks  
 If the `bEnable` parameter is `TRUE`, implement a custom action to perform when the browse button is clicked. To implement a custom action, derive a class from the `CMFCEditBrowseCtrl` class and then override its [OnBrowse](../vs140/CMFCEditBrowseCtrl--OnBrowse.md) method.  
  
 If the `bEnable` parameter is `TRUE`, the browse mode of the control is `BrowseMode_Default`; otherwise, the browse mode is `BrowseMode_None`. For more information about browse modes, see the [GetMode](../vs140/CMFCEditBrowseCtrl--GetMode.md) method.  
  
## Requirements  
 **Header:** afxeditbrowsectrl.h  
  
## See Also  
 [CMFCEditBrowseCtrl Class](../vs140/CMFCEditBrowseCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCEditBrowseCtrl::GetMode](../vs140/CMFCEditBrowseCtrl--GetMode.md)   
 [CMFCEditBrowseCtrl::EnableFileBrowseButton](../vs140/CMFCEditBrowseCtrl--EnableFileBrowseButton.md)   
 [CMFCEditBrowseCtrl::EnableFolderBrowseButton](../vs140/CMFCEditBrowseCtrl--EnableFolderBrowseButton.md)   
 [CMFCEditBrowseCtrl::SetBrowseButtonImage](../vs140/CMFCEditBrowseCtrl--SetBrowseButtonImage.md)