---
title: "CMFCEditBrowseCtrl::OnBrowse"
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
ms.assetid: 9683f527-072d-4bc7-b243-a782f3e36493
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCEditBrowseCtrl::OnBrowse
Called by the framework after the user clicks the browse button of the edit browse control.  
  
## Syntax  
  
```  
virtual void OnBrowse();  
```  
  
## Remarks  
 Use this method to execute custom code when the user clicks the browse button of the edit browse control. Derive your own class from the `CMFCEditBrowseCtrl` class and override its `OnBrowse` method. In that method, implement a custom browse action and optionally update the text box of the edit browse control. In your application, use the [EnableBrowseButton](../vs140/CMFCEditBrowseCtrl--EnableBrowseButton.md) method to put the edit browse control in *custom browse* mode.  
  
## Requirements  
 **Header:** afxeditbrowsectrl.h  
  
## See Also  
 [CMFCEditBrowseCtrl Class](../vs140/CMFCEditBrowseCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCEditBrowseCtrl::EnableBrowseButton](../vs140/CMFCEditBrowseCtrl--EnableBrowseButton.md)