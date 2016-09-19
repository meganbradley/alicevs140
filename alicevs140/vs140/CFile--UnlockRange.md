---
title: "CFile::UnlockRange"
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
ms.assetid: f531a98b-cf25-47c3-bd1a-6daba9fdf0af
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::UnlockRange
Unlocks a range of bytes in an open file.  
  
## Syntax  
  
```  
  
      virtual void UnlockRange(  
   ULONGLONG dwPos,  
   ULONGLONG dwCount   
);  
```  
  
#### Parameters  
 `dwPos`  
 The byte offset of the start of the byte range to unlock.  
  
 `dwCount`  
 The number of bytes in the range to unlock.  
  
## Remarks  
 See the description of the [LockRange](../vs140/CFile--LockRange.md) member function for details.  
  
> [!NOTE]
>  This function is not available for the `CMemFile`-derived class.  
  
## Example  
 [!CODE [NVC_MFCFiles#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#12)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::LockRange](../vs140/CFile--LockRange.md)