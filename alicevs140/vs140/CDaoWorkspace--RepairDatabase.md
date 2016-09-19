---
title: "CDaoWorkspace::RepairDatabase"
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
ms.assetid: f0ef3765-6d73-4850-a0de-2ad027c2216c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::RepairDatabase
Call this member function if you need to attempt to repair a corrupted database that accesses the Microsoft Jet database engine.  
  
## Syntax  
  
```  
  
      static void PASCAL RepairDatabase(   
   LPCTSTR lpszName    
);  
```  
  
#### Parameters  
 `lpszName`  
 The path and filename for an existing Microsoft Jet engine database file. If you omit the path, only the current directory is searched. If your system supports the uniform naming convention (UNC), you can also specify a network path, such as: "\\\\\\\MYSERVER\\\MYSHARE\\\MYDIR\\\MYDB.MDB". (Double backslashes are required in the path string because "\\" is the C++ escape character.)  
  
## Remarks  
 You must close the database specified by `lpszName` before you repair it. In a multiuser environment, other users cannot have `lpszName` open while you are repairing it. If `lpszName` is not closed or is not available for exclusive use, an error occurs.  
  
 This member function attempts to repair a database that was marked as possibly corrupt by an incomplete write operation. This can occur if an application using the Microsoft Jet database engine is closed unexpectedly because of a power outage or computer hardware problem. If you complete the operation and call the [Close](../vs140/CDaoDatabase--Close.md) member function or you quit the application in a usual way, the database will not be marked as possibly corrupt.  
  
> [!NOTE]
>  After repairing a database, it is also a good idea to compact it using the [CompactDatabase](../vs140/CDaoWorkspace--CompactDatabase.md) member function to defragment the file and to recover disk space.  
  
 For more information about repairing databases, see the topic "RepairDatabase Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)