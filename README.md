# PYNQZ2HopfFibration
An attempt to produce the Hopf Fibration using a SoC, specifically the PYNQ-Z2 board with Jupyters Notebook
# Hopf Fibration Visualization with PYNQ

This repository documents the process and results of visualising the Hopf Fibration on a PYNQ platform using a custom IP for the Hopf Map calculation. This work is a part of the EE315 Further VHDL and FPGA Design course project by Finlay Harris, Morgan McFarlane, and James Petrie at the University of Strathclyde.

## Overview

The Hopf Fibration is a rich and complex structure from the field of topology, representing a continuous map from a 3-dimensional sphere to a 2-dimensional sphere. The objective of this project was to generate an artistic representation of the Hopf Fibration, leveraging the computational capabilities of the programmable logic (PL) on a System on Chip (SoC) for parallel processing. We approached this goal through three primary methods:

1. A custom IP designed in System Generator that calculates the Hopf Map based on an angle input and trigonmetric methods.
2. An AXI-Stream IP to manage the computation of 4D coordinates, contrasted with a similar custom IP using AXI Lite for comparison.
3. A custom IP that calculates the Hopf Map using a linear algebra approach

## Project Structure

The project includes software and hardware implementations, along with the necessary tools and interfaces for visualising the Hopf Fibration. Here's how the repository is organised:

- `AXILite/`: Contains the Python notebook and .hwh, .bit & .slx files for the AXI-Lite-based visualisation of the Hopf Fibration using trig methods.
- `AXIStream/`: Contains the Python notebook and .hwh, .bit & .slx files for the AXI-Stream-based visualisation of the Hopf Fibration using trig methods.
- `HopfMapIP/`: Contains the Python notebook and .hwh, .bit & .slx files for the AXI-Lite-based visualisation of the Hopf Fibration using the custom Hopf Map IP.

## Hardware Implementation

The hardware implementation is realised through two interfaces:

### AXI-Stream Interface

- Processes data in large chunks, allowing for efficient and quick computations.
- Utilises FPGA to perform parallel computation of 4D coordinates and stereographic projections.

### AXI Lite Interface

- Provides a simpler interface for smaller data transfers.
- Uses the same custom IP but is limited in terms of speed due to sequential data processing.

## Visualising the Hopf Fibration

The visualisation is performed in 3D using matplotlib and mpl_toolkits in Python. It involves generating angles (alpha, phi, theta), computing 4D coordinates through the Hopf Map, and then performing stereographic projection to 3D.

## Getting Started

To run this project on your PYNQ board:

1. Clone the repository to your local machine or directly to the PYNQ board.
2. Ensure you have the required Python packages installed (`numpy`, `matplotlib`).
3. Deploy the PYNQ overlay by navigating to chosen folder and running the provided scripts.
4. Execute the visualisation scripts found in the notebook file.

## Contribution

Contributions to improve or enhance the visualization and computation methods are welcome. Please feel free to fork the repository, make changes, and submit a pull request as there is plenty of work to improve upon.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Professors and colleagues at the University of Strathclyde for their guidance and support.
- The open-source community for the continuous evolution of the PYNQ framework.

## Authors

- **Finlay Harris**
- **Morgan McFarlane**
- **James Petrie**

For any queries or further discussion, please contact the authors via GitHub or university email.
