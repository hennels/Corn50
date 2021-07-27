# Corn50
A dataset of 50 RGB point cloud models of artificial corn plants. This dataset was produced to aide the creation of precision agriculture algorithms but may be useful in many different contexts. This is an initial stage of the dataset which will hopefully grow over time as I get around to adding more reconstructions.

### Description
Since using real data is difficult, this dataset takes the approach of making things as easy as possible. If your algorithm doesn't work on these, there is no hope for it on real data. Each reconstruction is of an artificial corn stalk so all models have the same structural components except for tassel and ear which only appear on a few of the corn stalks.

The data was produced using [COLMAP](https://colmap.github.io/) on a set of images taken with a consumer-grade digital camera. It was then filtered for noise and segmented from the environment and neighboring plants by hand. After that each was oriented so that the stalk of the plant runs through the origin and is parallel with the **z** axis. Each plant was then translated so that the centroid of the model falls at **z**=0.

While the images used to produce the models were all taken indoors in the same environment you can see in the models that there is a difference in lighting between the models making the color look slightly different in each of the models.

Each line of the `tassel.txt` file is a 0 or 1 representing the boolean value of whether the model with that index has a tassel and ear, 0 for no tassel/ear and 1 for having a tassel/ear.

More details can be found in [this paper](https://ieeexplore.ieee.org/document/9341765).

## Citation
If you find this dataset useful, please cite:
### Bibtex
```
@INPROCEEDINGS{9341765,
    author={Nelson, Henry J. and Papanikolopoulos, Nikolaos},
    booktitle={2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
    title={Learning Continuous Object Representations from Point Cloud Data},
    year={2020},
    volume={},
    number={},
    pages={2446-2451},
    doi={10.1109/IROS45743.2020.9341765}
}
```

### Plaintext
H. J. Nelson and N. Papanikolopoulos, "Learning Continuous Object Representations from Point Cloud Data," 2020 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2020, pp. 2446-2451, doi: 10.1109/IROS45743.2020.9341765.
