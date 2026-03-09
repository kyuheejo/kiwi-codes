# AI Medical Image Platform (Rail.ai)

Description: AI-enabled medical image viewer
Status: RIP
Tags: Healthcare
Role: Founder

[https://youtu.be/EyaFUT3iaWU](https://youtu.be/EyaFUT3iaWU)

# TL;DR

This project started in my sophomore year and lasted until my graduation in 2022. It started off as a tumor segmentation tool for clinical trials and diagnostics using AI. After interviewing and chatting with radiologists at Hopkins, we observed first-hand how horrible the UI and UX of medical imaging systems are, and pivoted to AI-powered medical image platform. We even had the honor to develop the platform using AWS’s then-new Healthlake imaging when it was still in beta, and present our platform in RSNA in AWS’s booth. We got invited to YC interview as well. However, seeing hundreds of AI medical imaging platforms at RSNA made me realize how competitive the space was, and ultimately, the project is no longer active.

# Product demo

![Copy of Copy of Copy of Rail.ai.gif](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Copy_of_Copy_of_Copy_of_Rail.ai.gif)

![Copy of Copy of Copy of Rail.ai (1).gif](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Copy_of_Copy_of_Copy_of_Rail.ai_(1).gif)

![Copy of Copy of Copy of Rail.ai (2).gif](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Copy_of_Copy_of_Copy_of_Rail.ai_(2).gif)

## Product Overview

Rail Imaging is an AI-enabled, cloud-based medical image management platform designed to address the challenges of managing, analyzing, and storing vast amounts of medical imaging data. It leverages cutting-edge AI and cloud technologies to improve workflow efficiency, enhance data accessibility, and enable AI-driven medical research.

---

## Problem Statement

Medical imaging data management faces critical challenges that hinder operational efficiency and innovation:

1. **Massive Data Volumes**:
    - Imaging data accounts for 80% of hospital data, requiring petabytes of storage
    - On-premise solutions are expensive and lack scalability
2. **Security Vulnerabilities**:
    - Growing threats of ransomware and data breaches
    - Regulatory requirements mandate secure data retention for at least seven years
3. **Barriers in Research**:
    - Difficulty in curating, anonymizing, and analyzing datasets
    - Inconsistent metadata and lack of optimization for AI applications
4. **Workflow Inefficiencies**:
    - Slow retrieval of DICOM images
    - Latency and compatibility issues with legacy systems

---

## Objectives

Rail Imaging aims to:

1. Provide scalable, secure, and cost-effective cloud storage solutions
2. Improve data access with low-latency retrieval and enhanced metadata management
3. Enable seamless integration of AI applications for medical image analysis
4. Support researchers by streamlining dataset curation and anonymization

---

## Key Features

1. **Cloud-Based Image Management**:
    - Store and retrieve medical images using AWS S3 and Glacier for cost-effective, scalable storage
    - Intelligent tiering for efficient data management
2. **AI-Driven Image Analysis**:
    - Automated metadata correction (e.g., laterality, anatomy)
    - Predictive analytics for data demand optimization
3. **Enhanced Data Ingestion**:
    - Support for DICOM and DICOMweb standards
    - Seamless integration with PACS servers and on-premise systems
4. **Faster Retrieval**:
    - Use Curie API for high-speed image retrieval and compression
    - Intelligent caching to reduce latency for frequently accessed data
5. **Workflow Optimization**:
    - Automated hanging protocols for radiologists
    - Recommend comparison studies based on modality and anatomy
6. **AI Research Enablement**:
    - Query metadata to curate datasets
    - Deploy AI models using serverless solutions like AWS Lambda
7. **Security and Compliance**:
    - Encryption and advanced security protocols
    - Compliance with medical data retention regulations

---

## Technical Specifications

![Screen Shot 2025-01-16 at 9.18.08 AM.png](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Screen_Shot_2025-01-16_at_9.18.08_AM.png)

![Screen Shot 2025-01-16 at 9.18.20 AM.png](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Screen_Shot_2025-01-16_at_9.18.20_AM.png)

### Infrastructure

- **Cloud Provider**: AWS (S3, Glacier, Snowball, Storage Gateway).
- **Data Standards**: DICOM, DICOMweb.
- **AI Integration**: Open AI application platform for ML model deployment.

### Architecture

- **Hybrid System**: Combines on-premise storage with cloud capabilities.
- **Image Lifecycle Management**:
    - Automates movement between online, offline, and archival storage.
    - Utilizes intelligent tiering for cost efficiency.
- **File Transfer**:
    - Secure and fast DICOM transfer via intelligent caching.
    - Synchronization through Snowball for bulk migrations.

# Pitch deck

[Copy of Copy of Rail.ai.pdf](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Copy_of_Copy_of_Rail.ai.pdf)

# RSNA

Participated in AWS Healthlake imaging booth in RSNA 2022. 

![Screen Shot 2025-01-15 at 11.30.43 PM.png](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Screen_Shot_2025-01-15_at_11.30.43_PM.png)

![Screen Shot 2025-01-15 at 11.30.55 PM.png](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Screen_Shot_2025-01-15_at_11.30.55_PM.png)

# Original product concept

*Tumor segmentation and 3D reconstruction for clinical trial and diagnostics* 

### Demo

[Untitled design.mp4](AI%20Medical%20Image%20Platform%20(Rail%20ai)/Untitled_design.mp4)

### Underlying Research

[https://github.com/kyuheejo/liver-tumor-segmentation](https://github.com/kyuheejo/liver-tumor-segmentation)