---
title: "CBitmapButton::AutoLoad"
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
ms.assetid: 297ce926-182e-4662-9bee-f21e80633b65
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBitmapButton::AutoLoad
Associates a button in a dialog box with an object of the `CBitmapButton` class, loads the bitmap(s) by name, and sizes the button to fit the bitmap.  
  
## Syntax  
  
```  
  
      BOOL AutoLoad(  
   UINT nID,  
   CWnd* pParent   
);  
```  
  
#### Parameters  
 `nID`  
 The button's control ID.  
  
 `pParent`  
 Pointer to the object that owns the button.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Use the `AutoLoad` function to initialize an owner-draw button in a dialog box as a bitmap button. Instructions for using this function are in the remarks for the [CBitmapButton](../vs140/CBitmapButton-Class.md) class.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#75](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#75)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CBitmapButton Class](../vs140/CBitmapButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBitmapButton::LoadBitmaps](../vs140/CBitmapButton--LoadBitmaps.md)   
 [CBitmapButton::SizeToContent](../vs140/CBitmapButton--SizeToContent.md)