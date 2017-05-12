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

    min{H(xt,vt|Ztm1,Btm1) = 1/2 ||Phi*(xt + vt) - yt||_2^2 + lambda*mu*sum(betaj*||Wj(xt-zj)||_1) + mu*||[Btm1 vt]||_*}

Inputs:

    yt - m x 1 vector of observations/data (required input)
    Phi - m x n measurement matrix (required input)
    Ztm1 - n x J the foreground prior: initialized by J previous foregrounds 
    Btm1 - n x d the background prior: could be initialized by d previous backgrounds

Outputs:

    xt, vt - n x 1 estimates of foreground and background
    Zt - n x J the updated foreground prior
    Bt - n x d the updated background prior
