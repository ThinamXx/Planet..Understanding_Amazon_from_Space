# [**Planet: Understanding the Amazon from Space**](https://www.kaggle.com/c/planet-understanding-the-amazon-from-space/overview)

**Overview and Description**
- Every minute, the world loses an area of forest the size of 48 football fields. And deforestation in the Amazon Basin accounts for the largest share, contributing to reduced biodiversity, habitat loss, climate change, and other devastating effects. But better data about the location of deforestation and human encroachment on forests can help governments and local stakeholders respond more quickly and effectively.
Planet, designer and builder of the world’s largest constellation of Earth-imaging satellites, will soon be collecting daily imagery of the entire land surface of the earth at 3-5 meter resolution. While considerable research has been devoted to tracking changes in forests, it typically depends on coarse-resolution imagery from Landsat (30 meter pixels) or MODIS (250 meter pixels). This limits its effectiveness in areas where small-scale deforestation or forest degradation dominate.
Furthermore, these existing methods generally cannot differentiate between human causes of forest loss and natural causes. Higher resolution imagery has already been shown to be exceptionally good at this, but robust methods have not yet been developed for Planet imagery.

**Fastai Library or API**
- [Fast.ai](https://www.fast.ai/about/) is the first deep learning library to provide a single consistent interface to all the most commonly used deep learning applications for vision, text, tabular data, time series, and collaborative filtering.
- [Fast.ai](https://www.fast.ai/about/) is a deep learning library which provides practitioners with high-level components that can quickly and easily provide state-of-the-art results in standard deep learning domains, and provides researchers with low-level components that can be mixed and matched to build new approaches.

**Preparing the Model**
- I have used [Fastai](https://www.fast.ai/about/) API to train the Model. It seems quite challenging to understand the code if you have never encountered with Fast.ai API before.
One important note for anyone who has never used Fastai API before is to go through [Fastai Documentation](https://docs.fast.ai/). And if you are using Fastai in Jupyter Notebook then you can use doc(function_name) to get the documentation instantly.

**Data**
- I had prepared the Data for this Project from [Kaggle](https://www.kaggle.com/c/planet-understanding-the-amazon-from-space/data)

**Creating ImageList with Fastai**

```javascript
get_transforms(flip_vert=True, max_zoom=1.05, max_lighting=0.1, max_warp=0.)
```

```javascript
(ImageList.from_csv(path, "....csv", folder="train-jpg", suffix='.jpg')
      .split_by_rand_pct(0.2)
      .label_from_df(label_delim=' '))
```

**Observing the Data Prepared**

![Image](https://res.cloudinary.com/dge89aqpc/image/upload/v1596721725/Planet_mdnqj2.png)

**Snapshot of the Model Accuracy**

![Image](https://res.cloudinary.com/dge89aqpc/image/upload/v1596721843/11_dex89b.png)

**Snapshot of the Loss Function**
- As, shown in the figure below, the Loss Function is gradually decreasing which means that the Model is not overfitting.

![Image](https://res.cloudinary.com/dge89aqpc/image/upload/v1596721964/Lossss_qeknbl.png)
