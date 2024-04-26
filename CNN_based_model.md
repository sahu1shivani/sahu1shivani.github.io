# Gender Image Recognition 🖼️

![GIR](/img1.png)

## Overview 📄

The **Gender Image Recognition** project is designed to classify images into four categories based on gender and emotional expression: HappyMale, HappyFemale, SadMale, and SadFemale. This system uses machine learning techniques to achieve accurate predictions with the help of pre-trained models and custom datasets.

## Project Structure 🏗️

- **Data Preparation**: Load and prepare your data efficiently using H5 files.
- **Model Building**: Leverage TensorFlow and Keras to build a deep learning model.
- **Training and Evaluation**: Train the model on the dataset and evaluate its performance.
- **Prediction**: Implement functionality to predict and categorize new images.

## Installation 🛠️

Before running the project, install the required libraries:

```bash
pip install numpy h5py pillow matplotlib tensorflow scikit-learn tqdm
```

# Usage 🔧

Here's how to run the project:

## 1. Load the Dataset:
Load your images and labels from H5 files to prepare the dataset for training and testing.
```python
train_images, train_labels = load_h5_dataset('path/to/train.h5', 'train_set_x', 'train_set_y')
```
## 2. Inspect Dataset Files:
Quickly inspect H5 files to understand their structure and contents.
```python
inspect_h5_file('path/to/dataset.h5')
```
## 3. Model Training:
Train your model using the pre-processed images and labels.
```python
history = model.fit(x_train, y_train, validation_data=(x_val, y_val), epochs=10, batch_size=32)
```

## 4. Evaluate the Model:
Assess the model's performance on a separate test dataset.
```python
test_loss, test_accuracy = model.evaluate(test_images, test_labels)
print(f"Test Accuracy: {test_accuracy}, Test Loss: {test_loss}")
```
## 5. Predict New Images:
Use the trained model to predict the category of new images.
```python
result = detect_happy(model, 'path/to/new/image.jpg')
print(f"The image is: {result}")
```

## Results 📊
The model achieved a test accuracy of over 95%, demonstrating high efficacy in recognizing gender and emotional expressions from images.

## Future Work 🔮
Future enhancements may include:
- Increasing the dataset size for better model generalization.
- Experimenting with different model architectures.
- Implementing real-time image recognition.

## Contributions 🤝
Contributions are welcome! If you have suggestions or improvements, please fork the repo and submit a pull request.

## License 📜
Distributed under the MIT License. See `LICENSE` for more information.

Happy coding! 😄 Feel free to star ⭐ this repo if you find it useful!


