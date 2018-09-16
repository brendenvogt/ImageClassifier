
# Image Classifier Machine Learning Model
#### A Computer Vision ML Model written in **Python**.
This model makes use of Google's Machine learning api named **Keras** to assemble and train the model. Keras uses a Google's ML frameworks called **Tensorflow** as the backend for this model. <br/>
The model is **trained on the Image-Net dataset**, <br/>
and is served through a **Flask server**. <br/>
The model can be tested by sending an HTTP POST request to "localhost:5000/predict" to make predictions.

## Usage 
### 1. Install Necessary Libraries
#### Install Keras and Tensorflow
https://keras.io/

#### Install flask gevent requests and pillow
```
$ pip install flask gevent requests pillow
```

### Run
```
python Sense.py
```

<img src="https://github.com/brendenvogt/ImageClassifier/raw/master/resources/ImageClassifierStartup.png"/>
<br/>

### 3. Test Endpoint
#### 3.A Curl
```
curl -X POST -F image=@dog.jpg 'http://localhost:5000/predict'
```
Response
```
{"predictions":[{"label":"beagle","probability":0.9901767373085022},{"label":"Walker_hound","probability":0.0022487046662718058},{"label":"Brittany_spaniel","probability":0.0011901347897946835},{"label":"pot","probability":0.0011802910594269633},{"label":"Cardigan","probability":0.0006831124192103744}],"success":true}
```
<img src="https://github.com/brendenvogt/ImageClassifier/raw/master/resources/ImageClassifierCurl.png"/>
<br/>

#### 3.B Postman
```
http://localhost:5000/predict
```
Post a form file named "image" to localhost:5000/predict

<img src="https://github.com/brendenvogt/ImageClassifier/raw/master/resources/ImageClassifierPostman.png"/>
