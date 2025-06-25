# 🌱 Smart Crop Recommendation System

An AI-powered web application that provides intelligent crop recommendations based on soil nutrients, climate conditions, and environmental factors. This system uses machine learning algorithms to help farmers make informed decisions about crop selection.

## 🎯 Features

- **Dual AI Models**: Choose between Random Forest and K-Nearest Neighbors algorithms
- **Real-time Predictions**: Get instant crop recommendations based on input parameters
- **Interactive Web Interface**: User-friendly design with tooltips and visual feedback
- **High Accuracy**: Models trained on agricultural datasets with 92-95% accuracy
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 📋 Prerequisites

Before running the application, make sure you have the following installed on your system:

- **Python 3.7 or higher**
- **Flask** (Python web framework)
- **Required Python packages** (see requirements.txt)

## 🚀 Installation & Setup

### Step 1: Clone or Download the Project
```bash
# If using Git
git clone https://github.com/swasthikdevadiga1/Data-Science
cd Data-Science

# Or download and extract the project folder
```

### Step 2: Install Required Dependencies
```bash
# Install Flask and other required packages
pip install flask
pip install pandas numpy scikit-learn pickle

# OR install all dependencies from requirements.txt
pip install -r requirements.txt
```

### Step 3: Verify Project Structure
Make sure your project folder contains these files:
```
crop-recommendation-system/
├── app.py                 # Main Flask application
├── train_model.py         # Model training script (already executed)
├── requirements.txt       # Python dependencies
├── templates/
│   └── index.html        # Web interface template
├── crop_model_rf.pkl     # Trained Random Forest model
├── crop_model_knn.pkl    # Trained KNN model
├── label_encoder.pkl     # Label encoder for crop names
├── feature_scaler.pkl    # Feature scaler for input normalization
└── README.md             # This file
```

**Note**: The `.pkl` files contain pre-trained models, so you don't need to run `train_model.py` unless you want to retrain the models.

## 🖥️ Running the Application

### Step 1: Open Terminal/Command Prompt
Navigate to your project folder:
```bash
cd path/to/your/crop-recommendation-system
```

### Step 2: Start the Flask Application
```bash
python app.py
```

### Step 3: Access the Web Application
After running the command, you'll see output similar to:
```
* Running on http://127.0.0.1:5000
* Debug mode: on
```

Open your web browser and go to: **http://127.0.0.1:5000/** or **http://localhost:5000/**

## 📖 How to Use

### Input Parameters
Enter the following soil and climate parameters:

1. **Nitrogen (N)**: Nitrogen content in soil (ppm)
   - Example: 90
   - Range: Typically 0-150

2. **Phosphorus (P)**: Phosphorus content in soil (ppm)
   - Example: 42
   - Range: Typically 0-100

3. **Potassium (K)**: Potassium content in soil (ppm)
   - Example: 43
   - Range: Typically 0-100

4. **Temperature**: Average temperature in Celsius
   - Example: 25.5
   - Range: Typically 15-40°C

5. **Humidity**: Relative humidity percentage
   - Example: 82
   - Range: 20-100%

6. **pH Level**: Soil pH level
   - Example: 6.5
   - Range: 4.0-9.0 (7.0 is neutral)

7. **Rainfall**: Annual rainfall in millimeters
   - Example: 200
   - Range: Typically 50-3000mm

### Model Selection
Choose between two AI models:

- **🌲 Random Forest**: Higher accuracy (95%), uses multiple decision trees
- **🎯 K-Nearest Neighbors**: Good accuracy (92%), uses pattern matching

### Getting Results
1. Fill in all the required parameters
2. Select your preferred AI model
3. Click "🚀 Get Crop Recommendation"
4. View your personalized crop recommendation with model accuracy

## 🔧 Troubleshooting

### Common Issues:

**1. Flask not found error:**
```bash
pip install flask
```

**2. Module import errors:**
```bash
pip install pandas numpy scikit-learn
```

**3. Port already in use:**
- Try a different port by modifying `app.py`:
```python
if __name__ == "__main__":
    app.run(debug=True, port=5001)  # Change port number
```

**4. Template not found error:**
- Ensure `index.html` is in the `templates/` folder
- Check the folder structure matches the requirements

**5. Model files not found:**
- Make sure all `.pkl` files are in the project root directory
- If missing, run `python train_model.py` to generate them

### Performance Tips:
- Use Random Forest model for better accuracy
- Ensure input values are within realistic ranges
- Check your internet connection for CSS/styling to load properly

## 📊 Model Information

### Random Forest Classifier
- **Accuracy**: ~95%
- **Algorithm**: Ensemble of decision trees
- **Best for**: Complex pattern recognition, high accuracy requirements

### K-Nearest Neighbors (KNN)
- **Accuracy**: ~92%
- **Algorithm**: Instance-based learning
- **Best for**: Pattern matching, interpretable results

### Supported Crops
The system can recommend various crops including:
- Rice, Wheat, Barley, Maize
- Banana, Mango, Grapes, Apple
- Cotton, Jute, Coffee
- And many more agricultural crops

## 🛠️ Technical Details

### Technology Stack:
- **Backend**: Python Flask
- **Frontend**: HTML5, CSS3, JavaScript
- **Machine Learning**: Scikit-learn
- **Data Processing**: Pandas, NumPy

### File Descriptions:
- `app.py`: Main Flask application with routing and prediction logic
- `train_model.py`: Model training script (pre-executed)
- `index.html`: Responsive web interface with modern UI/UX
- `*.pkl files`: Serialized trained models and preprocessing components

## 📝 Notes for Developers

### Retraining Models:
If you want to retrain the models with new data:
1. Place your `Crop_recommendation.csv` in the project folder
2. Run: `python train_model.py`
3. New model files will be generated

### Customization:
- Modify `templates/index.html` for UI changes
- Update `app.py` for backend logic modifications
- Add new models by updating both training and prediction scripts

## 📞 Support

If you encounter any issues:
1. Check the troubleshooting section above
2. Verify all dependencies are installed correctly
3. Ensure Python version compatibility (3.7+)
4. Check that all required files are present in the project directory

## 🎉 Success!

Once everything is set up correctly, you should see a beautiful, responsive web interface where you can input soil and climate parameters to get AI-powered crop recommendations. The system will help optimize agricultural decisions based on scientific data and machine learning algorithms.

---

**Happy Farming! 🌾** Use this tool to make informed crop selection decisions and optimize your agricultural yield.
