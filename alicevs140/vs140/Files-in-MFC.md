---
title: "Files in MFC"
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
ms.assetid: ae25e2c5-2859-4679-ab97-438824e93ce1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Files in MFC
In the Microsoft Foundation Class Library (MFC), class [CFile](../vs140/CFile-Class.md) handles normal file I/O operations. This family of articles explains how to open and close files as well as read and write data to those files. It also discusses file status operations. For a description of how to use the object-based serialization features of MFC as an alternative way of reading and writing data in files, see the article [Serialization](../vs140/Serialization-in-MFC.md).  
  
> [!NOTE]
>  When you use MFC **CDocument** objects, the framework does much of the serialization work for you. In particular, the framework creates and uses the `CFile` object. You only have to write code in your override of the `Serialize` member function of class **CDocument**.  
  
 The `CFile` class provides an interface for general-purpose binary file operations. The `CStdioFile` and `CMemFile` classes derived from `CFile` and the `CSharedFile` class derived from `CMemFile` supply more specialized file services.  
  
 For more information about alternatives to MFC file handling, see [File Handling](../Topic/File%20Handling.md) in the *Run-Time Library Reference*.  
  
 For information about derived `CFile` classes, see the [MFC hierarchy chart](../vs140/Hierarchy-Chart.md).  
  
## What do you want to do?  
 *Use CFile*  
  
-   [Open a file with CFile](../vs140/Opening-Files.md)  
  
-   [Read and write a file with CFile](../vs140/Reading-and-Writing-Files.md)  
  
-   [Close a file with CFile](../vs140/Closing-Files.md)  
  
-   [Access file status with CFile](../vs140/Accessing-File-Status.md)  
  
 *Use MFC Serialization (Object Persistence)*  
  
-   [Create a serializable class](../vs140/Serialization--Making-a-Serializable-Class.md)  
  
-   [Serialize an object via a CArchive object](../vs140/Serialization--Serializing-an-Object.md)  
  
-   [Create a CArchive object](../vs140/Two-Ways-to-Create-a-CArchive-Object.md)  
  
-   [Use CArchive << and >> operators](../vs140/Using-the-CArchive----and----Operators.md)  
  
-   [Store and load CObjects and CObject-derived objects via an archive](../vs140/Storing-and-Loading-CObjects-via-an-Archive.md)  
  
## See Also  
 [Concepts](../vs140/MFC-Concepts.md)   
 [General MFC Topics](../vs140/General-MFC-Topics.md)   
 [CArchive Class](../vs140/CArchive-Class.md)   
 [CObject Class](../vs140/CObject-Class.md)   
 [How Do I: Use the CFile Class?](http://go.microsoft.com/fwlink/?LinkId=128046)