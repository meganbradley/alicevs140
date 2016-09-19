---
title: "CDC::EnumObjects"
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
ms.assetid: 62703ddf-7eec-4f13-85d6-fef9d6f3df62
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::EnumObjects
Enumerates the pens and brushes available in a device context.  
  
## Syntax  
  
```  
  
      int EnumObjects(  
   int nObjectType,  
   int ( CALLBACK * lpfn )( LPVOID, LPARAM ),  
   LPARAM lpData  
);  
```  
  
#### Parameters  
 *nObjectType*  
 Specifies the object type. It can have the values **OBJ_BRUSH** or **OBJ_PEN**.  
  
 `lpfn`  
 Is the procedure-instance address of the application-supplied callback function. See the "Remarks" section below.  
  
 `lpData`  
 Points to the application-supplied data. The data is passed to the callback function along with the object information.  
  
## Return Value  
 Specifies the last value returned by the [callback function](../vs140/Callback-Function-for-CDC--EnumObjects.md). Its meaning is user-defined.  
  
## Remarks  
 For each object of a given type, the callback function that you pass is called with the information for that object. The system calls the callback function until there are no more objects or the callback function returns 0.  
  
 Note that new features of Microsoft Visual C++ let you use an ordinary function as the function passed to `EnumObjects`. The address passed to `EnumObjects` is a pointer to a function exported with **EXPORT** and with the Pascal calling convention. In protect-mode applications, you do not have to create this function with the Windows [MakeProcInstance](https://msdn.microsoft.com/en-us/library/aa383722.aspx) function or free the function after use with the [FreeProcInstance](https://msdn.microsoft.com/en-us/library/aa383722.aspx) Windows function.  
  
 You also do not have to export the function name in an **EXPORTS** statement in your application's module-definition file. You can instead use the **EXPORT** function modifier, as in  
  
 **int CALLBACK EXPORT** AFunction**( LPSTR**, **LPSTR );**  
  
 to cause the compiler to emit the proper export record for export by name without aliasing. This works for most needs. For some special cases, such as exporting a function by ordinal or aliasing the export, you still need to use an **EXPORTS** statement in a module-definition file.  
  
 For compiling Microsoft Foundation programs, you will normally use the /GA and /GEs compiler options. The /Gw compiler option is not used with the Microsoft Foundation classes. (If you do use the Windows function **MakeProcInstance**, you will need to explicitly cast the returned function pointer from **FARPROC** to the type needed in this API.) Callback registration interfaces are now type-safe (you must pass in a function pointer that points to the right kind of function for the specific callback).  
  
 Also note that all callback functions must trap Microsoft Foundation exceptions before returning to Windows, since exceptions cannot be thrown across callback boundaries. For more information about exceptions, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Example  
 [!CODE [NVC_MFCDocView#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#35)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [EnumObjects](http://msdn.microsoft.com/library/windows/desktop/dd162685)