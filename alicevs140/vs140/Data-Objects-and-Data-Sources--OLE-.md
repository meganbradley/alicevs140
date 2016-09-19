---
title: "Data Objects and Data Sources (OLE)"
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
ms.assetid: 8f68eed8-0ce8-4489-a4cc-f95554f89090
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Objects and Data Sources (OLE)
When you perform a data transfer, either by using the Clipboard or drag and drop, the data has a source and a destination. One application provides the data for copying and another application accepts it for pasting. Each side of the transfer needs to perform different operations on the same data for the transfer to succeed. The Microsoft Foundation Class (MFC) Library provides two classes that represent each side of this transfer:  
  
-   Data sources (as implemented by `COleDataSource` objects) represent the source side of the data transfer. They are created by the source application when data is to be copied to the Clipboard, or when data is provided for a drag-and-drop operation.  
  
-   Data objects (as implemented by `COleDataObject` objects) represent the destination side of the data transfer. They are created when the destination application has data dropped into it, or when it is asked to perform a paste operation from the Clipboard.  
  
 The following articles explain how to use data objects and data sources in your applications. This information applies to both container and server applications, because both may be called upon to copy and paste data.  
  
-   [Data Objects and Data Sources: Creation and Destruction](../vs140/Data-Objects-and-Data-Sources--Creation-and-Destruction.md)  
  
-   [Data Objects and Data Sources: Manipulation](../vs140/Data-Objects-and-Data-Sources--Manipulation.md)  
  
## In This Section  
 [Drag and Drop](../vs140/Drag-and-Drop--OLE-.md)  
  
 [Clipboard](../vs140/Clipboard.md)  
  
## See Also  
 [OLE](../vs140/OLE-in-MFC.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)