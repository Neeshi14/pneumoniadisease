# Pneumonia Disease

What is Pneumonia?


Pneumonia is a respiratory infection that inflames the air sacs in one or both lungs. The air sacs may fill with fluid or pus, causing symptoms such as cough, fever, chills, and difficulty breathing. Pneumonia can be caused by a variety of microorganisms, including bacteria, viruses, and fungi.

Common symptoms of pneumonia include:

Cough: Often producing mucus (may be green, yellow, or bloody).


Fever: A high body temperature is a common symptom.


Shortness of breath: Difficulty breathing or rapid breathing.


Chest pain: Sharp or stabbing pain that may worsen with deep breaths or coughing.


Fatigue: Feeling very tired or weak.


Sweating: Profuse sweating, especially in fever.

The severity of pneumonia can range from mild to life-threatening, and certain populations, such as the elderly, young children, and individuals with weakened immune systems, are more vulnerable. Diagnosis is typically based on a combination of symptoms, physical examination, and imaging studies like chest X-rays.

Treatment depends on the underlying cause of pneumonia. Bacterial pneumonia is often treated with antibiotics, while viral pneumonia may require antiviral medications. Supportive care, including rest, hydration, and sometimes hospitalization, may be necessary depending on the severity of the illness.

Preventive measures include vaccination against certain bacteria and viruses that can cause pneumonia, practicing good hand hygiene, avoiding smoking, and maintaining overall health to support a robust immune system. If you suspect you or someone else may have pneumonia, it is important to seek medical attention for an accurate diagnosis and appropriate treatment.



1.  **Download the dataset:**

   Automatically download and extract the dataset from Kaggle.
   You can access the dataset [here](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).




2.  **Prepare the model:**

    The script will perform the following steps:

    * Load the dataset.
    * Preprocess the images (resize, convert to grayscale, normalize).
    * Load the pre-trained ResNet50 model and modify it for binary classification.
    * Train the model.
    * Evaluate the model on the test set.

## Model Architecture

* **Backbone:** ResNet50 (pre-trained on ImageNet)
* **Input:** Grayscale chest X-ray images (150x150 pixels)
* **Modification:** The first convolution layer of the ResNet50 is modified to accept single-channel grayscale images.
* **Classification Head:** A custom classification head with two fully connected layers and a sigmoid activation function is added for binary classification.
* **Loss Function:** Binary Cross-Entropy Loss (BCELoss)
* **Optimizer:** Adam

## Training Details

* **Epochs:** 5
* **Batch Size:** 32
* **Learning Rate:** 0.001
* **Image Size:** 150x150
* **Grayscale Images:** The model processes grayscale images.
* **Transfer Learning:** Pretrained Resnet50 with non frozen layers and the final fully connected layers are trained.
* **Device:** Cuda if available, else CPU.

## Evaluation

The model's performance is evaluated 

-> test accuracy is 68%.

-> Training accuracy is 87%.

## Results

The model achieves good accuracy in detecting pneumonia from chest X-ray images.




