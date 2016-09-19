---
title: "CDaoRecordset::m_bCheckCacheForDirtyFields"
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
ms.assetid: 7e87ed8e-0586-4705-b9a9-cd5882779394
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::m_bCheckCacheForDirtyFields
Contains a flag indicating whether cached fields are automatically marked as dirty (changed) and Null.  
  
## Remarks  
 The flag defaults to **TRUE**. The setting in this data member controls the entire double-buffering mechanism. If you set the flag to **TRUE**, you can turn off the caching on a field-by-field basis using the DFX mechanism. If you set the flag to **FALSE**, you must call `SetFieldDirty` and `SetFieldNull` yourself.  
  
 Set this data member before calling **Open**. This mechanism is primarily for ease-of-use. Performance may be slower because of the double-buffering of fields as changes are made.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetFieldNull](../vs140/CDaoRecordset--SetFieldNull.md)   
 [CDaoRecordset::IsFieldNull](../vs140/CDaoRecordset--IsFieldNull.md)   
 [CDaoRecordset::IsFieldDirty](../vs140/CDaoRecordset--IsFieldDirty.md)   
 [CDaoRecordset::SetFieldDirty](../vs140/CDaoRecordset--SetFieldDirty.md)