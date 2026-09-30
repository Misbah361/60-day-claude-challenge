Key Learnings – Day 17: E85 Vehicle Cost Dashboard

1. Cheaper at the pump doesn't mean cheaper to run (the E85 paradox).

E85 is about 18% cheaper per litre than Petrol (₹82 vs ₹100).
Its running cost is still about 3.6% higher per km (₹6.37 vs ₹6.15).
The reason is mileage. E85 averages about 12.9 km/L against about 16.3 km/L for Petrol.
E85 would break even with Petrol at about ₹79/L, so it needs to be a little cheaper than the current ₹82.

2. Cost per km ranking (lowest to highest): EV ₹1.75, CNG ₹3.33, Diesel ₹4.67, Petrol ₹6.15, E85 ₹6.37.

3. E85 has the lowest emissions of the liquid fuels.

E85 emits about 0.070 kg CO₂/km, the lowest of all five fuels.
EV is next at 0.091.
Diesel (0.179) and Petrol (0.171) are the highest.

4. Maintenance cost per km.

EV is lowest at ₹0.23.
E85 (₹0.46) and Petrol (₹0.47) are nearly the same.
Diesel is highest at ₹1.01.

5. Refuelling time is a trade-off. EV recharging takes about 45 minutes, against 5 to 8 minutes for the other fuels.

6. Prompt and data skills.

A structured prompt (role, formulas, layout rules and output format) produced a working dashboard in one pass.
Fuel names in the raw data were messy, for example "Petrol (E20)" and "E85 (Flex-Fuel)". They had to be cleaned before grouping.
Each fuel has only 9 to 11 records, so these averages are indicative rather than statistically strong.
The CSV has no vehicle-model column, so the Kia Seltos details only affect the header, not the numbers.

7. Technical takeaways. I built the charts as pure SVG, with no external libraries, and the layout is responsive from 375px to 1440px.
