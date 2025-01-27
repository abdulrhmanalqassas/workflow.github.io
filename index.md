<h1>linked in file for workfloe test </h1>
# Plugin Development Training Material

**Training Academy of Penta-b®**

**Copyright © 2032 Penta-b**

---

## Table of Contents

1. [Introduction](#introduction)
2. [Training Environment and Scope](#training-environment-and-scope)
3. [Testing and Evaluation](#testing-and-evaluation)
4. [Implementing the Plugin Story](#implementing-the-plugin-story)
   - [Lesson Introduction](#lesson-introduction)
   - [Settings Design](#settings-design)
   - [Plugin Design](#plugin-design)
   - [Exercises](#exercises)
5. [Review Questions](#review-questions)

---

## Introduction

This document provides the training catalog for the Plugin Development course. It outlines the necessary steps and best practices for creating a robust plugin using Penta-b’s proprietary tools and libraries.

**Course Version:** 1.2  
**Version Release Date:** March 2023  
**Printed in Egypt.**

**Important:** The information contained in this document is protected under copyright laws and must not be reproduced or transmitted in any form without explicit permission from Penta-b.

---

## Training Environment and Scope

### Training Environment
Training will be conducted at Penta-b’s premises or at the client’s site in a classroom format.

### Training Scope
This course is designed to train:

- GIS End-users (Non-Professional)
- Professional Users
- System Administrators

---

## Testing and Evaluation

1. **Pre-training Test:**
   - A 30-question test to assess the qualifications of trainees.
   - A minimum score of 24 correct answers is required to proceed.

2. **Post-training Test:**
   - A certification test to evaluate the trainee's ability to operate the system successfully.

---

## Implementing the Plugin Story

### Lesson Introduction
The plugin we will develop has the following features:

1. Interact with a layer of points.
2. Display a grid of points showing the ID and name of each point.
3. Zoom in, highlight, and view more details for any point.
4. Add new points to the map dynamically.

**Key Concept:** Always plan your settings and plugin design before implementation.

---

### Settings Design

The plugin will interact with a single layer of points. Configuration settings will include:

1. **Single Layer Picker Field:** For selecting the layer.
2. **Dynamic Add Form:** Using a nested designer field for flexibility.
3. **Custom Styles:** A radio group to allow the user to select point styles (e.g., colored points or specific images).

**Configuration Example:**
- Layer Picker: Layer 1
- Form Body: Dynamic Fields (e.g., Name, Coordinates)
- Style Options: Colored points, Image-based points

---

### Plugin Design

The plugin’s main functionalities will include:

1. Displaying points in a grid format using the **Penta-Grid** component.
2. Enabling functions like zoom, highlight, and add buttons.

---

### Exercises

#### Exercise 3B: Reading the Settings

1. Log plugin settings in `MapClick.js` using `console.log`.
2. Inspect the settings via browser developer tools.

#### Exercise 3C: Implementing the Story

1. **Trigger Logic:** Implement logic in `MapClick.js` to open/close the sidebar.
2. **Fetching Points:**
   - Create `queryService.js` to fetch points from the database.
   - Use `genQueryBody` and `callQueryService` functions for querying.
3. **Drawing Points:**
   - Add points to the map dynamically using styles defined in `mapUtils.js`.
4. **Using Penta-Grid:**
   - Install the grid package: `npm i @penta-b/grid`.
   - Map features to grid properties and display in a table format.

5. **Enhancements:**
   - Add zoom, highlight, and info buttons.
   - Add a custom “Add New Point” button to dynamically update the grid and map.

---

## Review Questions

1. **How can we read the settings in the plugin code?**
   - Answer: Plugin settings can be found in the props of exported React components.

2. **What is the action used to mount other components?**
   - Answer: `showComponent`

3. **How can we add zoom and highlight buttons to the grid?**
   - Answer: By importing them from the component registry and adding them to the `trComponents` prop.

4. **What component is used to display dynamic configurable forms?**
   - Answer: The Form component imported from `@penta-b/ma-penta-smart-forms`.

---

This concludes the training material. For more details, refer to the technical documentation provided by Penta-b.

