# Intelligent-Plant-Pathology-Solution
I have developed an intelligent plant disease diagnosis system using advanced image processing and deep learning models like VGG16. The diverse dataset ensures accurate results. Experience easy plant image uploads and prompt diagnoses through an user-friendly web application.

**Dataset Description:**
The dataset contains images of plant leaves from three different plant categories: potato, tomato, and pepper. Each category has multiple classes, including healthy and diseased states. For potato, the classes are potato healthy, potato late blight, and potato early blight. For tomato, the classes include tomato target spot, tomato mosaic virus, tomato yellow leaf curl virus, tomato bacterial spot, tomato early blight, tomato healthy, tomato late blight, tomato leaf mold, tomato septoria leaf spot, and tomato spider mites two-spotted spider mite. For pepper, the classes are pepper bell bacterial spot and pepper bell healthy. The dataset aims to assist in the detection and classification of plant diseases to help farmers take necessary measures to protect their crops. In total, there are around 20,000 images in the dataset, with a varying number of images per class.
Dataset Link: https://www.kaggle.com/datasets/emmarex/plantdisease

**Architecture Diagram**
![image](https://github.com/nikhil-188/Intelligent-Plant-Pathology-Solution/assets/84719583/ac1f7f7c-c7d5-496a-9bff-f7d286c2846c)

Web Interface: - The interface will be built using ReactJS where the user can upload the leaf images which will be sent as a POST request to the FastAPI server. The FastAPI server retrieves the uploaded image and its metadata, such as filename and content type. 
Disease Mapping: - Now the pre-processed image will be fed into the trained and selected deep learning model which analyzes the image to determine the type of disease based on the extracted features. 
Showing results: - The model's predictions will be returned as a JSON object, which is sent back to the users front end interface through FastAPI server. 
Pesticide Suggestion: - Once the trained deep learning model has identified the type of disease affecting the crop in the uploaded image, the system can access a database of known pesticides and their effectiveness against that disease. The system can then suggest appropriate pesticides that have been proven to be effective against that disease. 
In addition to suggesting appropriate pesticides, the system can also provide information about the appropriate dosage, application frequency, and any precautions that need to be taken when using the recommended pesticide. 
Deep learning model architecture
Dataset collection: Collecting datasets from Kaggle that have labeled images of diseased crops from various regions and weather conditions. 
Preprocessing images: Before the images can be used to train a deep learning model, they need to be preprocessed to standardize their size and color and to remove any background noise or other artifacts. Preprocessing can include tasks such as resizing, cropping, normalization, and data augmentation. 
Model planning and building: This step includes planning and building a customized model using several architectures like CNN, VGG, Inception, etc by adding a suitable number of convolutions, max-pooling layers, and activation functions. 
Training model: Now these preprocessed images will be fed into the model, and optimized using regularization, and hyper parameter tuning. 
Model evaluation and selection: The models built will be evaluated using several performance metrics such as precision, recall, and F1 score, based on which the final deployment model will be selected.

**Proposed methodology:**
The proposed methodology for our plant disease diagnosis and remediation system involves several key steps. First, we use image processing techniques to classify the uploaded image and identify the plant name. This is accomplished by training a deep learning model on a dataset of images of different plants, including potato, tomato, and pepper, each with several classes representing different disease states and healthy plants.
Next, we used the same approach to identify any diseases present in the uploaded image of the plant. This is done by training and testing separate models for each plant and disease class, using CNN and pre-trained VGG16 (using transfer learning). And ultimately selected CNN architecture based on several performance metrics. For example, if the uploaded image is of a tomato plant, the system will use the tomato disease model to determine if the plant has any of the common tomato diseases such as target spot or early blight.
If the plant is found to be diseased, the system will recommend specific pesticides that are effective against the identified disease. These recommendations are from the dataset, which we created on own and are based on extensive research and manual note-taking on the most effective pesticides for each disease, and are presented to the user in an easy-to-understand format.
Finally, the system is implemented using the fast API framework to create a user-friendly web application. This allows farmers to easily upload images of their plants and receive quick and accurate diagnoses of any diseases present, as well as recommendations for appropriate remediation measures.
Overall, our proposed methodology leverages state-of-the-art deep learning techniques and extensive research on plant diseases and their treatments to create a powerful tool for farmers to diagnose and treat plant diseases quickly and effectively, leading to higher crop yields and a more sustainable agricultural sector

**Results:**
Home page of the website:
![image](https://github.com/nikhil-188/Intelligent-Plant-Pathology-Solution/assets/84719583/9c35eb3f-6461-4ca6-99cf-21ad50420fb0)

After clicking on get started
![image](https://github.com/nikhil-188/Intelligent-Plant-Pathology-Solution/assets/84719583/2070a275-afe1-48d0-a5ed-016b22373f4c)

If farmer clicks on choose file
![image](https://github.com/nikhil-188/Intelligent-Plant-Pathology-Solution/assets/84719583/16c00b97-4b2f-490a-ba7b-2f4fa0c785a5)

Here he can choose whatever leaf image, for which he wants to know the plant name, leaf disease and pesticides and chemicals.
Our website is predicting the given image as Potato, and disease as Early Blight and recommending the pesticides and chemicals that can be used
![image](https://github.com/nikhil-188/Intelligent-Plant-Pathology-Solution/assets/84719583/12d5a69c-56e8-447d-a941-f75f20347504)


