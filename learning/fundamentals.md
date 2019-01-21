---
title: Fundamentals of 3D printing
toc: true
toc_title: Table of Contents
toc_icon: "cog"
---

## Principles

The principles of 3DP, what to expect and what 3DP is not or not yet.

### Fabrication

{% include video id="tfYGzZoYbuM" provider="youtube" %}

#### Additive vs Subtractive
{% include figure image_path="/assets/additive.gif" caption="Additive" %}
{% include figure image_path="/assets/subtractive.gif" caption="Subtractive" %}

#### Computer Numerical Control

{% include figure image_path="/assets/human.gif" caption="Human control" %}
{% include figure image_path="/assets/plotter.gif" caption="Cumputer control" %}

### Safety & precautions

  * Moving parts & Computer control
  * Chemicals & fumes
  * Heat
  * Eye protection

## Techniques
**Fused Deposition Modeling (FDM)**
{: .text-center}
{% include figure image_path="/assets/fdm.gif" %}

**Stereolithography (SLA)**
{: .text-center}
{% include figure image_path="/assets/sla.gif" %}

**Selective Laser Sintering (SLS)**
{: .text-center}
{% include figure image_path="/assets/sls.gif" %}

**Continuous Liquid Interface Production (CLIP)**
{: .text-center}
{% include figure image_path="/assets/clip.gif" %}

## FDM Materials
  * **PLA** _(Polylactic Acid)_ is easy to print, rigid, strong and brittle
  * **ABS** _(Acrylonitrile Butadiene Styrene)_ higer temperature resistance and less brittle than PLA, requires heated bed
  * **PETG** _(Polyethylene Terephthalate Glycol)_ higher temperature resistance than ABS, requires higher temperatures and heated bed, more difficult to print
  * **TPU** _(Thermoplastic Polyurethane)_ semi-flexible to flexible, high impact resistance
  * **Nylon** _(Polyamide)_ high strenght, doesn't wear off easily, problematic on layer adhesion
  * **Infused** represent variations of the above (mostly PLA) infused with other materials like: copper, bronze, wood, fiberglass, coffee and more.

## Printer parts

### Geometry
**Cartesian**
{: .text-center}
{% include figure image_path="/assets/cartesian.gif" %} 

**Delta**
{: .text-center}
{% include figure image_path="/assets/delta.gif" %}


### Extruder
  * Direct drive & Bowden extruder

### Hot end
  * Nozzle
  * Heat break

### Print bed

## Slicer

  * Cura ([download](https://ultimaker.com/en/products/ultimaker-cura-software))
  * Slic3r Prusa Edition ([download](https://github.com/prusa3d/Slic3r/releases))

### Gcode sneak peak

```gcode
G21 ;metric values
G28 X Y ;home X and Y axes
G28 Z ;home Z axis
G90 ;absolute positioning
M82 ;set extruder to absolute mode
M107 ;start with the fan off
G1 F3000 Z10.0 ;move Z axis up 10mm
G92 E0 ;zero the extruded length
G1 F200 E3 ;extrude 3mm of feed stock
G92 E0 ;zero the extruded length again
; other code here
M104 S0 ;extruder heater off
M140 S0 ;heated bed heater off
M220 S100 ;reset speed factor to 100%
M221 S100 ;reset extrude factor to 100%
G91 ;set coordinates to relative
G1 F1800 E-3 ;retract filament 3 mm to prevent oozing
G1 F3000 Z+5 E-5 ;move Z axis up and retract more
G90 ;absolute positioning
; cura {machine_depth} - slic3r [bed_shape_2]
G1 F6000 X0 Y{machine_depth} ;move bed to the front for easy print removal
M84 ;disable steppers
M300 S1000 P50 ;beep
M300 S0 P250 ;wait
M300 S1000 P50 ;beep
```

### Printer settings
  * Firmware
  * Bed size & print height
  * Nozzle size
### Filament settings
  * Filament diameter
  * Nozzle & bed temperature
### Print settings
  * Layer
    * Thickness
    * Perimeters & Surfaces
  * Infill percentage & pattern
  * Print, wall, infill & travel speed
  * Skirt, brim & raft
  * Supports
  * Retraction distance & speed
  * Vase mode
## Fusion 360
[Download](https://www.autodesk.com/products/fusion-360/free-trial)
  * Sketching
    * Shapes
    * Constraints
  * Modelling
    * Extrude & Revolve
    * Fillet & Chamfer

### Links

  * https://all3dp.com/guides/
  * https://www.thingiverse.com/