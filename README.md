# Module11
**Required Assignment 11.1: What Drives the Price of a Car?**


**In this application,required to explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. goal is to understand what factors make a car more or less expensive.  As a result of analysis provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.**

From a business perspective, identifying features in used which impact prices. Customer preferences and needs , before makeing the inventory for new customers.  Using a few sentences. 

**Data type understanding for Model uses**

Provided attribute for car feathers as below provide by business to analyse the data for customer needs.

*Price :	The current market value or asking price of the vehicle in its current state.	Primary target variable for prediction.
*Year :	The calendar year the vehicle was manufactured.	Directly impacts depreciation; older cars usually cost less.
*Model :	The specific name of the vehicle line (e.g., Camry, F-150).	Defines the specific features, size, and luxury level.
*Condition :	The physical and mechanical state of the car (New, Excellent, Good, Fair, Salvage).	A major "weight" in pricing; poor condition overrides low mileage.
*Cylinders :	The number of combustion chambers in the engine (e.g., 4, 6, 8 cylinders).	High correlation with horsepower and fuel consumption
*Fuel :	The energy source used (Gas, Diesel, Hybrid, Electric).	Affects long-term running costs and environmental appeal.
*Odometer :	The total distance the vehicle has traveled (mileage).	Higher mileage generally indicates more wear and lower value.
*Title Status :	The legal status of the vehicle's ownership document (e.g., Clean, Salvage, Rebuilt, Lien).	A "Clean" title is worth significantly more. "Salvage" or "Rebuilt" indicates the car was previously declared a total loss.
*Transmission:	The mechanism that transmits power from the engine to the wheels (Manual, Automatic, Semi-auto).	Affects driving ease and fuel efficiency. Automatic is standard in most regions, while Manual is often preferred for sports cars.
*VIN	(Vehicle Identification Number) : A unique 17-character code that acts as the car's "fingerprint" or DNA.	Used to track the car's history, accidents, recalls, and registrations.
*Drive :	The drivetrain system that receives power from the engine (FWD, RWD, 4WD/AWD).	Determines how the car handles in snow, mud, or high-speed cornering.
*Size :	The physical dimensions or classification category (Compact, Mid-size, Full-size).	Dictates cabin space, parking ease, and overall footprint.
*Type :	The body style of the vehicle (SUV, Sedan, Pickup, Coupe, Hatchback, Convertible).	This is usually the first filter a buyer uses based on their lifestyle needs.
*Paint Color	The exterior color of the vehicle.	While subjective, neutral colors (White, Black, Silver) tend to have higher resale value than "loud" colors.
*State	The geographic location (US State) where the car is listed or registered.	Impacts price due to local demand, taxes, and environmental factors (e.g., cars from "Salt Belt" states may have more rust).



Since many of your attributes are marked as (object), to perform Categorical Encoding (like One-Hot Encoding or Label Encoding) if you plan to use this data in a machine learning model, as algorithms require numerical input.

1. Defining a High-Quality ModelA model in this industry is considered "high quality" not just if it has a high score, but if its errors are predictable and manageable for a buyer.Accuracy:
2.Our final model achieved an $R^2$ of 0.73-0.79, meaning it captures the vast majority of factors influencing car prices.
3.The "Error" Margin: The **Median Absolute Error** is approximately $2,847. This means that for half of the cars in the market, our model's prediction is within $2,800 of the actual price a very useful range for setting initial auction 4.bids.Consistency: Through cross-validation, proved that these drivers (Year, Odometer, Type) are consistent across different samples of data, ensuring the model isn't just "memorizing" specific listings.
5.Meaningful Insights: What Consumers Value The model reveals a clear hierarchy of value in the used car
6.market:Predictability of Family Vehicles: The model is most accurate at pricing Minivans, Sedans, and Wagons (lowest error rates).
7.These are "commodity" vehicles where price is strictly driven by age and mileage. Consumers in this segment value reliability and value-for-money.
8.The "Truck" Variance: Trucks and Pickups show higher *MAE* margins (approx. $5,400).
9.The Depreciation Curve: We learned that the relationship between price and age is non-linear. A vehicle loses value rapidly in its first 3–5 years, but the "floor" for a functional, clean-title vehicle remains relatively high regardless of  age, provided it falls into the "Truck" or "SUV" categories.
10 This suggests that for these vehicles, "hidden" factors not in our data—such as towing packages, aftermarket modifications, or specific engine conditions—drastically shift the price.
 Consumers here value utility and specialized features.
11.Reflection: Revisitation vs. ValueDoes the process need adjustment?While our model provides excellent general guidance, the Residual Analysis (visualized below) shows that as car prices increase (above $50,000), the model’s predictions become less precise. This is the "Luxury/Specialty Gap."Recommendation for Revisitation: If the dealership intends to move into the high-end luxury or classic car market, we would need to revisit the "Data Preparation" phase to include more granular details like specific trim levels, "Model" names (which we previously excluded for speed), and perhaps regional economic data.Immediate Value: For the standard inventory (cars under $40,000), the current model is ready for use. It provides a robust "baseline price" that your team can use to identify undervalued trade-ins or overpriced auction listings.Final Summary for the ClientYou now have a data-driven framework that identifies Year, Odometer, and Vehicle Type (Trucks/Pickups) as your primary profit drivers. By focusing your inventory on diesel-powered trucks and newer SUVs, and using our model to set "ceiling" prices for family sedans, you can minimize the risk of overpaying at auctions and maximize your turnaround on the lot.

6. <img width="395" height="298" alt="image" src="https://github.com/user-attachments/assets/30e10774-f973-4cc1-8221-ff616645a0c3" />
