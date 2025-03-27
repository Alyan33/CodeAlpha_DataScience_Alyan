# CodeAlpha_DataScience_Alyan

## **📈 Stock Price Prediction Using LSTM**
This project implements a **Long Short-Term Memory (LSTM)** neural network to predict stock prices using historical stock market data. The model learns patterns from past stock prices and predicts future trends.

## **📌 Features**
✔ Load stock market data from a **CSV file**  
✔ **Fix date format issues** and preprocess data  
✔ **Normalize data** for better training  
✔ **Train an LSTM model** for time-series forecasting  
✔ **Predict and visualize stock prices**  

---

## **📂 Dataset**
- The dataset should be a **CSV file** containing stock price data.  
- The dataset **must include a 'Date' column** and a target column (e.g., 'Close' price).  
- Ensure the 'Date' format is **DD/MM/YYYY**.  

### **📌 Example Dataset Format**
| Date       | Open  | High  | Low   | Close | Volume  |
|------------|-------|-------|-------|-------|---------|
| 13/02/2018 | 120.5 | 122.3 | 118.8 | 121.1 | 1500000 |
| 14/02/2018 | 121.1 | 124.0 | 120.5 | 123.5 | 1300000 |

## **🔧 Installation**
### **1️⃣ Install Required Libraries**
```bash
pip install pandas numpy matplotlib tensorflow scikit-learn
```
### **2️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/stock-price-prediction-lstm.git
cd stock-price-prediction-lstm
```
### **3️⃣ Add Your CSV File**
Place your dataset (`your_file.csv`) in the project folder.

## **🚀 Usage**
### **Run the Jupyter Notebook**
```bash
jupyter notebook
```
Open `stock_prediction.ipynb` and execute the cells.

## **📜 Code Explanation**
### **1️⃣ Load Data**
- Reads stock data from `your_file.csv`.
- Converts the 'Date' column to a **datetime format**.

### **2️⃣ Preprocess Data**
- Extracts **'Close' prices** for training.
- **Scales the data** using `MinMaxScaler`.

### **3️⃣ Create LSTM Model**
- Uses **past 60 days of data** to predict the next day’s stock price.
- LSTM architecture:
  - **2 LSTM layers** (50 units each)
  - **Dropout layers** (to prevent overfitting)
  - **Dense layers** for output.

### **4️⃣ Train the Model**
- **Runs for 20 epochs** (can be increased for better accuracy).
- Uses `adam` optimizer and `mean_squared_error` loss function.

### **5️⃣ Predict & Plot Results**
- Converts predicted values back to original scale.
- **Plots actual vs. predicted prices**.

## **📊 Visualization**
The model outputs a graph comparing **actual stock prices** with **predicted values**:

![Stock Prediction Graph](https://your-image-url.com/graph.png)


## **📌 Where to Get Stock Data?**
You can get stock market datasets from:
- [Yahoo Finance](https://finance.yahoo.com/)
- [Alpha Vantage](https://www.alphavantage.co/)
- [Quandl](https://www.quandl.com/)
- Your own stock CSV file.

## **🔮 Future Improvements**
✅ Increase **training epochs** for better accuracy.  
✅ Tune **hyperparameters** (LSTM units, batch size).  
✅ Use **real-time stock data** from APIs.  

---

## **🤝 Contributing**
Feel free to contribute! Fork this repository, improve the code, and submit a **Pull Request**.  

## **📜 License**
This project is licensed under the **MIT License**. 
