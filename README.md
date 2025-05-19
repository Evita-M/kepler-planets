# Kepler Planets

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Prettier](https://img.shields.io/badge/prettier-%23F7B93E.svg?style=for-the-badge&logo=prettier&logoColor=black)

## Project Details

This project is part of humanity's quest to answer one of the most profound questions: Are we alone in the universe? By analyzing NASA's Kepler mission data, we process and filter information about exoplanets to identify potentially habitable worlds. The Kepler mission, a revolutionary space observatory, has discovered thousands of planets orbiting other stars, expanding our understanding of the cosmos and our place within it.

The analysis in this project focuses on identifying planets that might be suitable for life by examining key characteristics:

- Planet disposition (confirmed planets)
- Insolation flux (amount of stellar radiation)
- Planetary radius

This project contributes to the broader scientific effort to understand the conditions necessary for life beyond Earth, using the same principles that NASA scientists employ in their search for habitable worlds.

## Technologies Used

- Node.js
- [csv-parse](https://www.npmjs.com/package/csv-parse) library for data processing
- Prettier for code formatting

## Features

- Reads and processes Kepler mission data from CSV files
- Implements scientific criteria for identifying habitable planets:
  - Confirmed planet status
  - Appropriate insolation flux (0.36 to 1.11)
  - Planetary radius less than 1.6 Earth radii
- Outputs a list of potentially habitable planets with their Kepler names
- Provides a count of total habitable planets found

## Data Processing

The project implements efficient data streaming to handle large datasets:

- Uses Node.js streams for memory-efficient processing
- Processes the Kepler data CSV file line by line
- Implements real-time filtering of planetary data
- Provides immediate feedback during data processing
- Handles large datasets without loading entire file into memory

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   pnpm install
   ```
3. Run the project:
   ```bash
   pnpm start
   ```
   Or for development:
   ```bash
   pnpm watch
   ```

The program will process the `kepler_data.csv` file and output the names of potentially habitable planets along with the total count.

## Data Source

The project uses [data from NASA's Kepler mission](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative), which was designed to discover Earth-size planets orbiting other stars. The data is stored in the `kepler_data.csv` file.
