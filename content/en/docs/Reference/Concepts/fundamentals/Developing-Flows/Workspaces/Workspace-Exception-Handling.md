---
title: "Workspace Exception Handling"
linkTitle: "Workspace Exception Handling"
description: "Handling exceptions at the Workspace level."
weight: 30
---

# {{< param title >}}

## Summary

Flows can provide for a range of exception handling techniques:

* Exceptions can be handled at the [block level][Block-Level] (Highest Priority)
* Exceptions can be handled at the [workspace level][Workspace-Level]
* Exceptions can be handled at the [flow level][Flow-Level] (Lowest Priority)

A single [Handle Workspace Exception][Block-Handle-Workspace-Exception] [block][What-Is-Block] may be placed on a [workspace][What-Is-Workspace], handling exceptions at the [workspace level][Workspace-Level].

It acts as a common point for handling exceptions on the workspace that are not caught by the higher priority [Handle Block Exception][Block-Handle-Block-Exception] [blocks][What-Is-Block].

For detailed information about Workspace Exception Handling, see [Handling Exceptions at the Workspace Level][Workspace-Level].

## Related Concepts

* [Flows][Flow]
* [Workspaces][What-Is-Workspace]
* [Blocks][Block]
* [Execution Exceptions][Exceptions]

## Related Blocks

* [Handle Workspace Exception][Block-Handle-Workspace-Exception]
* [Handle Block Exception][Block-Handle-Block-Exception]

[Block]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Blocks.MainDoc" >}}
[Block-Exception-Handling]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Blocks.BlockExceptionHandling.MainDoc" >}}
[Block-Handle-Block-Exception]: {{< url "Cortex.Reference.Blocks.Exceptions.HandleBlock.HandleBlockException.MainDoc" >}}
[Block-Handle-Flow-Exception]: {{< url "Cortex.Reference.Blocks.Exceptions.HandleFlow.HandleFlowException.MainDoc" >}}
[Block-Handle-Workspace-Exception]: {{< url "Cortex.Reference.Blocks.Exceptions.HandleWorkspace.HandleWorkspaceException.MainDoc" >}}
[Block-Throw-Exception]: {{< url "Cortex.Reference.Blocks.Exceptions.ThrowException.ThrowNewFlowException.MainDoc" >}}
[Block-Workspace-Block]: {{< url "Cortex.Reference.Blocks.Workspaces.Workspace.WorkspaceBlock.MainDoc" >}}
[Flow]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Flows.MainDoc" >}}
[Flow-Exception-Handling]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Flows.Flow-Exception-Handling.MainDoc" >}}
[Workspace]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Workspaces.MainDoc" >}}

[What-Is-Block]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Blocks.WhatIsABlock.MainDoc" >}}
[What-Is-Execution]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Executions.What-Is-An-Execution.MainDoc" >}}
[What-Is-Workspace]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Workspaces.What-Is-A-Workspace.MainDoc" >}}

[Exceptions]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Executions.Exceptions.MainDoc" >}}
[Block-Level]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Executions.Exceptions.Block-Level" >}}
[Flow-Level]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Executions.Exceptions.Flow-Level" >}}
[Workspace-Level]: {{< url "Cortex.Reference.Concepts.Fundamentals.DevelopingFlows.Executions.Exceptions.Workspace-Level" >}}