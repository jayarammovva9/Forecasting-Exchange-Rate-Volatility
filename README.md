Forecasting USD/INR Exchange Rate Volatility

This project focuses on forecasting the volatility of the USD/INR currency pair using a multivariate deep learning approach. The core model is a stacked Long Short-Term Memory (LSTM) network enhanced with an attention mechanism. Its performance is compared against standard econometric models such as GARCH(1,1), GJR-GARCH, and HAR-RV.

Project Summary

Exchange rate volatility creates financial uncertainty for firms operating internationally. Anticipating volatility patterns helps businesses manage risk, optimise hedging decisions, and budget more effectively.
This work builds a forecasting pipeline that integrates market and macro-financial variables, processes them into time-series features, and trains neural models to detect evolving patterns in volatility.

Dataset

Data is sourced entirely from open-access providers.
It includes daily observations from 2007–2025.

Variables used:

USD/INR

S&P 500

VIX

Gold prices

Crude oil (WTI)

U.S. Treasury yields (10Y, 1Y, 3M)

CPI (India)

Sources include:

Yahoo Finance

Federal Reserve Economic Data (FRED)

RBI Database on Indian Economy (DBIE)

The realised volatility target is constructed using the 21-day rolling standard deviation of USD/INR log-returns, annualised.

Method Overview

Clean and align daily data from multiple sources

Generate log returns and realised volatility

Create HAR-style lagged features (daily, weekly, monthly)

Build feature window sequences for neural modelling

Train a stacked LSTM with an attention module

Fit and compare benchmark models (HAR-RV, GARCH, GJR-GARCH)

Evaluate performance using RMSE, MAE

Visualise forecast behaviour against realised volatility

Model Details

The deep learning model consists of:

Two sequential LSTM layers

A custom attention layer to emphasise the most influential time periods

Dropout regularisation

Dense final layer to generate volatility forecasts

Econometric benchmarks:

GARCH(1,1)

GJR-GARCH(1,1)

HAR-RV (linear regression)

Key Findings

The stacked LSTM with attention showed measurable gains over GARCH-based methods and demonstrated an ability to learn complex market effects.
HAR-RV remained a strong statistical baseline.

Contents

Raw and processed data folder (placeholder)

Notebook containing end-to-end workflow

Source files for LSTM and comparison models

Figures and result outputs

Requirements list for environment setup

Reproducibility

All data sources are public, and the full codebase is available to enable complete replication of results.
The workflow runs end-to-end from data preparation to model training and evaluation.

Extensions

The project can be extended to:

Multi-head attention

Transformer architectures

Regime-shift analysis

Probabilistic forecasts

Rolling walk-forward evaluation

Authors

Chaganty Sai Anirudh

Gaurav Nautiyal

Jayaram Movva

Goa Institute of Management — Big Data Analytics
