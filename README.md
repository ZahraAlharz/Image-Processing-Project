Corrosion Detection in Gas Pipelines

Overview
This project focuses on developing an advanced machine learning model to detect corrosion in gas pipelines efficiently. By utilizing image processing techniques and the lightweight MobileNetV2 architecture, the project achieves high accuracy in identifying potential pipeline defects. The system significantly enhances early detection, reducing maintenance costs and preventing system failures in critical energy infrastructure.
Objectives
•	Develop a reliable image preprocessing pipeline for corrosion detection.
•	Implement a MobileNetV2-based CNN model for multi-class classification.
•	Achieve high accuracy in identifying pipeline conditions, such as leaks, cracks, and water presence.

Dataset
The dataset used in this project consists of 1,567 images from the Roboflow platform, labeled for five classes:
•	Crack
•	Gas
•	Leak
•	No Leak
•	Water

Key steps in data preparation:
1.	Preprocessing: Auto-orientation, resizing, cropping, and normalization.
2.	Augmentation: Grayscale conversion, hue adjustment, bounding box cropping, and brightness changes.
   
Model Architecture
The MobileNetV2 architecture was chosen for its lightweight design and efficiency, featuring:
•	Depthwise Separable Convolutions for reduced computational cost.
•	Inverted Residuals for increased accuracy.
•	Linear Bottlenecks to minimize information loss.
•	Squeeze-and-Excitation Blocks for adaptive feature recalibration.

Additional Layers:
•	A Conv2D layer with 256 filters.
•	A Flatten layer for dimensionality reduction.
•	A Dense layer for classification using the Softmax activation function.

Methodology
1.	Preprocessing: Auto-orientation and augmentation methods were applied to enhance dataset quality. Bounding box information was normalized for consistent scaling.
2.	Model Training: MobileNetV2 was fine-tuned with additional layers and trained using the Adam optimizer. Cross-entropy loss was employed to evaluate classification accuracy.
3.	Evaluation: The dataset was split into 80% training and 20% validation. The model achieved a validation accuracy of 95.63%.
4.	Inference: The trained model predicts pipeline conditions by classifying images into one of the five predefined categories.

Results
The proposed model achieved:
•	Initial Training Accuracy: 92.53%
•	Final Training Accuracy: 94.92%
•	Validation Accuracy: 95.63%
These results demonstrate the model's capability to accurately classify various pipeline conditions, making it a powerful tool for real-world applications.

Technologies Used
•	Python: Programming language
•	TensorFlow/Keras: Deep learning framework
•	OpenCV: Image processing library
•	NumPy: Numerical computation
 
Usage
1.	Clone this repository: 
git clone https://github.com/ZahraAlharz/Image-Processing-Project.git
2.	Install dependencies: 
pip install -r requirements.txt
3.	Run the preprocessing script: 
python preprocess.py
4.	Train the model: 
python train.py
5.	Test the model: 
python test.py

Future Work
•	Expand the dataset to further improve model generalization.
•	Explore additional CNN architectures for enhanced performance.
•	Integrate the system into a real-time monitoring pipeline.

Contributors
•	Zahra Alharz
•	Shahad Alshammary
•	Maha Alrashidi
•	Leena Alessa
•	Afnan Rayyani
•	Zeina Alabido

Acknowledgments
We express our gratitude to Dr. Sara Althubaiti for her invaluable guidance throughout this project.

References
1.	Wright, R.F., et al. "Corrosion Sensors for Structural Health Monitoring of Oil and Natural Gas Infrastructure: A Review." Sensors, 19(18), p.3964.
2.	Roboflow Computer Vision Tools: Roboflow Universe
3.	MobileNetV2 Explained: Papers with Code
4.	Bento, M.P., et al. "Image Processing Techniques applied for Corrosion Damage Analysis." Proceedings of the IEEE International Conference on Image Processing, 2009.

Note: Due to confidentiality considerations, I am unable to share the research document or its contents publicly.
