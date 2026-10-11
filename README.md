# Aquatic Ecotoxicity Testing

This repository presents a series of laboratory experiments conducted as part of the course **12237 Chemicals in the Environment** at the Technical University of Denmark (DTU).

The project investigates the aquatic toxicity of **4-nitrophenol (4-NP)** using three different test organisms representing different biological responses:

- Marine bacterium — *Vibrio fischeri*
- Freshwater green alga — *Raphidocelis subcapitata*
- Marine crustacean — *Acartia tonsa*

Across the three experiments, concentration–response relationships were used to evaluate chemical toxicity and estimate effect or lethal concentrations.

---

## Project Overview

The laboratory series examines how the same chemical contaminant can produce different toxic responses across aquatic organisms.

Three ecotoxicological tests were conducted:

| Laboratory Test | Test Organism | Toxicity Endpoint | Main Metrics |
|---|---|---|---|
| Lab 1 | *Vibrio fischeri* | Bioluminescence inhibition | EC10, EC20, EC50 |
| Lab 2 | *Raphidocelis subcapitata* | Algal growth inhibition | EC10, EC20, EC50 |
| Lab 3 | *Acartia tonsa* | Mortality | LC10, LC20, LC50 |

The experiments combine laboratory measurements with concentration–response modelling to characterize the acute or short-term toxic effects of 4-nitrophenol.

---

## Lab 1 — *Vibrio fischeri* Bioluminescence Inhibition

The first experiment investigated the acute toxicity of 4-nitrophenol using the marine bioluminescent bacterium *Vibrio fischeri*.

The test followed the principles of **ISO 11348-3**, where toxicity is evaluated through changes in bacterial light emission following chemical exposure.

### Experimental Approach

- Five 4-nitrophenol concentrations were tested.
- Bioluminescence was measured after 10 and 20 minutes of exposure.
- Correction factors were used to evaluate test validity.
- Concentration–response relationships were analysed using R.
- EC10, EC20, and EC50 values were estimated.

### Key Results

For the valid **10-minute exposure dataset**:

- **EC10:** 116.8 mg/L
- **EC20:** 140.9 mg/L
- **EC50:** 201.8 mg/L

The 10-minute correction factor satisfied the test validity criterion, whereas the 20-minute dataset did not fully meet the criterion and was therefore interpreted with caution.

The experiment also showed negative inhibition values at several lower concentrations, indicating possible low-dose stimulation and experimental variability.

---

## Lab 2 — Freshwater Algal Growth Inhibition

The second experiment evaluated the toxicity of 4-nitrophenol to the freshwater green alga *Raphidocelis subcapitata*.

The experiment followed **ISO 8692** and assessed toxicity through inhibition of algal growth.

### Experimental Approach

- Algae were exposed to a concentration series of 4-nitrophenol.
- The exposure period was approximately 72 hours.
- Biomass development was quantified using fluorescence measurements of acetone-extracted chlorophyll.
- Growth rates were calculated relative to the untreated control.
- Concentration–response modelling was used to estimate EC values.

### Key Results

The experiment produced a clear sigmoidal concentration–response relationship.

The estimated effect concentrations were:

- **EC10:** 1.986 mg/L
- **EC20:** 3.588 mg/L
- **EC50:** 11.12 mg/L

Growth inhibition increased progressively with concentration, reaching **100% inhibition at 120 mg/L**.

The EC50 estimate was well constrained, while the lower-effect region contained greater uncertainty because the lowest tested concentration already caused substantial inhibition.

---

## Lab 3 — *Acartia tonsa* Acute Toxicity

The third experiment investigated the acute toxicity of 4-nitrophenol to the marine copepod *Acartia tonsa*.

Unlike the previous experiments, which measured inhibition, this test used **mortality as the toxicity endpoint**.

### Experimental Approach

- Organisms were exposed to a concentration range of 0–120 mg/L.
- Four replicates were used for each concentration.
- Mortality was recorded after 24 hours.
- A concentration–response model was fitted to the experimental data.
- LC10, LC20, and LC50 values were estimated.

### Key Results

Mortality increased strongly with increasing 4-nitrophenol concentration:

- **28.6% mortality at 7.5 mg/L**
- **48.0% mortality at 15 mg/L**
- **96.4% mortality at 30 mg/L**
- **100% mortality at 120 mg/L**

The estimated lethal concentrations were:

- **LC10:** 5.30 mg/L
- **LC20:** 7.25 mg/L
- **LC50:** 13.22 mg/L

The concentration–response curve showed a steep transition between 15 and 30 mg/L.

Control mortality reached 16.7%, exceeding the formal validity criterion of 10%. This limitation was therefore considered when interpreting the absolute LC estimates.

---

## Cross-Species Comparison

The three experiments demonstrate that toxicity assessment depends strongly on both the **test organism** and the **biological endpoint**.

| Test Organism | Endpoint | 50% Effect / Lethal Concentration |
|---|---|---:|
| *Vibrio fischeri* | Luminescence inhibition | EC50 = 201.8 mg/L |
| *Raphidocelis subcapitata* | Growth inhibition | EC50 = 11.12 mg/L |
| *Acartia tonsa* | Mortality | LC50 = 13.22 mg/L |

Under the tested experimental conditions, *Vibrio fischeri* required substantially higher concentrations of 4-nitrophenol to produce the modelled 50% effect than the algae and crustacean tests.

However, these values represent different organisms, endpoints, and exposure durations and therefore should not be interpreted as directly interchangeable toxicity thresholds.

The comparison highlights the value of using multiple biological test systems when evaluating aquatic chemical toxicity.

---

## Key Skills & Methods

**Ecotoxicology**

- Aquatic toxicity testing
- Concentration–response assessment
- EC10, EC20, EC50 estimation
- LC10, LC20, LC50 estimation
- Test validity assessment
- Cross-species toxicity interpretation

**Laboratory Methods**

- Preparation of chemical concentration series
- Biological exposure experiments
- Bioluminescence measurements
- Fluorescence-based biomass measurements
- Mortality assessment
- Replicate and control design

**Data Analysis**

- Concentration–response modelling
- Nonlinear dose–response analysis
- Confidence interval interpretation
- Experimental uncertainty assessment
- R-based analysis using course-provided scripts

**Environmental Assessment**

- Aquatic ecotoxicology
- Chemical hazard assessment
- Species-specific toxicity
- Environmental risk interpretation

---

## Experimental Limitations

The experiments also illustrate several practical challenges in ecotoxicological testing:

- Test validity criteria can influence the reliability of toxicity estimates.
- Concentration selection affects how well the complete dose–response curve is captured.
- Low-effect regions may contain substantial uncertainty.
- Biological variability and experimental handling can influence measured responses.
- Different organisms and endpoints can produce substantially different toxicity estimates.
- Modelled EC/LC values should therefore be interpreted together with experimental design and confidence intervals.

---

## Repository Structure

```text
aquatic-ecotoxicity-testing/
├── lab-1-vibrio-fischeri/
│   └── lab-1-vibrio-fischeri.pdf
├── lab-2-freshwater-algae/
│   └── lab-2-freshwater-algae.pdf
├── lab-3-acartia-tonsa/
│   └── lab-3-acartia-tonsa.pdf
└── README.md
```

Each directory contains the corresponding laboratory report, including experimental methodology, results, concentration–response analysis, discussion, and interpretation.

---

## Project Information

**Course:** 12237 Chemicals in the Environment  
**Institution:** Technical University of Denmark (DTU)  
**Semester:** Spring 2026  
**Project Type:** Laboratory-based aquatic ecotoxicity assessment  
**Test Chemical:** 4-Nitrophenol
