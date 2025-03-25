# E-commerce Customer Behavior Analysis

## Project Overview
This repository contains a comprehensive set of Python scripts for analyzing online shopping behavior and predicting purchase intentions. The project uses machine learning techniques to analyze patterns in e-commerce user data to optimize sales strategies and improve conversion rates.

## Dataset
The project is designed to work with the "Online Shoppers Intention" dataset (not included in the repository). To use this code, you need to:
1. Place the `online_shoppers_intention.csv` file in the `data/` directory
2. The dataset should contain visitor behavior features including:
   - Page visits (Administrative, Informational, Product Related)
   - Page durations
   - Bounce rates
   - Exit rates
   - Special day information
   - Visitor type (New/Returning)
   - Weekend flag
   - Month information

## Project Structure
- `main.py`: Entry point for running the complete analysis pipeline
- `data_analysis.py`: Exploratory data analysis and visualization tools
- `customer_purchase_analysis.py`: Detailed analysis of customer segments and purchase patterns
- `SalesOptimizationAnalyzer.py`: Basic sales optimization analysis
- `EnhancedSalesOptimizationAnalyzer.py`: Advanced sales analysis with ROI metrics and competitor benchmarking
- `lstm_model.py`: Deep learning model (LSTM) for purchase prediction
- `requirements.txt`: Required Python packages

## Features
This codebase provides the following capabilities:

### Data Analysis
- Exploratory data analysis with comprehensive visualizations
- Statistical analysis of customer behavior patterns
- Correlation analysis between behaviors and conversion rates
- Seasonal trend identification

### Customer Segmentation
- Visitor type analysis (New vs Returning)
- Time-based segmentation (Weekend vs Weekday)
- Special day impact analysis
- Custom feature engineering for customer behavior patterns

### Sales Optimization
- ROI metrics calculation
- Seasonal trend analysis
- Competitive benchmarking
- Cost-benefit analysis for optimization strategies

### Predictive Modeling
- LSTM-based deep learning model for purchase prediction
- Model evaluation with comprehensive metrics
- Performance visualization and analysis

## How to Use

### Prerequisites
Install the required packages:
```bash
pip install -r requirements.txt
```

### Running the Analysis
```bash
python main.py
```
This will:
1. Load and analyze the dataset
2. Generate visualizations of key patterns
3. Train and evaluate the LSTM model
4. Display optimization recommendations

### Individual Component Usage

#### Data Analysis
```python
from data_analysis import load_and_analyze_data
df = load_and_analyze_data('data/online_shoppers_intention.csv')
```

#### Customer Segmentation
```python
from customer_purchase_analysis import preprocess_data, analyze_customer_segments
df_processed, month_encoder, visitor_encoder = preprocess_data(df)
segment_analysis = analyze_customer_segments(df_processed, visitor_encoder)
```

#### Sales Optimization
```python
from EnhancedSalesOptimizationAnalyzer import EnhancedSalesOptimizationAnalyzer
analyzer = EnhancedSalesOptimizationAnalyzer(df)
recommendations = analyzer.generate_enhanced_recommendations()
```

#### Predictive Modeling
```python
from lstm_model import train_lstm_model
model = train_lstm_model('data/online_shoppers_intention.csv')
```

## Key Insights and Recommendations

The analysis pipeline generates several types of recommendations:
1. **Immediate actions**: Short-term optimization opportunities with high ROI
2. **Strategic initiatives**: Longer-term structural improvements
3. **Seasonal preparations**: Time-specific optimization strategies
4. **Competitive responses**: Positioning against industry benchmarks

## Advanced Analytics
The repository includes several advanced analytics capabilities:
- Time-based conversion rate analysis
- Special day impact quantification
- Deep customer segmentation with ROI metrics
- Purchase condition analysis for different customer types

## Model Performance
The LSTM model provides:
- Binary classification for purchase prediction
- Classification metrics (precision, recall, F1-score)
- Confusion matrix visualization
- Performance comparison across customer segments

## Contributing
Feel free to submit issues or pull requests to improve the analysis pipeline or add new features.
