---
title: "CArchive::Write"
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
ms.assetid: 229d20c8-ede5-4595-9ccf-17183e12a8fe
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::Write
Writes a specified number of bytes to the archive.  
  
## Syntax  
  
```  
  
      void Write(  
   const void* lpBuf,  
   UINT nMax   
);  
```  
  
#### Parameters  
 `lpBuf`  
 A pointer to a user-supplied buffer that contains the data to be written to the archive.  
  
 `nMax`  
 An integer that specifies the number of bytes to be written to the archive.  
  
## Remarks  
 The archive does not format the bytes.  
  
 You can use the **Write** member function within your `Serialize` function to write ordinary structures that are contained in your objects.  
  
## Example  
 [!CODE [NVC_MFCSerialization#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#23)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Read](../vs140/CArchive--Read.md)