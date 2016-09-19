---
title: "CArchiveException::m_cause"
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
ms.assetid: 92e69164-827b-432c-a5c9-f5660e9157d6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchiveException::m_cause
Specifies the cause of the exception.  
  
## Syntax  
  
```  
  
int m_cause;  
  
```  
  
## Remarks  
 This data member is a public variable of type `int`. Its values are defined by a `CArchiveException` enumerated type. The enumerators and their meanings are as follows:  
  
-   **CArchiveException::none** No error occurred.  
  
-   **CArchiveException::genericException** Unspecified error.  
  
-   **CArchiveException::readOnly** Tried to write into an archive opened for loading.  
  
-   **CArchiveException::endOfFile** Reached end of file while reading an object.  
  
-   **CArchiveException::writeOnly** Tried to read from an archive opened for storing.  
  
-   **CArchiveException::badIndex** Invalid file format.  
  
-   **CArchiveException::badClass** Tried to read an object into an object of the wrong type.  
  
-   **CArchiveException::badSchema** Tried to read an object with a different version of the class.  
  
    > [!NOTE]
    >  These `CArchiveException` cause enumerators are distinct from the `CFileException` cause enumerators.  
  
    > [!NOTE]
    >  **CArchiveException::generic** is deprecated. Use **genericException** instead. If **generic** is used in an application and built with /clr, there will be syntax errors that are not easy to decipher.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)