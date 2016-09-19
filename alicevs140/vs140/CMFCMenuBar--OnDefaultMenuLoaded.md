---
title: "CMFCMenuBar::OnDefaultMenuLoaded"
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
ms.assetid: 74ec3b50-5c3a-4bb2-bda8-3339eb949e22
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::OnDefaultMenuLoaded
The framework calls this method when it loads the menu resource from the resource file.  
  
## Syntax  
  
```  
virtual void OnDefaultMenuLoaded(  
   HMENU hMenu  
);  
```  
  
#### Parameters  
 [in] `hMenu`  
 The handle for the menu attached to the [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object.  
  
## Remarks  
 The default implementation of this function does nothing. Override this function to execute custom code after the framework loads a menu resource from the resource file.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)