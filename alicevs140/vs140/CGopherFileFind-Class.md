---
title: "CGopherFileFind Class"
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
ms.assetid: 8465a979-6323-496d-ab4b-e81383fb999d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFileFind Class
Aids in Internet file searches of gopher servers.  
  
> [!NOTE]
>  The classes `CGopherConnection`, `CGopherFile`, `CGopherFileFind`, `CGopherLocator` and their members have been deprecated because they do not work on the Windows XP platform, but they will continue to work on earlier platforms.  
  
## Syntax  
  
```  
class CGopherFileFind : public CFileFind  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CGopherFileFind::CGopherFileFind](#cgopherfilefind__cgopherfilefind)|Constructs a `CGopherFileFind` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CGopherFileFind::FindFile](#cgopherfilefind__findfile)|Finds a file on a gopher server.|  
|[CGopherFileFind::FindNextFile](#cgopherfilefind__findnextfile)|Continues a file search from a previous call to [FindFile](#cgopherfilefind__findfile).|  
|[CGopherFileFind::GetCreationTime](#cgopherfilefind__getcreationtime)|Gets the time the specified file was created.|  
|[CGopherFileFind::GetLastAccessTime](#cgopherfilefind__getlastaccesstime)|Gets the time the specified file was last accessed.|  
|[CGopherFileFind::GetLastWriteTime](#cgopherfilefind__getlastwritetime)|Gets the time the specified file was last written to.|  
|[CGopherFileFind::GetLength](#cgopherfilefind__getlength)|Gets the length of the found file, in bytes.|  
|[CGopherFileFind::GetLocator](#cgopherfilefind__getlocator)|Get a `CGopherLocator` object.|  
|[CGopherFileFind::GetScreenName](#cgopherfilefind__getscreenname)|Gets the name of a gopher screen.|  
|[CGopherFileFind::IsDots](#cgopherfilefind__isdots)|Tests for the current directory and parent directory markers while iterating through files.|  
  
## Remarks  
 `CGopherFileFind` includes member functions that begin a search, locate a file, and return a file's URL.  
  
 Other MFC classes designed for Internet and local file searched include [CFtpFileFind](../vs140/CFtpFileFind-Class.md) and [CFileFind](../vs140/CFileFind-Class.md). Together with `CGopherFileFind`, these classes provide a seamless mechanism for the user to find specific files, regardless of the server protocol, file type, or location (either a local machine or a remote server.) Note that there is no MFC class for searching on HTTP servers because HTTP does not support the direct file manipulation required by searches.  
  
> [!NOTE]
>  `CGopherFileFind` does not support the following member functions of its base class [CFileFind](../vs140/CFileFind-Class.md):  
  
-   [GetRoot](../vs140/CFileFind-Class.md#cfilefind__getroot)  
  
-   [GetFileName](../vs140/CFileFind-Class.md#cfilefind__getfilename)  
  
-   [GetFilePath](../vs140/CFileFind-Class.md#cfilefind__getfilepath)  
  
-   [GetFileTitle](../vs140/CFileFind-Class.md#cfilefind__getfiletitle)  
  
-   [GetFileURL](../vs140/CFileFind-Class.md#cfilefind__getfileurl)  
  
 In addition, when used with `CGopherFileFind`, the `CFileFind` member function [IsDots](../vs140/CFileFind-Class.md#cfilefind__isdots) is always **FALSE**.  
  
 For more information about how to use `CGopherFileFind` and the other WinInet classes, see the article [Internet Programming with WinInet](../vs140/Win32-Internet-Extensions--WinInet-.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CFileFind](../vs140/CFileFind-Class.md)  
  
 `CGopherFileFind`  
  
## Requirements  
 **Header:** afxinet.h  
  
##  <a name="cgopherfilefind__cgopherfilefind"></a>  CGopherFileFind::CGopherFileFind  
 This member function is called to construct a `CGopherFileFind` object.  
  
```  
explicit CGopherFileFind(    CGopherConnection*  pConnection ,    DWORD_PTR  dwContext  = 1  );  
  
```  
  
### Parameters  
 `pConnection`  
 A pointer to a [CGopherConnection](../vs140/CGopherConnection-Class.md) object.  
  
 `dwContext`  
 The context identifier for the operation. See **Remarks** for more information about `dwContext`.  
  
### Remarks  
 The default value for `dwContext` is sent by MFC to the `CGopherFileFind` object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the `CGopherFileFind` object. When you construct a `CGopherFileFind` object, you can override the default to set the context identifier to a value of your choosing. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession-Class.md#cinternetsession__onstatuscallback) to provide status on the object with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
##  <a name="cgopherfilefind__findfile"></a>  CGopherFileFind::FindFile  
 Call this member function to find a gopher file.  
  
```  
virtual BOOL FindFile(    CGopherLocator&  refLocator ,    LPCTSTR  pstrString ,    DWORD  dwFlags  = INTERNET_FLAG_RELOAD  ); virtual BOOL FindFile(    LPCTSTR  pstrString ,    DWORD  dwFlags  = INTERNET_FLAG_RELOAD  );  
  
```  
  
### Parameters  
 `refLocator`  
 A reference to a [CGopherLocator](../vs140/CGopherLocator-Class.md) object.  
  
 *pstrString*  
 A pointer to a string containing the file name.  
  
 `dwFlags`  
 The flags describing how to handle this session. The valid flags are:  
  
-   INTERNET_FLAG_RELOAD   Get the data from the remote server even if it is locally cached.  
  
-   INTERNET_FLAG_DONT_CACHE   Do not cache the data, either locally or in any gateways.  
  
-   INTERNET_FLAG_SECURE   Request secure transactions on the wire with Secure Sockets Layer or PCT. This flag is applicable to HTTP requests only.  
  
-   INTERNET_FLAG_USE_EXISTING   If possible, reuse the existing connections to the server for new **FindFile** requests, instead of creating a new session for each request.  
  
### Return Value  
 Nonzero if successful; otherwise 0. To get extended error information, call the Win32 function                         [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360).  
  
### Remarks  
 After calling **FindFile** to retrieve the first gopher object, you can call [FindNextFile](#cgopherfilefind__findnextfile) to retrieve subsequent gopher files.  
  
##  <a name="cgopherfilefind__findnextfile"></a>  CGopherFileFind::FindNextFile  
 Call this member function to continue a file search begun with a call to [CGopherFileFind::FindFile](#cgopherfilefind__findfile).  
  
```  
virtual BOOL FindNextFile( );  
  
```  
  
### Return Value  
 Nonzero if there are more files; zero if the file found is the last one in the directory or if an error occurred. To get extended error information, call the Win32 function                         [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360). If the file found is the last file in the directory, or if no matching files can be found, the `GetLastError` function returns ERROR_NO_MORE_FILES.  
  
##  <a name="cgopherfilefind__getcreationtime"></a>  CGopherFileFind::GetCreationTime  
 Gets the creation time for the current file.  
  
```  
virtual BOOL GetCreationTime(    FILETIME*  pTimeStamp ) const; virtual BOOL GetCreationTime(    CTime&  refTime ) const;  
  
```  
  
### Parameters  
 `pTimeStamp`  
 A pointer to a                                 [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure containing the time the file was created.  
  
 `refTime`  
 A reference to a [CTime](../Topic/CTime%20Class.md) object.  
  
### Return Value  
 Nonzero if successful; 0 if unsuccessful. `GetCreationTime` returns 0 only if [FindNextFile](#cgopherfilefind__findnextfile) has never been called on this `CGopherFileFind` object.  
  
### Remarks  
 You must call [FindNextFile](#cgopherfilefind__findnextfile) at least once before calling `GetCreationTime`.  
  
> [!NOTE]
>  Not all file systems use the same semantics to implement the time stamp returned by this function. This function may return the same value returned by other time stamp functions if the underlying file system or server does not support keeping the time attribute. See the                             [Win32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure for information about time formats. On some operating systems, the returned time is in the time zone local to the machine were the file is located. See the Win32                             [FileTimeToLocalFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724277) API for more information.  
  
##  <a name="cgopherfilefind__getlastaccesstime"></a>  CGopherFileFind::GetLastAccessTime  
 Gets the time the specified file was last accessed.  
  
```  
virtual BOOL GetLastAccessTime(    CTime&  refTime ) const; virtual BOOL GetLastAccessTime(    FILETIME*  pTimeStamp ) const;  
  
```  
  
### Parameters  
 `refTime`  
 A reference to a [CTime](../Topic/CTime%20Class.md) object.  
  
 `pTimeStamp`  
 A pointer to a                                 [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure containing the time the file was last accessed.  
  
### Return Value  
 Nonzero if successful; 0 if unsuccessful. `GetLastAccessTime` returns 0 only if [FindNextFile](#cgopherfilefind__findnextfile) has never been called on this `CGopherFileFind` object.  
  
### Remarks  
 You must call [FindNextFile](#cgopherfilefind__findnextfile) at least once before calling `GetLastAccessTime`.  
  
> [!NOTE]
>  Not all file systems use the same semantics to implement the time stamp returned by this function. This function may return the same value returned by other time stamp functions if the underlying file system or server does not support keeping the time attribute. See the                             [Win32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure for information about time formats. On some operating systems, the returned time is in the time zone local to the machine were the file is located. See the Win32                             [FileTimeToLocalFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724277) API for more information.  
  
##  <a name="cgopherfilefind__getlastwritetime"></a>  CGopherFileFind::GetLastWriteTime  
 Gets the last time the file was changed.  
  
```  
virtual BOOL GetLastWriteTime(    FILETIME*  pTimeStamp ) const; virtual BOOL GetLastWriteTime(    CTime&  refTime ) const;  
  
```  
  
### Parameters  
 `pTimeStamp`  
 A pointer to a                                 [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure containing the time the file was last written to.  
  
 `refTime`  
 A reference to a [CTime](../Topic/CTime%20Class.md) object.  
  
### Return Value  
 Nonzero if successful; 0 if unsuccessful. `GetLastWriteTime` returns 0 only if [FindNextFile](#cgopherfilefind__findnextfile) has never been called on this `CGopherFileFind` object.  
  
### Remarks  
 You must call [FindNextFile](#cgopherfilefind__findnextfile) at least once before calling `GetLastWriteTime`.  
  
> [!NOTE]
>  Not all file systems use the same semantics to implement the time stamp returned by this function. This function may return the same value returned by other time stamp functions if the underlying file system or server does not support keeping the time attribute. See the                             [Win32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure for information about time formats. On some operating systems, the returned time is in the time zone local to the machine were the file is located. See the Win32                             [FileTimeToLocalFileTime](http://msdn.microsoft.com/library/windows/desktop/ms724277) API for more information.  
  
##  <a name="cgopherfilefind__getlength"></a>  CGopherFileFind::GetLength  
 Call this member function to get the length, in bytes, of the found file.  
  
```  
virtual ULONGLONG GetLength( ) const;  
  
```  
  
### Return Value  
 The length, in bytes, of the found file.  
  
### Remarks  
 `GetLength` uses the Win32 structure                         [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) to get the value of the file size in bytes.  
  
> [!NOTE]
>  As of MFC 7.0, `GetLength` supports 64-bit integer types. Previously-existing code built with this newer version of the library may result in truncation warnings.  
  
### Example  
  See the example for [CFile::GetLength](../vs140/CFile-Class.md#cfile__getlength) (the base class implementation).  
  
##  <a name="cgopherfilefind__getlocator"></a>  CGopherFileFind::GetLocator  
 Call this member function to get the [CGopherLocator](../vs140/CGopherLocator-Class.md) object that [FindFile](#cgopherfilefind__findfile) uses to find the gopher file.  
  
```  
CGopherLocator GetLocator( ) const;  
  
```  
  
### Return Value  
 A `CGopherLocator` object.  
  
##  <a name="cgopherfilefind__getscreenname"></a>  CGopherFileFind::GetScreenName  
 Call this member function to get the name of the gopher screen.  
  
```  
CString GetScreenName( ) const;  
  
```  
  
### Return Value  
 The name of the gopher screen.  
  
##  <a name="cgopherfilefind__isdots"></a>  CGopherFileFind::IsDots  
 Tests for the current directory and parent directory markers while iterating through files.  
  
```  
virtual BOOL IsDots( ) const;  
  
```  
  
### Return Value  
 Nonzero if the found file has the name "." or "..", which indicates that the found file is actually a directory. Otherwise 0.  
  
### Remarks  
 You must call [FindNextFile](#cgopherfilefind__findnextfile) at least once before calling `IsDots`.  
  
## See Also  
 [Base Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpFileFind](../vs140/CFtpFileFind-Class.md)   
 [CFileFind](../vs140/CFileFind-Class.md)   
 [CInternetFile](../vs140/CInternetFile-Class.md)   
 [CGopherFile](../vs140/CGopherFile-Class.md)   
 [CHttpFile](../vs140/CHttpFile-Class.md)