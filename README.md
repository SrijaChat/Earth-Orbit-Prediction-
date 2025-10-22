# Earth-Orbit-Prediction-
This is a fun mini project which predicts the coordinate(in (x,y,z)) of earth with respect to the sun across different dates till 2030.

## Model Training
- Data Collection: Utilizes the astroquery library to fetch Earth's position data from JPL Horizons. The AD (Anno Domini) prefix in the date strings is removed to standardize the datetime format.

- Feature Engineering: Introduces cyclical features to capture the periodic nature of Earth's orbit. Specifically, the day of the year is transformed using sine and cosine functions to represent its cyclical behavior.

- Model Architecture: Employs a Sequential neural network model with two hidden layers, each containing 64 neurons and ReLU activation functions. The output layer predicts the 3D coordinates (x, y, z) of Earth's position.

- Model Training: The model is trained using the Adam optimizer and mean squared error loss function over 300 epochs.

## Why AD removal and use Cyclical Features?
- AD Removal: Standardizes date formats by removing the "A.D." prefix, ensuring consistency in datetime operations.

- Cyclical Features: Earth's position exhibits periodic behavior. By transforming the day of the year into sine and cosine components, we capture this cyclical nature, allowing the model to learn patterns more effectively.


