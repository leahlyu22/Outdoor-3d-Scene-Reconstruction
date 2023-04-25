# Outdoor 3d Scene Reconstruction
## Project description
The project aimed to improve the performance of outdoor scene reconstruction, with a specific focus on the sky regions by proposing and implementing a novel algorithm.


[Urban Radiance Field (Google Research)](https://urban-radiance-fields.github.io/) is used as the theoretical basis combining with [Neural Scene Graphs for Dynamic Scene (CVPR 2021)](https://light.princeton.edu/publication/neural-scene-graphs/) for this project. Original repository forked from the Implementation of Original [Neural Scene Graph Implementation](https://github.com/princeton-computational-imaging/neural-scene-graphs), [original readme]([./nerf_license/README.md](https://github.com/princeton-computational-imaging/neural-scene-graphs/blob/main/README.md)).

To enhance the supervisory signal in sky regions, an additional MLP model is added to the sky region with a pretrained segmentation [DeepLabV3Plus](https://github.com/VainF/DeepLabV3Plus-Pytorch) model.

---

## Model performance
The final loss is 0.38 compared to the starting point of 0.79.<br />
The final psnr is 22.13 compared to the starting point of 10.26.

<p float="left">
  <img src="https://github.com/leahlyu22/neural-scene-graphs/blob/main/performance/model_performance_tf.png?raw=true" width="150" height="300" />
  <img src="https://github.com/leahlyu22/neural-scene-graphs/blob/main/performance/model_performance.png?raw=true" width="150" height="300" /> 
</p>

The top right image is the rendering result only for non-sky-region. The middle right image is the result of combining both sky and the non-sky region. The bottom right image is the ground-truth image.

The result of sky-region reconstruction:
 <img src="https://github.com/leahlyu22/neural-scene-graphs/blob/main/performance/rendering_result_sky.png?raw=true">


Check the video result here:

![IMB_nGcFXK](https://user-images.githubusercontent.com/91255799/234092699-8b9766b3-505c-4739-9e93-e116de734bae.gif)

---

Citation
```
@InProceedings{Ost_2021_CVPR,
    author    = {Ost, Julian and Mannan, Fahim and Thuerey, Nils and Knodt, Julian and Heide, Felix},
    title     = {Neural Scene Graphs for Dynamic Scenes},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2021},
    pages     = {2856-2865}
}

@article{rematas2022urf,
    title={Urban Radiance Fields},
    author={Konstantinos Rematas and Andrew Liu and Pratul P. Srinivasan and Jonathan T. Barron and Andrea Tagliasacchi and Tom Funkhouser and Vittorio Ferrari},
    journal={CVPR},
    year={2022}
}
```
