---
title: "CMFCToolBar::GetButtonInfo"
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
ms.assetid: 792413fe-93cc-4e8f-9f3f-e5723ba7f4b0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetButtonInfo
Returns the command ID, style, and image index of the button at a specified index.  
  
## Syntax  
  
```  
void GetButtonInfo(  
   int nIndex,  
   UINT& nID,  
   UINT& nStyle,  
   int& iImage   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the button in the list of buttons on the toolbar.  
  
 [out] `nID`  
 The command ID of a button.  
  
 [out] `nStyle`  
 The style of the button.  
  
 [out] `iImage`  
 The index of the image for the button.  
  
## Remarks  
 The `GetButtonInfo` method finds a toolbar button at the specified index and retrieves the command ID, style and image index of the button.  
  
 If the button at the specified index does not exist, the framework sets `nID` and `nStyle` to 0, and `iImage` to -1 when the method returns.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)