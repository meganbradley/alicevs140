---
title: "CMFCAutoHideButton::OnDraw"
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
ms.assetid: 91575789-2fd8-4a81-ac51-aba34285239b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideButton::OnDraw
The framework calls this method when it draws the auto-hide button.  
  
## Syntax  
  
```  
virtual void OnDraw(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
## Remarks  
 If you want to customize the appearance of auto-hide buttons in your application, create a new class derived from the [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md). In your derived class, override this method.  
  
## Requirements  
 **Header:** afxautohidebutton.h  
  
## See Also  
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)