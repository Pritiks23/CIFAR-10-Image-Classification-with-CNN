

# CIFAR-10 Image Classification with CNN
<img width="386" height="416" alt="Screen Shot 2025-09-05 at 9 29 29 PM" src="https://github.com/user-attachments/assets/220d617f-9493-44b7-b58a-85040916d2bc" />
<img width="813" height="626" alt="Screen Shot 2025-09-05 at 9 30 22 PM" src="https://github.com/user-attachments/assets/3bcd2bc4-c3fb-4c74-abea-cfdf4b61426f" />

## Technical Overview  

I built a convolutional neural network (CNN) to classify images from the CIFAR-10 dataset. The dataset has 60,000 color images (32x32x3) across 10 classes such as airplanes, cars, cats, dogs, and more.  

The model is a Sequential CNN with:  
- Conv2D + ReLU for feature extraction  
- BatchNormalization for stable training  
- MaxPooling2D for downsampling  
- Another Conv2D layer for deeper features  
- Flatten → Dense → Softmax for classification  
##Check it out here: https://colab.research.google.com/drive/1N--_liw2MS_d1yh8lqBcHNNsVD0h4EfM?usp=sharing

Training setup:  
- Optimizer: Adam  
- Loss: Categorical Crossentropy  
- Metrics: Accuracy  
- Callbacks: EarlyStopping and ModelCheckpoint to avoid overfitting and save the best model  

The model was evaluated on the test set and visualized on random test samples. I also tested interactive uploads in Colab, resizing custom images to 32x32 and running predictions. A confusion matrix was generated to analyze misclassifications (e.g., cars vs trucks, cats vs dogs).  

The model was saved in both `.h5` (legacy) and `.keras`  formats for reloading later.  

---

## Key Takeaways  

- CNNs are a strong baseline for image classification — even a simple one works decently on CIFAR-10  
- Preprocessing (normalizing inputs) is critical  
- Callbacks (EarlyStopping + ModelCheckpoint) make training more efficient and safer  
- Visualization (plots + confusion matrix) highlights where the model struggles  
- The modern way to save models is with `.keras` format instead of `.h5`  
- Colab makes it easy to train, test, and deploy small demos without worrying about environment setup  
