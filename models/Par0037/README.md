# Par0037 - elastix

###  Registration Description
intra-subject; translational registration; mutual information	

###  Image data

Lung Digital Tomosynthesis (DTS)

###  Application

* The registration was used for target localization in radiation therapy
* The registration was applied between reference DTS synthesized from CT and on-board DTS acquired with patient on treatment couch
* ![alt-text](DTS_images.png)
* as shown in the figure, the left is the on-board DTS and the right is the reference DTS. The tumor is localized (pointed by arrows) through image registration.

###  Registration settings

`elastix` version: 4.600

Description:

* Rigid-TransforTotal: the translational registration was applied on the whole body
* Rigid-TransforROI: the translational registration was applied on ROIs for fine-tuning, which uses the registration results from the above as the starting point

Command line call:


    elastix -f FixedImage_i.mhd -m MovingImage_j.mhd -p Rigid-TransforTotal -out outputdir
    elastix -f FixedImage_i.mhd -m MovingImage_j.mhd -p Rigid-TransforROI -t0 resultsfromabove -fmask selectedroiregion -out outputdir


###  Published in

[1] [You Zhang, Fang-Fang Yin, Irina Vergalasova, Lei Ren, "Pilot Clinical Study of Orthogonal-view Phase-matched Digital Tomosynthesis for Lung Tumor Localization" _in preparation_ 2015]
