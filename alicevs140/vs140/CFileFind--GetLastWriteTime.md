---
title: "CFileFind::GetLastWriteTime"
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
ms.assetid: 1943ca28-4193-489c-a07c-31a07b20d17f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetLastWriteTime
Call this member function to get the last time the file was changed.  
  
## Syntax  
  
```  
  
      virtual BOOL GetLastWriteTime(  
   FILETIME* pTimeStamp   
) const;  
virtual BOOL GetLastWriteTime(  
   CTime& refTime   
) const;  
```  
  
#### Parameters  
 `pTimeStamp`  
 A pointer to a [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure containing the time the file was last written to.  
  
 `refTime`  
 A reference to a [CTime](../Topic/CTime%20Class.md) object.  
  
## Return Value  
 Nonzero if successful; 0 if unsuccessful. `GetLastWriteTime` returns 0 only if [FindNextFile](../vs140/CFileFind--FindNextFile.md) has never been called on this `CFileFind` object.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `GetLastWriteTime`.  
  
> [!NOTE]
>  Not all file systems use the same semantics to implement the time stamp returned by this function. This function may return the same value returned by other time stamp functions if the underlying file system or server does not support keeping the time attribute. See the [Win32_Find_Data](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure for information about time formats. On some operation systems, the returned time is in the time zone local to the machine were the file is located. See the Win32 [FileTimeToLocalFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724277) API for more information.  
  
## Example  
 See the example for [CFileFind::GetLength](../vs140/CFileFind--GetLength.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)