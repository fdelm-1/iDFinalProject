# Celestial Classification Algorithm

 * For my project, I decided to train an image detection algorithm to classify different celestial bodies such as stars and nebulae.
 * The algorithm has classes:
   - Satellite
   - Space
   - Galaxy
   - Gas Giant
   - Moon
   - Nebula
   - Protostar
   - Star
   - Star Cluster
   - Supernova
   - Planet

![image](https://github.com/user-attachments/assets/59b8503f-827d-4c01-90f2-748468bfcfa0)
![image](https://github.com/user-attachments/assets/d04ad6f3-7f0f-4009-95cb-39104f234735)



## The Algorithm

* My classification AI categorizes different images into predefined classes or categories based on data that it given to it. I decided on 11 celestial objects or bodies listed above. I created a database of 60 images of each class and input them into the Jetson Nano. The model was then trained to classify each image into its correct class.
* Training a model involves feeding the a section of the correctly labeled data into the chosen algorithm. The algorithm learns from the data to create a model that, for this program, correctly classifies images of celestial bodies into their classes. This process involves adjusting the model to minimize the errors and running it for multiple dollar bills.
* After the AI is trained, it is tested. The model's performance is evaluated using a separate set of data, the test set. Once trained and evaluated, the model can be used to make predictions for images it's never seen before. The images are fed into the model, which then outputs the predicted class based on what it's already learned. To the re-trained ResNet-18 model for testing it needs to be converted into ONNX format. ONNX is an open model format that supports many popular machine learning frameworks, and it simplifies the process of sharing models between tools.
* In conclusion, the algorithm teaches computers to sort things into the correct classes by showing them lots of examples. It learns from these examples and then makes predictions about new things based on what it learned. 

## Running this project

1. Connect to your Jetson Nano and connect via SSH on VSCode

2. Download all of the files included in this repository as a .zip.

3. Ensure the jetson-inference library has been installed on your Jetson Nano.

4. Upload and unzip the code in your Nano under the jetson-inference/python/training/classification directory

5. Run the code

  * To run the code and have the input be your own video/image file, put that file within the jetson-inference folder on your Nano. Once that is completed, continue and run: imagenet --model=/home/nvidia/jetson-inference/python/training/classification/models/celestial/resnet18.onnx --labels=/home/nvidia/jetson-inference/python/training/classification/models/celestial/labels.txt --input-blob=input_0 --output-blob=output_0 /[path-to-your-file] /[path-to-where-you-want-the-image-to-be-output]

6. Open the output image that will have appeared and see the results

   [Here is the video guide to using the algorithm.](https://www.youtube.com/watch?v=kKGlmmkxOJ8)
