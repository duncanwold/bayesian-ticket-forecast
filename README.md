# Bayesian Ticket Forecast

![Forecast Visualization](screenshot.png)

A Bayesian statistical forecasting tool for predicting ticket sales at live 
event venues. Originally developed for PianoFight Theater in San Francisco.

## Overview

This application uses historical event data to predict final ticket sales for 
upcoming shows. By analyzing patterns from past events with similar 
characteristics (venue, timing, initial sales velocity), it generates 
probabilistic forecasts with confidence intervals.

## Features

- **Bayesian Probability Model** — Calculates likelihood of various sales 
outcomes based on historical data
- **Real-time Forecasting** — Projects final ticket sales based on current 
sales and time until event
- **Interactive Visualizations** — Dynamic plots showing probability 
distributions and sales trajectories
- **Credible Intervals** — Statistical confidence ranges for predictions
- **Historical Pattern Matching** — Identifies similar past events to improve 
forecast accuracy
- **Multi-venue Support** — Handles different venue capacities

## How It Works

### The Forecasting Algorithm

1. **State Definition** — Defines a "state" based on current conditions:
   - Number of tickets sold (with tolerance range)
   - Time until event start (with tolerance range)
   - Venue type

2. **Historical Analysis** — Scans historical events to find matches:
   - Filters for events that passed through the defined state
   - Tracks their final attendance numbers

3. **Bayesian Calculation** — Computes probabilities:
