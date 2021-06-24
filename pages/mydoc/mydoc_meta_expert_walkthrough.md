---
title: Walkthrough: Metacontroller and Experts
tags: [tutorial]
keywords: metacontroller
last_updated: June 24, 2021
summary: "Walk through creation of a new metacontroller and expert"
sidebar: mydoc_sidebar
permalink: mydoc_meta_expert_walkthrough.html
folder: mydoc
---
{% include note.html content="DTLight is produced for traffic management. You will not have permission to access the tool until explicitly requested and validated." %}

## Overview

### 1. Click on any marker on the map 

![Homempage Map](images/walkthrough/homepage)


## Metacontroller tutorial: no experts

### 1. Default metacontroller
A new intersection metacontroller is from scratch. There are no boolean statements nor experts yet.

![Default metacontroller.](images/walkthrough/default_metacontroller)

### 2.  Right click to show options for building the controller.

You must click on the circle, not the label. You can then add parent and leaves, or delete nodes from the tree.

![Context menu](images/walkthrough/metacontroller_context_menu)

### 3.  Add a new expert

Add a parent or leaf node into the tree. Right click on any leaf to either show the existing expert associated with the node, or turn the node into an expert.

![The context menu to convert the node into an expert.](images/walkthrough/metacontroller_make_expert)


## Expert tutorial

### 4. Default expert

After creating an expert directly from the metacontroller interface, the expert will be assigned a color.

![The context menu to convert the node into an expert.](images/walkthrough/default_expert)

### 5. Right click to show options for building the controller.

The context menu is similar to that of the meta controller. However, the leaves of the experts are signal actions, not nested experts.

### 6. Version control

Once you create an expert or make changes, be sure to save (or revert changes if you not longer want them). Otherwise, your tree will not be updated.

![Build your expert](images/walkthrough/expert_with_leaf)

{% include links.html %}

## Metacontroller tutorial: with experts

### 1. Simmple metacontroller

![Default metacontroller.](images/walkthrough/metacontroller_with_expert)

### 2.  Name your experts appropriately

Click on the label. When you are done editing. Press enter while focusing on the textbox to save the label.

![Context menu](images/walkthrough/metacontroller_with_label_edit)

### 3.  Move experts around the tree

You can delete or add expert nodes. However, to add the expert back in, drag the box from the legend into the tree. It will be added as a leaf to the nearest node.

![Add a new expert into the tree](images/walkthrough/metacontroller_drag_expert)

### 4. Permanently remove experts from the metacontroller

If you want to completely delete an expert for good (not just its location in the metacontroller), you must first delete the node from the tree. Then, you can hover over the label in the legend. When you see the strikethrough, click. The expert will be deleted.

![Remove an expert](images/walkthrough/metacontroller_remove_expert)
