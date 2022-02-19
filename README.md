# Scanline Rendering Engine

 This Scanline Renderer was created for my CS430 course at Drexel University.

 This program has the following features:
 
    1. Reads in arguments from the command line for up to three different SMF files, viewport boundaries, PRP, VRP, VPN, VUP, VRC, front plane, back plane, and whether the projection is parallel or perspective 
    
    2. Reads in information on vertices and faces of a mesh from the specified SMF file
    3. Composes normalizing matrix based on projection type
    
    4. Extends 3D points to homogenous coordinates
    
    5. Projects coordinates onto image plane based on projection type
    
    6. Clips vertices to normalized window based on projection type
    
    7. Applies world to viewport transformation to vertices
    
    8. Colors any point on the mesh's surface within the front and back clipping planes based on z-depth and the order the model is inputted on the command line in viewport window of a 501 x 501 image
    
    9. Outputs drawing to a .xpm file

 This program takes parameters, but if none are specified, it will produce the same results as:
   
    ./scanlineRenderer -f bound-sprellpsd.smf -j 0 -k 0 -o 500 -p 500 -x 0.0 -y 0.0 -z 1.0 -X 0.0 -Y 0.0 -Z 0.0 -q 0.0 -r 0.0 -w -1.0 -Q 0.0 -R 1.0 -W 0.0 -u -0.7 -v -0.7 -Y 0.7 -V 0.7 -F 0.6 -B -0.6 > out.pbm

 This program was written in Python 2.7, so everything needed to run it is in the file scanlineRenderer.
 A sample .smf file is included in this repository to be used as sample input for the script.
 The code can be run using the command ./scanlineRenderer.
