# Connect 4 Game with AI Agents

This project implements the classic Connect 4 game with various AI implementations, including Minimax algorithm, Machine Learning-based agents, and other AI strategies. The project features multiple game modes, performance evaluation tools, and a comprehensive AI training system.

## Project Overview

The project consists of several components:
- Console-based game for basic gameplay
- GUI-based game with Minimax AI
- AI vs AI gameplay modes
- Performance evaluation tools
- Machine Learning model training system

## Requirements

- Python 3.x
- Required packages:
  - NumPy: For numerical computations and board representation
  - Pygame: For GUI implementation
  - scikit-learn: For machine learning model implementation
  - pandas: For data processing
  - joblib: For model serialization
  - matplotlib: For performance visualization
  - seaborn: For statistical visualizations
  - psutil: For performance monitoring

Install all required packages using:

```bash
pip install numpy pygame scikit-learn pandas joblib matplotlib seaborn psutil
```

## File Structure and Description

### Core Game Files
- `game_console_version.py`: Text-based implementation of Connect 4
  - Features: Human vs Random AI gameplay
  - Simple interface for testing game mechanics
  - Perfect for quick games and testing

- `game_minmax.py`: GUI-based game with Minimax AI
  - Implements the Minimax algorithm with alpha-beta pruning
  - Features a graphical interface using Pygame
  - Contains core game logic and board representation
  - Includes sophisticated board evaluation heuristics

### AI and Machine Learning
- `train_ml_model.py`: Machine Learning model training script
  - Trains a Random Forest classifier on the Connect 4 dataset
  - Processes and prepares training data
  - Saves the trained model to `connect4_model.joblib`

- `game_ai_vs_minimax.py`: AI vs AI gameplay
  - Pits ML-based AI against Minimax AI
  - Features adjustable game speed
  - Includes visualization of AI decision-making

### Performance and Evaluation
- `performance_evaluation.py`: Comprehensive evaluation suite
  - Measures AI agent performance
  - Tracks metrics like win rates, game lengths, and execution times
  - Generates performance visualizations and reports
  - Includes various AI agent implementations for comparison

### Data Files
- `connect-4.data`: Main dataset (67,557 game positions)
- `connect-4.names`: Dataset format documentation
- `connect4_model.joblib`: Trained ML model file (generated after training)

## How to Run

### 1. Console Version (Beginner-Friendly)
```bash
python game_console_version.py
```
- Use numbers 0-6 to select columns
- Perfect for learning the game mechanics

### 2. GUI Version with Minimax AI
```bash
python game_minmax.py
```
- Click on columns to drop pieces
- Features visual feedback and game state display

### 3. AI vs AI Version
```bash
python game_ai_vs_minimax.py
```
Controls:
- Up Arrow: Increase game speed
- Down Arrow: Decrease game speed
- Space: Pause/Resume game

### 4. Performance Evaluation
```bash
python performance_evaluation.py
```
- Runs comprehensive performance tests
- Generates performance reports and visualizations
- Results saved in `evaluation_results` directory

## Training Your Own Model

To train a new ML model:
1. Ensure the dataset files are present
2. Run:
```bash
python train_ml_model.py
```
- The script will process the dataset and train a new model
- The trained model will be saved as `connect4_model.joblib`

## Implementation Details

### Machine Learning Model
- Uses Random Forest classifier
- Trained on 67,557 game positions
- Features engineered from board states
- Predicts optimal moves based on board patterns

### Minimax AI
- Implements alpha-beta pruning for efficiency
- Configurable search depth
- Custom position evaluation heuristics
- Considers multiple winning patterns

### Performance Metrics
- Win/Loss/Draw ratios
- Game length statistics
- Execution time analysis
- Memory usage tracking
- Pattern recognition analysis

## Contributing

Feel free to contribute to this project by:
1. Implementing new AI strategies
2. Improving existing algorithms
3. Enhancing the UI/UX
4. Adding new features or game modes

## Troubleshooting

Common issues and solutions:
1. If the GUI doesn't launch, ensure Pygame is properly installed
2. For ML model errors, verify all dataset files are present
3. For performance issues, adjust the Minimax depth or ML model parameters 
