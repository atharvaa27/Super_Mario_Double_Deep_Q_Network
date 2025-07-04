# 🎮 Super Mario Bros AI Agent — Double Deep Q-Network (DDQN)

Train an AI agent to play **Super Mario Bros (NES)** using **Double Deep Q-Network (DDQN)** reinforcement learning.  
The agent learns optimal actions by interacting with the environment, maximizing its score over thousands of training episodes.

---

## 📂 Table of Contents
- [🚀 Project Highlights](#-project-highlights)
- [🔧 Tech Stack](#-tech-stack)
- [🛠️ Setup Instructions](#️-setup-instructions)
- [🎮 Usage](#-usage)
- [📈 Example Results](#-example-results)
- [🔬 Key Learnings](#-key-learnings)
- [🚀 Future Improvements](#-future-improvements)
- [📜 License](#-license)
- [🤝 Acknowledgements](#-acknowledgements)

---

## 🚀 Project Highlights
- ✅ Implemented Double Deep Q-Network (DDQN) to avoid Q-value overestimation
- ✅ Trained the agent on `SuperMarioBros-1-1-v0` using the `RIGHT_ONLY` action set
- ✅ Performed frame preprocessing (resize, grayscale, skip frames)
- ✅ Automated gameplay recording for each test episode
- ✅ Visualized training progress with reward plots

---

## 🔧 Tech Stack
| Technology           | Purpose                               |
|----------------------|---------------------------------------|
| Python               | Core programming language            |
| PyTorch              | Deep learning framework (DDQN model) |
| gym-super-mario-bros | NES Mario environment                |
| nes-py               | NES emulator backend                 |
| OpenAI Gym           | RL environment framework             |
| matplotlib           | Training performance plots           |

---

## 🛠️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/atharvaa27/Super_Mario_Double_Deep_Q_Network.git
cd Super_Mario_Double_Deep_Q_Network
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Install ffmpeg for video recording
- macOS: `brew install ffmpeg`
- Ubuntu: `sudo apt install ffmpeg`

---

## 🎮 Usage

### ▶️ Train the Agent
Run the training in your notebook:
```python
trained_agent = train()
```

### ▶️ Test the Agent and Record Gameplay
```python
scores = test(agent=trained_agent, episodes=3, video_folder="videos", speed=1.0, epsilon=0.0)
```
- Videos saved in the `videos/` folder.
- Set `epsilon > 0` to enable exploration during testing.

---

## 📈 Example Results
- Trained agent consistently completes parts of Level 1-1.
- Example total reward across episodes:  
  ![Reward Plot](reward_plot.png)

---

## 🔬 Key Learnings
- Practical application of Deep Reinforcement Learning
- Improved Q-Learning performance with Double DQN
- Real-time environment interaction & reward maximization
- Optimized agent training pipeline using PyTorch and Gym

---

## 🚀 Future Improvements
- Expand to **SIMPLE_MOVEMENT** for advanced moves (run + jump)
- Train on higher levels (e.g., Level 1-2)
- Add prioritized experience replay
- Deploy to Google Colab for GPU acceleration

---

## 📜 License
MIT License © 2025 Atharvaa Rane

---

## 🤝 Acknowledgements
- [gym-super-mario-bros](https://github.com/Kautenja/gym-super-mario-bros)
- [nes-py](https://github.com/Kautenja/nes-py)
- [OpenAI Gym](https://github.com/openai/gym)
