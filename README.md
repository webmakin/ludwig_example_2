
* How to
1. create virtualenv - `mkvirtualenv ../venv`
2. install requirements - `pip install -r requirements.txt`
3. train the model
```
ludwig train \
--dataset bestsellers_with_categories.csv \
--config_file config.yaml
```
4. serve
```
python -m ludwig.serve --model_path ./results/experiment_run_2/model
```

5. predict
```
curl http://0.0.0.0:8000/predict -X POST -F 'Name=Wonder'
```
