# megaline-plan-reccomendation
Machine learning classification project to recommend Megaline's Smart or Ultra plan.
# Megaline Plan Recommendation Model

## Project Overview
This project predicts whether a Megaline customer should be recommended the **Smart** or **Ultra** plan based on usage data.

## Dataset
Source: `datasets/users_behavior.csv`  
Features: calls, minutes, messages, mb_used  
Target: is_ultra (0 = Smart, 1 = Ultra)

## Results
- Best Model: Random Forest (max_depth=8, n_estimators=10)
- Validation Accuracy: 83.2%
- Test Accuracy: 81.5%
- Baseline Accuracy: 69.3%
