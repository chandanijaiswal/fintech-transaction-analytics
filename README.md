# Fintech Transaction Analytics

Analysis of 5,000 digital payment transactions to find payment failure and fraud patterns.

## Business questions
1. How are failure rates different across payment methods?
2. When does fraud happen?
3. Which categories bring the most transaction volume?
4. How does volume change month by month?

## Tools
Python, pandas, NumPy, Matplotlib, Jupyter Notebook

## Data
Synthetic dataset (created for practice, not real customer data):
- 5,025 raw transactions (5,000 after removing 25 duplicates)
- 800 customers, 12 months, amounts in INR
- Added on purpose: 60 missing device values, 40 missing category values and 25 duplicate rows

## What I did
1. Loaded and explored the data (shape, info, describe, value counts)
2. Cleaned the data: removed duplicates, filled missing values, converted timestamp to datetime
3. Created new columns: month, hour, failed
4. Calculated KPIs
5. Made charts and wrote insights

## Key numbers
- Success rate: 94.36%
- Successful volume: INR 15,364,720.78
- Average ticket size: INR 3,256.62
- Fraud rate: 1.21% of successful transactions

## Key insights
- Net Banking has the highest failure rate (7.92%), about 2.6 times higher than Debit Card (3.01%).
- Late-night transactions (midnight to 5 AM) have a fraud rate of 4.88%, about 5.5 times higher than the rest of the day (0.88%).
- The first and last months have partial data, so the monthly trend uses full months only. Volume rises over this period.

## Recommendations
- Improve the reliability of the Net Banking payment flow and suggest UPI as a backup option when a payment fails.
- Add extra verification (OTP or a transaction limit) for late-night payments.

## Charts
See the `outputs` folder: failure by payment method, fraud by hour, monthly volume, category volume.

## Files
- `Fintech_Analysis.ipynb` : the full analysis
- `data/` : raw and cleaned data
- `outputs/` : saved charts