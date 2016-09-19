---
title: "CMonikerFile Class"
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
ms.assetid: 87be5966-f4f7-4235-bce2-1fa39e9417de
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonikerFile Class
Represents a stream of data (            [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034)) named by an             [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705).  
  
## Syntax  
  
```  
class CMonikerFile : public COleStreamFile  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMonikerFile::CMonikerFile](#cmonikerfile__cmonikerfile)|Constructs a `CMonikerFile` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMonikerFile::Close](#cmonikerfile__close)|Detaches and releases the stream and releases the moniker.|  
|[CMonikerFile::Detach](#cmonikerfile__detach)|Detaches the `IMoniker` from this `CMonikerFile` object.|  
|[CMonikerFile::GetMoniker](#cmonikerfile__getmoniker)|Returns the current moniker.|  
|[CMonikerFile::Open](#cmonikerfile__open)|Opens the specified file to obtain a stream.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMonikerFile::CreateBindContext](#cmonikerfile__createbindcontext)|Obtains the bind context or creates a default initialized bind context.|  
  
## Remarks  
 A moniker contains information much like a pathname to a file. If you have a pointer to a moniker object's `IMoniker` interface, you can get access to the identified file without having any other specific information about where the file is actually located.  
  
 Derived from `COleStreamFile`, `CMonikerFile` takes a moniker or a string representation it can make into a moniker and binds to the stream for which the moniker is a name. You can then read and write to that stream. The real purpose of `CMonikerFile` is to provide simple access to `IStream`s named by `IMoniker`s so that you do not have to bind to a stream yourself, yet have `CFile` functionality to the stream.  
  
 `CMonikerFile` cannot be used to bind to anything other than a stream. If you want to bind to storage or an object, you must use the `IMoniker` interface directly.  
  
 For more information on streams and monikers, see [COleStreamFile](../vs140/COleStreamFile-Class.md) in the                 *MFC Reference* and                 [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) and                 [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CFile](../vs140/CFile-Class.md)  
  
 [COleStreamFile](../vs140/COleStreamFile-Class.md)  
  
 `CMonikerFile`  
  
## Requirements  
 **Header:** afxole.h  
  
##  <a name="cmonikerfile__close"></a>  CMonikerFile::Close  
 Call this function to detach and release the stream and to release the moniker.  
  
```  
virtual void Close( );  
  
```  
  
### Remarks  
 Can be called on unopened or already closed streams.  
  
##  <a name="cmonikerfile__cmonikerfile"></a>  CMonikerFile::CMonikerFile  
 Constructs a `CMonikerFile` object.  
  
```  
CMonikerFile( );  
  
```  
  
##  <a name="cmonikerfile__createbindcontext"></a>  CMonikerFile::CreateBindContext  
 Call this function to create a default initialized bind context.  
  
```  
IBindCtx* CreateBindContext(    CFileException*  pError );  
  
```  
  
### Parameters  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
### Return Value  
 A pointer to the bind context                         [IBindCtx](http://msdn.microsoft.com/library/windows/desktop/ms693755) to bind with if successful; otherwise **NULL**. If the instance was opened with an `IBindHost` interface, the bind context is retrieved from the `IBindHost`. If there is no `IBindHost` interface or the interface fails to return a bind context, a bind context is created. For a description of the                         [IBindHost](http://msdn.microsoft.com/library/ie/ms775076) interface, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Remarks  
 A bind context is an object that stores information about a particular moniker binding operation. You can override this function to provide a custom bind context.  
  
##  <a name="cmonikerfile__detach"></a>  CMonikerFile::Detach  
 Call this function to close the stream.  
  
```  
BOOL Detach(    CFileException* pError = NULL );  
  
```  
  
### Parameters  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
### Return Value  
 Nonzero if successful; otherwise 0.  
  
##  <a name="cmonikerfile__getmoniker"></a>  CMonikerFile::GetMoniker  
 Call this function to retrieve a pointer to the current moniker.  
  
```  
IMoniker* GetMoniker( ) const;  
  
```  
  
### Return Value  
 A pointer to the current moniker interface (                        [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705)).  
  
### Remarks  
 Since `CMonikerFile` is not an interface, the pointer returned does not increment the reference count (through                         [AddRef](http://msdn.microsoft.com/library/windows/desktop/ms691379)), and the moniker is released when the `CMonikerFile` object is released. If you want to hold onto the moniker or release it yourself, you must `AddRef` it.  
  
##  <a name="cmonikerfile__open"></a>  CMonikerFile::Open  
 Call this member function to open a file or moniker object.  
  
```  
virtual BOOL Open(    LPCTSTR lpszURL ,    CFileException* pError = NULL ); virtual BOOL Open(    IMoniker* pMoniker ,    CFileException* pError = NULL );  
  
```  
  
### Parameters  
 `lpszURL`  
 A URL or filename of the file to be opened.  
  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
 `pMoniker`  
 A pointer to the moniker interface `IMoniker` to be used to obtain a stream.  
  
### Return Value  
 Nonzero if successful; otherwise 0.  
  
### Remarks  
 The `lpszURL` parameter cannot be used on a Macintosh. Only the `pMoniker` form of **Open** can be used on a Macintosh.  
  
 You can use a URL or a filename for the `lpszURL` parameter. For example:  
  
 [!CODE [NVC_MFCWinInet#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#6)]  
  
 – or –  
  
 [!CODE [NVC_MFCWinInet#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#7)]  
  
## See Also  
 [Base Class](../vs140/COleStreamFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncMonikerFile](../vs140/CAsyncMonikerFile-Class.md)