[![Bluelake](https://raw.githubusercontent.com/lancelee82/bluelake/master/data/bl2.png)](https://github.com/lancelee82/bluelake)

# Bluelake: Pygame Based Framework and Games.


## Bluegym

In order to learn Deep Reinforcement Learning with OpenAI Gym and
[Bluelake](https://github.com/lancelee82/bluelake), Bluegym wraps
the games and exposes a Gym environment like Atari games.

The main purpose of this project is providing a convenient method
to design and test functions for Reinforcement Learning, such as
designing the reward functions, testing action spaces, etc.


## Usage

```python
from bluegym import env_bluelake

ENV_GAME_NAME = 'Sandroad-v0'
BLG_GAME_NAME = 'gymroad'

def env_reg():
    env_bluelake.gym_env_register_bluelake(
        BLG_GAME_NAME, (640, 480),
        ENV_GAME_NAME,
        obs_type='image',
        ##frameskip=(1, 2)
        frameskip=(1, 5)
    )

def env_make():
    env = gym.make(ENV_GAME_NAME)
    np.random.seed(123)
    env.seed(123)

    return env

my_env = env_make()
```
