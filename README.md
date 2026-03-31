# TableTennisEnvironment

A PyBullet-based physics simulation environment for training robotic arms to play table tennis. The environment models ball trajectory, bounce physics, and arm kinematics, and provides a Gym-compatible interface for reinforcement learning. It also includes inverse kinematics (IK) solvers for a delta robot and data-driven trajectory prediction using regression models.

## Features

- PyBullet simulation environment for table tennis with configurable physics
- Custom OpenAI Gym environment (`TableTennisEnvironmentV0`)
- Ball trajectory data collection and replay
- Delta robot inverse kinematics via DH parameters
- Hitting point and timing prediction using Random Forest regression
- IK estimation with scikit-learn and saved model (`.joblib`)
- Visualization of ball trajectories and environment states

## Tech Stack

- Python 3
- PyBullet
- OpenAI Gym
- scikit-learn
- NumPy, Pandas
- Jupyter Notebooks

## Project Structure

| File / Directory | Description |
|---|---|
| `TableTennisEnvironment.ipynb` | Main environment development and testing notebook |
| `TableTennisEnvironmentV0/` | Gym environment source code |
| `IK_delta.ipynb` | Inverse kinematics for delta robot |
| `inverse_kinematics_DH_parameters.ipynb` | DH parameter-based IK derivation |
| `TrainHittingPointAndTime.ipynb` | ML model to predict ball hitting point and timing |
| `delta_regressor_RF.joblib` | Saved Random Forest regressor for IK |
| `delta_estimate.csv` | Training data for delta IK regressor |
| `utils/` | Utility functions |

## Requirements

```
pybullet
gym
scikit-learn
numpy
pandas
matplotlib
jupyter
```

## Usage

```bash
pip install pybullet gym scikit-learn numpy pandas matplotlib
jupyter notebook TableTennisEnvironment.ipynb
```

## License

MIT
