---
title: "Using the CArchive &lt;&lt; and &gt;&gt; Operators"
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
ms.assetid: 56aef326-02dc-4992-8282-f0a4b78a064e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using the CArchive &lt;&lt; and &gt;&gt; Operators
`CArchive` provides << and >> operators for writing and reading simple data types as well as `CObject`s to and from a file.  
  
#### To store an object in a file via an archive  
  
1.  The following example shows how to store an object in a file via an archive:  
  
     [!CODE [NVC_MFCSerialization#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#7)]  
  
#### To load an object from a value previously stored in a file  
  
1.  The following example shows how to load an object from a value previously stored in a file:  
  
     [!CODE [NVC_MFCSerialization#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#8)]  
  
 Usually, you store and load data to and from a file via an archive in the `Serialize` functions of `CObject`-derived classes, which you must have declared with the **DECLARE_SERIALIZE** macro. A reference to a `CArchive` object is passed to your `Serialize` function. You call the `IsLoading` function of the `CArchive` object to determine whether the `Serialize` function has been called to load data from the file or store data to the file.  
  
 The `Serialize` function of a serializable `CObject`-derived class typically has the following form:  
  
 [!CODE [NVC_MFCSerialization#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#9)]  
  
 The above code template is exactly the same as the one AppWizard creates for the `Serialize` function of the document (a class derived from **CDocument)**. This code template helps you write code that is easier to review, because the storing code and the loading code should always be parallel, as in the following example:  
  
 [!CODE [NVC_MFCSerialization#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#10)]  
  
 The library defines **<<** and **>>** operators for `CArchive` as the first operand and the following data types and class types as the second operand:  
  
||||  
|-|-|-|  
|`CObject*`|**SIZE and CSize**|**float**|  
|**WORD**|`CString`|**POINT** and `CPoint`|  
|`DWORD`|**BYTE**|`RECT` and `CRect`|  
|**Double**|**LONG**|`CTime` and `CTimeSpan`|  
|`Int`|**COleCurrency**|`COleVariant`|  
|`COleDateTime`|`COleDateTimeSpan`||  
  
> [!NOTE]
>  Storing and loading `CObject`s via an archive requires extra consideration. For more information, see [Storing and Loading CObjects via an Archive](../vs140/Storing-and-Loading-CObjects-via-an-Archive.md).  
  
 The **CArchive <<** and **>>** operators always return a reference to the `CArchive` object, which is the first operand. This enables you to chain the operators, as illustrated below:  
  
 [!CODE [NVC_MFCSerialization#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#11)]  
  
## See Also  
 [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md)