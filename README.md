# Antenna Simulation

A comprehensive MATLAB project for simulating and analyzing radiation patterns of dipole antennas and linear antenna arrays.

## 📋 Overview

This repository contains two main MATLAB assignments that explore antenna radiation characteristics through numerical simulation and visualization:

1. **Radiation Pattern Simulation and Directivity Analysis** - Analysis of omnidirectional dipole antennas
2. **Radiation Pattern Analysis of Linear Antenna Arrays** - Study of broadside and end-fire array configurations

## 🎯 Project Objectives

- Simulate radiation patterns for various antenna configurations
- Analyze how antenna parameters affect radiation characteristics
- Visualize patterns in 2D (polar plots) and 3D surface plots
- Calculate and analyze directivity as a function of antenna dimensions


## 🔬 Part 1: Dipole Antenna Analysis

### Features
- Simulation of omnidirectional dipole antennas for multiple length-to-wavelength ratios
- Analysis of ratios: 0.1, 0.25, 0.5, 0.625, 0.75, 0.9999
- Elevation and azimuthal pattern visualization
- 3D radiation pattern rendering
- Directivity calculation and optimization

### Key Findings
- **l/λ = 0.1**: Nearly perfect figure-eight pattern (Hertzian dipole)
- **l/λ = 0.625**: Maximum directivity achieved
- **l/λ ≥ 0.75**: Side lobes develop, reducing efficiency

### Electric Field Formula
```
E(θ) = [cos(βl cos θ) - cos(βl)] / [sin θ · (1 - cos(βl))]
```

## 📡 Part 2: Linear Antenna Array Analysis

### Configurations Studied

#### Broadside Array
- **Spacing**: d = λ/2
- **Phase shift**: Φ = 0
- **Maximum radiation**: Perpendicular to array axis (θ = 90°)

#### End-Fire Array
- **Spacing**: d = λ/4
- **Phase shift**: Φ = -π/2
- **Maximum radiation**: Along array axis (θ = 0° or 180°)

### Parameters Analyzed
1. **Number of elements (N)**: 2 to 20 elements
2. **Element spacing (d/λ)**: 0.1 to 2.0

### Array Factor Formula
```
AF(θ) = sin(Nψ/2) / [N sin(ψ/2)]
where ψ = kd cos θ + Φ
```

### Key Observations

**Broadside Arrays:**
- Optimal spacing: d/λ = 0.5
- Increasing N narrows the main beam and increases directivity
- Spacing > λ causes grating lobes

**End-Fire Arrays:**
- Highly directional along array axis
- Optimal spacing: d/λ = 0.25 to 0.5
- Rapid beamwidth reduction with increasing N

## 🛠️ Requirements

- MATLAB R2016b or later
- No additional toolboxes required (uses base MATLAB functions)

## 🚀 Usage

### Running Dipole Antenna Simulation
```matlab
% Navigate to dipole_antenna directory
cd dipole_antenna
% Run the main script
dipole_simulation
```

### Running Linear Array Simulations
```matlab
% Navigate to linear_array directory
cd linear_array

% For broadside array with varying N
broadside_array_varying_N

% For broadside array with varying spacing
broadside_array_varying_spacing

% For end-fire array with varying N
endfire_array_varying_N

% For end-fire array with varying spacing
endfire_array_varying_spacing
```

## 📊 Output

All scripts generate:
- **2D polar plots**: Show radiation pattern in the elevation plane
- **3D surface plots**: Visualize complete 3D radiation pattern
- **PNG files**: Automatically saved for each configuration
- **Directivity plots**: Show optimization curves

## 📈 Results Summary

### Dipole Directivity
- Maximum directivity occurs at **l/λ ≈ 0.625**
- Directivity decreases for both shorter and longer antennas
- Side lobes appear when l/λ > 0.75

### Array Performance
- **Broadside**: Best for perpendicular coverage, d/λ = 0.5 optimal
- **End-fire**: Best for directional applications, highly focused beam
- Increasing N improves directivity but adds complexity

## 📝 Notes

- All simulations use isotropic radiating elements
- Uniform amplitude distribution assumed
- Patterns calculated using array factor theory
- Figures are automatically saved to avoid memory issues with multiple open windows

## 🔍 Applications

These simulations are useful for:
- Antenna design and optimization
- Wireless communication system planning
- Radar and sensor array design
- RF engineering education
- Beamforming research
