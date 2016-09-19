---
title: "CMFCPropertyGridCtrl::ValidateItemData"
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
ms.assetid: 5e696742-7019-43ae-9bdb-313fc28cd601
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::ValidateItemData
Called by the framework to validate property data.  
  
## Syntax  
  
```  
virtual BOOL ValidateItemData(  
   CMFCPropertyGridProperty* pProp  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pProp`|Pointer to a property. This parameter is not used.|  
  
## Return Value  
 Always `TRUE`.  
  
## Remarks  
 The [CMFCPropertyGridCtrl::EndEditItem](../vs140/CMFCPropertyGridCtrl--EndEditItem.md) method calls this method to validate data. By default, this method does not use its `pProp` parameter and its return value is always `TRUE`.  
  
 If you override this method, return `TRUE` if the specified property data is valid. Otherwise, return `FALSE`, in which case the framework does not update the property.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::EndEditItem](../vs140/CMFCPropertyGridCtrl--EndEditItem.md)