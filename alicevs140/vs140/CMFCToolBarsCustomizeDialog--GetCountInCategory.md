---
title: "CMFCToolBarsCustomizeDialog::GetCountInCategory"
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
ms.assetid: b055c2fc-4427-4bd0-9023-f96f060c6ee9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::GetCountInCategory
Retrieves the number of items in the provided list that have a given text label.  
  
## Syntax  
  
```  
int GetCountInCategory(  
   LPCTSTR lpszItemName,  
   const CObList& lstCommands  
) const;  
```  
  
#### Parameters  
 [in] `lpszItemName`  
 The text label to match.  
  
 [in] `lstCommands`  
 A reference to a list that contains `CMFCToolBarButton` objects.  
  
## Return Value  
 The number of items in the provided list whose text label equals `lpszItemName`.  
  
## Remarks  
 Each element in the provided object list must be of type `CMFCToolBarButton`. This method compares `lpszItemName` with the [CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md) data member.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md)