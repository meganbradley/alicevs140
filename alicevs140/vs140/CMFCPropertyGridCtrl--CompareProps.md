---
title: "CMFCPropertyGridCtrl::CompareProps"
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
ms.assetid: b52240bc-fc12-4a7a-92dd-5950c9e560f8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::CompareProps
Called by the property grid control to sort properties.  
  
## Syntax  
  
```  
virtual int CompareProps(  
   const CMFCPropertyGridProperty* pProp1,  
   const CMFCPropertyGridProperty* pProp2   
) const;  
```  
  
#### Parameters  
 `pProp1`  
 A pointer to a property.  
  
 `pProp2`  
 A pointer to a property.  
  
## Return Value  
  
|Return Value|Description|  
|------------------|-----------------|  
|< 0|The name of the `pProp1` parameter is less than the name of the `pProp2` parameter.|  
|0|The name of the `pProp1` parameter is equal to the name of the `pProp2` parameter.|  
|> 0|The name of the `pProp1` object is greater than the name of the `pProp2` parameter.|  
  
## Remarks  
 By default, this method uses the [CString::Compare](../vs140/CStringT--Compare.md) method to compare the `CMFCPropertyGridProperty::m_strName` members of the specified parameters.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)