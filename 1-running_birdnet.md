# Using BirdNET 3.0

## Running the Detection Model

The detection model is run from the terminal (powershell). Below are some example commands to run. Copy and paste to the terminal prompt.  

**Simple example using the tensorflow model file**
```{powershell}
python birdnet-V3.0-dev/analyze.py audio_files/soundscape.wav --out-csv outputs/results.csv --export-embeddings true

python birdnet-V3.0-dev/analyze.py audio_files/soundscape.wav --model models/BirdNET+_V3.0-preview3.1_Global_11K_FP32.pt --export-embeddings true

```

**Using the FP16 ONNX model (recommended: smaller, same accuracy)** 
```{powershell}
python birdnet-V3.0-dev/analyze.py audio_files/soundscape.wav --model models/BirdNET+_V3.0-preview3.1_Global_11K_FP16_pruned.onnx
```

##Browser Interface
```{powershell}
uv run python -m streamlit run app.py
```
