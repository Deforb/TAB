# Get Started

You can find our official code here: [TAB github](https://github.com/DevCrafterLZY/TAB)

## Table of Contents

<!-- 1. [Steps to develop your own method](#Steps-to-develop-your-own-method)
1. [Steps to evaluate on your own time series](#Steps-to-evaluate-on-your-own-time-series)
1. [Pipeline introduction](#Pipeline-introduction)
1. [FAQ](#FAQ)
1. [Citing TFB](#Citing-TFB)  -->

1. [Quickstart](#Quickstart)
1. [Contact](#Contact)

## Quickstart

### Installation

Follow the steps below to configure the TAB environment.

#### 1. Install Git

Some models require Git to run. Please ensure that Git is installed on your system. If not, you can install it using the following command:

```shell
sudo apt-get install git
```

#### 2. Download and Extract Environment

Download the environment from [OneDrive](https://1drv.ms/u/c/801ce36c4ff3f93b/Eapc8wI7tqxOqmOPZ66uMG4BgeX8j7AewKq7NekCI0Al2w?e=NdenlL). (This may take some time, please wait patiently.) Then, create a directory my_env (we recommend creating it under `conda/envs/`) and extract the environment into this directory:

```shell
mkdir -p my_env
tar -xzf TAB.tar.gz -C my_env
```

#### 3. Activate the Environment

```shell
source my_env/bin/activate
```

#### 4. Clean Environment Prefix

You can clear the environment prefix using the following command. Now the environment is the same as one created directly with conda at this path.

```shell
(my_env) $ conda-unpack
```

### Data preparation

Prepare Data. You can obtained the well pre-processed datasets from [Google Drive](https://drive.google.com/file/d/1oHDHKCGMT_xkHhCI113bQ-4IzGnKPU3I/view?usp=drive_link). Then place the downloaded data under the folder `./dataset`.

### Train and evaluate model

We provide the experiment scripts for all benchmarks under the folder `./scripts/multivariate_detection`, and `./scripts/univariate_detection`. For example you can reproduce a experiment result as the following:

```shell
sh ./scripts/multivariate_detection/detect_label/MSL_script/ModernTCN.sh
```

## Contact

If you have any questions or suggestions, feel free to contact:

- Xiangfei Qiu (xfqiu@stu.ecnu.edu.cn)

<!-- ### Configure your Configuration File

  - Modify the corresponding config under the folder `./config/`.

  - Modify the contents in  `./scripts/run_benchmark.py/`.

  - **We strongly recommend using the pre-defined configurations in `./config/`. Create your own  configuration file only when you have a clear understanding of the configuration items.**

### Run it

```shell
python ./scripts/run_benchmark.py --config-path "rolling_forecast_config.json" --data-name-list "ILI.csv" --strategy-args '{"horizon":24}' --model-name "time_series_library.DLinear" --model-hyper-params '{"batch_size": 16, "d_ff": 512, "d_model": 256, "lr": 0.01, "horizon": 24, "seq_len": 104}' --adapter "transformer_adapter"  --gpus 0  --num-workers 1  --timeout 60000  --save-path "ILI/DLinear"
``` -->

<!-- ### Define you model or adapter class

The user-implemented model or adapter class should implement the following functions in order to adapt to this benchmark.

"required_hyper_params" function is optional，__repr__ functions is necessary.

**The function prototypes are as follows：**

- required_hyper_params  function:

  ```python
  """
  Return the hyperparameters required by the model
  This function is optional and static

  :return: A dictionary that represents the hyperparameters required by the model
  :rtype: dict
  """
  # For example
  @staticmethod
  def required_hyper_params() -> dict:
      """
      An empty dictionary indicating that model does not require
      additional hyperparameters.
      """
      return {}
  ```

- forecast_fit  function training model

  ```python
  """
  Train the model.

  :param train_data: Time series data used for training.
  :param train_ratio_in_tv: Represents the splitting ratio of the training
  set validation set. If it is equal to 1, it means that the validation
  set is not partitioned.
  """
  # For example
  def forecast_fit(self, train_data: pd.DataFrame, *, train_ratio_in_tv: float = 1.0, **kwargs) -> "ModelBase":
      pass
  ```

- forecast function utilizing the model for inference

  ```python
  """
  Use models for forecasting

  :param horizon: Predict length
  :type horizon: int
  :param series: Training data used to fit the model
  :type series: pd.DataFrame

  :return: Forecasting results
  :rtype: np.ndarray
  """
  # For example
  def forecast(self, horizon: int, series: pd.DataFrame, **kwargs) -> np.ndarray:
      pass
  ```
- __repr __ string representation of function model name

  ```python
  """
  Returns a string representation of the model name

  :return: Returns a string representation of the model name
  :rtype: str
  """
  # For example
  def __repr__(self) -> str:
      return self.model_name
  ``` -->
