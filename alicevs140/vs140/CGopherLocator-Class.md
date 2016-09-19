---
title: "CGopherLocator Class"
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
ms.assetid: 6fcc015f-5ae6-4959-b936-858634c71019
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherLocator Class
Gets a gopher "locator" from a gopher server, determines the locator's type, and makes the locator available to [CGopherFileFind](../vs140/CGopherFileFind-Class.md).  
  
> [!NOTE]
>  The classes `CGopherConnection`, `CGopherFile`, `CGopherFileFind`, `CGopherLocator` and their members have been deprecated because they do not work on the Windows XP platform, but they will continue to work on earlier platforms.  
  
## Syntax  
  
```  
class CGopherLocator : public CObject  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CGopherLocator::CGopherLocator](#cgopherlocator__cgopherlocator)|Constructs a `CGopherLocator` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CGopherLocator::GetLocatorType](#cgopherlocator__getlocatortype)|Parses a gopher locator and determines its attributes.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CGopherLocator::operator LPCTSTR](#cgopherlocator__operator_lpctstr)|Directly accesses characters stored in a `CGopherLocator` object as a C-style string.|  
  
## Remarks  
 An application must get a gopher server's locator before it can retrieve information from that server. Once it has the locator, it must treat the locator as an opaque token.  
  
 Each gopher locator has attributes that determine the type of file or server found. See [GetLocatorType](#cgopherlocator__getlocatortype) for a list of types of gopher locators.  
  
 An application normally uses the locator for calls to [CGopherFileFind::FindFile](../vs140/CGopherFileFind-Class.md#cgopherfilefind__findfile) to retrieve a specific piece of information.  
  
 To learn more about how `CGopherLocator` works with the other MFC Internet classes, see the article [Internet Programming with WinInet](../vs140/Win32-Internet-Extensions--WinInet-.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 `CGopherLocator`  
  
## Requirements  
 **Header:** afxinet.h  
  
##  <a name="cgopherlocator__cgopherlocator"></a>  CGopherLocator::CGopherLocator  
 This member function is called to create a `CGopherLocator` object.  
  
```  
CGopherLocator(    const CGopherLocator&  ref );  
  
```  
  
### Parameters  
 `ref`  
 A reference to a constant `CGopherLocator` object.  
  
### Remarks  
 You never create a `CGopherLocator` object directly. Instead, call [CGopherConnection::CreateLocator](../vs140/CGopherConnection-Class.md#cgopherconnection__createlocator) to create and return a pointer to the `CGopherLocator` object.  
  
##  <a name="cgopherlocator__getlocatortype"></a>  CGopherLocator::GetLocatorType  
 Call this member function to get the locator type.  
  
```  
BOOL GetLocatorType(    DWORD&  dwRef ) const;  
  
```  
  
### Parameters  
 *dwRef*  
 A reference to a `DWORD` that will receive the locator type. See **Remarks** for a table of locator types.  
  
### Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function                         [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
### Remarks  
 The possible types are as follows:  
  
|Value|Meaning|  
|-----------|-------------|  
|GOPHER_TYPE_TEXT_FILE|An ASCII text file.|  
|GOPHER_TYPE_DIRECTORY|A directory of additional Gopher items.|  
|GOPHER_TYPE_CSO|A CSO phone book server.|  
|GOPHER_TYPE_ERROR|Indicates an error condition.|  
|GOPHER_TYPE_MAC_BINHEX|A Macintosh file in BINHEX format.|  
|GOPHER_TYPE_DOS_ARCHIVE|A DOS archive file.|  
|GOPHER_TYPE_UNIX_UUENCODED|A UUENCODED file.|  
|GOPHER_TYPE_INDEX_SERVER|An index server.|  
|GOPHER_TYPE_TELNET|A Telnet Server.|  
|GOPHER_TYPE_BINARY|A binary file.|  
|GOPHER_TYPE_REDUNDANT|A duplicated server. The information contained within is a duplicate of the primary server. The primary server is the last directory entry that did not have a GOPHER_TYPE_REDUNDANT type.|  
|GOPHER_TYPE_TN3270|A TN3270 server.|  
|GOPHER_TYPE_GIF|A GIF graphics file.|  
|GOPHER_TYPE_IMAGE|An image file.|  
|GOPHER_TYPE_BITMAP|A bitmap file.|  
|GOPHER_TYPE_MOVIE|A movie file.|  
|GOPHER_TYPE_SOUND|A sound file.|  
|GOPHER_TYPE_HTML|An HTML document.|  
|GOPHER_TYPE_PDF|A PDF file.|  
|GOPHER_TYPE_CALENDAR|A calendar file.|  
|GOPHER_TYPE_INLINE|An inline file.|  
|GOPHER_TYPE_UNKNOWN|The item type is unknown.|  
|GOPHER_TYPE_ASK|An Ask+ item.|  
|GOPHER_TYPE_GOPHER_PLUS|A Gopher+ item.|  
  
##  <a name="cgopherlocator__operator_lpctstr"></a>  CGopherLocator::operator LPCTSTR  
 This useful casting operator provides an efficient method to access the null-terminated C string contained in a `CGopherLocator` object.  
  
```  
operator LPCTSTR ( ) const;  
  
```  
  
### Return Value  
 A character pointer to the string's data.  
  
### Remarks  
 No characters are copied; only a pointer is returned.  
  
## See Also  
 [Base Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGopherFileFind](../vs140/CGopherFileFind-Class.md)