# Awesome-Text-To-CAD

## Top Text-to-CAD Tools Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Natural Language to Parametric Model Generation, AI-Assisted Design & Code-Based CAD*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Text-to-CAD**. These tools transform natural language descriptions into 3D models — from quick concept meshes to fully editable parametric CAD assemblies — enabling engineers, designers, and makers to generate geometry without manual sketching or feature-by-feature modeling.



**Examples** include Onshape, Zoo Text-to-CAD, Leo AI, Spline AI, Meshy, 3DFY.ai, Sloyd, Tripo AI, Autodesk Fusion 360, and Masterpiece Studio (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom LLM-to-CAD pipelines, and transparent parametric generation — ideal for engineers seeking data sovereignty, developers building design automation, and researchers advancing text-to-CAD models.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Onshape](https://www.onshape.com/)**  

  Cloud-native parametric CAD platform with a documented REST API for programmatic model creation. Onshape clients are open-source, enabling automation scripts and integration with external systems. No native text-to-CAD feature, but the API allows building custom LLM-to-CAD pipelines .



- **[Zoo Text-to-CAD](https://zoo.dev/)**  

  API-first text-to-CAD service generating parametric models from natural language prompts. Returns models in multiple formats including FBX, GLB, GLTF, OBJ, PLY, STEP, and STL. Features async generation with status tracking, conversation-based iteration (KCL code output), and a Blender addon for direct integration . Zoo's ML API produces KCL (KittyCAD Language) code that can be iterated conversationally.



- **[Leo AI](https://www.leo.ai/)**  

  Mechanical engineering copilot that generates **full CAD assemblies** from text prompts. Handles design calculations, searches internal and online parts, and assembles B-Rep models with full part and feature trees. Compatible with Solidworks, Onshape, Catia, and Inventor. Used by Nvidia, HP, Intel, and the U.S. military. Raised $9.7M, founded 2022 . Farid describes it as passing the "mechanical Turing test" — the output is indistinguishable from human-designed assemblies .



- **[Spline AI](https://spline.design/)**  

  AI 3D generation within Spline's design platform. Transforms text and 2D images into 3D models using models including Hunyuan3D (default), Hunyuan 3.1 Pro, Trellis 2, and Meshy. Generated models drop directly into Spline scenes for positioning, styling, and animation . Hana V2 adds GLTF/GLB import with skeletons, skinning, and morph targets .



- **[Meshy](https://www.meshy.ai/)**  

  AI 3D model generator producing production-ready assets from text, images, and conversation. Uses Meshy 6 for text-to-3D (20 credits, ~1 minute) and Meshy 7 for image-to-3D with improved alignment. Features Smart Topology for game-ready meshes, PBR texture generation, and export to GLB, FBX, OBJ, STL, USDZ, and 3MF. Free tier: 100 credits/month. 12M+ creators .



- **[3DFY.ai](https://3dfy.ai/)**  

  AI-powered 3D model generation from text and images. Enables mass creation of scalable, high-quality 3D assets for AR/VR ecosystems and online retail. Supports glb/blend/fbx output with multiple levels of detail. Enterprise API available .



- **[Sloyd](https://www.sloyd.ai/)**  

  AI 3D model generator focused on real-time parametric generation for games and interactive applications.



- **[Tripo AI](https://www.tripo3d.ai/)**  

  AI 3D generation platform producing detailed models from text and images with texture support.



- **[Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/)**  

  Professional CAD/CAM software with API access for automation. Can be driven by LLM-generated feature plans through MCP servers and add-ins (see open-source section below).



- **[Masterpiece Studio](https://masterpiecestudio.com/)**  

  AI-powered 3D content creation suite with text-to-3D and VR modeling capabilities.



## Open-Source GitHub Projects



- **[cycleCAD](https://github.com/vvlars-cmd/cyclecad)**  

  **The most complete open-source text-to-CAD platform**. Browser-based parametric CAD with real B-Rep kernel (OpenCascade.js WASM) — the same geometry engine behind FreeCAD and KiCad. Features:

  - **Text-to-CAD**: Natural language to 3D geometry with live preview

  - **Photo-to-CAD**: Phone photo to parametric model via edge detection + AI

  - **DFM feedback**: 9 processes, 20+ materials

  - **Generative Design**: SIMP topology optimization

  - **Multi-Physics Simulation**: FEA, thermal, modal, drop test in-browser

  - **Agent API**: 55 commands across 10 namespaces via JSON-RPC, MCP server, CLI, and REST API

  - **Real fillets, real booleans, STEP import/export**

  - MIT licensed. Runs entirely in browser at cyclecad.com/app. Compare to OnShape ($1,500/yr) and Fusion 360 ($545/yr) — cycleCAD is free forever .



- **[text-to-cad (Bhooorya)](https://github.com/Bhooorya/text-to-cad)**  

  Describe a part in plain English, get a fully editable parametric Fusion 360 model. An LLM emits a validated JSON feature plan against 28 typed CAD endpoints, executed through an MCP server and a Fusion 360 add-in. **Parameters come first** — every plan declares named parameters that become real Fusion 360 user parameters, making output editable instead of dead geometry. Ships a mock backend so it runs with no CAD install. Supports Claude Code/Desktop via MCP, with a rule-based planner fallback for common prompts like brackets and hole grids. Python 3.10+ .



- **[CADFusion](https://github.com/microsoft/CADFusion)**  

  Microsoft Research's open-source text-to-CAD model. Takes natural language describing appearance, components, and functionality, and generates CAD model as structured text with modeling operations and dimensions. Fine-tuned from LLaMA-3-8B using a two-stage process: sequential learning on paired descriptions/models, then visual feedback using a vision-language model to prefer better CAD outputs. MIT licensed. **Research purposes only** — not for commercial deployment without extensive testing .



- **[CodeToCAD](https://github.com/CodeToCAD/CodeToCAD)**  

  Code-based modeling automation for Blender and OnShape. Unlike CADQuery and OpenSCAD, CodeToCAD interfaces directly with existing modeling software, so you keep using your preferred CAD tool while leveraging Python automation. Not vendor-locked — models are defined in open-source Python. Future integrations planned for FreeCAD, KiCAD, CADQuery, and ThreeJS .



- **[onpy](https://github.com/kyle-tennison/onpy)**  

  Python API for building Onshape models programmatically. 22 GitHub stars. Enables scripted parametric model generation and integration with external automation pipelines .



### Additional Strong Open-Source Options



- **[OpenCascade.js](https://github.com/donalffons/opencascade.js)** — WASM port of the OpenCascade B-Rep kernel. Foundation for browser-based CAD including cycleCAD.

- **[CadQuery](https://github.com/CadQuery/cadquery)** — Python library for building parametric 3D CAD models with a fluent API.

- **[FreeCAD](https://github.com/FreeCAD/FreeCAD)** — Full open-source parametric 3D CAD modeler with Python scripting.

- **[Blender](https://github.com/blender/blender)** — Open-source 3D creation suite with Python API for procedural modeling.

- **LLM-to-CAD Pipelines** — MCP servers and JSON schema validators for converting natural language to CAD operations.

- **Vector Databases** — Qdrant, Weaviate for semantic retrieval of CAD parts and features.



**Frameworks for building custom systems**: Combine **cycleCAD** for browser-based text-to-CAD with real B-Rep geometry, **text-to-cad (Bhooorya)** for Fusion 360 parametric model generation via LLM feature plans, **CADFusion** for research on LLM-based CAD generation, **CodeToCAD** for Python automation across CAD platforms, and **onpy** for Onshape API integration to build a complete open-source text-to-CAD stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Text-to-CAD tools must comply with applicable engineering standards, safety regulations, and intellectual property laws. AI-generated CAD models may contain errors or unsafe designs and must be validated by qualified engineers before manufacturing or construction.

- Self-hosted open-source solutions require proper security hardening, model validation, and ongoing maintenance.



---



**Made for mechanical engineers, product designers, makers, and developers building AI-assisted CAD platforms.**  

Let's make text-to-CAD more open, accurate, and engineer-friendly.
