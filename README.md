# RNA Surface Segmentation Dataset

This dataset contains 640 triangulated surface meshes of the molecular envelopes for RNA molecules, gathered from the PDB database. Each vertex is assigned a ground-truth segmentation label according to one of 260 functional categories (see the quoted blurb below for a full description of the meaning and collection process). We use this data as a representative task for 3D machine learning on surfaces, predicting the functional segmentation from only the molecule shape.


From: **Effective Rotation-invariant Point CNN with Spherical Harmonics Kernels**, *Adrien Poulenard, Marie-Julie Rakotosaona, Yann Ponty, Maks Ovsjanikov*, in 3DV 2019.

Please cite this dataset as:
```bib
@inproceedings{poulenard2019effective,
  title={Effective rotation-invariant point cnn with spherical harmonics kernels},
  author={Poulenard, Adrien and Rakotosaona, Marie-Julie and Ponty, Yann and Ovsjanikov, Maks},
  booktitle={2019 International Conference on 3D Vision (3DV)},
  pages={47--56},
  year={2019},
  organization={IEEE}
}
```




### Full description

(the following description is quoted from Poulenard et. al. above, please contact the authors therein for further questions)

> We also applied our approach to tackle the challenging task of segmenting molecular surfaces into functionally homologous regions within RNA molecules. We considered a family of 640 structures of 5s ribosomal RNAs (5s rRNAs), downloaded from the PDB database [3]. A surface, or molecular envelope, was computed for each RNA model by sweeping the volume around the atomic positions with a small ball of fixed radius. This task was performed using the scripting interface of the Chimera structure-modelling environment [20]. Individual RNA sequences were then globally aligned, using an implementation of the NeedlemanWunsch algorithm [19], onto the RFAM [12] reference alignment RF00001 (5s rRNAs). Since columns in multiple sequence alignments are meant to capture functional homology, we treated each column index as a label, which we assigned to individual nucleotides, and their corresponding atoms, within each RNA. Labels were finally projected onto individual vertices of the surface by assigning to a vertex the label of its closest atom. This results in each shape represented as a triangle mesh consisting of approximately 10k vertices, and its segmentation into approximately 120 regions, typically represented as connected components. Shapes in this dataset are not pre-aligned and can have fairly significant geometric variability arising both from different conformations as well as from the molecule acquisition and reconstruction process (see Fig. 5 for an example).


### Papers using this dataset
(create a pull request to add yours!)
- ["Effective Rotation-invariant Point CNN with Spherical Harmonics Kernels"](https://arxiv.org/abs/1906.11555) by Poulenard et al., 3DV 2019
- ["DiffusionNet: Discretization Agnostic Learning on Surfaces"](https://arxiv.org/abs/2012.00888) by Sharp et al., ACM ToG 2021
