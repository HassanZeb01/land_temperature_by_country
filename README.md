\documentclass[12pt]{article}
\usepackage[a4paper, margin=1in]{geometry}
\usepackage{graphicx}
\usepackage{hyperref}
\usepackage{amsmath}
\usepackage{booktabs}
\usepackage{xcolor}
\usepackage{listings}
\usepackage{setspace}

\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    urlcolor=blue
}

\setstretch{1.2}

\begin{document}

\begin{center}
    {\LARGE \textbf{Global Land Temperature Forecasting and CO\textsubscript{2} Emission Analysis}} \\[0.5cm]
    {\large Author: Rizwan} \\
    {\small MSc Data Science | Machine Learning \& AI Enthusiast | London, UK}
\end{center}

\section*{Overview}
This project aims to forecast \textbf{global land temperature} and analyse its relationship with \textbf{CO\textsubscript{2} emissions} using time series and machine learning techniques.  
Two datasets were obtained from \textbf{Kaggle} --- Global Land Temperature and CO\textsubscript{2} Emission datasets --- to understand long-term temperature trends and their possible connection to greenhouse gas emissions.

The study is divided into two main phases:
\begin{enumerate}
    \item \textbf{Phase 1:} Temperature forecasting using SARIMA and LSTM models.
    \item \textbf{Phase 2:} Regression analysis using Random Forest to evaluate the relationship between temperature and CO\textsubscript{2} emissions.
\end{enumerate}

\section*{Objectives}
\begin{itemize}
    \item Forecast global land temperature using statistical and deep learning models.
    \item Evaluate and compare the performance of SARIMA and LSTM models.
    \item Analyse the correlation between CO\textsubscript{2} emissions and temperature using Random Forest regression.
    \item Identify strengths and limitations of different predictive approaches for climate data.
\end{itemize}

\section*{Methodology}

\subsection*{Phase 1: Temperature Forecasting}
\begin{itemize}
    \item \textbf{Dataset:} Global Land Temperature (1743--2013) from Berkeley Earth via Kaggle.
    \item \textbf{Models Used:}
    \begin{itemize}
        \item \textbf{SARIMA (Seasonal AutoRegressive Integrated Moving Average)} – captures linear and seasonal temperature trends.
        \item \textbf{LSTM (Long Short-Term Memory Neural Network)} – models nonlinear, long-term dependencies in time series data.
    \end{itemize}
    \item \textbf{Evaluation Metrics:} Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).
    \item \textbf{Results:}
    \begin{itemize}
        \item SARIMA --- MSE: 0.0999, RMSE: 0.3160
        \item LSTM --- MSE: 0.1089, RMSE: 0.3299
    \end{itemize}
\end{itemize}
SARIMA slightly outperformed LSTM, showing stronger ability to model seasonal temperature fluctuations.

\subsection*{Phase 2: CO\textsubscript{2}--Temperature Relationship}
\begin{itemize}
    \item \textbf{Dataset:} CO\textsubscript{2} Emissions (1960--2019) from UNFCCC and IEA via Kaggle.
    \item \textbf{Model Used:} Random Forest Regression.
    \item \textbf{Evaluation Metrics:}
    \begin{itemize}
        \item MSE: 31.3190
        \item RMSE: 5.5963
    \end{itemize}
\end{itemize}

\noindent
\textbf{Interpretation:}  
CO\textsubscript{2} emissions show a quantifiable but weak relationship with global land temperature.  
This weaker correlation may result from differences in dataset granularity (annual CO\textsubscript{2} vs. monthly temperature) and the influence of other variables such as methane, aerosols, and oceanic heat retention.

\section*{Tools and Libraries}
\begin{itemize}
    \item \textbf{Programming Language:} Python
    \item \textbf{Libraries:} Pandas, NumPy, Matplotlib, Seaborn, Statsmodels, TensorFlow/Keras, Scikit-learn
\end{itemize}

\section*{Key Findings}
\begin{itemize}
    \item SARIMA captured temperature seasonality more effectively than LSTM due to the dataset’s linear patterns.
    \item LSTM performed reasonably well but required more data and hyperparameter tuning for improved accuracy.
    \item Random Forest regression revealed that while CO\textsubscript{2} emissions influence temperature, they are not the sole factor driving climate change.
\end{itemize}

\section*{Future Work}
\begin{itemize}
    \item Incorporate additional climate factors such as methane, humidity, and ocean temperature for multivariable forecasting.
    \item Apply advanced deep learning models such as BiLSTM, GRU, or CNN-LSTM hybrids.
    \item Perform extensive hyperparameter tuning and cross-validation to enhance accuracy.
    \item Extend the study to regional-level forecasting and evaluate implications for environmental policy.
\end{itemize}

\section*{Project Structure}
\begin{lstlisting}[language=bash]
├── data/
│   ├── GlobalLandTemperature.csv
│   ├── CO2Emission.csv
│
├── notebooks/
│   ├── phase1_temperature_forecasting.ipynb
│   ├── phase2_co2_relationship.ipynb
│
├── models/
│   ├── sarima_model.pkl
│   ├── lstm_model.h5
│   ├── random_forest_model.pkl
│
├── results/
│   ├── sarima_forecast_plot.png
│   ├── lstm_forecast_plot.png
│   ├── rf_regression_plot.png
│
├── README.md
└── requirements.txt
\end{lstlisting}

\section*{Evaluation Metrics}
\begin{center}
\begin{tabular}{lcc}
\toprule
\textbf{Model} & \textbf{MSE} & \textbf{RMSE} \\
\midrule
SARIMA & 0.0999 & 0.3160 \\
LSTM & 0.1089 & 0.3299 \\
Random Forest & 31.3190 & 5.5963 \\
\bottomrule
\end{tabular}
\end{center}

\section*{Conclusion}
The project demonstrates how traditional statistical models like SARIMA can outperform deep learning models such as LSTM on seasonal datasets.  
Although CO\textsubscript{2} emissions have a measurable impact on temperature, the relationship remains weak due to the complex, multivariate nature of climate systems.  
This study contributes to understanding climate forecasting and shows how machine learning methods can be applied effectively in environmental data analysis.

\section*{Contact}
\textbf{Author:} Hassan Zeb \\
\textbf{Email:} --- \\
\textbf{Location:} London, United Kingdom

\end{document}
