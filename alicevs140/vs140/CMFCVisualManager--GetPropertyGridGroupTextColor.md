---
title: "CMFCVisualManager::GetPropertyGridGroupTextColor"
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
ms.assetid: 532a17f1-6e90-4d50-afcb-6693cdd8ddd0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::GetPropertyGridGroupTextColor
The framework calls this method to retrieve the text color of a property list.  
  
## Syntax  
  
```  
virtual COLORREF GetPropertyGridGroupTextColor(  
   CMFCPropertyGridCtrl* pPropList   
);  
```  
  
#### Parameters  
 [in] `pPropList`  
 A pointer to the property list.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the text color of the property list.  
  
## Remarks  
 Override this function to customize the text color of a property list in your application.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)