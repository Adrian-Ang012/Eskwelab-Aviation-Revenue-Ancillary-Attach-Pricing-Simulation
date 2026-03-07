# Eskwelab-Aviation-Revenue-Ancillary-Attach-Pricing-Simulation

✈️ Aviation Revenue & Ancillary Pricing Simulation
This repository contains a high-fidelity synthetic data engine designed for Revenue Management and Ancillary Product Analysis. By simulating passenger decision-making based on economic "first principles," this project allows analysts to test pricing strategies, model consumer behavior, and perform feature importance analysis without the constraints of PII or limited real-world datasets.

🏗️ Project Architecture
The project is divided into two decoupled modules to ensure scalability and reproducibility:

The Generation Engine (ESKWELAB.ipynb): A class-based Python simulation that generates synthetic booking, offer, and conversion logs. It embeds causal behaviors such as the "Elena Ceiling" (price sensitivity cliffs) and "Basket Reinforcement" (sequential purchase priming).

The Analytical Showcase (Showcase_Analysis.ipynb): A self-contained notebook designed for EDA and ML validation. It consumes the output of the generator to perform revenue optimization and predictive modeling.

📊 Data Dictionary
The simulation produces three relational tables:

dim_bookings: Passenger context (Segment, Channel, Fare, Days to Departure).

fact_offers: Ancillary offer details (Type, Price, Display Rank, Inventory).

fact_conversions: Binary purchase outcomes and decision timestamps.

🚀 How to Run
Generate Data: Open ESKWELAB.ipynb and run the simulation engine to generate the CSV datasets.

Analyze: Open Showcase_Analysis.ipynb. This notebook will automatically ingest the generated CSV files.

Explore: Follow the "Analytical Playground" (Chapter 2) to visualize demand curves, and "Predictive Modeling" (Chapter 3) to test your own pricing hypotheses.
