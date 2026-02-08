# Credential Stuffing Detection (Failed Login Velocity)

This project detects credential stuffing attacks by identifying high-velocity failed login
attempts across multiple user accounts originating from the same IP address within short
time windows.

## Problem Statement
Credential stuffing is a common account takeover (ATO) attack in which automated systems
attempt to authenticate across many user accounts using previously leaked credentials.
These attacks are characterized by rapid login attempts, high failure rates, and broad
account targeting.

## Approach
The detection logic is based on behavioral aggregation rather than machine learning:

1. Group login events by IP address and fixed 10-minute time windows  
2. Count failed login attempts and distinct user accounts per window  
3. Flag suspicious behavior using explainable thresholds  
4. Extract raw event evidence for investigation  

## Key Signals
- Failed login velocity  
- Number of distinct users targeted  
- Short time-based attack windows  

## Output
- Aggregated alert table identifying suspicious IP and time windows  
- Evidence view showing raw login events that triggered alerts  
- Optional visualization highlighting IPs with elevated failure volume  

## Tools Used
- Python  
- pandas  
- Jupyter Notebook
- Matplotlib

## Why This Matters
This project mirrors real-world fraud and trust & safety workflows by emphasizing
explainable detection logic, investigation-ready outputs, and practical signal design.
