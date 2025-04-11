---
layout: default
title: WaitFast Application
github_url: https://github.com/TiernanJesrani/WaitFast
---

<style>
  .slider-container {
    width: 100%;
    overflow-x: auto;
    white-space: nowrap;
    padding: 20px 0;
    -webkit-overflow-scrolling: touch; 
    scrollbar-width: thin; 
  }
  
  .slider-container::-webkit-scrollbar {
    height: 8px;
  }
  
  .slider-container::-webkit-scrollbar-thumb {
    background-color: rgba(0, 0, 0, 0.3);
    border-radius: 4px;
  }
  
  .slider {
    display: inline-flex;
    flex-wrap: nowrap;
  }
  
  .slider img {
    width: 300px;
    height: 550px; 
    object-fit: cover; 
    margin: 0 10px;
    border-radius: 8px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  }
</style>

[← Back to Home](../index.html)

# WaitFast: Dynamically Updated Wait Time Application  
*January 2025 – Present*

---

## Overview

**WaitFast** is a mobile application designed to provide users with real-time, crowd-sourced wait times for restaurants and bars. The app empowers users to make informed decisions by offering accurate and dynamically updated information.

---

## Key Contributions:
- **Mobile Development:**  
  Developed using **Swift**, integrating Google and Apple location APIs for precise user and venue tracking.

- **Backend Integration:**  
  Engineered a **Flask** backend connected to a PostgreSQL database, handling live data updates through optimized **SQL** queries and dynamically formatted **JSON** payloads.

- **Data Crowdsourcing:**  
  Designed a community-driven system where users can submit and verify wait times—aggregated, validated, and surfaced through the app interface.

- **Security and Data**
  Secured backend endpoints using **AWS** Secrets Manager for credential handling and hosted the database on **AWS RDS** for scalability.
  
- **Real-Time UX:**
  Implemented logic for displaying high-confidence, crowd-validated wait estimates based on recent submissions and historical trends.

---

## Problem & Persona

Users often struggle to decide where to eat or drink due to long wait times and lack of accurate information.  
**WaitFast** addresses this by offering:
- Verified, real-time data.
- A simple interface tailored to users' immediate decision-making needs.

---

## Tech Stack:
- **Frontend:** Swift (iOS)
- **APIs:** Google Places API, Apple Maps API
- **Backend:** AWS, SQL, JSON for dynamic data updates, Python 

## Access:
- This application is currently available for free on the appstore!
[View On App Store](https://apps.apple.com/us/app/waitfast/id6744225739)

---

[← Back to Home](../index.html)