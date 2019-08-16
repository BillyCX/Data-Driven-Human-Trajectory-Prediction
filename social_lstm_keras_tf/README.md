# social_lstm_keras_tf

Social LSTM implementation with Keras (and TensorFlow as backend)  

## Requirements

* Python 3.6.0+

## Usage

### 1. Preparation

Set `dataset` attribute of the config files in `configs/`. In other word, modifying the path in json file to the absolute path to dataset.

### 2. Training

Run `train_social_model.py`.
```
python train_social_model.py --config path/to/config.json [--out_root OUT_ROOT]

```
In my case,

```
python train_social_model.py  --config data/configs/***.json (***-dataset name) 

```

### 3. Testing

Run `evaluate_social_model.py`
```
python evaluate_social_model.py --trained_model_config /home/USRlab/Downloads/social_lstm_keras_tf-master/data/results/20190814192712/test=zara2/zara2.json --trained_model_file /home/USRlab/Downloads/social_lstm_keras_tf-master/data/results/20190814192712/test=zara2/social_train_model_e0010.h5
```
The files all are in data/result/.

## Restrictions

* work only on batch size = 1
* require much RAM (use almost all 16GB in my environment),therefore we could decrease the size of the dataset.

## References

* Alexandre Alahi, Kratarth Goel, Vignesh Ramanathan, Alexandre Robicquet, Li Fei-Fei, Silvio Savarese. **Social LSTM: Human Trajectory Prediction in Crowded Spaces**. The IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016, pp. 961-971
* My implementation based on: [Social LSTM using TensorFlow](https://github.com/vvanirudh/social-lstm-tf)
* Fork from [social_lstm_keras_tf](https://github.com/chetanchawla/social_lstm_keras_tf) 
