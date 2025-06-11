
# g4padre

**g4padre** is a simplified Geant4-based simulation extracted from the `g4main` framework. It models a basic detector setup consisting of:

* A single **CdTe detector**
* **X-ray windows**
* An **aluminum window**

This setup is intended for x-ray detection studies or as a clean starting point for detector development and testing in simulation.

## Project Structure

* Based on the `g4stix` package (simplified)
* Minimal geometry focused on essential components only

## Author

**Hualin Xiao**
[hualin.xiao@fhnw.ch](mailto:hualin.xiao@fhnw.ch)

## History

* **Jun 11, 2025**: Initial version extracted and simplified from `g4stix`

## Requirements

* Geant4 (tested with version ≥10.7)
* CMake
* ROOT



## Workflow

* compile source code:
  - cd <SOURCE_CODE>
  - cmake .
  - make

* validation with visualization
  - ./g4main --gui -m vis.mac
* run simulations
  - ./g4main  -m response.mac -o response.root
* create response matrix from the simulation outputs
  - cd analysis
  - python process_root.py



