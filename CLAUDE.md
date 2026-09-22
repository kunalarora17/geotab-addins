# geotab-addins

MyGeotab custom page Add-Ins hosted on GitHub Pages at https://kunalarora17.github.io/geotab-addins/

## Add-Ins

### walmart-gph-utilization
- **URL:** https://kunalarora17.github.io/geotab-addins/walmart-gph-utilization/
- **Purpose:** Combined GPH (Gallons Per Hour), HPG (Hours Per Gallon), and asset utilization report
- **Granularity:** One row per asset per day
- **Formulas:**
  - Engine ON Hours = Driving Hours + Idling Hours
  - GPH = Fuel (gal) / Engine ON Hours
  - HPG = Engine ON Hours / Fuel (gal)
  - Utilization = Driving Hours / 21.7 (Walmart threshold)
- **API calls:** `Trip` (distance, drivingDuration, idlingDuration) + `FuelUsed` (totalFuelUsed in liters)
- **Units:** Miles, Gallons (converted from km/liters in API)
- **Database:** Generic (any MyGeotab database)

### knx-hos-tracker
- **URL:** https://kunalarora17.github.io/geotab-addins/knx-hos-tracker/
- **Purpose:** Driver HOS hours remaining on 70-hr/8-day ruleset
- **API calls:** `User` (driver search) + `DutyStatusAvailability` (remaining hours + daily recap)
- **Database:** Generic (any MyGeotab database with HOS enabled)

## Registering in MyGeotab
Administration > System > System Settings > Add-Ins > + Add
Paste the contents of the relevant `config.json` file.

## GitHub Pages
Hosted from the `main` branch root directory.
To update: push changes to main — Pages rebuilds automatically.
