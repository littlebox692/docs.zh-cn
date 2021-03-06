---
title: "如何：添加对类型库的引用 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "COM 互操作, 导入类型库"
  - "导入类型库"
  - "互操作程序集, 生成"
  - "类型库"
ms.assetid: f5cfa6ba-cc25-4017-82cd-ba7391859113
caps.latest.revision: 12
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 12
---
# 如何：添加对类型库的引用
当添加对类型库的引用时，Visual Studio 将生成包含元数据的互操作程序集。  如果主互操作程序集可用，则 Visual Studio 在生成新的互操作程序集之前将使用现有程序集。  
  
### 在 Visual Studio 中添加对类型库的引用  
  
1.  在计算机上安装 COM DLL 或 EXE 文件，除非 Windows Setup.exe 文件会为你执行此安装。  
  
2.  依次选择**“项目”**、**“添加引用”**。  
  
3.  在“引用管理器”中，选择**“COM”**。  
  
4.  从列表中选择类型库，或通过浏览选择 .tlb 文件。  
  
5.  选择**“确定”**。  
  
6.  在“解决方案资源管理器”中，打开刚刚添加的引用的快捷菜单，然后选择**“属性”**。  
  
7.  在**“属性”**窗口中，确保将**“嵌入互操作类型”**属性设置为**“True”**。  通过此设置，Visual Studio 将会在可执行文件中嵌入 COM 类型的类型信息，从而不必将主互操作程序集与你的应用一起部署。  
  
> [!NOTE]
>  根据你使用的 Visual Studio 版本，菜单和对话框选项可能会有所不同。  
  
### 添加对类型库的引用以进行命令行编译  
  
1.  如[如何：从类型库生成互操作程序集](../../../docs/framework/interop/how-to-generate-interop-assemblies-from-type-libraries.md)中所述，生成一个互操作程序集。  
  
2.  将 [\/link \(Link to COM Assembly\)](../Topic/-link%20\(C%23%20Compiler%20Options\).md)或 [\/link](../Topic/-link%20\(Visual%20Basic\).md) 编译器选项与互操作程序集名称一起使用，以便将 COM 类型的类型信息嵌入到可执行文件中。  
  
## 请参阅  
 [将类型库当作程序集导入](../../../docs/framework/interop/importing-a-type-library-as-an-assembly.md)   
 [向 .NET Framework 公开 COM 组件](../../../docs/framework/interop/exposing-com-components.md)   
 [演练：嵌入 Microsoft Office 程序集中的类型信息](../Topic/Walkthrough:%20Embedding%20Type%20Information%20from%20Microsoft%20Office%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md)   
 [演练：嵌入托管程序集中的类型](../Topic/Walkthrough:%20Embedding%20Types%20from%20Managed%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md)   
 [\/link \(Link to COM Assembly\)](../Topic/-link%20\(C%23%20Compiler%20Options\).md)   
 [\/link](../Topic/-link%20\(Visual%20Basic\).md)