Co-Blade v2.0.0_rc1 (Release Candidate 1)
========

     ▄████████  ▄██████▄         ▀█████████▄   ▄█          ▄████████ ████████▄     ▄████████ 
    ███    ███ ███    ███          ███    ███ ███         ███    ███ ███   ▀███   ███    ███ 
    ███    █▀  ███    ███          ███    ███ ███         ███    ███ ███    ███   ███    █▀  
    ███        ███    ███         ▄███▄▄▄██▀  ███         ███    ███ ███    ███  ▄███▄▄▄     
    ███        ███    ███  ████  ▀▀███▀▀▀██▄  ███       ▀███████████ ███    ███ ▀▀███▀▀▀     
    ███    █▄  ███    ███          ███    ██▄ ███         ███    ███ ███    ███   ███    █▄  
    ███    ███ ███    ███          ███    ███ ███▌    ▄   ███    ███ ███   ▄███   ███    ███ 
    ████████▀   ▀██████▀         ▄█████████▀  █████▄▄██   ███    █▀  ████████▀    ██████████ 
                                              ▀                                              

# Co-Blade: Software for Analysis and Design of Composite Blades

## Co-Blade Overview:

Co-Blade is an open source software that can be used for the structural analysis and design of composite blades for wind and hydrokinetic turbines. The objective of Co-Blade is to help designers accelerate the preliminary design phase by providing the capabilities to quickly analyze alternative composite layups and to study their effects on composite blade properties, deformations, and material stresses and strains.
   
![](https://raw.githubusercontent.com/nnmrec/Co-Blade/master/Documentation/images/Co-Blade%20logo.png)

In summary, the Co-Blade software contains many features:

* Realistic Modeling of Composite Blades
  * nearly arbitrary topology & material properties
* Computation of Structural Properties
  * offsets: center-of-mass, tension-center, & shear-center
  * inertias: mass & mass moments of inertia
  * stiffnesses: axial, bending, & torsional
  * principal axes: inertial, centroidal, & elastic principal axes
  * modal analysis: coupled mode shapes & frequencies (via integration w/ BModes)
* Structural Analysis
  * nearly arbitrary applied aerodynamic forces & moments
  * computation of body forces (centrifugal, weight, & buoyancy)
  * computation of load induced blade deflections, lamina-level stresses & strains, & panel buckling stresses
* Optimization of Composite Layup
  * For a given external blade shape & design load, Co-Blade can determine an optimal composite layup which minimizes blade mass while simultaneously satisfying constraints on maximum stress, buckling, deflection, & placement of natural frequencies
* Graphical Post-Processing
  * A large variety of 2D & 3D visualizations can be created through a graphical user interface to provide instant visual feedback

## Showcase:

On the [Showcases page](https://github.com/nnmrec/Co-Blade/blob/master/Documentation/2_Showcases.md), you can see some examples of screenshots from the Co-Blade code.


## Code & Documentation:

Obtain the latest version of Co-Blade and user’s guide on the [Release Downloads page](https://github.com/nnmrec/Co-Blade/releases). The modal analysis capabilities of Co-Blade also require the BModes v3.00.00 code ([which must be obtained from NREL](https://nwtc.nrel.gov/BModes)). If using the compiled version of Co-Blade, you will also need to install the [Matlab Component Runtime v7.16](http://wind.nrel.gov/designcodes/miscellaneous/MatLab_MCRInstaller/).  Some Matlab toolboxes are also required, but optional (the Optimization and Global Optimization toolboxes).

Some notes related to theory and equation derivation are available here, [Theory Guide](https://github.com/nnmrec/Co-Blade/blob/master/Documentation/4_Notes.md).

Co-Blade is an open source project aimed at developing user friendly software for the analysis and design of composite blades for wind and hydrokinetic turbines. If you are interested in becoming a contributor to the Co-Blade project (either through modifying the code, adding new features, validating Co-Blade results, or anything else you are interested in) please feel free to contact me, I am happy to discuss possible collaborations.


## Run the Co-Blade Examples

Edit the main User Input file, denoted by *.inp file type, following the [examples here](https://github.com/nnmrec/Co-Blade/tree/master/Inputs).
From the Matlab prompt (compatible with Linux, Windows, and Mac), call the function simply by

    $ CoBlade('input_filename.inp')

or from the Windows command prompt (using the compiled version)

    $ CoBlade.exe input_filename.inp
