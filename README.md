# tf-fastapi-docker-iris
Para reproducir el proceso de creación y despliegue de un modelo para predecir el tipo de flor.

Considerations:

Directory structure, where data transformations (if any), training, predictions, among other things, are separated.
Modularization of code using Object Oriented Programming.
Refactoring of functions to avoid duplication in actions.
Optimization of actions to make the project faster and more efficient.
Annotations to improve the reading of the code.
Docstrings to document the code.
Integration of logs (Logging) to record what happens in the project.
Add unit and integration tests.
Add file .gitignore
Add file requirements.txt with list of dependencies
Add a README.md file to the project.

Data
The Iris dataset is a simple, yet popular dataset consisting of 150 observations. Each observation captures the sepal length, sepal width, petal length, petal width of an iris (all in cm) and the corresponding iris subclass (one of setosa, versicolor, virginica).

Setup
Clone the project
Just open your terminal, go or create a directory, and run the following command:
$ git clone https://github.com/carloslme/tf-fastapi-docker-iris.git
- Change the branch: 
$ git checkout refactor

Create virtual environment
Create a virtual environment with:
python3 -m venv venv
Activate the virtual environment
source venv/bin/activate

Install the other libraries
Run the following command to install the other libraries.

pip install -r requirements.txt

Usage
Predict dummy value
Run the following command
python src/classifier/predict_iris.py   
You should get something like this
DEBUG: 2022-11-16 22:37:12,164|__main__|input_data: [3, 4, 5, 8]
INFO: 2022-11-16 22:37:12,165|iris_classifier|Iris dataset loaded.
INFO: 2022-11-16 22:37:12,199|iris_classifier|Iris model trained.
INFO: 2022-11-16 22:37:12,201|iris_classifier|Iris model exported.
INFO: 2022-11-16 22:37:12,201|iris_classifier|Iris types defined.
INFO: 2022-11-16 22:37:12,202|iris_classifier|Iris model loaded.
DEBUG: 2022-11-16 22:37:12,202|__main__|prediction: {'class': 'virginica', 'probability': 1.0}

Run unit tests
Open the terminal, and run
pytest tests/unit/test_classification_response.py -v
You should see something like this: