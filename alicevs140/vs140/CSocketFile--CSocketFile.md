---
title: "CSocketFile::CSocketFile"
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
ms.assetid: b1b2310e-45f9-4f6a-9a99-7fc85fecd338
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocketFile::CSocketFile
Constructs a `CSocketFile` object.  
  
## Syntax  
  
```  
  
      explicit CSocketFile(  
   CSocket* pSocket,  
   BOOL bArchiveCompatible = TRUE   
);  
```  
  
#### Parameters  
 `pSocket`  
 The socket to attach to the `CSocketFile` object.  
  
 `bArchiveCompatible`  
 Specifies whether the file object is for use with a `CArchive` object. Pass **FALSE** only if you want to use the `CSocketFile` object in a stand-alone manner as you would a stand-alone `CFile` object, with certain limitations. This flag changes how the `CArchive` object attached to the `CSocketFile` object manages its buffer for reading.  
  
## Remarks  
 The object's destructor disassociates itself from the socket object when the object goes out of scope or is deleted.  
  
> [!NOTE]
>  A `CSocketFile` can also be used as a (limited) file without a `CArchive` object. By default, the `CSocketFile` constructor's `bArchiveCompatible` parameter is **TRUE**. This specifies that the file object is for use with an archive. To use the file object without an archive, pass **FALSE** in the `bArchiveCompatible` parameter.  
  
 In its "archive compatible" mode, a `CSocketFile` object provides better performance and reduces the danger of a "deadlock." A deadlock occurs when both the sending and receiving sockets are waiting on each other, or for a common resource. This situation might occur if the `CArchive` object worked with the `CSocketFile` the way it does with a `CFile` object. With `CFile`, the archive can assume that if it receives fewer bytes than it requested, the end of file has been reached.  
  
 With `CSocketFile`, however, data is message based; the buffer can contain multiple messages, so receiving fewer than the number of bytes requested does not imply end of file. The application does not block in this case as it might with `CFile`, and it can continue reading messages from the buffer until the buffer is empty. The [CArchive::IsBufferEmpty](../vs140/CArchive--IsBufferEmpty.md) function is useful for monitoring the state of the archive's buffer in such a case.  
  
 For more information on the use of `CSocketFile`, see the articles [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md) and [Windows Sockets: Example of Sockets Using Archives](../vs140/Windows-Sockets--Example-of-Sockets-Using-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocketFile Class](../vs140/CSocketFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::CFile](../vs140/CFile--CFile.md)   
 [CFile::Read](../vs140/CFile--Read.md)