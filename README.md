
  * How to
  ** create virtualenv - `mkvirtualenv ../venv`
  ** install requirements - `pip install -r requirements.txt`
  ** train the model
```  ludwig train \
--dataset bestsellers_with_categories.csv \
--config_file config.yaml
```
  ** serve
```
python -m ludwig.serve --model_path ./results/experiment_run_2/model
```

  ** predict
```
curl http://0.0.0.0:8000/predict -X POST -F 'Name=Wonder'
```
