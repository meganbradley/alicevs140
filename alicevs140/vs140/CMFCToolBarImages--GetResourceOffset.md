---
title: "CMFCToolBarImages::GetResourceOffset"
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
ms.assetid: ccae5004-98bb-4d77-ac98-1f0631193a4a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::GetResourceOffset
Returns the image index for a specified resource ID.  
  
## Syntax  
  
```  
int GetResourceOffset(  
   UINT uiResId   
) const;  
```  
  
#### Parameters  
 [in] `uiResId`  
 An image resource ID.  
  
## Return Value  
 An image index if the method was successful; -1 if the image with the specified resource ID does not exist.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)