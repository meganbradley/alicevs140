---
title: "CMFCPropertyGridProperty::SetData"
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
ms.assetid: 63603e75-d8ec-424c-a217-d068ebd8abae
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::SetData
Associates a `DWORD` value with a property.  
  
## Syntax  
  
```  
void SetData(  
   DWORD_PTR dwData   
);  
```  
  
#### Parameters  
 [in] `dwData`  
 An application-specific 32-bit value, such as an integer or a pointer to other data.  
  
## Remarks  
 Use the [CMFCPropertyGridProperty::GetData](../vs140/CMFCPropertyGridProperty--GetData.md) method to retrieve the `DWORD` value. Use the [CMFCPropertyGridCtrl::FindItemByData](../vs140/CMFCPropertyGridCtrl--FindItemByData.md) method to locate the property list item that is associated with the specified `DWORD` value.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::GetData](../vs140/CMFCPropertyGridProperty--GetData.md)   
 [CMFCPropertyGridCtrl::FindItemByData](../vs140/CMFCPropertyGridCtrl--FindItemByData.md)