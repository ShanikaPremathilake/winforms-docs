---
title: Removing items
page_title: Removing items
description: Removing items
slug: diagram-items-manipulation-removing-items
tags: removing,items
published: True
position: 4
---

# Removing items



__RadDiagram__ gives you the ability to remove __RadDiagramItems__ interactively, 
        programmatically or with __DiagramCommands__.

## Removing Items Interactively

You can remove the selected __RadDiagramItems__ by pressing the Delete Key.

Below you can see the result of delete operation over the selected __RadDiagramItems__:![diagram-items-manipulation-removing-items 001](images/diagram-items-manipulation-removing-items001.gif)

## Removing Items in code behind

You can remove __RadDiagramItems__ in code behind by using the RadDiagram.__Items__ 
        collection and its __Remove()__ or __RemoveAt()__ methods:

#### __[C#] __

{{source=..\SamplesCS\Diagram\DiagramItemsManipulation.cs region=RemoveItems}}
	            
	            this.radDiagram1.Items.RemoveAt(2);
	            this.radDiagram1.Items.Remove(shape1);
	
	{{endregion}}



#### __[VB.NET] __

{{source=..\SamplesVB\Diagram\DiagramItemsManipulation.vb region=RemoveItems}}
	        Me.RadDiagram1.Items.RemoveAt(2)
	        Me.RadDiagram1.Items.Remove(shape1)
	{{endregion}}



## Delete with DiagramCommands

You can use the __DiagramCommand__ "Delete" in order to remove the selected __RadDiagramItems__.

#### __[C#] __

{{source=..\SamplesCS\Diagram\DiagramItemsManipulation.cs region=DeleteCommands}}
	            
	            this.radDiagram1.SelectedItem = shape1;
	            this.radDiagram1.DiagramElement.TryExecuteCommand(DiagramCommands.Delete, "");
	            
	{{endregion}}



#### __[VB.NET] __

{{source=..\SamplesVB\Diagram\DiagramItemsManipulation.vb region=DeleteCommands}}
	
	        Me.RadDiagram1.SelectedItem = shape1
	        Me.RadDiagram1.DiagramElement.TryExecuteCommand(DiagramCommands.Delete, "")
	
	{{endregion}}

