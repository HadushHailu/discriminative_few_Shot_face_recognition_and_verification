# Discriminative few Shot face Recognition and Verification

A few-shot learning method for face recognition and verification utilizes a Siamese Network Architecture. By using a triplet loss function, the model refines the embedding space to group faces of the same person together and distinguish those of different people, improving accuracy and efficiency with minimal training data. The original Siamese Network Architecture was introduced by Gregory Koch et al. in the paper ["Siamese Neural Networks for One-shot Image Recognition."](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf)

## Real-time Face recognition and Verification
   - Score: The likelihood that the bounding box contains a face.
   - Verified: If the confidence score exceeds 85%, this is set to True.
   - Confidence: The probability indicating how similar the detected face is to the positive class.</br>

     The first picture is a positive class and the second one is a negative class. 
     ![result](resource/positive_negative_class.png)

## Siamese Network Architecture
![Example Image](resource/Module_siamese_ntk.png)


## Requirement
| No | Name | Version |
|----------|----------|----------|
| 1 | cuda  | 12.2 |
| 2 | nvidia driver | 535.104.05 |
| 3 | tensorflow | 2.15.0 |
| 4 | retinaface | 0.0.17 |
| 5 | mtcnn | 0.1.0 |
| 6 | openface | 19.24.4 |
| 7 | cv2 | 4.9.0 |

## Dataset
#### Positive Classes
The positvie class for this project was collected by ourselves from webcam and cropped to be 100x100 pixels. If more datasets is needed it is possible to get a dataset from kaggle using this [link](https://www.kaggle.com/datasets/vasukipatel/face-recognition-dataset?resource=download)

#### Negative classes
- The Negative class is collected from [labeled faces in the wild dataset](https://vis-www.cs.umass.edu/lfw/#download).
- Create a folder named "negative" under the 01_colab_data/data and unzip the dataset there. 

#### Anchor Classes
- The anchor class contains a copy of shuffled positive class

#### Verification_image
- Contains 50 samples per individual positive class. 


### Trained Model(.hs format)
- The trained model cab be downloaded [here](https://drive.google.com/file/d/1MslUExsEdewxx0RyH5_wB1QsKaguWzth/view?usp=drive_link) and be used for inference. 

## Presentation
Presentation of this project is [here](https://drive.google.com/drive/u/1/folders/1bfVkrbz1KlbR-7vHCaFQD9IJPU_dgUEW)

## References
1. [https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf)
2. https://www.sitepoint.com/keras-face-detection-recognition/
3. https://medium.com/@iselagradilla94/multi-task-cascaded-convolutional-networks-mtcnn-for-face-detection-and-facial-landmark-alignment-7c21e8007923
4. https://medium.com/axinc-ai/retinaface-a-face-detection-model-designed-for-high-resolution-6c3900771a01
5. https://medium.com/@vrushabhkangale/face-recognition-system-using-open-face-480d581986b
6. https://www.v7labs.com/blog/triplet-loss
7. https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras/
   
