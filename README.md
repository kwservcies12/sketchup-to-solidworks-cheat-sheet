# How to Transition from SketchUp to SOLIDWORKS Without Losing Your Mind (Command Reference)

> **Need the complete reference?** Grab the full [41-Tool SketchUp to SOLIDWORKS Command Translation Guide ($19)](https://sketchup-to-solidworks-guide.netlify.app/)

---

## The Core Pain Point: Direct Surface Modeling vs. Parametric Features

If you are moving from SketchUp Web to SOLIDWORKS Desktop, the hardest part isn't finding buttons—it's shifting your modeling mindset. 

In SketchUp, you operate in **direct surface modeling**: you draw lines freely in 3D model space, push and pull surfaces to create geometry, and type sizes directly into the Measurements box while drawing. 

In SOLIDWORKS, you operate in **parametric feature-based modeling**: 
1. You must select a plane or flat face and **start a sketch first**.
2. You draw a 2D sketch outline.
3. You apply **Smart Dimensions** to parametrically drive and lock the size *after* drawing.
4. You apply 3D feature operations (like Extrudes, Cuts, or Sweeps) to create solid geometry.

Searching through SOLIDWORKS' deep menus to find the tool that performs the same basic job as your favorite SketchUp feature can stop your workflow cold. Here is a look at core tool translations:

---

## Key Tool Translations

| SketchUp Web Tool | SOLIDWORKS Equivalent | Match Type | Key Workflow Shift |
| :--- | :--- | :--- | :--- |
| **Pencil / Line** | **Line** | Matching Tool | In SketchUp, you draw in 3D model space. In SOLIDWORKS, select a plane or flat face, click **Sketch**, then draw inside the active sketch. *(Quick access: `L` / SOLIDWORKS `W` search)* |
| **Push/Pull** | **Extruded Boss/Base** (or **Extruded Cut**) | Close Match | In SketchUp, Push/Pull directly offsets a face. In SOLIDWORKS, you draw a 2D sketch profile first, then launch Boss-Extrude to add volume or Cut-Extrude to remove material. *(Quick access: `P`)* |
| **Tape Measure** | **Smart Dimension** | Close Match | In SketchUp, Tape Measure reads distances, sets guidelines, and resizes models. In SOLIDWORKS, **Smart Dimension** in a sketch creates driving dimensions that lock and control geometry size. |
| **Offset** | **Offset Entities** | Matching Tool | In SketchUp, Offset creates parallel edges directly on a face. In SOLIDWORKS, Offset Entities duplicates lines or curves at a set distance within an active 2D sketch. *(Quick access: `F`)* |
| **Follow Me** | **Swept Boss/Base** | Close Match | In SketchUp, Follow Me sweeps an existing face along a path. In SOLIDWORKS, Sweep requires two distinct sketches: a **Profile** sketch and a **Path** sketch. |

---

## SOLIDWORKS Pro-Tip: The Command Search (`W`)
In SOLIDWORKS, pressing **`W`** on your keyboard opens the **Command Search** bar instantly. You can type the tool name (like *"Extrude"* or *"Offset Entities"*), select it from the dropdown, and press **Enter** to run it without hunting through toolbar tabs.

---

## Comprehensive Tool Summary

### 1. Selection, Erasing, and Materials
* **Select → Select (Matching):** Click geometry or features in the FeatureManager Design Tree *(SketchUp shortcut: `Spacebar`)*.
* **Lasso → Lasso Selection (Close Match):** Right-click and select Lasso Selection; crossing lasso selection is restricted to sketches and drawings in SOLIDWORKS.
* **Eraser → Trim Entities / Delete (Close Match):** SketchUp erases edges, while SOLIDWORKS uses Trim Entities for sketch line segments or the `Delete` key for whole entities.
* **Paint Bucket → Edit Appearance (Matching):** Applies appearances at the face, feature, body, or part level *(SketchUp shortcut: `B`)*.
* **Sample Material → Copy Appearance (Matching):** Copies and pastes material properties across surfaces *(SOLIDWORKS shortcut: `Ctrl+Shift+C`)*.

### 2. Drawing Lines, Shapes, and Arcs
* **Pencil/Line → Line (Matching):** Draws straight sketch entities inside an active sketch *(SketchUp shortcut: `L`)*.
* **Rectangle → Corner Rectangle (Matching):** Creates 2D rectangular sketch outlines using two opposite corners *(SketchUp shortcut: `R`)*.
* **Rotated Rectangle → 3 Point Corner Rectangle (Matching):** Sets two points for an edge, then defines width.
* **Circle → Circle (Matching):** SOLIDWORKS creates true mathematical sketch arcs/circles rather than segmented polygon approximations.
* **Polygon → Polygon (Matching):** Defines center, radius, and side count within a 2D sketch.
* **Freehand → Spline / Pen Sketch (Close Match):** Creates smooth continuous parametric curves rather than joined straight segments.
* **2-Point Arc / 3-Point Arc → 3 Point Arc (Matching):** Creates true sketch arcs; point selection order varies slightly between programs.
* **Arc → Centerpoint Arc (Matching):** Defines arc by selecting center point, start, and end points.

### 3. 3D Features & Modeling Operations
* **Push/Pull → Extruded Boss/Base or Extruded Cut (Close Match):** SketchUp directly offsets face geometry, whereas SOLIDWORKS requires a 2D profile sketch to extrude volume or cut existing material *(SketchUp shortcut: `P`)*.
* **Follow Me → Swept Boss/Base (Close Match):** Sweeps geometry along a path; SOLIDWORKS requires two separate sketches (Profile and Path).
* **Offset → Offset Entities (Matching):** Creates parallel sketch entities at a specified distance *(SketchUp shortcut: `F`)*.
* **Move → Move/Copy Bodies (Close Match):** Moves solid bodies by distance/direction in parts; sketch entities use Move Entities *(SketchUp shortcut: `M`)*.
* **Rotate → Move/Copy Bodies (Close Match):** Rotates solid bodies about an axis; sketch entities use Rotate Entities *(SketchUp shortcut: `Q`)*.
* **Scale → Scale (Matching):** Scales solid bodies using a reference center point and uniform/non-uniform scale factors *(SketchUp shortcut: `S`)*.
* **Flip → Mirror (Close Match):** Mirrors features or bodies across a reference plane.

### 4. Combining and Cutting Solids
* **Outer Shell / Union Solid → Combine > Add (Close Match / Matching):** Merges multiple solid bodies into a single solid body within a part.
* **Intersect Solid → Combine > Common (Matching):** Retains only the overlapping volume between bodies.
* **Subtract Solid → Combine > Subtract (Matching):** Subtracts secondary bodies from a main body.
* **Trim Solid → Indent > Cut (Close Match):** Uses a tool body to cut a target body while preserving the cutter.
* **Split Solid → Intersect (Close Match):** Splits overlapping bodies into separate unmerged regions.

### 5. Measuring, Annotations, and View Navigation
* **Tape Measure / Protractor → Measure (Matching):** Reads distances, lengths, and angles between geometry elements *(SketchUp shortcut: `T`)*.
* **Dimension → Smart Dimension (Close Match):** Creates driving dimensions that parametrically lock and alter geometry size.
* **Axes → Coordinate System (Close Match):** Establishes reference coordinate systems while maintaining the fixed part origin.
* **Text Label → Note (Close Match):** Inserts text annotations with optional leader lines.
* **Create Section → Section View (Matching):** Cuts a dynamic cross-section view using specified planes.
* **Orbit / Pan / Zoom → Rotate View / Pan / Zoom (Matching):** Navigates workspace using standard mouse shortcuts *(e.g., Middle Mouse Drag for Rotate View, `Ctrl` + Middle Mouse Drag for Pan, Mouse Wheel for Zoom, `F` for Zoom to Fit)*.
* **Position Camera / Walk → Add Camera / Walk-through (Close Match):** Sets up perspective viewpoints and recording paths inside the 3D scene.

---

## Need the Complete Master Reference Guide?

This repository covers key functional mappings. If you want the complete, formatted quick-reference manual, grab the full **SketchUp to SOLIDWORKS Tool & Symbol Translation Guide** ($19):

* **41 Direct & Close Tool Matches** (covering drawing, features, solid operations, measuring, and view navigation).
* **Side-by-Side Symbol Translations** so you recognize icons across software versions.
* **Exact Windows Default Keyboard Shortcuts** and SOLIDWORKS Command Search workflows.
* **Detailed Workflow Notes** written specifically for SketchUp Web users migrating to SOLIDWORKS Desktop.

👉 **[Get the Full 41-Tool Translation Guide Here](https://sketchup-to-solidworks-guide.netlify.app/)**
