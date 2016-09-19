---
title: "CArchive::ReadString"
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
ms.assetid: 5d06747a-1194-4a0c-bd1a-36bc0ed500f7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::ReadString
Call this member function to read text data into a buffer from the file associated with the `CArchive` object.  
  
## Syntax  
  
```  
  
      BOOL ReadString(   
   CString& rString    
);  
LPTSTR ReadString(  
   LPTSTR lpsz,  
   UINT nMax   
);  
```  
  
#### Parameters  
 `rString`  
 A reference to a [CString](../vs140/CStringT-Class.md) that will contain the resultant string after it is read from the file associated with the CArchive object.  
  
 `lpsz`  
 Specifies a pointer to a user-supplied buffer that will receive a null-terminated text string.  
  
 `nMax`  
 Specifies the maximum number of characters to read. Should be one less than the size of the *lpsz* buffer.  
  
## Return Value  
 In the version that returns **BOOL**, **TRUE** if successful; **FALSE** otherwise.  
  
 In the version that returns an `LPTSTR`, a pointer to the buffer containing the text data; **NULL** if end-of-file was reached.  
  
## Remarks  
 In the version of the member function with the `nMax` parameter, the buffer will hold up to a limit of `nMax` - 1 characters. Reading is stopped by a carriage return-linefeed pair. Trailing newline characters are always removed. A null character ('\0') is appended in either case.  
  
 [CArchive::Read](../vs140/CArchive--Read.md) is also available for text-mode input, but it does not terminate on a carriage return-linefeed pair.  
  
## Example  
 See the example for [CArchive::WriteString](../vs140/CArchive--WriteString.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Read](../vs140/CArchive--Read.md)   
 [CArchive::Write](../vs140/CArchive--Write.md)   
 [CArchive::WriteString](../vs140/CArchive--WriteString.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)