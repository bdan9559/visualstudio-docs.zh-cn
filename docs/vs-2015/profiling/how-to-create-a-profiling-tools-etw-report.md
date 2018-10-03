---
title: 如何：创建分析工具 ETW 报告 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 93aea1474bb8e8ac215a6eb8e3c8b695d4901cba
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47482269"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>如何：创建分析工具 ETW 报告
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[如何： 创建分析工具 ETW 报告](https://docs.microsoft.com/visualstudio/profiling/how-to-create-a-profiling-tools-etw-report)。  
  
Windows 事件跟踪 (ETW) 报告列出 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 分析工具的性能会话中所记录的 ETW 事件。 在二进制 (.etl) 文件中收集 ETW 数据。 有关此报告的详细信息，请参阅 [Windows 事件跟踪 (ETW) 报告](../profiling/event-tracing-for-windows-etw-report.md)。  
  
> [!NOTE]
>  不能在 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 的接口中显示 ETW 报告。  
  
-   有关如何使用 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 的接口收集 ETW 数据的信息，请参阅[如何：收集 Windows 事件跟踪 (ETW) 数据](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)。  
  
-   有关如何从命令提示符收集 ETW 数据的信息，请参阅 [VSPerfCmd](../profiling/vsperfcmd.md) 和[事件](../profiling/events-vsperfcmd.md)。  
  
 使用 **VSReport/summary:etw** 命令生成 ETW 报告。 包含 ETW 数据的 .etl 必须与分析数据（.vsp 或 .vsps）文件位于同一目录中。 默认情况下，报告将生成为逗号分隔值 (.csv) 文件。 有关详细信息，请参阅 [VSPerfReport](../profiling/vsperfreport.md)。  
  
### <a name="to-generate-an-etw-report"></a>创建 ETW 报告  
  
-   在“命令提示符”窗口中，键入以下命令行：  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/Summary:ETW [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|分析工具实用工具的路径。 有关详细信息，请参阅[指定命令行工具的路径](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)。|  
    |*VSPFile*|分析数据（.vsp 或 .vsps）文件。 接受完整和部分路径。|  
    |Xml|生成 XML 格式的报告。|


