# AeroCalc — Airspeed Converter

A single-page web application for converting between aviation airspeed types using the ICAO ISA (International Standard Atmosphere) model.

## What It Does

AeroCalc converts between the four primary aviation airspeed definitions at any altitude:

| Speed Type | Description |
|---|---|
| **CAS** | Calibrated Airspeed — pitot-tube reading corrected for instrument error |
| **TAS** | True Airspeed — actual speed relative to the surrounding air mass |
| **EAS** | Equivalent Airspeed — speed producing equal dynamic pressure at sea level |
| **MACH** | Mach number — ratio of TAS to the local speed of sound |

It also displays the ISA standard atmosphere properties (temperature, pressure, density, speed of sound, density ratio) at the entered altitude.

## How to Use

1. **Select input type** — Choose which speed type you are entering (CAS / TAS / EAS / MACH).
2. **Enter speed** — Type a value in knots (KTS) or metres per second (M/S).
3. **Enter altitude** — Type a value in feet (FT) or metres (M). Valid range: −2 000 ft to 80 000 ft.
4. **Click CALCULATE** (or press Enter) — All four speed types and ISA atmosphere values are displayed instantly.

The highlighted result card corresponds to the speed type you entered.

## Live Demo

The application is hosted on GitHub Pages:

**[https://tunahanakbey.github.io/AirspeedConverter/](https://tunahanakbey.github.io/AirspeedConverter/)**

No installation or build step is required — it runs entirely in the browser from a single `index.html` file.

## Running Locally

Clone the repository and open `index.html` in any modern browser:

```bash
git clone https://github.com/tunahanakbey/AirspeedConverter.git
cd AirspeedConverter
open index.html   # macOS
# or: xdg-open index.html  (Linux)
# or: start index.html     (Windows)
```

## References

- **ICAO Doc 7488/3** — *Manual of the ICAO Standard Atmosphere*, 3rd ed. (1993). ISA atmosphere equations for temperature, pressure, and density as a function of altitude.
- **ICAO Doc 8168 Vol. I** — *Procedures for Air Navigation Services – Aircraft Operations*, Attachment A. CAS/TAS compressible flow conversion method.
- **Anderson, J. D.** — *Introduction to Flight*, 8th ed. McGraw-Hill (2015). Isentropic flow equations for airspeed conversion (Eq. 4.74).
- **Gracey, W.** — *Measurement of Aircraft Speed and Altitude*, NASA Reference Publication 1046 (1980). EAS/TAS density-ratio relationship.
- **Rayleigh, Lord** — "Aerial Plane Waves of Finite Amplitude", *Proceedings of the Royal Society* (1910); formalised in **NACA Technical Note 1135** (1953). Rayleigh Pitot-tube formula for supersonic CAS/TAS conversion.
