---
title: "CDaoRecordset::GetEditMode"
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
ms.assetid: d7e3bbe9-82e3-427f-bc98-c3037de4a0dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetEditMode
Call this member function to determine the state of editing, which is one of the following values:  
  
## Syntax  
  
```  
  
short GetEditMode( );  
  
```  
  
## Return Value  
 Returns a value that indicates the state of editing for the current record.  
  
## Remarks  
  
|Value|Description|  
|-----------|-----------------|  
|**dbEditNone**|No editing operation is in progress.|  
|**dbEditInProgress**|**Edit** has been called.|  
|**dbEditAdd**|`AddNew` has been called.|  
  
 For related information, see the topic "EditMode Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)