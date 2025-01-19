# Installation and Running Instructions for Retinal Vessel Segmentation Model on MacBook M4 Max 2024 with macOS Sequoia 15.3

## Step 1: Install Homebrew
Homebrew is a package manager for macOS that simplifies the installation of software. Open the Terminal and run the following command to install Homebrew:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Step 2: Install Python
Install Python using Homebrew:

```sh
brew install python
```

## Step 3: Install Virtualenv
Virtualenv is a tool to create isolated Python environments. Install it using pip:

```sh
pip install virtualenv
```

## Step 4: Create a Virtual Environment
Create a virtual environment for the project:

```sh
virtualenv retina_venv
```

Activate the virtual environment:

```sh
source retina_venv/bin/activate
```

## Step 5: Install Required Python Packages
Navigate to the `Retina Blood Vessel Segmentation` directory and install the required Python packages using the `requirements.txt` file:

```sh
pip install -r requirements.txt
```

If the `requirements.txt` file does not exist, manually install the required packages:

```sh
pip install numpy scipy matplotlib scikit-learn keras tensorflow h5py pillow opencv-python
```

## Step 6: Download the DRIVE Dataset
Download the DRIVE dataset from [this link](https://drive.google.com/open?id=17wVfELqgwbp4Q02GD247jJyjq6lwB0l6) and extract both training and test folders in a folder named `DRIVE`.

## Step 7: Prepare the Dataset
Run the `prepare_datasets_DRIVE.py` script to prepare the dataset:

```sh
python prepare_datasets_DRIVE.py
```

## Step 8: Extract Patches
Run the `save_patch.py` script to extract patches from the training set:

```sh
python save_patch.py
```

## Step 9: Train the Model
Run the `train_retina.py` script to train the model:

```sh
python train_retina.py
```

## Step 10: Evaluate the Model
Run the `evaluate.py` script to evaluate the model:

```sh
python evaluate.py
```

## Step 11: Deactivate the Virtual Environment
Once you are done, deactivate the virtual environment:

```sh
deactivate
```

## Additional Notes
- Ensure that you have a stable internet connection for downloading packages and datasets.
- If you encounter any issues, refer to the official documentation of the respective tools and libraries for troubleshooting.
