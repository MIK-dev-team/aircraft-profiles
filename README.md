# aircraft-profiles

This repository contains aircraft profiles for Malmi Aviation Club aircraft.
Currently supported applications are:

- Skydemon (.aircraft)

## SkyDemon profiles

| File                                                    | Aircraft | Flight rules | Wheel fairings |
|---------------------------------------------------------|----------|--------------|----------------|
| `Diamond DA40 NG (VFR) (OH-STL).aircraft`               | OH-STL   | VFR          | Fitted         |
| `Diamond DA40 NG (IFR) (OH-STL).aircraft`               | OH-STL   | IFR          | Fitted         |
| `Diamond DA40 NG (VFR) (no fairings) (OH-STL).aircraft` | OH-STL   | VFR          | Removed        |
| `Diamond DA40 NG (IFR) (no fairings) (OH-STL).aircraft` | OH-STL   | IFR          | Removed        |
| `Diamond DV20 (OH-IHQ) (no fairings).aircraft`          | OH-IHQ   | VFR          | Removed        |

Pick the profile that matches the flight rules you're flying under and whether the aircraft currently has its wheel fairings fitted.

### VFR and IFR

The VFR and IFR profiles are otherwise identical. The only difference is the final reserve fuel: 30 minutes for VFR and 45 minutes for IFR.

### No fairings

Without wheel fairings the aircraft is slower and climbs less well, so the "no fairings" profiles have:

- cruise airspeeds reduced by 4%
- climb rates reduced by 40 ft/min
- a lower glide ratio (OH-STL: 9.4 instead of 9.7)

OH-IHQ only has a "no fairings" profile.

### Units

Fuel values in the `.aircraft` files are stored in litres even when the profile displays fuel in US gallons (OH-STL). For example, `TaxiFuel="3.785412"` is 1 US gal. Don't convert these values by hand; edit them in SkyDemon and export the profile instead.
