---
title: "CArchive::Read"
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
ms.assetid: 41e0d014-5bfe-49b3-bb39-003fdb810ee0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::Read
Reads a specified number of bytes from the archive.  
  
## Syntax  
  
```  
  
      UINT Read(  
   void* lpBuf,  
   UINT nMax   
);  
```  
  
#### Parameters  
 `lpBuf`  
 A pointer to a user-supplied buffer that is to receive the data read from the archive.  
  
 `nMax`  
 An unsigned integer specifying the number of bytes to be read from the archive.  
  
## Return Value  
 An unsigned integer containing the number of bytes actually read. If the return value is less than the number requested, the end of file has been reached. No exception is thrown on the end-of-file condition.  
  
## Remarks  
 The archive does not interpret the bytes.  
  
 You can use the **Read** member function within your `Serialize` function for reading ordinary structures that are contained in your objects.  
  
## Example  
 [!CODE [NVC_MFCSerialization#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#24)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)