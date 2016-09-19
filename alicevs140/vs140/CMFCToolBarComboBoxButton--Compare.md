---
title: "CMFCToolBarComboBoxButton::Compare"
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
ms.assetid: 636357ee-2a4c-4cae-962f-5d4644046285
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::Compare
Compares two strings.  
  
## Syntax  
  
```  
virtual int Compare(  
   LPCTSTR lpszItem1,  
   LPCTSTR lpszItem2   
);  
```  
  
#### Parameters  
 [in] `lpszItem1`  
 The first string to compare.  
  
 [in] `lpszItem2`  
 The second string to compare.  
  
## Return Value  
 A value that indicates the case-sensitive lexicographic relationship between the strings. The following table lists the possible values:  
  
|Value|Description|  
|-----------|-----------------|  
|<0|The first string is less than the second.|  
|0|The first string equals the second.|  
|>0|The first string is greater than the second.|  
  
## Remarks  
 Override this method to change how items are sorted in the list box.  
  
 The comparison is case-sensitive.  
  
 This method is called only from the [AddSortedItem](../vs140/CMFCToolBarComboBoxButton--AddSortedItem.md) method.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarComboBoxButton::AddSortedItem](../vs140/CMFCToolBarComboBoxButton--AddSortedItem.md)