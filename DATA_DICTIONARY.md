# 📋 Data Dictionary — Car Price Dataset

This file describes every column in `data/CarPrice_Assignment.csv`.

| # | Column | Type | Description |
|---|--------|------|-------------|
| 1 | `car_ID` | int | Unique identifier for each car |
| 2 | `symboling` | int | Insurance risk rating (-3 to +3). +3 = risky, -3 = safe |
| 3 | `CarName` | str | Company name and car model (e.g., "toyota corolla") |
| 4 | `fueltype` | str | Fuel type: `gas` or `diesel` |
| 5 | `aspiration` | str | Aspiration type: `std` (standard) or `turbo` |
| 6 | `doornumber` | str | Number of doors: `two` or `four` |
| 7 | `carbody` | str | Body style: `convertible`, `hatchback`, `sedan`, `wagon`, `hardtop` |
| 8 | `drivewheel` | str | Drive wheel type: `fwd`, `rwd`, `4wd` |
| 9 | `enginelocation` | str | Engine location: `front` or `rear` |
| 10 | `wheelbase` | float | Distance between front and rear axles (inches) |
| 11 | `carlength` | float | Length of car (inches) |
| 12 | `carwidth` | float | Width of car (inches) |
| 13 | `carheight` | float | Height of car (inches) |
| 14 | `curbweight` | int | Weight of car without passengers/cargo (lbs) |
| 15 | `enginetype` | str | Engine type: `dohc`, `ohc`, `ohcv`, `ohcf`, `l`, `rotor` |
| 16 | `cylindernumber` | str | Number of cylinders: `two` through `twelve` |
| 17 | `enginesize` | int | Size of engine (cubic inches) |
| 18 | `fuelsystem` | str | Fuel system: `mpfi`, `2bbl`, `idi`, `1bbl`, `spdi`, `4bbl`, `mfi`, `spfi` |
| 19 | `boreratio` | float | Bore ratio of the engine |
| 20 | `stroke` | float | Stroke length of the engine |
| 21 | `compressionratio` | float | Compression ratio of the engine |
| 22 | `horsepower` | int | Engine horsepower |
| 23 | `peakrpm` | int | Peak revolutions per minute |
| 24 | `citympg` | int | Mileage in city (miles per gallon) |
| 25 | `highwaympg` | int | Mileage on highway (miles per gallon) |
| 26 | `price` | float | **Target variable** — Price of the car (USD) |

## Notes

- `CarName` contains both the brand and model separated by a space. The brand name may have inconsistent spellings (e.g., "maxda" instead of "mazda").
- `symboling` is an actuarial risk rating: cars are initially assigned a risk factor based on their price, then adjusted up or down.
- Numeric features like `horsepower`, `enginesize`, and `curbweight` tend to have the strongest correlation with `price`.
