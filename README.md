# Worldometers daily data


## Apps using this data (sorted by easy accessibility)

#### Web Apps
1. [coronavirus.davidb.dev](https://coronavirus.davidb.dev) - The most complete covid-19 live dashboard with predictions
2. [covid-2019 stats](https://observablehq.com/@phantomydn/covid-2019-stats-country-state-selection) - Covid-19 Stats js notebook


#### Apps
1.  [covid](https://github.com/jsidew/covid#) - Outbreak controlling status in the world



If you have your application built on top of this data, please make PR and add it to the list


## Foreword

Recently (from 23 March) [CSSEGISandData/COVID-19](https://github.com/CSSEGISandData/COVID-19) stopped supplementing recovered data for covid-19.  This was the final issue which motivated me to let this repo go and started my own data repository building.

Recovery information is very important, because we can calculate active cases based on it and  check progress of disease in the world.


## How

Data will just come from Worldometers and it will be updated every day

## Automation
Becase, I did not want to do this manually, I wrote a small js notebook, which scrapes worldometer page and merges that data with already existing data


https://observablehq.com/d/c99a630b3931dfbc

So we will just need to copy that merged data and paste to this csv file

## Challenges

Because worldometer does not provide data on county and state level, I had to spread that data proportionally across US states and counties , summing them up  will produce right number country wide (After rounding )


## Other modifications
I just recently realised, they no longer would be updating the data for recovered dataset, so I had to manually edit data to and had to fixe irregularities for those time ranges (23 March specifically)

I also modified some country names (left side names changed to right side names)
```javascript
nameStandards = ({
 "Mainland China":"China",
  
 "US":"USA",
 "United States":"USA",
  
 "United Kingdom":"UK",
 "England":"UK",
  

 "Others":"Diamond Princess",
 "Cruise Ship":"Diamond Princess",
  
 "Czechia":"Czech Republic",
 "United Arab Emirates":"UAE",
 "Iran (Islamic Republic of)":"Iran",
 "Hong Kong SAR":"Hong Kong",

 "Viet Nam":"Vietnam",
 "occupied Palestinian territory":"Palestine",
 "Macao SAR":"Macao",
 "Russian Federation":"Russia",
 "Republic of Moldova":"Moldova",
 "Macedonia":"North Macedonia",
 "Republic of Serbia":"Serbia",
 "Saint Vincent and the Grenadines": "St. Vincent Grenadines",
 "Ivory Coast":"Cote d'Ivoire",
 "Saint Barthelemy":"St. Barth",
 "Faroe Islands": "Faeroe Islands",
 "Faeroe Islands": "Faeroe Islands",
 "Réunion":"Reunion",
 "The Gambia":"Gambia",
   "Central African Republic":"CAR",
  "Curacao":"Curaçao",
  "Curaçao":"Curaçao",
  "Jersey":"Channel Islands",
  "Guernsey":"Channel Islands",
  "East Timor":"Timor-Leste",

  
 "Republic of Korea":"South Korea",
 "S. Korea":"South Korea",
 "Korea, South":"South Korea",
  "United Republic of Tanzania":"Tanzania",
  

  
 "Holy See":"Vatican City",
 "Vatican":"Vatican City",
 "Holy See (Vatican City State)":"Vatican City",
  


  "Taiwan*":"Taiwan",
   "Taipei and environs":"Taiwan",

  
  "Democratic Republic of Congo":"Congo",
  "Congo (Kinshasa)":"Congo",
  "DRC":"Congo",
  "The Democratic Republic of Congo":"Congo",
  "Democratic Republic of the Congo":"Congo",
  
  "Congo (Brazzaville)":"Congo (Brazzaville)",
  

  "The Bahamas":"Bahamas", 
  "Bahamas, The":"Bahamas",
  
  "Gambia, The":"Gambia",
  
  
})
```

## Lack of 
Some small countries may be lacking, I plan to identify and add them into dataset

## Contribution
They are welcome, but I doubt there will be need for this. One area which we can improve, is to standartize country names using ISO country codes

