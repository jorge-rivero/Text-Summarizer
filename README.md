# Text-Summarizer

## Workflow
1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. Update the components
6. Update the pipeline
7. Update the main.py
8. Update the app.py


## Error during training:
1. Updated the libraries:
```
pip install --upgrade accelerate
pip uninstall -y transformers accelerate
pip install transformers accelerate
```
2. Exported variables in Pycharm Venv terminal executed:
```
export PYTORCH_MPS_HIGH_WATERMARK_RATIO=0.0 
```
This one seems to solve the issue:
```
export COMMANDLINE_ARGS="--precision full --no-half --skip-torch-cuda-test" "--skip-torch-cuda-test --precision full --no-half --no-progressbar-hiding --opt-channelslast"
```
3. Ran the pipeline from the terminal instead than running it from Pycharm. 