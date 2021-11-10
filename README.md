# :dollar: Dollar Costs
---
Calculate how much return you might be forgoing by purchasing something now rather than putting that money into an account, including many factors such as:
* Inflation
* Time-discounting
* Compounding period (up to daily)
* Consumption frequency: Ongoing consumption (ie a coffee every day) vs lump sum consumption (ie buying a coffee maker)
* Time until retirement or divestment
One parameter that's missing is how much you value the thing you're buying. That's because it's up to you to figure out if the benefit you get is greater than the opportunity cost you forgo.

## User Input
* Present dollar value of unit of consumption (may be omitted)
* Consumption frequency 
  * (this can be linear, as in units are consumed at a steady rate, or geometric, which means units are consumed at an increasing or decreasing rate)
* Type of output: lost return in terms of (present-day) dollars or the original unit
* Time-discounting factor
* Time until retirement or divestment
* *Risk-avoidance*

A few typical settings are included to guide inputs

## Investments
An investment is stored with many different parameters:
* Compounding frequency
* Notes (ex: Roth IRA accounts have a certain fixed value you can add to them annually, but these limtis are not accounted for)
* Average/Projected annual return
* Whether return is inflation indexed (note: the inflation indexing is taken at face value, but may be inconsistent with inflation adjustment elsewhere)
* *Risk (beta is used, and is relative to the market, unless otherwise noted)*

## Data Sources
* St. Louis Federal Reserve's [FRED](https://fred.stlouisfed.org/docs/api/fred/fred.html)

## Potential Features
### Prediction versus Reality
* Measuring the real value of the type of investment

> Note: *italics indicated features to be added later*

---
# Documentation
## Structure
* `.json` files are used to store enumerations of fields, investment data, and typical settings
* `.ts` files in src
  * You can build them using `tsc` (see [TypeScript tooling](https://www.typescriptlang.org/docs/handbook/typescript-tooling-in-5-minutes.html) for details); once they are built to JS file(s), they should automatically be placed in the `built` directory, which you can run
