
## Project Overview: 

.Building and Deploying an End-to-End Deep Learning Solution for Lung Tumor Detection on AWS EC2 Using Docker and Jenkins

In this project, our goal was to revolutionize healthcare by accurately classifying chest diseases from CT scan images, thereby enhancing early diagnosis and treatment. We utilized a Transfer Learning approach by downloading a pre-trained Vgg16 model (a CNN architecture) from Keras and fine-tuning it to suit our custom dataset.

The fine-tuning process involved removing the original dense layers and adding a custom dense layer, as our dataset contained only two classes (Normal and Adenocarcinoma), unlike the 1000 classes in the original Imagenet data used for pre-training Vgg16.

The project structure was designed using a data science project template, which ensured the modularity, reusability, and maintainability of the code. This template included modules for logging, exception handling, and utilities.

For experiment tracking and model management, we utilized DagsHub with MLflow, which allowed us to track experiments, compare results, and manage models effectively. We also integrated Data Version Control (DVC) to manage the data pipeline, ensuring reproducibility and collaboration among team members.

## End-to-End Robust Automatic Pipeline Flow:

Data Ingestion: We used the gdown package to ingest CT scan images from Google Drive. The images were then preprocessed to remove noise and normalize pixel values.

Base Model Preparation: We utilized the pre-trained VGG16 model as our base CNN model. To customize it for our dataset, we removed the original dense layers and added a custom dense layer, as our dataset had only two classes.

Model Training: The customized CNN model was trained on the processed dataset. We used a training-validation split to evaluate the model's ability to generalize to new data.

Model Evaluation: The model's performance was assessed on a test dataset. Key metrics such as accuracy, precision, recall, and F1-score were calculated to gauge the model's effectiveness.

MLflow Integration: We integrated MLflow with the model training and evaluation processes, enabling us to track experiments and manage models efficiently.

DVC Pipeline: DVC was incorporated into the data ingestion, model training, and evaluation components, ensuring reproducibility and facilitating collaboration among team members.

Deployment: The entire pipeline was deployed to AWS EC2 using Docker containers, AWS ECR, and Jenkins for CI/CD.

User Application: A user-friendly application was built using Flask, allowing users to upload CT scan images and receive diagnostic results.

By the end of this project, we achieved a high level of accuracy in classifying chest diseases from CT scan images, significantly improving the early diagnosis and treatment of patients with these conditions.


## Files to Update for Each Component:

1. config.yaml: Define and update constants.
2. params.yaml: Specify and adjust parameters.
3. Entity: Update entity definitions.
4. Configuration Manager: Update in the src/config directory.
5. Components: Make necessary updates to individual components.
6. Pipeline: Update the pipeline structure and logic.
7. main.py: Implement changes in the main script.
8. dvc.yaml: Update DVC pipeline configuration.








