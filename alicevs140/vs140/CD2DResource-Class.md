---
title: "CD2DResource Class"
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
ms.assetid: 34e3ee18-aab6-4c39-9294-de869e1f7820
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DResource Class
An abstract class that provides a interface for creating and managing D2D resources such as brushes, layers, and texts.  
  
## Syntax  
  
```  
class CD2DResource : public CObject;  
```  
  
## Members  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DResource::CD2DResource](#cd2dresource__cd2dresource)|Constructs a CD2DResource object.|  
|[CD2DResource::~CD2DResource](#cd2dresource__~cd2dresource)|The destructor. Called when a D2D resource object is being destroyed.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DResource::Create](#cd2dresource__create)|Creates a CD2DResource.|  
|[CD2DResource::Destroy](#cd2dresource__destroy)|Destroys a CD2DResource object.|  
|[CD2DResource::IsValid](#cd2dresource__isvalid)|Checks resource validity|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DResource::IsAutoDestroy](#cd2dresource__isautodestroy)|Check auto destroy flag.|  
|[CD2DResource::ReCreate](#cd2dresource__recreate)|Re-creates a CD2DResource.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CD2DResource::m_bIsAutoDestroy](#cd2dresource__m_bisautodestroy)|Resource will be destoyed by owner (CRenderTarget)|  
|[CD2DResource::m_pParentTarget](#cd2dresource__m_pparenttarget)|Pointer to the parent CRenderTarget)|  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CD2DResource](../vs140/CD2DResource-Class.md)  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
##  <a name="cd2dresource___dtorcd2dresource"></a>  CD2DResource::~CD2DResource  
 The destructor. Called when a D2D resource object is being destroyed.  
  
```  
virtual ~CD2DResource();  
```  
  
##  <a name="cd2dresource__cd2dresource"></a>  CD2DResource::CD2DResource  
 Constructs a CD2DResource object.  
  
```  
CD2DResource(  
   CRenderTarget* pParentTarget,  
   BOOL bAutoDestroy  
);  
```  
  
### Parameters  
 `pParentTarget`  
 A pointer to the render target.  
  
 `bAutoDestroy`  
 Indicates that the object will be destroyed by owner (pParentTarget).  
  
##  <a name="cd2dresource__create"></a>  CD2DResource::Create  
 Creates a CD2DResource.  
  
```  
virtual HRESULT Create(  
   CRenderTarget* pRenderTarget  
) = 0;  
```  
  
### Parameters  
 `pRenderTarget`  
 A pointer to the render target.  
  
### Return Value  
 If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.  
  
##  <a name="cd2dresource__destroy"></a>  CD2DResource::Destroy  
 Destroys a CD2DResource object.  
  
```  
virtual void Destroy() = 0;  
```  
  
##  <a name="cd2dresource__isautodestroy"></a>  CD2DResource::IsAutoDestroy  
 Check auto destroy flag.  
  
```  
BOOL IsAutoDestroy() const;  
```  
  
### Return Value  
 TRUE if the object will be destroyed by its owner; otherwise FALSE.  
  
##  <a name="cd2dresource__isvalid"></a>  CD2DResource::IsValid  
 Checks resource validity  
  
```  
virtual BOOL IsValid() const = 0;  
```  
  
### Return Value  
 TRUE if resource is valid; otherwise FALSE.  
  
##  <a name="cd2dresource__m_bisautodestroy"></a>  CD2DResource::m_bIsAutoDestroy  
 Resource will be destoyed by owner (CRenderTarget)  
  
```  
BOOL m_bIsAutoDestroy;  
```  
  
##  <a name="cd2dresource__m_pparenttarget"></a>  CD2DResource::m_pParentTarget  
 Pointer to the parent CRenderTarget)  
  
```  
CRenderTarget* m_pParentTarget;  
```  
  
##  <a name="cd2dresource__recreate"></a>  CD2DResource::ReCreate  
 Re-creates a CD2DResource.  
  
```  
virtual HRESULT ReCreate(  
   CRenderTarget* pRenderTarget  
);  
```  
  
### Parameters  
 `pRenderTarget`  
 A pointer to the render target.  
  
### Return Value  
 If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.  
  
## See Also  
 [MFC Classes](../vs140/MFC-Classes.md)