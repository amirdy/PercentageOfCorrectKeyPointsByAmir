# Percentage Of CorrectKey Points Calculator
 A python project that calculates a metric called PercentageOfCorrectKeyPoints.


## Setup

To get started with this package, follow the steps below.


### 1. Install Dependencies

Install the required Python packages using `pip`:

```bash
pip install numpy
```

### 2. Install the Package
Install the Package using the command below:

```bash
pip install PercentageOfCorrectKeyPointsByAmir==0.1.1
```

## Usage

```python
from PercentageOfCorrectKeyPointsByAmir.PercentageOfCorrectKeyPoints import PercentageOfCorrectKeyPoints
'''
y_true: np.ndarary  # true heatmaps of a batch of data, of shape (batch_size, h, w, num_keypoints), with values in range(0, 1)
y_pred: np.ndarary  # predicted heatmaps of a batch of data, of shape (batch_size, h, w, num_keypoints), with values in range(0, 1)
'''
# a key-point will be assumed as correct, if predicted key-point is in a radial distance of (0.1 * image_height) pixels from true keypoint
metric = PercentageOfCorrectKeyPoints(relative_distance_threshold=0.1)
result = metric.apply(y_true, y_pred)
```
