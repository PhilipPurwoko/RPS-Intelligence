## ⛰️ 📄 ✂️ RPS-Intelligence
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/PhilipPurwoko/RPS-Intelligence/blob/main/RPS-Classification.ipynb)

Recognize Rock-Paper-Scissor hand photo using Artificial Intelligence. Multi-class classification using Tensorflow Neural Network :brain:

### 📊 Dataset
- **AUTHOR:** Julien de la Bruère-Terreault (drgfreeman@tuta.io)
- **LICENSE:** CC-BY-SA 4.0
- **DESCRIPTION:** This dataset contains images of hand gestures from the Rock-Paper-Scissors game. The images were captured as part of a hobby project where I developped a Rock-Paper-Scissors game using computer vision and machine learning on the Raspberry Pi (https://github.com/DrGFreeman/rps-cv)
- **CONTENTS:** The dataset contains a total of 2188 images corresponding to the 'Rock' (726 images), 'Paper' (710 images) and 'Scissors' (752 images) hand gestures of the Rock-Paper-Scissors game. All image are taken on a green background with relatively consistent ligithing and white balance.
- **FORMAT:** All images are RGB images of 300 pixels wide by 200 pixels high in .png format. The images are separated in three sub-folders named 'rock', 'paper' and 'scissors' according to their respective class.

### 🧠 Neural Network
```python
# Input Layer
keras.layers.Conv2D(32, kernel_size=(3, 3), activation='relu', input_shape=(IMG_SIZE, IMG_SIZE, 3)),
keras.layers.MaxPooling2D(),
keras.layers.Dropout(0.2),

# Hidden Layer
keras.layers.Conv2D(64, kernel_size=(3,3), activation='relu'),
keras.layers.MaxPooling2D(),
keras.layers.Dropout(0.2),
keras.layers.Conv2D(128, kernel_size=(3,3), activation='relu'),
keras.layers.MaxPooling2D(),
keras.layers.Dropout(0.2),
keras.layers.Conv2D(128, kernel_size=(3,3), activation='relu'),
keras.layers.MaxPooling2D(),
keras.layers.Dropout(0.2),
keras.layers.Flatten(),
keras.layers.Dense(512, activation='relu'),
keras.layers.Dropout(0.2),

# Output Layer
keras.layers.Dense(3),
keras.layers.Activation('softmax')
```
