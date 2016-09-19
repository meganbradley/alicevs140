---
title: "CDaoRecordset::IsFieldNull"
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
ms.assetid: d18aab49-c798-4930-9c52-3a59198b8160
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::IsFieldNull
Call this member function to determine whether the specified field data member of a recordset has been flagged as Null.  
  
## Syntax  
  
```  
  
      BOOL IsFieldNull(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 A pointer to the field data member whose status you want to check, or **NULL** to determine if any of the fields are Null.  
  
## Return Value  
 Nonzero if the specified field data member is flagged as Null; otherwise 0.  
  
## Remarks  
 (In database terminology, Null means "having no value" and is not the same as **NULL** in C++.) If a field data member is flagged as Null, it is interpreted as a column of the current record for which there is no value.  
  
> [!NOTE]
>  In certain situations, using `IsFieldNull` can be inefficient, as the following code example illustrates:  
  
 [!CODE [NVC_MFCDatabase#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#5)]  
  
> [!NOTE]
>  If you are using dynamic record binding, without deriving from `CDaoRecordset`, be sure to use **VT_NULL** as shown in the example.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::IsFieldDirty](../vs140/CDaoRecordset--IsFieldDirty.md)   
 [CDaoRecordset::IsFieldNullable](../vs140/CDaoRecordset--IsFieldNullable.md)