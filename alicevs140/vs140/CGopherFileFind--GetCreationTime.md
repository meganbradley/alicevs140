---
title: "CGopherFileFind::GetCreationTime"
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
ms.assetid: 635f9d55-fa29-42de-a087-3d476ed64b62
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFileFind::GetCreationTime
Gets the creation time for the current file.  
  
## Syntax  
  
```  
  
      virtual BOOL GetCreationTime(  
   FILETIME* pTimeStamp  
) const;  
virtual BOOL GetCreationTime(  
   CTime& refTime  
) const;  
```  
  
#### Parameters  
 `pTimeStamp`  
 A pointer to a [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure containing the time the file was created.  
  
 `refTime`  
 A reference to a [CTime](../Topic/CTime%20Class.md) object.  
  
## Return Value  
 Nonzero if successful; 0 if unsuccessful. `GetCreationTime` returns 0 only if [FindNextFile](../vs140/CGopherFileFind--FindNextFile.md) has never been called on this `CGopherFileFind` object.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CGopherFileFind--FindNextFile.md) at least once before calling `GetCreationTime`.  
  
> [!NOTE]
>  Not all file systems use the same semantics to implement the time stamp returned by this function. This function may return the same value returned by other time stamp functions if the underlying file system or server does not support keeping the time attribute. See the [Win32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure for information about time formats. On some operating systems, the returned time is in the time zone local to the machine were the file is located. See the Win32 [FileTimeToLocalFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724277) API for more information.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)