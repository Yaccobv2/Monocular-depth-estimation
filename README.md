# Monocular-depth-estimation
Depth detection using neural network and single RGB camera image

# Purpose of the project

The goal of the project is to create a neural network capable of estimating relative depth in rgb images of building interiors and underground parking lots.


# Neural network block diagram.

An illustrative diagram of the denseU-net. The figure due to limitations of the tensorflow framework using the subclassing api does not show the connections between the steps of the encoder "densenet" and the decoding block:
![image](https://user-images.githubusercontent.com/39679208/172727663-4cb22fcc-4ee8-4135-b179-dea3558fdce0.png)


Schematic of the u-net showing the general concept of the encoder-decoder architecture:
![image](https://user-images.githubusercontent.com/39679208/172727740-f4c5f54e-b4d8-4d3c-9950-2ee83eae67d2.png)

# Dataset
The dataset "NYU DEPTH DATASET V2" was used to learn the neural network, which consists of rgb images and depth images representing the same shot. The depth images were acquired using a kinect sensor, and missing pixels were filled in by the authors during preprocessing. Approximately 80,000 image pairs were used for training, this is due to limited computational resources.

![image](https://user-images.githubusercontent.com/39679208/172727877-b34c1912-1eab-4e13-a027-a24bd1152320.png)

# Network Training
The network training took about 8 hours and was discontinued after three epochs due to the constraints imposed by the google colaboratory environment. By using transfer learing in the encoding part, it was possible to significantly reduce the time required to obtain satisfactory results.

![image](https://user-images.githubusercontent.com/39679208/172727958-b11578d8-a97b-4867-baa8-0dbbee2297f6.png)

![image](https://user-images.githubusercontent.com/39679208/172727968-d34ed8cc-df7d-4462-932f-5d0969e65696.png)

![image](https://user-images.githubusercontent.com/39679208/172727980-82ba4a4f-03a9-48e7-a1e3-4b97f46cefb5.png)

# Results
The proposed network architecture achieves very good results during depth detection inside buildings and underground garages. The network on images taken outdoors does not achieve the best results, but due to the characteristics of the dataset this is the result that could be expected. The proposed neural network architecture is able to achieve much better results, at the level of 96-97% accuracy, but to achieve such results much more computing power, amount of memory and much longer training time are needed. Due to the limitations imposed by the google colaboratory environment, this was not possible.

![image](https://user-images.githubusercontent.com/39679208/172728218-24c1571e-e0b1-4253-8801-6405c519a1c5.png)
![image](https://user-images.githubusercontent.com/39679208/172728223-cce5e386-6915-4fa5-8192-96162f573224.png)
![image](https://user-images.githubusercontent.com/39679208/172728228-39a896db-02dd-4c7d-9c53-3f9dbd8402cc.png)



# How to run this project
The user guide can be found in the Jupyter Notebook file. The trained model can be downloaded from my google drive: https://drive.google.com/drive/folders/1VqxSQfWkMepXw7CeD9vY-YbuNcyhrH4s?usp=sharing


