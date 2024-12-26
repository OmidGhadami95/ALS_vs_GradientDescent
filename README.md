# ALS_vs_GradientDescent
Matrix Factorization (ALS vs Gradient Descent)

<a href="https://ibb.co/b28BMgQ"><img src="https://i.ibb.co/dLz2w0j/Screenshot-12-25-2024-11-06-37-PM.png" alt="Screenshot-12-25-2024-11-06-37-PM" border="0"></a>


This code implements two collaborative filtering approaches for movie rating prediction: Gradient Descent and Alternating Least Squares (ALS). Both methods use matrix factorization to learn latent factors for users and items.

Data Preparation:

The code loads training and validation datasets from CSV files.
It creates user-item rating matrices and centers the ratings by subtracting user and item means.

Gradient Descent Model:

Initializes user and movie factor matrices with random values.
Uses Mean Absolute Error (MAE) as the loss function.
Implements gradient descent with dynamic learning rate and gradient clipping.
Applies regularization to prevent overfitting.
Trains for 100 epochs with a batch size of 2000.

ALS Model:

Initializes user and item matrices with random values.
Uses Alternating Least Squares optimization.
Applies regularization (lambda_reg = 0.0001).
Trains for 50 iterations with 200 latent factors.
Evaluation and Visualization

Both models:

Calculate MAE on validation set after each epoch/iteration.
Plot training and validation loss curves.
Visualize actual vs. predicted ratings.
Save predictions to CSV and TXT files.

Results:

Final MAE values are calculated for both models on the validation set.
Predictions are made on a new test set without ratings.
Predicted ratings are clipped to the valid range (0.5 to 5) and rounded to 3 decimal places.

Analysis:

The Gradient Descent model uses a dynamic learning rate and gradient clipping for stability.
The ALS model alternates between updating user and item factors, potentially converging faster.
Both models handle the cold start problem by using global means for unknown user-item pairs.
The code provides a comprehensive implementation of two popular collaborative filtering techniques, allowing for comparison of their performance on the movie rating prediction task.
