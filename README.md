# Octave libraries
Image processing, computer vision, computational geometry

# libraries sources
- https://github.com/drakeguan
- http://www.peterkovesi.com/

## edge-aware filtering
- bilateral
- WLS
- Local extrema [matlab][1]
- Diffusion map
- Domain transform
- Local Laplacian
- L0 minimization 
- Guided filter 
-
[1]: https://github.com/jacksky64/cp11fall_project1/tree/develop/localExtrema/

The whole testing process is in **[testSmooth.m](https://github.com/jacksky64/cp11fall_project1/tree/develop/testSmooth.m)**.



## Plotting of Input(I), Smoothed(M) and Detail(D)

For each filtering, the plotting of **flower** is demonstrated here.
I just randomly pick one line from the image (actually, I pick the line with one-third height). 
The original input image is **Blue**, the smoothed one is **Green**, and
the detail(the difference between input and smoothed one) is **Red**.

For more plotting, please go to **[result/plot](https://github.com/drakeguan/cp11fall_project1/tree/develop/result/plot/)**.

### Bilateral
![Bilateral](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_bilateralFilter.jpg)
### WLS
![WLS](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_wlsFilter.jpg)
### Domain Transform
![Domain Transform](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_domainTransform.jpg)
### Guided
![Guided](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_guidedFilter.jpg)
### L0 Minimization
![L0 Minimization](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_l0Minimization.jpg)
### Local Extrema
![Local Extrema](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/plot/flower_plot_IMD_by_localExtrema.jpg)



## Video(Image Sequence) Result

Here, I apply the **Local Extrema Filter** to an open source movie, 
[Sintel, the Durian Open Movie Proejct](http://www.sintel.org/).
The first one is just the smoothed version, mimicing the NPR effect.
The second one (if generated) is the edge-enhanced version.

[![Sintel](http://www.sintel.org/wp-content/uploads/2010/06/08.2l_comp_000465.jpg)](http://www.youtube.com/watch?v=eRsGyueVLvQ)
Youtube: [Sintel - Third Open Movie by Blender Foundation](http://www.youtube.com/watch?v=eRsGyueVLvQ)

[![Sintel by Local Extrema](https://github.com/drakeguan/cp11fall_project1/raw/develop/result/sintel/sintel_trailer_smoothed.jpg)](http://www.youtube.com/watch?v=\_F0fnSJkFkI)
Youtube: [Sintel by Local Extrema](http://www.youtube.com/watch?v=\_F0fnSJkFkI)



## Reference

1. S. Paris and F. Durand, A Fast Approximation of the Bilateral Filter Using a Signal Processing Approach, IJCV 2009. ([matlab code](http://people.csail.mit.edu/jiawen/software/bilateralFilter.m))
2. Z. Farbman, R. Fattal, D. Lischinski, R. Szeliski, Edge-Preserving Decompositions for Multi-Scale Tone and Detail Manipulation, SIGGRAPH 2008. ([matlab code](http://www.cs.huji.ac.il/~danix/epd/wlsFilter.m))
3. K. Subr, C. Soler, F. Durand, Edge-Preserving Multiscale Image Decomposition Based on Local Extrema, SIGGRAPH Asia 2009.
4. Z. Farbman, R. Fattal, D. Lischinski, Diffusion Maps for Edge-Aware Image Editing, SIGGRAPH Asia 2010.
5. E. Gastal, M. Oliveira, Domain Transform for Edge-Aware Image and Video Processing, SIGGRAPH 2011. ([matlab code](http://inf.ufrgs.br/~eslgastal/DomainTransform/DomainTransformFilters-Source-v1.0.zip))
6. S. Paris, S. Hasinoff, J. Kautz, Local Laplacian Filters: Edge-Aware Image Processing with a Laplacian Pyramid, SIGGRAPH 2011. ([matlab code](http://people.csail.mit.edu/sparis/publi/2011/siggraph/matlab_source_code.zip))
7. L. Xu, C. Lu, Y. Xu, J. Jia, Image smoothing via L0 Gradient Minimization, SIGGRAPH Asia 2011. ([matlab code](http://www.cse.cuhk.edu.hk/~leojia/projects/L0smoothing/L0smoothing.zip))
8. K. He, J. Sun, X. Tang, Guided Image Filtering, ECCV 2010. ([matlab code](http://personal.ie.cuhk.edu.hk/~hkm007/eccv10/guided-filter-code-v1.rar))
