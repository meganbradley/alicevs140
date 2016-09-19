---
title: "CFile::Open"
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
ms.assetid: b11e5c20-f099-4b17-9730-8a605d6b36a1
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Open
Overloaded. **Open** is designed for use with the default `CFile` constructor.  
  
## Syntax  
  
```  
  
      virtual BOOL Open(  
   LPCTSTR lpszFileName,  
   UINT nOpenFlags,  
   CFileException* pError = NULL   
);  
virtual BOOL Open(  
   LPCTSTR lpszFileName,  
   UINT nOpenFlags,  
   CAtlTransactionManager* pTM,  
   CFileException* pError = NULL  
);  
```  
  
#### Parameters  
 `lpszFileName`  
 A string that is the path to the desired file. The path can be relative, absolute, or a network name (UNC).  
  
 `nOpenFlags`  
 A **UINT** that defines the file's sharing and access mode. It specifies the action to take when opening the file. You can combine options by using the bitwise-OR ( **&#124;** ) operator. One access permission and one share option are required; the **modeCreate** and **modeNoInherit** modes are optional. See the [CFile](../vs140/CFile--CFile.md) constructor for a list of mode options.  
  
 `pError`  
 A pointer to an existing file-exception object that will receive the status of a failed operation.  
  
 `pTM`  
 Pointer to CAtlTransactionManager object  
  
## Return Value  
 Nonzero if the open was successful; otherwise 0. The `pError` parameter is meaningful only if 0 is returned.  
  
## Remarks  
 The two functions form a "safe" method for opening a file where a failure is a normal, expected condition.  
  
 While the `CFile` constructor will throw an exception in an error condition, **Open** will return **FALSE** for error conditions. **Open** can still initialize a [CFileException](../vs140/CFileException-Class.md) object to describe the error, however. If you don't supply the `pError` parameter, or if you pass **NULL** for `pError`, **Open** will return **FALSE** and not throw a `CFileException`. If you pass a pointer to an existing `CFileException`, and **Open** encounters an error, the function will fill it with information describing that error. In neither case will **Open** throw an exception.  
  
 The following table describes the possible results of **Open**.  
  
|`pError`|Error encountered?|Return value|CFileException content|  
|--------------|------------------------|------------------|----------------------------|  
|**NULL**|No|**TRUE**|n/a|  
|ptr to `CFileException`|No|**TRUE**|unchanged|  
|**NULL**|Yes|**FALSE**|n/a|  
|ptr to `CFileException`|Yes|**FALSE**|initialized to describe error|  
  
## Example  
 [!CODE [NVC_MFCFiles#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#13)]  
  
 [!CODE [NVC_MFCFiles#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#14)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::CFile](../vs140/CFile--CFile.md)   
 [CFile::Close](../vs140/CFile--Close.md)