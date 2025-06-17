**Train Simulator CLI**
Terminal-Based Train Simulator for the Pakenham Line

**Overview**
This terminal-based train simulator provides a simulated command-line experience of a train operating along Melbourne’s Pakenham line. Built in Java with Eclipse and thoroughly tested using JUnit, the simulator derives passenger count data from CSV files and offers train customisation and statistical reporting.

> [!NOTE]  
> The train line does not contain every station.

---

## Features

* **Line Simulation**: Simulates the Pakenham line from Flinders Street to Pakenham, including intermediate stations.
* **Train Configuration**: Create and delete train carriages, toggle direction and train line of choice.
* **Station Configuration**: Edit the passenger demend for each platform. for each time session of the day, add or rem,aove station platforms.
* **Passenger Data**: Read and parse CSV files containing historical passenger counts per station, per hour.
* **Custom Schedules**: Define time session, each with their own data.
* **Real-time Statistics**: Display on-demand stats such as CO2 Emissions (overall and specific to train sections (locomotives/carriages)), passengers left behind, total passengers carried, and the number of complaints.
* **JUnit Test Suite**: Comprehensive automated tests covering core functionality, data parsing, and statistical calculations.

---

## Technology Stack

* **Language**: Java 11+
* **IDE**: Eclipse IDE 2024-06 or later
* **Build & Dependency**: Maven or Gradle (configurable)
* **Testing**: JUnit 5
* **Data**: CSV files for passenger counts

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/noah-bakr/train-simulator-cli.git
   cd train-simulator-cli
   ```
   
2. **Import into Eclipse**

   * Open Eclipse IDE.
   * File → Import → Existing Maven/Gradle Project.
   * Select the cloned directory.
   
3. **Build & Run**

   * Use `mvn clean install` or your IDE’s build function.
   * Run the `Main.java` class from the `src/main/java` folder.

---

## Usage

1. **Loading Passenger Data**

   	Select `c) Import train stations map CSV`, and then `a) Import CSV from File` to import the train line.
   	Return to the Main Menu.
   	Select `d) Import a train station’s demand CSV`, and then `a) Import CSV from File` to import the demand of each station (number of passengers).

2. **Creating a Train**

   	Select `g) Simulate a train run` to view options for the simulation.
   	Select `a) Add/remove a carriage` to configure the size of the train.
   
3. **Configuring the Train Line and Direction**

   	Select `b) Specify line and direction`.

3. **Configuring the Time of Day**

   	Select `c) Specify time session`.
  
4. **Running the Simulation**

	Select `d) Run sim`.

   
5. **Viewing Statistics**

   Select `h) Show statistics based on last run`.

---

## Customization Options

* **Train Parameters**: Adjust number of cars, passenger capacity, acceleration/deceleration rates.
* **Schedule Settings**: Modify departure intervals, dwell times at each station.
* **Delay Injection**: Introduce random or scheduled delays to test resilience.
* **Output Formats**: Switch between table view, CSV export, or JSON summary.

---

## Data Input (CSV Format)

The simulator expects passenger counts in CSV format with the following columns:

```
Station,Hour,PassengerCount
Flinders Street,06,1200
Caulfield,06,800
…
```

Ensure there are no header typos and all data rows use valid station names matching the internal station list.

---

## Testing

Run the full suite of JUnit tests to verify components:

```bash
mvn test
```

Key test packages:

* `com.simulator.model` – Train, Station, Schedule classes
* `com.simulator.io` – CSV parser and data loader
* `com.simulator.stats` – Statistical analysis modules

---

## Future Enhancements

* **Graphical Front-End**: Develop a simple Swing or JavaFX GUI.
* **Live Data Integration**: Connect to real-time APIs for passenger flow.
* **Multi-Line Support**: Expand beyond the Pakenham line to cover the full metropolitan network.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add Your Feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License. See `LICENSE` for more details.

---

## Contact

**Author**: Your Name
**Email**: [your.email@example.com](mailto:your.email@example.com)
**GitHub**: [https://github.com/yourusername](https://github.com/yourusername)

Feel free to reach out with any questions or suggestions!

