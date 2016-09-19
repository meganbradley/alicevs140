---
title: "CImageList::Copy"
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
ms.assetid: 56929e17-d4de-4ece-940b-39826f438a54
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::Copy
This member function implements the behavior of the Win32 function [ImageList_Copy](http://msdn.microsoft.com/library/windows/desktop/bb761520), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL Copy(  
   int iDst,  
   int iSrc,  
   UINT uFlags = ILCF_MOVE   
);  
BOOL Copy(  
   int iDst,  
   CImageList* pSrc,  
   int iSrc,  
   UINT uFlags = ILCF_MOVE   
);  
```  
  
#### Parameters  
 *iDst*  
 The zero-based index of the image to be used as the destination of the copy operation.  
  
 `iSrc`  
 The zero-based index of the image to be used as the source of the copy operation.  
  
 `uFlags`  
 The bit flag value that specifies the type of copy operation to be made. This parameter can be one of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|`ILCF_MOVE`|The source image is copied to the destination image's index. This operation results in multiple instances of a given image. `ILCF_MOVE` is the default.|  
|`ILCF_SWAP`|The source and destination images exchange positions within the image list.|  
  
 `pSrc`  
 A pointer to a `CImageList` object that is the target of the copy operation.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#6)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)