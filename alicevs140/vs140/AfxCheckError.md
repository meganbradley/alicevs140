---
title: "AfxCheckError"
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
ms.assetid: 84738e07-075c-4227-9a9a-1de137b50f82
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxCheckError
This function tests the passed **SCODE** to see if it is an error.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxCheckError(  
   SCODE sc   
);  
throw CMemoryException*  
throw COleException*  
```  
  
## Remarks  
 If it is an error, the function throws an exception. If the passed `SCODE` is **E_OUTOFMEMORY**, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) by calling [AfxThrowMemoryException](../vs140/AfxThrowMemoryException.md). Otherwise, the function throws a [COleException](../vs140/COleException-Class.md) by calling [AfxThrowOleException](../vs140/AfxThrowOleException.md).  
  
 This function can be used to check the return values of calls to OLE functions in your application. By testing the return value with this function in your application, you can properly react to error conditions with a minimal amount of code.  
  
> [!NOTE]
>  This function has the same effect in debug and non-debug builds.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#33)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)