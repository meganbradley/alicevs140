---
title: "System Calls"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0255f2ec-a5a0-487e-8b09-9dad001d81ed
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# System Calls
The following functions are Windows operating system calls.  
  
### System Call Functions  
  
|Function|Use|.NET Framework equivalent|  
|--------------|---------|-------------------------------|  
|[_findclose](../vs140/_findclose.md)|Release resources from previous find operations|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_findfirst, _findfirst32, _findfirst64, _findfirsti64, _findfirst32i64, _findfirst64i32, _wfindfirst, _wfindfirst32, _wfindfirst64, _wfindfirsti64, _wfindfirst32i64, _wfindfirst64i32](../vs140/_findfirst--_findfirst32--_findfirst32i64--_findfirst64--_findfirst64i32--_findfirsti64--_wfindfirst--_wfindfirst32--_wfindfirst32i64--_wfindfirst64--_wfindfirst64i32--_wfindfirsti64.md)|Find file with specified attributes|[System::IO::DirectoryInfo::GetFiles](https://msdn.microsoft.com/en-us/library/system.io.directoryinfo.getfiles.aspx)|  
|[_findnext, _findnext32, _findnext64, _findnexti64, _findnext32i64, _findnext64i32, _wfindnext, _wfindnext32, _wfindnexti64, _wfindnext64, _wfindnexti64](../vs140/_findnext--_findnext32--_findnext32i64--_findnext64--_findnext64i32--_findnexti64--_wfindnext--_wfindnext32--_wfindnext32i64--_wfindnext64--_wfindnext64i32--_wfindnexti64.md)|Find next file with specified attributes|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)   
 [File Handling](../Topic/File%20Handling.md)   
 [Directory Control](../vs140/Directory-Control.md)   
 [Low-Level I/O](../vs140/Low-Level-I-O.md)