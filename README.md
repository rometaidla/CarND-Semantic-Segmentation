# Semantic Segmentation

### Network hyperparameters

Epochs: 50
Batch size: 8

### Result

Running network for 50 epochs gave following result:

![result gif](./samples/result.gif)

Loss was continuously going smaller and would probably get even better result when training longer 
(but there's risk of overfitting): 

![result chart](./samples/result_chart.png)

#### 10 epochs vs 50 epochs

Here are some more interesting images, where network trained for 10 epochs struggled, but network trained for 50 epoch did quite well:

10 epochs          |  50 epochs
:-------------------------:|:-------------------------:
![um_000009_10](./samples/10epoch/um_000009.png)  |  ![um_000009_50](./samples/50epoch/um_000009.png)
![um_000069_10](./samples/10epoch/um_000069.png)  |  ![um_000069_50](./samples/50epoch/um_000069.png)
![umm_000019_10](./samples/10epoch/umm_000019.png)|  ![umm_000019_50](./samples/50epoch/umm_000019.png)
![uu_000052_10](./samples/10epoch/uu_000052.png)  |  ![uu_000052_50](./samples/50epoch/uu_000052.png)
![uu_000053_10](./samples/10epoch/uu_000053.png)  |  ![uu_000053_50](./samples/50epoch/uu_000053.png)
![uu_000067_10](./samples/10epoch/uu_000067.png)  |  ![uu_000067_50](./samples/50epoch/uu_000067.png)

### Setup
##### GPU
`main.py` will check to make sure you are using GPU - if you don't have a GPU on your system, you can use AWS or another cloud computing platform.
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)

You may also need [Python Image Library (PIL)](https://pillow.readthedocs.io/) for SciPy's `imresize` function.

##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

##### Run
Run the following command to run the project:
```
python main.py
```
**Note:** If running this in Jupyter Notebook system messages, such as those regarding test status, may appear in the terminal rather than the notebook.