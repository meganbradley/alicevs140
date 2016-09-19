---
title: "Accessing File Status"
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
ms.assetid: 1b8891d6-eb0f-4037-a837-4928fe595222
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accessing File Status
`CFile` also supports getting file status, including whether the file exists, creation and modification dates and times, logical size, and path.  
  
### To get file status  
  
1.  Use the [CFile](../vs140/CFile-Class.md) class to get and set information about a file. One useful application is to use the `CFile` static member function **GetStatus** to determine if a file exists. **GetStatus** returns 0 if the specified file does not exist.  
  
 Thus, you could use the result of **GetStatus** to determine whether to use the **CFile::modeCreate** flag when opening a file, as shown by the following example:  
  
 [!CODE [NVC_MFCFiles#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#3)]  
  
 For related information, see [Serialization](../vs140/Serialization-in-MFC.md).  
  
## See Also  
 [Files](../vs140/Files-in-MFC.md)