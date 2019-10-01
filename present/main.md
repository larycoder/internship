---
# pandoc main.md -H preamble.tex -t beamer -o main.pdf --slide-level=2
title: "Development of USTH interactive virtual world using Unreal Engine"
author: 
- Do Hoang
date: \today{}
institute: 
-  University of Science And Technology of Hanoi 
theme:
- Ilmenau
colortheme:
- default 
innertheme:
- circles 
# outertheme:
# - miniframes 
header-includes:
- \newcommand{\hideFromPandoc}[1]{#1}
- \hideFromPandoc{
    \let\Begin\begin
    \let\End\end
  }
mainfont: "SourceSansPro-Regular"
caption-justification: centering
toc: 
- true
---

# Introduction
## Context

![A virtual world based biosafety training application for medical students](context.png){ width=3.5in }

## Context 
- **Problem**:
	
	- 10 years anniversary of USTH. 
	- Marketing. 
	- Virtual trips for remote students or overseas student.
- **Objectives**:

	- *Collect* a dataset of 2D images for different views of USTH.
	- *Conduct* fully 3D models from collected 2D images.
	- *Build* a realtime and interactive 3D virtual world of USTH from constructed 3D models.

# Methodology
## Tools 

\begin{figure}
\centering
{\includegraphics[width=2.9in]{../docs/sketch+unreal.jpg}}
\caption{Sketch and Unreal Engine}
\end{figure}

* SketchUp.

* Unreal Engine.

* 3DSMax, Substance Painter, Adobe Tools.

## Work flow 

![Work Flow Overall Diagram](../docs/workflow2.png){ width=\linewidth }

## Input Data: 2D Images
\Begin{columns}
\Begin{column}{0.5\textwidth}

![](inputdata.jpg)

\End{column}
\Begin{column}{0.5\textwidth}

![](../docs/floorplanex.png)

\End{column}
\End{columns}

- 2D panoramic pictures, Floor plans, videos with different views of USTH.

## 3D Modelling

\begin{figure}
\centering
{\includegraphics[width=\linewidth]{../docs/mainphase.png}}
\caption{3D modelling steps}
\end{figure}

# Results

## Results
### Dataset of 2D images: 
- **726 images**, **18 videos** with different views of USTH with: High resolution, Easily captured, Cheap, Popular. 

### Raw 3D models of USTH 
- **6 3D models**, **300+ different objects and textures**.
- Foundations for other reaseacher or developer to create others virtual world of USTH.

### Fully interactive virtual world of USTH 
Succesfully implement 3 floors ( 7th floor, 4th floors and 1st floor ) to create a virtual world with Unreal Engine.

- Lighting 
- Shading
- 30 blueprints.

# Future Plan
## Future Plan

# Demo 

## Demo

## Q&A
