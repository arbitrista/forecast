## Dominican Growth Projections

Todo

- Use python,
- Take past growth rates,
- Look at growth rates by  sector,
- ….

### Growth Projections

- **Compound Annual Growth Rate (CAGR)** provides a smoothed growth rate from the beginning to the end of a period, assuming a consistent rate each year.
- **Scenario Analysis**:  Develop different scenarios (e.g., optimistic, pessimistic, and baseline) based on assumptions about key drivers of growth (e.g., economic policies, technological advances).
- **Industry or Sector Analysis (Growth Factors)**:   Compare growth projections with industry benchmarks or sector trends. Many sectors have well-researched growth rates based on historical data and forecasts.
    - Use Economic Complexity
    - …
- More advanced methods include using econometric models (e.g., panel data regression) or machine learning algorithms (e.g., XGBoost, Random Forests) that consider multiple factors affecting growth.

```python
import pandas as pd

# Function to calculate growth model
def growth_model(initial_income, growth_rate, years):
    # Create an empty list to store results
    results = []
    
    # Calculate income for each year
    for year in range(1, years + 1):
        income = initial_income * (1 + growth_rate / 100) ** year
        results.append({"Year": year, "Income per Capita": income})
    
    # Convert results to a DataFrame
    df = pd.DataFrame(results)
    return df

# Parameters
initial_income = 12000      # Starting per capita income
growth_rate = 5             # Growth rate in percentage
years = 11                  # Number of years

# Generate growth model
growth_df = growth_model(initial_income, growth_rate, years)
print(growth_df)
```

References

- https://www.worldbank.org/en/research/brief/LTGM
- Tkacz, G. (2001). Neural network forecasting of Canadian GDP growth. International Journal of Forecasting, 17(1), 57-69.
- DeJong, D. N., Liesenfeld, R., & Richard, J. F. (2005). A nonlinear forecasting model of GDP growth. Review of Economics and Statistics, 87(4), 697-708.
- https://www.conference-board.org/publications/how-to-forecast-GDP-in-the-long-run
- …
