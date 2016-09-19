---
title: "Retrieving a BLOB"
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
ms.assetid: 2893eb0a-5c05-4016-8914-1e40ccbaf0b3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Retrieving a BLOB
You can retrieve a binary large object (BLOB) in various ways. You can use **DBTYPE_BYTES** to retrieve the BLOB as a sequence of bytes or use an interface like `ISequentialStream`. For more information, see [BLOBS and OLE Objects](https://msdn.microsoft.com/en-us/library/ms711511.aspx) in the *OLE DB Programmer's Reference*.  
  
 The following code shows how to retrieve a BLOB using `ISequentialStream`. The macro [BLOB_ENTRY](../vs140/BLOB_ENTRY.md) allows you to specify the interface and the flags used for the interface. After opening the table, the code calls **Read** repeatedly on `ISequentialStream` to read bytes from the BLOB. The code calls **Release** to dispose of the interface pointer before calling `MoveNext` to obtain the next record.  
  
```  
class CCategories  
{  
public:  
   ISequentialStream*   pPicture;  
  
BEGIN_COLUMN_MAP(CCategories)  
   BLOB_ENTRY(4, IID_ISequentialStream, STGM_READ, pPicture)  
END_COLUMN_MAP()  
};  
  
CTable<CAccessor<CCategories> > categories;  
ULONG          cb;  
BYTE            myBuffer[65536];  
  
categories.Open(session, "Categories");  
while (categories.MoveNext() == S_OK)  
{  
   do  
   {  
      categories.pPicture->Read(myBuffer, 65536, &cb);  
      // Do something with the buffer  
   } while (cb > 0);  
   categories.pPicture->Release();  
}  
```  
  
 For more information about macros that handle BLOB data, see "Column Map Macros" in [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md).  
  
## See Also  
 [Using Accessors](../vs140/Using-Accessors.md)   
 [Macros and Global Functions for OLE DB Consumer Templates](../vs140/Macros-and-Global-Functions-for-OLE-DB-Consumer-Templates.md)