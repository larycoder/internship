---
title: "3D Modelling with Unreal Engine "
author: \textbf{DO Duy Huy Hoang} \newline
        \newline
        \textit{University of Science and Technology Hanoi} \newline 
        \textit{ICT Department}
date: "2019-06-18"
logo: "logo.pdf"
logo-width: 200
titlepage: true
header-includes: |
    \usepackage{multicol}
    \usepackage{graphicx}
footer-left: Do Hoang
...

\newpage{}
\tableofcontents
\newpage{}


# I. Introduction

## 1.1 Context and Motivation	

A virtual world or a digital world is a computer-based online community environment that is designed and shared by individuals, or may be populated by many users who can create a personal avatar so that they can interact in a custom-built, simulated world. These avatars are graphically rendered using computer graphics imaging (CGI) or any other rendering technology which can make people feel like they are in the real world. Individuals control their avatars using input devices like the keyboard, mouse and other specially designed command and simulation gadgets. 

Today's virtual worlds are purpose-built for entertainment, social, educational, training and various other purposes. It is being more better than the real world. So the virtual reality has take over everything. For instance the illustrations showed in a game are more better than the reality we live in. It provides the gamer a whole new experience by taking over his imaginations it’s as if we are playing the real game with all those real gaming characters in the real life. Virtual world is bringing out all our imaginations so that we can experience it in reality. Similarly for the automobile industry we can take a virtual ride of the desired vehicle we want to buy which provides a whole new dimension to the world of buying things. 

Moreovers, virtual world has been adopted in education for teaching and learning situations. Students are able to interact with each other and within a three dimensional environment. Students can also be taken on virtual field trips, for example, to museums, taking tours of the solar system and going back in time to different eras.

## 1.2 Objectives 

Develop an interactive 3D virtual world of USTH building from easily captured 2D images. Specific goals include 
- Collect a dataset of 2D images from cameras for different views of USTH 
- Conduct fully 3D models from collected 2D images which will be a 3D model foundations for other reaseacher or developer to create others world of USTH
- Build a realtime and interactive 3D virtual world of USTH from constructed 3D models.  

## 1.3 Thesis structures

# II. State of the art 

# III. Programs, Materials, Methodologies 

## 3.1 Programs 

### 3.1.1 Sketchup

SketchUp is a 3D modeling computer program for a wide range of drawing applications such as architectural, interior design, landscape architecture, civil and mechanical engineering, film and video game design. This program was used in this project in order to create and conduct a fully 3D models from scratch. Therefore, they also provide an open library called 3D Warehouse which SketchUp users may upload and download 3D models to share. The models can be downloaded right into the program without anything having to be saved onto your computer's storage and it is free so anyone can download files for use in SketchUp or even other software such as AutoCAD, Revit and ArchiCAD.

### 3.1.2 3DS Max

Autodesk 3ds Max is a professional 3D computer graphics program for making 3D animations, models, games and images. With this feature, the software will help me to correct the position of the texture and also to edit UV mapping of some models.

### 3.1.3 Substance Painter

Substance Painter gives me all the tools I need to texture my 3D assets and also this software can help me to bake a normal map and metalic map.

### 3.1.3 Unreal Engine

## 3.2 Materials


## 3.3 Work Breakdown 

### 3.3.1 Work Breakdown Diagram

\begin{figure}
\centering
{\includegraphics[width=4in]{work-breakdown.png}}
\caption{Work Breakdown Diagram}
\end{figure}

### 3.3.2 Work Breakdown Description

This section is a visualiazation and a brief summary of the work, We shall be discussing these terms in depth in the methodology section.

#### a. Pre-project

* **Conduct a meeting with the participant** of the Planning Phase, which involves setting expectations, articulating likely risk, etc.
* **Develop Work Breakdown Structure:** break the project into smaller, measurable of work packages with a work breakdown structure.
- **Collect a dataset** of *2D images* USTH: We will use a simple camera from a smartphones to perform this task. After taking picstures with different view and also furnitures of USTH, these photos will be classified to specific folder ( e.g: Room 5/Lab ICT). This approach has two drawbacks howerver, it is time-consuming and easy to make mistakes.

#### b. Main phase

- **Conduct** fully 3D models from collected 2D images which will be a 3D model foundations for other reaseacher or developer to create others world of USTH.
\begin{figure}
\centering
{\includegraphics[width=5in]{mainphase.png}}
\caption{3D modelling steps}
\end{figure}

First of all we need to create a Floor Plans. We use a 2D legacy floor plans image and transfer it to a digital layout as the figure below.

\begin{figure}
\begin{multicols}{2}
    \includegraphics[width=\linewidth]{floorplanex.png}\par 
    \includegraphics[width=\linewidth]{floorplan.png}\par 
    \end{multicols}
\caption{Ground Prep}
\end{figure}

\newpage{}
After created a floor plans  with sketchup layout, we start to structure and interior walls and Finally in order to make the 3D model complete, we import sketchup textures, create custom materials and also add furniture objects.

\begin{figure}
\begin{multicols}{2}
    \includegraphics[width=\linewidth]{example1.png}\par 
    \includegraphics[width=\linewidth]{example2.png}\par 
\end{multicols}
    \centering
    \includegraphics[width=\linewidth]{wall.png}\par 
\caption{Structure wall and Completed model example}
\end{figure}

To finish the 3D models and prepare models for Unreal Engine, the final step is to turn a model into a normal map for exporting to be used in 3rd party renderers. We use **Substance Painter** application and also a plugin called **CLF Normal Map Maker** from Sketchup. It will paint the model as a normal map, export an image, and then revert all materials back to what they were. 

\begin{figure}
\begin{multicols}{2}
    \includegraphics[width=\linewidth]{normal_map_banner1.png}\par 
    \includegraphics[width=\linewidth]{normal_banner_2.png}\par 
    \end{multicols}
\caption{Normal map example}
\end{figure}

* **Preprocess data**: Before we can get started working with  SketchUp content in the Unreal Engine, we need to install the Unreal Datasmith Exporter plugin for SketchUp and able to export a scence from SketchUp as a *.udatasmith* file, thus the previous application creates models in a .SKP file.

* **Build a realtime and interact 3D virtual world**: We start making our 3D virtual world by adding player, light, interact, and some technique like *level streaming*....

## 3.3 Methods 

This section will explain all the methods of the work.

### 3.3.1 Preparation

Unreal Engine can be dowloaded from the official website - it is free for everyone. As I mentioned before, to be able to run Unity, and create a new project, we’ll need at least direct x11 for simulation of lighting, shadows on the scene. 

Start with importing our 3D models to UE4. Datasmith brings structure data from an combination of source applications into Unreal Engine, frequently to fabricate steady representations and experiences around that data. In any case, routinely, whereas you are working on buiding those visuallizations and experiences in UE, our sence needs to be changed in order to meet new requirements or incorporate feedback from stakeholders. 

In our 3D models, i tried to making as many as repeating elements as possible such as windows, doors, chairs, thus when Datasmith detects multiple copies of the same component in your SketchUp scene, it only creates one set of Static Mesh assets for that component, and places multiple instances of those Static Meshes into the scene. So that it is typically better for the runtime memory requirements and performance, as well as making it easier to manage the number of Static Mesh assets. 

\newpage{}
#### Units and Scale
In the Unreal Engine, all separations are constantly estimated in centimeters. However, other 3D design applications typically offer a choice of units of measurement. But Datasmith naturally deals with modifying the size of our scene so our geometry shows up at the very same genuine size in the Unreal Engine, and at the correct areas in 3D space. So we do not need to change anything from the previous work with Sketchup application.

#### Materials
The Datasmith import process creates a new Material Asset in the Unreal Engine Project to represent ech different set of geometry surface properties it recognizes in the scene it imports. But we also need to tweak these Materials after import thus most of the materials assets are *Material instances*, it is referred to as the Parent Material, which can be used as a base to make a wide varitety of different looking Materials.

\begin{figure}
\centering
{\includegraphics[width=5in]{datasmith-material-instance.jpg}}
\caption{Unreal Engine Materials}
\end{figure}

#### The Datasmith Color Material
Sketchup use simple surface color to shade geometry so we can easily use Datasmith exporter to brings these surfaces into Unreal as Instances of the *Datasmith-color Material*. The color of this Material is typically pre-set to exactly match a color from our Sketchup models, but as i mentioned before, we sometimes need to change/tweak some values. For example the brightness of the color maybe too bright so we need to reduce in order for our lighting to look realistic.

\begin{figure}
\centering
{\includegraphics[width=4in]{datasmith-color-material.jpg}}
\caption{Unreal Engine Object Color}
\end{figure}

#### Layer
While creating 3D models with SketchUp, I use *Layer* tool a alot to organize the content, eg: a roof-floor will be a layers. Datasmith preserves that organization in the Unreal Editor so that we can easily show or hide layer to quickly find and select all objects in a layer.

\begin{figure}
\begin{multicols}{2}
    \includegraphics[width=\linewidth]{layer1.png}\par 
    \includegraphics[width=\linewidth]{layer2.png}\par 
    \end{multicols}
\caption{Left: Layer in UE4. Right: Layer in SketchUp}
\end{figure}

# IV Result and Discussion

# V. Conclusion and Future work 