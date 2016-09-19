---
title: "CDaoRecordset::IsOpen"
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
ms.assetid: 69f18194-5b69-48b3-aa88-53c6e8045468
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::IsOpen
Call this member function to determine if the recordset is open.  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
  
```  
  
## Return Value  
 Nonzero if the recordset object's **Open** or **Requery** member function has previously been called and the recordset has not been closed; otherwise 0.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::Open](../vs140/CDaoRecordset--Open.md)   
 [CDaoRecordset::Close](../vs140/CDaoRecordset--Close.md)