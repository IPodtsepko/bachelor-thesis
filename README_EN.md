# Bachelor's Graduation Thesis

> [!NOTE]
> Для чтения данного документа на русском языке перейдите по [ссылке](README.md).

This repository contains materials for my bachelor's graduation thesis on the topic "Transcoding JPEG Images by Predicting DCT Coefficients Using a Neural Network," which was prepared by me upon graduation from the Computer Technologies Department of ITMO University. The defense took place on June 7, 2024. Below is the main information about the thesis.

### Table of Contents

- [SUMMARY OF THE GRADUATION THESIS](#summary-of-the-graduation-thesis)
- [DESCRIPTION OF THE GRADUATION THESIS](#description-of-the-graduation-thesis)
  - [Technical Specification](#technical-specification)
  - [Research Goal](#research-goal)
  - [Research Tasks](#research-tasks)
  - [Short Summary of Results/Findings](#short-summary-of-resultsfindings)
- [Repository Structure](#repository-structure)


## SUMMARY OF THE GRADUATION THESIS

**Student** Igor Sergeevich Podtsepko

**Faculty/Institute/Cluster** Faculty of Information Technology and Programming

**Group** M34381

**Educational Program** Informatics and Programming 2020

**Language of the Educational Program** Russian

**Degree Level** Bachelor

**Thesis Topic** Transcoding JPEG Images by Predicting DCT Coefficients Using a Neural Network

**Thesis Supervisor** Evgeny Alexandrovich Belyaev, PhD, ITMO University, Faculty of Information Technology and Programming, Associate Professor

## DESCRIPTION OF THE GRADUATION THESIS

### Technical Specification

Develop and train a neural network that predicts a portion of discrete cosine transform (DCT) coefficients from the input JPEG image and use the predicted coefficients for entropy coding of the original coefficients.

### Research Goal
To explore the potential of neural networks for implementing the internal prediction stage of DCT coefficients during the transcoding of JPEG images.

### Research Tasks

1. Implement decoding of JPEG images with removal (zeroing) of some DCT coefficients to prepare a dataset for training the neural network;
2. Develop and train a neural network that predicts (calculates) a portion of DCT coefficients based on the remaining coefficients;
3. Implement prediction-based encoding to compress the selected portion of DCT coefficients;
4. Evaluate the degree of compression achieved through neural network-based internal prediction.

### Short Summary of Results/Findings

A method for internal prediction of DCT coefficients for transcoding JPEG images was developed, based on the application of a neural network, resulting in an average reduction of JPEG file size from a subset of the ImageNet dataset by 3.33% with a median of 3.38%. The best achieved compression was 6.28%. The method successfully integrates with the Jpegtran utility, allowing for replacing Huffman coding with arithmetic coding, with an overall compression ratio averaging 13.16%.

## Repository Structure

- [output](output) — PDF files of the thesis report and presentation submitted for defense;
- [presentation](presentation) — presentation source files in Figma;
- [program](program) — developed library for transcoding JPEG images;
- [thesis](thesis) — LaTeX source files of the thesis report.
