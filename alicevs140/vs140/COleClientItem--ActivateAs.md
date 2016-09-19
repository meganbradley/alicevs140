---
title: "COleClientItem::ActivateAs"
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
ms.assetid: 92adc79d-4c04-49a9-b1ec-1ab3a0803da0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::ActivateAs
Uses OLE's object conversion facilities to activate the item as though it were an item of the type specified by `clsidNew`.  
  
## Syntax  
  
```  
  
      virtual BOOL ActivateAs(  
   LPCTSTR lpszUserType,  
   REFCLSID clsidOld,  
   REFCLSID clsidNew   
);  
```  
  
#### Parameters  
 *lpszUserType*  
 Pointer to a string representing the target user type, such as "Word Document."  
  
 *clsidOld*  
 A reference to the item's current class ID. The class ID should represent the type of the actual object, as stored, unless it is a link. In that case, it should be the CLSID of the item to which the link refers. The [COleConvertDialog](../vs140/COleConvertDialog-Class.md) automatically provides the correct class ID for the item.  
  
 `clsidNew`  
 A reference to the target class ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This is called automatically by [COleConvertDialog::DoConvert](../vs140/COleConvertDialog--DoConvert.md). It is not usually called directly.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [COleClientItem::ConvertTo](../vs140/COleClientItem--ConvertTo.md)   
 [COleClientItem::Reload](../vs140/COleClientItem--Reload.md)