# Option Pricing and Volatility Analysis in Python

This repository contains a Python script for option pricing and volatility analysis. The main functionalities are implemented in three core functions, `normal_cdf`, `bs_eur`, and `apply_iv`.

## Core Functions

- `normal_cdf(mu, sigma, x)`: Calculates the cumulative density function (CDF) for a normal distribution. Used in the `bs_eur` function to calculate the cumulative probability distributions N(d1) and N(d2) for the Black-Scholes formula.

- `bs_eur(ex_price, int_rate, cur_price, time, vol, option, mu=0)`: Utilizes the Black-Scholes formula to compute the price of a European option (either 'call' or 'put'). It requires parameters like the current price of the underlying asset, the exercise price of the option, the risk-free interest rate, the time until option expiry, and the asset's volatility.

- `apply_iv(in_filename, out_filename, plot_filename=None,*, ex_price_field, option_val_field, iv_field, cur_price, int_rate, maturity_time, option_type)`: Reads data from an input CSV file, computes implied volatilities using the `bs_eur_estimate_iv` function (not included in the provided code), and writes the output to another CSV file. Optionally, it generates a volatility smile plot and saves it as an image file.

- `root_bisection(f, a, b)`: Implements the Bisection method to find a root of a continuous function within a specified interval. The function is used internally for numerical computations.

## Usage

Please note that the actual function calls and usage will depend on your specific use case, your input data, and where you want to output the results. Make sure to pass the correct parameters to the functions, as per your requirements.

