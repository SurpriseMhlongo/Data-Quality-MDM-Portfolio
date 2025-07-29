# Wildfire Analysis Visualisation Guide (TO BE UPDATED, AS CODE CHANGED)
##### by Surprise Mhlongo - 27/07/2025
## Plot Order & Interpretation

### 2. Weather Distributions Plot 
<img width="706" height="493" alt="image" src="https://github.com/user-attachments/assets/0d6948a7-7829-4e01-909f-811105d9ce00" />
  
How to Read:
- Four histograms (Temperature, RH, Ws, Rain)
- X-axis: Measurement ranges
- Y-axis: Frequency of occurrences
- Shape:
  - Narrow = Consistent values
  - Wide = Variable conditions

### 3. Fire Indices Heatmap
<img width="584" height="487" alt="image" src="https://github.com/user-attachments/assets/c18ed287-b697-45df-9228-d136b78f06f5" />
  
How to Read:
- Matrix showing relationships between:
  - FFMC, DMC, DC, ISI, BUI, FWI
- Color Key:
  - +1.0 (Red): Perfect positive correlation
  - 0 (White): No relationship
  - -1.0 (Blue): Inverse relationship

### 4. Risk Classification Plot
<img width="701" height="388" alt="image" src="https://github.com/user-attachments/assets/8642534b-30b4-466b-adc4-849ad78d218e" />
 
How to Read:
- X-axis: FWI (Fire Weather Index)
- Y-axis: ISI (Initial Spread Index)
- Colored clusters:
  - Green: Low risk
  - Yellow: Moderate
  - Orange: High
  - Red: Extreme
- Dotted lines: Official danger thresholds

### 5. Feature Importance Plot
<img width="596" height="294" alt="image" src="https://github.com/user-attachments/assets/b161c032-2601-466d-a6f9-610a96a41fdd" />
 
How to Read:
- Bars show predictive power:
  - Longer = More important
- Percentage values: Exact contribution
- Top predictors listed left-to-right

### Prediction Results
<img width="525" height="483" alt="image" src="https://github.com/user-attachments/assets/b910d17e-9e60-444a-93bf-7fa553fdaa0e" />

## Data Notes
- All plots generated from `FireData_Cleaned.csv`
- Raw data available in `/data` folder
- See notebook for exact generation code

## Explore the project:##  
📊 [Kaggle Notebook](https://www.kaggle.com/code/surprisemhlongo/data-quality-mdm-portfolio/) (Interactive Analysis)  
