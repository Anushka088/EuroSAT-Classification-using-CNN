<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Satellite Land Cover Classification Project</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; max-width: 900px; margin: auto; padding: 20px; }
        h1 { color: #2c3e50; border-bottom: 2px solid #3498db; padding-bottom: 10px; }
        h2 { color: #2980b9; margin-top: 30px; }
        .badge { display: inline-block; padding: 5px 12px; border-radius: 4px; color: white; font-weight: bold; font-size: 14px; margin-right: 5px; }
        .bg-pytorch { background-color: #ee4c2c; }
        .bg-python { background-color: #3776ab; }
        .bg-colab { background-color: #f9ab00; }
        code { background-color: #f4f4f4; padding: 2px 5px; border-radius: 3px; font-family: 'Courier New', Courier, monospace; }
        pre { background: #2d3436; color: #dfe6e9; padding: 15px; border-radius: 5px; overflow-x: auto; }
        .container { border: 1px solid #ddd; border-radius: 8px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        ul { list-style-type: square; }
    </style>
</head>
<body>

<div class="container">
    <h1>🛰️ Satellite Land Cover Classification</h1>
    
    <div>
        <span class="badge bg-colab">Google Colab Ready</span>
        <span class="badge bg-pytorch">PyTorch</span>
        <span class="badge bg-python">Python 3.8+</span>
    </div>

    <h2>📋 Project Overview</h2>
    <p>
        This project focuses on <strong>Automated Land Cover Classification (LCC)</strong> using Deep Learning. 
        By implementing a <strong>ResNet-50</strong> Convolutional Neural Network, the model successfully 
        classifies high-resolution satellite imagery into 10 distinct environmental categories. 
        This mirrors industry-standard workflows used by organizations such as <strong>NRSC/ISRO</strong> 
        for geospatial analysis and urban planning.
    </p>

    <h2>🏗️ Technical Architecture</h2>
    <ul>
        <li><strong>Backbone:</strong> ResNet-50 (Transfer Learning from ImageNet)</li>
        <li><strong>Data Pipeline:</strong> Customized <code>torchvision</code> transforms including normalization and random flips for robust augmentation.</li>
        <li><strong>Classification Head:</strong> Fully connected layers with Dropout (0.3) to prevent overfitting.</li>
        <li><strong>Optimization:</strong> Adam Optimizer with Negative Log-Likelihood Loss (NLLLoss).</li>
    </ul>

    <h2>📊 Dataset Details</h2>
    <p>
        The model was trained on the <strong>EuroSAT (RGB)</strong> dataset, derived from Sentinel-2 satellite imagery.
        Classes include: <em>Annual Crop, Forest, Herbaceous Vegetation, Highway, Industrial, Pasture, Permanent Crop, Residential, River, Sea Lake.</em>
    </p>

    <h2>📈 Key Performance Results</h2>
    <ul>
        <li><strong>Accuracy:</strong> ~96% on Validation Set.</li>
        <li><strong>Efficiency:</strong> Leveraged GPU acceleration (T4) in Colab for fast convergence.</li>
        <li><strong>Evaluation:</strong> Performance verified via Confusion Matrix and F1-score analysis.</li>
    </ul>

    <h2>🛠️ How to Run</h2>
    <p>1. Install the required libraries:</p>
    <pre>pip install torch torchvision matplotlib seaborn scikit-learn tqdm</pre>
    
    <p>2. Open the notebook in Google Colab, upload your <code>EuroSAT_Upload.zip</code>, and execute the training cells.</p>

    <hr>
    <p style="text-align: center;"><em>Developed for Portfolio - 2024</em></p>
</div>

</body>
</html>
