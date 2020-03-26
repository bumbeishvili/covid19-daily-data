# worldometers-daily-data



## Foreword

Recently [CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19) stopped supplementing recovered data for covid-19.  This was the last issue which motivated me to let this repo go and started my own data repository building.

Recovery information is very important, because we can calculate active cases based on it and  check progress of disease in the world.


## How

Data will just come from Worldometers and it will be updated every day

## Automation
Becase, I did not want to do this manually, I wrote a small js notebook, which scrapes worldometer page and merges that data with already existing data


https://observablehq.com/d/c99a630b3931dfbc

So we will just need to copy that merged data and paste to this csv file

## Challenges

Because worldometer does not provide data on county and state level, I had to spread that data proportionally across US states and counties , summing them up  will produce right number country wide (After rounding )

