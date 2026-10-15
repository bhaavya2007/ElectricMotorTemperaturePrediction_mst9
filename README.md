# Electric Motor Winding Temperature Prediction

**AI & Machine Learning Mini Project | UCS321**

**Thapar Institute of Engineering and Technology, Patiala**

## Project Overview

This project uses machine learning to predict the stator winding temperature of a Permanent Magnet Synchronous Motor (PMSM) from electrical, mechanical, and thermal operating parameters.

Two regression algorithms were implemented and compared: Linear Regression and Random Forest Regressor.

## Dataset

- Source: [Electric Motor Temperature Dataset — Kaggle](https://www.kaggle.com/datasets/wkirgsn/electric-motor-temperature)
- Cleaned observations: 98,198
- Input features: 9
- Target variable: `stator_winding`
- Training/testing split: 80:20

### Input Features

`u_q`, `u_d`, `i_d`, `i_q`, `pm`, `motor_speed`, `coolant`, `ambient`, `torque`

## Technologies Used

- Python
- Google Colab
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn

## Machine Learning Models

**Linear Regression:** Used as the baseline regression model.

**Random Forest Regressor:** Used to capture more complex relationships between motor operating parameters and winding temperature.

## Model Results

| Model | MAE (°C) | RMSE (°C) | R² |
|---|---:|---:|---:|
| Linear Regression | 3.6739 | 5.9473 | 0.95519 |
| Random Forest | 0.05886 | 0.30747 | 0.999880 |

Random Forest achieved lower prediction errors on the random test split.

## Visualizations

The notebook includes exploratory data analysis, actual-versus-predicted temperature comparisons, residual analysis, and Random Forest feature importance.

The most important feature identified by Random Forest was `i_d`.

## How to Run

1. Download the notebook from this repository.
2. Open it in Google Colab.
3. Download the original dataset from Kaggle.
4. Upload the dataset to Colab and update the CSV filename or path if required.
5. Run the notebook cells in order.

## Limitations

The models were evaluated using a random train-test split. Their performance on completely unseen motor operating profiles has not yet been established.

## Future Improvements

- Profile-based train-test splitting
- Additional regression algorithms
- Hyperparameter tuning
- Testing on independent motor data

## Author

**Bhaavya Jain**  
Roll Number: 1025150361  
Thapar Institute of Engineering and Technology

**Academic Year:** 2026–2027
