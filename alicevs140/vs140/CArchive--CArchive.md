---
title: "CArchive::CArchive"
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
ms.assetid: d21b525f-a538-4b0d-ace7-c5985e72c5df
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::CArchive
Constructs a `CArchive` object and specifies whether it will be used for loading or storing objects.  
  
## Syntax  
  
```  
  
      CArchive(  
   CFile* pFile,  
   UINT nMode,  
   int nBufSize = 4096,  
   void* lpBuf = NULL   
);  
```  
  
#### Parameters  
 `pFile`  
 A pointer to the `CFile` object that is the ultimate source or destination of the persistent data.  
  
 `nMode`  
 A flag that specifies whether objects will be loaded from or stored to the archive. The `nMode` parameter must have one of the following values:  
  
-   **CArchive::load** Loads data from the archive. Requires only `CFile` read permission.  
  
-   **CArchive::store** Saves data to the archive. Requires `CFile` write permission.  
  
-   **CArchive::bNoFlushOnDelete** Prevents the archive from automatically calling `Flush` when the archive destructor is called. If you set this flag, you are responsible for explicitly calling **Close** before the destructor is called. If you do not, your data will be corrupted.  
  
 `nBufSize`  
 An integer that specifies the size of the internal file buffer, in bytes. Note that the default buffer size is 4,096 bytes. If you routinely archive large objects, you will improve performance if you use a larger buffer size that is a multiple of the file buffer size.  
  
 `lpBuf`  
 An optional pointer to a user-supplied buffer of size `nBufSize`. If you do not specify this parameter, the archive allocates a buffer from the local heap and frees it when the object is destroyed. The archive does not free a user-supplied buffer.  
  
## Remarks  
 You cannot change this specification after you have created the archive.  
  
 You may not use `CFile` operations to alter the state of the file until you have closed the archive. Any such operation will damage the integrity of the archive. You may access the position of the file pointer at any time during serialization by obtaining the archive's file object from the [GetFile](../vs140/CArchive--GetFile.md) member function and then using the [CFile::GetPosition](../vs140/CFile--GetPosition.md) function. You should call [CArchive::Flush](../vs140/CArchive--Flush.md) before obtaining the position of the file pointer.  
  
## Example  
 [!CODE [NVC_MFCSerialization#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#12)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Close](../vs140/CArchive--Close.md)   
 [CArchive::Flush](../vs140/CArchive--Flush.md)   
 [CFile::Close](../vs140/CFile--Close.md)