---
title: "CCheckListBox::MeasureItem"
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
ms.assetid: c12e8ae3-2170-4c3b-84c7-a97eb0ce7a6f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::MeasureItem
Called by the framework when a checklist box with a nondefault style is created.  
  
## Syntax  
  
```  
  
      virtual void MeasureItem(  
   LPMEASUREITEMSTRUCT lpMeasureItemStruct   
);  
```  
  
#### Parameters  
 `lpMeasureItemStruct`  
 A long pointer to a [MEASUREITEMSTRUCT](../vs140/MEASUREITEMSTRUCT-Structure.md) structure.  
  
## Remarks  
 By default, this member function does nothing. Override this member function and fill in the `MEASUREITEMSTRUCT` structure to inform Windows of the dimensions of checklist-box items. If the checklist box is created with the [LBS_OWNERDRAWVARIABLE](../vs140/List-Box-Styles.md) style, the framework calls this member function for each item in the list box. Otherwise, this member is called only once.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::Create](../vs140/CCheckListBox--Create.md)   
 [CCheckListBox::DrawItem](../vs140/CCheckListBox--DrawItem.md)