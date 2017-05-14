# corpca
Compressive Online Robust Principal Component Analysis with Multiple Prior Information (CORPCA).

    Version 1.1,  Jan. 24, 2017
    Implementations by Huynh Van Luong, Email: huynh.luong@fau.de,
    Multimedia Communications and Signal Processing, University of Erlangen-Nuremberg.

    Please see the file LICENSE for the full text of the license.

Please cite this publication

    PUBLICATION: Huynh Van Luong, N. Deligiannis, J. Seiler, S. Forchhammer, and A. Kaup, 
            "Incorporating Prior Information in Compressive Online Robust Principal Component Analysis," 
             in e-print, arXiv, Jan. 2017.
             
Solving the problem

<img src="https://latex.codecogs.com/svg.latex?\dpi{150}&space;\small&space;\min_{\boldsymbol{x}_{t},\boldsymbol{v}_{t}}\Big\{H(\boldsymbol{x}_{t},\boldsymbol{v}_{t})=\frac{1}{2}\|\mathbf{\Phi}(\boldsymbol{x}_{t}&plus;\boldsymbol{v}_{t})-\boldsymbol{y}_{t}\|^{2}_{2}&space;&plus;\lambda\mu\sum\limits_{j=0}^{J}\beta_{j}\|\mathbf{W}_{j}(\boldsymbol{x}_{t}-\boldsymbol{z}_{j})\|_{1}&plus;&space;\mu\Big\|[\boldsymbol{B}_{t-1}\boldsymbol{v}_{t}]\Big\|_{*}\Big\}" title="\small \min_{\boldsymbol{x}_{t},\boldsymbol{v}_{t}}\Big\{H(\boldsymbol{x}_{t},\boldsymbol{v}_{t})=\frac{1}{2}\|\mathbf{\Phi}(\boldsymbol{x}_{t}+\boldsymbol{v}_{t})-\boldsymbol{y}_{t}\|^{2}_{2} +\lambda\mu\sum\limits_{j=0}^{J}\beta_{j}\|\mathbf{W}_{j}(\boldsymbol{x}_{t}-\boldsymbol{z}_{j})\|_{1}+ \mu\Big\|[\boldsymbol{B}_{t-1}\boldsymbol{v}_{t}]\Big\|_{*}\Big\}" /></a>

Inputs:

<img src="https://latex.codecogs.com/svg.latex?\dpi{150}&space;\boldsymbol{y}_{t}\in&space;\mathbb{R}^{m}" title="\boldsymbol{y}_{t}\in \mathbb{R}^{m}" />: a vector of observations/data <br />
Phi - a measurement matrix
    Ztm1 - n x J the foreground prior: initialized by J previous foregrounds 
    Btm1 - n x d the background prior: could be initialized by d previous backgrounds

Outputs:

    xt, vt - n x 1 estimates of foreground and background
    Zt - n x J the updated foreground prior
    Bt - n x d the updated background prior
