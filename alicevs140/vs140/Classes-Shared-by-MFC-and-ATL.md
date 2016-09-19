---
title: "Classes Shared by MFC and ATL"
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
ms.assetid: ca8b4b6b-744d-430b-b31f-d5b2f17bf210
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Classes Shared by MFC and ATL
The following table lists the classes shared between MFC and ATL.  
  
|Class|Description|Header file|  
|-----------|-----------------|-----------------|  
|[CFileTime](../vs140/CFileTime-Class.md)|Provides methods for managing the date and time values associated with a file.|atltime.h|  
|[CFileTimeSpan](../vs140/CFileTimeSpan-Class.md)|Provides methods for managing relative date and time values associated with a file.|atltime.h|  
|[CFixedStringT](../vs140/CFixedStringT-Class.md)|Represents a string object with a fixed character buffer.|cstringt.h|  
|[CImage](../vs140/CImage-Class.md)|Provides enhanced bitmap support, including the ability to load and save images in JPEG, GIF, BMP, and Portable Network Graphics (PNG) formats.|atlimage.h|  
|[COleDateTime](../vs140/COleDateTime-Class.md)|Encapsulates the **DATE** data type used in OLE automation.|atlcomtime.h|  
|[COleDateTimeSpan](../vs140/COleDateTimeSpan-Class.md)|Represents a relative time, a time span.|atlcomtime.h|  
|[CPoint](../vs140/CPoint-Class.md)|A class similar to the Windows [POINT](../vs140/POINT-Structure.md) structure that also includes member functions to manipulate `CPoint` and **POINT** structures.|atltypes.h|  
|[CRect](../vs140/CRect-Class.md)|A class similar to a Windows [RECT](../vs140/RECT-Structure.md) structure that also includes member functions to manipulate `CRect` objects and Windows `RECT` structures.|atltypes.h|  
|[CSimpleStringT](../vs140/CSimpleStringT-Class.md)|Represents a `CSimpleStringT` object.|atlsimpstr.h|  
|[CSize](../vs140/CSize-Class.md)|A class similar to the Windows SIZE structure, which implements a relative coordinate or position.|atltypes.h|  
|[CStrBufT](../vs140/CStrBufT-Class.md)|Provides automatic resource cleanup for `GetBuffer` and `ReleaseBuffer` calls on a existing `CStringT` object.|atlsimpstr.h|  
|[CStringData](../vs140/CStringData-Class.md)|Represents the data of a string object.|atlsimpstr.h|  
|[CStringT](../vs140/CStringT-Class.md)|Represents a `CStringT` object.|cstringt.h (MFC dependent) atlstr.h (MFC independent)|  
|[CTime](../Topic/CTime%20Class.md)|Represents an absolute time and date.|atltime.h|  
|[CTimeSpan](../vs140/CTimeSpan-Class.md)|An amount of time, which is internally stored as the number of seconds in the time span.|atltime.h|  
|[IAtlStringMgr](../vs140/IAtlStringMgr-Class.md)|Represents the interface to a `CStringT` memory manager.|atlsimpstr.h|  
  
## See Also  
 [ATL/MFC Shared Classes](../vs140/ATL-MFC-Shared-Classes.md)