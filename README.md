🚗 Dynamic Pricing for Urban Parking Lots

Capstone Project – Summer Analytics 2025
Developed using: Python, NumPy, Pandas, Bokeh

📌 Overview

Urban parking is a scarce and dynamic resource. Static pricing results in overcrowding or underutilization of lots. This project introduces a dynamic pricing engine that adjusts parking prices in real-time based on demand, traffic, vehicle type, special events, and competitor pricing. It simulates 14 parking lots over 73 days with data captured at 30-minute intervals.

🧰 Tech Stack

Component	Technology
Language	Python
Data Handling	Pandas, NumPy
Visualization	Bokeh
Environment	Google Colab
📊 Architecture Diagram (Mermaid)

flowchart TD
A[Input CSV: dataset.csv] --> B[Real-Time Data Ingestion]
B --> C[Pricing Engine]
C --> C1[Model 1: Linear Pricing]
C --> C2[Model 2: Demand-Based Pricing]
C --> C3[Model 3: Competitive Pricing]
C --> D[Streaming Output]
D --> E[Bokeh Dashboard]

🧠 Project Structure

📦 dynamic-parking-pricing
├── main.ipynb            # Jupyter Notebook with complete code
├── report.pdf            # Explanation of models and logic
├── dataset.csv           # Provided dataset for 14 lots over 73 days
├── README.md             # Project summary and setup
📈 Model Details

✅ Model 1 – Linear Pricing
Adjusts price linearly based on occupancy.
price = previous_price + α × (occupancy / capacity)
✅ Model 2 – Demand-Based Pricing
Uses a demand function:
demand = α * (occupancy / capacity) + β * queue - γ * traffic + δ * special + ε_vehicle_weight
Final price:
price = BasePrice × (1 + λ × normalized_demand)
✅ Model 3 – Competitive Pricing
Uses Haversine formula to find nearby lots within 1km.
Price is adjusted based on nearby competitor prices and local lot status.
Optional rerouting suggestion logic included.
⚙️ Key Assumptions

Base price = $10
Price bounds: $5 to $20
Vehicle weights:
car = 1.0, bike = 0.5, truck = 1.5
Competitors within 1 km are considered
🖥️ How to Run

Open the notebook main.ipynb in Google Colab.
Upload dataset.csv to the Colab file system.
Run all cells to simulate real-time pricing and visualizations.
Output: Interactive plots showing dynamic prices for each lot using Bokeh.
📎 Report

A full project report explaining each model, demand function, and visualization output is available in report.pdf.

👥 Contributors

Harsh Gupta (or your full team name)
📬 Contact

For questions or access issues, open an issue or contact via email.

📄 License

This project is part of the Summer Analytics 2025 program and is shared for educational purposes only.

