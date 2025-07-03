# Grid World Reinforcement Learning

A comprehensive implementation of **Policy Iteration** and **Value Iteration** algorithms for solving a classic 4x3 grid world problem in reinforcement learning.

## 🎯 Overview

This project demonstrates the fundamental dynamic programming algorithms used in reinforcement learning through a visual and interactive grid world environment. The implementation includes detailed analysis, visualizations, and performance comparisons between Policy Iteration and Value Iteration algorithms.

## 🌟 Features

- **Complete Grid World Environment**: 4x3 grid with customizable rewards and obstacles
- **Policy Iteration Algorithm**: Full implementation with policy evaluation and improvement
- **Value Iteration Algorithm**: Bellman equation-based value updates
- **Rich Visualizations**: 
  - Grid world layout with color-coded states
  - Utility value heatmaps
  - Policy direction arrows
  - Convergence analysis plots
  - Algorithm comparison charts
- **Comprehensive Analysis**: 
  - State-by-state comparisons
  - Optimal path tracing
  - Performance metrics
  - Convergence tracking

## 🚀 Quick Start

### Prerequisites

```bash
pip install numpy pandas matplotlib seaborn
```

### Running the Code

```bash
jupyter nbconvert --execute --to notebook --inplace gridworld_rl.ipynb
```

## 🗺️ Grid World Setup

The environment consists of:
- **Grid Size**: 4x3 (12 total cells)
- **Start State**: (1,1) - bottom-left corner
- **Terminal States**: 
  - (4,3): +1 reward (goal state)
  - (4,2): -1 reward (penalty state)
- **Wall**: (2,2) - impassable obstacle
- **Living Penalty**: -0.04 per step
- **Discount Factor**: γ = 0.9

### Action Model
- **Intended Action**: 80% probability
- **Perpendicular Actions**: 10% each
- **Actions**: Up, Down, Left, Right

## 📊 Algorithm Implementations

### Policy Iteration
1. **Policy Evaluation**: Calculate utilities for current policy
2. **Policy Improvement**: Update policy based on utilities
3. **Convergence**: Repeat until policy stabilizes

### Value Iteration
1. **Value Updates**: Apply Bellman equation to all states
2. **Policy Extraction**: Derive optimal policy from final utilities
3. **Convergence**: Continue until utility changes are minimal

## 🎨 Visualizations

The implementation generates several types of visualizations:

1. **Grid World Layout**: Shows the environment structure
2. **Utility Heatmaps**: Color-coded utility values
3. **Policy Arrows**: Visual representation of optimal actions
4. **Convergence Plots**: Algorithm performance over iterations
5. **Comparison Charts**: Side-by-side algorithm analysis

## 📈 Results & Analysis

### Key Findings
- Both algorithms converge to nearly identical solutions
- Policy Iteration typically requires fewer iterations
- Value Iteration provides more stable convergence
- Optimal policies successfully avoid the -1 terminal state
- Living penalty encourages quick termination

### Performance Metrics
- **Convergence Speed**: Iterations required for each algorithm
- **Utility Accuracy**: Precision of final state values
- **Policy Agreement**: Percentage of states with identical policies
- **Path Optimality**: Analysis of generated paths to goal

## 🔧 Code Structure

```
gridworld_rl.ipynb
├── GridWorld class          # Environment definition
├── PolicyIteration class    # Policy iteration implementation
├── ValueIteration class     # Value iteration implementation
├── Visualization functions  # Plotting and analysis tools
└── Analysis functions       # Comparison and metrics
```

## 🧪 Experiments

The code automatically runs several experiments:

1. **Basic Algorithm Execution**: Run both algorithms on the standard grid
2. **Convergence Analysis**: Track how utilities change over iterations
3. **Policy Comparison**: Compare optimal policies from both methods
4. **Path Analysis**: Trace optimal paths from start to goal
5. **Performance Benchmarking**: Compare computational efficiency

## 📚 Educational Value

This implementation is designed for:
- **Students** learning reinforcement learning fundamentals
- **Researchers** exploring dynamic programming algorithms
- **Educators** teaching MDP solution methods
- **Practitioners** understanding algorithm trade-offs

## 🎛️ Customization

Easy to modify parameters:
- Grid dimensions and layout
- Reward values and terminal states
- Action probabilities and noise
- Convergence criteria and tolerances
- Visualization styles and colors

## 📖 Theory Background

### Markov Decision Process (MDP)
The grid world represents a finite MDP with:
- **States**: Grid positions
- **Actions**: Movement directions
- **Transitions**: Stochastic movement model
- **Rewards**: Immediate payoffs
- **Policy**: Action selection strategy

### Bellman Equations
Both algorithms solve the Bellman equations:
- **Value Function**: V(s) = max_a Σ P(s'|s,a)[R(s,a,s') + γV(s')]
- **Policy Function**: π(s) = argmax_a Σ P(s'|s,a)[R(s,a,s') + γV(s')]

## 🤝 Contributing

Contributions are welcome! Areas for improvement:
- Additional visualization options
- More grid world configurations
- Performance optimizations
- Extended analysis features
- Interactive GUI components

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Based on classic reinforcement learning textbook examples
- Inspired by Russell & Norvig's "Artificial Intelligence: A Modern Approach"
- Visualization techniques adapted from matplotlib documentation

## 📞 Contact

For questions, suggestions, or collaborations, please open an issue or submit a pull request.

---

*This implementation provides a solid foundation for understanding dynamic programming in reinforcement learning through hands-on experimentation and visualization.*
