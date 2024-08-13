# 🗓️ Intelligent Course Scheduler

## 📚 Project Overview

This project implements an intelligent course scheduling system using a genetic algorithm. It automates the complex task of creating optimal timetables for educational institutions.

## 🔧 Key Components

### 1. 📊 Data Loading and Cleaning

- 📥 Loads course details from an Excel file using pandas
- 🧹 Removes unnecessary header rows
- 🏷️ Renames columns for clarity (e.g., 'Course-Code', 'Course Name')
- 🚮 Eliminates rows with NaN values for data integrity

### 2. 🛠️ Algorithm Setup

- ⏰ Defines time slots for classes
- 🏫 Sets up available room numbers
- ⚙️ Configures genetic algorithm parameters

### 3. 🧬 Genetic Algorithm Implementation

- 💪 Fitness Function: Evaluates timetable quality
  - Checks for teacher conflicts
  - Identifies room double-bookings
  - Assesses other potential clashes
- 🎲 Create Individual: Generates a random timetable
- 🔀 Crossover: Combines two timetables to create a new one
- 🔄 Mutate: Introduces random changes to explore alternatives
- 🏆 Selection: Chooses the best timetables from a random group

### 4. 🚀 Algorithm Execution

- 🌱 Initializes a population of random timetables
- 🔁 Iteratively improves timetables through crossover and mutation
- 🔍 Searches for the optimal timetable over multiple generations

### 5. 📊 Output Generation

- 🏅 Selects the best-performing timetable
- 📋 Converts the optimal timetable to a user-friendly dataframe format

## 🚀 Getting Started

1. Ensure you have Python installed on your system
2. Install required libraries: `pip install pandas numpy`
3. Place your course data Excel file in the project directory
4. Run the script: `python timetable_generator.py`

## 📈 Results

The final output will be a comprehensive timetable that:
- Avoids teacher conflicts
- Prevents room double-bookings
- Optimizes course scheduling
