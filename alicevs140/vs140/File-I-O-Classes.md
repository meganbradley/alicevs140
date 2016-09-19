---
title: "File I-O Classes"
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
ms.topic: article
H1: File I/O Classes
ms.assetid: 92821c3f-d9e1-47f6-98c9-3b632d86e811
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File I-O Classes
These classes provide an interface to traditional disk files, in-memory files, Active streams, and Windows sockets. All of the classes derived from `CFile` can be used with a `CArchive` object to perform serialization.  
  
 Use the following classes, particularly `CArchive` and `CFile`, if you write your own input/output processing. Normally you do not need to derive from these classes. If you use the application framework, the default implementations of the **Open** and **Save** commands on the **File** menu will handle file I/O (using class `CArchive`), as long as you override your document's `Serialize` function to supply details about how a document serializes its contents. For more information about the file classes and serialization, see the article [Files in MFC](../vs140/Files-in-MFC.md) and the article [Serialization](../vs140/Serialization-in-MFC.md).  
  
 [CFile](../vs140/CFile-Class.md)  
 Provides a file interface to binary disk files.  
  
 [CStdioFile](../vs140/CStdioFile-Class.md)  
 Provides a `CFile` interface to buffered stream disk files, usually in text mode.  
  
 [CMemFile](../vs140/CMemFile-Class.md)  
 Provides a `CFile` interface to in-memory files.  
  
 [CSharedFile](../vs140/CSharedFile-Class.md)  
 Provides a `CFile` interface to shared in-memory files.  
  
 [COleStreamFile](../vs140/COleStreamFile-Class.md)  
 Uses the COM `IStream` interface to provide `CFile` access to compound files.  
  
 [CSocketFile](../vs140/CSocketFile-Class.md)  
 Provides a `CFile` interface to a Windows Socket.  
  
## Related Classes  
 [CArchive](../vs140/CArchive-Class.md)  
 Cooperates with a `CFile` object to implement persistent storage for objects through serialization (see [CObject::Serialize](../vs140/CObject--Serialize.md)).  
  
 [CArchiveException](../vs140/CArchiveException-Class.md)  
 An archive exception.  
  
 [CFileException](../vs140/CFileException-Class.md)  
 A file-oriented exception.  
  
 [CFileDialog](../vs140/CFileDialog-Class.md)  
 Provides a standard dialog box for opening or saving a file.  
  
 [CRecentFileList](../vs140/CRecentFileList-Class.md)  
 Maintains the most recently used (MRU) file list.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)