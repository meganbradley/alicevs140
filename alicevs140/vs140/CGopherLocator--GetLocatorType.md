---
title: "CGopherLocator::GetLocatorType"
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
ms.assetid: 51bf9225-0417-4d93-beb0-18185dd32144
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherLocator::GetLocatorType
Call this member function to get the locator type.  
  
## Syntax  
  
```  
  
      BOOL GetLocatorType(  
   DWORD& dwRef   
) const;  
```  
  
#### Parameters  
 *dwRef*  
 A reference to a `DWORD` that will receive the locator type. See **Remarks** for a table of locator types.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
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
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherLocator Class](../vs140/CGopherLocator-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)